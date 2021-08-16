---
description: Fuerza al codificador a codificar el fotograma siguiente como fotograma clave.
ms.assetid: 1E252967-6C28-4DA3-9E64-BD276E475753
title: CODECAPI_AVEncVideoForceKeyFrame propiedad (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2e28738dcd7398ce04abe7f71778e94d7d5d4f49393365e92c43bbb347d98c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880711"
---
# <a name="codecapi_avencvideoforcekeyframe-property"></a>Propiedad CODECAPI \_ AVEncVideoForceKeyFrame

Fuerza al codificador a codificar el fotograma siguiente como fotograma clave.

## <a name="data-type"></a>Tipo de datos

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoForceKeyFrame**

## <a name="property-value"></a>Valor de propiedad

Si el valor es distinto de cero, el codificador codificará el fotograma siguiente como fotograma clave. Si el valor es cero, el codificador selecciona si se codifica el fotograma siguiente como fotograma clave.

Esta propiedad se aplica al fotograma siguiente que el codificador recibe como entrada. Para una Media Foundation transformación de datos (MFT), este es el siguiente fotograma que se pasa al método [**:P input.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) La configuración se restablece a cero después del fotograma siguiente.

## <a name="remarks"></a>Comentarios

Esta propiedad también se usa con codificadores de cámara [H.264 UVC 1.5.](camera-encoder-h264-uvc-1-5.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                     |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

