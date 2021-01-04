
void step1() {

  digitalWrite(2, HIGH);
  digitalWrite(3, HIGH);
  digitalWrite(4, LOW);
  digitalWrite(5, LOW);

}

void step2() {

  digitalWrite(2, LOW);
  digitalWrite(3, HIGH);
  digitalWrite(4, HIGH);
  digitalWrite(5, LOW);

}

void step3() {

  digitalWrite(2, LOW);
  digitalWrite(3, LOW);
  digitalWrite(4, HIGH);
  digitalWrite(5, HIGH);

}

void step4() {

  digitalWrite(2, HIGH);
  digitalWrite(3, LOW);
  digitalWrite(4, LOW);
  digitalWrite(5, HIGH);

}




void step5() {

  digitalWrite(8, HIGH);
  digitalWrite(9, HIGH);
  digitalWrite(10, LOW);
  digitalWrite(11, LOW);

}

void step6() {

  digitalWrite(8, LOW);
  digitalWrite(9, HIGH);
  digitalWrite(10, HIGH);
  digitalWrite(11, LOW);

}

void step7() {

  digitalWrite(8, LOW);
  digitalWrite(9, LOW);
  digitalWrite(10, HIGH);
  digitalWrite(11, HIGH);

}

void step8() {

  digitalWrite(8, HIGH);
  digitalWrite(9, LOW);
  digitalWrite(10, LOW);
  digitalWrite(11, HIGH);

}





void setup() {
  Serial.begin(9600);

  pinMode(2, OUTPUT);
  pinMode(3, OUTPUT);
  pinMode(4, OUTPUT);
  pinMode(5, OUTPUT);

  pinMode(8, OUTPUT);
  pinMode(9, OUTPUT);
  pinMode(10, OUTPUT);
  pinMode(11, OUTPUT);

  digitalWrite(2, LOW);
  digitalWrite(3, LOW);
  digitalWrite(4, LOW);
  digitalWrite(5, LOW);

   digitalWrite(8, LOW);
  digitalWrite(9, LOW);
  digitalWrite(10, LOW);
  digitalWrite(11, LOW);

}




int pos = 0;// 1 - down , 2 - up 

float topposition = 1200; //estimativ 2000 de pasi 

float stepcounter = 0.0;

int i = 10; //2.5 //4 //10
int on = 0;








void loop() {

  /*if (on == 1){ //stop if going down and reaching 
  //if(digitalRead(2)==0)
  {
    on = 0;
    pos = 1;
    stepcounter = 0.0;
  }  
  }

  if(pos == 0) //initializarea
  {
    if(digitalRead(2) != 0)
    on = 1;
    else pos = 1;
  }*/

  //Serial.println(digitalRead(3)); //buton de start 1-free 0-pressed
  //Serial.println(digitalRead(2)); //end stopper 1-free 0-pressed

  if (Serial.available()) {

    char c = Serial.read();
    if (c == 'w')
      on = 2;
    if (c == 's')
      on = 1;
    if (c == 'x')
      on = 0;
     if (c == 'd')
      on = 3;
     if (c == 'a')
      on = 4;

  }

  if (on == 1) { //go backward
    i = 4;

    
    step1();
    step5();
    delay(i);
    step2();
    step6();
    delay(i);
    step3();
    step7();
    delay(i);
    step4();
    step8();
    delay(i);

    stepcounter = stepcounter - 0.1;
    
  }

  else if (on == 3) { //go left
    i = 4;

    
    step1();
    step8();
    delay(i);
    step2();
    step7();
    delay(i);
    step3();
    step6();
    delay(i);
    step4();
    step5();
    delay(i);

    //stepcounter = stepcounter - 0.1;
    
  }

  else if (on == 4) { //go right

    i = 4;
    
    step4();
    step5();
    delay(i);
    step3();
    step6();
    delay(i);
    step2();
    step7();
    delay(i);
    step1();
    step8();
    delay(i);

    //stepcounter = stepcounter + 0.1;
  }
  
  else if (on == 2) { //go forward

    i = 2.5;
    
    step4();
    step8();
    delay(i);
    step3();
    step7();
    delay(i);
    step2();
    step6();
    delay(i);
    step1();
    step5();
    delay(i);

    stepcounter = stepcounter + 0.1;
  }
  
  else{

    
    digitalWrite(2, LOW);
    digitalWrite(3, LOW);
    digitalWrite(4, LOW);
    digitalWrite(5, LOW);

    digitalWrite(8, LOW);
    digitalWrite(9, LOW);
    digitalWrite(10, LOW);
    digitalWrite(11, LOW);

    //Serial.print("stepcounter: ");
    //Serial.println(stepcounter);

    delay(100);

  }


}
