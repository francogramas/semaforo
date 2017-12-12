# semaforo
Problema del semforo
#define verde1 P1_6
#define naranja1 P1_1
#define rojo1 P1_2
#define verde2 P1_3
#define naranja2 P1_4
#define rojo2 P1_5
#define boton1 P1_3
#define boton2 P2_1
#define boton3 P2_2


byte ban1=0;
byte ban2=0;
byte ban3=0;

void setup() {
  pinMode(verde1, OUTPUT);
  pinMode(naranja1, OUTPUT);
  pinMode(rojo1, OUTPUT);
  pinMode(verde2, OUTPUT);
  pinMode(naranja2, OUTPUT);
  pinMode(rojo2, OUTPUT);
  pinMode(boton1, INPUT_PULLUP);
  pinMode(boton2, INPUT_PULLUP);
  pinMode(boton3, INPUT_PULLUP);
}

void loop() {
  if(digitalRead(boton1)==0){
      if(ban1==0){
          ban1=1;
        }
        else{
          ban1=0;  
        }
      digitalWrite(verde1,ban1);
      delay(1000);
    }

   
}

void apagar(){
  digitalWrite(verde1,0);
  digitalWrite(verde2,0);
  digitalWrite(naranja1,0);
  digitalWrite(naranja2,0);
  digitalWrite(rojo1,0);
  digitalWrite(rojo2,0);  
}
