readme.txt
==========

This project demonstrates FreeRTOS on the FRDM-K20D50M board. The FreeRTOS port has been generated by Processor Expert.
Change the FreeRTOSConfig.h to your needs.

How to use the FreeRTOS port in a new CodeWarrior project:
- Create a new project for your device with the CodeWarrior New Project wizard.
- Add the FreeRTOS folder with all files to your project
- Add the FreeRTOS folder to the search/include path of your assembler and compiler
- Change the following RTOS interrupt handlers in your vector table (Project_Settings\Startup_Code\kinetis_sysinit.c):
    /*SVC_Handler*/ vPortSVCHandler,
    ...
    /*PendSV_Handler*/ vPortPendSVHandler,
    /*SysTick_Handler*/vPortTickHandler,
- Include
  #include "FreeRTOS.h"
  in kinetis_sysinit.c
- Have fun :-)
