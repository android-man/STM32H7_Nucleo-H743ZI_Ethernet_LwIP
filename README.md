# Nucleo-H743ZI + Ethernet + LwIP (without RTOS)
Working (tested) example of **LwIP** stack usage with static IP address **192.168.1.100** (/24).

Please, pay your attention to the lines below.

[STM32H743ZITx_FLASH.ld](/STM32H743ZITx_FLASH.ld):
- [#L35-L39](/STM32H743ZITx_FLASH.ld#L35-L39) : stack/heap size
- [#L134](/STM32H743ZITx_FLASH.ld#L134), [#L151](/STM32H743ZITx_FLASH.ld#L151), [#L162](/STM32H743ZITx_FLASH.ld#L162) : data/bss/heap location
- [#L166-L175](/STM32H743ZITx_FLASH.ld#L166-L175) : LwIP Rx/Tx data location

[main.c](/main.c):
- [#L133-L141](/main.c#L133-L141) : HAL_Delay() & MX_LWIP_Process() usage
- [#L237-L262](/main.c#L237-L262) : MPU configuration

[ethernetif.c](/Src/ethernetif.c):
- [#L189](/Src/ethernetif.c#L189), [#L196](/Src/ethernetif.c#L196), [#L203](/Src/ethernetif.c#L203), [#L210](/Src/ethernetif.c#L210) : Ethernet GPIOs speed
