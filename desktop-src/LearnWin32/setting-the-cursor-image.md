---
title: Establecer la imagen del cursor
description: Establecer la imagen del cursor
ms.assetid: FB223131-19AE-41DD-87DE-73992AE2A0CA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3bc993b7566dee1fa47bd2b53c270ad0e4f64b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487610"
---
# <a name="setting-the-cursor-image"></a><span data-ttu-id="67eda-103">Establecer la imagen del cursor</span><span class="sxs-lookup"><span data-stu-id="67eda-103">Setting the Cursor Image</span></span>

<span data-ttu-id="67eda-104">El *cursor* es la imagen pequeña que muestra la ubicación del mouse u otro dispositivo señalador.</span><span class="sxs-lookup"><span data-stu-id="67eda-104">The *cursor* is the small image that shows the location of the mouse or other pointing device.</span></span> <span data-ttu-id="67eda-105">Muchas aplicaciones cambian la imagen del cursor para proporcionar comentarios al usuario.</span><span class="sxs-lookup"><span data-stu-id="67eda-105">Many applications change the cursor image to give feedback to the user.</span></span> <span data-ttu-id="67eda-106">Aunque no es necesario, agrega un buen aspecto a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="67eda-106">Although it is not required, it adds a nice bit of polish to your application.</span></span>

<span data-ttu-id="67eda-107">Windows proporciona un conjunto de imágenes de cursores estándar, llamadas *cursores del sistema*.</span><span class="sxs-lookup"><span data-stu-id="67eda-107">Windows provides a set of standard cursor images, called *system cursors*.</span></span> <span data-ttu-id="67eda-108">Entre ellas se incluyen la flecha, la mano, el rayo, el reloj de arena (que ahora es un círculo girado) y otros.</span><span class="sxs-lookup"><span data-stu-id="67eda-108">These include the arrow, the hand, the I-beam, the hourglass (which is now a spinning circle), and others.</span></span> <span data-ttu-id="67eda-109">En esta sección se describe cómo usar los cursores del sistema.</span><span class="sxs-lookup"><span data-stu-id="67eda-109">This section describes how to use the system cursors.</span></span> <span data-ttu-id="67eda-110">Para tareas más avanzadas, como la creación de cursores personalizados, vea [cursores](/windows/desktop/menurc/cursors).</span><span class="sxs-lookup"><span data-stu-id="67eda-110">For more advanced tasks, such as creating custom cursors, see [Cursors](/windows/desktop/menurc/cursors).</span></span>

<span data-ttu-id="67eda-111">Puede asociar un cursor a una clase de ventana estableciendo el miembro **hCursor** de la estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) o [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) .</span><span class="sxs-lookup"><span data-stu-id="67eda-111">You can associate a cursor with a window class by setting the **hCursor** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) or [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) structure.</span></span> <span data-ttu-id="67eda-112">De lo contrario, el cursor predeterminado es la flecha.</span><span class="sxs-lookup"><span data-stu-id="67eda-112">Otherwise, the default cursor is the arrow.</span></span> <span data-ttu-id="67eda-113">Cuando el mouse se mueve sobre una ventana, la ventana recibe un mensaje de [**\_ SETCURSOR de WM**](/windows/desktop/menurc/wm-setcursor) (a menos que otra ventana haya capturado el mouse).</span><span class="sxs-lookup"><span data-stu-id="67eda-113">When the mouse moves over a window, the window receives a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message (unless another window has captured the mouse).</span></span> <span data-ttu-id="67eda-114">En este momento, se produce uno de los siguientes eventos:</span><span class="sxs-lookup"><span data-stu-id="67eda-114">At this point, one of the following events occurs:</span></span>

-   <span data-ttu-id="67eda-115">La aplicación establece el cursor y el procedimiento de ventana devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="67eda-115">The application sets the cursor and the window procedure returns **TRUE**.</span></span>
-   <span data-ttu-id="67eda-116">La aplicación no realiza ninguna acción y pasa [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="67eda-116">The application does nothing and passes [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="67eda-117">Para establecer el cursor, un programa hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="67eda-117">To set the cursor, a program does the following:</span></span>

1.  <span data-ttu-id="67eda-118">Llama a [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) para cargar el cursor en la memoria.</span><span class="sxs-lookup"><span data-stu-id="67eda-118">Calls [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) to load the cursor into memory.</span></span> <span data-ttu-id="67eda-119">Esta función devuelve un identificador al cursor.</span><span class="sxs-lookup"><span data-stu-id="67eda-119">This function returns a handle to the cursor.</span></span>
2.  <span data-ttu-id="67eda-120">Llama a [**setCursor**](/windows/desktop/api/winuser/nf-winuser-setcursor) y pasa el identificador del cursor.</span><span class="sxs-lookup"><span data-stu-id="67eda-120">Calls [**SetCursor**](/windows/desktop/api/winuser/nf-winuser-setcursor) and passes in the cursor handle.</span></span>

<span data-ttu-id="67eda-121">De lo contrario, si la aplicación pasa [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), la función **DefWindowProc** usa el siguiente algoritmo para establecer la imagen del cursor:</span><span class="sxs-lookup"><span data-stu-id="67eda-121">Otherwise, if the application passes [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), the **DefWindowProc** function uses the following algorithm to set the cursor image:</span></span>

1.  <span data-ttu-id="67eda-122">Si la ventana tiene un elemento primario, reenvíe el mensaje de [**\_ SETCURSOR de WM**](/windows/desktop/menurc/wm-setcursor) al elemento primario para controlar.</span><span class="sxs-lookup"><span data-stu-id="67eda-122">If the window has a parent, forward the [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message to the parent to handle.</span></span>
2.  <span data-ttu-id="67eda-123">De lo contrario, si la ventana tiene un cursor de clase, establezca el cursor en el cursor de clase.</span><span class="sxs-lookup"><span data-stu-id="67eda-123">Otherwise, if the window has a class cursor, set the cursor to the class cursor.</span></span>
3.  <span data-ttu-id="67eda-124">Si no hay ningún cursor de clase, establezca el cursor en el cursor de flecha.</span><span class="sxs-lookup"><span data-stu-id="67eda-124">If there is no class cursor, set the cursor to the arrow cursor.</span></span>

<span data-ttu-id="67eda-125">La función [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) puede cargar un cursor personalizado de un recurso, o uno de los cursores del sistema.</span><span class="sxs-lookup"><span data-stu-id="67eda-125">The [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) function can load either a custom cursor from a resource, or one of the system cursors.</span></span> <span data-ttu-id="67eda-126">En el ejemplo siguiente se muestra cómo establecer el cursor en el cursor de mano del sistema.</span><span class="sxs-lookup"><span data-stu-id="67eda-126">The following example shows how to set the cursor to the system hand cursor.</span></span>


```C++
    hCursor = LoadCursor(NULL, cursor);
    SetCursor(hCursor);
```



<span data-ttu-id="67eda-127">Si cambia el cursor, la imagen del cursor se restablecerá en el siguiente movimiento del mouse, a menos que se intercepte el mensaje de [**\_ SETCURSOR de WM**](/windows/desktop/menurc/wm-setcursor) y se vuelva a establecer el cursor.</span><span class="sxs-lookup"><span data-stu-id="67eda-127">If you change the cursor, the cursor image resets on the next mouse move, unless you intercept the [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message and set the cursor again.</span></span> <span data-ttu-id="67eda-128">En el código siguiente se muestra cómo administrar **WM \_ SETCURSOR**.</span><span class="sxs-lookup"><span data-stu-id="67eda-128">The following code shows how to handle **WM\_SETCURSOR**.</span></span>


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



<span data-ttu-id="67eda-129">Este código comprueba primero los 16 bits inferiores de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="67eda-129">This code first checks the lower 16 bits of *lParam*.</span></span> <span data-ttu-id="67eda-130">Si es `LOWORD(lParam)` igual a **HTCLIENT**, significa que el cursor está sobre el área cliente de la ventana.</span><span class="sxs-lookup"><span data-stu-id="67eda-130">If `LOWORD(lParam)` equals **HTCLIENT**, it means the cursor is over the client area of the window.</span></span> <span data-ttu-id="67eda-131">De lo contrario, el cursor se encuentra sobre el área no cliente.</span><span class="sxs-lookup"><span data-stu-id="67eda-131">Otherwise, the cursor is over the nonclient area.</span></span> <span data-ttu-id="67eda-132">Normalmente, solo debe establecer el cursor para el área cliente y dejar que Windows configure el cursor para el área no cliente.</span><span class="sxs-lookup"><span data-stu-id="67eda-132">Typically, you should only set the cursor for the client area, and let Windows set the cursor for the nonclient area.</span></span>

## <a name="next"></a><span data-ttu-id="67eda-133">Siguientes</span><span class="sxs-lookup"><span data-stu-id="67eda-133">Next</span></span>

[<span data-ttu-id="67eda-134">Entrada de usuario: ejemplo extendido</span><span class="sxs-lookup"><span data-stu-id="67eda-134">User Input: Extended Example</span></span>](user-input--extended-example.md)

 

 