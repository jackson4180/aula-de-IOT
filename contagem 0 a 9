#define A 12 //
#define B 13 // define o pino respectivo
#define C  7 // a cada led
#define D  8 //
#define E  9 //
#define F 11 //
#define G 10 //

#define QTD_SEG   7 //quantidade de leds
#define QTD_CHAR 10 //quantidade de dígitos

int seg[] = {A, B, C, D, E, F, G}; //vetor referente aos pinos
int contador; //usado para definir qual dígito será mostrado

bool num[][10] = { {1, 1, 1, 1, 1, 1, 0},   // mapeia
                   {0, 1, 1, 0, 0, 0, 0},   // cada
                   {1, 1, 0, 1, 1, 0, 1},   // dígito
                   {1, 1, 1, 1, 0, 0, 1},   // à respectiva
                   {0, 1, 1, 0, 0, 1, 1},   // combinação
                   {1, 0, 1, 1, 0, 1, 1},   // de leds
                   {1, 0, 1, 1, 1, 1, 1},   // acesos
                   {1, 1, 1, 0, 0, 0, 0},   //
                   {1, 1, 1, 1, 1, 1, 1},   //
                   {1, 1, 1, 1, 0, 1, 1} }; //
         
void setup() {
  contador = 0; //inicia o contador
  for(int i = 0; i < QTD_SEG; i ++)
    pinMode(seg[i], OUTPUT); //inicia os pinos
}

void loop() {
  for(int i = 0; i < QTD_SEG; i ++)
    digitalWrite(seg[i], num[contador][i]); //exibe os dígitos
  contador = contador == 9 ? 0 : contador + 1; //trata o contador
  delay(1000);
}
