# AVR-Lib
C++ header only libraries optimized for avr 


## Display.h
<br>

  this header file is a alpha numeric Lcd Driver Based on Hitachi HD44780 LCD controller
  
  usage sample : 
  ```C++
  #include "AVR_Lib/Display.h"
  #include <util/delay.h>
  ............................
  ............................
  ............................
  	Display::LCD_Init();
	Display::LCD_setCursor(0,0);//goto 0,0
	Display::LCD_Disp("AVR_Lib");
	Display::LCD_setCursor(0,1);//goto next line
	Display::LCD_Disp("Test");
	
	_delay_ms(5000);
	Display::ResetDisplay();
  ```
## Keypad.h

<br>  

  this header file is a 4*4 keypad Driver with both normal and pullup input capture implemented
  
  usage sample : 
  ```C++
  #include "AVR_Lib/Keypad.h"
  ............................
  ............................
  ............................
  while (true)
	{
		
		inputs inp=Keypad::CapturePullupInput();
		
		//if some input captured prevent Debunce
		if (inp!=inputs::End)
		{
			_delay_ms(350);
		}
		
		switch(inp){
			
			case inputs::zero:
			
			break;
			case inputs::one:
			
			break;
			case inputs::two:
			
			break;
			case inputs::three:
			
			break;
			case inputs::four:
			
			break;
			case inputs::five:
			
			break;
			case inputs::six:
			
			break;
			case inputs::seven:
      
			break;
			case inputs::eight:
      
			break;
			case inputs::nine:
			
			break;
			case inputs::Dot:
			
			break;
			case inputs::plus:
			
			break;
			case inputs::minus:
			
			break;
			case inputs::devision:
			
			break;
			case inputs::multiply:
			
			break;
			case inputs::Evaluate:
     			 // = is pressed
			break;
			
			case inputs::End:
			//no input do noting
			break;
			
		}
		
		
	}
  ```
