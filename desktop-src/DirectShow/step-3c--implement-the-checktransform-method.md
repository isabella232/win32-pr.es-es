---
description: Paso 3C.
ms.assetid: e780df46-bf47-4334-b788-05ad8179f051
title: Paso 3C. Implementar el método CheckTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78148701fc54e73a6970d45fde95d70f4cf0df3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278825"
---
# <a name="step-3c-implement-the-checktransform-method"></a>Paso 3C. Implementar el método CheckTransform

Este es el paso 3C del tutorial [Writing Transform filters](writing-transform-filters.md).

> [!Note]  
> Este paso no es necesario para los filtros que derivan de **CTransInPlaceFilter**.

 

El método [**CTransformFilter:: CheckTransform**](ctransformfilter-checktransform.md) comprueba si un tipo de resultado propuesto es compatible con el tipo de entrada actual. También se llama al método si el PIN de entrada se vuelve a conectar después de que se conecte el PIN de salida.

En el ejemplo siguiente se comprueba si el formato es RLE8 video; las dimensiones de la imagen coinciden con el formato de entrada; y las entradas de la paleta son las mismas. También rechaza los rectángulos de origen y de destino que no coinciden con el tamaño de la imagen.


```C++
HRESULT CRleFilter::CheckTransform(
    const CMediaType *mtIn, const CMediaType *mtOut)
{
    // Check the major type.
    if (mtOut->majortype != MEDIATYPE_Video)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Check the subtype and format type.
    FOURCCMap fccMap = FCC('MRLE'); 
    if (mtOut->subtype != static_cast<GUID>(fccMap))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    if ((mtOut->formattype != FORMAT_VideoInfo) || 
        (mtOut->cbFormat < sizeof(VIDEOINFOHEADER)))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Compare the bitmap information against the input type.
    ASSERT(mtIn->formattype == FORMAT_VideoInfo);
    BITMAPINFOHEADER *pBmiOut = HEADER(mtOut->pbFormat);
    BITMAPINFOHEADER *pBmiIn = HEADER(mtIn->pbFormat);
    if ((pBmiOut->biPlanes != 1) ||
        (pBmiOut->biBitCount != 8) ||
        (pBmiOut->biCompression != BI_RLE8) ||
        (pBmiOut->biWidth != pBmiIn->biWidth) ||
        (pBmiOut->biHeight != pBmiIn->biHeight))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Compare source and target rectangles.
    RECT rcImg;
    SetRect(&rcImg, 0, 0, pBmiIn->biWidth, pBmiIn->biHeight);
    RECT *prcSrc = &((VIDEOINFOHEADER*)(mtIn->pbFormat))->rcSource;
    RECT *prcTarget = &((VIDEOINFOHEADER*)(mtOut->pbFormat))->rcTarget;
    if (!IsRectEmpty(prcSrc) && !EqualRect(prcSrc, &rcImg))
    {
        return VFW_E_INVALIDMEDIATYPE;
    }
    if (!IsRectEmpty(prcTarget) && !EqualRect(prcTarget, &rcImg))
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the palette table.
    if (pBmiOut->biClrUsed != pBmiIn->biClrUsed)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    DWORD cbPalette = pBmiOut->biClrUsed * sizeof(RGBQUAD);
    if (mtOut->cbFormat < sizeof(VIDEOINFOHEADER) + cbPalette)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    if (0 != memcmp(pBmiOut + 1, pBmiIn + 1, cbPalette))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Everything is good.
    return S_OK;
}
```



**Anclar reconexiones**

Las aplicaciones pueden desconectarse y volver a conectarse. Supongamos que una aplicación conecta ambos PIN, desconecta el PIN de entrada y, a continuación, vuelve a conectar el PIN de entrada con un nuevo tamaño de imagen. En ese caso, **CheckTransform** produce un error porque las dimensiones de la imagen ya no coinciden. Este comportamiento es razonable, aunque el filtro también podría intentar volver a conectar el PIN de salida con un nuevo tipo de medio.

Siguiente: [paso 4. Establecer propiedades de asignador](step-4--set-allocator-properties.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Volver a conectar PIN](reconnecting-pins.md)
</dt> <dt>

[Rectángulos de origen y de destino en representadores de vídeo](source-and-target-rectangles-in-video-renderers.md)
</dt> <dt>

[Escribir filtros de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



