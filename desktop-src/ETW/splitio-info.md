---
description: Esta clase es la clase de tipo de evento para los eventos de E/S divididos. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: 0eb1f712-8b1c-4de1-b701-5c7dbabb0f55
title: SplitIo_Info clase
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
ms.openlocfilehash: 5ae5623f4d05bc4c0e5460415656f59d8b91eeedfe1671cae6a36c7a33e0a86f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766425"
---
# <a name="splitio_info-class"></a>SplitIo \_ Info (clase)

Esta clase es la clase de tipo de evento para los eventos de E/S divididos.

La sintaxis siguiente se simplifica a partir del código MOF.

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

La **clase SplitIo \_ Info** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase SplitIo \_ Info** tiene estas propiedades.

<dl> <dt>

**ChildIrp**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(2), Pointer
</dt> </dl>

Paquete de solicitud de E/S secundaria.

</dd> <dt>

**ParentIrp**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(1), Pointer
</dt> </dl>

Paquete de solicitud de E/S principal.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Indica que el administrador de volúmenes divide el IRP en dos IRP.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 




