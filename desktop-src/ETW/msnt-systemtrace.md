---
description: Clase primaria de la que se derivan todas las clases de seguimiento de eventos del sistema. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: 27979d9c-eca7-426f-8f8e-99443e5a0188
title: MSNT_SystemTrace clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSNT_SystemTrace
- MSNT_SystemTrace.Flags
api_type:
- NA
api_location: ''
ms.openlocfilehash: c083f7a2336a374e8009af2ba8094d57d9826197e16b7577aaf3b00a4c035173
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829625"
---
# <a name="msnt_systemtrace-class"></a>Clase SystemTrace de MSNT \_

Clase primaria de la que se derivan todas las clases de seguimiento de eventos del sistema.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{9e814aad-3204-11d2-9a82-006008a86939}")]
class MSNT_SystemTrace : EventTrace
{
  uint32 Flags;
};
```

## <a name="members"></a>Miembros

La **clase \_ SystemTrace de MSNT** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SystemTrace de MSNT** tiene estas propiedades.

<dl> <dt>

**Marcas**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **DefineValues{"EVENT \_ TRACE FLAG \_ \_ PROCESS", "EVENT \_ TRACE FLAG \_ \_ THREAD", "EVENT \_ TRACE FLAG IMAGE \_ \_ \_ LOAD", "EVENT \_ TRACE FLAG PROCESS \_ \_ \_ COUNTERS", "EVENT \_ TRACE FLAG \_ \_ CSWITCH", "EVENT \_ TRACE FLAG \_ \_ DPC", "EVENT TRACE FLAG \_ \_ \_ INTERRUPT", "EVENT \_ TRACE FLAG \_ \_ SYSTEMCALL", "EVENT \_ TRACE FLAG DISK \_ \_ \_ IO", "EVENT \_ TRACE FLAG DISK FILE \_ \_ \_ \_ IO", "EVENT TRACE FLAG DISK \_ IO \_ \_ \_ \_ INIT", "EVENT TRACE FLAG \_ \_ \_ DISPATCHER", "EVENT TRACE FLAG MEMORY PAGE \_ \_ \_ \_ \_ FAULTS", \_ "EVENT TRACE FLAG MEMORY HARD \_ \_ \_ \_ FAULTS", "EVENT \_ TRACE FLAG VIRTUAL \_ \_ \_ ALLOC", "EVENT \_ TRACE FLAG NETWORK \_ \_ \_ TCPIP", "EVENT \_ TRACE FLAG \_ \_ REGISTRY", "EVENT \_ TRACE FLAG \_ \_ ALPC", " EVENT \_ \_ TRACE FLAG SPLIT \_ \_ IO", "EVENT \_ TRACE FLAG \_ \_ DRIVER", "EVENT \_ TRACE FLAG \_ \_ PROFILE", "EVENT \_ TRACE FLAG FILE \_ \_ \_ IO", "EVENT \_ TRACE FLAG FILE IO \_ \_ \_ \_ INIT"}**, **ValueMap{"0x00000001", "0x00000002", "0x00000004", "0x00000008", "0x00000010", "0x00000020", "0x00000040", "0x00000080", "0x00000100", "0x00000200", "0x00000400", "0x00000800", "0x00001000", "0x00002000", "0x00004000", "0x00010000", "0x00020000", "0x00100000", "0x00200000", "0x00800000", "0x01000000", "0x02000000", "0x04000000"}**
</dt> </dl>

Marca de habilitación que indica los proveedores de kernel habilitados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



 

 




