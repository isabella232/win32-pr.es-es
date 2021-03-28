---
description: Esta clase es la clase de tipo de evento para los eventos de solicitud de finalización de controlador. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: c9c9be05-c1c6-4d77-a47a-44a61ebfcdc7
title: Clase DriverCompleteRequest
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompleteRequest
- DriverCompleteRequest.RoutineAddr
- DriverCompleteRequest.Irp
- DriverCompleteRequest.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 57cf49d0e37dc870c0eb46c31ef39e0d81689811
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984235"
---
# <a name="drivercompleterequest-class"></a>Clase DriverCompleteRequest

Esta clase es la clase de tipo de evento para los eventos de solicitud de finalización de controlador.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{52}, EventTypeName{"DrvComplReq"}]
class DriverCompleteRequest : DiskIo
{
  uint32 RoutineAddr;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a>Miembros

La clase **DriverCompleteRequest** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **DriverCompleteRequest** tiene estas propiedades.

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

**RoutineAddr**
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

Identificador que identifica de forma única la solicitud. Use este identificador para correlacionar con los otros eventos del controlador, por ejemplo, el evento [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) .

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

 

 




