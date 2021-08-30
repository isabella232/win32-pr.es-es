---
description: En este tema se describe cómo solicitar permisos al usuario para usar sensores. Para obtener información general sobre los permisos en sensor API, consulte Administración de permisos de usuario.
ms.assetid: e43ad497-86f1-4804-a67a-0aeb56b80d7f
title: Solicitud de permisos de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2bb6c977306ff68f40fb8d3a77b598114cb6f77feeb35d4beca96c05fbce224
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992685"
---
# <a name="requesting-user-permissions"></a>Solicitud de permisos de usuario

En este tema se describe cómo solicitar permisos al usuario para usar sensores. Para obtener información general sobre los permisos en sensor API, consulte [Administración de permisos de usuario.](managing-user-permissions.md)

En los ejemplos siguientes se muestran algunos de los escenarios comunes en los que puede optar por solicitar permisos de usuario.

El código de ejemplo siguiente simplemente solicita permisos para todos los sensores recuperados del administrador de sensores, por tipo, mediante una llamada de método asincrónico. La plataforma abrirá un cuadro de diálogo para solicitar al usuario que solo habilite los sensores que aún no están habilitados. Para determinar si el usuario ha habilitado algún sensor en este caso, debe controlar el [**evento ISensorEvents::OnStateChanged.**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged)


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



Puede optar por probar el estado del sensor sincrónicamente antes de intentar recuperar datos. En el código de ejemplo siguiente se muestra esta técnica.


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



El código de ejemplo siguiente solicita al usuario permisos de sensor si se produce un error al intentar recuperar un informe de datos de un sensor determinado.


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

[Administración de permisos de usuario](managing-user-permissions.md)
</dt> </dl>

 

 
