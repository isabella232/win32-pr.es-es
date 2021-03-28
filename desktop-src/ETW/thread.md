---
description: Esta clase es la clase primaria para los eventos de subproceso. La siguiente sintaxis se simplifica desde el código MOF.
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
ms.openlocfilehash: c4af87462607b675e46b3459a811925fbefe3ed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279667"
---
# <a name="thread-class"></a>Thread (clase)

Esta clase es la clase primaria para los eventos de subproceso.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Thread : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La clase **Thread** no define ningún miembro.

## <a name="remarks"></a>Observaciones

Para habilitar eventos de subproceso en una sesión de registro del kernel de NT, especifique la marca de **\_ \_ \_ subproceso de marca de seguimiento de eventos** en el miembro **EnableFlags** de una estructura de [**\_ \_ propiedades de seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la función [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para eventos de subprocesos llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**ThreadGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid* . Utilice los siguientes tipos de eventos para identificar el evento de subproceso real al consumir eventos.



| Tipo de evento                                                      | Descripción                                                                                                                                                                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ de Tipo de seguimiento \_ \_ End**(el valor de tipo de evento es 2)<br/>   | Evento de fin de subproceso. La clase de MOF [**Thread \_ TypeGroup1**](thread-typegroup1.md) define los datos de evento para este evento.                                                                                                        |
| **Evento \_ de Tipo de seguimiento \_ \_ Start**(el valor del tipo de evento es 1)<br/> | Evento de subproceso de inicio. La clase de MOF [**Thread \_ TypeGroup1**](thread-typegroup1.md) define los datos de evento para este evento.                                                                                                      |
| Valor del tipo de evento, 3                                             | Iniciar evento de subproceso de recopilación de datos. Enumera los subprocesos que se están ejecutando actualmente en el momento en que se inicia la sesión del kernel. La clase de MOF [**Thread \_ TypeGroup1**](thread-typegroup1.md) define los datos de evento para este evento. |
| Valor del tipo de evento, 4                                             | Evento End Data Collection Thread. Enumera los subprocesos que se están ejecutando actualmente en el momento en que finaliza la sesión del kernel. La clase de MOF [**Thread \_ TypeGroup1**](thread-typegroup1.md) define los datos de evento para este evento.     |



 

Los eventos de inicio de procesos y subprocesos pueden registrarse en el contexto del proceso o subproceso primario. Como resultado, es posible que los miembros **ProcessId** y **ThreadId** del [**encabezado de \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) no se correspondan con el proceso y el subproceso que se está creando. Este es el motivo por el que estos eventos contienen los identificadores de proceso y de subproceso en los datos de evento (además de los del encabezado de evento).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**Subproceso \_ TypeGroup1**](thread-typegroup1.md)
</dt> <dt>

[**Subproceso \_ v0**](thread-v0.md)
</dt> <dt>

[**Subproceso \_ v1**](thread-v1.md)
</dt> <dt>

[**Subproceso \_ V2**](thread-v2.md)
</dt> </dl>

 

 
