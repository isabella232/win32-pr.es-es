---
description: En este tema se describe cómo recuperar y establecer valores para las propiedades del sensor. La interfaz ISensor proporciona los métodos para establecer y recuperar los valores de las propiedades del sensor.
ms.assetid: 7d10e5b4-bae7-4564-84eb-75c6a2eeef8f
title: Recuperación y configuración de las propiedades del sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f64bf0e253f47ae2d8cd1f4945f3b87aa3406b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667890"
---
# <a name="retrieving-and-setting-sensor-properties"></a><span data-ttu-id="2723d-104">Recuperación y configuración de las propiedades del sensor</span><span class="sxs-lookup"><span data-stu-id="2723d-104">Retrieving and Setting Sensor Properties</span></span>

<span data-ttu-id="2723d-105">En este tema se describe cómo recuperar y establecer valores para las propiedades del sensor.</span><span class="sxs-lookup"><span data-stu-id="2723d-105">This topic describes how to retrieve and set values for sensor properties.</span></span> <span data-ttu-id="2723d-106">La interfaz [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) proporciona los métodos para establecer y recuperar los valores de las propiedades del sensor.</span><span class="sxs-lookup"><span data-stu-id="2723d-106">The [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) interface provides the methods to set and retrieve values for sensor properties.</span></span>

## <a name="retrieving-sensor-properties"></a><span data-ttu-id="2723d-107">Recuperando propiedades de sensor</span><span class="sxs-lookup"><span data-stu-id="2723d-107">Retrieving Sensor Properties</span></span>

<span data-ttu-id="2723d-108">Puede recuperar algunos valores de propiedad de un sensor antes de que el usuario lo haya habilitado.</span><span class="sxs-lookup"><span data-stu-id="2723d-108">You can retrieve some property values from a sensor before the user has enabled it.</span></span> <span data-ttu-id="2723d-109">La información como el nombre del fabricante o el modelo del sensor puede ayudarle a decidir si el programa puede usar el sensor.</span><span class="sxs-lookup"><span data-stu-id="2723d-109">Information such as the manufacturer's name or the model of the sensor can help you to decide whether your program can use the sensor.</span></span>

<span data-ttu-id="2723d-110">Puede optar por recuperar un solo valor de propiedad o recuperar una colección de valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="2723d-110">You can choose to retrieve a single property value, or to retrieve a collection of property values together.</span></span> <span data-ttu-id="2723d-111">Para recuperar un único valor, llame a [**ISensor:: GetProperty**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getproperty).</span><span class="sxs-lookup"><span data-stu-id="2723d-111">To retrieve single value, call [**ISensor::GetProperty**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getproperty).</span></span> <span data-ttu-id="2723d-112">Para recuperar una colección de valores, llame a [**ISensor:: GetProperties**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getproperties).</span><span class="sxs-lookup"><span data-stu-id="2723d-112">To retrieve a collection of values, call [**ISensor::GetProperties**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getproperties).</span></span> <span data-ttu-id="2723d-113">Puede recuperar todas las propiedades de un sensor si pasa **null** a través del primer parámetro a **ISensor:: GetProperties**.</span><span class="sxs-lookup"><span data-stu-id="2723d-113">You can retrieve all properties for a sensor by passing **NULL** through the first parameter to **ISensor::GetProperties**.</span></span>

<span data-ttu-id="2723d-114">En el código de ejemplo siguiente se crea una función auxiliar que imprime el valor de una sola propiedad.</span><span class="sxs-lookup"><span data-stu-id="2723d-114">The following example code creates a helper function that prints the value of a single property.</span></span> <span data-ttu-id="2723d-115">La función recibe un puntero al sensor del que se va a recuperar el valor y una clave de propiedad que contiene la propiedad que se va a imprimir.</span><span class="sxs-lookup"><span data-stu-id="2723d-115">The function receives a pointer to the sensor from which to retrieve the value and a property key that contains the property to print.</span></span> <span data-ttu-id="2723d-116">La función puede imprimir valores de números, cadenas y **GUID**, pero no de otros tipos más complejos.</span><span class="sxs-lookup"><span data-stu-id="2723d-116">The function can print values for numbers, strings, and **GUID** s, but not other, more complex types.</span></span>


```C++
HRESULT PrintSensorProperty(ISensor* pSensor, REFPROPERTYKEY pk)
{
    assert(pSensor);

    HRESULT hr = S_OK;

    PROPVARIANT pv = {};

    hr = pSensor->GetProperty(pk, &pv);

    if(SUCCEEDED(hr))
    {
        if(pv.vt == VT_UI4)  // Number
        {
            wprintf_s(L"\nSensor integer value: %u\n", pv.ulVal);
        }
        else if(pv.vt == VT_LPWSTR)  // String
        {
            wprintf_s(L"\nSensor string value: %s\n", pv.pwszVal);
        }
        else if(pv.vt == VT_CLSID)  // GUID
        {
            int iRet = 0;

            // Convert the GUID to a string.
            OLECHAR wszGuid[39] = {}; // Buffer for string.
            iRet = ::StringFromGUID2(*(pv.puuid), wszGuid, 39);

            assert(39 == iRet); // Count of characters returned for GUID.

            wprintf_s(L"\nSensor GUID value: %s\n", wszGuid);
        }
        else  // Interface or vector
        {
            wprintf_s(L"\nSensor property is a compound type. Unable to print value.");
        }
    }

    PropVariantClear(&pv);

    return hr;    
}
```



<span data-ttu-id="2723d-117">En el código de ejemplo siguiente se crea una función que recupera e imprime una colección de propiedades.</span><span class="sxs-lookup"><span data-stu-id="2723d-117">The following example code creates a function that retrieves and prints a collection of properties.</span></span> <span data-ttu-id="2723d-118">El conjunto de propiedades que se va a imprimir se define en la matriz denominada SensorProperties.</span><span class="sxs-lookup"><span data-stu-id="2723d-118">The set of properties to print is defined by the array named SensorProperties.</span></span>


```C++
HRESULT PrintSensorProperties(ISensor* pSensor)
{
    assert(pSensor);

    HRESULT hr = S_OK;

    DWORD cVals = 0; // Count of returned properties.
    IPortableDeviceKeyCollection* pKeys = NULL; // Input
    IPortableDeviceValues* pValues = NULL;  // Output

    // Properties to print.
    const PROPERTYKEY SensorProperties[] =
    {
        SENSOR_PROPERTY_MANUFACTURER,
        SENSOR_PROPERTY_SERIAL_NUMBER,
        SENSOR_PROPERTY_DESCRIPTION,
        SENSOR_PROPERTY_FRIENDLY_NAME
    };

    // CoCreate a key collection to store property keys.
    hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection, 
                                NULL, 
                                CLSCTX_INPROC_SERVER,                                 
                                IID_PPV_ARGS(&pKeys));

    if(SUCCEEDED(hr))
    {
        // Add the properties to the key collection.
        for (DWORD dwIndex = 0; dwIndex < ARRAYSIZE(SensorProperties); dwIndex++)
        {
            hr = pKeys->Add(SensorProperties[dwIndex]);

            if(FAILED(hr))
            {
                // Unexpected.
                // This example returns the failed HRESULT.
                // You may choose to ignore failures, here.
                break;
            }
        }
    }

    if(SUCCEEDED(hr))
    {
        // Retrieve the properties from the sensor.
        hr = pSensor->GetProperties(pKeys, &pValues);
    }

    if(SUCCEEDED(hr))
    {
        // Get the number of values returned.        
        hr = pValues->GetCount(&cVals);
    }

    if(SUCCEEDED(hr))
    {
        PROPERTYKEY pk; // Keys
        PROPVARIANT pv = {}; // Values

        // Loop through the values;
        for (DWORD i = 0; i < cVals; i++)
        {
            // Get the value at the current index.
            hr = pValues->GetAt(i, &pk, &pv);

            if(SUCCEEDED(hr))
            { 
                // Find and print the property.
                if(IsEqualPropertyKey(pk, SENSOR_PROPERTY_MANUFACTURER))
                {
                    wprintf_s(L"\nManufacturer: %s\n", pv.pwszVal);
                }
                else if(IsEqualPropertyKey(pk, SENSOR_PROPERTY_SERIAL_NUMBER))
                {
                    wprintf_s(L"Serial number: %s\n", pv.pwszVal);
                }
                else if(IsEqualPropertyKey(pk, SENSOR_PROPERTY_FRIENDLY_NAME))
                {
                    wprintf_s(L"Friendly name: %s\n", pv.pwszVal);
                }
                else if(IsEqualPropertyKey(pk, SENSOR_PROPERTY_DESCRIPTION))
                {
                    wprintf_s(L"Description: %s\n", pv.pwszVal);
                }
            }

            PropVariantClear(&pv);
        } // end i loop        
    }

    SafeRelease(&pKeys);
    SafeRelease(&pValues);

    return hr;
};
```



## <a name="setting-sensor-properties"></a><span data-ttu-id="2723d-119">Configuración de las propiedades del sensor</span><span class="sxs-lookup"><span data-stu-id="2723d-119">Setting Sensor Properties</span></span>

<span data-ttu-id="2723d-120">Para poder establecer los valores de propiedad de un sensor, el usuario debe habilitar el sensor.</span><span class="sxs-lookup"><span data-stu-id="2723d-120">Before you can set property values for a sensor, the user must enable the sensor.</span></span> <span data-ttu-id="2723d-121">Además, no se pueden establecer todas las propiedades del sensor.</span><span class="sxs-lookup"><span data-stu-id="2723d-121">Also, not all sensor properties can be set.</span></span>

<span data-ttu-id="2723d-122">Para establecer uno o varios valores para las propiedades, llame a [**ISensor:: SetProperties**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-setproperties).</span><span class="sxs-lookup"><span data-stu-id="2723d-122">To set one or more values for properties, call [**ISensor::SetProperties**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-setproperties).</span></span> <span data-ttu-id="2723d-123">Este método se proporciona con un puntero [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) que contiene la colección de propiedades que se van a establecer y sus valores asociados.</span><span class="sxs-lookup"><span data-stu-id="2723d-123">You provide this method with an [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) pointer that contains the collection of properties to set, and their associated values.</span></span> <span data-ttu-id="2723d-124">El método devuelve una interfaz [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) correspondiente que puede contener códigos de error para las propiedades que no se pueden establecer.</span><span class="sxs-lookup"><span data-stu-id="2723d-124">The method returns a corresponding [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) interface that may contain error codes for properties that could not be set.</span></span>

<span data-ttu-id="2723d-125">En el código de ejemplo siguiente se crea una función auxiliar que establece un nuevo valor para \_ la \_ propiedad de intervalo de informe actual de la propiedad de sensor \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2723d-125">The following example code creates a helper function that sets a new value for the SENSOR\_PROPERTY\_CURRENT\_REPORT\_INTERVAL property.</span></span> <span data-ttu-id="2723d-126">La función toma un puntero al sensor para el que se establece la propiedad y un valor **ULong** que indica el nuevo intervalo del informe que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="2723d-126">The function takes a pointer to the sensor for which to set the property, and a **ULONG** value that indicates the new report interval to be set.</span></span> <span data-ttu-id="2723d-127">(Tenga en cuenta que si se establece un valor para esta propiedad concreta, no se garantiza que el sensor acepte el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="2723d-127">(Note that setting a value for this particular property does not guarantee that the sensor will accept the specified value.</span></span> <span data-ttu-id="2723d-128">Consulte [**propiedades del sensor**](sensor-properties.md) para obtener información sobre cómo funciona esta propiedad.)</span><span class="sxs-lookup"><span data-stu-id="2723d-128">See [**Sensor Properties**](sensor-properties.md) for information about how this property works.)</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="2723d-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2723d-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2723d-130">**Propiedades del sensor**</span><span class="sxs-lookup"><span data-stu-id="2723d-130">**Sensor Properties**</span></span>](sensor-properties.md)
</dt> </dl>

 

 
