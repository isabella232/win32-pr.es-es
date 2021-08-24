---
description: Esta clase es la clase de tipo de evento para los eventos de rutina completos del controlador. La sintaxis siguiente se simplifica a partir del código MOF.
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
ms.openlocfilehash: ac1329c60f38ebfb4597b85ec251e074babd2c1fde7e58fee2423b6a11be92f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117814893"
---
# <a name="drivercompletionroutine-class"></a>Clase DriverCompletionRoutine

Esta clase es la clase de tipo de evento para los eventos de rutina completos del controlador.

La sintaxis siguiente se simplifica a partir del código MOF.

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

La **clase DriverCompletionRoutine** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase DriverCompletionRoutine** tiene estas propiedades.

<dl> <dt>

**Irp**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(2), Pointer
</dt> </dl>

Paquete de solicitud de E/S.

</dd> <dt>

**Rutina**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(1), Pointer
</dt> </dl>

Dirección de la función de controlador a la que se llama.

</dd> <dt>

**UniqMatchId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(3)
</dt> </dl>

Identificador que identifica de forma única la solicitud. Use este identificador para correlacionar con los demás eventos de controlador, por ejemplo, [**el evento DriverCompleteRequest.**](drivercompleterequest.md)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DiskIo**](diskio.md)
</dt> </dl>

 

 




