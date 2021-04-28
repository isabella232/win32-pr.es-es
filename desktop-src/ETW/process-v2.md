---
description: 'Process_V2 clase : esta clase es la clase primaria para los eventos de proceso. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: 75596278-43cc-4040-a43d-6958d0935b68
title: Process_V2 clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process
api_type:
- NA
api_location: ''
ms.openlocfilehash: 77d700e7847d0ad19a019985a4e19343ce8f383d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106303"
---
# <a name="process_v2-class"></a>Clase Process \_ V2

Esta clase es la clase primaria para los eventos de proceso.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class Process_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La **clase Process** no define ningún miembro.

## <a name="remarks"></a>Comentarios

Para habilitar los eventos de proceso en una sesión de registro del kernel de NT, especifique la marca **EVENT \_ TRACE FLAG \_ \_ PROCESS** en el **miembro EnableFlags** de una estructura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la [**función StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea) También puede especificar la marca siguiente:

-   **CONTADORES \_ DE PROCESO DE MARCA DE SEGUIMIENTO DE \_ \_ \_ EVENTOS**

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para eventos de proceso llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**ProcessGuid**](nt-kernel-logger-constants.md) como *parámetro pGuid.* Use los siguientes tipos de eventos para identificar el evento de proceso real al consumir eventos.



| Tipo de evento                                                      | Descripción                                                                                                                                                                                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENT \_ TRACE \_ TYPE \_ END**(el valor del tipo de evento es 2)<br/>   | Evento de proceso final. La [**clase \_ MOF Process TypeGroup1**](process-typegroup1.md) define los datos de evento para este evento.                                                                                                          |
| **EVENT \_ TRACE \_ TYPE \_ START**(el valor del tipo de evento es 1)<br/> | Evento de inicio del proceso. La [**clase \_ MOF Process TypeGroup1**](process-typegroup1.md) define los datos de evento para este evento.                                                                                                        |
| Valor de tipo de evento, 3                                             | Evento de inicio del proceso de recopilación de datos. Enumera los procesos que se están ejecutando actualmente en el momento en que se inicia la sesión del kernel. La [**clase \_ MOF Process TypeGroup1**](process-typegroup1.md) define los datos de evento para este evento. |
| Valor de tipo de evento, 4                                             | Evento de proceso de recopilación de datos final. Enumera los procesos que se están ejecutando actualmente en el momento en que finaliza la sesión del kernel. La [**clase \_ MOF Process TypeGroup1**](process-typegroup1.md) define los datos de evento para este evento.     |
| Valor del tipo de evento, 32                                            | Evento de contadores de rendimiento. La [**clase \_ MOF Process V2 \_ TypeGroup2**](process-v2-typegroup2.md) define los datos de evento para este evento.                                                                                          |
| Valor del tipo de evento, 33                                            | Resumen de los contadores de rendimiento al principio de la sesión. La [**clase \_ MOF Process V2 \_ TypeGroup2**](process-v2-typegroup2.md) define los datos de evento para este evento.                                                     |
| Valor del tipo de evento, 39                                            | Evento de proceso en desa desarrollo. La [**clase \_ MOF Process TypeGroup1**](process-typegroup1.md) define los datos de evento para este evento.                                                                                                      |



 

Los eventos de inicio de procesos y subprocesos se pueden registrar en el contexto del proceso o subproceso primario. Como resultado, es posible que los **miembros ProcessId** y **ThreadId** de [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) no se correspondan con el proceso y el subproceso que se crean. Este es el motivo por el que estos eventos contienen los identificadores de proceso y subproceso en los datos del evento (además de los del encabezado de evento).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Aplicaciones de escritorio de Windows Vista \[ \| para aplicaciones para UWP\]<br/>       |
| Servidor mínimo compatible<br/> | Aplicaciones de escritorio de Windows Server 2008 \[ \| aplicaciones para UWP\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SystemTrace de MSNT \_**](msnt-systemtrace.md)
</dt> <dt>

[**Proceso**](process.md)
</dt> <dt>

[**Process \_ TypeGroup1**](process-typegroup1.md)
</dt> <dt>

[**Proceso \_ V0**](process-v0.md)
</dt> <dt>

[**Proceso \_ V1**](process-v1.md)
</dt> </dl>

 

 
