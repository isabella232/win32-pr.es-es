---
description: Esta clase es la clase de tipo de evento para la llamada del sistema Enter Events. La siguiente sintaxis se simplifica desde el código MOF.
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
ms.openlocfilehash: 1497491de622e564b945e8a80fcb1d8755886f39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985699"
---
# <a name="syscallenter-class"></a>Clase SysCallEnter

Esta clase es la clase de tipo de evento para la llamada del sistema Enter Events.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{51}, EventTypeName{"SysClEnter"}]
class SysCallEnter : PerfInfo
{
  uint32 SysCallAddress;
};
```

## <a name="members"></a>Miembros

La clase **SysCallEnter** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **SysCallEnter** tiene estas propiedades.

<dl> <dt>

**SysCallAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (1), puntero
</dt> </dl>

Dirección de la llamada de función NT que se va a escribir.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 




