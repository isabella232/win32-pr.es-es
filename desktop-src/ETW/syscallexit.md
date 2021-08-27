---
description: Esta clase es la clase de tipo de evento para los eventos de salida de llamadas del sistema. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: bb9a2770-f37b-4055-8811-59ba117adf82
title: SysCallExit (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SysCallExit
- SysCallExit.SysCallNtStatus
api_type:
- NA
api_location: ''
ms.openlocfilehash: aa297ced8f6c0d17c0c01da9ce11705d30fe7448c8bc2f2ae6358ddc85f653be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102065"
---
# <a name="syscallexit-class"></a>SysCallExit (clase)

Esta clase es la clase de tipo de evento para los eventos de salida de llamadas del sistema.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{52}, EventTypeName{"SysClExit"}]
class SysCallExit : PerfInfo
{
  uint32 SysCallNtStatus;
};
```

## <a name="members"></a>Miembros

La **clase SysCallExit** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase SysCallExit** tiene estas propiedades.

<dl> <dt>

**SysCallNtStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(1), Format("x")
</dt> </dl>

Código de estado devuelto por la llamada del sistema NT.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 




