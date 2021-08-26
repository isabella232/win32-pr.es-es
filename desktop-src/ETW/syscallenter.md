---
description: Esta clase es la clase de tipo de evento para los eventos enter de llamada del sistema. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: 1ab32977-3f59-4816-b311-67142475dff2
title: Clase SysCallEnter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SysCallEnter
- SysCallEnter.SysCallAddress
api_type:
- NA
api_location: ''
ms.openlocfilehash: 53389fb4c5d78316020a145999ac13d2c8abfbf7474efaad802e29632d40beaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083195"
---
# <a name="syscallenter-class"></a>Clase SysCallEnter

Esta clase es la clase de tipo de evento para los eventos enter de llamada del sistema.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{51}, EventTypeName{"SysClEnter"}]
class SysCallEnter : PerfInfo
{
  uint32 SysCallAddress;
};
```

## <a name="members"></a>Miembros

La **clase SysCallEnter** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase SysCallEnter** tiene estas propiedades.

<dl> <dt>

**SysCallAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(1), Pointer
</dt> </dl>

Dirección de la llamada de función NT que se está escribió.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 




