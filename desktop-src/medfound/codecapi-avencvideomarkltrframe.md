---
description: Marca el marco actual como un marco LTR.
ms.assetid: D70A54D6-DA9B-40E5-B130-0AA9C5363DF0
title: CODECAPI_AVEncVideoMarkLTRFrame propiedad (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a377f30aec049bc5cbc850ea03ace9dcc640bd6d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127269268"
---
# <a name="codecapi_avencvideomarkltrframe-property"></a>Propiedad CODECAPI \_ AVEncVideoMarkLTRFrame

Marca el marco actual como un marco LTR.

## <a name="data-type"></a>Tipo de datos

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoMarkLTRFrame**

## <a name="remarks"></a>Observaciones

**Codificadores H.264/AVC:**

El valor de este control es el valor de la sintaxis H.264 *LongTermFramIdx* asociada al marco actual. Si el marco actual no está en la capa base, por ejemplo, el identificador *temporal \_* del elemento de sintaxis no es igual a 0, esta propiedad se aplica al siguiente marco de capa base en orden de codificación.

No se debe llamar a esta propiedad si se ha emitido una llamada pendiente para marcar un marco LTR mediante la propiedad CODECAPI AVEncVideoMarkLTRFrame y el codificador aún no ha marcado un marco \_ como LTR. En otras palabras, el codificador no debe poner en cola las solicitudes CODECAPI \_ AVEncVideoMarkLTRFrame. Si se envía una solicitud \_ CODECAPI AVEncVideoMarkLTRFrame mientras hay otra solicitud CODECAPI AVEncVideoMarkLTRFrame pendiente, se debe descartar la solicitud \_ anterior.

La propiedad CODECAPI \_ AVEncVideoMarkLTRFrame es dinámica y se puede establecer durante la sesión de codificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| para aplicaciones para UWP\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




