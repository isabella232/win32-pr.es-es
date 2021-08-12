---
description: Paso 3A.
ms.assetid: 774fcb12-8928-4667-8ef6-dce86717cc29
title: Paso 3A. Implementación del método CheckInputType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692175e0def453f86b618a355044e4a117a4343fed56f029704091134e8bc31f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652145"
---
# <a name="step-3a-implement-the-checkinputtype-method"></a>Paso 3A. Implementación del método CheckInputType

Este es el paso 3A del tutorial Escribir [filtros de transformación](writing-transform-filters.md).

Se [**llama al método CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) cuando el filtro ascendente propone un tipo de medio al filtro de transformación. Este método toma un puntero a un [**objeto CMediaType,**](cmediatype.md) que es un contenedor fino para la [**estructura AM MEDIA \_ \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type) En este método, debe examinar todos los campos pertinentes de la estructura **\_ AM MEDIA \_ TYPE,** incluidos los campos del bloque de formato. Puede usar los métodos de accessor definidos en **CMediaType** o hacer referencia directamente a los miembros de la estructura. Si algún campo no es válido, devuelva VFW \_ E \_ TYPE NOT \_ \_ ACCEPTED. Si todo el tipo de medio es válido, devuelva S \_ OK.

Por ejemplo, en el filtro del codificador RLE, el tipo de entrada debe ser vídeo RGB de 8 o 4 bits sin comprimir. No hay ninguna razón para admitir otros formatos de entrada, como RGB de 16 o 24 bits, porque el [](color-space-converter-filter.md) filtro tendría que convertirlos a una profundidad de bits inferior y DirectShow ya proporciona un filtro convertidor de espacio de color para ese propósito. En el ejemplo siguiente se supone que el codificador admite vídeo de 8 bits, pero no vídeo de 4 bits:


```C++
HRESULT CRleFilter::CheckInputType(const CMediaType *mtIn)
{
    if ((mtIn->majortype != MEDIATYPE_Video) ||
        (mtIn->subtype != MEDIASUBTYPE_RGB8) ||
        (mtIn->formattype != FORMAT_VideoInfo) || 
        (mtIn->cbFormat < sizeof(VIDEOINFOHEADER)))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    VIDEOINFOHEADER *pVih = 
        reinterpret_cast<VIDEOINFOHEADER*>(mtIn->pbFormat);
    if ((pVih->bmiHeader.biBitCount != 8) ||
        (pVih->bmiHeader.biCompression != BI_RGB))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Check the palette table.
    if (pVih->bmiHeader.biClrUsed > PALETTE_ENTRIES(pVih))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    DWORD cbPalette = pVih->bmiHeader.biClrUsed * sizeof(RGBQUAD);
    if (mtIn->cbFormat < sizeof(VIDEOINFOHEADER) + cbPalette)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Everything is good.
    return S_OK;
}
```



En este ejemplo, el método comprueba primero el tipo principal y el subtipo. A continuación, comprueba el tipo de formato para asegurarse de que el bloque de formato es una [**estructura VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) El filtro también podría admitir [**VIDEOINFOHEADER2,**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)pero en este caso no habría ninguna ventaja real. La **estructura VIDEOINFOHEADER2** agrega compatibilidad con entrelazado y píxeles no cuadrados, que es probable que no sean pertinentes en vídeo de 8 bits.

Si el tipo de formato es correcto, en el ejemplo se comprueban los miembros **biBitCount** y **biCompression** de la estructura **VIDEOINFOHEADER** para comprobar que el formato es RGB sin comprimir de 8 bits. Como se muestra en este ejemplo, debe coaccion


```C++
pbFormat
```



puntero a la estructura correcta, según el tipo de formato. Compruebe siempre el guid de tipo de formato (**formattype**) y el tamaño del bloque de formato **(cbFormat**) antes de convertir el puntero.

En el ejemplo también se comprueba que el número de entradas de paleta es compatible con la profundidad de bits y que el bloque de formato es lo suficientemente grande como para contener las entradas de la paleta. Si toda esta información es correcta, el método devuelve S \_ OK.

Siguiente: [Paso 3B. Implementar el método GetMediaType](step-3b--implement-the-getmediatype-method.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir DirectShow filtros](writing-directshow-filters.md)
</dt> </dl>

 

 



