---
description: Esta clase es la clase primaria para los eventos del registro. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 7ad92377-3fd7-47e0-b96e-bab530ea9d99
title: Registry_V1 (clase)
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
ms.openlocfilehash: 320a2bce9213228be4ff5c1880d884ee9622b68c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984566"
---
# <a name="registry_v1-class"></a>Registry \_ v1 (clase)

Esta clase es la clase primaria para los eventos del registro.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{ae53722e-c863-11d2-8659-00c04fa321a1}"), EventVersion(1)]
class Registry_V1 : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La clase **Registry \_ v1** no define ningún miembro.

## <a name="remarks"></a>Observaciones

Para habilitar los eventos del registro en una sesión de registro del kernel de NT, especifique el registro  de la marca de seguimiento de **eventos \_ \_ \_** en el miembro EnableFlags de una estructura de [**propiedades de \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la función [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para los eventos del registro llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando **RegistryGuid** como parámetro *pGuid* . Utilice los siguientes tipos de eventos para identificar el evento de registro real al consumir eventos.



| Tipo de evento                                                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ de Tipo de seguimiento \_ \_ REGCREATE**(el valor del tipo de evento es 10)<br/>             | Evento de creación de clave. La clase [**del registro \_ TypeGroup1**](registry-typegroup1.md) mof define los datos de evento para este evento.                                                                                                                                                                                                                                                                                                                     |
| **Evento \_ de Tipo de seguimiento \_ \_ REGDELETE**(el valor de tipo de evento es 12)<br/>             | Evento de eliminación de clave. La clase [**del registro \_ TypeGroup1**](registry-typegroup1.md) mof define los datos de evento para este evento.                                                                                                                                                                                                                                                                                                                     |
| **Evento \_ de Tipo de seguimiento \_ \_ error en regdeletevalue**(el valor del tipo de evento es 15)<br/>        | Evento de valor de eliminación. La clase [**del registro \_ TypeGroup1**](registry-typegroup1.md) mof define los datos de evento para este evento.                                                                                                                                                                                                                                                                                                                   |
| **Evento \_ de Tipo de seguimiento \_ \_ REGENUMERATEKEY**(el valor del tipo de evento es 17)<br/>       | Evento de enumeración de clave. La clase [**del registro \_ TypeGroup1**](registry-typegroup1.md) mof define los datos de evento para este evento.                                                                                                                                                                                                                                                                                                                  |
| **Evento \_ de Tipo de seguimiento \_ \_ REGENUMERATEVALUEKEY**(el valor de tipo de evento es 18)<br/>  | Evento de clave de valor de enumeración. La clase [**del registro \_ TypeGroup1**](registry-typegroup1.md) mof define los datos de evento para este evento.                                                                                                                                                                                                                                                                                                            |
| **Evento \_ de Tipo de seguimiento \_ \_ REGFLUSH**(el valor de tipo de evento es 21)<br/>              | Evento de clave de vaciado. La clase [**del registro \_ TypeGroup1**](registry-typegroup1.md) mof define los datos de evento para este evento.                                                                                                                                                                                                                                                                                                                      |
| **Evento \_ de Tipo de seguimiento \_ \_ REGKCBDMP**(el valor del tipo de evento es 22)<br/>             | Se genera cuando una operación del registro utiliza identificadores en lugar de cadenas para hacer referencia a las subclaves. Estos eventos se registran una vez para cada identificador, la primera vez que se hace referencia al identificador. Las referencias repetidas al identificador no generan varios eventos.<br/> La clase [**del registro \_ TypeGroup1**](registry-typegroup1.md) mof define los datos de evento para este evento.<br/> **Windows 2000:** Este valor no se admite.<br/> |
| **Evento \_ de Tipo de seguimiento \_ \_ REGOPEN**(el valor de tipo de evento es 11)<br/>               | Evento de clave abierta. La clase [**del registro \_ TypeGroup1**](registry-typegroup1.md) mof define los datos de evento para este evento.                                                                                                                                                                                                                                                                                                                       |
| **Evento \_ de Tipo de seguimiento \_ \_ REGQUERY**(el valor de tipo de evento es 13)<br/>              | Evento de clave de consulta. La clase [**del registro \_ TypeGroup1**](registry-typegroup1.md) mof define los datos de evento para este evento.                                                                                                                                                                                                                                                                                                                      |
| **Evento \_ de Tipo de seguimiento \_ \_ REGQUERYMULTIPLEVALUE**(el valor del tipo de evento es 19)<br/> | Evento consultar varios valores. La clase [**del registro \_ TypeGroup1**](registry-typegroup1.md) mof define los datos de evento para este evento.                                                                                                                                                                                                                                                                                                           |
| **Evento \_ de Tipo de seguimiento \_ \_ REGQUERYVALUE**(el valor de tipo de evento es 16)<br/>         | Evento de valor de consulta. La clase [**del registro \_ TypeGroup1**](registry-typegroup1.md) mof define los datos de evento para este evento.                                                                                                                                                                                                                                                                                                                    |
| **Evento \_ de Tipo de seguimiento \_ \_ REGSETINFORMATION**(el valor de tipo de evento es 20)<br/>     | Evento de información de conjunto. La clase [**del registro \_ TypeGroup1**](registry-typegroup1.md) mof define los datos de evento para este evento.                                                                                                                                                                                                                                                                                                                |
| **Evento \_ de Tipo de seguimiento \_ \_ REGSETVALUE**(el valor del tipo de evento es 14)<br/>           | Evento de valor establecido. La clase [**del registro \_ TypeGroup1**](registry-typegroup1.md) mof define los datos de evento para este evento.                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**Registro**](registry.md)
</dt> <dt>

[**Registro \_ v0**](registry-v0.md)
</dt> <dt>

[**Registro \_ v1 \_ TypeGroup1**](registry-v1-typegroup1.md)
</dt> </dl>

 

 
