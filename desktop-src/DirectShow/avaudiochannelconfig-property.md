---
description: Obtiene la configuración del hablante de los canales de audio de la secuencia de bits de audio.
ms.assetid: ec13bb55-47af-4d79-9560-d297bce8e236
title: Propiedad AVAudioChannelConfig (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba9c497305292abeb34b86a7989fb05fbb872c898d10743ebd93b3982089e00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983795"
---
# <a name="avaudiochannelconfig-property"></a>Propiedad AVAudioChannelConfig

Obtiene la configuración del hablante de los canales de audio de la secuencia de bits de audio.

Esta propiedad es de solo lectura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVAudioChannelConfig**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad es un OR bit a bit de miembros de la [**enumeración eAVAudioChannelConfig.**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig)

## <a name="remarks"></a>Comentarios

El número de canales incluye el canal de efecto de baja frecuencia (LFE), si está presente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




