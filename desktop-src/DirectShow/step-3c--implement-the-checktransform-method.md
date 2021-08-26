---
description: Paso 3C.
ms.assetid: e780df46-bf47-4334-b788-05ad8179f051
title: Paso 3C. Implementación del método CheckTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 430ad933acfa7fc41a8b075183080e0b710a5d4780b55fa89cd4bf80984c1edc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075595"
---
# <a name="step-3c-implement-the-checktransform-method"></a>Paso 3C. Implementación del método CheckTransform

Este es el paso 3C del tutorial [Escribir filtros de transformación](writing-transform-filters.md).

> [!Note]  
> Este paso no es necesario para los filtros que derivan de **CTransInPlaceFilter**.

 

El [**método CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) comprueba si un tipo de salida propuesto es compatible con el tipo de entrada actual. También se llama al método si el pin de entrada se vuelve a conectar después de que se conecte el pin de salida.

En el ejemplo siguiente se comprueba si el formato es vídeo RLE8; las dimensiones de imagen coinciden con el formato de entrada; y las entradas de la paleta son las mismas. También rechaza los rectángulos de origen y destino que no coinciden con el tamaño de la imagen.


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

Las aplicaciones pueden desconectar y volver a conectar las clavijas. Supongamos que una aplicación conecta ambos pines, desconecta el pin de entrada y, a continuación, vuelve a conectar el pin de entrada con un nuevo tamaño de imagen. En ese caso, Se produce un error **en CheckTransform** porque las dimensiones de la imagen ya no coinciden. Este comportamiento es razonable, aunque el filtro también podría intentar volver a conectar el pin de salida con un nuevo tipo de medio.

Siguiente: [Paso 4. Establezca Propiedades del asignador](step-4--set-allocator-properties.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Volver a conectar los pines](reconnecting-pins.md)
</dt> <dt>

[Rectángulos de origen y destino en representadores de vídeo](source-and-target-rectangles-in-video-renderers.md)
</dt> <dt>

[Escribir DirectShow filtros](writing-directshow-filters.md)
</dt> </dl>

 

 



