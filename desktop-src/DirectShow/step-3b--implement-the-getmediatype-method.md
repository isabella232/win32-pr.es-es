---
description: Paso 3B.
ms.assetid: 0ec57083-b192-404a-938f-bc6bb1cf0ddb
title: Paso 3B. Implementación del método GetMediaType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f386c16e3166f910e8221d139af519363d1b49279a412603e0cfddfa41773ede
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583115"
---
# <a name="step-3b-implement-the-getmediatype-method"></a>Paso 3B. Implementación del método GetMediaType

Este es el paso 3B del tutorial [Escribir filtros de transformación](writing-transform-filters.md).

> [!Note]  
> Este paso no es necesario para los filtros que derivan de **CTransInPlaceFilter.**

 

El [**método CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) devuelve uno de los tipos de salida preferidos del filtro, al que hace referencia el número de índice. Nunca se llama a este método a menos que la marca de entrada del filtro ya esté conectada. Por lo tanto, puede usar el tipo de medio de la conexión ascendente para determinar los tipos de salida preferidos.

Normalmente, un codificador ofrece un único tipo preferido, que representa el formato de destino. Por lo general, los descodificadores admiten una variedad de formatos de salida y los ofrecen en orden descendente de calidad o eficiencia. Por ejemplo, la lista podría ser UYVY, Y211, RGB-24, RGB-565, RGB-555 y RGB-8, en ese orden. Los filtros de efecto pueden requerir una coincidencia exacta entre el formato de salida y el formato de entrada.

En el ejemplo siguiente se devuelve un tipo de salida único, que se construye modificando el tipo de entrada para especificar la compresión RLE8:


```C++
HRESULT CRleFilter::GetMediaType(int iPosition, CMediaType *pMediaType)
{
    ASSERT(m_pInput->IsConnected());
    if (iPosition < 0)
    {
        return E_INVALIDARG;
    }
    if (iPosition == 0)
    {
        HRESULT hr = m_pInput->ConnectionMediaType(pMediaType);
        if (FAILED(hr))
        {
            return hr;
        }
        FOURCCMap fccMap = FCC('MRLE'); 
        pMediaType->subtype = static_cast<GUID>(fccMap);
        pMediaType->SetVariableSize();
        pMediaType->SetTemporalCompression(FALSE);

        ASSERT(pMediaType->formattype == FORMAT_VideoInfo);
        VIDEOINFOHEADER *pVih =
            reinterpret_cast<VIDEOINFOHEADER*>(pMediaType->pbFormat);
        pVih->bmiHeader.biCompression = BI_RLE8;
        pVih->bmiHeader.biSizeImage = DIBSIZE(pVih->bmiHeader); 
        return S_OK;
    }
    // else
    return VFW_S_NO_MORE_ITEMS;
}
```



En este ejemplo, el método llama [**a IPin::ConnectionMediaType para**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) obtener el tipo de entrada del pin de entrada. A continuación, cambia algunos de los campos para indicar el formato de compresión, como se indica a continuación:

-   Asigna un nuevo GUID de subtipo, que se construye a partir del código FOURCC "MRLE", mediante la [**clase FOURCCMap.**](fourccmap.md)
-   Llama al [**método CMediaType::SetVariableSize,**](cmediatype-setvariablesize.md) que establece la marca **bFixedSizeSamples** en **FALSE** y el miembro **lSampleSize** en cero, lo que indica ejemplos de tamaño variable.
-   Llama al [**método CMediaType::SetComposiciónCompression**](cmediatype-settemporalcompression.md) con el valor **FALSE**, lo que indica que cada fotograma es un fotograma clave. (Este campo solo es informativo, por lo que podría omitirlo de forma segura).
-   Establece el **campo biCompression** en BI \_ RLE8.
-   Establece el campo **biSizeImage** en el tamaño de la imagen.

Siguiente: [Paso 3C. Implementar el método CheckTransform](step-3c--implement-the-checktransform-method.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir DirectShow filtros](writing-directshow-filters.md)
</dt> </dl>

 

 



