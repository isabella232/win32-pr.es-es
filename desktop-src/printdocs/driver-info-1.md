---
description: La estructura DRIVER \_ INFO \_ 1 identifica un controlador de impresora.
ms.assetid: 9435192b-3eba-4937-8cd3-bff4e9eb84d3
title: DRIVER_INFO_1 estructura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_1
- _DRIVER_INFO_1A
- _DRIVER_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 21301cdab4449d0a48254660d195d4f2507a80e3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568649"
---
# <a name="driver_info_1-structure"></a>Estructura \_ DRIVER INFO \_ 1

La **estructura DRIVER INFO \_ \_ 1** identifica un controlador de impresora.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _DRIVER_INFO_1 {
  LPTSTR pName;
} DRIVER_INFO_1, *PDRIVER_INFO_1;
```



## <a name="members"></a>Members

<dl> <dt>

**pName**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre de un controlador de impresora.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ DRIVER \_ INFO \_ 1W** (Unicode) e **\_ DRIVER INFO \_ \_ 1A** (ANSI)<br/>                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de LA API del colador de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> </dl>

 

 




