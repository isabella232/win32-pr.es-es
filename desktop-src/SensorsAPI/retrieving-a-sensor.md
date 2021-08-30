---
description: Para recuperar un objeto de sensor, use la interfaz ISensorManager. Puede pensar en esta interfaz como la interfaz raíz de sensor API. Para usar ISensorManager, primero debe llamar al método COM CoCreateInstance.
ms.assetid: 36631bae-f237-4951-9959-6ab6286bd1f7
title: Recuperar un objeto sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 985829572476dd46fc235229c43b9d11585e0e0d62a3e8d805aa7cf8fd566601
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126645"
---
# <a name="retrieving-a-sensor-object"></a>Recuperar un objeto sensor

Para recuperar un objeto de sensor, use la [**interfaz ISensorManager.**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager) Puede pensar en esta interfaz como la interfaz raíz de sensor API. Para usar **ISensorManager,** primero debe llamar al método COM **CoCreateInstance.**

El código de ejemplo siguiente crea una instancia del administrador de sensores.


```C++
// Create the sensor manager.
hr = CoCreateInstance(CLSID_SensorManager, 
                        NULL, CLSCTX_INPROC_SERVER,
                        IID_PPV_ARGS(&pSensorManager));

if(hr == HRESULT_FROM_WIN32(ERROR_ACCESS_DISABLED_BY_POLICY))
{
    // Unable to retrieve sensor manager due to 
    // group policy settings. Alert the user.
}
```



Después de recuperar correctamente un puntero a [**ISensorManager,**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager)puede recuperar sensores por categoría, tipo o identificador. Si recupera sensores por tipo o categoría, recibirá un puntero a una interfaz [**ISensorCollection**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorcollection) que contiene todos los sensores disponibles que pertenecen a la categoría o tipo solicitados. Si recupera un sensor por su identificador, recibirá un puntero a una interfaz [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) que representa el sensor único que solicitó.

El código de ejemplo siguiente recupera una colección de sensores que pertenecen a la categoría denominada SAMPLE \_ SENSOR \_ CATEGORY DATE \_ \_ TIME. A continuación, el código recupera el primer sensor de la colección por su índice.


```C++
// Get the sensor collection.
hr = pSensorManager->GetSensorsByCategory(SAMPLE_SENSOR_CATEGORY_DATE_TIME, &pSensorColl);
  
if(SUCCEEDED(hr))
{
    ULONG ulCount = 0;

    // Verify that the collection contains
    // at least one sensor.
    hr = pSensorColl->GetCount(&ulCount);

    if(SUCCEEDED(hr))
    {
        if(ulCount < 1)
        {
            wprintf_s(L"\nNo sensors of the requested category.\n");
            hr = E_UNEXPECTED;
        }
    }
}

if(SUCCEEDED(hr))
{
    // Get the first available sensor.
    hr = pSensorColl->GetAt(0, &pSensor);
}
```



Tenga en cuenta que puede recuperar todos los sensores disponibles mediante SENSOR \_ CATEGORY \_ ALL.

De forma similar, puede recuperar sensores de un tipo determinado.

El código de ejemplo siguiente recupera una colección de sensores del tipo denominado SAMPLE \_ SENSOR \_ TYPE \_ TIME. A continuación, el código recupera el primer sensor de la colección por su índice.


```C++
// Get the sensor collection.
hr = pSensorManager->GetSensorsByType(SAMPLE_SENSOR_TYPE_TIME, &pSensorColl);
  
if(SUCCEEDED(hr))
{
    ULONG ulCount = 0;

    // Verify that the collection contains
    // at least one sensor.
    hr = pSensorColl->GetCount(&ulCount);

    if(SUCCEEDED(hr))
    {
        if(ulCount < 1)
        {
            wprintf_s(L"\nNo sensors of the requested type.\n");
            hr = E_UNEXPECTED;
        }
    }
}

if(SUCCEEDED(hr))
{
    // Get the first available sensor.
    hr = pSensorColl->GetAt(0, &pSensor);
}
```



Para recuperar un sensor por su identificador, debe conocer el identificador único del sensor. Normalmente, los sensores generan este identificador cuando se conectan por primera vez para permitirle identificar varios sensores de la misma make y model. Esto significa que probablemente no conocerá el identificador del sensor de antemano. Sin embargo, si ha almacenado una copia de un identificador de sensor determinado que recuperó anteriormente, por ejemplo mediante una llamada a [**ISensor::GetID,**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getid)puede que desee recuperar de nuevo el mismo sensor.

En el código de ejemplo siguiente se muestra cómo recuperar un sensor mediante su identificador.


```C++
ISensor* pSensor = NULL;

// Get the sensor collection.
hr = pSensorManager->GetSensorByID(SAMPLE_SENSOR_TIME_ID, &pSensor);

```



También puede recuperar sensores cuando estén disponibles recibiendo un evento del administrador de sensores. Para obtener más información, [**vea ISensorManager::SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ISensorManagerEvents::OnSensorEnter**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanagerevents-onsensorenter)
</dt> </dl>

 

 
