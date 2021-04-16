---
description: Paso 3B.
ms.assetid: 0ec57083-b192-404a-938f-bc6bb1cf0ddb
title: Paso 3B. Implementar el método GetMediaType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab3ee41c6740fc2914f943784c0d51116f90428
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104547358"
---
# <a name="step-3b-implement-the-getmediatype-method"></a>Paso 3B. Implementar el método GetMediaType

Este es el paso 3B del tutorial de [escritura de filtros de transformación](writing-transform-filters.md).

> [!Note]  
> Este paso no es necesario para los filtros que derivan de **CTransInPlaceFilter**.

 

El método [**CTransformFilter:: GetMediaType**](ctransformfilter-getmediatype.md) devuelve uno de los tipos de salida preferidos del filtro, al que se hace referencia en el número de índice. Nunca se llama a este método a menos que el PIN de entrada del filtro ya esté conectado. Por lo tanto, puede usar el tipo de medio de la conexión de nivel superior para determinar los tipos de salida preferidos.

Un codificador suele ofrecer un único tipo preferido que representa el formato de destino. Los descodificadores generalmente admiten una variedad de formatos de salida y los ofrecen en orden de calidad o eficacia descendente. Por ejemplo, la lista puede ser UYVY, Y211, RGB-24, RGB-565, RGB-555 y RGB-8, en ese orden. Los filtros de efectos pueden requerir una coincidencia exacta entre el formato de salida y el formato de entrada.

En el ejemplo siguiente se devuelve un solo tipo de salida, que se construye modificando el tipo de entrada para especificar la compresión RLE8:


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



En este ejemplo, el método llama a [**IPin:: ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) para obtener el tipo de entrada del PIN de entrada. Después, cambia algunos de los campos para indicar el formato de compresión, como se indica a continuación:

-   Asigna un nuevo GUID de subtipo, que se construye a partir del código FOURCC ' MRLE ', mediante la clase [**FOURCCMap**](fourccmap.md) .
-   Llama al método [**CMediaType:: SetVariableSize**](cmediatype-setvariablesize.md) , que establece la marca **bFixedSizeSamples** en **false** y el miembro **lSampleSize** en cero, lo que indica ejemplos de tamaño variable.
-   Llama al método [**CMediaType:: SetTemporalCompression**](cmediatype-settemporalcompression.md) con el valor **false**, lo que indica que cada fotograma es un fotograma clave. (Este campo es meramente informativo, por lo que puede omitirlo sin ningún riesgo).
-   Establece el campo **bicompression** en RLE8 de BI \_ .
-   Establece el campo **biSizeImage** en el tamaño de la imagen.

Siguiente: [paso 3C. implemente el método CheckTransform](step-3c--implement-the-checktransform-method.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir filtros de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



