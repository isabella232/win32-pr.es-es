---
title: Cerrar la ventana
description: Cuando el usuario cierra una ventana, esa acción desencadena una secuencia de mensajes de ventana.
ms.assetid: f0449f11-0569-4a3a-92bc-bced7e0db516
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6422966d6b0351654632a1c77b7ebf07e2b5ffef
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904610"
---
# <a name="closing-the-window"></a><span data-ttu-id="2b029-103">Cerrar la ventana</span><span class="sxs-lookup"><span data-stu-id="2b029-103">Closing the Window</span></span>

<span data-ttu-id="2b029-104">Cuando el usuario cierra una ventana, esa acción desencadena una secuencia de mensajes de ventana.</span><span class="sxs-lookup"><span data-stu-id="2b029-104">When the user closes a window, that action triggers a sequence of window messages.</span></span>

<span data-ttu-id="2b029-105">El usuario puede cerrar una ventana de la aplicación haciendo clic en el botón **cerrar** o usando un método abreviado de teclado, como Alt + F4.</span><span class="sxs-lookup"><span data-stu-id="2b029-105">The user can close an application window by clicking the **Close** button, or by using a keyboard shortcut such as ALT+F4.</span></span> <span data-ttu-id="2b029-106">Cualquiera de estas acciones hace que la ventana reciba un mensaje de [**\_ cierre de WM**](/windows/desktop/winmsg/wm-close) .</span><span class="sxs-lookup"><span data-stu-id="2b029-106">Any of these actions causes the window to receive a [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close) message.</span></span> <span data-ttu-id="2b029-107">El mensaje de **\_ cierre de WM** le ofrece la oportunidad de preguntar al usuario antes de cerrar la ventana.</span><span class="sxs-lookup"><span data-stu-id="2b029-107">The **WM\_CLOSE** message gives you an opportunity to prompt the user before closing the window.</span></span> <span data-ttu-id="2b029-108">Si realmente desea cerrar la ventana, llame a la función [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) .</span><span class="sxs-lookup"><span data-stu-id="2b029-108">If you really do want to close the window, call the [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) function.</span></span> <span data-ttu-id="2b029-109">De lo contrario, simplemente devuelva cero desde el mensaje de **\_ cierre de WM** y el sistema operativo omitirá el mensaje y no destruirá la ventana.</span><span class="sxs-lookup"><span data-stu-id="2b029-109">Otherwise, simply return zero from the **WM\_CLOSE** message, and the operating system will ignore the message and not destroy the window.</span></span>

<span data-ttu-id="2b029-110">Este es un ejemplo de cómo un programa puede controlar [**el \_ cierre de WM**](/windows/desktop/winmsg/wm-close).</span><span class="sxs-lookup"><span data-stu-id="2b029-110">Here is an example of how a program might handle [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close).</span></span>

```C++
case WM_CLOSE:
    if (MessageBox(hwnd, L"Really quit?", L"My application", MB_OKCANCEL) == IDOK)
    {
        DestroyWindow(hwnd);
    }
    // Else: User canceled. Do nothing.
    return 0;
```

<span data-ttu-id="2b029-111">En este ejemplo, la función [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) muestra un cuadro de diálogo modal que contiene los botones **Aceptar** y **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="2b029-111">In this example, the [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) function shows a modal dialog that contains **OK** and **Cancel** buttons.</span></span> <span data-ttu-id="2b029-112">Si el usuario hace clic en **Aceptar**, el programa llama a [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow).</span><span class="sxs-lookup"><span data-stu-id="2b029-112">If the user clicks **OK**, the program calls [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow).</span></span> <span data-ttu-id="2b029-113">De lo contrario, si el usuario hace clic en **Cancelar**, se omite la llamada a **DestroyWindow** y la ventana permanece abierta.</span><span class="sxs-lookup"><span data-stu-id="2b029-113">Otherwise, if the user clicks **Cancel**, the call to **DestroyWindow** is skipped, and the window remains open.</span></span> <span data-ttu-id="2b029-114">En cualquier caso, devuelva cero para indicar que se ha controlado el mensaje.</span><span class="sxs-lookup"><span data-stu-id="2b029-114">In either case, return zero to indicate that you handled the message.</span></span>

<span data-ttu-id="2b029-115">Si desea cerrar la ventana sin preguntar al usuario, puede llamar simplemente a [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) sin la llamada a [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox).</span><span class="sxs-lookup"><span data-stu-id="2b029-115">If you want to close the window without prompting the user, you could simply call [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) without the call to [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox).</span></span> <span data-ttu-id="2b029-116">Sin embargo, en este caso, hay un acceso directo.</span><span class="sxs-lookup"><span data-stu-id="2b029-116">However, there is a shortcut in this case.</span></span> <span data-ttu-id="2b029-117">Recuerde que [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ejecuta la acción predeterminada para cualquier mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="2b029-117">Recall that [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) executes the default action for any window message.</span></span> <span data-ttu-id="2b029-118">En el caso de [**\_ Close de WM**](/windows/desktop/winmsg/wm-close), **DefWindowProc** llama automáticamente a **DestroyWindow**.</span><span class="sxs-lookup"><span data-stu-id="2b029-118">In the case of [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close), **DefWindowProc** automatically calls **DestroyWindow**.</span></span> <span data-ttu-id="2b029-119">Esto significa que si se omite el mensaje de **\_ cierre de WM** en la instrucción **Switch** , la ventana se destruye de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2b029-119">That means if you ignore the **WM\_CLOSE** message in your **switch** statement, the window is destroyed by default.</span></span>

<span data-ttu-id="2b029-120">Cuando una ventana está a punto de ser destruida, recibe un mensaje de [**\_ destrucción de WM**](/windows/desktop/winmsg/wm-destroy) .</span><span class="sxs-lookup"><span data-stu-id="2b029-120">When a window is about to be destroyed, it receives a [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message.</span></span> <span data-ttu-id="2b029-121">Este mensaje se envía después de quitar la ventana de la pantalla, pero antes de que se produzca la destrucción (en particular, antes de que se destruyan las ventanas secundarias).</span><span class="sxs-lookup"><span data-stu-id="2b029-121">This message is sent after the window is removed from the screen, but before the destruction occurs (in particular, before any child windows are destroyed).</span></span>

<span data-ttu-id="2b029-122">En la ventana principal de la aplicación, normalmente responderá a la [**\_ destrucción de WM**](/windows/desktop/winmsg/wm-destroy) mediante una llamada a [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage).</span><span class="sxs-lookup"><span data-stu-id="2b029-122">In your main application window, you will typically respond to [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) by calling [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage).</span></span>

```C++
case WM_DESTROY:
    PostQuitMessage(0);
    return 0;
```

<span data-ttu-id="2b029-123">Vimos en la sección de [mensajes de ventana](window-messages.md) que [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) coloca un mensaje de [**\_ salida de WM**](/windows/desktop/winmsg/wm-quit) en la cola de mensajes, lo que hace que el bucle de mensajes finalice.</span><span class="sxs-lookup"><span data-stu-id="2b029-123">We saw in the [Window Messages](window-messages.md) section that [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) puts a [**WM\_QUIT**](/windows/desktop/winmsg/wm-quit) message on the message queue, causing the message loop to end.</span></span>

<span data-ttu-id="2b029-124">Este es un diagrama de flujo en el que se muestra la manera habitual de procesar los mensajes de [**WM \_ Close**](/windows/desktop/winmsg/wm-close) y [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) :</span><span class="sxs-lookup"><span data-stu-id="2b029-124">Here is a flow chart showing the typical way to process [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close) and [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) messages:</span></span>

![diagrama de flujo que muestra cómo controlar \- los mensajes de WM Close y WM \- Destroy](images/wmclose01.png)

## <a name="next"></a><span data-ttu-id="2b029-126">Siguientes</span><span class="sxs-lookup"><span data-stu-id="2b029-126">Next</span></span>

[<span data-ttu-id="2b029-127">Administración del estado de la aplicación</span><span class="sxs-lookup"><span data-stu-id="2b029-127">Managing Application State</span></span>](managing-application-state-.md)