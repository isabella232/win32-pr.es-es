---
title: Mensaje SETRGBSTRING (commdlg. h)
description: El procedimiento de enlace de un cuadro de diálogo de color, CCHookProc, puede enviar el mensaje registrado de SETRGBSTRING al cuadro de diálogo para establecer la selección de color actual.
ms.assetid: 02d36248-be75-4552-853f-6ac3ec034ebe
keywords:
- Cuadros de diálogo de mensaje de SETRGBSTRING
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
ms.openlocfilehash: dea5489aaa6fafcaa19a97a44d81fd85abb178d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803091"
---
# <a name="setrgbstring-message"></a>Mensaje SETRGBSTRING

El procedimiento de enlace de un cuadro de diálogo de **color** , [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), puede enviar el mensaje registrado de **SETRGBSTRING** al cuadro de diálogo para establecer la selección de color actual.


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

Valor RGB del color que se va a seleccionar en el cuadro de diálogo de **color** . Puede usar la macro [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) para especificar las intensidades rojo, verde y azul de un valor de color RGB.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no tiene ningún valor devuelto.

## <a name="remarks"></a>Observaciones

Si *lParam* coincide con uno de los colores básicos o con uno de los 16 colores personalizados, el procedimiento de cuadro de diálogo selecciona ese color. El procedimiento de cuadro de diálogo también actualiza todos los controles de la extensión de color personalizada del cuadro de diálogo **color** , si está abierto.

Si *lParam* no coincide con un color básico o personalizado, el procedimiento del cuadro de diálogo no cambia la selección de color actual, pero actualiza los controles de color personalizados, si están visibles.

## <a name="examples"></a>Ejemplos

En el código de ejemplo siguiente se obtiene el identificador de mensaje **SETRGBSTRING** y, a continuación, se establece la selección de color en azul.


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
| Encabezado<br/>                   | <dl> <dt>Commdlg. h (incluir Windows. h)</dt> </dl> |
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

**Vista**
</dt> <dt>

[Biblioteca de cuadros de diálogo comunes](common-dialog-box-library.md)
</dt> </dl>

 

