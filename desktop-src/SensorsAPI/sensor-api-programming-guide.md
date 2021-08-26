---
description: En esta sección se proporciona información, incluido el código de ejemplo, sobre cómo usar las características de Sensor API. Para obtener información general sobre las distintas interfaces de programación, consulte Acerca de sensor API.
ms.assetid: 4c2ffd22-49ee-4318-bfa0-e0ce4d8c67bb
title: Guía de programación de Sensor API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5886564e66a0a8db64713b280b44f85a197430dc23523266bc45e66e44c956b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073245"
---
# <a name="sensor-api-programming-guide"></a>Guía de programación de Sensor API

En esta sección se proporciona información, incluido el código de ejemplo, sobre cómo usar las características de Sensor API. Para obtener información general sobre las distintas interfaces de programación, consulte [Acerca de sensor API.](about-the-sensor-api.md)

El código de ejemplo de esta sección usa los siguientes encabezados incluidos adicionales.


```C++
#include <windows.h>
#include <initguid.h>
#include <propkeydef.h>


#include <iostream>
#include <propvarutil.h>
#include <functiondiscoverykeys.h>
#include <assert.h>
```





También debe vincular a estos archivos de biblioteca asociados adicionales: Propsys.lib y PortableDeviceGuids.lib.

El código de ejemplo de esta sección usa las siguientes constantes para categorías de sensores, tipos y campos de datos. Estas constantes son valores personalizados definidos por el ejemplo de controlador TimeSensor en el Windows Driver Kit. Tenga en cuenta que, aunque la plataforma sensor permite definir y usar tipos personalizados como estos, debe usar tipos definidos por la plataforma siempre que sea posible.


```C++
// Define an object ID.
// {0D77BEE3-7169-42bf-8379-28F9A9B59A57}
DEFINE_GUID(SAMPLE_SENSOR_TIME_ID, 
0xd77bee3, 0x7169, 0x42bf, 0x83, 0x79, 0x28, 0xf9, 0xa9, 0xb5, 0x9a, 0x57);

// Define a custom category.
// {062A5C3B-44C1-4ad1-8EFC-0F65B2E4AD48}
DEFINE_GUID(SAMPLE_SENSOR_CATEGORY_DATE_TIME, 
0x62a5c3b, 0x44c1, 0x4ad1, 0x8e, 0xfc, 0xf, 0x65, 0xb2, 0xe4, 0xad, 0x48);

// Define a custom type.
// {5F199A84-409F-4e35-B2DD-F9C79F5318A0}
DEFINE_GUID(SAMPLE_SENSOR_TYPE_TIME, 
0x5f199a84, 0x409f, 0x4e35, 0xb2, 0xdd, 0xf9, 0xc7, 0x9f, 0x53, 0x18, 0xa0);

// Time sensor fields.
// Because these are related, each field uses the same GUID, but changes the PID.
// {340946F2-9A77-42b0-8176-57D4DF00E5CA}
DEFINE_PROPERTYKEY(SAMPLE_SENSOR_DATA_TYPE_HOUR, 
0x340946f2, 0x9a77, 0x42b0, 0x81, 0x76, 0x57, 0xd4, 0xdf, 0x0, 0xe5, 0xca, PID_FIRST_USABLE); // PID = 2

DEFINE_PROPERTYKEY(SAMPLE_SENSOR_DATA_TYPE_MINUTE, 
0x340946f2, 0x9a77, 0x42b0, 0x81, 0x76, 0x57, 0xd4, 0xdf, 0x0, 0xe5, 0xca, PID_FIRST_USABLE + 1); // PID = 3

DEFINE_PROPERTYKEY(SAMPLE_SENSOR_DATA_TYPE_SECOND, 
0x340946f2, 0x9a77, 0x42b0, 0x81, 0x76, 0x57, 0xd4, 0xdf, 0x0, 0xe5, 0xca, PID_FIRST_USABLE + 2); // PID = 4
```



El código de ejemplo de esta sección usa las siguientes variables.


```C++
HRESULT hr = S_OK;

// Sensor interface pointers
ISensorManager* pSensorManager = NULL;    
ISensorCollection* pSensorColl = NULL;
ISensor* pSensor = NULL; 
ISensorDataReport* pReport = NULL;

// Time sensor data field variables
ULONG ulHour, ulMinute, ulSecond = 0;

```



El código de ejemplo de esta sección usa la siguiente función para liberar punteros de interfaz COM.


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



## <a name="in-this-section"></a>En esta sección

-   [Recuperar un objeto sensor](retrieving-a-sensor.md)
-   [Solicitud de permisos de usuario](requesting-user-permissions.md)
-   [Recuperar y establecer propiedades del sensor](setting-and-retrieving-sensor-properties.md)
-   [Comprobación de los campos de datos de sensor admitidos](checking-for-supported-sensor-data-fields.md)
-   [Uso de eventos de SENSOR API](using-sensor-api-events.md)
-   [Recuperación de valores de datos del sensor](retrieving-sensor-data-fields.md)
-   [Recuperar tipos de vectores](retrieving-vector-types.md)
-   [Uso de sensores lógicos](using-logical-sensors.md)
-   [Creación de Light-Aware interfaces de usuario](creating-light-aware-user-interfaces.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Sensor API](about-the-sensor-api.md)
</dt> </dl>

 

 



