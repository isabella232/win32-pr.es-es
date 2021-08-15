---
description: Especifica si la aplicación requiere un rendimiento de codificación en tiempo real.
ms.assetid: 7e98a9f4-113b-45d0-ae55-7dc3f2af099e
title: Propiedad AVEncCommonRealTime (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b718f4f58d230448689700fc2e681c109e645d48cb33eb1788e45ac607350951
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118403895"
---
# <a name="avenccommonrealtime-property"></a>Propiedad AVEncCommonRealTime

Especifica si la aplicación requiere un rendimiento de codificación en tiempo real.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncCommonRealTime**

## <a name="remarks"></a>Comentarios

Para especificar que la codificación debe realizarse en tiempo real, establezca esta propiedad en **VARIANT \_ TRUE.** Los códecs también pueden devolver esta propiedad como una funcionalidad.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional \[ aplicaciones de escritorio para \| UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




