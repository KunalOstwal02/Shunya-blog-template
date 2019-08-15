### IR Sensor GPIO

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

### Alcohol Sensor I2C

_Code:_

```
#include <stdio.h>
#include <stdlib.h>

#include <shunyaInterfaces.h>
#include <Wire.h>
#include <pcf8591.h>

int main(void)
{
	shunyaInterfacesSetup();
	pcf8591Setup();
	while(1) {
		int value;
		value = pcf8591Read(A1);
		printf("Alcohol Value is BAC %d\n",value);
	}
	return 0;
}
```


