# Sensado de calidad de aire/ambiente (IEQ)

El objetivo de este projecto es crear un simple PCB con solo las conexiones para un puerto I2C (SDA, SCL, 3V3 y GND) y que permita medir las variables necesarias para estimar la calidad del aire indoor.


## Variables a medir

Se considero que las variables importantes a tener en cuenta son:
- Temperatura.
- Humedad.
- VOCs (son particulas comunmente relacionadas a la cocina, cualquier spray y respiracion humana).
- NOx (NO y NO2 relacionados a la combustion que suelen concentrarse si hay una mala ventilacion).

Se podrian haber incluido tambien un sensor que mida temperatura de la iluminacion o medicion de intensidad luminica, pero ambas variables son menos relevantes y por lo tanto se las descarto.

## Sensores

Como el objetivo es tener una conexion simple con I2C, se busco incorporar sensores unicamente que utilizen este protocolo y que se alimenten con 3V3. Por lo tanto se eligieron los siguientes componentes:

- `SHT3x-DIS`: Temperatura y humedad.
- `BMP280`: Presión.
- `SGP41`: Concentración de VOCs y NOx.

Los eleccion no solo fue porque cumplen las condiciones mencionadas, sino que ademas estoy familiarizado con los primeros dos sensores. Por otro lado el SGP41 es de Sensirion que tambien produce el SHT3x y posee un datasheet similar a este.
