---
description: Tipos de medios de vídeo sin comprimir
ms.assetid: 50bf2947-27ee-4092-9d3a-a1c13ee80e95
title: Tipos de medios de vídeo sin comprimir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69d01dab1179e0fc77872a7122e915e67c4c70dc98afd9586f02569c53e61547
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118057592"
---
# <a name="uncompressed-video-media-types"></a>Tipos de medios de vídeo sin comprimir

En este tema se describe cómo crear un tipo de medio que describe un formato de vídeo sin comprimir. Para obtener más información sobre los tipos de medios por lo general, vea [Acerca de los tipos de medios](about-media-types.md).

Para crear un tipo de vídeo sin comprimir completo, establezca los siguientes atributos en el puntero de [**interfaz DE LANMEDIATYPE.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)



| Atributo                                                                            | Descripción                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TIPO \_ PRINCIPAL DE MT \_ DE \_ MF**](mf-mt-major-type-attribute.md)                            | Tipo principal. Establezca en **MFMediaType \_ Video**.                                                                                                                                                                                          |
| [**\_SUBTIPO DE MT DE MF \_**](mf-mt-subtype-attribute.md)                                   | Subtipo. Consulte [GUID de subtipo de vídeo.](video-subtype-guids.md)                                                                                                                                                                        |
| [**MF \_ MT \_ DEFAULT \_ STRIDE**](mf-mt-default-stride-attribute.md)                    | Paso de superficie. El *paso es* el número de bytes necesarios para pasar de una fila de píxeles a la siguiente. Establezca este atributo si el paso en bytes no es el mismo que el ancho del vídeo en bytes. De lo contrario, puede omitir este atributo. |
| [**MF \_ MT \_ FRAME \_ RATE**](mf-mt-frame-rate-attribute.md)                            | Velocidad de fotogramas.                                                                                                                                                                                                                         |
| [**TAMAÑO \_ DEL MARCO DE MT \_ \_ DE MF**](mf-mt-frame-size-attribute.md)                            | Tamaño del marco.                                                                                                                                                                                                                         |
| [**MODO \_ DE \_ INTERLACE MF \_ MT**](mf-mt-interlace-mode-attribute.md)                    | Modo de entrelazado.                                                                                                                                                                                                                   |
| [**MF \_ MT \_ ALL \_ SAMPLES \_ INDEPENDENT**](mf-mt-all-samples-independent-attribute.md) | Especifica si cada muestra es independiente. Establezca en **TRUE para** formatos sin comprimir.                                                                                                                                             |
| [**RELACIÓN DE \_ ASPECTO \_ DE PÍXELES DE MT \_ DE \_ MF**](mf-mt-pixel-aspect-ratio-attribute.md)           | Relación de aspecto de píxeles.                                                                                                                                                                                                                 |



 

Además, establezca los siguientes atributos si conoce los valores correctos. (De lo contrario, omita estos atributos).



| Atributo                                                                    | Descripción        |
|------------------------------------------------------------------------------|--------------------|
| [**MF \_ MT \_ VIDEO \_ PRIMARIES**](mf-mt-video-primaries-attribute.md)          | Color principal.   |
| [**MF \_ MT \_ TRANSFER \_ FUNCTION**](mf-mt-transfer-function-attribute.md)      | Función de transferencia. |
| [**MF \_ MT \_ YUV \_ MATRIX**](mf-mt-yuv-matrix-attribute.md)                    | Matriz de transferencia.   |
| [**MF \_ MT \_ VIDEO \_ CHROMA \_ SITING**](mf-mt-video-chroma-siting-attribute.md) | Siting de siting de siting.     |
| [**MF \_ MT \_ VIDEO \_ NOMINAL \_ RANGE**](mf-mt-video-nominal-range-attribute.md) | Intervalo nominal.     |



 

Para obtener más información, vea [Información de color extendida](extended-color-information.md). Por ejemplo, si crea un tipo de medio que describe un estándar de vídeo y el estándar define el siting de la barra, agregue esta información al tipo de medio. Esto ayuda a conservar la fidelidad del color a lo largo de la canalización.

Las siguientes funciones pueden ser útiles al crear un tipo de medio de vídeo.



| Función                                                                     | Descripción                                                                                                                                                                          |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) | Calcula la velocidad de fotogramas, dada la duración media del fotograma.                                                                                                                         |
| [**MFCalculateImageSize**](/windows/desktop/api/mfapi/nf-mfapi-mfcalculateimagesize)                         | Calcula el tamaño de la imagen para un formato de vídeo sin comprimir.                                                                                                                          |
| [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) | Calcula la duración media de un fotograma de vídeo, dada la velocidad de fotogramas.                                                                                                              |
| [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader)     | Devuelve el paso de superficie mínimo para un formato de vídeo. Para obtener más información, vea [Image Stride](image-stride.md).                                                                   |
| [**MFInitVideoFormat**](/windows/desktop/api/mfapi/nf-mfapi-mfinitvideoformat)                               | Inicializa una estructura [**MFVIDEOFORMAT para**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat) algunos formatos de vídeo estándar, como televisión CLIP. A continuación, puede usar la estructura para inicializar un tipo de medio. |
| [**MFIsFormatYUV**](/windows/desktop/api/mfapi/nf-mfapi-mfisformatyuv)                                       | Consulta si un formato de vídeo es un formato YUV.                                                                                                                                      |



 

## <a name="examples"></a>Ejemplos

En este ejemplo se muestra una función que rellena la información más común para un formato de vídeo sin comprimir. La función devuelve un puntero [**de interfaz IMFMediaType.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) A continuación, puede agregar atributos adicionales al tipo de medio según sea necesario.


```C++
HRESULT CreateUncompressedVideoType(
    DWORD                fccFormat,  // FOURCC or D3DFORMAT value.     
    UINT32               width, 
    UINT32               height,
    MFVideoInterlaceMode interlaceMode,
    const MFRatio&       frameRate,
    const MFRatio&       par,
    IMFMediaType         **ppType
    )
{
    if (ppType == NULL)
    {
        return E_POINTER;
    }

    GUID    subtype = MFVideoFormat_Base;
    LONG    lStride = 0;
    UINT    cbImage = 0;

    IMFMediaType *pType = NULL;

    // Set the subtype GUID from the FOURCC or D3DFORMAT value.
    subtype.Data1 = fccFormat;

    HRESULT hr = MFCreateMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_SUBTYPE, subtype);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_INTERLACE_MODE, interlaceMode);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFSetAttributeSize(pType, MF_MT_FRAME_SIZE, width, height);
    if (FAILED(hr))
    {
        goto done;
    }

    // Calculate the default stride value.
    hr = pType->SetUINT32(MF_MT_DEFAULT_STRIDE, UINT32(lStride));
    if (FAILED(hr))
    {
        goto done;
    }

    // Calculate the image size in bytes.
    hr = MFCalculateImageSize(subtype, width, height, &cbImage);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_SAMPLE_SIZE, cbImage);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_FIXED_SIZE_SAMPLES, TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Frame rate
    hr = MFSetAttributeRatio(pType, MF_MT_FRAME_RATE, frameRate.Numerator, 
        frameRate.Denominator);
    if (FAILED(hr))
    {
        goto done;
    }

    // Pixel aspect ratio
    hr = MFSetAttributeRatio(pType, MF_MT_PIXEL_ASPECT_RATIO, par.Numerator, 
        par.Denominator);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppType = pType;
    (*ppType)->AddRef();

done:
    SafeRelease(&pType);
    return hr;
}
```



En el ejemplo siguiente se toma un formato de vídeo codificado como entrada y se crea un tipo de vídeo sin comprimir correspondiente. Este tipo sería adecuado para establecer en un codificador o descodificador, por ejemplo.


```C++
HRESULT ConvertVideoTypeToUncompressedType(
    IMFMediaType *pType,    // Pointer to an encoded video type.
    const GUID& subtype,    // Uncompressed subtype (eg, RGB-32, AYUV)
    IMFMediaType **ppType   // Receives a matching uncompressed video type.
    )
{
    IMFMediaType *pTypeUncomp = NULL;

    HRESULT hr = S_OK;
    GUID majortype = { 0 };
    MFRatio par = { 0 };

    hr = pType->GetMajorType(&majortype);

    if (majortype != MFMediaType_Video)
    {
        return MF_E_INVALIDMEDIATYPE;
    }

    // Create a new media type and copy over all of the items.
    // This ensures that extended color information is retained.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pTypeUncomp);
    }

    if (SUCCEEDED(hr))
    {
        hr = pType->CopyAllItems(pTypeUncomp);
    }

    // Set the subtype.
    if (SUCCEEDED(hr))
    {
        hr = pTypeUncomp->SetGUID(MF_MT_SUBTYPE, subtype);
    }

    // Uncompressed means all samples are independent.
    if (SUCCEEDED(hr))
    {
        hr = pTypeUncomp->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
    }

    // Fix up PAR if not set on the original type.
    if (SUCCEEDED(hr))
    {
        hr = MFGetAttributeRatio(
            pTypeUncomp, 
            MF_MT_PIXEL_ASPECT_RATIO, 
            (UINT32*)&par.Numerator, 
            (UINT32*)&par.Denominator
            );

        // Default to square pixels.
        if (FAILED(hr))
        {
            hr = MFSetAttributeRatio(
                pTypeUncomp, 
                MF_MT_PIXEL_ASPECT_RATIO, 
                1, 1
                );
        }
    }

    if (SUCCEEDED(hr))
    {
        *ppType = pTypeUncomp;
        (*ppType)->AddRef();
    }

    SafeRelease(&pTypeUncomp);
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información de color extendida](extended-color-information.md)
</dt> <dt>

[Image Stride](image-stride.md)
</dt> <dt>

[Tipos de medios](media-types.md)
</dt> <dt>

[Tipos de medios de vídeo](video-media-types.md)
</dt> <dt>

[GUID de subtipo de vídeo](video-subtype-guids.md)
</dt> </dl>

 

 



