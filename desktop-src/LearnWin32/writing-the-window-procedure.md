---
title: Escribir el procedimiento de ventana
description: .
ms.assetid: f022bb88-6e4c-4ec4-9eef-f125ad92167e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f11b22ba5dd0653905ca4e2bdb546d106183fc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105676359"
---
# <a name="writing-the-window-procedure"></a><span data-ttu-id="d37a4-103">Escribir el procedimiento de ventana</span><span class="sxs-lookup"><span data-stu-id="d37a4-103">Writing the Window Procedure</span></span>

<span data-ttu-id="d37a4-104">La función [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) llama al procedimiento de ventana de la ventana que es el destino del mensaje.</span><span class="sxs-lookup"><span data-stu-id="d37a4-104">The [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) function calls the window procedure of the window that is the target of the message.</span></span> <span data-ttu-id="d37a4-105">El procedimiento de ventana tiene la siguiente firma.</span><span class="sxs-lookup"><span data-stu-id="d37a4-105">The window procedure has the following signature.</span></span>

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam);
```

<span data-ttu-id="d37a4-106">Hay cuatro parámetros:</span><span class="sxs-lookup"><span data-stu-id="d37a4-106">There are four parameters:</span></span>

- <span data-ttu-id="d37a4-107">*hWnd* es un identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="d37a4-107">*hwnd* is a handle to the window.</span></span>
- <span data-ttu-id="d37a4-108">*uMsg* es el código del mensaje; por ejemplo, el mensaje de [**\_ tamaño de WM**](/windows/desktop/winmsg/wm-size) indica que se ha cambiado el tamaño de la ventana.</span><span class="sxs-lookup"><span data-stu-id="d37a4-108">*uMsg* is the message code; for example, the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message indicates the window was resized.</span></span>
- <span data-ttu-id="d37a4-109">*wParam* y *lParam* contienen datos adicionales relacionados con el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d37a4-109">*wParam* and *lParam* contain additional data that pertains to the message.</span></span> <span data-ttu-id="d37a4-110">El significado exacto depende del código del mensaje.</span><span class="sxs-lookup"><span data-stu-id="d37a4-110">The exact meaning depends on the message code.</span></span>

<span data-ttu-id="d37a4-111">**LRESULT** es un valor entero que el programa devuelve a Windows.</span><span class="sxs-lookup"><span data-stu-id="d37a4-111">**LRESULT** is an integer value that your program returns to Windows.</span></span> <span data-ttu-id="d37a4-112">Contiene la respuesta del programa a un mensaje determinado.</span><span class="sxs-lookup"><span data-stu-id="d37a4-112">It contains your program's response to a particular message.</span></span> <span data-ttu-id="d37a4-113">El significado de este valor depende del código del mensaje.</span><span class="sxs-lookup"><span data-stu-id="d37a4-113">The meaning of this value depends on the message code.</span></span> <span data-ttu-id="d37a4-114">**Callback** es la Convención de llamada de la función.</span><span class="sxs-lookup"><span data-stu-id="d37a4-114">**CALLBACK** is the calling convention for the function.</span></span>

<span data-ttu-id="d37a4-115">Un procedimiento de ventana típico es simplemente una gran instrucción switch que cambia en el código del mensaje.</span><span class="sxs-lookup"><span data-stu-id="d37a4-115">A typical window procedure is simply a large switch statement that switches on the message code.</span></span> <span data-ttu-id="d37a4-116">Agregue casos para cada mensaje que desee controlar.</span><span class="sxs-lookup"><span data-stu-id="d37a4-116">Add cases for each message that you want to handle.</span></span>

```C++
switch (uMsg)
{
    case WM_SIZE: // Handle window resizing

    // etc
}
```

<span data-ttu-id="d37a4-117">Los datos adicionales para el mensaje se encuentran en los parámetros *lParam* y *wParam* .</span><span class="sxs-lookup"><span data-stu-id="d37a4-117">Additional data for the message is contained in the *lParam* and *wParam* parameters.</span></span> <span data-ttu-id="d37a4-118">Ambos parámetros son valores enteros el tamaño de un puntero de ancho (32 bits o 64 bits).</span><span class="sxs-lookup"><span data-stu-id="d37a4-118">Both parameters are integer values the size of a pointer width (32 bits or 64 bits).</span></span> <span data-ttu-id="d37a4-119">El significado de cada depende del código del mensaje (*uMsg*).</span><span class="sxs-lookup"><span data-stu-id="d37a4-119">The meaning of each depends on the message code (*uMsg*).</span></span> <span data-ttu-id="d37a4-120">Para cada mensaje, tendrá que buscar el código de mensaje en MSDN y convertir los parámetros al tipo de datos correcto.</span><span class="sxs-lookup"><span data-stu-id="d37a4-120">For each message, you will need to look up the message code on MSDN and cast the parameters to the correct data type.</span></span> <span data-ttu-id="d37a4-121">Normalmente, los datos son un valor numérico o un puntero a una estructura.</span><span class="sxs-lookup"><span data-stu-id="d37a4-121">Usually the data is either a numeric value or a pointer to a structure.</span></span> <span data-ttu-id="d37a4-122">Algunos mensajes no tienen datos.</span><span class="sxs-lookup"><span data-stu-id="d37a4-122">Some messages do not have any data.</span></span>

<span data-ttu-id="d37a4-123">Por ejemplo, la documentación del mensaje [**de \_ tamaño de WM**](/windows/desktop/winmsg/wm-size) indica que:</span><span class="sxs-lookup"><span data-stu-id="d37a4-123">For example, the documentation for the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message states that:</span></span>

- <span data-ttu-id="d37a4-124">*wParam* es una marca que indica si la ventana se ha minimizado, maximizado o cambiado de tamaño.</span><span class="sxs-lookup"><span data-stu-id="d37a4-124">*wParam* is a flag that indicates whether the window was minimized, maximized, or resized.</span></span>
- <span data-ttu-id="d37a4-125">*lParam* contiene el nuevo ancho y alto de la ventana como valores de 16 bits empaquetados en un número de 1 32 o 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d37a4-125">*lParam* contains the new width and height of the window as 16-bit values packed into one 32- or 64-bit number.</span></span> <span data-ttu-id="d37a4-126">Tendrá que realizar algún cambio de bits para obtener estos valores.</span><span class="sxs-lookup"><span data-stu-id="d37a4-126">You will need to perform some bit-shifting to get these values.</span></span> <span data-ttu-id="d37a4-127">Afortunadamente, el archivo de encabezado WinDef. h incluye macros auxiliares que lo hacen.</span><span class="sxs-lookup"><span data-stu-id="d37a4-127">Fortunately, the header file WinDef.h includes helper macros that do this.</span></span>

<span data-ttu-id="d37a4-128">Un procedimiento de ventana típico controla docenas de mensajes, por lo que puede crecer bastante.</span><span class="sxs-lookup"><span data-stu-id="d37a4-128">A typical window procedure handles dozens of messages, so it can grow quite long.</span></span> <span data-ttu-id="d37a4-129">Una manera de hacer que el código sea más modular es colocar la lógica para controlar cada mensaje en una función independiente.</span><span class="sxs-lookup"><span data-stu-id="d37a4-129">One way to make your code more modular is to put the logic for handling each message in a separate function.</span></span> <span data-ttu-id="d37a4-130">En el procedimiento de ventana, convierta los parámetros *wParam* e *lParam* al tipo de datos correcto y pase esos valores a la función.</span><span class="sxs-lookup"><span data-stu-id="d37a4-130">In the window procedure, cast the *wParam* and *lParam* parameters to the correct data type, and pass those values to the function.</span></span> <span data-ttu-id="d37a4-131">Por ejemplo, para controlar el mensaje de [**\_ tamaño de WM**](/windows/desktop/winmsg/wm-size) , el procedimiento de ventana tendría el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="d37a4-131">For example, to handle the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message, the window procedure would look like this:</span></span>

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_SIZE:
        {
            int width = LOWORD(lParam);  // Macro to get the low-order word.
            int height = HIWORD(lParam); // Macro to get the high-order word.

            // Respond to the message:
            OnSize(hwnd, (UINT)wParam, width, height);
        }
        break;
    }
}

void OnSize(HWND hwnd, UINT flag, int width, int height)
{
    // Handle resizing
}
```

<span data-ttu-id="d37a4-132">Las macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) y [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) obtienen los valores de ancho y alto de 16 bits de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="d37a4-132">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros get the 16-bit width and height values from *lParam*.</span></span> <span data-ttu-id="d37a4-133">(Puede buscar estos tipos de detalles en la documentación de MSDN para cada código de mensaje). El procedimiento de ventana extrae el ancho y el alto y, a continuación, pasa estos valores a la `OnSize` función.</span><span class="sxs-lookup"><span data-stu-id="d37a4-133">(You can look up these kinds of details in the MSDN documentation for each message code.) The window procedure extracts the width and height, and then passes these values to the `OnSize` function.</span></span>

## <a name="default-message-handling"></a><span data-ttu-id="d37a4-134">Control de mensajes predeterminado</span><span class="sxs-lookup"><span data-stu-id="d37a4-134">Default Message Handling</span></span>

<span data-ttu-id="d37a4-135">Si no controla un mensaje determinado en el procedimiento de ventana, pase los parámetros de mensaje directamente a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="d37a4-135">If you don't handle a particular message in your window procedure, pass the message parameters directly to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="d37a4-136">Esta función realiza la acción predeterminada para el mensaje, que varía según el tipo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="d37a4-136">This function performs the default action for the message, which varies by message type.</span></span>

```C++
return DefWindowProc(hwnd, uMsg, wParam, lParam);
```

## <a name="avoiding-bottlenecks-in-your-window-procedure"></a><span data-ttu-id="d37a4-137">Evitar cuellos de botella en el procedimiento de ventana</span><span class="sxs-lookup"><span data-stu-id="d37a4-137">Avoiding Bottlenecks in Your Window Procedure</span></span>

<span data-ttu-id="d37a4-138">Mientras se ejecuta el procedimiento de ventana, se bloquea cualquier otro mensaje para Windows creado en el mismo subproceso.</span><span class="sxs-lookup"><span data-stu-id="d37a4-138">While your window procedure executes, it blocks any other messages for windows created on the same thread.</span></span> <span data-ttu-id="d37a4-139">Por lo tanto, evite el procesamiento largo dentro del procedimiento de ventana.</span><span class="sxs-lookup"><span data-stu-id="d37a4-139">Therefore, avoid lengthy processing inside your window procedure.</span></span> <span data-ttu-id="d37a4-140">Por ejemplo, supongamos que el programa abre una conexión TCP y espera indefinidamente a que el servidor responda.</span><span class="sxs-lookup"><span data-stu-id="d37a4-140">For example, suppose your program opens a TCP connection and waits indefinitely for the server to respond.</span></span> <span data-ttu-id="d37a4-141">Si lo hace dentro del procedimiento de ventana, la interfaz de usuario no responderá hasta que se complete la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d37a4-141">If you do that inside the window procedure, your UI will not respond until the request completes.</span></span> <span data-ttu-id="d37a4-142">Durante ese tiempo, la ventana no puede procesar la entrada del mouse o del teclado, volver a dibujarse o incluso cerrarse.</span><span class="sxs-lookup"><span data-stu-id="d37a4-142">During that time, the window cannot process mouse or keyboard input, repaint itself, or even close.</span></span>

<span data-ttu-id="d37a4-143">En su lugar, debe trasladar el trabajo a otro subproceso, utilizando uno de los recursos de multitarea integrados en Windows:</span><span class="sxs-lookup"><span data-stu-id="d37a4-143">Instead, you should move the work to another thread, using one of the multitasking facilities that are built into Windows:</span></span>

- <span data-ttu-id="d37a4-144">Cree un nuevo subproceso.</span><span class="sxs-lookup"><span data-stu-id="d37a4-144">Create a new thread.</span></span>
- <span data-ttu-id="d37a4-145">Use un grupo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="d37a4-145">Use a thread pool.</span></span>
- <span data-ttu-id="d37a4-146">Usar llamadas de e/s asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="d37a4-146">Use asynchronous I/O calls.</span></span>
- <span data-ttu-id="d37a4-147">Use llamadas a procedimientos asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="d37a4-147">Use asynchronous procedure calls.</span></span>

## <a name="next"></a><span data-ttu-id="d37a4-148">Siguientes</span><span class="sxs-lookup"><span data-stu-id="d37a4-148">Next</span></span>

[<span data-ttu-id="d37a4-149">Pintar la ventana</span><span class="sxs-lookup"><span data-stu-id="d37a4-149">Painting the Window</span></span>](painting-the-window.md)