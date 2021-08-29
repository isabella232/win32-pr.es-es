---
description: 'Process_V2_TypeGroup1 clase : esta clase es la clase de tipo de evento para los eventos de proceso. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: ff5c1f64-2087-4238-81f9-6283f0f0e68a
title: Process_V2_TypeGroup1 clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V2_TypeGroup1
- Process_V2_TypeGroup1.UniqueProcessKey
- Process_V2_TypeGroup1.ProcessId
- Process_V2_TypeGroup1.ParentId
- Process_V2_TypeGroup1.SessionId
- Process_V2_TypeGroup1.ExitStatus
- Process_V2_TypeGroup1.UserSID
- Process_V2_TypeGroup1.ImageFileName
- Process_V2_TypeGroup1.CommandLine
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4686ed24682f27358b9a7959d7bb91519674b9db295a6d9c2aa10df1d06a87f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069975"
---
# <a name="process_v2_typegroup1-class"></a>Clase \_ \_ TypeGroup1 de Process V2

Esta clase es la clase de tipo de evento para los eventos de proceso.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{1, 2, 3, 4, 39}, EventTypeName{"Start", "End", "DCStart", "DCEnd", "Defunct"}]
class Process_V2_TypeGroup1 : Process_V2
{
  uint32 UniqueProcessKey;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  object UserSID;
  string ImageFileName;
  string CommandLine;
};
```

## <a name="members"></a>Miembros

La **clase \_ \_ TypeGroup1 de Process V2** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ \_ TypeGroup1 de Process V2** tiene estas propiedades.

<dl> <dt>

CommandLine
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(8), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Línea de comandos completa del proceso.

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

Calificadores: WmiDataId(7), StringTermination("NullTerminated")
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

Identificador único del proceso que crea este proceso. Los números de identificador de proceso se reutilizan, por lo que solo identifican un proceso para la duración de ese proceso. Es posible que el proceso identificado por ParentProcessId finalice, por lo que ParentProcessId puede no hacer referencia a un proceso en ejecución. También es posible que ParentProcessId se refiere incorrectamente a un proceso que reutiliza un identificador de proceso.

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

Identificador único que genera un sistema operativo cuando crea una nueva sesión. Una sesión abarca un período de tiempo desde el inicio de sesión hasta la cierre de sesión de un sistema específico.

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

Calificadores: WmiDataId(6), Extension("Sid")
</dt> </dl>

Identificador de seguridad (SID) para el contexto de usuario en el que se produce el evento.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los tipos de eventos DCStart y DCEnd enumeran el proceso que se está ejecutando actualmente, incluidos los procesos inactivos y del sistema, en el momento en que se inicia y finaliza la sesión del kernel, respectivamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Proceso \_ V2**](process-v2.md)
</dt> </dl>

 

 




