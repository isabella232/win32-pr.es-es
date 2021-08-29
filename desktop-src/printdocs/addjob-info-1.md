---
description: La estructura ADDJOB INFO 1 identifica un trabajo de impresión, así como el directorio y el archivo en los que una aplicación \_ \_ puede almacenar ese trabajo.
ms.assetid: de915932-11a7-47e8-9be9-edab76d94189
title: ADDJOB_INFO_1 estructura (Winspool.h)
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
ms.openlocfilehash: 6a0abcd2d9d09b65e8b4d5dd27e01532859a8060eda7847f0c1b7888a3c9714f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950765"
---
# <a name="addjob_info_1-structure"></a>Estructura ADDJOB \_ INFO \_ 1

La **estructura ADDJOB \_ INFO \_ 1** identifica un trabajo de impresión, así como el directorio y el archivo en los que una aplicación puede almacenar ese trabajo.

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

Puntero a una cadena terminada en NULL que contiene la ruta de acceso y el nombre de archivo que la aplicación puede usar para almacenar el trabajo de impresión.

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
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ ADDJOB \_ INFO \_ 1W** (Unicode) y **\_ ADDJOB \_ INFO \_ 1A** (ANSI)<br/>                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del colador de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddJob**](addjob.md)
</dt> </dl>

 

 




