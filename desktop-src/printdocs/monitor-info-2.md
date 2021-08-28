---
description: La estructura \_ MONITOR INFO \_ 2 identifica un monitor.
ms.assetid: 4dd1ca15-6983-403e-8159-1a6d35a88162
title: MONITOR_INFO_2 estructura (Winspool.h)
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
ms.openlocfilehash: c01377740c77ef4cb2be15e785b9ea3e93449944c11f2014ed660d8c3e3245b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112335"
---
# <a name="monitor_info_2-structure"></a>Estructura \_ de MONITOR INFO \_ 2

La **estructura MONITOR INFO \_ \_ 2** identifica un monitor.

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

Puntero a una cadena terminada en NULL que es el nombre del monitor.

</dd> <dt>

**pEnvironment**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el entorno para el que se escribió el monitor (por ejemplo, Windows NT x86, Windows IA64, Windows x64).

</dd> <dt>

**pDLLName**
</dt> <dd>

Puntero a una cadena terminada en NULL que es el nombre del archivo DLL del monitor.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ MONITOR \_ INFO \_ 2W** (Unicode) y **\_ MONITOR INFO \_ \_ 2A** (ANSI)<br/>                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de LA API del colador de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddMonitor**](addmonitor.md)
</dt> <dt>

[**EnumMonitors**](enummonitors.md)
</dt> <dt>

[**INFORMACIÓN \_ DE SUPERVISIÓN \_ 1**](monitor-info-1.md)
</dt> </dl>

 

 




