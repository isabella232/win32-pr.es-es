---
description: Especifica cómo reproduce el descodificador el audio mono dual.
ms.assetid: 3ef1f52c-13b2-4d9f-99fe-3317846be8a0
title: Propiedad AVDecAudioDualMonoReproMode (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71ebe7e003b2dc4b6eebc30901525ffb918a9a9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162154"
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

## <a name="remarks"></a>Observaciones

Esta propiedad solo se aplica cuando la secuencia de bits de entrada del descodificador contiene audio mono dual. Para probar esta condición, obtenga el valor de la [propiedad AVDecAudioDualMono.](avdecaudiodualmono-property.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| aplicaciones para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP de 2000 \[ \| Server\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




