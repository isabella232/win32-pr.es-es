---
description: Determina la longitud, en caracteres, del texto asociado a una ventana.
ms.assetid: 9e185435-a624-4380-adfd-be4f3645ee5d
title: Mensaje de WM_GETTEXTLENGTH (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0efc058033f9c4939137414d305d0717b54bef54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002385"
---
# <a name="wm_gettextlength-message"></a>Mensaje de GETTEXTLENGTH de WM \_

Determina la longitud, en caracteres, del texto asociado a una ventana.


```C++
#define WM_GETTEXTLENGTH                0x000E
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza y debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza y debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

El valor devuelto es la longitud del texto en caracteres, sin incluir el carácter nulo de terminación.

## <a name="remarks"></a>Observaciones

Para un control de edición, el texto que se va a copiar es el contenido del control de edición. En el caso de un cuadro combinado, el texto es el contenido de la parte del control de edición (o texto estático) del cuadro combinado. En el caso de un botón, el texto es el nombre del botón. Para otras ventanas, el texto es el título de la ventana. Para determinar la longitud de un elemento en un cuadro de lista, una aplicación puede usar el mensaje [**lb \_ GETTEXTLEN**](../controls/lb-gettextlen.md) .

Cuando se envía el mensaje de **\_ GETTEXTLENGTH de WM** , la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve la longitud, en caracteres, del texto. En determinadas condiciones, la función **DefWindowProc** devuelve un valor que es mayor que la longitud real del texto. Esto sucede con ciertas mezclas de ANSI y Unicode, y se debe a que el sistema permite la existencia de caracteres de juegos de caracteres de doble byte (DBCS) en el texto. Sin embargo, el valor devuelto siempre será al menos tan grande como la longitud real del texto; por tanto, se puede usar siempre para guiar la asignación de búfer. Este comportamiento puede producirse cuando una aplicación usa funciones ANSI y cuadros de diálogo comunes, que usan Unicode.

Para obtener la longitud exacta del texto, use los mensajes [**de \_ WM gettext**](wm-gettext.md), [**lb \_ gettext**](../controls/lb-gettext.md)o [**CB \_ GETLBTEXT**](../controls/cb-getlbtext.md) , o la función [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta) .

El envío de un mensaje de **WM \_ GETTEXTLENGTH** a un control estático que no sea de texto, como un mapa de bits estático o un icono estático controlc, no devuelve un valor de cadena. En su lugar, devuelve cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



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

[**GETTEXT de WM \_**](wm-gettext.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**CB \_ GETLBTEXT**](../controls/cb-getlbtext.md)
</dt> <dt>

[**\_apgettext GETTEXT**](../controls/lb-gettext.md)
</dt> <dt>

[**LB \_ GETTEXTLEN**](../controls/lb-gettextlen.md)
</dt> </dl>

 

 
