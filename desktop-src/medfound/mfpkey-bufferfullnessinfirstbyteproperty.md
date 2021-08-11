---
description: Especifica si la secuencia de bits de vídeo codificada contiene un valor de integridad del búfer con cada fotograma clave.
ms.assetid: 5574ee3c-ccb3-4ff6-8280-efe5626e6dd6
title: MFPKEY_BUFFERFULLNESSINFIRSTBYTE propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 087b505680dfc3c51fe2cb50cdae76a425ca2ff5798356e9893794d47a7e22e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243004"
---
# <a name="mfpkey_bufferfullnessinfirstbyte-property"></a>Propiedad \_ BUFFERFULLNESSINFIRSTBYTE de MFPKEY

Especifica si la secuencia de bits de vídeo codificada contiene un valor de integridad del búfer con cada fotograma clave.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCBufferFullnessInFirstByte

## <a name="data-type"></a>Tipo de datos

VT \_ BOOL

## <a name="remarks"></a>Comentarios

Debe establecer un tipo de salida antes de obtener este valor.

Puede obtener el valor de esta propiedad mediante [IWMCodecProps::GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop). Si usa **IPropertyBag**, primero debe establecer el valor FOURCC del formato comprimido deseado con la [propiedad \_ MFPKEY FOURCC.](mfpkey-fourccproperty.md)

Tener la integridad del búfer en el primer byte de todos los fotogramas clave le permite determinar el tamaño de búfer necesario al concatenar secuencias de vídeo comprimidas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




