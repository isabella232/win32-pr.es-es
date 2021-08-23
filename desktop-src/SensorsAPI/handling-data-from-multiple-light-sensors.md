---
description: Uso de datos del sensor de luz
ms.assetid: 98272df5-08c0-4392-a74b-2919bbdcb022
title: Uso de datos del sensor de luz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae4f7047301c7d31d18014bb09512d1f3944c418a34c153a87c001f95fb63a8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425135"
---
# <a name="using-light-sensor-data"></a>Uso de datos del sensor de luz

Hay dos maneras recomendadas de interpretar y usar datos de color que proceden de sensores de luz ambiente.

-   Aplique una transformación a los datos para que el nivel de luz normalizado se pueda usar en proporción directa con las interacciones o comportamientos del programa. Un ejemplo sería variar el tamaño de un botón del programa en proporción directa con los datos normalizados (o un intervalo de los datos normalizados, correspondientes a exteriores, por ejemplo). Este enfoque proporciona la implementación óptima.
-   Tratar con intervalos de datos de hadas y asignar comportamientos y reacción de los programas a los umbrales superior e inferior de estos intervalos de datos de ándalo. Se trata de una manera sencilla de responder a las condiciones de iluminación y puede no producir la experiencia óptima del usuario. Sin embargo, este enfoque funciona bien si las transiciones fluidas no son factibles.

## <a name="handling-data-from-multiple-light-sensors"></a>Control de datos de varios sensores de luz

Para producir la aproximación más precisa de las condiciones de iluminación actuales, puede usar datos de varios sensores de luz ambiente. Dado que los sensores de luz ambiente pueden estar parcial o totalmente ocultos por sombras u objetos que cubren el sensor, varios sensores situados a cierta distancia pueden proporcionar una aproximación mucho mejor de las condiciones de iluminación actuales que un único sensor.

Para realizar un seguimiento de los datos procedentes de varios sensores, puede usar las dos técnicas siguientes:

-   Se puede conservar el valor de datos más reciente de cada sensor de luz ambiente, junto con la marca de tiempo del informe de datos del sensor para cada una de estas lecturas. El último [**ISensorDataReport recibido**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) para cada lectura del sensor se pudo conservar y podría proporcionar ambos valores para referencia posterior. Al hacer referencia a la marca de tiempo de cada informe de datos del sensor, los datos se pueden administrar en función de su antigüedad. Por ejemplo, si los datos tienen más de 2 segundos de antigüedad, podrían omitirse. En función de los valores de datos del sensor más recientes, se podría usar la lectura más alta porque se supone que el sensor correspondiente no se oculta.
-   Puede usar el último valor del sensor de luz ambiente notificado. Esta implementación no sería óptima porque los valores de varios sensores no se comparan entre sí para obtener el resultado más preciso. No se recomienda este método.

## <a name="example-code"></a>Código de ejemplo

El código de ejemplo siguiente muestra una implementación para el [**evento OnDataUpdated.**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) El controlador de eventos llama a una función auxiliar, **denominada UpdateUI,** que cambia la interfaz de usuario en función del valor de . La escritura de la implementación de UpdateUI es su parte.


```C++
// Override of ISensorEvents::OnDataUpdated
// Part of an event sink implementation for ISensorEvents
STDMETHODIMP CALSEventSink::OnDataUpdated(
    ISensor* pSensor, 
    ISensorDataReport* pNewData)
{
    HRESULT hr = S_OK;
   
    if(pSensor == NULL ||
       pNewData == NULL)
    {
         return E_POINTER;
    }

    // Declare and initialize the PROPVARIANT
    PROPVARIANT lightLevel;
    PropVariantInit(&lightLevel);

    // Get the sensor reading from the ISensorDataReport object
    hr = pNewData->GetSensorValue(
        SENSOR_DATA_TYPE_LIGHT_LEVEL_LUX, 
        &lightLevel);

    if(SUCCEEDED(hr))
    {
        if(lightlevel.vt == VT_R4)
        {
            // Extract the float value from the PROPVARIANT object
            float luxValue = lightLevel.fltVal;

            // Normalize the light sensor data
            double lightNormalized = ::log10(luxValue) / 5.0;

            // Handle UI changes based on the normalized LUX data
            // which ranges from 0.0 - 1.0 for a lux range of 
            // 0 lux to 100,000 lux. 
            UpdateUI(lightNormalized);
        }
    }

    // Release the variant.     
    PropVariantClear(&lightLevel);

    return hr;
}
```



 

 
