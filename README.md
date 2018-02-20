# esp8266-uart
Classic UART usage for ESP
Using UART0 for serial communication in classic style.

Send byetes when nesseray, receive when its ready. Check availabe bytes in the reciver buffer

//init uarts 0 and 1 with corresponded baud rate

void ICACHE_FLASH_ATTR uart_init(UartBautRate uart0_br, UartBautRate uart1_br);

//set uart receive callback

void ICACHE_FLASH_ATTR set_uart_cb(tuart_cb *uart_cb);

//read byte from the uart0. return -1 if buffer empty

int ICACHE_FLASH_ATTR uart_rx_one_char();

//available bytes in the uart0 receiver

int ICACHE_FLASH_ATTR uart_rx_avail();

//for send data to uart0 use uart_tx_one_char(char c);
//use uart0 to transfer buffer

void ICACHE_FLASH_ATTR uart_tx_buffer(uint8 *buf, uint16 len);

void ICACHE_FLASH_ATTR clear_uart0(void);

STATUS ICACHE_FLASH_ATTR uart0_tx_one_char(uint8 TxChar);
