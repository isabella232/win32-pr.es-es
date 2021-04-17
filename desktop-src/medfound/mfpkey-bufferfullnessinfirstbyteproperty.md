---
description: Especifica si la secuencia de bits de vídeo codificada contiene un valor de llenado de búfer con cada fotograma clave.
ms.assetid: 5574ee3c-ccb3-4ff6-8280-efe5626e6dd6
title: Propiedad MFPKEY_BUFFERFULLNESSINFIRSTBYTE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10fbcdb6306faeb7481f1cc7be20088ff0cedd5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697698"
---
# <a name="mfpkey_bufferfullnessinfirstbyte-property"></a>\_Propiedad BUFFERFULLNESSINFIRSTBYTE de MFPKEY

Especifica si la secuencia de bits de vídeo codificada contiene un valor de llenado de búfer con cada fotograma clave.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCBufferFullnessInFirstByte

## <a name="data-type"></a>Tipo de datos

VT \_ bool

## <a name="remarks"></a>Observaciones

Debe establecer un tipo de salida antes de obtener este valor.

Puede obtener el valor de esta propiedad mediante [IWMCodecProps:: GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop). Si usa **IPropertyBag**, primero debe establecer el valor de FourCC del formato comprimido deseado con la propiedad [ \_ FourCC MFPKEY](mfpkey-fourccproperty.md) .

Tener el llenado del búfer en el primer byte de todos los fotogramas clave permite determinar el tamaño de búfer necesario al concatenar secuencias de vídeo comprimidas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




