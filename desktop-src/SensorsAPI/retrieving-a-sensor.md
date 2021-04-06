---
description: Para recuperar un objeto de sensor, se usa la interfaz ISensorManager. Esta interfaz se puede considerar como la interfaz raíz de la API del sensor. Para usar ISensorManager, debe llamar primero al método COM CoCreateInstance.
ms.assetid: 36631bae-f237-4951-9959-6ab6286bd1f7
title: Recuperación de un objeto de sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cda6ea04d1a0580c38aef5a0b9c4186b908300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001036"
---
# <a name="retrieving-a-sensor-object"></a>Recuperación de un objeto de sensor

Para recuperar un objeto de sensor, se usa la interfaz [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager) . Esta interfaz se puede considerar como la interfaz raíz de la API del sensor. Para usar **ISensorManager**, debe llamar primero al método com **CoCreateInstance** .

En el código de ejemplo siguiente se crea una instancia del administrador del sensor.


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



Después de recuperar correctamente un puntero a [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager), puede recuperar los sensores por categoría, tipo o identificador. Si recupera sensores por tipo o categoría, recibirá un puntero a una interfaz [**ISensorCollection**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorcollection) que contiene todos los sensores disponibles que pertenecen a la categoría o tipo solicitado. Si recupera un sensor por su identificador, recibirá un puntero a una interfaz [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) que representa el sensor único que solicitó.

En el ejemplo de código siguiente se recupera una colección de sensores que pertenecen a la categoría denominada SAMPLE \_ sensor \_ Category \_ Date \_ Time. A continuación, el código recupera el primer sensor de la colección por su índice.


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



Tenga en cuenta que puede recuperar todos los sensores disponibles mediante categoría de \_ sensor \_ ALL.

De forma similar, puede recuperar sensores de un tipo determinado.

En el código de ejemplo siguiente se recupera una colección de sensores del tipo denominado SAMPLE \_ sensor \_ Type \_ Time. A continuación, el código recupera el primer sensor de la colección por su índice.


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



Para recuperar un sensor por su identificador, debe conocer el identificador único para el sensor. Normalmente, los sensores generan este identificador cuando se conecta por primera vez para que pueda identificar varios sensores de la misma marca y modelo. Esto significa que probablemente no conocerá el ID. de sensor de antemano. Sin embargo, si ha almacenado una copia de un identificador de sensor determinado que recuperó anteriormente, por ejemplo llamando a [**ISensor:: getId**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getid), puede que desee volver a recuperar el mismo sensor.

En el ejemplo de código siguiente se muestra cómo recuperar un sensor mediante su identificador.


```C++
ISensor* pSensor = NULL;

// Get the sensor collection.
hr = pSensorManager->GetSensorByID(SAMPLE_SENSOR_TIME_ID, &pSensor);

```



También puede recuperar los sensores cuando estén disponibles mediante la recepción de un evento desde el administrador del sensor. Para obtener más información, vea [**ISensorManager:: SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ISensorManagerEvents::OnSensorEnter**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanagerevents-onsensorenter)
</dt> </dl>

 

 
