# Shift Register Arduino

<p align="center">Biblioteca para facilitar o uso de shift registers como o 74HC595 no arduino como expansor de I/O's. </p>

# Funcionalidades
- Controlar cada pino individualmente: setPin(pin, LOW/HIGH)
- Obter o estado atual de cada pino individualmente: getPinValue(pin)
- Inverter o estado atual de cada pino individualmente: invertPin(pin)
- Controlar todos os pinos de uma vez: setAllTO(LOW/HIGH), setAllPins(0b00000001)
- Definir o brilho do conjunto geral: setBrightness(0-255)
- Utiliza��o de v�rios Shift Registers no mesmo circuito

# Instanciando a classe

Atualmente a classe possui 5 par�metros: dataPin, latchPin, clockPin, oePin e numSr. Sendo os 3 primeiros obrigar�rios.

O par�metro oePin precisa ser definido apenas caso a fun��o setBrithness seja usada.
- sr shiftregister(pin2, pin3, pin4, pin5)

O par�metro numSr precisa ser definido apenas quando mais de um shift register esteja sendo usado.
- sr shiftregister(pin2, pin3, pin4, NULL, 2)
- sr shiftregister(pin2, pin3, pin4, pin5, 2)

Obs: Caso a fun��o setBrithness n�o esteja sendo usada, o pino OE do shift register deve estar conectado ao terra.