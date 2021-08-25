---
description: La estructura PORT \_ INFO \_ 1 identifica un puerto de impresora compatible.
ms.assetid: e474fe9c-e554-406a-a5bf-de07f9a72b32
title: PORT_INFO_1 estructura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_1
- _PORT_INFO_1A
- _PORT_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ff6e4c3a43c35118772aede2e329a2e1e761fc0f147b5a3a9ceeef97bbf8fb00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947815"
---
# <a name="port_info_1-structure"></a>Estructura \_ PORT INFO \_ 1

La **estructura PORT INFO \_ \_ 1** identifica un puerto de impresora compatible.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PORT_INFO_1 {
  LPTSTR pName;
} PORT_INFO_1, *PPORT_INFO_1;
```



## <a name="members"></a>Miembros

<dl> <dt>

**pName**
</dt> <dd>

Puntero a una cadena terminada en NULL que identifica un puerto de impresora compatible (por ejemplo, "LPT1:").

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ PORT \_ INFO \_ 1W** (Unicode) e **\_ PORT INFO \_ \_ 1A** (ANSI)<br/>                                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de LA API del colador de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> </dl>

 

 




