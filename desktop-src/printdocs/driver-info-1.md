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
ms.openlocfilehash: 57fd1fe4eea1585dce36d3d5bd03d2039ad345adbabcfdf1ab4b301f3fc15a69
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092085"
---
# <a name="driver_info_1-structure"></a>Estructura \_ DRIVER INFO \_ 1

La **estructura DRIVER INFO \_ \_ 1** identifica un controlador de impresora.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _DRIVER_INFO_1 {
  LPTSTR pName;
} DRIVER_INFO_1, *PDRIVER_INFO_1;
```



## <a name="members"></a>Miembros

<dl> <dt>

**pName**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre de un controlador de impresora.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ DRIVER \_ INFO \_ 1W** (Unicode) e **\_ DRIVER INFO \_ \_ 1A** (ANSI)<br/>                             |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del colador de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> </dl>

 

 




