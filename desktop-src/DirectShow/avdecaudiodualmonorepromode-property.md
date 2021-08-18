---
description: Especifica cómo reproduce el descodificador el audio mono dual.
ms.assetid: 3ef1f52c-13b2-4d9f-99fe-3317846be8a0
title: Propiedad AVDecAudioDualMonoReproMode (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9151ed6b996ec4ab92791221b7fb4c920913c818eac4a079ee6f40d04591a9db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917065"
---
# <a name="avdecaudiodualmonorepromode-property"></a>Propiedad AVDecAudioDualMonoReproMode

Especifica cómo reproduce el descodificador el audio mono dual.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecAudioDualMonoReproMode**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad es un miembro de la [**enumeración eAVDecAudioDualMonoReproMode.**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmonorepromode)

## <a name="remarks"></a>Comentarios

Esta propiedad solo se aplica cuando la secuencia de bits de entrada del descodificador contiene audio mono dual. Para probar esta condición, obtenga el valor de la [propiedad AVDecAudioDualMono.](avdecaudiodualmono-property.md)

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

 

 




