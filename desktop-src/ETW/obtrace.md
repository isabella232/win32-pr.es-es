---
description: Representa la clase primaria de la que se derivan todas las clases de seguimiento de eventos del administrador de objetos.
ms.assetid: 07cfc4a2-c665-4080-bc4b-fe9ec7191fdc
title: Clase ObTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObTrace
api_type:
- NA
api_location: ''
ms.openlocfilehash: ca89f58df9f5dd741da5b1fb8572b153c956cd43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815238"
---
# <a name="obtrace-class"></a>Clase ObTrace

Representa la clase primaria de la que se derivan todas las clases de seguimiento de eventos del administrador de objetos.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[DisplayName("Object"), Dynamic, EventVersion(2), Guid("{89497f50-effe-4440-8cf2-ce6b1cdcaca7}")]
class ObTrace : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La clase **ObTrace** no define ningún miembro.

## <a name="remarks"></a>Observaciones

Para habilitar el seguimiento de eventos del administrador de objetos, llame a la función [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) con el parámetro *InformationClass* igual al valor de enumeración de la [**clase de \_ información \_ de seguimiento**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) **TraceSystemTraceEnableFlagsInfo** y el miembro **EnableFlags** de la estructura de [**propiedades de \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) es igual al **identificador de rendimiento \_ OB \_** (0x80000040).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                   |
| MOF<br/>                      | <dl> <dt>Wmicore. mof</dt> </dl> |



 

 
