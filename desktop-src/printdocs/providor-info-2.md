---
description: La estructura PROVIDOR \_ INFO 2 anexa un proveedor de impresión a la lista de pedidos del proveedor de \_ impresión.
ms.assetid: 840523ca-22d0-460f-81fb-e0a9e2d4f5d6
title: PROVIDOR_INFO_2 estructura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROVIDOR_INFO_2
- _PROVIDOR_INFO_2A
- _PROVIDOR_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d40f5843bf68254b92e3d814d9f308ba4f058889
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127248390"
---
# <a name="providor_info_2-structure"></a>PROVIDOR \_ INFO \_ 2 (estructura)

La **estructura PROVIDOR \_ INFO \_ 2** anexa un proveedor de impresión a la lista de pedidos del proveedor de impresión.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PROVIDOR_INFO_2 {
  LPTSTR pOrder;
} PROVIDOR_INFO_2, *PPROVIDOR_INFO_2;
```



## <a name="members"></a>Members

<dl> <dt>

**pOrder**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del proveedor de impresión.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se usa al llamar a [**AddPrintProvidor,**](addprintprovidor.md)nivel 2, para agregar el proveedor de impresión especificado al final de la lista de pedidos del proveedor de impresión. El proveedor se usa inmediatamente para el enrutamiento si la llamada se realiza correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ PROVIDOR \_ INFO \_ 2W** (Unicode) y **\_ PROVIDOR \_ INFO \_ 2A** (ANSI)<br/>                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de LA API del colador de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrintProvidor**](addprintprovidor.md)
</dt> </dl>

 

 




