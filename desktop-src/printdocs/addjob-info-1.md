---
description: La \_ estructura ADDJOB info \_ 1 identifica un trabajo de impresión, así como el directorio y el archivo en el que una aplicación puede almacenar ese trabajo.
ms.assetid: de915932-11a7-47e8-9be9-edab76d94189
title: Estructura de ADDJOB_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDJOB_INFO_1
- _ADDJOB_INFO_1A
- _ADDJOB_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 08197a6a72da7e38a349014e08d2d2c2c946f6e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279034"
---
# <a name="addjob_info_1-structure"></a>ADDJOB \_ estructura de información \_ 1

La estructura **ADDJOB \_ info \_ 1** identifica un trabajo de impresión, así como el directorio y el archivo en el que una aplicación puede almacenar ese trabajo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _ADDJOB_INFO_1 {
  LPTSTR Path;
  DWORD  JobId;
} ADDJOB_INFO_1, *PADDJOB_INFO_1;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Ruta de acceso**
</dt> <dd>

Puntero a una cadena terminada en null que contiene la ruta de acceso y el nombre de archivo que la aplicación puede usar para almacenar el trabajo de impresión.

</dd> <dt>

**JobId**
</dt> <dd>

Identificador del trabajo de impresión.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ ADDJOB \_ info \_ 1W** (Unicode) y **\_ ADDJOB \_ info \_ 1A** (ANSI)<br/>                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddJob**](addjob.md)
</dt> </dl>

 

 




