---
description: Esta clase es la clase primaria para los eventos de contador de rendimiento. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: 2606fea3-0651-4f7f-83a6-63021039eb95
title: PerfInfo (clase)
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
ms.openlocfilehash: 641ebb361d14fa8abb0c8199cf113cfd85a2e6700e262447c1302f3f1b66231a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151411"
---
# <a name="perfinfo-class"></a>PerfInfo (clase)

Esta clase es la clase primaria para los eventos de contador de rendimiento.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{ce1dbfb4-137e-4da6-87b0-3f59aa102cbc}"), EventVersion(2)]
class PerfInfo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La **clase PerfInfo** no define ningún miembro.

## <a name="remarks"></a>Comentarios

Para habilitar eventos de llamada a procedimiento diferido (DPC) en una sesión de registro de kernel de NT, especifique la marca **\_ \_ \_ DPC EVENT TRACE FLAG** en el miembro **EnableFlags** de una estructura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la [**función StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea) También puede especificar una o varias de las marcas siguientes:

-   **INTERRUPCIÓN \_ DE LA MARCA DE SEGUIMIENTO DE \_ \_ EVENTOS**
-   **PERFIL DE \_ MARCA DE SEGUIMIENTO DE \_ \_ EVENTOS**
-   **MARCA DE \_ SEGUIMIENTO \_ DE EVENTOS \_ SYSTEMCALL**

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para eventos DPC llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**PerfInfoGuid**](nt-kernel-logger-constants.md) como *parámetro pGuid.* Use los siguientes tipos de eventos para identificar el evento real al consumir eventos.



| Tipo de evento           | Descripción                                                                                                          |
|----------------------|----------------------------------------------------------------------------------------------------------------------|
| Valor del tipo de evento, 46 | Evento de perfil muestreado. La [**clase MOF SampledProfile**](sampledprofile.md) define los datos de evento para este evento. |
| Valor de tipo de evento, 51 | Evento enter de llamada del sistema. La [**clase MOF SysCallEnter**](syscallenter.md) define los datos de evento para este evento.   |
| Valor del tipo de evento, 52 | Evento de salida de llamada del sistema. La [**clase MOF SysCallExit**](syscallexit.md) define los datos de evento para este evento.      |
| Valor del tipo de evento, 66 | Evento DPC subproceso. La [**clase DPC**](dpc.md) MOF define los datos de evento para este evento.                          |
| Valor del tipo de evento, 67 | Evento de rutina de servicio de interrupción (ISR). La [**clase MOF**](isr.md) de ISR define los datos de evento para este evento.       |
| Valor de tipo de evento, 68 | Evento DPC. La [**clase DPC**](dpc.md) MOF define los datos de evento para este evento.                                   |
| Valor de tipo de evento, 69 | Evento de temporizador DPC. La [**clase DPC**](dpc.md) MOF define los datos de evento para este evento.                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 
