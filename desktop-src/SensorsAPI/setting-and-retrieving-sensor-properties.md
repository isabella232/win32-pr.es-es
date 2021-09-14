---
description: En este tema se describe cómo recuperar y establecer valores para las propiedades del sensor. La interfaz ISensor proporciona los métodos para establecer y recuperar valores para las propiedades del sensor.
ms.assetid: 7d10e5b4-bae7-4564-84eb-75c6a2eeef8f
title: Recuperar y establecer las propiedades del sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f64bf0e253f47ae2d8cd1f4945f3b87aa3406b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265167"
---
# <a name="retrieving-and-setting-sensor-properties"></a>Recuperar y establecer las propiedades del sensor

En este tema se describe cómo recuperar y establecer valores para las propiedades del sensor. La [**interfaz ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) proporciona los métodos para establecer y recuperar valores para las propiedades del sensor.

## <a name="retrieving-sensor-properties"></a>Recuperación de propiedades del sensor

Puede recuperar algunos valores de propiedad de un sensor antes de que el usuario lo haya habilitado. Información como el nombre del fabricante o el modelo del sensor puede ayudarle a decidir si el programa puede usar el sensor.

Puede elegir recuperar un único valor de propiedad o recuperar una colección de valores de propiedad juntos. Para recuperar un valor único, llame [**a ISensor::GetProperty**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getproperty). Para recuperar una colección de valores, llame [**a ISensor::GetProperties.**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getproperties) Puede recuperar todas las propiedades de un sensor pasando **NULL** a través del primer parámetro a **ISensor::GetProperties.**

El código de ejemplo siguiente crea una función auxiliar que imprime el valor de una sola propiedad. La función recibe un puntero al sensor del que se va a recuperar el valor y una clave de propiedad que contiene la propiedad que se va a imprimir. La función puede imprimir valores para números, cadenas y **GUID,** pero no otros tipos más complejos.


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



El código de ejemplo siguiente crea una función que recupera e imprime una colección de propiedades. El conjunto de propiedades que se va a imprimir se define mediante la matriz denominada SensorProperties.


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



## <a name="setting-sensor-properties"></a>Establecimiento de las propiedades del sensor

Para poder establecer los valores de propiedad de un sensor, el usuario debe habilitarlo. Además, no se pueden establecer todas las propiedades del sensor.

Para establecer uno o varios valores para las propiedades, llame [**a ISensor::SetProperties.**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-setproperties) Este método se proporciona con un [puntero IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) que contiene la colección de propiedades que se va a establecer y sus valores asociados. El método devuelve una interfaz [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) correspondiente que puede contener códigos de error para las propiedades que no se pudieron establecer.

El código de ejemplo siguiente crea una función auxiliar que establece un nuevo valor para la propiedad SENSOR \_ PROPERTY \_ CURRENT REPORT \_ \_ INTERVAL. La función toma un puntero al sensor para el que se va a establecer la propiedad y un valor **ULONG** que indica el nuevo intervalo de informe que se va a establecer. (Tenga en cuenta que establecer un valor para esta propiedad determinada no garantiza que el sensor acepte el valor especificado. Consulte [**Propiedades del sensor**](sensor-properties.md) para obtener información sobre cómo funciona esta propiedad).


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Propiedades del sensor**](sensor-properties.md)
</dt> </dl>

 

 
