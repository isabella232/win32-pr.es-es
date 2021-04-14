---
description: Esta clase es la clase de tipo de evento para los eventos de salida de la llamada del sistema. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: bb9a2770-f37b-4055-8811-59ba117adf82
title: Clase SysCallExit
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
ms.openlocfilehash: af46f374d4532efc15185a4716526beabfe5ced1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985698"
---
# <a name="syscallexit-class"></a>Clase SysCallExit

Esta clase es la clase de tipo de evento para los eventos de salida de la llamada del sistema.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{52}, EventTypeName{"SysClExit"}]
class SysCallExit : PerfInfo
{
  uint32 SysCallNtStatus;
};
```

## <a name="members"></a>Miembros

La clase **SysCallExit** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **SysCallExit** tiene estas propiedades.

<dl> <dt>

**SysCallNtStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (1), Format ("x")
</dt> </dl>

Código de estado devuelto por la llamada del sistema NT.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 




