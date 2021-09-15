---
description: En este tema se describe cómo implementar un pin de vista previa en un filtro DirectShow captura de datos.
ms.assetid: 60306702-97d4-4627-8fbe-e7c8750f3902
title: Implementar un pin de vista previa (opcional)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d1e09d070be2aa154428cb8684ff1c405fac959
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473979"
---
# <a name="implementing-a-preview-pin-optional"></a>Implementar un pin de vista previa (opcional)

En este tema se describe cómo implementar un pin de vista previa en un filtro DirectShow captura de datos.

Si el filtro tiene un pin de vista previa, el pin de vista previa debe enviar una copia de los datos entregados por el pin de captura. Enviar solo datos desde el pin de vista previa al hacerlo no hará que el pin de captura coloque fotogramas. El pin de captura siempre tiene prioridad sobre el pin de vista previa.

El pin de captura y el pin de vista previa deben enviar datos con el mismo formato. Por lo tanto, deben conectarse mediante tipos de medios idénticos. Si el pin de captura se conecta primero, el pin de vista previa debe ofrecer el mismo tipo de medio y rechazar cualquier otro tipo. Si el pin de vista previa se conecta primero y el pin de captura se conecta con un tipo de medio diferente, el pin de vista previa debe volver a conectarse con el nuevo tipo de medio. Si el filtro de nivel inferior del pin de vista previa rechaza el nuevo tipo, el pin de captura también debe rechazar el tipo. Use el [**método IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) para consultar el filtro de bajada desde el pin de vista previa y use el método [**IFilterGraph::Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect) para volver a conectar el pin. Estas reglas también se aplican si filter Graph Manager vuelve a conectar el pin de captura.

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

[Cómo se Conectar](how-filters-connect.md)
</dt> <dt>

[Escribir filtros de captura](writing-capture-filters.md)
</dt> </dl>

 

 



