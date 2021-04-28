---
description: 'Clase del Registro: esta clase es la clase primaria para los eventos del Registro. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: 362d7653-1ba0-45b7-80f3-0fccca0badf1
title: Clase del Registro
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry
api_type:
- NA
api_location: ''
ms.openlocfilehash: 23cd59e8d6afeb7578bd65625741caaae8156066
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106133"
---
# <a name="registry-class"></a>Clase del Registro

Esta clase es la clase primaria para los eventos del Registro.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{ae53722e-c863-11d2-8659-00c04fa321a1}"), EventVersion(2)]
class Registry : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La **clase Registry** no define ningún miembro.

## <a name="remarks"></a>Comentarios

Para habilitar eventos del Registro en una sesión de registro del kernel de NT, especifique **EVENT \_ TRACE FLAG \_ \_ REGISTRY** en el **miembro EnableFlags** de una estructura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la [**función StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para eventos del Registro llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**RegistryGuid**](nt-kernel-logger-constants.md) como *el parámetro pGuid.* Use los siguientes tipos de eventos para identificar el evento del Registro real al consumir eventos.



| Tipo de evento                                                                       | Descripción                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENT \_ TRACE \_ TYPE \_ REGCREATE**(el valor del tipo de evento es 10)<br/>             | Crear evento clave. La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento.                                                                                            |
| **EVENT \_ TRACE \_ TYPE \_ REGDELETE**(el valor del tipo de evento es 12)<br/>             | Evento de eliminación de clave. La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento.                                                                                            |
| **EVENT \_ TRACE \_ TYPE \_ REGDELETEVALUE**(el valor del tipo de evento es 15)<br/>        | Evento de eliminación de valor. La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento.                                                                                          |
| **EVENT \_ TRACE \_ TYPE \_ REGENUMERATEKEY**(el valor del tipo de evento es 17)<br/>       | Enumerar evento clave. La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento.                                                                                         |
| **EVENTO \_ TRACE \_ TYPE \_ REGENUMERATEVALUEKEY**(El valor del tipo de evento es 18)<br/>  | Enumerar evento de clave de valor. La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento.                                                                                   |
| **EVENTO \_ TRACE \_ TYPE \_ REGFLUSH**(el valor del tipo de evento es 21)<br/>              | Evento de clave de vaciado. La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento.                                                                                             |
| **EVENTO \_ TRACE \_ TYPE \_ REGKCBDMP**(el valor del tipo de evento es 22)<br/>             | Crear evento clave. Se genera cuando una operación del Registro usa identificadores en lugar de cadenas para hacer referencia a subclaves. La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento. |
| **EVENTO \_ TRACE \_ TYPE \_ REGOPEN**(el valor del tipo de evento es 11)<br/>               | Evento de clave abierta. La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento.                                                                                              |
| **EVENTO \_ TRACE \_ TYPE \_ REGQUERY**(el valor del tipo de evento es 13)<br/>              | Evento de clave de consulta. La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento.                                                                                             |
| **EVENTO \_ TRACE \_ TYPE \_ REGQUERYMULTIPLEVALUE**(El valor del tipo de evento es 19)<br/> | Consulta de varios eventos de valor. La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento.                                                                                  |
| **EVENT \_ TRACE \_ TYPE \_ REGQUERYVALUE**(el valor del tipo de evento es 16)<br/>         | Evento de valor de consulta. La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento.                                                                                           |
| **EVENT \_ TRACE \_ TYPE \_ REGSETINFORMATION**(el valor del tipo de evento es 20)<br/>     | Establecer evento de información. La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento.                                                                                       |
| **EVENT \_ TRACE \_ TYPE \_ REGSETVALUE**(el valor del tipo de evento es 14)<br/>           | Evento de valor establecido. La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento.                                                                                             |
| Valor de tipo de evento, 23                                                             | evento de eliminación de clave. Se genera cuando una operación del Registro usa identificadores en lugar de cadenas para hacer referencia a subclaves. La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento. |
| Valor de tipo de evento, 24                                                             | Enumera las claves del Registro abiertas al principio de la sesión. La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento.                                           |
| Valor de tipo de evento, 25                                                             | Enumera las claves del Registro abiertas al final de la sesión. La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento.                                                  |
| Valor de tipo de evento, 26                                                             | La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento.                                                                                                              |
| Valor del tipo de evento, 27                                                             | Evento de clave abierta. La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento.                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows \[ Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SystemTrace de MSNT \_**](msnt-systemtrace.md)
</dt> <dt>

[**Registry \_ TypeGroup1**](registry-typegroup1.md)
</dt> <dt>

[**Registro \_ V0**](registry-v0.md)
</dt> <dt>

[**Registro \_ V1**](registry-v1.md)
</dt> </dl>

 

 
