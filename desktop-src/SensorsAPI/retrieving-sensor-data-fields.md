---
description: En este tema se describe cómo recuperar datos de un sensor de forma sincrónica y asincrónica.
ms.assetid: 4ae80816-5e53-4ed1-9300-4b38c22d65e2
title: Recuperar valores de datos del sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e240b9bc14d917db0e0c4280ad957aa139369eb7762abfcd69441d25e66857d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960035"
---
# <a name="retrieving-sensor-data-values"></a>Recuperar valores de datos del sensor

En este tema se describe cómo recuperar datos de un sensor de forma sincrónica y asincrónica.

## <a name="retrieving-data-synchronously"></a>Recuperar datos de forma sincrónica

Puede recuperar los datos del sensor sincrónicamente llamando [**a ISensor::GetData**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getdata).

El código de ejemplo siguiente recupera un informe de datos del sensor y, a continuación, recupera tres valores de campo de datos individuales. El sensor de ejemplo proporciona datos personalizados sobre la hora local actual en campos de datos de hora, minuto y segundo. La variable denominada pSensor contiene un puntero a [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) que representa el sensor que proporciona los datos.


```C++
if(SUCCEEDED(hr))
{
    // Get the data report.
    hr = pSensor->GetData(&pReport);
}
  
if(SUCCEEDED(hr))
{
    PROPVARIANT var = {};

    hr = pReport->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_HOUR, &var);

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulHour = var.ulVal;                
        }
    }

    PropVariantClear(&var);

    hr = pReport->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_MINUTE, &var);

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulMinute = var.ulVal;
        }
    }

    PropVariantClear(&var);

    hr = pReport->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_SECOND, &var);

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulSecond = var.ulVal;
        }
    }

    PropVariantClear(&var);        

    if(SUCCEEDED(hr))
    {
        // Print the local time to the console window.
        wprintf_s(L"\nCurrent local time is: \n");
        wprintf_s(L"%02d:%02d:%02d (synchronous)\n\n", ulHour, ulMinute, ulSecond);
    }

```



## <a name="retrieving-data-asynchronously"></a>Recuperar datos de forma asincrónica

Puede recibir datos del sensor de forma asincrónica si se registra para recibir el evento [**ISensorEvents::OnDataUpdated.**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) Para entender cómo recibir devoluciones de llamada de eventos de sensor, consulte [Uso de eventos de sensor API.](using-sensor-api-events.md)

El código de ejemplo siguiente muestra una implementación de [**ISensorEvents::OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) que recupera los valores de datos del informe de datos proporcionado por el evento . El sensor de ejemplo proporciona datos personalizados sobre la hora local actual en campos de datos de hora, minuto y segundo.


```C++
STDMETHODIMP OnDataUpdated(
        ISensor *pSensor,
        ISensorDataReport *pNewData)
{
    HRESULT hr = S_OK;

    if(NULL == pNewData ||
       NULL == pSensor)
    {
        return E_INVALIDARG;
    }

    ULONG ulHour = 0;
    ULONG ulMinute = 0;
    ULONG ulSecond = 0;

    PROPVARIANT var = {};

    hr = pNewData->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_HOUR, &var);

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulHour = var.ulVal;                
        }
    }

    PropVariantClear(&var);

    if(SUCCEEDED(hr))
    {
        hr = pNewData->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_MINUTE, &var);
    }

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulMinute = var.ulVal;
        }
    }

    PropVariantClear(&var);

    if(SUCCEEDED(hr))
    {
        hr = pNewData->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_SECOND, &var);
    }

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulSecond = var.ulVal;
        }
    }

    PropVariantClear(&var);

    if(SUCCEEDED(hr))
    {
        // Print
        wprintf_s(L"Current local time is: \n");
        wprintf_s(L"%02d:%02d:%02d (asynchronous)\n", ulHour, ulMinute, ulSecond);
    }

    return hr;
}
```



 

 
