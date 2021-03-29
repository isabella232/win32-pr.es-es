---
description: En este tema se describe cómo solicitar permisos al usuario para usar sensores. Para obtener información general sobre los permisos de la API de sensor, consulte Administración de permisos de usuario.
ms.assetid: e43ad497-86f1-4804-a67a-0aeb56b80d7f
title: Solicitar permisos de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41e103426388d2db49bb5a8fb01d3370207ec49b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540899"
---
# <a name="requesting-user-permissions"></a>Solicitar permisos de usuario

En este tema se describe cómo solicitar permisos al usuario para usar sensores. Para obtener información general sobre los permisos de la API de sensor, consulte [Administración de permisos de usuario](managing-user-permissions.md).

En los siguientes ejemplos se ilustran algunos de los escenarios comunes en los que puede elegir solicitar permisos de usuario.

El código de ejemplo siguiente simplemente solicita permisos para todos los sensores recuperados del administrador del sensor, por tipo, mediante una llamada de método asincrónico. La plataforma abrirá un cuadro de diálogo para pedir al usuario que habilite solo los sensores que aún no están habilitados. Para determinar si el usuario ha habilitado los sensores en este caso, debe controlar el evento [**ISensorEvents:: OnStateChanged**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged) .


```C++
// Get the sensor collection.
hr = pSensorManager->GetSensorsByType(SAMPLE_SENSOR_TYPE_TIME, &pSensorColl);

if(SUCCEEDED(hr))
{
    // Request permissions for all sensors
    // in the collection.
    hr = pSensorManager->RequestPermissions(0, pSensorColl, FALSE);
}

```



Puede optar por probar el estado del sensor sincrónicamente antes de intentar recuperar los datos. En el ejemplo de código siguiente se muestra esta técnica.


```C++
if(SUCCEEDED(hr))
{
   // Check the current sensor state.
   SensorState state = SENSOR_STATE_NOT_AVAILABLE;

   hr = pSensor->GetState(&state);

   if(SUCCEEDED(hr))
   {
       if(state == SENSOR_STATE_ACCESS_DENIED)
       {
           wprintf_s(L"\nSensor not enabled, requesting permissions...\n");
           hr = pSensorManager->RequestPermissions(0, pSensorColl, TRUE);

           if(hr == HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED) ||
              hr == HRESULT_FROM_WIN32(ERROR_CANCELLED)) 
           {
               wprintf_s(L"\nYou have previously denied access to this sensor.\n");
               wprintf_s(L"Please use the Location and Other Sensors control panel\n");
               wprintf_s(L"to enable the WDK Time Sensor and run this program again.\n");
           }
       }
   }
}

if(SUCCEEDED(hr))
{
    // Get the data report.
    hr = pSensor->GetData(&pReport);
}
```



En el código de ejemplo siguiente se pide al usuario permisos de sensor si se produce un error al intentar recuperar un informe de datos de un sensor determinado.


```C++
if(SUCCEEDED(hr))
{
    // Get the data report.
    hr = pSensor->GetData(&pReport);

    if(E_ACCESSDENIED == hr)
    {
       wprintf_s(L"\nSensor not enabled, requesting permissions...\n");
       hr = pSensorManager->RequestPermissions(0, pSensorColl, TRUE);

       if(hr == HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED) ||
          hr == HRESULT_FROM_WIN32(ERROR_CANCELLED)) 
       {
           wprintf_s(L"\nYou have previously denied access to this sensor.\n");
           wprintf_s(L"Please use the Location and Other Sensors control panel\n");
           wprintf_s(L"to enable the WDK Time Sensor and run this program again.\n");
       }
    }
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager)
</dt> <dt>

[Administrar permisos de usuario](managing-user-permissions.md)
</dt> </dl>

 

 
