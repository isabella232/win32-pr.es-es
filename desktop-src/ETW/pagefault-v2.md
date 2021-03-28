---
description: Esta clase es la clase primaria para los eventos de error de página. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: cc349e75-fe81-427e-8cf9-15c76e8e4dad
title: PageFault_V2 (clase)
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
ms.openlocfilehash: a545e8ae7c5afb000c26d89d9359f620fa7a653d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984479"
---
# <a name="pagefault_v2-class"></a>\_Clase errores V2

Esta clase es la clase primaria para los eventos de error de página.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{3d6fa8d3-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class PageFault_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La clase **errores \_ V2** no define ningún miembro.

## <a name="remarks"></a>Observaciones

Para habilitar todos los eventos de error de página en una sesión de registro del kernel de NT, especifique la marca **Event \_ Trace \_ Flag \_ Memory \_ \_ faults** en el miembro **EnableFlags** de una estructura de [**propiedades de \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la función [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) . También puede especificar las marcas siguientes:

-   **\_ \_ \_ \_ errores severos de memoria de marca de seguimiento \_ de eventos**
-   **\_ \_ asignación virtual de marca de seguimiento de \_ eventos \_**

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para todos los eventos de error de página llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**PageFaultGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid* . Utilice los siguientes tipos de eventos para identificar el evento de memoria real al consumir eventos.



| Tipo de evento                                                     | Descripción                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo de seguimiento de evento \_ \_ \_ mm \_ Cow (el valor de tipo de evento es 12)<br/> | Evento de copia en escritura. La clase MOF [**errores \_ TypeGroup1**](pagefault-typegroup1.md) define los datos de evento para este evento. Antes de Windows Vista, la clase MOF [**errores \_ TransitionFault**](pagefault-transitionfault.md) define el evento.     |
| Tipo de seguimiento de eventos \_ \_ \_ mm \_ DZF (el valor de tipo de evento es 11)<br/> | Evento de error de petición cero. La clase MOF [**errores \_ TypeGroup1**](pagefault-typegroup1.md) define los datos de evento para este evento. Antes de Windows Vista, la clase MOF [**errores \_ TransitionFault**](pagefault-transitionfault.md) define el evento. |
| Tipo de seguimiento de eventos \_ \_ \_ mm \_ GPF (el valor de tipo de evento es 13)<br/> | Evento de error de página de protección. La clase MOF [**errores \_ TypeGroup1**](pagefault-typegroup1.md) define los datos de evento para este evento. Antes de Windows Vista, la clase MOF [**errores \_ TransitionFault**](pagefault-transitionfault.md) define el evento.  |
| Tipo de seguimiento de eventos \_ \_ \_ mm \_ HPF (el valor de tipo de evento es 14)<br/> | Evento de error de página de hardware. La clase MOF [**errores \_ TypeGroup1**](pagefault-typegroup1.md) define los datos de evento para este evento. Antes de Windows Vista, la clase MOF [**errores \_ TransitionFault**](pagefault-transitionfault.md) define el evento.   |
| Tipo de seguimiento de eventos \_ \_ \_ mm \_ TF (el valor de tipo de evento es 10)<br/>  | Evento de error de transición. La clase MOF [**errores \_ TypeGroup1**](pagefault-typegroup1.md) define los datos de evento para este evento. Antes de Windows Vista, la clase MOF [**errores \_ TransitionFault**](pagefault-transitionfault.md) define el evento.  |
| Tipo de seguimiento de evento \_ \_ \_ mm \_ AV (el valor de tipo de evento es 15)<br/>  | Evento de infracción de acceso. La clase MOF [**errores \_ TypeGroup1**](pagefault-typegroup1.md) define los datos de evento para este evento.                                                                                                                           |
| Valor del tipo de evento, 32                                           | Evento de error de página de hardware. La clase MOF [**errores \_ HardFault**](pagefault-hardfault.md) define los datos de evento para este evento.                                                                                                                               |
| Valor del tipo de evento, 105                                          | Carga de la imagen en el evento de archivo de paginación. La clase MOF [**errores \_ ImageLoadBacked**](pagefault-imageloadbacked.md) define los datos de evento para este evento.                                                                                                          |
| Valor del tipo de evento, 98                                           | Evento de asignación virtual. La clase [**VirtualAlloc**](pagefault-virtualalloc.md) de mof define los datos de evento para este evento.                                                                                                                                |
| Valor del tipo de evento, 99                                           | Evento gratuito virtual. La clase [**VirtualAlloc**](pagefault-virtualalloc.md) de mof define los datos de evento para este evento.                                                                                                                                      |



 

Puede usar los miembros **ProcessId** y **ThreadId** del [**encabezado de \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) para identificar el proceso o subproceso con errores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



 

 
