---
description: Esta clase es la clase de tipo de evento para los eventos de proceso. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: fcf2897d-32b4-42b9-892c-f0106687d3c2
title: Process_V0_TypeGroup1 (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V0_TypeGroup1
- Process_V0_TypeGroup1.ProcessId
- Process_V0_TypeGroup1.ParentId
- Process_V0_TypeGroup1.UserSID
- Process_V0_TypeGroup1.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2889feb05bfc396f2c2018ca59d2cf46fba8ec13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984511"
---
# <a name="process_v0_typegroup1-class"></a>Process \_ V0 \_ TypeGroup1 (clase)

Esta clase es la clase de tipo de evento para los eventos de proceso.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Process_V0_TypeGroup1 : Process_V0
{
  uint32 ProcessId;
  uint32 ParentId;
  object UserSID;
  string ImageFileName;
};
```

## <a name="members"></a>Miembros

La clase **Process \_ V0 \_ TypeGroup1** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **Process \_ V0 \_ TypeGroup1** tiene estas propiedades.

<dl> <dt>

ImageFileName
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (4), StringTermination ("NullTerminated")
</dt> </dl>

Ruta de acceso al archivo ejecutable del proceso.

</dd> <dt>

ParentId
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (2), puntero
</dt> </dl>

Identificador único del proceso que crea un proceso. Los números de identificador de proceso se reutilizan, por lo que solo identifican un proceso para la duración de ese proceso. Es posible que el proceso identificado por ParentProcessId termine, de modo que ParentProcessId no puede hacer referencia a un proceso en ejecución. También es posible que ParentProcessId haga referencia incorrectamente a un proceso que reutiliza un identificador de proceso.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (1), puntero
</dt> </dl>

Identificador de proceso global que puede usar para identificar un proceso. El valor es válido desde el momento en que se crea un proceso hasta que se termina.

</dd> <dt>

UserSID
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (3), extensión ("Sid")
</dt> </dl>

Identificador de seguridad (SID) del contexto de usuario en el que se produce el evento.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Procesar \_ v0**](process-v0.md)
</dt> </dl>

 

 




