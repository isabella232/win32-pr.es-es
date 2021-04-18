---
description: En este tema se describe cómo recuperar datos de un sensor, de forma sincrónica y asincrónica.
ms.assetid: 4ae80816-5e53-4ed1-9300-4b38c22d65e2
title: Recuperación de los valores de datos del sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4642f120e549cd77b1b37610037092facf2ead1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666368"
---
# <a name="retrieving-sensor-data-values"></a><span data-ttu-id="660c5-103">Recuperación de los valores de datos del sensor</span><span class="sxs-lookup"><span data-stu-id="660c5-103">Retrieving Sensor Data Values</span></span>

<span data-ttu-id="660c5-104">En este tema se describe cómo recuperar datos de un sensor, de forma sincrónica y asincrónica.</span><span class="sxs-lookup"><span data-stu-id="660c5-104">This topic describes how to retrieve data from a sensor, synchronously and asynchronously.</span></span>

## <a name="retrieving-data-synchronously"></a><span data-ttu-id="660c5-105">Recuperar datos sincrónicamente</span><span class="sxs-lookup"><span data-stu-id="660c5-105">Retrieving Data Synchronously</span></span>

<span data-ttu-id="660c5-106">Puede recuperar los datos del sensor sincrónicamente llamando a [**ISensor:: GetData**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getdata).</span><span class="sxs-lookup"><span data-stu-id="660c5-106">You can retrieve sensor data synchronously by calling [**ISensor::GetData**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getdata).</span></span>

<span data-ttu-id="660c5-107">En el código de ejemplo siguiente se recupera un informe de datos de sensor y, a continuación, se recuperan tres valores de campo de datos individuales.</span><span class="sxs-lookup"><span data-stu-id="660c5-107">The following example code retrieves a sensor data report, and then retrieves three individual data field values.</span></span> <span data-ttu-id="660c5-108">El sensor de ejemplo proporciona datos personalizados sobre la hora local actual en los campos de datos hora, minuto y segundo.</span><span class="sxs-lookup"><span data-stu-id="660c5-108">The sample sensor provides custom data about the current local time in hour, minute, and second data fields.</span></span> <span data-ttu-id="660c5-109">La variable denominada pSensor contiene un puntero a [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) que representa el sensor que proporciona los datos.</span><span class="sxs-lookup"><span data-stu-id="660c5-109">The variable named pSensor contains a pointer to [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) that represents the sensor that supplies the data.</span></span>


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



## <a name="retrieving-data-asynchronously"></a><span data-ttu-id="660c5-110">Recuperar datos de forma asincrónica</span><span class="sxs-lookup"><span data-stu-id="660c5-110">Retrieving Data Asynchronously</span></span>

<span data-ttu-id="660c5-111">Puede recibir datos de sensor de forma asincrónica si se registra para recibir el evento [**ISensorEvents:: OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) .</span><span class="sxs-lookup"><span data-stu-id="660c5-111">You can receive sensor data asynchronously by registering to receive the [**ISensorEvents::OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) event.</span></span> <span data-ttu-id="660c5-112">Para saber cómo recibir devoluciones de llamada de eventos del sensor, consulte uso de eventos de la [API de sensor](using-sensor-api-events.md).</span><span class="sxs-lookup"><span data-stu-id="660c5-112">To understand how to receive sensor event callbacks, see [Using Sensor API Events](using-sensor-api-events.md).</span></span>

<span data-ttu-id="660c5-113">En el ejemplo de código siguiente se muestra una implementación de [**ISensorEvents:: OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) que recupera los valores de datos del informe de datos proporcionado por el evento.</span><span class="sxs-lookup"><span data-stu-id="660c5-113">The following example code shows an implementation of [**ISensorEvents::OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) that retrieves data values from the data report provided by the event.</span></span> <span data-ttu-id="660c5-114">El sensor de ejemplo proporciona datos personalizados sobre la hora local actual en los campos de datos hora, minuto y segundo.</span><span class="sxs-lookup"><span data-stu-id="660c5-114">The sample sensor provides custom data about the current local time in hour, minute, and second data fields.</span></span>


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



 

 
