---
description: La estructura PROVIDOR \_ INFO \_ 2 anexa un proveedor de impresión a la lista de pedidos del proveedor de impresión.
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
ms.openlocfilehash: 969af36fe0a64bb586fbf62912ca27c6ebba9ba0a627701e4bc57f6202bfe1b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091685"
---
# <a name="providor_info_2-structure"></a>Estructura DE PROVIDOR \_ INFO \_ 2

La **estructura PROVIDOR \_ INFO \_ 2** anexa un proveedor de impresión a la lista de pedidos del proveedor de impresión.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PROVIDOR_INFO_2 {
  LPTSTR pOrder;
} PROVIDOR_INFO_2, *PPROVIDOR_INFO_2;
```



## <a name="members"></a>Miembros

<dl> <dt>

**pOrder**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del proveedor de impresión.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura se usa al llamar a [**AddPrintProvidor**](addprintprovidor.md), nivel 2, para agregar el proveedor de impresión especificado al final de la lista de pedidos del proveedor de impresión. El proveedor se usa inmediatamente para el enrutamiento si la llamada se realiza correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ PROVIDOR \_ INFO \_ 2W** (Unicode) y **\_ PROVIDOR \_ INFO \_ 2A** (ANSI)<br/>                         |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API de Spooler de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrintProvidor**](addprintprovidor.md)
</dt> </dl>

 

 




