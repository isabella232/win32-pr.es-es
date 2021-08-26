---
description: Copia el texto que corresponde a una ventana en un búfer proporcionado por el autor de la llamada.
ms.assetid: 117c3d6d-24cd-462f-bdb0-b65d8914273a
title: WM_GETTEXT mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e1bc6a8a77c51b3ab5b84f5cce700e65b180b357c932b4044a2b65cb49fc8e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089895"
---
# <a name="wm_gettext-message"></a>Mensaje \_ GETTEXT de WM

Copia el texto que corresponde a una ventana en un búfer proporcionado por el autor de la llamada.


```C++
#define WM_GETTEXT                      0x000D
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número máximo de caracteres que se van a copiar, incluido el carácter nulo de terminación.

Las aplicaciones ANSI pueden tener la cadena en el búfer reducida en tamaño (a un mínimo de la mitad del valor *wParam)* debido a la conversión de ANSI a Unicode.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero al búfer que va a recibir el texto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

El valor devuelto es el número de caracteres copiados, sin incluir el carácter nulo final.

## <a name="remarks"></a>Comentarios

La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) copia el texto asociado a la ventana en el búfer especificado y devuelve el número de caracteres copiados. Tenga en cuenta que para los controles estáticos que no son de texto, esto proporciona el texto con el que se creó originalmente el control, es decir, el número de identificador. Sin embargo, proporciona el identificador del control estático que no es de texto tal y como se creó originalmente. Es decir, si posteriormente usó **un \_ setimage de STM** para cambiarlo, se devolvería el identificador original.

Para un control de edición, el texto que se va a copiar es el contenido del control de edición. Para un cuadro combinado, el texto es el contenido de la parte del control de edición (o texto estático) del cuadro combinado. Para un botón, el texto es el nombre del botón. Para otras ventanas, el texto es el título de la ventana. Para copiar el texto de un elemento en un cuadro de lista, una aplicación puede usar el [**mensaje \_ LB GETTEXT.**](../controls/lb-gettext.md)

Cuando el **mensaje \_ WM GETTEXT** se envía a un control estático con el estilo ICON de **\_ SS,** se devolverá un identificador al icono en los cuatro primeros bytes del búfer al que *apunta lParam*. Esto solo es cierto si se ha usado el mensaje [**\_ WM SETTEXT**](wm-settext.md) para establecer el icono.

**Edición enriquecte:** Si el texto que se va a copiar supera los 64 000, use el mensaje [**EM \_ STREAMOUT**](../controls/em-streamout.md) o [**EM \_ GETSELTEXT.**](../controls/em-getseltext.md)

El envío **de un \_ mensaje GETTEXT** de WM a un control estático que no es de texto, como un mapa de bits estático o un control de icono estático, no devuelve un valor de cadena. En su lugar, devuelve cero. Además, en las primeras versiones de Windows, las aplicaciones podían enviar un mensaje **\_ GETTEXT de WM** a un control estático que no es de texto para recuperar el identificador del control. Para recuperar el identificador de un control, las aplicaciones pueden usar [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) pasando el identificador **de \_ GWL** como valor de índice o [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) mediante el identificador **de GWLP \_**.

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

[**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
</dt> <dt>

[**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
</dt> <dt>

[**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**GetWindowTextLength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[**WM \_ GETTEXTLENGTH**](wm-gettextlength.md)
</dt> <dt>

[**WM \_ SETTEXT**](wm-settext.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**EM \_ GETSELTEXT**](../controls/em-getseltext.md)
</dt> <dt>

[**STREAMOUT DE EM \_**](../controls/em-streamout.md)
</dt> <dt>

[**LB \_ GETTEXT**](../controls/lb-gettext.md)
</dt> </dl>

 

 
