---
description: En este tema se describe cómo implementar un PIN de vista previa en un filtro de captura de DirectShow.
ms.assetid: 60306702-97d4-4627-8fbe-e7c8750f3902
title: Implementación de un PIN de versión preliminar (opcional)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d1e09d070be2aa154428cb8684ff1c405fac959
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423008"
---
# <a name="implementing-a-preview-pin-optional"></a><span data-ttu-id="35b10-103">Implementación de un PIN de versión preliminar (opcional)</span><span class="sxs-lookup"><span data-stu-id="35b10-103">Implementing a Preview Pin (Optional)</span></span>

<span data-ttu-id="35b10-104">En este tema se describe cómo implementar un PIN de vista previa en un filtro de captura de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="35b10-104">This topic describes how to implement a preview pin on a DirectShow capture filter.</span></span>

<span data-ttu-id="35b10-105">Si el filtro tiene un PIN de vista previa, el PIN de vista previa debe enviar una copia de los datos entregados por el PIN de captura.</span><span class="sxs-lookup"><span data-stu-id="35b10-105">If your filter has a preview pin, the preview pin must send a copy of the data delivered by the capture pin.</span></span> <span data-ttu-id="35b10-106">Enviar solo los datos del PIN de vista previa al hacerlo no hará que el PIN de captura Coloque los fotogramas.</span><span class="sxs-lookup"><span data-stu-id="35b10-106">Only send data from the preview pin when doing so will not cause the capture pin to drop frames.</span></span> <span data-ttu-id="35b10-107">El PIN de captura siempre tiene prioridad sobre el PIN de vista previa.</span><span class="sxs-lookup"><span data-stu-id="35b10-107">The capture pin always has priority over the preview pin.</span></span>

<span data-ttu-id="35b10-108">El PIN de captura y el PIN de vista previa deben enviar datos con el mismo formato.</span><span class="sxs-lookup"><span data-stu-id="35b10-108">The capture pin and the preview pin must send data with the same format.</span></span> <span data-ttu-id="35b10-109">Por lo tanto, deben conectarse con tipos de medios idénticos.</span><span class="sxs-lookup"><span data-stu-id="35b10-109">Therefore, they must connect using identical media types.</span></span> <span data-ttu-id="35b10-110">Si el PIN de captura se conecta primero, el PIN de vista previa debe ofrecer el mismo tipo de medio y rechazar los demás tipos.</span><span class="sxs-lookup"><span data-stu-id="35b10-110">If the capture pin connects first, the preview pin should offer the same media type, and reject any others types.</span></span> <span data-ttu-id="35b10-111">Si el PIN de vista previa se conecta primero y el PIN de captura se conecta a un tipo de medio diferente, el PIN de vista previa se debe volver a conectar con el nuevo tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="35b10-111">If the preview pin connects first, and the capture pin connects with a different media type, the preview pin should reconnect using the new media type.</span></span> <span data-ttu-id="35b10-112">Si el filtro de nivel inferior del PIN de vista previa rechaza el nuevo tipo, el PIN de captura también debe rechazar el tipo.</span><span class="sxs-lookup"><span data-stu-id="35b10-112">If the filter downstream from the preview pin rejects the new type, the capture pin should also reject the type.</span></span> <span data-ttu-id="35b10-113">Use el método [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) para consultar el filtro de nivel inferior del PIN de vista previa y use el método [**IFilterGraph:: reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect) para volver a conectar el PIN.</span><span class="sxs-lookup"><span data-stu-id="35b10-113">Use the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method to query the filter downstream from the preview pin, and use the [**IFilterGraph::Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect) method to reconnect the pin.</span></span> <span data-ttu-id="35b10-114">Estas reglas también se aplican si el administrador de gráficos de filtro vuelve a conectar el PIN de captura.</span><span class="sxs-lookup"><span data-stu-id="35b10-114">These rules also apply if the Filter Graph Manager reconnects the capture pin.</span></span>

<span data-ttu-id="35b10-115">En el ejemplo siguiente se muestra un esquema de este proceso:</span><span class="sxs-lookup"><span data-stu-id="35b10-115">The following example shows an outline of this process:</span></span>


```C++
// Override CBasePin::CheckMediaType.
CCapturePin::CheckMediaType(CMediaType *pmt)
{
    if (m_pMyPreviewPin->IsConnected()) 
    {
        // The preview pin is already connected, so query the pin it is
        // connected to. If the other pin rejects it, so do we.
        hr = m_pMyPreviewPin->GetConnected()->QueryAccept(pmt);
        if (hr != S_OK) 
        {
            // The preview pin cannot reconnect with this media type.
            return E_INVALIDARG;
        }
        // The preview pin will reconnect when SetMediaType is called.
    }
    // Decide whether the capture pin accepts the format. 
    BOOL fAcceptThisType = ...  // (Not shown.)
    return (fAcceptThisType? S_OK : E_FAIL);
}

// Override CBasePin::SetMediaType.
CCapturePin::SetMediaType(CMediaType *pmt);
{
    if (m_pMyPreviewPin->IsConnected()) 
    {
        // The preview pin is already connected, so it must reconnect.
        if (m_pMyPreviewPin->GetConnected()->QueryAccept(pmt) == S_OK)
        {
            // The downstream pin will accept the new type, so it's safe
            // to reconnect. 
            m_pFilter->m_pGraph->Reconnect(m_pMyPreviewPin);
        }
        else
        {
            return VFW_E_INVALIDMEDIATYPE;
        }
    }
    // Now do anything that the capture pin needs to set the type.
    hr = MyInternalSetMediaType(pmt);

    // And finally, call the base-class method.
    return CBasePin::SetMediaType(pmt);
}

CPreviewPin::CheckMediaType(CMediaType *pmt)
{
    if (m_pMyCapturePin->IsConnected())
    {
       // The preview pin must connect with the same type.
       CMediaType cmt = m_pMyCapturePin->m_mt;
       return (*pmt == cmt ? S_OK : VFW_E_INVALIDMEDIATYPE);
    }
    // Decide whether the preview pin accepts the format. You can use your 
    // knowledge of which types the capture pin will accept. Regardless,
    // when the capture pin connects, the preview pin will reconnect.
    return (fAcceptThisType? S_OK : E_FAIL);
}
```



## <a name="related-topics"></a><span data-ttu-id="35b10-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="35b10-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35b10-117">Cómo se conectan los filtros</span><span class="sxs-lookup"><span data-stu-id="35b10-117">How Filters Connect</span></span>](how-filters-connect.md)
</dt> <dt>

[<span data-ttu-id="35b10-118">Escribir filtros de captura</span><span class="sxs-lookup"><span data-stu-id="35b10-118">Writing Capture Filters</span></span>](writing-capture-filters.md)
</dt> </dl>

 

 



