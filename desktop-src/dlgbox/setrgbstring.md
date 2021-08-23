---
title: Mensaje SETRGBSTRING (Commdlg.h)
description: El procedimiento de enlace de un cuadro de diálogo Color, CCHookProc, puede enviar el mensaje registrado SETRGBSTRING al cuadro de diálogo para establecer la selección de color actual.
ms.assetid: 02d36248-be75-4552-853f-6ac3ec034ebe
keywords:
- Cuadros de diálogo del mensaje SETRGBSTRING
topic_type:
- apiref
api_name:
- SETRGBSTRING
- SETRGBSTRINGA
- SETRGBSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8322bb07300ce188684f5097232563e80721fadf0f614c24ac5f7b2d034c1fff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985315"
---
# <a name="setrgbstring-message"></a>Mensaje SETRGBSTRING

El procedimiento de enlace de un cuadro de diálogo **Color,** [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), puede enviar el mensaje registrado **SETRGBSTRING** al cuadro de diálogo para establecer la selección de color actual.


```C++
#define SETRGBSTRING TEXT("commdlg_SetRGBColor")
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor RGB del color que se selecciona en el **cuadro de diálogo** Color. Puede usar la [**macro RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) para especificar las intensidades de color rojo, verde y azul de un valor de color RGB.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no tiene ningún valor devuelto.

## <a name="remarks"></a>Comentarios

Si *lParam coincide* con uno de los colores básicos o uno de los 16 colores personalizados, el procedimiento del cuadro de diálogo selecciona ese color. El procedimiento del cuadro de diálogo también actualiza todos los controles de la extensión de color personalizado del cuadro de diálogo **Color,** si está abierto.

Si *lParam* no coincide con un color básico o personalizado, el procedimiento del cuadro de diálogo no cambia la selección de color actual, pero actualiza los controles de color personalizados, si están visibles.

## <a name="examples"></a>Ejemplos

El código de ejemplo siguiente obtiene el identificador del mensaje **SETRGBSTRING** y, a continuación, establece la selección de color en azul.


```
UINT uiSetRGB;

uiSetRGB = RegisterWindowMessage(SETRGBSTRING);

SendMessage(hdlg, uiSetRGB, 0, (LPARAM) RGB(0, 0, 255)); 
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Commdlg.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **SETRGBSTRINGW** (Unicode) y **SETRGBSTRINGA** (ANSI)<br/>                                      |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Biblioteca común de cuadros de diálogo](common-dialog-box-library.md)
</dt> </dl>

 

