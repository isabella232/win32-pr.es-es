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
# <a name="implementing-a-preview-pin-optional"></a>Implementación de un PIN de versión preliminar (opcional)

En este tema se describe cómo implementar un PIN de vista previa en un filtro de captura de DirectShow.

Si el filtro tiene un PIN de vista previa, el PIN de vista previa debe enviar una copia de los datos entregados por el PIN de captura. Enviar solo los datos del PIN de vista previa al hacerlo no hará que el PIN de captura Coloque los fotogramas. El PIN de captura siempre tiene prioridad sobre el PIN de vista previa.

El PIN de captura y el PIN de vista previa deben enviar datos con el mismo formato. Por lo tanto, deben conectarse con tipos de medios idénticos. Si el PIN de captura se conecta primero, el PIN de vista previa debe ofrecer el mismo tipo de medio y rechazar los demás tipos. Si el PIN de vista previa se conecta primero y el PIN de captura se conecta a un tipo de medio diferente, el PIN de vista previa se debe volver a conectar con el nuevo tipo de medio. Si el filtro de nivel inferior del PIN de vista previa rechaza el nuevo tipo, el PIN de captura también debe rechazar el tipo. Use el método [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) para consultar el filtro de nivel inferior del PIN de vista previa y use el método [**IFilterGraph:: reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect) para volver a conectar el PIN. Estas reglas también se aplican si el administrador de gráficos de filtro vuelve a conectar el PIN de captura.

En el ejemplo siguiente se muestra un esquema de este proceso:


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo se conectan los filtros](how-filters-connect.md)
</dt> <dt>

[Escribir filtros de captura](writing-capture-filters.md)
</dt> </dl>

 

 



