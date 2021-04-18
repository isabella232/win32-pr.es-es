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
# <a name="subclassing-and-automatic-message-translation"></a><span data-ttu-id="246f0-103">Subclase y traducción automática de mensajes</span><span class="sxs-lookup"><span data-stu-id="246f0-103">Subclassing and Automatic Message Translation</span></span>

<span data-ttu-id="246f0-104">La subclase es una técnica que permite a una aplicación interceptar y procesar los mensajes enviados o publicados en una ventana determinada antes de que un procedimiento de ventana tenga la oportunidad de procesarlos.</span><span class="sxs-lookup"><span data-stu-id="246f0-104">Subclassing is a technique that allows an application to intercept and process messages sent or posted to a particular window before a window procedure has a chance to process them.</span></span> <span data-ttu-id="246f0-105">El sistema operativo traduce automáticamente los mensajes en la [Página de códigos de Windows (ANSI)](code-pages.md) o en el formato [Unicode](unicode.md) , dependiendo del formulario de la función que ha subclase el procedimiento de ventana.</span><span class="sxs-lookup"><span data-stu-id="246f0-105">The operating system automatically translates messages into [Windows (ANSI) code page](code-pages.md) or [Unicode](unicode.md) form, depending on the form of the function that has subclassed the window procedure.</span></span>

<span data-ttu-id="246f0-106">La siguiente llamada a la función [**SetWindowLongA**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) subclases el procedimiento de ventana actual asociado a la ventana identificada por el parámetro *hWnd* .</span><span class="sxs-lookup"><span data-stu-id="246f0-106">The following call to the [**SetWindowLongA**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function subclasses the current window procedure associated with the window identified by the *hWnd* parameter.</span></span> <span data-ttu-id="246f0-107">Como alternativa, una aplicación puede usar [**SetWindowLongPtrA**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra).</span><span class="sxs-lookup"><span data-stu-id="246f0-107">Alternatively, an application can use [**SetWindowLongPtrA**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra).</span></span> <span data-ttu-id="246f0-108">El nuevo procedimiento de ventana **NewWndProc**, recibirá mensajes con texto en formato de página de códigos de Windows.</span><span class="sxs-lookup"><span data-stu-id="246f0-108">The new window procedure **NewWndProc**, will receive messages with text in Windows code page format.</span></span>


```C++
OldWndProc = (WNDPROC) SetWindowLongA(hWnd,
             GWL_WNDPROC, (LONG)NewWndProc); 
```



<span data-ttu-id="246f0-109">Cuando **NewWndProc** ha finalizado el procesamiento de un mensaje, utiliza la función [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) como se indica a continuación para pasar el mensaje a **OldWndProc**.</span><span class="sxs-lookup"><span data-stu-id="246f0-109">When **NewWndProc** has finished processing a message, it uses the [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) function as follows to pass the message to **OldWndProc**.</span></span>


```C++
CallWindowProc(OldWndProc, hWnd, uMessage, wParam, lParam);
```



<span data-ttu-id="246f0-110">Si **OldWndProc** se creó con un estilo de clase de Unicode, los mensajes se traducen desde el formulario de página de códigos de Windows recibido por **NewWndProc** a Unicode.</span><span class="sxs-lookup"><span data-stu-id="246f0-110">If **OldWndProc** was created with a class style of UNICODE, messages are translated from the Windows code page form received by **NewWndProc** into Unicode.</span></span>

<span data-ttu-id="246f0-111">Del mismo modo, una llamada a la función [**SetWindowLongW**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) o [**SetWindowLongPtrW**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) subclases del procedimiento de ventana actual con un procedimiento de ventana que espera mensajes de texto Unicode.</span><span class="sxs-lookup"><span data-stu-id="246f0-111">Similarly, a call to the [**SetWindowLongW**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) or [**SetWindowLongPtrW**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) function subclasses the current window procedure with a window procedure that expects Unicode text messages.</span></span> <span data-ttu-id="246f0-112">La traducción de mensajes, si es necesario, se realiza durante el procesamiento de la función [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="246f0-112">Message translation, if necessary, is performed during the processing of the [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) function.</span></span>

<span data-ttu-id="246f0-113">Para obtener más información sobre las subclases, vea [procedimientos de ventana](../winmsg/window-procedures.md).</span><span class="sxs-lookup"><span data-stu-id="246f0-113">For more information about subclassing, see [Window Procedures](../winmsg/window-procedures.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="246f0-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="246f0-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="246f0-115">Usar Unicode y juegos de caracteres</span><span class="sxs-lookup"><span data-stu-id="246f0-115">Using Unicode and Character Sets</span></span>](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
