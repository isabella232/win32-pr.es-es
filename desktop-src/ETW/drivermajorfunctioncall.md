---
description: Esta clase es la clase de tipo de evento para los eventos de llamada de función principal del controlador. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: 8c913145-ac50-4d40-8519-5fed79d977ba
title: Clase DriverMajorFunctionCall
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverMajorFunctionCall
- DriverMajorFunctionCall.MajorFunction
- DriverMajorFunctionCall.MinorFunction
- DriverMajorFunctionCall.RoutineAddr
- DriverMajorFunctionCall.FileObject
- DriverMajorFunctionCall.Irp
- DriverMajorFunctionCall.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: c944b11c9019ba5244850f035bfc7c02d5ca3350
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255044"
---
# <a name="drivermajorfunctioncall-class"></a>Clase DriverMajorFunctionCall

Esta clase es la clase de tipo de evento para los eventos de llamada de función principal del controlador.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{34}, EventTypeName{"DrvMjFnCall"}]
class DriverMajorFunctionCall : DiskIo
{
  uint32 MajorFunction;
  uint32 MinorFunction;
  uint32 RoutineAddr;
  uint32 FileObject;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a>Members

La **clase DriverMajorFunctionCall** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase DriverMajorFunctionCall** tiene estas propiedades.

<dl> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(4), Pointer
</dt> </dl>

Coincide con el valor de este puntero con el valor de puntero **FileObject** de un evento [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) para determinar el tipo de operación de E/S.

</dd> <dt>

**Irp**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(5), Pointer
</dt> </dl>

Paquete de solicitud de E/S.

</dd> <dt>

**MajorFunction**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(1)
</dt> </dl>

Código que identifica la función principal a la que se llama.

</dd> <dt>

**MinorFunction**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(2)
</dt> </dl>

Código que inicia la función secundaria a la que se llama.

</dd> <dt>

**RoutineAddr**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(3), Pointer
</dt> </dl>

Dirección de la función de controlador a la que se llama.

</dd> <dt>

**UniqMatchId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(6)
</dt> </dl>

Identificador que identifica de forma única la solicitud. Use este identificador para correlacionar con los demás eventos de controlador, por ejemplo, el [**evento DriverCompleteRequest.**](drivercompleterequest.md)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DiskIo**](diskio.md)
</dt> </dl>

 

 




