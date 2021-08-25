---
description: Esta clase es la clase de tipo de evento para los eventos devueltos de llamadas de función principal del controlador. La sintaxis siguiente se simplifica a partir del código MOF.
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
ms.openlocfilehash: de8c18d7655aec0f9ae4748c384b26015a5a1083721aae367e132ea7c39f80a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914475"
---
# <a name="drivermajorfunctionreturn-class"></a>Clase DriverMajorFunctionReturn

Esta clase es la clase de tipo de evento para los eventos devueltos de llamadas de función principal del controlador.

La sintaxis siguiente se simplifica a partir del código MOF.

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

La **clase DriverMajorFunctionReturn** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase DriverMajorFunctionReturn** tiene estas propiedades.

<dl> <dt>

**Irp**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(1), Pointer
</dt> </dl>

Paquete de solicitud de E/S.

</dd> <dt>

**UniqMatchId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(2)
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

 

 




