---
description: La estructura de supervisión de la \_ información \_ 1 identifica un monitor instalado.
ms.assetid: 7a4660bd-5df8-49dd-92f6-9574f451f10d
title: Estructura de MONITOR_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MONITOR_INFO_1
- _MONITOR_INFO_1A
- _MONITOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b6af1e1b9111ac6221273f2faf68fc6ed70e07a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697154"
---
# <a name="monitor_info_1-structure"></a>Estructura de supervisión de la \_ información \_ 1

La estructura de supervisión de la **\_ información \_ 1** identifica un monitor instalado.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _MONITOR_INFO_1 {
  LPTSTR pName;
} MONITOR_INFO_1, *PMONITOR_INFO_1;
```



## <a name="members"></a>Miembros

<dl> <dt>

**pName**
</dt> <dd>

Un puntero a una cadena terminada en null que identifica un monitor instalado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | Supervisión de la **\_ \_ información \_ 1W** (Unicode) y supervisión de la **\_ \_ información \_ 1A** (ANSI)<br/>                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumMonitors**](enummonitors.md)
</dt> <dt>

[**Información de supervisión \_ \_ 2**](monitor-info-2.md)
</dt> </dl>

 

 




