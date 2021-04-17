---
description: Uso de datos del sensor de luz
ms.assetid: 98272df5-08c0-4392-a74b-2919bbdcb022
title: Uso de datos del sensor de luz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ccf1c032b4100174afd6073d8c43db27bce3892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668188"
---
# <a name="using-light-sensor-data"></a>Uso de datos del sensor de luz

Hay dos maneras recomendadas de interpretar y usar datos de Lux procedentes de sensores de luz ambiente.

-   Aplicar una transformación a los datos para que el nivel de luz normalizado se pueda usar en proporción directa a los comportamientos del programa o a las interacciones. Un ejemplo sería cambiar el tamaño de un botón en el programa en proporción directa a los datos normalizados (o un intervalo de los datos normalizados, que se corresponden con el exterior, por ejemplo). Este enfoque proporciona la implementación óptima.
-   Tratar con intervalos de datos de Lux y asignar comportamientos y reacciones del programa a los umbrales superior e inferior de estos intervalos de datos de Lux. Se trata de una manera sencilla de responder a las condiciones de iluminación y es posible que no ofrezca una experiencia de usuario óptima. Sin embargo, este enfoque funciona bien si las transiciones suaves no son factibles.

## <a name="handling-data-from-multiple-light-sensors"></a>Tratamiento de los datos de varios sensores ligeros

Para generar la aproximación más precisa de las condiciones de iluminación actuales, puede usar datos de varios sensores de luz ambiente. Dado que los sensores de luz ambiente se pueden ocultar parcial o totalmente a las sombras u objetos que cubren el sensor, varios sensores colocados a cierta distancia pueden proporcionar una aproximación mucho mejor de las condiciones de iluminación actuales que un solo sensor.

Para realizar un seguimiento de los datos procedentes de varios sensores, puede usar las dos técnicas siguientes:

-   Se puede conservar el valor de datos más reciente de cada sensor de luz ambiente, junto con la marca de tiempo del informe de datos de sensor para cada una de estas lecturas. Los últimos [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) recibidos por cada lectura de sensor se pueden conservar y pueden proporcionar ambos valores para una referencia posterior. Al hacer referencia a la marca de tiempo de cada informe de datos de sensor, los datos se pueden administrar en función de su antigüedad. Por ejemplo, si los datos tienen más de 2 segundos de antigüedad, se podría omitir. En función de los valores de datos del sensor más recientes, se podría usar la lectura más alta, ya que se consideraría que el sensor correspondiente no estuviera oculto.
-   Puede usar el último valor del sensor de luz ambiente indicado. Esta implementación no sería óptima porque los valores de varios sensores no se comparan entre sí para obtener el resultado más preciso. No se recomienda este método.

## <a name="example-code"></a>Código de ejemplo

En el ejemplo de código siguiente se muestra una implementación para el evento [**OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) . El controlador de eventos llama a una función auxiliar, denominada **updateUI**, que cambia la interfaz de usuario basada en el valor Lux. La escritura de la implementación de UpdateUI depende de usted.


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



 

 
