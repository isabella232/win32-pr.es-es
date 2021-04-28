---
title: Escribir el procedimiento de ventana
description: Escribir el procedimiento de ventana
ms.assetid: f022bb88-6e4c-4ec4-9eef-f125ad92167e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 832aba88211a7decf20c233f5d9ab4fbeb1b1c27
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105723"
---
# <a name="writing-the-window-procedure"></a><span data-ttu-id="15c88-103">Escribir el procedimiento de ventana</span><span class="sxs-lookup"><span data-stu-id="15c88-103">Writing the Window Procedure</span></span>

<span data-ttu-id="15c88-104">La [**función DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) llama al procedimiento de ventana de la ventana que es el destino del mensaje.</span><span class="sxs-lookup"><span data-stu-id="15c88-104">The [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) function calls the window procedure of the window that is the target of the message.</span></span> <span data-ttu-id="15c88-105">El procedimiento de ventana tiene la firma siguiente.</span><span class="sxs-lookup"><span data-stu-id="15c88-105">The window procedure has the following signature.</span></span>

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam);
```

<span data-ttu-id="15c88-106">Hay cuatro parámetros:</span><span class="sxs-lookup"><span data-stu-id="15c88-106">There are four parameters:</span></span>

- <span data-ttu-id="15c88-107">*hwnd* es un identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="15c88-107">*hwnd* is a handle to the window.</span></span>
- <span data-ttu-id="15c88-108">*uMsg* es el código del mensaje; Por ejemplo, el [**mensaje WM \_ SIZE**](/windows/desktop/winmsg/wm-size) indica que se ha cambiado el tamaño de la ventana.</span><span class="sxs-lookup"><span data-stu-id="15c88-108">*uMsg* is the message code; for example, the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message indicates the window was resized.</span></span>
- <span data-ttu-id="15c88-109">*wParam* e *lParam* contienen datos adicionales que pertenecen al mensaje.</span><span class="sxs-lookup"><span data-stu-id="15c88-109">*wParam* and *lParam* contain additional data that pertains to the message.</span></span> <span data-ttu-id="15c88-110">El significado exacto depende del código del mensaje.</span><span class="sxs-lookup"><span data-stu-id="15c88-110">The exact meaning depends on the message code.</span></span>

<span data-ttu-id="15c88-111">**LRESULT** es un valor entero que el programa devuelve a Windows.</span><span class="sxs-lookup"><span data-stu-id="15c88-111">**LRESULT** is an integer value that your program returns to Windows.</span></span> <span data-ttu-id="15c88-112">Contiene la respuesta del programa a un mensaje determinado.</span><span class="sxs-lookup"><span data-stu-id="15c88-112">It contains your program's response to a particular message.</span></span> <span data-ttu-id="15c88-113">El significado de este valor depende del código del mensaje.</span><span class="sxs-lookup"><span data-stu-id="15c88-113">The meaning of this value depends on the message code.</span></span> <span data-ttu-id="15c88-114">**CALLBACK es** la convención de llamada para la función.</span><span class="sxs-lookup"><span data-stu-id="15c88-114">**CALLBACK** is the calling convention for the function.</span></span>

<span data-ttu-id="15c88-115">Un procedimiento de ventana típico es simplemente una instrucción switch de gran tamaño que activa el código del mensaje.</span><span class="sxs-lookup"><span data-stu-id="15c88-115">A typical window procedure is simply a large switch statement that switches on the message code.</span></span> <span data-ttu-id="15c88-116">Agregue casos para cada mensaje que desee controlar.</span><span class="sxs-lookup"><span data-stu-id="15c88-116">Add cases for each message that you want to handle.</span></span>

```C++
switch (uMsg)
{
    case WM_SIZE: // Handle window resizing

    // etc
}
```

<span data-ttu-id="15c88-117">Los datos adicionales del mensaje se encuentran en los parámetros *lParam* *y wParam.*</span><span class="sxs-lookup"><span data-stu-id="15c88-117">Additional data for the message is contained in the *lParam* and *wParam* parameters.</span></span> <span data-ttu-id="15c88-118">Ambos parámetros son valores enteros del tamaño de un ancho de puntero (32 bits o 64 bits).</span><span class="sxs-lookup"><span data-stu-id="15c88-118">Both parameters are integer values the size of a pointer width (32 bits or 64 bits).</span></span> <span data-ttu-id="15c88-119">El significado de cada uno depende del código del mensaje (*uMsg*).</span><span class="sxs-lookup"><span data-stu-id="15c88-119">The meaning of each depends on the message code (*uMsg*).</span></span> <span data-ttu-id="15c88-120">Para cada mensaje, deberá buscar el código del mensaje en MSDN y convertir los parámetros al tipo de datos correcto.</span><span class="sxs-lookup"><span data-stu-id="15c88-120">For each message, you will need to look up the message code on MSDN and cast the parameters to the correct data type.</span></span> <span data-ttu-id="15c88-121">Normalmente, los datos son un valor numérico o un puntero a una estructura.</span><span class="sxs-lookup"><span data-stu-id="15c88-121">Usually the data is either a numeric value or a pointer to a structure.</span></span> <span data-ttu-id="15c88-122">Algunos mensajes no tienen datos.</span><span class="sxs-lookup"><span data-stu-id="15c88-122">Some messages do not have any data.</span></span>

<span data-ttu-id="15c88-123">Por ejemplo, la documentación del mensaje [**WM \_ SIZE**](/windows/desktop/winmsg/wm-size) indica que:</span><span class="sxs-lookup"><span data-stu-id="15c88-123">For example, the documentation for the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message states that:</span></span>

- <span data-ttu-id="15c88-124">*wParam* es una marca que indica si la ventana se ha minimizado, maximizado o cambiado de tamaño.</span><span class="sxs-lookup"><span data-stu-id="15c88-124">*wParam* is a flag that indicates whether the window was minimized, maximized, or resized.</span></span>
- <span data-ttu-id="15c88-125">*lParam contiene* el nuevo ancho y alto de la ventana como valores de 16 bits empaquetados en un número de 32 o 64 bits.</span><span class="sxs-lookup"><span data-stu-id="15c88-125">*lParam* contains the new width and height of the window as 16-bit values packed into one 32- or 64-bit number.</span></span> <span data-ttu-id="15c88-126">Tendrá que realizar algunos desplazamientos de bits para obtener estos valores.</span><span class="sxs-lookup"><span data-stu-id="15c88-126">You will need to perform some bit-shifting to get these values.</span></span> <span data-ttu-id="15c88-127">Afortunadamente, el archivo de encabezado WinDef.h incluye macros auxiliares que lo hacen.</span><span class="sxs-lookup"><span data-stu-id="15c88-127">Fortunately, the header file WinDef.h includes helper macros that do this.</span></span>

<span data-ttu-id="15c88-128">Un procedimiento de ventana típico controla decenas de mensajes, por lo que puede crecer bastante tiempo.</span><span class="sxs-lookup"><span data-stu-id="15c88-128">A typical window procedure handles dozens of messages, so it can grow quite long.</span></span> <span data-ttu-id="15c88-129">Una manera de hacer que el código sea más modular es colocar la lógica para controlar cada mensaje en una función independiente.</span><span class="sxs-lookup"><span data-stu-id="15c88-129">One way to make your code more modular is to put the logic for handling each message in a separate function.</span></span> <span data-ttu-id="15c88-130">En el procedimiento de ventana, convierte los parámetros *wParam* y *lParam* al tipo de datos correcto y pasa esos valores a la función.</span><span class="sxs-lookup"><span data-stu-id="15c88-130">In the window procedure, cast the *wParam* and *lParam* parameters to the correct data type, and pass those values to the function.</span></span> <span data-ttu-id="15c88-131">Por ejemplo, para controlar el [**mensaje WM \_ SIZE,**](/windows/desktop/winmsg/wm-size) el procedimiento de ventana tendría el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="15c88-131">For example, to handle the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message, the window procedure would look like this:</span></span>

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

<span data-ttu-id="15c88-132">Las [**macros LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) [**e HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) obtienen los valores de ancho y alto de 16 bits *de lParam.*</span><span class="sxs-lookup"><span data-stu-id="15c88-132">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros get the 16-bit width and height values from *lParam*.</span></span> <span data-ttu-id="15c88-133">(Puede buscar estos tipos de detalles en la documentación de MSDN para cada código de mensaje). El procedimiento de ventana extrae el ancho y el alto y, a continuación, pasa estos valores a la `OnSize` función .</span><span class="sxs-lookup"><span data-stu-id="15c88-133">(You can look up these kinds of details in the MSDN documentation for each message code.) The window procedure extracts the width and height, and then passes these values to the `OnSize` function.</span></span>

## <a name="default-message-handling"></a><span data-ttu-id="15c88-134">Control de mensajes predeterminado</span><span class="sxs-lookup"><span data-stu-id="15c88-134">Default Message Handling</span></span>

<span data-ttu-id="15c88-135">Si no controla un mensaje determinado en el procedimiento de ventana, pase los parámetros del mensaje directamente a la [**función DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)</span><span class="sxs-lookup"><span data-stu-id="15c88-135">If you don't handle a particular message in your window procedure, pass the message parameters directly to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="15c88-136">Esta función realiza la acción predeterminada para el mensaje, que varía según el tipo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="15c88-136">This function performs the default action for the message, which varies by message type.</span></span>

```C++
return DefWindowProc(hwnd, uMsg, wParam, lParam);
```

## <a name="avoiding-bottlenecks-in-your-window-procedure"></a><span data-ttu-id="15c88-137">Evitar cuellos de botella en el procedimiento de ventana</span><span class="sxs-lookup"><span data-stu-id="15c88-137">Avoiding Bottlenecks in Your Window Procedure</span></span>

<span data-ttu-id="15c88-138">Mientras se ejecuta el procedimiento de ventana, bloquea cualquier otro mensaje para las ventanas creadas en el mismo subproceso.</span><span class="sxs-lookup"><span data-stu-id="15c88-138">While your window procedure executes, it blocks any other messages for windows created on the same thread.</span></span> <span data-ttu-id="15c88-139">Por lo tanto, evite un procesamiento largo dentro del procedimiento de ventana.</span><span class="sxs-lookup"><span data-stu-id="15c88-139">Therefore, avoid lengthy processing inside your window procedure.</span></span> <span data-ttu-id="15c88-140">Por ejemplo, suponga que el programa abre una conexión TCP y espera indefinidamente a que el servidor responda.</span><span class="sxs-lookup"><span data-stu-id="15c88-140">For example, suppose your program opens a TCP connection and waits indefinitely for the server to respond.</span></span> <span data-ttu-id="15c88-141">Si lo hace dentro del procedimiento de ventana, la interfaz de usuario no responderá hasta que se complete la solicitud.</span><span class="sxs-lookup"><span data-stu-id="15c88-141">If you do that inside the window procedure, your UI will not respond until the request completes.</span></span> <span data-ttu-id="15c88-142">Durante ese tiempo, la ventana no puede procesar la entrada del mouse o el teclado, volver a dibujarse a sí misma o incluso cerrarse.</span><span class="sxs-lookup"><span data-stu-id="15c88-142">During that time, the window cannot process mouse or keyboard input, repaint itself, or even close.</span></span>

<span data-ttu-id="15c88-143">En su lugar, debe mover el trabajo a otro subproceso mediante una de las funciones multitarea integradas en Windows:</span><span class="sxs-lookup"><span data-stu-id="15c88-143">Instead, you should move the work to another thread, using one of the multitasking facilities that are built into Windows:</span></span>

- <span data-ttu-id="15c88-144">Cree un subproceso.</span><span class="sxs-lookup"><span data-stu-id="15c88-144">Create a new thread.</span></span>
- <span data-ttu-id="15c88-145">Use un grupo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="15c88-145">Use a thread pool.</span></span>
- <span data-ttu-id="15c88-146">Use llamadas de E/S asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="15c88-146">Use asynchronous I/O calls.</span></span>
- <span data-ttu-id="15c88-147">Use llamadas a procedimiento asincrónico.</span><span class="sxs-lookup"><span data-stu-id="15c88-147">Use asynchronous procedure calls.</span></span>

## <a name="next"></a><span data-ttu-id="15c88-148">Siguientes</span><span class="sxs-lookup"><span data-stu-id="15c88-148">Next</span></span>

[<span data-ttu-id="15c88-149">Pintar la ventana</span><span class="sxs-lookup"><span data-stu-id="15c88-149">Painting the Window</span></span>](painting-the-window.md)
