---
description: Esta clase es la clase primaria para los eventos de contador de rendimiento. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 2606fea3-0651-4f7f-83a6-63021039eb95
title: Clase PerfInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PerfInfo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 93f12242fef86e5eab81bb702b783eb1f4c1915c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984514"
---
# <a name="perfinfo-class"></a>Clase PerfInfo

Esta clase es la clase primaria para los eventos de contador de rendimiento.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{ce1dbfb4-137e-4da6-87b0-3f59aa102cbc}"), EventVersion(2)]
class PerfInfo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La clase **PerfInfo** no define ningún miembro.

## <a name="remarks"></a>Observaciones

Para habilitar los eventos de llamada a procedimiento diferida (DPC) en una sesión de registro del kernel de NT, especifique la marca de DPC de la **marca de \_ seguimiento \_ \_ de eventos** en el miembro **EnableFlags** de una estructura de [**propiedades de \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la función [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) . También puede especificar una o varias de las marcas siguientes:

-   **\_interrupción de \_ marca de seguimiento de eventos \_**
-   **\_Perfil de \_ marca de seguimiento de eventos \_**
-   **marca de seguimiento de eventos \_ \_ \_ SYSTEMCALL**

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para los eventos de DPC llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**PerfInfoGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid* . Utilice los siguientes tipos de eventos para identificar el evento real al consumir eventos.



| Tipo de evento           | Descripción                                                                                                          |
|----------------------|----------------------------------------------------------------------------------------------------------------------|
| Valor del tipo de evento, 46 | Evento de perfil muestreado. La clase MOF [**SampledProfile**](sampledprofile.md) define los datos de evento para este evento. |
| Valor del tipo de evento, 51 | Evento de entrada de llamada del sistema. La clase MOF [**SysCallEnter**](syscallenter.md) define los datos de evento para este evento.   |
| Valor del tipo de evento, 52 | Evento de salida de llamada del sistema. La clase MOF [**SysCallExit**](syscallexit.md) define los datos de evento para este evento.      |
| Valor del tipo de evento, 66 | Evento de DPC de subproceso. La clase MOF de [**DPC**](dpc.md) define los datos de evento para este evento.                          |
| Valor del tipo de evento, 67 | Evento de la rutina de servicio de interrupción (ISR). La clase MOF de [**ISR**](isr.md) define los datos de evento para este evento.       |
| Valor del tipo de evento, 68 | Evento de DPC. La clase MOF de [**DPC**](dpc.md) define los datos de evento para este evento.                                   |
| Valor del tipo de evento, 69 | Evento de temporizador de DPC. La clase MOF de [**DPC**](dpc.md) define los datos de evento para este evento.                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 
