---
description: Velocidad de fotogramas de un tipo de medio de vídeo, en fotogramas por segundo.
ms.assetid: 8336559c-06f1-478e-b921-e9eae7425230
title: MF_MT_FRAME_RATE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8df2ef4268bd643d9f65eb16c3f7257bcaceb1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104423991"
---
# <a name="mf_mt_frame_rate-attribute"></a>MF \_ MT ( \_ atributo de velocidad de fotogramas) \_

Velocidad de fotogramas de un tipo de medio de vídeo, en fotogramas por segundo.

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="remarks"></a>Observaciones

La velocidad de fotogramas se expresa como una proporción. Los 32 superiores del valor del atributo contienen el numerador y los 32 bits inferiores contienen el denominador. Por ejemplo, si la velocidad de fotogramas es de 30 fotogramas por segundo (FPS), la relación es 30/1. Si la velocidad de fotogramas es 29,97 fps, la relación es 30000/1001.

Para establecer el valor, use la función [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) . Para obtener el valor, use la función [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) .

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se establece la velocidad de fotogramas en un tipo de medio de vídeo.


```
// Helper function to set the frame rate on a video media type.
inline HRESULT SetFrameRate(
    IMFMediaType *pType, 
    UINT32 numerator, 
    UINT32 denominator
    )
{
    return MFSetAttributeRatio(
        pType, 
        MF_MT_FRAME_RATE, 
        numerator, 
        denominator
        );
}
```



En el ejemplo siguiente se obtiene la velocidad de fotogramas de un tipo de medio de vídeo.


```
// Helper function to get the frame rate from a video media type.
inline HRESULT GetFrameRate(
    IMFMediaType *pType, 
    UINT32 *pNumerator, 
    UINT32 *pDenominator
    )
{
    return MFGetAttributeRatio(
        pType, 
        MF_MT_FRAME_RATE, 
        pNumerator, 
        pDenominator
        );
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]<br/>                              |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> <dt>

[**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate)
</dt> <dt>

[**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe)
</dt> </dl>

 

 




