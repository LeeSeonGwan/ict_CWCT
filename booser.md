const int time = 100;

const int waiting = 100;

int k=0;



void setup()

{

  pinMode(4, OUTPUT);

  pinMode(5, OUTPUT);

  pinMode(6, OUTPUT);

  pinMode(7, OUTPUT);

}



void loop()

{

  for(int v=0; v<4; v++){

​    if(v==0){

​      //부저, PIN4

​      k=4;

​    morse_s();

   morse_o();

​    morse_s();

​      k=0;

​    }

​    if(v==1){

​       k=5;

​    morse_s();

   morse_o();

​    morse_s();

​      k=0;

​      //LED 빨강, PIN5

​    }

​    if(v==2){

​       k=6;

​    morse_s();

   morse_o();

​    morse_s();

​      k=0;

​      //LED 노랑, PIN6

​    }

​    if(v==3){

​      k=7;

​    morse_s();

   morse_o();

​    morse_s();

​      k=0;

​      //LED 초록, PIN7

​    }

  }

  delay(300);





}





void dot()

{

  digitalWrite(k,HIGH);

  delay(time);

  digitalWrite(k,LOW);

  delay(waiting);

}





void bar()

{

  digitalWrite(k,HIGH);

  delay(3*time);

  digitalWrite(k,LOW);

  delay(waiting);

}



void morse_s()

{

  dot();

  dot();

  dot();

}



void morse_o()

{

  bar();

  bar();

  bar();

}



void morse_l()

{

  dot();

  bar();

  dot();

  dot();

}



void morse_e()

{

  dot();

}



void morse_t()

{

  bar();

}



void morse_a(){

  dot();

  bar();

}



void morse_k(){

  bar();

  dot();

  bar();

}



void morse_g()

{

  bar();

  bar();

  dot();

}



void morse_i(){

  dot();

  dot();

}