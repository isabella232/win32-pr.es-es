---
description: Obliga al codificador a codificar el siguiente fotograma como un fotograma clave.
ms.assetid: 1E252967-6C28-4DA3-9E64-BD276E475753
title: Propiedad CODECAPI_AVEncVideoForceKeyFrame (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d72c555d5680e822e9a8308b3e143a754eb22b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705423"
---
# <a name="codecapi_avencvideoforcekeyframe-property"></a>\_Propiedad AVEncVideoForceKeyFrame de CODECAPI

Obliga al codificador a codificar el siguiente fotograma como un fotograma clave.

## <a name="data-type"></a>Tipo de datos

**ULong** (VT \_ UI4)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoForceKeyFrame**

## <a name="property-value"></a>Valor de propiedad

Si el valor es distinto de cero, el codificador codificará el siguiente fotograma como un fotograma clave. Si el valor es cero, el codificador selecciona si se debe codificar el fotograma siguiente como un fotograma clave.

Esta propiedad se aplica al siguiente fotograma que el codificador recibe como entrada. En el caso de una transformación de Media Foundation (MFT), este es el siguiente fotograma que se pasa al método [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) . La configuración se restablece en cero después del fotograma siguiente.

## <a name="remarks"></a>Observaciones

Esta propiedad también se usa con [codificadores de cámara H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                     |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

