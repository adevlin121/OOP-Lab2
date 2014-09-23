OOP-Lab2
========
int x = 100;
int y = 100;
int gov = 30;
int goh = 30;
int dia = 50;
int i,j,k,l,m = 0;
int count = 0;

void setup()
{
  size(1600,1000);
}

void draw()
{
  background(random(0,255), random(0,255), random(0,255));
  stroke(random(0,255), random(0,255), random(0,255));
  fill(i, j, k);
  if(count<255)
  {
    i++;
    count++;
  }
  else if(count >=255 && count < 510)
  {
    j++;
    i--;
    count++;
  }
  else if(count >=510 && count <765)
  {
    j--;
    k++;
    count++;
  }
  else
  {
    i=0;
    j=0;
    k=0;
    count = 0;
  }
  smooth();
  ellipse(x, y, dia, dia);
  x = x+goh;
  y = y+gov;
  
  if(x > width-(dia/2) || x < 0+(dia/2))
  {
    goh = goh * -1;
  }
  
  if(y > (height-(dia/2)) || y < 0+(dia/2))
  {
    gov = gov * -1;
  }
  
}
