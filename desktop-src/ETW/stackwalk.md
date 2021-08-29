---
description: Esta clase es la clase primaria para los eventos de seguimiento de pila.
ms.assetid: 3c0ff01b-fb37-4931-9484-ff8048abca66
title: StackWalk (clase)
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
ms.openlocfilehash: 1a5245964cf6a87c6bb09be0f3f83aa30b1b9337a2a5238be873d90ade90ba91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746535"
---
# <a name="stackwalk-class"></a>StackWalk (clase)

Esta clase es la clase primaria para los eventos de seguimiento de pila.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{def2fe46-7bd6-4b80-bd94-f57fe20d0ce3}")]
class StackWalk : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La **clase StackWalk** no define ningún miembro.

## <a name="remarks"></a>Comentarios

Para habilitar el seguimiento de pila de eventos de kernel, llame a la función [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) y especifique los eventos y tipos de kernel para los que desea capturar el seguimiento de la pila. Para habilitar el seguimiento de pila para otros eventos, establezca el **miembro EnableProperty** de [**ENABLE TRACE \_ \_ PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) en **EVENT ENABLE PROPERTY STACK \_ \_ \_ \_ TRACE**.

Use el siguiente tipo de evento para identificar el evento real al consumir eventos.



| Tipo de evento           | Descripción                                                                                                           |
|----------------------|-----------------------------------------------------------------------------------------------------------------------|
| Valor de tipo de evento, 32 | Evento de seguimiento de pila. La [**clase StackWalk \_ Event**](stackwalk-event.md) MOF define los datos de evento para este evento. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



 

 
