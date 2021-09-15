---
description: Especifica si la secuencia de bits de vídeo codificada contiene un valor de integridad del búfer con cada fotograma clave.
ms.assetid: 5574ee3c-ccb3-4ff6-8280-efe5626e6dd6
title: MFPKEY_BUFFERFULLNESSINFIRSTBYTE propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10fbcdb6306faeb7481f1cc7be20088ff0cedd5b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468651"
---
# <a name="mfpkey_bufferfullnessinfirstbyte-property"></a>Propiedad \_ BUFFERFULLNESSINFIRSTBYTE de MFPKEY

Especifica si la secuencia de bits de vídeo codificada contiene un valor de integridad del búfer con cada fotograma clave.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCBufferFullnessInFirstByte

## <a name="data-type"></a>Tipo de datos

VT \_ BOOL

## <a name="remarks"></a>Observaciones

Debe establecer un tipo de salida antes de obtener este valor.

Puede obtener el valor de esta propiedad mediante [IWMCodecProps::GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop). Si usa **IPropertyBag**, primero debe establecer el valor FOURCC del formato comprimido deseado con la [propiedad \_ MFPKEY FOURCC.](mfpkey-fourccproperty.md)

Tener la integridad del búfer en el primer byte de todos los fotogramas clave le permite determinar el tamaño de búfer necesario al concatenar secuencias de vídeo comprimidas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




