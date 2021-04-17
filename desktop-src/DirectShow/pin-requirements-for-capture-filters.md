---
description: En este tema se describen los requisitos para implementar un PIN de salida en un filtro de captura de DirectShow.
ms.assetid: cb9cda1c-efa2-4abb-934b-21ba8cb80f30
title: Requisitos de PIN para los filtros de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a97d3e5c0f7fe0f5a9a341899651685df1cdd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686308"
---
# <a name="pin-requirements-for-capture-filters"></a><span data-ttu-id="91a39-103">Requisitos de PIN para los filtros de captura</span><span class="sxs-lookup"><span data-stu-id="91a39-103">Pin Requirements for Capture Filters</span></span>

<span data-ttu-id="91a39-104">En este tema se describen los requisitos para implementar un PIN de salida en un filtro de captura de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="91a39-104">This topic describes the requirements for implementing an output pin on a DirectShow capture filter.</span></span>

## <a name="pin-name"></a><span data-ttu-id="91a39-105">Nombre del pin</span><span class="sxs-lookup"><span data-stu-id="91a39-105">Pin Name</span></span>

<span data-ttu-id="91a39-106">Puede asignar un nombre a un PIN.</span><span class="sxs-lookup"><span data-stu-id="91a39-106">You can give a pin any name.</span></span> <span data-ttu-id="91a39-107">Si el nombre del anclaje comienza con el carácter de tilde (~), el administrador de gráficos de filtro no representará automáticamente ese pin cuando una aplicación llame a [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile).</span><span class="sxs-lookup"><span data-stu-id="91a39-107">If the pin name begins with the tilde (~) character, the Filter Graph Manager does not automatically render that pin when an application calls [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile).</span></span> <span data-ttu-id="91a39-108">Por ejemplo, si el filtro tiene un PIN de captura y un PIN de vista previa, puede asignarles el nombre "~ Capture" y "Preview", respectivamente.</span><span class="sxs-lookup"><span data-stu-id="91a39-108">For example, if the filter has a capture pin and a preview pin, you might name them "~Capture" and "Preview," respectively.</span></span> <span data-ttu-id="91a39-109">Si una aplicación representa ese filtro en un gráfico, el PIN de vista previa se conectará a su representador predeterminado y no se conectará nada al pin de captura, que es un comportamiento predeterminado razonable.</span><span class="sxs-lookup"><span data-stu-id="91a39-109">If an application renders that filter in a graph, the preview pin will connect to its default renderer, and nothing will connect to the capture pin, which is a reasonable default behavior.</span></span> <span data-ttu-id="91a39-110">Esto también se puede aplicar a los PIN que proporcionan datos informativos que no están diseñados para ser representados o PIN que necesitan propiedades personalizadas establecidas.</span><span class="sxs-lookup"><span data-stu-id="91a39-110">This can also apply to pins that deliver informational data that is not meant to be rendered, or pins that need custom properties set.</span></span> <span data-ttu-id="91a39-111">Tenga en cuenta que la aplicación puede seguir conectando manualmente los pin con el prefijo de tilde (~).</span><span class="sxs-lookup"><span data-stu-id="91a39-111">Note that pins with the tilde (~) prefix can still be connected manually by the application.</span></span>

## <a name="pin-category"></a><span data-ttu-id="91a39-112">Categoría de PIN</span><span class="sxs-lookup"><span data-stu-id="91a39-112">Pin Category</span></span>

<span data-ttu-id="91a39-113">Un filtro de captura siempre tiene un PIN de captura y puede tener un PIN de vista previa.</span><span class="sxs-lookup"><span data-stu-id="91a39-113">A capture filter always has a capture pin, and might have a preview pin.</span></span> <span data-ttu-id="91a39-114">Algunos filtros de captura pueden tener otros PIN de salida para ofrecer otros tipos de datos, como la información de control.</span><span class="sxs-lookup"><span data-stu-id="91a39-114">Some capture filters might have other output pins, to deliver other types of data, such as control information.</span></span> <span data-ttu-id="91a39-115">Cada terminal de salida debe exponer la interfaz [**IKsPropertySet**](ikspropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="91a39-115">Each output pin must expose the [**IKsPropertySet**](ikspropertyset.md) interface.</span></span> <span data-ttu-id="91a39-116">Las aplicaciones usan esta interfaz para determinar la categoría del PIN.</span><span class="sxs-lookup"><span data-stu-id="91a39-116">Applications use this interface to determine the pin category.</span></span> <span data-ttu-id="91a39-117">El PIN normalmente devuelve la \_ vista previa de la \_ captura de categoría de PIN o de la categoría de PIN \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="91a39-117">The pin typically returns either PIN\_CATEGORY\_CAPTURE or PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="91a39-118">Para obtener más información, vea [conjunto de propiedades de PIN](pin-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="91a39-118">For more information, see [Pin Property Set](pin-property-set.md).</span></span>

<span data-ttu-id="91a39-119">En el ejemplo siguiente se muestra cómo implementar [**IKsPropertySet**](ikspropertyset.md) para devolver la categoría PIN en un PIN de captura:</span><span class="sxs-lookup"><span data-stu-id="91a39-119">The following example shows how to implement [**IKsPropertySet**](ikspropertyset.md) to return the pin category on a capture pin:</span></span>


```C++
// Set: Cannot set any properties.
HRESULT CMyCapturePin::Set(REFGUID guidPropSet, DWORD dwID,
    void *pInstanceData, DWORD cbInstanceData, void *pPropData, 
    DWORD cbPropData)
{
    return E_NOTIMPL;
}

// Get: Return the pin category (our only property). 
HRESULT CMyCapturePin::Get(
    REFGUID guidPropSet,   // Which property set.
    DWORD dwPropID,        // Which property in that set.
    void *pInstanceData,   // Instance data (ignore).
    DWORD cbInstanceData,  // Size of the instance data (ignore).
    void *pPropData,       // Buffer to receive the property data.
    DWORD cbPropData,      // Size of the buffer.
    DWORD *pcbReturned     // Return the size of the property.
)
{
    if (guidPropSet != AMPROPSETID_Pin) 
        return E_PROP_SET_UNSUPPORTED;
    if (dwPropID != AMPROPERTY_PIN_CATEGORY)
        return E_PROP_ID_UNSUPPORTED;
    if (pPropData == NULL && pcbReturned == NULL)
        return E_POINTER;
    if (pcbReturned)
        *pcbReturned = sizeof(GUID);
    if (pPropData == NULL)  // Caller just wants to know the size.
        return S_OK;
    if (cbPropData < sizeof(GUID)) // The buffer is too small.
        return E_UNEXPECTED;
    *(GUID *)pPropData = PIN_CATEGORY_CAPTURE;
    return S_OK;
}

// QuerySupported: Query whether the pin supports the specified property.
HRESULT CMyCapturePin::QuerySupported(REFGUID guidPropSet, DWORD dwPropID,
    DWORD *pTypeSupport)
{
    if (guidPropSet != AMPROPSETID_Pin)
        return E_PROP_SET_UNSUPPORTED;
    if (dwPropID != AMPROPERTY_PIN_CATEGORY)
        return E_PROP_ID_UNSUPPORTED;
    if (pTypeSupport)
        // We support getting this property, but not setting it.
        *pTypeSupport = KSPROPERTY_SUPPORT_GET; 
    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="91a39-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="91a39-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91a39-121">Escribir filtros de captura</span><span class="sxs-lookup"><span data-stu-id="91a39-121">Writing Capture Filters</span></span>](writing-capture-filters.md)
</dt> </dl>

 

 



