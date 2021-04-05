---
description: La API de sensor proporciona notificaciones de eventos a través de interfaces de devolución de llamada.
ms.assetid: 0c396d54-cb2e-4b07-999f-3f4001db2a02
title: Uso de eventos de la API de sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a54fcb14138c1b20470a2b716e5cce86235c3102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002332"
---
# <a name="using-sensor-api-events"></a><span data-ttu-id="4c8f5-103">Uso de eventos de la API de sensor</span><span class="sxs-lookup"><span data-stu-id="4c8f5-103">Using Sensor API Events</span></span>

<span data-ttu-id="4c8f5-104">La API de sensor proporciona notificaciones de eventos a través de interfaces de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="4c8f5-104">The Sensor API provides event notifications through callback interfaces.</span></span>

<span data-ttu-id="4c8f5-105">Para recibir el evento notfications, el programa debe implementar las interfaces de devolución de llamada COM necesarias.</span><span class="sxs-lookup"><span data-stu-id="4c8f5-105">To receive event notfications, your program must implement the required COM callback interfaces.</span></span> <span data-ttu-id="4c8f5-106">Para recibir eventos de sensores, debe implementar [**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span><span class="sxs-lookup"><span data-stu-id="4c8f5-106">To receive events from sensors, you must implement [**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span></span> <span data-ttu-id="4c8f5-107">Para recibir eventos del administrador del sensor, debe implementar [**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents).</span><span class="sxs-lookup"><span data-stu-id="4c8f5-107">To receive events from the sensor manager, you must implement [**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents).</span></span>

<span data-ttu-id="4c8f5-108">En el código de ejemplo siguiente se crea una clase que implementa [**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span><span class="sxs-lookup"><span data-stu-id="4c8f5-108">The following example code creates a class that implements [**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span></span>


```C++
class CMyEvents : public ISensorEvents
{
public:

    STDMETHODIMP QueryInterface(REFIID iid, void** ppv)
    {
        if (ppv == NULL)
        {
            return E_POINTER;
        }
        if (iid == __uuidof(IUnknown))
        {
            *ppv = static_cast<IUnknown*>(this);
        }
        else if (iid == __uuidof(ISensorEvents))
        {
            *ppv = static_cast<ISensorEvents*>(this);
        }
        else
        {
            *ppv = NULL;
            return E_NOINTERFACE;
        }
        AddRef();
        return S_OK;
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef); 
    }

    STDMETHODIMP_(ULONG) Release()
    {
        ULONG count = InterlockedDecrement(&m_cRef);
        if (count == 0)
        {
            delete this;
            return 0;
        }
        return count;
    }

    //
    // ISensorEvents methods.
    //

    STDMETHODIMP OnEvent(
            ISensor *pSensor,
            REFGUID eventID,
            IPortableDeviceValues *pEventData)
    {
        HRESULT hr = S_OK;

        // Handle custom events here.

        return hr;
    }

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

    STDMETHODIMP OnLeave(
            REFSENSOR_ID sensorID)
    {
        HRESULT hr = S_OK;

        // Peform any housekeeping tasks for the sensor that is leaving.
        // For example, if you have maintained a reference to the sensor,
        // release it now and set the pointer to NULL.

        return hr;
    }

    STDMETHODIMP OnStateChanged(
            ISensor* pSensor,
            SensorState state)
    {
        HRESULT hr = S_OK;

        if(NULL == pSensor)
        {
            return E_INVALIDARG;
        }


        if(state == SENSOR_STATE_READY)
        {
            wprintf_s(L"\nTime sensor is now ready.");
        }
        else if(state == SENSOR_STATE_ACCESS_DENIED)
        {
            wprintf_s(L"\nNo permission for the time sensor.\n");
            wprintf_s(L"Enable the sensor in the control panel.\n");
        }
  

        return hr;
    }

    private:
        long m_cRef;

};

```



<span data-ttu-id="4c8f5-109">Después de implementar la interfaz de devolución de llamada, puede proporcionar un sensor determinado con un puntero a una instancia de la clase de devolución de llamada para empezar a recibir notificaciones de eventos del sensor.</span><span class="sxs-lookup"><span data-stu-id="4c8f5-109">After implementing the callback interface, you can provide a particular sensor with a pointer to an instance of your callback class to start receiving event notifications from the sensor.</span></span>

<span data-ttu-id="4c8f5-110">En el código de ejemplo siguiente se crea una instancia de la clase de devolución de llamada y, a continuación, se solicita el evento notificaciones de un sensor.</span><span class="sxs-lookup"><span data-stu-id="4c8f5-110">The following example code creates an instance of the callback class, and then requests event notifcations from a sensor.</span></span>


```C++
CMyEvents* pEventClass = NULL;
ISensorEvents* pMyEvents = NULL;

if(SUCCEEDED(hr))
{
    // Create an instance of the event class.
    pEventClass = new(std::nothrow) CMyEvents();        
}

if(SUCCEEDED(hr))
{
    // Retrieve the pointer to the callback interface.
    hr = pEventClass->QueryInterface(IID_PPV_ARGS(&pMyEvents));
}

if(SUCCEEDED(hr))
{
    // Start receiving events.
    hr = pSensor->SetEventSink(pMyEvents);
} 

```



<span data-ttu-id="4c8f5-111">Puede escribir código similar para recibir eventos del administrador del sensor.</span><span class="sxs-lookup"><span data-stu-id="4c8f5-111">You can write similar code to receive events from the sensor manager.</span></span>

<span data-ttu-id="4c8f5-112">En el ejemplo de código siguiente se muestra cómo dejar de recibir notificaciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="4c8f5-112">The following example code shows how to stop receiving event notifications.</span></span>


```C++
if(SUCCEEDED(hr))
{
    hr = pSensor->SetEventSink(NULL);
}
```



## <a name="requesting-a-report-interval"></a><span data-ttu-id="4c8f5-113">Solicitar un intervalo de informe</span><span class="sxs-lookup"><span data-stu-id="4c8f5-113">Requesting a Report Interval</span></span>

<span data-ttu-id="4c8f5-114">Puede sugerir un valor de la frecuencia con la que la ha recibido los eventos de actualización de datos.</span><span class="sxs-lookup"><span data-stu-id="4c8f5-114">You can suggest a value for how frequently your applicaton receives data-updated events.</span></span> <span data-ttu-id="4c8f5-115">Sin embargo, no es necesario que los sensores proporcionen eventos en un intervalo determinado.</span><span class="sxs-lookup"><span data-stu-id="4c8f5-115">However, sensors are not required to provide events at any particular interval.</span></span> <span data-ttu-id="4c8f5-116">Debe tener en cuenta que el valor sugerido podría no coincidir con el intervalo de informes real que el sensor usa para generar eventos.</span><span class="sxs-lookup"><span data-stu-id="4c8f5-116">You should be aware that your suggested value might not match the actual report interval the sensor uses to raise events.</span></span> <span data-ttu-id="4c8f5-117">Para conocer el intervalo de informes real, recupere el valor de la propiedad de intervalo de informe actual de la propiedad de SENSOR \_ \_ \_ \_ , como se describe en [recuperar y establecer las propiedades del sensor](setting-and-retrieving-sensor-properties.md).</span><span class="sxs-lookup"><span data-stu-id="4c8f5-117">To know the actual report interval, retrieve the value for the SENSOR\_PROPERTY\_CURRENT\_REPORT\_INTERVAL property, as described in [Retrieving and Setting Sensor Properties](setting-and-retrieving-sensor-properties.md).</span></span>

<span data-ttu-id="4c8f5-118">En el código de ejemplo siguiente se crea una función auxiliar que solicita un nuevo valor para \_ la \_ propiedad de intervalo de informe actual de la propiedad de sensor \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4c8f5-118">The following example code creates a helper function that requests a new value for the SENSOR\_PROPERTY\_CURRENT\_REPORT\_INTERVAL property.</span></span> <span data-ttu-id="4c8f5-119">La función toma un puntero al sensor para el que se establece la propiedad y un valor **ULong** que indica el nuevo intervalo del informe que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="4c8f5-119">The function takes a pointer to the sensor for which to set the property, and a **ULONG** value that indicates the new report interval to be set.</span></span>


```C++
HRESULT SetCurrentReportInterval(ISensor* pSensor, ULONG ulNewInterval)
{
    assert(pSensor);

    HRESULT hr = S_OK;

    IPortableDeviceValues* pPropsToSet = NULL; // Input
    IPortableDeviceValues* pPropsReturn = NULL; // Output

    // Create the input object.
    hr = CoCreateInstance(__uuidof(PortableDeviceValues),
                            NULL,
                            CLSCTX_INPROC_SERVER,                           
                            IID_PPV_ARGS(&pPropsToSet));

    if(SUCCEEDED(hr))
    {
        // Add the current report interval property.
        hr = pPropsToSet->SetUnsignedIntegerValue(SENSOR_PROPERTY_CURRENT_REPORT_INTERVAL, ulNewInterval);
    }

    if(SUCCEEDED(hr))
    {
        // Only setting a single property, here.
        hr = pSensor->SetProperties(pPropsToSet, &pPropsReturn);
    }

    // Test for failure.
    if(hr == S_FALSE)
    {
        HRESULT hrError = S_OK;
      
        // Check results for failure.
        hr = pPropsReturn->GetErrorValue(SENSOR_PROPERTY_CURRENT_REPORT_INTERVAL, &hrError);

        if(SUCCEEDED(hr))
        {
            // Print an error message.
            wprintf_s(L"\nSetting current report interval failed with error 0x%X\n", hrError);

            // Return the error code.
            hr = hrError;
        }
    }
    else if(hr == E_ACCESSDENIED)
    {
        // No permission. Take appropriate action.
    }

    SafeRelease(&pPropsToSet);
    SafeRelease(&pPropsReturn);
   
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="4c8f5-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4c8f5-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c8f5-121">Acerca de los eventos de la API de sensor</span><span class="sxs-lookup"><span data-stu-id="4c8f5-121">About Sensor API Events</span></span>](about-sensor-events.md)
</dt> </dl>

 

 



