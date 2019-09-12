# Ejercicio 2: Rifa Ethereum

## Objetivo

Crear uno (o varios) smart contracts en ethereum para simular una
rifa. La idea es que el smart contract tiene una llave publica
vara validad si un ticket de la rifa es valido o no. El emisor
de los tickets en un punto escoge un ganador aleatoreamente
de la rifa.

### Smart Contract

El smart contract correspondiente a la rifa debe tener (al menos) los
siguientes campos:

* Llave publica del creador de la rifa (implicito)
* Lista de participantes en la rifa
* Ganador de la rifa (vacio inicialmente, pero se selecionara)

### Emision de Ticket de Rifa

1. El creador de la rifa genera un numero aleatoreo
2. El creador de la rifa aplica su firma digital al numero
3. El creador distribuye el numero de rifa (firmado digitalmente) a un participante

### Participacion en la Rifa
1. El participante recibe un numero de rifa (firmado digitalmente)
2. El participante envia su numero de rifa como transaccion al smart contract
3. El smart contract verifica que el numero este firmado por el creador de la rifa
4. El smart contract verifica que el numero de rifa no haya sido utilizado
5. El smart contract registra al creador de la transaccion como participante en la rifa

### Seleccion de Ganador
1. El creador de la rifa envia una transaccion que inicia la seleccion del ganador
2. El smart contract genera un numero aleatoreo
3. El smart contract utiliza el numero aleatoreo para seleccionar al participante ganador y lo registra en el smart contract.


### Referencias
* https://ethereum.stackexchange.com/questions/710/how-can-i-verify-a-cryptographic-signature-that-was-produced-by-an-ethereum-addr/718#718