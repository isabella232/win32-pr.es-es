---
description: 'Process_TypeGroup1 clase : esta clase es la clase de tipo de evento para los eventos de proceso. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: 4f06e1af-3f9a-4346-aa50-50f3ee82cd98
title: Process_TypeGroup1 clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_TypeGroup1
- Process_TypeGroup1.UniqueProcessKey
- Process_TypeGroup1.ProcessId
- Process_TypeGroup1.ParentId
- Process_TypeGroup1.SessionId
- Process_TypeGroup1.ExitStatus
- Process_TypeGroup1.DirectoryTableBase
- Process_TypeGroup1.UserSID
- Process_TypeGroup1.ImageFileName
- Process_TypeGroup1.CommandLine
api_type:
- NA
api_location: ''
ms.openlocfilehash: bd67059f5257dad9b66e1c21f642fef04f03719e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106383"
---
# <a name="process_typegroup1-class"></a>Clase \_ Process TypeGroup1

Esta clase es la clase de tipo de evento para los eventos de proceso.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{1, 2, 3, 4, 39}, EventTypeName{"Start", "End", "DCStart", "DCEnd", "Defunct"}]
class Process_TypeGroup1 : Process
{
  uint32 UniqueProcessKey;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  uint32 DirectoryTableBase;
  object UserSID;
  string ImageFileName;
  string CommandLine;
};
```

## <a name="members"></a>Miembros

La **clase \_ Process TypeGroup1** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ Process TypeGroup1** tiene estas propiedades.

<dl> <dt>

CommandLine
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(9), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Línea de comandos completa del proceso.

</dd> <dt>

DirectoryTableBase
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(6), Pointer
</dt> </dl>

Dirección física de la tabla de páginas del proceso.

</dd> <dt>

ExitStatus
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(5)
</dt> </dl>

Estado de salida del proceso detenido.

</dd> <dt>

ImageFileName
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(8), StringTermination("NullTerminated")
</dt> </dl>

Ruta de acceso al archivo ejecutable del proceso.

</dd> <dt>

ParentId
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(3), Format("x")
</dt> </dl>

Identificador único del proceso que crea este proceso. Los números de identificador de proceso se reutilizan, por lo que solo identifican un proceso durante la vigencia de ese proceso. Es posible que el proceso identificado por ParentProcessId finalice, por lo que ParentProcessId puede no hacer referencia a un proceso en ejecución. También es posible que ParentProcessId se refiere incorrectamente a un proceso que reutiliza un identificador de proceso.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(2), Format("x")
</dt> </dl>

Identificador de proceso global que puede usar para identificar un proceso. El valor es válido desde el momento en que se crea un proceso hasta que finaliza.

</dd> <dt>

SessionId
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(4)
</dt> </dl>

Identificador único que genera un sistema operativo cuando crea una nueva sesión. Una sesión abarca un período de tiempo desde el inicio de sesión hasta la cierre de sesión desde un sistema específico.

</dd> <dt>

UniqueProcessKey
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(1), Pointer
</dt> </dl>

Dirección del objeto de proceso en el kernel.

</dd> <dt>

UserSID
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(7), Extension("Sid")
</dt> </dl>

Identificador de seguridad (SID) para el contexto de usuario en el que se produce el evento.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los tipos de eventos DCStart y DCEnd enumeran el proceso que se está ejecutando actualmente, incluidos los procesos inactivos y del sistema, en el momento en que se inicia y finaliza la sesión del kernel, respectivamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Proceso**](process.md)
</dt> </dl>

 

 




