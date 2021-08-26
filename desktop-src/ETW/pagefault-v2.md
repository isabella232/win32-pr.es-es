---
description: Esta clase es la clase primaria para los eventos de error de página. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: cc349e75-fe81-427e-8cf9-15c76e8e4dad
title: PageFault_V2 clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_V2
api_type:
- NA
api_location: ''
ms.openlocfilehash: bd8adfa698975f7661abdbd849136d04049b5539ff3fed3b52b61660791add0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900755"
---
# <a name="pagefault_v2-class"></a>PageFault \_ V2 (clase)

Esta clase es la clase primaria para los eventos de error de página.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{3d6fa8d3-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class PageFault_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La **clase PageFault \_ V2** no define ningún miembro.

## <a name="remarks"></a>Comentarios

Para habilitar todos los eventos de error de página en una sesión de registro del kernel de NT, especifique la marca **EVENT TRACE FLAG MEMORY PAGE \_ \_ \_ \_ \_ FAULTS** en el miembro **EnableFlags** de una estructura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la [**función StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea) También puede especificar las marcas siguientes:

-   **ERRORES \_ DE MEMORIA DE LA MARCA DE SEGUIMIENTO DE \_ \_ \_ \_ EVENTOS**
-   **\_ALOCACIÓN \_ VIRTUAL DE MARCA DE SEGUIMIENTO DE \_ \_ EVENTOS**

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para todos los eventos de error de página llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**PageFaultGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid.* Use los siguientes tipos de eventos para identificar el evento de memoria real al consumir eventos.



| Tipo de evento                                                     | Descripción                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EVENT \_ TRACE TYPE MM \_ \_ \_ COW(El valor del tipo de evento es 12)<br/> | Evento de copia en escritura. La [**clase MOF PageFault \_ TypeGroup1**](pagefault-typegroup1.md) define los datos de evento para este evento. Antes de Windows Vista, la [**clase MOF \_ PageFault TransitionFault**](pagefault-transitionfault.md) define el evento .     |
| EVENT \_ TRACE TYPE MM \_ \_ \_ DPF(El valor del tipo de evento es 11)<br/> | Evento de error de cero demanda. La [**clase MOF PageFault \_ TypeGroup1**](pagefault-typegroup1.md) define los datos de evento para este evento. Antes de Windows Vista, la [**clase MOF \_ PageFault TransitionFault**](pagefault-transitionfault.md) define el evento . |
| EVENT \_ TRACE TYPE MM \_ \_ \_ GPF(El valor del tipo de evento es 13)<br/> | Evento de error de página de protección. La [**clase MOF PageFault \_ TypeGroup1**](pagefault-typegroup1.md) define los datos de evento para este evento. Antes de Windows Vista, la [**clase MOF \_ PageFault TransitionFault**](pagefault-transitionfault.md) define el evento .  |
| EVENT \_ TRACE TYPE MM \_ \_ \_ HPF(El valor del tipo de evento es 14)<br/> | Evento de error de página dura. La [**clase MOF PageFault \_ TypeGroup1**](pagefault-typegroup1.md) define los datos de evento para este evento. Antes de Windows Vista, la [**clase MOF \_ PageFault TransitionFault**](pagefault-transitionfault.md) define el evento .   |
| EVENT \_ TRACE TYPE MM \_ \_ \_ TF(El valor del tipo de evento es 10)<br/>  | Evento de error de transición. La [**clase MOF PageFault \_ TypeGroup1**](pagefault-typegroup1.md) define los datos de evento para este evento. Antes de Windows Vista, la [**clase MOF \_ PageFault TransitionFault**](pagefault-transitionfault.md) define el evento .  |
| EVENT \_ TRACE TYPE MM \_ \_ \_ AV(El valor del tipo de evento es 15)<br/>  | Evento de infracción de acceso. La [**clase MOF PageFault \_ TypeGroup1**](pagefault-typegroup1.md) define los datos de evento para este evento.                                                                                                                           |
| Valor del tipo de evento, 32                                           | Evento de error de página dura. La [**clase MOF PageFault \_ HardFault**](pagefault-hardfault.md) define los datos de evento para este evento.                                                                                                                               |
| Valor de tipo de evento, 105                                          | Carga de imágenes en el evento de archivo de página. La [**clase MOF PageFault \_ ImageLoadBacked**](pagefault-imageloadbacked.md) define los datos de evento para este evento.                                                                                                          |
| Valor de tipo de evento, 98                                           | Evento de asignación virtual. La [**clase VirtualAlloc**](pagefault-virtualalloc.md) MOF define los datos de evento para este evento.                                                                                                                                |
| Valor de tipo de evento, 99                                           | Evento virtual gratuito. La [**clase VirtualAlloc**](pagefault-virtualalloc.md) MOF define los datos de evento para este evento.                                                                                                                                      |



 

Puede usar los miembros **ProcessId** y **ThreadId** de [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) para identificar el proceso o subproceso con errores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



 

 
