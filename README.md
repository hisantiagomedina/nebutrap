# Libreria `nebutrap`

La libreria `nebutrap` maneja la interacción con el módulo HX711 para medir el peso y volumen de agua. Esta libreria incluye métodos para inicializar el sensor, obtener lecturas, y encender o apagar el módulo.

## Métodos

### `void isnebutrap(int Datapin, int SCKpin, String objname)`

Inicializa el objeto tipo `nebutrap` configurando los pines de datos y reloj del módulo HX711 y asigna un nombre al objeto.

**Parámetros:**
- `Datapin`: El pin de datos (DT) del módulo HX711.
- `SCKpin`: El pin de reloj (SCK) del módulo HX711.
- `objname`: Nombre del objeto `nebutrap`.

**Uso:**
```cpp
nebutrap trap;
trap.isnebutrap(3, 2, "WaterTrap");
```

### `void on()` y `void off()`

Enciende y apaga respectivamente los pines definidos para el objeto tipo `nebutrap`.
**Uso:**
```cpp
Trampa.on();
Trampa.getWV();
Trampa.off();
```

### `void reset()`

Reinicia el objeto tipo `nebutrap`, configurando la recolección de agua a cero, apagando y encendiendo el módulo HX711, y recalibra el sensor.
**Uso:**
```cpp
trap.reset();
```

### `double getWW()`

Retorna el peso del agua recolectada en gramos
**Uso:**
```cpp
double waterWeight = trap.getWW();
Serial.println(waterWight);
```

### `double getWV()`

Retorna el peso del agua recolectada en gramos
**Uso:**
```cpp
double waterVolume = trap.getWV();
Serial.println(waterVolume);
```

