---
description: Esta clase es la clase primaria para los eventos de proceso. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: a505c693-2169-499b-bd32-42fa9bd69d2f
title: Process (clase)
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
ms.openlocfilehash: b014262044db9e227bec5af2b351d1392c243c23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985855"
---
# <a name="process-class"></a>Process (clase)

Esta clase es la clase primaria para los eventos de proceso.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Process : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La clase **Process** no define ningún miembro.

## <a name="remarks"></a>Observaciones

Para habilitar los eventos de procesamiento en una sesión de registro del kernel de NT, especifique la marca de  proceso de marca de seguimiento de eventos en el miembro EnableFlags [](/windows/win32/api/evntrace/nf-evntrace-starttracea) de una estructura de [**propiedades de \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la función StartTrace. **\_ \_ \_** También puede especificar la siguiente marca:

-   **\_ \_ \_ contadores del proceso de marca de seguimiento de eventos \_**

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para los eventos de proceso llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**ProcessGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid* . Utilice los siguientes tipos de eventos para identificar el evento de proceso real al consumir eventos.



| Tipo de evento                                                      | Descripción                                                                                                                                                                                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ de Tipo de seguimiento \_ \_ End**(el valor de tipo de evento es 2)<br/>   | Evento de finalización de proceso. La clase de MOF [**Process \_ TypeGroup1**](process-typegroup1.md) define los datos de evento para este evento.                                                                                                          |
| **Evento \_ de Tipo de seguimiento \_ \_ Start**(el valor del tipo de evento es 1)<br/> | Evento de inicio del proceso. La clase de MOF [**Process \_ TypeGroup1**](process-typegroup1.md) define los datos de evento para este evento.                                                                                                        |
| Valor del tipo de evento, 3                                             | Iniciar el evento del proceso de recopilación de datos. Enumera los procesos que se están ejecutando actualmente en el momento en que se inicia la sesión del kernel. La clase de MOF [**Process \_ TypeGroup1**](process-typegroup1.md) define los datos de evento para este evento. |
| Valor del tipo de evento, 4                                             | Evento finalizar proceso de recopilación de datos. Enumera los procesos que se están ejecutando actualmente en el momento en que finaliza la sesión del kernel. La clase de MOF [**Process \_ TypeGroup1**](process-typegroup1.md) define los datos de evento para este evento.     |



 

Los eventos de inicio de procesos y subprocesos pueden registrarse en el contexto del proceso o subproceso primario. Como resultado, es posible que los miembros **ProcessId** y **ThreadId** del [**encabezado de \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) no se correspondan con el proceso y el subproceso que se está creando. Este es el motivo por el que estos eventos contienen los identificadores de proceso y de subproceso en los datos de evento (además de los del encabezado de evento).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]<br/>       |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**Procesar \_ TypeGroup1**](process-typegroup1.md)
</dt> <dt>

[**Procesar \_ v0**](process-v0.md)
</dt> <dt>

[**Proceso \_ v1**](process-v1.md)
</dt> <dt>

[**Proceso \_ V2**](process-v2.md)
</dt> </dl>

 

 
