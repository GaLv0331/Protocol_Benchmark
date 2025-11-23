# Protocol_Benchmark
Comparing UART, SPI and I2C between different architechtures.

Test Parameters:

            1] Throughput            : The amount of data that can be transfered in given amount of time. 
            2] Latency               : The delay between sending data and the receiver actually getting it.
            3] Packet Integrity      : The packets arrived at receiver without corruption. 
            4] CPU Load              : The amount of time CPU has spend to handle the communication.
            5] Stress Test           : Communicating with maximum baudrate, minimum packet delay and continuous transfer.

Boards Used:

            1] STM32F407VGT6         (ARM)           
            3] ESP32-WROOM-32        (Xtensa)
            
Packet Inforamtion:

            Packet Size: 1KB, 10KB, 100KB
            Packet Format: [start of frame | length of frame | payload |   crc32   | end of frame]
                           [      2bytes   |        2bytes   | X bytes |  4 bytes  |    2 bytes  ]
            
