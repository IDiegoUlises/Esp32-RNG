# Esp32-RNG

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
* **Para crear una numero aleatorio debe estar funcionando el WiFi o el Bluetooth:** Porque utiliza la entropia del hardware del Esp32 que generan las ondas electromagneticas para obtener numeros verdaderamente aleatorio, en caso que el WiFi y el Blueooth se encuentran deshabilitado el Esp32 no podra generar numeros verdaderamente aleatorio por lo tanto se generaran numeros pseudoaleatorio 
  
