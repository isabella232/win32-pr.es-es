---
description: Determina la longitud, en caracteres, del texto asociado a una ventana.
ms.assetid: 9e185435-a624-4380-adfd-be4f3645ee5d
title: WM_GETTEXTLENGTH mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bc01f6f7a2b74df41e97a84bb4d7e17d9c3e21966215fcbcca04222d1d5537f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710395"
---
# <a name="wm_gettextlength-message"></a>Mensaje \_ GETTEXTLENGTH de WM

Determina la longitud, en caracteres, del texto asociado a una ventana.


```C++
#define WM_GETTEXTLENGTH                0x000E
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa y debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se usa y debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

El valor devuelto es la longitud del texto en caracteres, sin incluir el carácter nulo final.

## <a name="remarks"></a>Comentarios

Para un control de edición, el texto que se va a copiar es el contenido del control de edición. Para un cuadro combinado, el texto es el contenido de la parte del control de edición (o texto estático) del cuadro combinado. Para un botón, el texto es el nombre del botón. Para otras ventanas, el texto es el título de la ventana. Para determinar la longitud de un elemento en un cuadro de lista, una aplicación puede usar el [**mensaje \_ LB GETTEXTLEN.**](../controls/lb-gettextlen.md)

Cuando se **envía el mensaje WM \_ GETTEXTLENGTH,** la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve la longitud, en caracteres, del texto. En determinadas condiciones, **la función DefWindowProc** devuelve un valor mayor que la longitud real del texto. Esto se produce con ciertas mezclas de ANSI y Unicode, y se debe a que el sistema permite la posible existencia de caracteres de juego de caracteres de doble byte (DBCS) dentro del texto. Sin embargo, el valor devuelto siempre será al menos tan grande como la longitud real del texto; Por lo tanto, siempre puede usarlo para guiar la asignación del búfer. Este comportamiento puede producirse cuando una aplicación usa funciones ANSI y diálogos comunes, que usan Unicode.

Para obtener la longitud exacta del texto, use los mensajes [**WM \_ GETTEXT,**](wm-gettext.md) [**LB \_ GETTEXT**](../controls/lb-gettext.md)o [**CB \_ GETLBTEXT,**](../controls/cb-getlbtext.md) o la [**función GetWindowText.**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)

El envío **de \_ un mensaje GETTEXTLENGTH** de WM a un control estático que no sea de texto, como un mapa de bits estático o un control de icono estático, no devuelve un valor de cadena. En su lugar, devuelve cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**GetWindowTextLength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[**WM \_ GETTEXT**](wm-gettext.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**CB \_ GETLBTEXT**](../controls/cb-getlbtext.md)
</dt> <dt>

[**LB \_ GETTEXT**](../controls/lb-gettext.md)
</dt> <dt>

[**LB \_ GETTEXTLEN**](../controls/lb-gettextlen.md)
</dt> </dl>

 

 
