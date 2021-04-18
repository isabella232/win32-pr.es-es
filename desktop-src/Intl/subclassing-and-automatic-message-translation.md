---
description: La subclase es una técnica que permite a una aplicación interceptar y procesar los mensajes enviados o publicados en una ventana determinada antes de que un procedimiento de ventana tenga la oportunidad de procesarlos.
ms.assetid: 6f7ee9ff-479d-4cb0-8de1-1c3b671551f9
title: Subclase y traducción automática de mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7f0aebabe4bde259a982152327ce61a14de915c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687935"
---
# <a name="subclassing-and-automatic-message-translation"></a>Subclase y traducción automática de mensajes

La subclase es una técnica que permite a una aplicación interceptar y procesar los mensajes enviados o publicados en una ventana determinada antes de que un procedimiento de ventana tenga la oportunidad de procesarlos. El sistema operativo traduce automáticamente los mensajes en la [Página de códigos de Windows (ANSI)](code-pages.md) o en el formato [Unicode](unicode.md) , dependiendo del formulario de la función que ha subclase el procedimiento de ventana.

La siguiente llamada a la función [**SetWindowLongA**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) subclases el procedimiento de ventana actual asociado a la ventana identificada por el parámetro *hWnd* . Como alternativa, una aplicación puede usar [**SetWindowLongPtrA**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra). El nuevo procedimiento de ventana **NewWndProc**, recibirá mensajes con texto en formato de página de códigos de Windows.


```C++
OldWndProc = (WNDPROC) SetWindowLongA(hWnd,
             GWL_WNDPROC, (LONG)NewWndProc); 
```



Cuando **NewWndProc** ha finalizado el procesamiento de un mensaje, utiliza la función [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) como se indica a continuación para pasar el mensaje a **OldWndProc**.


```C++
CallWindowProc(OldWndProc, hWnd, uMessage, wParam, lParam);
```



Si **OldWndProc** se creó con un estilo de clase de Unicode, los mensajes se traducen desde el formulario de página de códigos de Windows recibido por **NewWndProc** a Unicode.

Del mismo modo, una llamada a la función [**SetWindowLongW**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) o [**SetWindowLongPtrW**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) subclases del procedimiento de ventana actual con un procedimiento de ventana que espera mensajes de texto Unicode. La traducción de mensajes, si es necesario, se realiza durante el procesamiento de la función [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) .

Para obtener más información sobre las subclases, vea [procedimientos de ventana](../winmsg/window-procedures.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar Unicode y juegos de caracteres](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
