---
description: Esta clase es la clase de tipo de evento para los eventos de e/s divididos. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 0eb1f712-8b1c-4de1-b701-5c7dbabb0f55
title: SplitIo_Info (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SplitIo_Info
- SplitIo_Info.ParentIrp
- SplitIo_Info.ChildIrp
api_type:
- NA
api_location: ''
ms.openlocfilehash: 469c8f04664f72b88e5a4378cb318b52f32fba24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912598"
---
# <a name="splitio_info-class"></a>Clase de información de SplitIo \_

Esta clase es la clase de tipo de evento para los eventos de e/s divididos.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{32}, EventTypeName{"VolMgr"}]
class SplitIo_Info : SplitIo
{
  uint32 ParentIrp;
  uint32 ChildIrp;
};
```

## <a name="members"></a>Miembros

La clase de **\_ información SplitIo** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase de **\_ información SplitIo** tiene estas propiedades.

<dl> <dt>

**ChildIrp**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (2), puntero
</dt> </dl>

Paquete de solicitud de e/s secundaria.

</dd> <dt>

**ParentIrp**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (1), puntero
</dt> </dl>

Paquete de solicitud de e/s primaria.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Indica que el administrador de volúmenes dividió el IRP en dos IRP.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 




