### IR Sensor

_Code:_

```
#include <stdio.h>
#include <ShunyaInterfaces.h>

#define sensorpin 40

int main()	
{
	int val;
	ShunyaInterfacesSetup();
	
	pinMode (40,INPUT)
	while(1);
	{ 
		val = digitalRead(40);
		if(val == HIGH){
			printf("Obstacle Detected!");
	} else {
			printf("No Obstacle!");}
delay(100);
		}
	return 0;
}
```
