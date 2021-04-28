---
description: 'Clase de subproceso: esta clase es la clase primaria para los eventos de subproceso. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: 0bf14240-3b8d-4eb5-b751-7b2e23b55762
title: Thread (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread
api_type:
- NA
api_location: ''
ms.openlocfilehash: 121a8d4aa04017011648d80329ee02396582987a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105533"
---
# <a name="thread-class"></a>Thread (clase)

Esta clase es la clase primaria para los eventos de subproceso.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Thread : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La **clase Thread** no define ningún miembro.

## <a name="remarks"></a>Comentarios

Para habilitar eventos de subproceso en una sesión de registro del kernel de NT, especifique la marca **EVENT \_ TRACE FLAG \_ \_ THREAD** en el **miembro EnableFlags** de una estructura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la [**función StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para eventos de subproceso llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**ThreadGuid**](nt-kernel-logger-constants.md) como *parámetro pGuid.* Use los siguientes tipos de eventos para identificar el evento de subproceso real al consumir eventos.



| Tipo de evento                                                      | Descripción                                                                                                                                                                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENT \_ TRACE \_ TYPE \_ END**(el valor del tipo de evento es 2)<br/>   | Evento de subproceso final. La [**clase \_ MOF Thread TypeGroup1**](thread-typegroup1.md) define los datos de evento para este evento.                                                                                                        |
| **EVENT \_ TRACE \_ TYPE \_ START**(el valor del tipo de evento es 1)<br/> | Iniciar evento de subproceso. La [**clase \_ MOF Thread TypeGroup1**](thread-typegroup1.md) define los datos de evento para este evento.                                                                                                      |
| Valor de tipo de evento, 3                                             | Iniciar evento de subproceso de recopilación de datos. Enumera los subprocesos que se están ejecutando actualmente en el momento en que se inicia la sesión del kernel. La [**clase \_ MOF Thread TypeGroup1**](thread-typegroup1.md) define los datos de evento para este evento. |
| Valor de tipo de evento, 4                                             | Evento de subproceso de recopilación de datos final. Enumera los subprocesos que se están ejecutando actualmente en el momento en que finaliza la sesión del kernel. La [**clase \_ MOF Thread TypeGroup1**](thread-typegroup1.md) define los datos de evento para este evento.     |



 

Los eventos de inicio de procesos y subprocesos se pueden registrar en el contexto del proceso o subproceso primario. Como resultado, es posible que los **miembros ProcessId** y **ThreadId** de [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) no se correspondan con el proceso y el subproceso que se crean. Este es el motivo por el que estos eventos contienen los identificadores de proceso y subproceso en los datos del evento (además de los del encabezado de evento).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SystemTrace de MSNT \_**](msnt-systemtrace.md)
</dt> <dt>

[**Thread \_ TypeGroup1**](thread-typegroup1.md)
</dt> <dt>

[**Subproceso \_ V0**](thread-v0.md)
</dt> <dt>

[**Subproceso \_ V1**](thread-v1.md)
</dt> <dt>

[**Subproceso \_ V2**](thread-v2.md)
</dt> </dl>

 

 
