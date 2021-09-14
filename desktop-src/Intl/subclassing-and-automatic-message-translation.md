---
description: La subclases es una técnica que permite a una aplicación interceptar y procesar los mensajes enviados o publicados en una ventana determinada antes de que un procedimiento de ventana tenga la oportunidad de procesarlos.
ms.assetid: 6f7ee9ff-479d-4cb0-8de1-1c3b671551f9
title: Subclases y traducción automática de mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7f0aebabe4bde259a982152327ce61a14de915c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171894"
---
# <a name="subclassing-and-automatic-message-translation"></a>Subclases y traducción automática de mensajes

La subclases es una técnica que permite a una aplicación interceptar y procesar los mensajes enviados o publicados en una ventana determinada antes de que un procedimiento de ventana tenga la oportunidad de procesarlos. El sistema operativo traduce automáticamente los mensajes Windows una página de códigos [(ANSI)](code-pages.md) o un formulario [Unicode,](unicode.md) en función del formato de la función que ha incluido subclases en el procedimiento de ventana.

La siguiente llamada a la [**función SetWindowLongA**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) subclases del procedimiento de ventana actual asociado a la ventana identificada por el *parámetro hWnd.* Como alternativa, una aplicación puede usar [**SetWindowLongPtrA**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra). El nuevo procedimiento de ventana **NewWndProc** recibirá mensajes con texto en Windows formato de página de códigos.


```C++
OldWndProc = (WNDPROC) SetWindowLongA(hWnd,
             GWL_WNDPROC, (LONG)NewWndProc); 
```



Cuando **NewWndProc** ha terminado de procesar un mensaje, usa la función [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) como se indica a continuación para pasar el mensaje a **OldWndProc**.


```C++
CallWindowProc(OldWndProc, hWnd, uMessage, wParam, lParam);
```



Si **OldWndProc** se creó con un estilo de clase UNICODE, los mensajes se traducen desde el formulario de página de códigos Windows recibido por **NewWndProc** a Unicode.

De forma similar, una llamada a las subclases de la función [**SetWindowLongW**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) o [**SetWindowLongPtrW**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) establece el procedimiento de ventana actual con un procedimiento de ventana que espera mensajes de texto Unicode. La traducción de mensajes, si es necesario, se realiza durante el procesamiento de [**la función CallWindowProc.**](/windows/win32/api/winuser/nf-winuser-callwindowproca)

Para obtener más información sobre las subclases, vea [Procedimientos de ventana](../winmsg/window-procedures.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Unicode y juegos de caracteres](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
