---
description: La \_ estructura PROVIDOR info \_ 2 anexa un proveedor de impresión a la lista de pedidos del proveedor de impresión.
ms.assetid: 840523ca-22d0-460f-81fb-e0a9e2d4f5d6
title: Estructura de PROVIDOR_INFO_2 (winspool. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688234"
---
# <a name="providor_info_2-structure"></a>Estructura de PROVIDOR \_ info \_ 2

La estructura **PROVIDOR \_ info \_ 2** anexa un proveedor de impresión a la lista de pedidos del proveedor de impresión.

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

Puntero a una cadena terminada en null que especifica el nombre del proveedor de impresión.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se usa al llamar a [**AddPrintProvidor**](addprintprovidor.md), nivel 2, para agregar el proveedor de impresión especificado al final de la lista de pedidos del proveedor de impresión. El proveedor se usa inmediatamente para el enrutamiento si la llamada se realiza correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ PROVIDOR \_ info \_ 2W** (Unicode) y **\_ PROVIDOR \_ info \_ 2A** (ANSI)<br/>                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrintProvidor**](addprintprovidor.md)
</dt> </dl>

 

 




