---
description: Esta clase es la clase de tipo de evento para los eventos de devolución de llamada de función principal del controlador. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: b3358935-d6fb-49eb-bdf7-4366b4fd14c5
title: Clase DriverMajorFunctionReturn
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverMajorFunctionReturn
- DriverMajorFunctionReturn.Irp
- DriverMajorFunctionReturn.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 21340224253d1eb3f3ddc733bf2d43e847844282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540358"
---
# <a name="drivermajorfunctionreturn-class"></a>Clase DriverMajorFunctionReturn

Esta clase es la clase de tipo de evento para los eventos de devolución de llamada de función principal del controlador.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{35}, EventTypeName{"DrvMjFnRet"}]
class DriverMajorFunctionReturn : DiskIo
{
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a>Miembros

La clase **DriverMajorFunctionReturn** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **DriverMajorFunctionReturn** tiene estas propiedades.

<dl> <dt>

**IRP**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (1), puntero
</dt> </dl>

Paquete de solicitud de e/s.

</dd> <dt>

**UniqMatchId**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (2)
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

 

 




