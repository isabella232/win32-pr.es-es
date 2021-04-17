---
description: Paso 3A.
ms.assetid: 774fcb12-8928-4667-8ef6-dce86717cc29
title: Paso 3A. Implementar el método CheckInputType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5eb6ff440838d7a4b65b586e5dba963ff254eef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678271"
---
# <a name="step-3a-implement-the-checkinputtype-method"></a>Paso 3A. Implementar el método CheckInputType

Este es el paso 3A del tutorial de [escritura de filtros de transformación](writing-transform-filters.md).

Se llama al método [**CTransformFilter:: CheckInputType**](ctransformfilter-checkinputtype.md) cuando el filtro de nivel superior propone un tipo de medio al filtro de transformación. Este método toma un puntero a un objeto [**CMediaType**](cmediatype.md) , que es un contenedor fino para la estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . En este método, debe examinar todos los campos pertinentes de la estructura de **\_ \_ tipo de medio am** , incluidos los campos del bloque de formato. Puede usar los métodos de descriptor de acceso definidos en **CMediaType** o hacer referencia a los miembros de la estructura directamente. Si un campo no es válido, devuelve el \_ tipo VFW E \_ \_ no \_ aceptado. Si el tipo de medio completo es válido, devuelva S \_ correctos.

Por ejemplo, en el filtro del codificador RLE, el tipo de entrada debe ser vídeo RGB sin comprimir de 8 bits o de 4 bits. No hay ninguna razón para admitir otros formatos de entrada, como RGB de 16 o 24 bits, ya que el filtro tendría que convertirlos a una profundidad de bits más baja y DirectShow ya proporciona un filtro de [convertidor de espacio de colores](color-space-converter-filter.md) para ese propósito. En el ejemplo siguiente se da por supuesto que el codificador admite vídeo de 8 bits, pero no vídeo de 4 bits:


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



En este ejemplo, el método comprueba primero el tipo y el subtipo principales. A continuación, comprueba el tipo de formato para asegurarse de que el bloque de formato es una estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) . El filtro también podría admitir [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2), pero en este caso no sería ninguna ventaja real. La estructura **VIDEOINFOHEADER2** agrega compatibilidad con el entrelazado y los píxeles no cuadrados, que es probable que no sean relevantes en el vídeo de 8 bits.

Si el tipo de formato es correcto, en el ejemplo se comprueban los miembros **biBitCount** y **bicompression** de la estructura **VIDEOINFOHEADER** para comprobar que el formato es RGB sin comprimir de 8 bits. Como se muestra en este ejemplo, debe forzar el


```C++
pbFormat
```



puntero a la estructura correcta, en función del tipo de formato. Compruebe siempre el GUID de tipo de formato (**formatType**) y el tamaño del bloque de formato (**cbFormat**) antes de convertir el puntero.

En el ejemplo también se comprueba que el número de entradas de la paleta es compatible con la profundidad de bits y que el bloque de formato es lo suficientemente grande como para contener las entradas de la paleta. Si toda esta información es correcta, el método devuelve S \_ correcto.

Siguiente: [paso 3B. implemente el método GetMediaType](step-3b--implement-the-getmediatype-method.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir filtros de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



