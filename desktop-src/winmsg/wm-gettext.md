---
description: Copia el texto que corresponde a una ventana en un búfer proporcionado por el autor de la llamada.
ms.assetid: 117c3d6d-24cd-462f-bdb0-b65d8914273a
title: Mensaje de WM_GETTEXT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47f8e2268c1d0ec043e24a001f16abae357bdbdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815454"
---
# <a name="wm_gettext-message"></a>\_Mensaje GETTEXT de WM

Copia el texto que corresponde a una ventana en un búfer proporcionado por el autor de la llamada.


```C++
#define WM_GETTEXT                      0x000D
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número máximo de caracteres que se van a copiar, incluido el carácter nulo de terminación.

Las aplicaciones ANSI pueden tener el tamaño de la cadena en el búfer reducido (a un mínimo de la mitad del valor de *wParam* ) debido a la conversión de ANSI a Unicode.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero al búfer que va a recibir el texto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

El valor devuelto es el número de caracteres copiados, sin incluir el carácter nulo de terminación.

## <a name="remarks"></a>Observaciones

La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) copia el texto asociado a la ventana en el búfer especificado y devuelve el número de caracteres copiados. Tenga en cuenta que para los controles estáticos que no son de texto, proporciona el texto con el que se creó originalmente el control, es decir, el número de identificación. Sin embargo, proporciona el identificador del control estático de no texto como se creó originalmente. Es decir, si usa posteriormente un **STM \_ SETIMAGE** para cambiarlo, el identificador original se seguiría devolviendo.

Para un control de edición, el texto que se va a copiar es el contenido del control de edición. En el caso de un cuadro combinado, el texto es el contenido de la parte del control de edición (o texto estático) del cuadro combinado. En el caso de un botón, el texto es el nombre del botón. Para otras ventanas, el texto es el título de la ventana. Para copiar el texto de un elemento en un cuadro de lista, una aplicación puede usar el mensaje [**lb \_ GETTEXT**](../controls/lb-gettext.md) .

Cuando el mensaje de **\_ GETTEXT GETTEXT** se envía a un control estático con el estilo de **\_ icono de SS** , se devolverá un identificador al icono en los primeros cuatro bytes del búfer al que apunta *lParam*. Esto solo es aplicable si se ha utilizado el mensaje de [**WM \_ SETTEXT**](wm-settext.md) para establecer el icono.

**Edición enriquecida:** Si el texto que se va a copiar es superior a 64 k, use el mensaje [**em \_ STREAMOUT**](../controls/em-streamout.md) o [**em \_ GETSELTEXT**](../controls/em-getseltext.md) .

El envío de un mensaje **\_ GETTEXT de WM** a un control estático que no sea de texto, como un mapa de bits estático o un control de icono estático, no devuelve un valor de cadena. En su lugar, devuelve cero. Además, en las primeras versiones de Windows, las aplicaciones pueden enviar un mensaje de **\_ GETTEXT de WM** a un control estático que no es de texto para recuperar el identificador del control. Para recuperar el identificador de un control, las aplicaciones pueden usar [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) pasando **GWL \_ ID** como valor de índice o [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) mediante el **\_ identificador de GWLP**.

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

[**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
</dt> <dt>

[**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
</dt> <dt>

[**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**GetWindowTextLength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[**GETTEXTLENGTH de WM \_**](wm-gettextlength.md)
</dt> <dt>

[**SETTEXT de WM \_**](wm-settext.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**\_GETSELTEXT em**](../controls/em-getseltext.md)
</dt> <dt>

[**\_STREAMOUT em**](../controls/em-streamout.md)
</dt> <dt>

[**\_apgettext GETTEXT**](../controls/lb-gettext.md)
</dt> </dl>

 

 
