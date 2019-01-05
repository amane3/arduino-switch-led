/*
Input Serial for changing led functions.
*/

// the setup function runs once when you press reset or power the board
void* __dso_handle;

void setup() {
  pinMode(LED_BUILTIN, OUTPUT);
  analogWrite(LED_BUILTIN, 255);
  Serial.begin(9600);
}


void loop(){
int inputchar; 
inputchar = Serial.read();
 
  if(inputchar != -1 ){
   switch(inputchar){
      int i;
      case 'b':
        Serial.print("LED BLINK\n");
        for(i=0;i<256;i++){
          analogWrite(LED_BUILTIN, i);
          delay(3);
          }        
        for(i=255;i>=0;i--){
          analogWrite(LED_BUILTIN, i);
          delay(3);
          }
        break;
      case 'f':  
        Serial.print("LED OFF\n");
        analogWrite(LED_BUILTIN, 0);
        break;
      case 'o':
        Serial.print("LED ON\n");
        analogWrite(LED_BUILTIN, 255);
        break;
    }
  } else { 
    
  }
}
