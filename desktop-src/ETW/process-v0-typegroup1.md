---
description: 'Process_V0_TypeGroup1 clase : esta clase es la clase de tipo de evento para los eventos de proceso. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: fcf2897d-32b4-42b9-892c-f0106687d3c2
title: Process_V0_TypeGroup1 clase
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
ms.openlocfilehash: 524d3c7da9f8ff76608da120834c5365eb1deb41
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106363"
---
# <a name="process_v0_typegroup1-class"></a>Clase \_ TypeGroup1 de Process V0 \_

Esta clase es la clase de tipo de evento para los eventos de proceso.

La sintaxis siguiente se simplifica a partir del código MOF.

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

La **clase Process \_ V0 \_ TypeGroup1** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ \_ TypeGroup1 Process V0** tiene estas propiedades.

<dl> <dt>

ImageFileName
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(4), StringTermination("NullTerminated")
</dt> </dl>

Ruta de acceso al archivo ejecutable del proceso.

</dd> <dt>

ParentId
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(2), Pointer
</dt> </dl>

Identificador único del proceso que crea un proceso. Los números de identificador de proceso se reutilizan, por lo que solo identifican un proceso para la duración de ese proceso. Es posible que el proceso identificado por ParentProcessId finalice, por lo que ParentProcessId puede no hacer referencia a un proceso en ejecución. También es posible que ParentProcessId hace referencia incorrectamente a un proceso que reutiliza un identificador de proceso.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(1), Pointer
</dt> </dl>

Identificador de proceso global que puede usar para identificar un proceso. El valor es válido desde el momento en que se crea un proceso hasta que finaliza.

</dd> <dt>

UserSID
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(3), Extension("Sid")
</dt> </dl>

Identificador de seguridad (SID) para el contexto de usuario en el que se produce el evento.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Proceso \_ V0**](process-v0.md)
</dt> </dl>

 

 




