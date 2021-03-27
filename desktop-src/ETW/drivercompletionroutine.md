---
description: Esta clase es la clase de tipo de evento para eventos de rutina completa de controlador. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: deb4f0b2-d73f-4ccf-b39b-6e92b32489fb
title: Clase DriverCompletionRoutine
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompletionRoutine
- DriverCompletionRoutine.Routine
- DriverCompletionRoutine.Irp
- DriverCompletionRoutine.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2b43862169cbe8f192f8fb9db561c2e101f377b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907709"
---
# <a name="drivercompletionroutine-class"></a>Clase DriverCompletionRoutine

Esta clase es la clase de tipo de evento para eventos de rutina completa de controlador.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{37}, EventTypeName{"DrvComplRout"}]
class DriverCompletionRoutine : DiskIo
{
  uint32 Routine;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a>Miembros

La clase **DriverCompletionRoutine** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **DriverCompletionRoutine** tiene estas propiedades.

<dl> <dt>

**IRP**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (2), puntero
</dt> </dl>

Paquete de solicitud de e/s.

</dd> <dt>

**Rutina**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (1), puntero
</dt> </dl>

Dirección de la función de controlador que se va a llamar.

</dd> <dt>

**UniqMatchId**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (3)
</dt> </dl>

Identificador que identifica de forma única la solicitud. Use este identificador para correlacionar con los otros eventos del controlador, por ejemplo, el evento [**DriverCompleteRequest**](drivercompleterequest.md) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Desmontaje**](diskio.md)
</dt> </dl>

 

 




