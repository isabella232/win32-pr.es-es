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
# <a name="using-light-sensor-data"></a><span data-ttu-id="d2c49-103">Uso de datos del sensor de luz</span><span class="sxs-lookup"><span data-stu-id="d2c49-103">Using Light Sensor Data</span></span>

<span data-ttu-id="d2c49-104">Hay dos maneras recomendadas de interpretar y usar datos de Lux procedentes de sensores de luz ambiente.</span><span class="sxs-lookup"><span data-stu-id="d2c49-104">There are two recommended ways of interpreting and using lux data that comes from ambient light sensors.</span></span>

-   <span data-ttu-id="d2c49-105">Aplicar una transformación a los datos para que el nivel de luz normalizado se pueda usar en proporción directa a los comportamientos del programa o a las interacciones.</span><span class="sxs-lookup"><span data-stu-id="d2c49-105">Apply a transform to the data so that the normalized light level can be used in direct proportion to program behaviors or interactions.</span></span> <span data-ttu-id="d2c49-106">Un ejemplo sería cambiar el tamaño de un botón en el programa en proporción directa a los datos normalizados (o un intervalo de los datos normalizados, que se corresponden con el exterior, por ejemplo).</span><span class="sxs-lookup"><span data-stu-id="d2c49-106">An example would be to vary the size of a button in your program in direct proportion to the normalized data (or a range of the normalized data, corresponding to outdoors, for example).</span></span> <span data-ttu-id="d2c49-107">Este enfoque proporciona la implementación óptima.</span><span class="sxs-lookup"><span data-stu-id="d2c49-107">This approach gives the optimal implementation.</span></span>
-   <span data-ttu-id="d2c49-108">Tratar con intervalos de datos de Lux y asignar comportamientos y reacciones del programa a los umbrales superior e inferior de estos intervalos de datos de Lux.</span><span class="sxs-lookup"><span data-stu-id="d2c49-108">Deal with ranges of lux data, and map program behaviors and reactions to the upper and lower thresholds of these ranges of lux data.</span></span> <span data-ttu-id="d2c49-109">Se trata de una manera sencilla de responder a las condiciones de iluminación y es posible que no ofrezca una experiencia de usuario óptima.</span><span class="sxs-lookup"><span data-stu-id="d2c49-109">This is a simple way to respond to lighting conditions and may not yield the optimal user experience.</span></span> <span data-ttu-id="d2c49-110">Sin embargo, este enfoque funciona bien si las transiciones suaves no son factibles.</span><span class="sxs-lookup"><span data-stu-id="d2c49-110">However, this approach works fine if smooth transitions are not feasible.</span></span>

## <a name="handling-data-from-multiple-light-sensors"></a><span data-ttu-id="d2c49-111">Tratamiento de los datos de varios sensores ligeros</span><span class="sxs-lookup"><span data-stu-id="d2c49-111">Handling Data from Multiple Light Sensors</span></span>

<span data-ttu-id="d2c49-112">Para generar la aproximación más precisa de las condiciones de iluminación actuales, puede usar datos de varios sensores de luz ambiente.</span><span class="sxs-lookup"><span data-stu-id="d2c49-112">To produce the most accurate approximation of the current lighting conditions, you can use data from multiple ambient light sensors.</span></span> <span data-ttu-id="d2c49-113">Dado que los sensores de luz ambiente se pueden ocultar parcial o totalmente a las sombras u objetos que cubren el sensor, varios sensores colocados a cierta distancia pueden proporcionar una aproximación mucho mejor de las condiciones de iluminación actuales que un solo sensor.</span><span class="sxs-lookup"><span data-stu-id="d2c49-113">Because ambient light sensors can be partly or fully obscured by shadows or objects that cover the sensor, multiple sensors placed some distance apart can provide a much better approximation of the current lighting conditions than a single sensor.</span></span>

<span data-ttu-id="d2c49-114">Para realizar un seguimiento de los datos procedentes de varios sensores, puede usar las dos técnicas siguientes:</span><span class="sxs-lookup"><span data-stu-id="d2c49-114">To keep track of the data coming from multiple sensors, you can use the following two techniques:</span></span>

-   <span data-ttu-id="d2c49-115">Se puede conservar el valor de datos más reciente de cada sensor de luz ambiente, junto con la marca de tiempo del informe de datos de sensor para cada una de estas lecturas.</span><span class="sxs-lookup"><span data-stu-id="d2c49-115">The most recent data value for each ambient light sensor can be retained, along with the time stamp from the sensor data report for each of these readings.</span></span> <span data-ttu-id="d2c49-116">Los últimos [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) recibidos por cada lectura de sensor se pueden conservar y pueden proporcionar ambos valores para una referencia posterior.</span><span class="sxs-lookup"><span data-stu-id="d2c49-116">The last [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) received for each sensor reading could be retained and could provide both values for later reference.</span></span> <span data-ttu-id="d2c49-117">Al hacer referencia a la marca de tiempo de cada informe de datos de sensor, los datos se pueden administrar en función de su antigüedad.</span><span class="sxs-lookup"><span data-stu-id="d2c49-117">By referring to the time stamp for each sensor data report, the data can be managed based on its age.</span></span> <span data-ttu-id="d2c49-118">Por ejemplo, si los datos tienen más de 2 segundos de antigüedad, se podría omitir.</span><span class="sxs-lookup"><span data-stu-id="d2c49-118">For example, if the data is more than 2 seconds old, it could be omitted.</span></span> <span data-ttu-id="d2c49-119">En función de los valores de datos del sensor más recientes, se podría usar la lectura más alta, ya que se consideraría que el sensor correspondiente no estuviera oculto.</span><span class="sxs-lookup"><span data-stu-id="d2c49-119">Based on the newer sensor data values, the highest reading could be used because the corresponding sensor would be presumed not to be obscured.</span></span>
-   <span data-ttu-id="d2c49-120">Puede usar el último valor del sensor de luz ambiente indicado.</span><span class="sxs-lookup"><span data-stu-id="d2c49-120">You can use the last ambient light sensor value reported.</span></span> <span data-ttu-id="d2c49-121">Esta implementación no sería óptima porque los valores de varios sensores no se comparan entre sí para obtener el resultado más preciso.</span><span class="sxs-lookup"><span data-stu-id="d2c49-121">This implementation would not be optimal because the values from multiple sensors are not compared to one another to obtain the most accurate result.</span></span> <span data-ttu-id="d2c49-122">No se recomienda este método.</span><span class="sxs-lookup"><span data-stu-id="d2c49-122">We do not recommend this method.</span></span>

## <a name="example-code"></a><span data-ttu-id="d2c49-123">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="d2c49-123">Example Code</span></span>

<span data-ttu-id="d2c49-124">En el ejemplo de código siguiente se muestra una implementación para el evento [**OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) .</span><span class="sxs-lookup"><span data-stu-id="d2c49-124">The following example code shows an implementation for the [**OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) event.</span></span> <span data-ttu-id="d2c49-125">El controlador de eventos llama a una función auxiliar, denominada **updateUI**, que cambia la interfaz de usuario basada en el valor Lux.</span><span class="sxs-lookup"><span data-stu-id="d2c49-125">The event handler calls a helper function, named **UpdateUI**, that changes the user interface based on the lux value.</span></span> <span data-ttu-id="d2c49-126">La escritura de la implementación de UpdateUI depende de usted.</span><span class="sxs-lookup"><span data-stu-id="d2c49-126">Writing the implementation of UpdateUI is up to you.</span></span>


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



 

 
