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
# <a name="wdm-class-driver-filters"></a><span data-ttu-id="3a6b1-103">Filtros de controlador de clase WDM</span><span class="sxs-lookup"><span data-stu-id="3a6b1-103">WDM Class Driver Filters</span></span>

<span data-ttu-id="3a6b1-104">Si un dispositivo de captura usa un controlador de Modelo de controlador de Windows (WDM), es posible que el gráfico requiera ciertos filtros ascendentes desde el filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="3a6b1-104">If a capture device uses a Windows Driver Model (WDM) driver, the graph might require certain filters upstream from the capture filter.</span></span> <span data-ttu-id="3a6b1-105">Estos filtros se denominan filtros de controlador de clase de secuencia o filtros WDM.</span><span class="sxs-lookup"><span data-stu-id="3a6b1-105">These filters are called stream-class driver filters or WDM filters.</span></span> <span data-ttu-id="3a6b1-106">Admiten funcionalidad adicional proporcionada por el hardware.</span><span class="sxs-lookup"><span data-stu-id="3a6b1-106">They support additional functionality provided by the hardware.</span></span> <span data-ttu-id="3a6b1-107">Por ejemplo, una tarjeta sintonizadora de TV tiene funciones para configurar el canal.</span><span class="sxs-lookup"><span data-stu-id="3a6b1-107">For example, a TV tuner card has functions for setting the channel.</span></span> <span data-ttu-id="3a6b1-108">El filtro correspondiente es el filtro de [sintonizador de TV](tv-tuner-filter.md) , que expone la interfaz [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) .</span><span class="sxs-lookup"><span data-stu-id="3a6b1-108">The corresponding filter is the [TV Tuner](tv-tuner-filter.md) filter, which exposes the [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) interface.</span></span> <span data-ttu-id="3a6b1-109">Para que esta funcionalidad esté disponible para la aplicación, debe conectar el filtro de sintonizador de TV al filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="3a6b1-109">To make this functionality available to the application, you must connect the TV Tuner filter to the capture filter.</span></span>

<span data-ttu-id="3a6b1-110">La interfaz [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) proporciona la forma más sencilla de agregar filtros WDM al gráfico.</span><span class="sxs-lookup"><span data-stu-id="3a6b1-110">The [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface provides the easiest way to add WDM filters to the graph.</span></span> <span data-ttu-id="3a6b1-111">En algún momento mientras se compila el gráfico, llame a [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) o [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).</span><span class="sxs-lookup"><span data-stu-id="3a6b1-111">At some point while building the graph, call [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) or [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).</span></span> <span data-ttu-id="3a6b1-112">Cualquiera de estos métodos buscará automáticamente los filtros WDM necesarios y los conectará al filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="3a6b1-112">Either one of these methods will automatically locate the necessary WDM filters and connect them to the capture filter.</span></span> <span data-ttu-id="3a6b1-113">En el resto de esta sección se describe cómo agregar filtros WDM manualmente.</span><span class="sxs-lookup"><span data-stu-id="3a6b1-113">The rest of this section describes how to add WDM filters manually.</span></span> <span data-ttu-id="3a6b1-114">Sin embargo, tenga en cuenta que el enfoque recomendado es simplemente llamar a uno de estos métodos **ICaptureGraphBuilder2** .</span><span class="sxs-lookup"><span data-stu-id="3a6b1-114">However, be aware that the recommend approach is simply to call one of these **ICaptureGraphBuilder2** methods.</span></span>

<span data-ttu-id="3a6b1-115">Los pin de un filtro WDM admiten uno o más medios.</span><span class="sxs-lookup"><span data-stu-id="3a6b1-115">The pins on a WDM filter support one or more mediums.</span></span> <span data-ttu-id="3a6b1-116">Un medio define un método de comunicación, como un bus.</span><span class="sxs-lookup"><span data-stu-id="3a6b1-116">A medium defines a method of communication, such as a bus.</span></span> <span data-ttu-id="3a6b1-117">Debe conectar las clavijas que admiten el mismo medio.</span><span class="sxs-lookup"><span data-stu-id="3a6b1-117">You must connect pins that support the same medium.</span></span> <span data-ttu-id="3a6b1-118">La estructura [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) , que es equivalente a la **estructura \_ mediana KSPIN** utilizada para los controladores de streaming de kernel, define un medio en DirectShow.</span><span class="sxs-lookup"><span data-stu-id="3a6b1-118">The [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) structure, which is equivalent to the **KSPIN\_MEDIUM** structure used for kernel streaming drivers, defines a medium in DirectShow.</span></span> <span data-ttu-id="3a6b1-119">El miembro **clsMedium** de la estructura **REGPINMEDIUM** especifica el identificador de clase (CLSID) del medio.</span><span class="sxs-lookup"><span data-stu-id="3a6b1-119">The **clsMedium** member of the **REGPINMEDIUM** structure specifies the class identifier (CLSID) for the medium.</span></span> <span data-ttu-id="3a6b1-120">Para recuperar el medio de un PIN, llame al método [**IKsPin:: KsQueryMediums**](ikspin-ksquerymediums.md) .</span><span class="sxs-lookup"><span data-stu-id="3a6b1-120">To retrieve a pin's medium, call the [**IKsPin::KsQueryMediums**](ikspin-ksquerymediums.md) method.</span></span> <span data-ttu-id="3a6b1-121">Este método devuelve un puntero a un bloque de memoria que contiene una estructura de [**\_ elementos KSMULTIPLE**](ksmultiple-item.md) , seguida de cero o más estructuras **REGPINMEDIUM** .</span><span class="sxs-lookup"><span data-stu-id="3a6b1-121">This method returns a pointer to a block of memory that contains a [**KSMULTIPLE\_ITEM**](ksmultiple-item.md) structure, followed by zero or more **REGPINMEDIUM** structures.</span></span> <span data-ttu-id="3a6b1-122">Cada estructura **REGPINMEDIUM** identifica un medio que admite el PIN.</span><span class="sxs-lookup"><span data-stu-id="3a6b1-122">Each **REGPINMEDIUM** structure identifies a medium the pin supports.</span></span>

<span data-ttu-id="3a6b1-123">No conecte un PIN si el medio tiene un CLSID de GUID \_ null o KSMEDIUMSETID \_ estándar.</span><span class="sxs-lookup"><span data-stu-id="3a6b1-123">Do not connect a pin if the medium has a CLSID of GUID\_NULL or KSMEDIUMSETID\_Standard.</span></span> <span data-ttu-id="3a6b1-124">Estos son los valores predeterminados que indican que el PIN no admite medios.</span><span class="sxs-lookup"><span data-stu-id="3a6b1-124">These are default values indicating that the pin does not support mediums.</span></span>

<span data-ttu-id="3a6b1-125">Además, no conecte un PIN a menos que el filtro requiera exactamente una instancia conectada de ese pin.</span><span class="sxs-lookup"><span data-stu-id="3a6b1-125">Also, do not connect a pin unless the filter requires exactly one connected instance of that pin.</span></span> <span data-ttu-id="3a6b1-126">De lo contrario, es posible que la aplicación intente conectar varios PIN que no deben tener conexiones, lo que puede hacer que el programa deje de responder.</span><span class="sxs-lookup"><span data-stu-id="3a6b1-126">Otherwise, your application might try to connect various pins that shouldn't have connections, which can cause the program to stop responding.</span></span> <span data-ttu-id="3a6b1-127">Para averiguar el número de instancias necesarias, recupere el \_ conjunto de propiedades KSPROPERTY PIN \_ NECESSARYINSTANCES, como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="3a6b1-127">To find out the number of required instances, retrieve the KSPROPERTY\_PIN\_NECESSARYINSTANCES property set, as shown in the following code example.</span></span> <span data-ttu-id="3a6b1-128">(Para mayor brevedad, este ejemplo no prueba ningún código de retorno ni libera ninguna interfaz.</span><span class="sxs-lookup"><span data-stu-id="3a6b1-128">(For brevity, this example does not test any return codes or release any interfaces.</span></span> <span data-ttu-id="3a6b1-129">Por supuesto, la aplicación debe hacer ambas cosas).</span><span class="sxs-lookup"><span data-stu-id="3a6b1-129">Your application should do both, of course.)</span></span>


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



<span data-ttu-id="3a6b1-130">El siguiente pseudocódigo es un esquema muy breve que muestra cómo buscar y conectar los filtros WDM.</span><span class="sxs-lookup"><span data-stu-id="3a6b1-130">The following pseudocode is an extremely brief outline showing how to find and connect the WDM filters.</span></span> <span data-ttu-id="3a6b1-131">Omite muchos detalles y solo está pensado para mostrar los pasos generales que debe realizar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3a6b1-131">It omits many details, and is only meant to show the general steps your application would need to take.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="3a6b1-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3a6b1-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a6b1-133">Temas de captura avanzada</span><span class="sxs-lookup"><span data-stu-id="3a6b1-133">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> </dl>

 

 



