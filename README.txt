移植时需修改：

在头文件重新定义motor-control.h下所使用的宏定义
#define RS485_RE_Pin GPIO_PIN_x
#define RS485_RE_GPIO_Port GPIOx
#define RS485_DE_Pin GPIO_PIN_x
#define RS485_DE_GPIO_Port GPIOx


修改GO-M8010-6.c
HAL_StatusTypeDef SERVO_Send_recv(MOTOR_send *pData, MOTOR_recv *rData)函数
所使用的串口&huartx

注意：需使能RS485-RE及RS485-DE所对应的引脚;需准备TTL转485模块
