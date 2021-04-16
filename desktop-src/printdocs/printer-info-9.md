---
description: La estructura de la información de la impresora \_ \_ 9 especifica la configuración de impresora predeterminada por usuario.
ms.assetid: 8bafb995-f31c-46e3-a950-45e240c678aa
title: Estructura de PRINTER_INFO_9 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_9
- _PRINTER_INFO_9A
- _PRINTER_INFO_9W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c0ae3c099da17d7fc437a67035d8da2cd00136bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720722"
---
# <a name="printer_info_9-structure"></a>Estructura de información de la impresora \_ \_ 9

La estructura de la información de la **impresora \_ \_ 9** especifica la configuración de impresora predeterminada por usuario.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PRINTER_INFO_9 {
  LPDEVMODE pDevMode;
} PRINTER_INFO_9, *PPRINTER_INFO_9;
```



## <a name="members"></a>Miembros

<dl> <dt>

**pDevMode**
</dt> <dd>

Puntero a una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que define los datos de impresora predeterminados por usuario, como la orientación del papel y la resolución. El **DEVMODE** se almacena en el registro del usuario.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los valores predeterminados por usuario solo afectarán a un usuario determinado o a cualquiera que use el perfil. En cambio, los valores predeterminados globales están establecidos por el administrador de una impresora que puede usar cualquier usuario. Para los valores predeterminados globales, use la información de la [**impresora \_ \_ 8**](printer-info-8.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | Información de la **\_ impresora \_ \_ 9W** (Unicode) e información de la **\_ impresora \_ \_ 9 bis** (ANSI)<br/>                           |



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

[**Información de la impresora \_ \_ 8**](printer-info-8.md)
</dt> </dl>

 

 




