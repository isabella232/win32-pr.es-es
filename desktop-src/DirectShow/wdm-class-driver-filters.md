---
description: Filtros de controlador de clase WDM
ms.assetid: 864fc5ad-5aeb-4dc7-bdd2-2ad2bfb57741
title: Filtros de controlador de clase WDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338e4ec4d2aaa58bdac737b58571497cad708876
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272708"
---
# <a name="wdm-class-driver-filters"></a>Filtros de controlador de clase WDM

Si un dispositivo de captura usa un controlador Windows Driver Model (WDM), el gráfico podría requerir ciertos filtros ascendentes desde el filtro de captura. Estos filtros se denominan filtros de controlador de clase de flujo o filtros WDM. Admiten la funcionalidad adicional proporcionada por el hardware. Por ejemplo, una tarjeta de ajuste de TV tiene funciones para establecer el canal. El filtro correspondiente es el [filtro de tv tuner,](tv-tuner-filter.md) que expone la [**interfaz IAMTVTuner.**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) Para que esta funcionalidad esté disponible para la aplicación, debe conectar el filtro de tv Tuner al filtro de captura.

La [**interfaz ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) proporciona la manera más fácil de agregar filtros WDM al gráfico. En algún momento al compilar el gráfico, llame a [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) o [**RenderStream.**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) Cualquiera de estos métodos buscará automáticamente los filtros WDM necesarios y los conectará al filtro de captura. En el resto de esta sección se describe cómo agregar filtros WDM manualmente. Sin embargo, tenga en cuenta que el enfoque recomendado es simplemente llamar a uno de estos **métodos ICaptureGraphBuilder2.**

Los pines de un filtro WDM admiten uno o varios medios. Un medio define un método de comunicación, como un bus. Debe conectar los pines que admiten el mismo medio. La [**estructura REGPINMEDIUM,**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) que es equivalente a la estructura MEDIUM de **KSPIN \_** que se usa para los controladores de streaming de kernel, define un medio en DirectShow. El **miembro clsMedium** de la **estructura REGPINMEDIUM** especifica el identificador de clase (CLSID) para el medio. Para recuperar el medio de un pin, llame al [**método IKsPin::KsQueryMediums.**](ikspin-ksquerymediums.md) Este método devuelve un puntero a un bloque de memoria que contiene una estructura [**\_ ITEM KSMULTIPLE,**](ksmultiple-item.md) seguida de cero o más estructuras **REGPINMEDIUM.** Cada **estructura REGPINMEDIUM** identifica un medio que admite el pin.

No conecte un pin si el medio tiene un CLSID de GUID \_ NULL o KSMEDIUMSETID \_ Standard. Estos son los valores predeterminados que indican que el pin no admite medios.

Además, no conecte un pin a menos que el filtro requiera exactamente una instancia conectada de ese pin. De lo contrario, la aplicación podría intentar conectar varios pines que no deberían tener conexiones, lo que puede hacer que el programa deje de responder. Para averiguar el número de instancias necesarias, recupere el conjunto de propiedades NECESSARYINSTANCES del PIN de KSPROPERTY, como se muestra \_ en el ejemplo de código \_ siguiente. (Por brevedad, en este ejemplo no se prueba ningún código de retorno ni se libera ninguna interfaz. La aplicación debe hacer ambas cosas, por supuesto).


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



El siguiente seudocódigo es un esquema muy breve que muestra cómo buscar y conectar los filtros WDM. Omite muchos detalles y solo está diseñado para mostrar los pasos generales que la aplicación tendría que realizar.


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

 

 



