---
description: Especifica el rectángulo de origen para el mezclador de vídeo del representador de vídeo mejorado (EVR). El rectángulo de origen es la parte del fotograma de vídeo que el mezclador blits a la superficie de destino.
ms.assetid: 4364ff87-816e-4b64-b5e9-c53dd6c9bb33
title: VIDEO_ZOOM_RECT atributo (Evr.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dda4efca5beab844baf3b3f53074d6b3012e8621
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268604"
---
# <a name="video_zoom_rect-attribute"></a>Atributo VIDEO \_ ZOOM \_ RECT

Especifica el rectángulo de origen para el mezclador de vídeo del [representador de](enhanced-video-renderer.md) vídeo mejorado (EVR). El rectángulo de origen es la parte del fotograma de vídeo que el mezclador blits a la superficie de destino.

## <a name="data-type"></a>Tipo de datos

Byte array

## <a name="remarks"></a>Observaciones

El valor de este atributo es una [**estructura MFVideoNormalizedRect.**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect)

El rectángulo de origen se define en relación con un sistema de coordenadas normalizado, en el que todo el fotograma de vídeo ocupa un rectángulo con coordenadas {0, 0, 1, 1}. El rectángulo de origen debe caber dentro del marco de vídeo; las coordenadas del rectángulo de origen tienen un intervalo de (0...1).

El presentador de EVR estándar establece este atributo en el mezclador. Para establecer el atributo, haga lo siguiente:

1.  Llame [**a IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) en el mezclador para obtener el almacén de atributos del mezclador.
2.  Llame [**a IMFAttributes::SetBlob para**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob) establecer el atributo VIDEO ZOOM **\_ \_ RECT** en el mezclador. El valor es una [**estructura MFVideoNormalizedRect.**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect)

En un presentador de EVR personalizado, puede usar este atributo para implementar el [**método IMFVideoDisplayControl::SetVideoPosition.**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) Para obtener más información, vea [Rectángulos de origen y destino.](how-to-write-an-evr-presenter.md)

La constante GUID para este atributo se exporta desde strmiids.lib.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se establece el rectángulo de origen en el mezclador.


```C++
HRESULT SetMixerSourceRect(IMFTransform *pMixer, const MFVideoNormalizedRect& nrcSource)
{
    if (pMixer == NULL)
    {
        return E_POINTER;
    }

    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMixer->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetBlob(VIDEO_ZOOM_RECT, (const UINT8*)&nrcSource, sizeof(nrcSource));
        pAttributes->Release();
    }
    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                   |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Evr.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos mejorados del representador de vídeo](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Cómo escribir un presentador de EVR](how-to-write-an-evr-presenter.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**ATTRIBUTEAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> </dl>

 

 




