# Lab03-Bump-Course

/*
Program to make the robot navigate the obstacle course using 
the touch sensor 

Author: Dan

#pragma config(Sensor, S1,touchSensor,sensorTouch)

//code 

task main()
{

  //initialisation of i for the for loop 

  int i;
  
  //for loop to run the robot till touch sensor is activated.
  
	for(i=0; i<3; i++)
	{
	
	  //while loop to run the robot till the sensor is activated.
	
  	while(SensorValue(touchSensor) == 0)
  	{
    	motor[motorA] = 50;
    	motor[motorC] = 50;
  	}
  	
  	//makes the robot reverse when an object is hit.

  	motor[motorA] = -35;
 		motor[motorC] = -35;
 		wait1Msec(750);
 		
 		//Makes the robot turn to avoid the object

 		motor[motorA]=25;
		motor[motorC]=-25;
		wait1Msec(700);
		
		//End for loop
		
 	}
 	
 	//End main
 	
}
