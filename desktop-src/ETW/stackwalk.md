---
description: Esta clase es la clase primaria para los eventos de seguimiento de la pila.
ms.assetid: 3c0ff01b-fb37-4931-9484-ff8048abca66
title: Clase StackWalk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StackWalk
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2ad873815cb5cea40c1a9d2f694eca8d0e90d11b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984471"
---
# <a name="stackwalk-class"></a>Clase StackWalk

Esta clase es la clase primaria para los eventos de seguimiento de la pila.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{def2fe46-7bd6-4b80-bd94-f57fe20d0ce3}")]
class StackWalk : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La clase **StackWalk** no define ningún miembro.

## <a name="remarks"></a>Observaciones

Para habilitar el seguimiento de la pila de los eventos de kernel, llame a la función [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) y especifique los eventos y tipos de kernel para los que desea capturar el seguimiento de la pila. Para habilitar el seguimiento de la pila para otros eventos, establezca el miembro **EnableProperty** de [**habilitar \_ \_ parámetros de seguimiento**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) en **evento \_ habilitar \_ \_ \_ seguimiento** de la pila de propiedades.

Use el siguiente tipo de evento para identificar el evento real al consumir eventos.



| Tipo de evento           | Descripción                                                                                                           |
|----------------------|-----------------------------------------------------------------------------------------------------------------------|
| Valor del tipo de evento, 32 | Evento de seguimiento de la pila. La clase MOF del [**\_ evento StackWalk**](stackwalk-event.md) define los datos de evento para este evento. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/> |



 

 
