# Esp32 RNG

```c++
void setup()
{
  //Inicia el puerto serial
  Serial.begin(115200);
}

void loop()
{
  //Obtiene un numero aleatorio y lo almacena en una variable
  uint32_t NumAleatorio = esp_random(); 
  
  //Se guarda en uint32_t porque es el valor que retorna
  
  //Imprime el numero aleatorio
  Serial.print("Numero Aleatorio: ");
  Serial.println(NumAleatorio);

  //Retardo de dos segundos
  delay(2000);
}
```

### Debug
<img src="https://github.com/IDiegoUlises/Esp32-RNG/blob/main/Imagenes/Numeros-Aleatorios.png" />

* **Para obtener numeros aleatorios debe estar funcionando el WiFi o el Bluetooth:** Porque utiliza la entropia del hardware del Esp32 que generan las ondas electromagneticas para obtener numeros aleatorios, en caso que el WiFi y el Blueooth se encuentren deshabilitado el Esp32 no podra generar numeros aleatorios por lo que se generaran numeros pseudoaleatorios
