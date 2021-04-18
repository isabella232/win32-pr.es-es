---
description: Marca el marco actual como un marco LTR.
ms.assetid: D70A54D6-DA9B-40E5-B130-0AA9C5363DF0
title: Propiedad CODECAPI_AVEncVideoMarkLTRFrame (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a377f30aec049bc5cbc850ea03ace9dcc640bd6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539622"
---
# <a name="codecapi_avencvideomarkltrframe-property"></a>\_Propiedad AVEncVideoMarkLTRFrame de CODECAPI

Marca el marco actual como un marco LTR.

## <a name="data-type"></a>Tipo de datos

**ULong** (VT \_ UI4)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoMarkLTRFrame**

## <a name="remarks"></a>Observaciones

**Codificadores H. 264/AVC:**

El valor de este control es el valor de la sintaxis H. 264 *LongTermFramIdx* asociada al marco actual. Si el marco actual no está en el nivel base, por ejemplo, el *\_ identificador temporal* del elemento de sintaxis no es igual a 0, esta propiedad se aplica al siguiente marco de capa base en el orden de codificación.

No se debe llamar a esta propiedad si se ha emitido una llamada pendiente para marcar un marco LTR mediante la \_ propiedad CODECAPI AVEncVideoMarkLTRFrame y el codificador aún no ha marcado un fotograma como LTR. En otras palabras, el codificador no debe poner en cola \_ las solicitudes de CODECAPI AVEncVideoMarkLTRFrame. Si \_ se envía una solicitud de AVEncVideoMarkLTRFrame de CODECAPI mientras otra solicitud de CODECAPI \_ AVEncVideoMarkLTRFrame todavía está pendiente, se debe quitar la solicitud anterior.

La \_ propiedad CODECAPI AVEncVideoMarkLTRFrame es dinámica y se puede establecer durante la sesión de codificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]<br/>                                   |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




