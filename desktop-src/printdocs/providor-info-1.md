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
ms.openlocfilehash: 2eabc00009b76247af71b06ea877ca0bf738c1d5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127248396"
---
# <a name="providor_info_1-structure"></a>PROVIDOR \_ INFO \_ 1 (estructura)

La **estructura PROVIDOR \_ INFO \_ 1** identifica un proveedor de impresión.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PROVIDOR_INFO_1 {
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDLLName;
} PROVIDOR_INFO_1, *PPROVIDOR_INFO_1;
```



## <a name="members"></a>Members

<dl> <dt>

**pName**
</dt> <dd>

Puntero a una cadena terminada en NULL que es el nombre del proveedor de impresión.

</dd> <dt>

**pEnvironment**
</dt> <dd>

Puntero a una cadena de entorno terminada en NULL que especifica el entorno en el que se va a ejecutar la biblioteca de vínculos dinámicos (DLL) del proveedor.

</dd> <dt>

**pDLLName**
</dt> <dd>

Puntero a una cadena terminada en NULL que es el nombre del proveedor .dll.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ PROVIDOR \_ INFO \_ 1W** (Unicode) y **\_ PROVIDOR \_ INFO \_ 1A** (ANSI)<br/>                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de LA API del colador de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrintProvidor**](addprintprovidor.md)
</dt> </dl>

 

 




