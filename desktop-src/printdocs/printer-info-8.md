---
description: La estructura PRINTER \_ INFO \_ 8 especifica la configuración de impresora predeterminada global.
ms.assetid: 98f26a45-5302-4358-bed6-691d9bc37554
title: PRINTER_INFO_8 estructura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_8
- _PRINTER_INFO_8A
- _PRINTER_INFO_8W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 0aa5d516dd099caeba5699a8328fa52add64f14ea970e6ccec28ea8bfbe87271
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947675"
---
# <a name="printer_info_8-structure"></a>Estructura PRINTER \_ INFO \_ 8

La **estructura PRINTER INFO \_ \_ 8** especifica la configuración de impresora predeterminada global.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PRINTER_INFO_8 {
  LPDEVMODE pDevMode;
} PRINTER_INFO_8, *PPRINTER_INFO_8;
```



## <a name="members"></a>Miembros

<dl> <dt>

**pDevMode**
</dt> <dd>

Puntero a una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que define los datos de impresora predeterminados globales, como la orientación del papel y la resolución.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El administrador de una impresora puede usar los valores predeterminados globales. En cambio, los valores predeterminados por usuario afectarán a un usuario determinado o a cualquier otra persona que use el perfil. Para los valores predeterminados por usuario, use [**PRINTER \_ INFO \_ 9**](printer-info-9.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ PRINTER \_ INFO \_ 8W** (Unicode) e **\_ PRINTER INFO \_ \_ 8A** (ANSI)<br/>                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API de Spooler de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**INFORMACIÓN \_ DE IMPRESORA \_ 9**](printer-info-9.md)
</dt> </dl>

 

 




