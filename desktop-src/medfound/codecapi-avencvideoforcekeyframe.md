---
description: Fuerza al codificador a codificar el fotograma siguiente como un fotograma clave.
ms.assetid: 1E252967-6C28-4DA3-9E64-BD276E475753
title: CODECAPI_AVEncVideoForceKeyFrame propiedad (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d72c555d5680e822e9a8308b3e143a754eb22b89
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467213"
---
# <a name="codecapi_avencvideoforcekeyframe-property"></a>Propiedad CODECAPI \_ AVEncVideoForceKeyFrame

Fuerza al codificador a codificar el fotograma siguiente como un fotograma clave.

## <a name="data-type"></a>Tipo de datos

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoForceKeyFrame**

## <a name="property-value"></a>Valor de propiedad

Si el valor es distinto de cero, el codificador codificará el fotograma siguiente como un fotograma clave. Si el valor es cero, el codificador selecciona si se codifica el fotograma siguiente como un fotograma clave.

Esta propiedad se aplica al siguiente fotograma que el codificador recibe como entrada. Para una Media Foundation transformación de datos (MFT), este es el siguiente fotograma que se pasa al método [**IMFTransform::P rocessInput.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) La configuración se restablece a cero después del fotograma siguiente.

## <a name="remarks"></a>Observaciones

Esta propiedad también se usa con codificadores de cámara [H.264 UVC 1.5](camera-encoder-h264-uvc-1-5.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                     |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

