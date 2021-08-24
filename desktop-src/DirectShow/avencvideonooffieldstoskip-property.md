---
description: Especifica el número de campos que se omitirán durante la codificación.
ms.assetid: 82f2a2c1-52ff-410d-b5da-b2419c0adfe3
title: Propiedad AVEncVideoNoOfFieldsToSkip (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 908a169b6f8ea868f7959afbd8fc90afa0b7a129b90674791990a156e67af948
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119342135"
---
# <a name="avencvideonooffieldstoskip-property"></a>Propiedad AVEncVideoNoOfFieldsToSkip

Especifica el número de campos que se omitirán durante la codificación.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT64** (**VT \_ UI8**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoNoOfFieldsToSkip**

## <a name="remarks"></a>Comentarios

En el caso del vídeo progresiva, establezca esta propiedad en el doble del número de fotogramas que se omitirán.

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

 

 




