---
description: Filtros de controlador de clase WDM
ms.assetid: 864fc5ad-5aeb-4dc7-bdd2-2ad2bfb57741
title: Filtros de controlador de clase WDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338e4ec4d2aaa58bdac737b58571497cad708876
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908363"
---
# <a name="wdm-class-driver-filters"></a>Filtros de controlador de clase WDM

Si un dispositivo de captura usa un controlador de Modelo de controlador de Windows (WDM), es posible que el gráfico requiera ciertos filtros ascendentes desde el filtro de captura. Estos filtros se denominan filtros de controlador de clase de secuencia o filtros WDM. Admiten funcionalidad adicional proporcionada por el hardware. Por ejemplo, una tarjeta sintonizadora de TV tiene funciones para configurar el canal. El filtro correspondiente es el filtro de [sintonizador de TV](tv-tuner-filter.md) , que expone la interfaz [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) . Para que esta funcionalidad esté disponible para la aplicación, debe conectar el filtro de sintonizador de TV al filtro de captura.

La interfaz [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) proporciona la forma más sencilla de agregar filtros WDM al gráfico. En algún momento mientras se compila el gráfico, llame a [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) o [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream). Cualquiera de estos métodos buscará automáticamente los filtros WDM necesarios y los conectará al filtro de captura. En el resto de esta sección se describe cómo agregar filtros WDM manualmente. Sin embargo, tenga en cuenta que el enfoque recomendado es simplemente llamar a uno de estos métodos **ICaptureGraphBuilder2** .

Los pin de un filtro WDM admiten uno o más medios. Un medio define un método de comunicación, como un bus. Debe conectar las clavijas que admiten el mismo medio. La estructura [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) , que es equivalente a la **estructura \_ mediana KSPIN** utilizada para los controladores de streaming de kernel, define un medio en DirectShow. El miembro **clsMedium** de la estructura **REGPINMEDIUM** especifica el identificador de clase (CLSID) del medio. Para recuperar el medio de un PIN, llame al método [**IKsPin:: KsQueryMediums**](ikspin-ksquerymediums.md) . Este método devuelve un puntero a un bloque de memoria que contiene una estructura de [**\_ elementos KSMULTIPLE**](ksmultiple-item.md) , seguida de cero o más estructuras **REGPINMEDIUM** . Cada estructura **REGPINMEDIUM** identifica un medio que admite el PIN.

No conecte un PIN si el medio tiene un CLSID de GUID \_ null o KSMEDIUMSETID \_ estándar. Estos son los valores predeterminados que indican que el PIN no admite medios.

Además, no conecte un PIN a menos que el filtro requiera exactamente una instancia conectada de ese pin. De lo contrario, es posible que la aplicación intente conectar varios PIN que no deben tener conexiones, lo que puede hacer que el programa deje de responder. Para averiguar el número de instancias necesarias, recupere el \_ conjunto de propiedades KSPROPERTY PIN \_ NECESSARYINSTANCES, como se muestra en el ejemplo de código siguiente. (Para mayor brevedad, este ejemplo no prueba ningún código de retorno ni libera ninguna interfaz. Por supuesto, la aplicación debe hacer ambas cosas).


```C++
// Obtain the pin factory identifier.
IKsPinFactory *pPinFactory;
hr = pPin->QueryInterface(IID_IKsPinFactory, (void **)&pPinFactory);

ULONG ulFactoryId;
hr = pPinFactory->KsPinFactory(&ulFactoryId);

// Get the "instance" property from the filter.
IKsControl *pKsControl;
hr = pFilter->QueryInterface(IID_IKsControl, (void **)&pKsControl);

KSP_PIN ksPin;
ksPin.Property.Set = KSPROPSETID_Pin;
ksPin.Property.Id = KSPROPERTY_PIN_NECESSARYINSTANCES;
ksPin.Property.Flags = KSPROPERTY_TYPE_GET;
ksPin.PinId = ulFactoryId;
ksPin.Reserved = 0; 

KSPROPERTY ksProp;
ULONG ulInstances, bytes;
pKsControl->KsProperty((PKSPROPERTY)&ksPin, sizeof(ksPin), 
    &ulInstances, sizeof(ULONG), &bytes);

if (hr == S_OK && bytes == sizeof(ULONG)) 
{
    if (ulInstances == 1) 
    {
        // Filter requires one instance of this pin.
        // This pin is OK.
    } 
}
```



El siguiente pseudocódigo es un esquema muy breve que muestra cómo buscar y conectar los filtros WDM. Omite muchos detalles y solo está pensado para mostrar los pasos generales que debe realizar la aplicación.


```C++
Add supporting filters:
{
    foreach input pin:
        skip if (pin is connected)
    
        Get pin medium
        skip if (medium is GUID_NULL or KSMEDIUMSETID_Standard)
    
        Query filter for KSPROPERTY_PIN_NECESSARYINSTANCES property
        skip if (necessary instances != 1)

        Match an existing pin || Find a matching filter
}    

Match an existing pin:
{
    foreach filter in the graph
        foreach unconnected pin
            Get pin medium
            if (mediums match)
                connect the pins    
}

Find a matching filter:
{    
    Query the filter graph manager for IFilterMapper2.
    Find a filter with an output pin that matches the medium.
    Add the filter to the graph.
    Connect the pins.
    Add supporting filters. (Recursive call.)
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Temas de captura avanzada](advanced-capture-topics.md)
</dt> </dl>

 

 



