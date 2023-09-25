const int mleft1=8;
 const int mleft2=9;
 const int mright1=10;
 const int mright2=11;
 const int sensleft=6;
 const int sensright=7; 
 int templeft=0;
 int tempright=0;
void setup() 
{
  pinMode (mleft1,OUTPUT);
  pinMode (mleft2,OUTPUT);
  pinMode (mright1,OUTPUT);
  pinMode (mright2,OUTPUT);
  pinMode (sensright,INPUT);
  pinMode (sensleft,INPUT);
}

void loop() 
{
templeft=digitalRead(sensleft);
tempright=digitalRead(sensright);
 if (templeft == HIGH && tempright == HIGH)  
 {
      digitalWrite (mleft1,HIGH);   
      digitalWrite (mleft2,LOW);  
      digitalWrite (mright1,HIGH);
      digitalWrite (mright2,LOW);
   
 }
 else if (templeft == HIGH && tempright == LOW)  
{
      digitalWrite (mleft1,HIGH);
      digitalWrite (mleft2,HIGH);  
      digitalWrite (mright1,HIGH); 
      digitalWrite (mright2,LOW);
  
}
else if (templeft == LOW && tempright == HIGH) 
{
    digitalWrite (mleft1,HIGH); 
    digitalWrite (mleft2,LOW);  
    digitalWrite (mright1,LOW);
    digitalWrite (mright2,LOW);
 
}
else
{
    digitalWrite (mleft1,LOW);  
    digitalWrite (mleft2,LOW);  
    digitalWrite (mright1,LOW);
    digitalWrite (mright2,LOW);

} 
}
