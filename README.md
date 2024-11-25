# ESP32BLE
//I'm trying to use ESP32 like scan BLE . 

//First problem : Compilation error: 'init' is not a member of 'BLEDevice' 

//We change the terms with libraries  , from this : 

#include <BLE2902.h>
#include <BLEDevice.h>
#include <BLEUtils.h>
#include <BLEServer.h>

//to this : 

#include <BLE2902.h>
#include <BLEDevice.h>
#include <BLEUtils.h>
#include <BLEServer.h>

//All code of the test : 

#include <BLE2902.h>
#include <BLEDevice.h>
#include <BLEUtils.h>
#include <BLEServer.h>

int scanTime = 5; // Tiempo de escaneo en segundos

void setup() {
  Serial.begin(115200);
  Serial.println("Iniciando escaneo BLE...");
  BLEDevice::init("");
  BLEScan* pBLEScan = BLEDevice::getScan();
  pBLEScan->setActiveScan(true);
  BLEScanResults scanResults = pBLEScan->start(scanTime);
  Serial.printf("Se encontraron %d dispositivos\n", scanResults.getCount());
}


