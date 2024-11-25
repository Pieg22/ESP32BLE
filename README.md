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


