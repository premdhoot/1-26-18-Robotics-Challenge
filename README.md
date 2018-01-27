#pragma config(Sensor, dgtl1, encoder, sensorRotation) 
#pragma config(Motor, port2, topLeft , tmotorVex393_MC29, openLoop) 
#pragma config(Motor, port3, bottomLeft, tmotorVex393_MC29, openLoop) 
#pragma config(Motor, port4, topRight, tmotorVex393_MC29, openLoop) 
#pragma config(Motor, port5, bottomRight, tmotorVex393_MC29, openLoop) 
//!!Code automatically generated by 'ROBOTC' configuration wizard !!//

#define target 1579

task main() {

float min = target - 5;
float max = target + 5;
SensorValue[encoder] = 0;
while(true) {
	float error = target - SensorValue[encoder];
	if ((SensorValue[encoder] > min)  & (SensorValue[encoder] < max)  )
	{
		motor[topLeft] = 0 * error;
		motor[bottomLeft] = 0 * error;
		motor[port3] = 	0 * error;
		motor[port4] = 0 * error;
	}
	else {
		motor[topLeft] = 0.1 * error;
		motor[bottomLeft] = 0.1 * error;
		motor[port3] = 	0.1 * error;
		motor[port4] = 0.1 * error;
	}
}
}
