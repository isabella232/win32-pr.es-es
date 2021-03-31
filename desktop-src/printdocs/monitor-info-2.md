---
description: La \_ estructura supervisar información \_ 2 identifica un monitor.
ms.assetid: 4dd1ca15-6983-403e-8159-1a6d35a88162
title: Estructura de MONITOR_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MONITOR_INFO_2
- _MONITOR_INFO_2A
- _MONITOR_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 9d3ad70a0728ca6e73c4dbefb248df58e858a996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817899"
---
# <a name="monitor_info_2-structure"></a>Estructura de supervisión de \_ información \_ 2

La estructura **supervisar \_ información \_ 2** identifica un monitor.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _MONITOR_INFO_2 {
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDLLName;
} MONITOR_INFO_2, *PMONITOR_INFO_2;
```



## <a name="members"></a>Miembros

<dl> <dt>

**pName**
</dt> <dd>

Puntero a una cadena terminada en null que es el nombre del monitor.

</dd> <dt>

**pEnvironment**
</dt> <dd>

Puntero a una cadena terminada en null que especifica el entorno para el que se escribió el monitor (por ejemplo, Windows NT x86, Windows IA64, Windows x64).

</dd> <dt>

**pDLLName**
</dt> <dd>

Un puntero a una cadena terminada en null que es el nombre del archivo DLL del monitor.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ Supervisar la \_ información \_ 2W** (Unicode) y la **\_ información de supervisión \_ \_ 2A** (ANSI)<br/>                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddMonitor**](addmonitor.md)
</dt> <dt>

[**EnumMonitors**](enummonitors.md)
</dt> <dt>

[**Información de supervisión \_ \_ 1**](monitor-info-1.md)
</dt> </dl>

 

 




