int state; 
void setup() { 
pinMode(2,OUTPUT); 
pinMode(3,OUTPUT); 
pinMode(4,OUTPUT); 
pinMode(5,OUTPUT); 
Serial.begin(9600); 
} 
void loop() { 
  if(Serial.available() > 0){      
      state = Serial.read(); 
      Serial.println(state);  
    if(state == 70){ 
    f(); 
} 
   if(state == 83){ 
    s(); 
} 
    if(state == 66){ 
    b(); 
  } 
    if(state == 82){ 
    l(); 
  } 
    if(state == 76){ 
    r(); 
  } 
  if(state == 73){ 
    fl(); 
  }   
  if(state == 71){ 
    fr(); 
  }     
} 
} 
void f(){ 
    analogWrite(2,130); 
    analogWrite(3,0); 
    analogWrite(4,130); 
    analogWrite(5,0); 
} 
void s(){ 
  analogWrite(2,0); 
  analogWrite(3,0); 
  analogWrite(4,0); 
  analogWrite(5,0); 
} 
void b(){ 
    analogWrite(2,0); 
    analogWrite(3,160); 
    analogWrite(4,0); 
    analogWrite(5,150); 
} 
void l(){ 
    analogWrite(2,130); 
    analogWrite(3,0); 
    analogWrite(4,0); 
    analogWrite(5,130); 
} 
void r(){ 
    analogWrite(2,0); 
    analogWrite(3,130); 
    analogWrite(4,130); 
    analogWrite(5,0); 
} 
void fr(){ 
    analogWrite(2,0); 
    analogWrite(3,0); 
    analogWrite(4,130); 
    analogWrite(5,0); 
} 
void fl(){ 
    analogWrite(2,130); 
    analogWrite(3,0); 
    analogWrite(4,0); 
    analogWrite(5,0); 
} 
