/*
 * fsm.h
 *
 *  Created on: 27 thg 11, 2025
 *      Author: Thanh Phong
 */
#include "stdint.h"
#include <string.h>
#include "stm32f1xx_hal.h"  // Đảm bảo rằng thư viện HAL được bao gồm để sử dụng HAL_GetTick


#ifndef INC_FSM_H_
#define INC_FSM_H_

typedef enum {
	WAITING_FOR_COMMAND,
	PARSING_COMMAND,
	COMPLETED_COMMAND
} CommandParserState;

typedef enum {
	IDLE,
	SEND,
	STOP
} CommandCommunicationState;

#define  MAX_BUFFER_SIZE 20
extern uint8_t  buffer_index[MAX_BUFFER_SIZE];
extern uint8_t  indexbuff;
extern uint8_t  temp;
extern uint8_t  buffer_flag;
extern uint8_t  flag_send_fsm;
extern uint8_t  flag_stop_fsm;
extern uint32_t last_receive_time;
extern uint8_t  timeout_flag;

void command_parser_fsm();
void uart_communication_fsm();

#endif /* INC_FSM_H_ */
