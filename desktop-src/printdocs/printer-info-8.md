---
description: La estructura de la información de la impresora \_ \_ 8 especifica la configuración de impresora predeterminada global.
ms.assetid: 98f26a45-5302-4358-bed6-691d9bc37554
title: Estructura de PRINTER_INFO_8 (winspool. h)
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
ms.openlocfilehash: e17780dc2f39dc3041e690de1ef7b5728c8743e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912958"
---
# <a name="printer_info_8-structure"></a>Información de impresora \_ \_ 8 (estructura)

La estructura de la información de la **impresora \_ \_ 8** especifica la configuración de impresora predeterminada global.

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

## <a name="remarks"></a>Observaciones

Los valores predeterminados globales están establecidos por el administrador de una impresora que puede usar cualquier usuario. Por el contrario, los valores predeterminados por usuario afectarán a un usuario determinado o a cualquier otra persona que use el perfil. Para los valores predeterminados por usuario, use la información de la [**impresora \_ \_ 9**](printer-info-9.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | Información de la **\_ impresora \_ \_ 8W** (Unicode) y la información de la **\_ impresora \_ \_ 8A** (ANSI)<br/>                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**Información de la impresora \_ \_ 9**](printer-info-9.md)
</dt> </dl>

 

 




