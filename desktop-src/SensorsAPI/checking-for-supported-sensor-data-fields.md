---
description: En este tema se describe cómo comprobar que un sensor puede proporcionar un conjunto determinado de campos de datos.
ms.assetid: 918ba4a3-d2ac-47ee-ba29-f7ddf67ffbc5
title: Comprobando los campos de datos del sensor admitidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cfd9cf42d1008ec1bb0e2785ec5113c5a817105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668300"
---
# <a name="checking-for-supported-sensor-data-fields"></a><span data-ttu-id="8bb0e-103">Comprobando los campos de datos del sensor admitidos</span><span class="sxs-lookup"><span data-stu-id="8bb0e-103">Checking for Supported Sensor Data Fields</span></span>

<span data-ttu-id="8bb0e-104">En este tema se describe cómo comprobar que un sensor puede proporcionar un conjunto determinado de campos de datos.</span><span class="sxs-lookup"><span data-stu-id="8bb0e-104">This topic describes how to verify that a sensor can provide a particular set of data fields.</span></span>

<span data-ttu-id="8bb0e-105">Después de recuperar un objeto de sensor, puede llamar a [**ISensor:: GetSupportedDataFields**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getsupporteddatafields) para determinar si el sensor puede proporcionar los datos que necesita.</span><span class="sxs-lookup"><span data-stu-id="8bb0e-105">After you have retrieved a sensor object, you can call [**ISensor::GetSupportedDataFields**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getsupporteddatafields) to determine whether the sensor can provide the data you need.</span></span>

<span data-ttu-id="8bb0e-106">En el código de ejemplo siguiente se crea una función auxiliar que prueba si el sensor puede proporcionar los tres campos de datos de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="8bb0e-106">The following example code creates a helper function that tests whether the sensor can provide all three of the sample data fields.</span></span> <span data-ttu-id="8bb0e-107">La función toma un puntero a un sensor como entrada y devuelve un valor booleano, donde **true** indica que el sensor puede proporcionar todos los campos de datos necesarios.</span><span class="sxs-lookup"><span data-stu-id="8bb0e-107">The function takes a pointer to a sensor as its input and returns a Boolean value, where **TRUE** indicates that the sensor can provide all the data fields required.</span></span>


```C++
BOOL CheckForSupportedDataFields(ISensor* pSensor)
{
    assert(pSensor);

    HRESULT hr = S_OK;
    DWORD cKeys = 0; // Key count.
    BOOL bRet = FALSE;

    IPortableDeviceKeyCollection* pKeys = NULL; // Output

    // CoCreate a key collection to store property keys.
    hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection, 
                                NULL, 
                                CLSCTX_INPROC_SERVER, 
                                IID_PPV_ARGS(&pKeys));

    if(SUCCEEDED(hr))
    {
        hr = pSensor->GetSupportedDataFields(&pKeys);
    }

    if(SUCCEEDED(hr))
    {
        hr = pKeys->GetCount(&cKeys);
    }

    if(SUCCEEDED(hr))
    {
        PROPERTYKEY pk;
        BOOL bHour, bMinute, bSecond = FALSE;

        for (DWORD i = 0; i < cKeys; i++)
        {
            hr = pKeys->GetAt(i, &pk);

            if(SUCCEEDED(hr))
            {
                // Test for the data fields.
                if(IsEqualPropertyKey(pk, SAMPLE_SENSOR_DATA_TYPE_HOUR))
                {
                    bHour = TRUE;
                }
                else if(IsEqualPropertyKey(pk, SAMPLE_SENSOR_DATA_TYPE_MINUTE))
                {
                    bMinute = TRUE;
                }
                else if(IsEqualPropertyKey(pk, SAMPLE_SENSOR_DATA_TYPE_SECOND))
                {
                    bSecond = TRUE;
                }
            }
        }

        // Compute the return value.
        // If all three properties were found,
        // bRet will resolve to TRUE.
        bRet = bHour && bMinute && bSecond;
    }

    SafeRelease(&pKeys);

    return bRet;
}
```



## <a name="related-topics"></a><span data-ttu-id="8bb0e-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8bb0e-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bb0e-109">**ISensorDataReport**</span><span class="sxs-lookup"><span data-stu-id="8bb0e-109">**ISensorDataReport**</span></span>](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport)
</dt> </dl>

 

 
