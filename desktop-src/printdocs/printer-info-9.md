---
description: La estructura PRINTER INFO 9 especifica la configuración predeterminada de la \_ \_ impresora por usuario.
ms.assetid: 8bafb995-f31c-46e3-a950-45e240c678aa
title: PRINTER_INFO_9 estructura (Winspool.h)
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
ms.openlocfilehash: 684ffc6ccfc4f94c036bde42faec9458c8bb60911fc8c9398006f58631baa791
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118234240"
---
# <a name="printer_info_9-structure"></a>Printer \_ INFO \_ 9 (estructura)

La **estructura PRINTER INFO \_ \_ 9** especifica la configuración predeterminada de la impresora por usuario.

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

Puntero a una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que define los datos de impresora predeterminados por usuario, como la orientación del papel y la resolución. **DEVMODE se** almacena en el registro del usuario.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los valores predeterminados por usuario solo afectarán a un usuario determinado o a cualquier persona que use el perfil. Por el contrario, los valores predeterminados globales los establece el administrador de una impresora que puede usar cualquier persona. Para los valores predeterminados globales, use [**PRINTER \_ INFO \_ 8**](printer-info-8.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ PRINTER \_ INFO \_ 9W** (Unicode) e **\_ PRINTER INFO \_ \_ 9A** (ANSI)<br/>                           |



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

[**PRINTER \_ INFO \_ 8**](printer-info-8.md)
</dt> </dl>

 

 




