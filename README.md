# 1-26-18-Robotics-Challenge

#pragma config(Sensor, dgtl1,  encoder,        sensorRotation)
#pragma config(Motor,  port2,           topLeft,       tmotorVex393_MC29, openLoop)
#pragma config(Motor,  port3,           bottomLeft,    tmotorVex393_MC29, openLoop)
#pragma config(Motor,  port4,           topRight,      tmotorVex393_MC29, openLoop)
#pragma config(Motor,  port5,           bottomRight,   tmotorVex393_MC29, openLoop)
//*!!Code automatically generated by 'ROBOTC' configuration wizard               !!*//

#define target SensorValue[encoder] - 1272


task main()
{

	float initialValue = SensorValue[encoder];

	while(true) {
		float error = target - SensorValue[encoder];

		if (SensorValue[encoder] == initialValue + 1272 ) {
			motor[port1] = 0.1 * error;
			motor[port2] = 0.1 * error;
			motor[port3] = 	0.1 * error;
			motor[port4] = 0.1 * error;
			} else if (Sensor ) {
			motor[port1] = 50;
			motor[port2] = 50;
			motor[port3] = 50;
			motor[port4] = 50;
		}

		else {
			motor[port1] = 127;
			motor[port2] = 127;
			motor[port3] = 127;
			motor[port4] = 127;
		}
	}
}
