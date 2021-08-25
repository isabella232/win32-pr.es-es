---
description: Marca el marco actual como un marco LTR.
ms.assetid: D70A54D6-DA9B-40E5-B130-0AA9C5363DF0
title: CODECAPI_AVEncVideoMarkLTRFrame propiedad (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a62f7bed0fd913dd17e06055ad259f4c8ed7037d90df2ecc53100e14ec4e505a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606435"
---
# <a name="codecapi_avencvideomarkltrframe-property"></a>Propiedad CODECAPI \_ AVEncVideoMarkLTRFrame

Marca el marco actual como un marco LTR.

## <a name="data-type"></a>Tipo de datos

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoMarkLTRFrame**

## <a name="remarks"></a>Comentarios

**Codificadores H.264/AVC:**

El valor de este control es el valor de la sintaxis de H.264 *LongTermFramIdx* asociada al marco actual. Si el marco actual no está en la capa base, por ejemplo, el identificador *temporal \_* del elemento de sintaxis no es igual a 0, esta propiedad se aplica al siguiente marco de capa base en orden de codificación.

No se debe llamar a esta propiedad si se ha emitido una llamada pendiente para marcar un marco LTR mediante la propiedad CODECAPI AVEncVideoMarkLTRFrame y el codificador aún no ha marcado un fotograma \_ como LTR. En otras palabras, el codificador no debe poner en cola las solicitudes CODECAPI \_ AVEncVideoMarkLTRFrame. Si se envía una solicitud CODECAPI AVEncVideoMarkLTRFrame mientras sigue pendiente otra solicitud \_ CODECAPI AVEncVideoMarkLTRFrame, se debe descartar la solicitud \_ anterior.

La propiedad CODECAPI \_ AVEncVideoMarkLTRFrame es dinámica y se puede establecer durante la sesión de codificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




