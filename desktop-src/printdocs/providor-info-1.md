---
description: La estructura PROVIDOR \_ INFO \_ 1 identifica un proveedor de impresión.
ms.assetid: 0eff115a-b3d2-4c8f-b820-46e7f62dd295
title: PROVIDOR_INFO_1 estructura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROVIDOR_INFO_1
- _PROVIDOR_INFO_1A
- _PROVIDOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 4f9e7015382ef34f4582c4772e148059c4ed01de9e81da5af71bc0849df26f15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091705"
---
# <a name="providor_info_1-structure"></a>Estructura DE PROVIDOR \_ INFO \_ 1

La **estructura PROVIDOR \_ INFO \_ 1** identifica un proveedor de impresión.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PROVIDOR_INFO_1 {
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDLLName;
} PROVIDOR_INFO_1, *PPROVIDOR_INFO_1;
```



## <a name="members"></a>Miembros

<dl> <dt>

**pName**
</dt> <dd>

Puntero a una cadena terminada en NULL que es el nombre del proveedor de impresión.

</dd> <dt>

**pEnvironment**
</dt> <dd>

Puntero a una cadena de entorno terminada en NULL que especifica el entorno en el que se ha diseñado la biblioteca de vínculos dinámicos (DLL) del proveedor.

</dd> <dt>

**pDLLName**
</dt> <dd>

Puntero a una cadena terminada en NULL que es el nombre del proveedor .dll.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ PROVIDOR \_ INFO \_ 1W** (Unicode) y **\_ PROVIDOR \_ INFO \_ 1A** (ANSI)<br/>                         |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API de Spooler de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrintProvidor**](addprintprovidor.md)
</dt> </dl>

 

 




