---
description: 'Registry_V1 clase : esta clase es la clase primaria para los eventos del Registro. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: 7ad92377-3fd7-47e0-b96e-bab530ea9d99
title: Registry_V1 clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_V1
api_type:
- NA
api_location: ''
ms.openlocfilehash: 7c74a52793873a725c4b84e451818e07a49baf5c2839ddd38891a879cee6cb76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394183"
---
# <a name="registry_v1-class"></a>Registry \_ V1 (clase)

Esta clase es la clase primaria para los eventos del Registro.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{ae53722e-c863-11d2-8659-00c04fa321a1}"), EventVersion(1)]
class Registry_V1 : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La **clase \_ Registry V1** no define ningún miembro.

## <a name="remarks"></a>Comentarios

Para habilitar eventos del Registro en una sesión de registro del kernel de NT, especifique **EVENT \_ TRACE FLAG \_ \_ REGISTRY** en el **miembro EnableFlags** de una estructura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la [**función StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para eventos del Registro llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando **RegistryGuid** como *el parámetro pGuid.* Use los siguientes tipos de eventos para identificar el evento del Registro real al consumir eventos.



| Tipo de evento                                                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENT \_ TRACE \_ TYPE \_ REGCREATE**(el valor del tipo de evento es 10)<br/>             | Crear evento clave. La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento.                                                                                                                                                                                                                                                                                                                     |
| **EVENT \_ TRACE \_ TYPE \_ REGDELETE**(el valor del tipo de evento es 12)<br/>             | Evento de eliminación de clave. La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento.                                                                                                                                                                                                                                                                                                                     |
| **EVENT \_ TRACE \_ TYPE \_ REGDELETEVALUE**(el valor del tipo de evento es 15)<br/>        | Evento de eliminación de valor. La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento.                                                                                                                                                                                                                                                                                                                   |
| **EVENT \_ TRACE \_ TYPE \_ REGENUMERATEKEY**(el valor del tipo de evento es 17)<br/>       | Enumerar evento clave. La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento.                                                                                                                                                                                                                                                                                                                  |
| **EVENT \_ TRACE \_ TYPE \_ REGENUMERATEVALUEKEY**(el valor del tipo de evento es 18)<br/>  | Enumerar evento de clave de valor. La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento.                                                                                                                                                                                                                                                                                                            |
| **EVENT \_ TRACE \_ TYPE \_ REGFLUSH**(el valor del tipo de evento es 21)<br/>              | Evento de clave de vaciado. La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento.                                                                                                                                                                                                                                                                                                                      |
| **EVENT \_ TRACE \_ TYPE \_ REGKCBDMP**(el valor del tipo de evento es 22)<br/>             | Se genera cuando una operación del Registro usa identificadores en lugar de cadenas para hacer referencia a subclaves. Estos eventos se registran una vez para cada identificador, la primera vez que se hace referencia al identificador. Las referencias repetidas al identificador no generan varios eventos.<br/> La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento.<br/> **Windows 2000:** Este valor no se admite.<br/> |
| **EVENT \_ TRACE \_ TYPE \_ REGOPEN**(el valor del tipo de evento es 11)<br/>               | Evento de clave abierta. La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento.                                                                                                                                                                                                                                                                                                                       |
| **EVENT \_ TRACE \_ TYPE \_ REGQUERY**(el valor del tipo de evento es 13)<br/>              | Evento de clave de consulta. La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento.                                                                                                                                                                                                                                                                                                                      |
| **EVENT \_ TRACE \_ TYPE \_ REGQUERYMULTIPLEVALUE**(el valor del tipo de evento es 19)<br/> | Consulta de varios eventos de valor. La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento.                                                                                                                                                                                                                                                                                                           |
| **EVENT \_ TRACE \_ TYPE \_ REGQUERYVALUE**(el valor del tipo de evento es 16)<br/>         | Evento de valor de consulta. La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento.                                                                                                                                                                                                                                                                                                                    |
| **EVENT \_ TRACE \_ TYPE \_ REGSETINFORMATION**(el valor del tipo de evento es 20)<br/>     | Establecer evento de información. La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento.                                                                                                                                                                                                                                                                                                                |
| **EVENT \_ TRACE \_ TYPE \_ REGSETVALUE**(el valor del tipo de evento es 14)<br/>           | Evento de valor establecido. La [**clase \_ MOF Registry TypeGroup1**](registry-typegroup1.md) define los datos de evento para este evento.                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SystemTrace de MSNT \_**](msnt-systemtrace.md)
</dt> <dt>

[**Registro**](registry.md)
</dt> <dt>

[**Registro \_ V0**](registry-v0.md)
</dt> <dt>

[**\_TypeGroup1 del Registro V1 \_**](registry-v1-typegroup1.md)
</dt> </dl>

 

 
