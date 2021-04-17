---
description: En los siguientes ejemplos de código se muestra cómo realizar las siguientes tareas asociadas a mensajes de Windows y colas de mensajes.
ms.assetid: 62b4616c-37bf-4d9f-8891-7010c7035d18
title: Uso de mensajes y colas de mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a33f422a1a7c77f2c2fcd5913f931168a350a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659889"
---
# <a name="using-messages-and-message-queues"></a><span data-ttu-id="87b41-103">Uso de mensajes y colas de mensajes</span><span class="sxs-lookup"><span data-stu-id="87b41-103">Using Messages and Message Queues</span></span>

<span data-ttu-id="87b41-104">En los siguientes ejemplos de código se muestra cómo realizar las siguientes tareas asociadas a mensajes de Windows y colas de mensajes.</span><span class="sxs-lookup"><span data-stu-id="87b41-104">The following code examples demonstrate how to perform the following tasks associated with Windows messages and message queues.</span></span>

-   [<span data-ttu-id="87b41-105">Crear un bucle de mensajes</span><span class="sxs-lookup"><span data-stu-id="87b41-105">Creating a Message Loop</span></span>](#creating-a-message-loop)
-   [<span data-ttu-id="87b41-106">Examinar una cola de mensajes</span><span class="sxs-lookup"><span data-stu-id="87b41-106">Examining a Message Queue</span></span>](#examining-a-message-queue)
-   [<span data-ttu-id="87b41-107">Publicar un mensaje</span><span class="sxs-lookup"><span data-stu-id="87b41-107">Posting a Message</span></span>](#posting-a-message)
-   [<span data-ttu-id="87b41-108">Envío de un mensaje</span><span class="sxs-lookup"><span data-stu-id="87b41-108">Sending a Message</span></span>](#sending-a-message)

## <a name="creating-a-message-loop"></a><span data-ttu-id="87b41-109">Crear un bucle de mensajes</span><span class="sxs-lookup"><span data-stu-id="87b41-109">Creating a Message Loop</span></span>

<span data-ttu-id="87b41-110">El sistema no crea automáticamente una cola de mensajes para cada subproceso.</span><span class="sxs-lookup"><span data-stu-id="87b41-110">The system does not automatically create a message queue for each thread.</span></span> <span data-ttu-id="87b41-111">En su lugar, el sistema crea una cola de mensajes solo para los subprocesos que realizan operaciones que requieren una cola de mensajes.</span><span class="sxs-lookup"><span data-stu-id="87b41-111">Instead, the system creates a message queue only for threads that perform operations which require a message queue.</span></span> <span data-ttu-id="87b41-112">Si el subproceso crea una o más ventanas, se debe proporcionar un bucle de mensajes. este bucle de mensajes recupera mensajes de la cola de mensajes del subproceso y los envía a los procedimientos de ventana adecuados.</span><span class="sxs-lookup"><span data-stu-id="87b41-112">If the thread creates one or more windows, a message loop must be provided; this message loop retrieves messages from the thread's message queue and dispatches them to the appropriate window procedures.</span></span>

<span data-ttu-id="87b41-113">Dado que el sistema dirige los mensajes a ventanas individuales en una aplicación, un subproceso debe crear al menos una ventana antes de iniciar su bucle de mensajes.</span><span class="sxs-lookup"><span data-stu-id="87b41-113">Because the system directs messages to individual windows in an application, a thread must create at least one window before starting its message loop.</span></span> <span data-ttu-id="87b41-114">La mayoría de las aplicaciones contienen un único subproceso que crea ventanas.</span><span class="sxs-lookup"><span data-stu-id="87b41-114">Most applications contain a single thread that creates windows.</span></span> <span data-ttu-id="87b41-115">Una aplicación típica registra la clase de ventana para su ventana principal, crea y muestra la ventana principal y, a continuación, inicia su bucle de mensajes, todo en la función [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) .</span><span class="sxs-lookup"><span data-stu-id="87b41-115">A typical application registers the window class for its main window, creates and shows the main window, and then starts its message loop — all in the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function.</span></span>

<span data-ttu-id="87b41-116">Puede crear un bucle de mensajes mediante las funciones [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) y [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) .</span><span class="sxs-lookup"><span data-stu-id="87b41-116">You create a message loop by using the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) and [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) functions.</span></span> <span data-ttu-id="87b41-117">Si la aplicación debe obtener la entrada de caracteres del usuario, incluya la función [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) en el bucle.</span><span class="sxs-lookup"><span data-stu-id="87b41-117">If your application must obtain character input from the user, include the [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) function in the loop.</span></span> <span data-ttu-id="87b41-118">**TranslateMessage** traduce los mensajes de clave virtual en mensajes de caracteres.</span><span class="sxs-lookup"><span data-stu-id="87b41-118">**TranslateMessage** translates virtual-key messages into character messages.</span></span> <span data-ttu-id="87b41-119">En el ejemplo siguiente se muestra el bucle de mensajes en la función [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) de una aplicación sencilla basada en Windows.</span><span class="sxs-lookup"><span data-stu-id="87b41-119">The following example shows the message loop in the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function of a simple Windows-based application.</span></span>


```
HINSTANCE hinst; 
HWND hwndMain; 
 
int PASCAL WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, 
    LPSTR lpszCmdLine, int nCmdShow) 
{ 
    MSG msg;
    BOOL bRet; 
    WNDCLASS wc; 
    UNREFERENCED_PARAMETER(lpszCmdLine); 
 
    // Register the window class for the main window. 
 
    if (!hPrevInstance) 
    { 
        wc.style = 0; 
        wc.lpfnWndProc = (WNDPROC) WndProc; 
        wc.cbClsExtra = 0; 
        wc.cbWndExtra = 0; 
        wc.hInstance = hInstance; 
        wc.hIcon = LoadIcon((HINSTANCE) NULL, 
            IDI_APPLICATION); 
        wc.hCursor = LoadCursor((HINSTANCE) NULL, 
            IDC_ARROW); 
        wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
        wc.lpszMenuName =  "MainMenu"; 
        wc.lpszClassName = "MainWndClass"; 
 
        if (!RegisterClass(&wc)) 
            return FALSE; 
    } 
 
    hinst = hInstance;  // save instance handle 
 
    // Create the main window. 
 
    hwndMain = CreateWindow("MainWndClass", "Sample", 
        WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, (HWND) NULL, 
        (HMENU) NULL, hinst, (LPVOID) NULL); 
 
    // If the main window cannot be created, terminate 
    // the application. 
 
    if (!hwndMain) 
        return FALSE; 
 
    // Show the window and paint its contents. 
 
    ShowWindow(hwndMain, nCmdShow); 
    UpdateWindow(hwndMain); 
 
    // Start the message loop. 
 
    while( (bRet = GetMessage( &msg, NULL, 0, 0 )) != 0)
    { 
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        {
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        }
    } 
 
    // Return the exit code to the system. 
 
    return msg.wParam; 
} 
```



<span data-ttu-id="87b41-120">En el ejemplo siguiente se muestra un bucle de mensajes para un subproceso que usa aceleradores y muestra un cuadro de diálogo no modal.</span><span class="sxs-lookup"><span data-stu-id="87b41-120">The following example shows a message loop for a thread that uses accelerators and displays a modeless dialog box.</span></span> <span data-ttu-id="87b41-121">Cuando [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) o [**IsDialogMessage**](/windows/win32/api/winuser/nf-winuser-isdialogmessagea) devuelve **true** (lo que indica que se ha procesado el mensaje), no se llama a [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) y [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) .</span><span class="sxs-lookup"><span data-stu-id="87b41-121">When [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) or [**IsDialogMessage**](/windows/win32/api/winuser/nf-winuser-isdialogmessagea) returns **TRUE** (indicating that the message has been processed), [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) and [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) are not called.</span></span> <span data-ttu-id="87b41-122">La razón de esto es que **TranslateAccelerator** y **IsDialogMessage** realizan todas las tareas de traducción y distribución de mensajes necesarias.</span><span class="sxs-lookup"><span data-stu-id="87b41-122">The reason for this is that **TranslateAccelerator** and **IsDialogMessage** perform all necessary translating and dispatching of messages.</span></span>


```
HWND hwndMain; 
HWND hwndDlgModeless = NULL; 
MSG msg;
BOOL bRet; 
HACCEL haccel; 
// 
// Perform initialization and create a main window. 
// 
 
while( (bRet = GetMessage( &msg, NULL, 0, 0 )) != 0)
{ 
    if (bRet == -1)
    {
        // handle the error and possibly exit
    }
    else
    {
        if (hwndDlgModeless == (HWND) NULL || 
                !IsDialogMessage(hwndDlgModeless, &msg) && 
                !TranslateAccelerator(hwndMain, haccel, 
                    &msg)) 
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        }
    } 
} 
```



## <a name="examining-a-message-queue"></a><span data-ttu-id="87b41-123">Examinar una cola de mensajes</span><span class="sxs-lookup"><span data-stu-id="87b41-123">Examining a Message Queue</span></span>

<span data-ttu-id="87b41-124">En ocasiones, una aplicación necesita examinar el contenido de la cola de mensajes de un subproceso desde fuera del bucle de mensajes del subproceso.</span><span class="sxs-lookup"><span data-stu-id="87b41-124">Occasionally, an application needs to examine the contents of a thread's message queue from outside the thread's message loop.</span></span> <span data-ttu-id="87b41-125">Por ejemplo, si el procedimiento de ventana de una aplicación realiza una operación de dibujo prolongada, puede que desee que el usuario pueda interrumpir la operación.</span><span class="sxs-lookup"><span data-stu-id="87b41-125">For example, if an application's window procedure performs a lengthy drawing operation, you may want the user to be able to interrupt the operation.</span></span> <span data-ttu-id="87b41-126">A menos que la aplicación examine periódicamente la cola de mensajes durante la operación de los mensajes del mouse y del teclado, no responderá a la entrada del usuario hasta que se haya completado la operación.</span><span class="sxs-lookup"><span data-stu-id="87b41-126">Unless your application periodically examines the message queue during the operation for mouse and keyboard messages, it will not respond to user input until after the operation has completed.</span></span> <span data-ttu-id="87b41-127">La razón de esto es que la función [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) en el bucle de mensajes del subproceso no vuelve hasta que el procedimiento de ventana finaliza el procesamiento de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="87b41-127">The reason for this is that the [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) function in the thread's message loop does not return until the window procedure finishes processing a message.</span></span>

<span data-ttu-id="87b41-128">Puede usar la función [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) para examinar una cola de mensajes durante una operación larga.</span><span class="sxs-lookup"><span data-stu-id="87b41-128">You can use the [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) function to examine a message queue during a lengthy operation.</span></span> <span data-ttu-id="87b41-129">**PeekMessage** es similar a la función [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ; ambos comprueban una cola de mensajes para un mensaje que coincide con los criterios de filtro y, a continuación, copia el mensaje en una estructura [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) .</span><span class="sxs-lookup"><span data-stu-id="87b41-129">**PeekMessage** is similar to the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) function; both check a message queue for a message that matches the filter criteria and then copy the message to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure.</span></span> <span data-ttu-id="87b41-130">La principal diferencia entre las dos funciones es que **GetMessage** no vuelve hasta que un mensaje que coincide con los criterios de filtro se coloca en la cola, mientras que **PeekMessage** vuelve inmediatamente, independientemente de si un mensaje está en la cola.</span><span class="sxs-lookup"><span data-stu-id="87b41-130">The main difference between the two functions is that **GetMessage** does not return until a message matching the filter criteria is placed in the queue, whereas **PeekMessage** returns immediately regardless of whether a message is in the queue.</span></span>

<span data-ttu-id="87b41-131">En el ejemplo siguiente se muestra cómo usar [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) para examinar una cola de mensajes para los clics del mouse y la entrada del teclado durante una operación larga.</span><span class="sxs-lookup"><span data-stu-id="87b41-131">The following example shows how to use [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) to examine a message queue for mouse clicks and keyboard input during a lengthy operation.</span></span>


```
HWND hwnd; 
BOOL fDone; 
MSG msg; 
 
// Begin the operation and continue until it is complete 
// or until the user clicks the mouse or presses a key. 
 
fDone = FALSE; 
while (!fDone) 
{ 
    fDone = DoLengthyOperation(); // application-defined function 
 
    // Remove any messages that may be in the queue. If the 
    // queue contains any mouse or keyboard 
    // messages, end the operation. 
 
    while (PeekMessage(&msg, hwnd,  0, 0, PM_REMOVE)) 
    { 
        switch(msg.message) 
        { 
            case WM_LBUTTONDOWN: 
            case WM_RBUTTONDOWN: 
            case WM_KEYDOWN: 
                // 
                // Perform any required cleanup. 
                // 
                fDone = TRUE; 
        } 
    } 
} 
```



<span data-ttu-id="87b41-132">Otras funciones, como [**GetQueueStatus**](/windows/win32/api/winuser/nf-winuser-getqueuestatus) y [**GetInputState**](/windows/win32/api/winuser/nf-winuser-getinputstate), también permiten examinar el contenido de la cola de mensajes de un subproceso.</span><span class="sxs-lookup"><span data-stu-id="87b41-132">Other functions, including [**GetQueueStatus**](/windows/win32/api/winuser/nf-winuser-getqueuestatus) and [**GetInputState**](/windows/win32/api/winuser/nf-winuser-getinputstate), also allow you to examine the contents of a thread's message queue.</span></span> <span data-ttu-id="87b41-133">**GetQueueStatus** devuelve una matriz de marcas que indica los tipos de mensajes de la cola; el uso de esta es la manera más rápida de detectar si la cola contiene algún mensaje.</span><span class="sxs-lookup"><span data-stu-id="87b41-133">**GetQueueStatus** returns an array of flags that indicates the types of messages in the queue; using it is the fastest way to discover whether the queue contains any messages.</span></span> <span data-ttu-id="87b41-134">**GetInputState** devuelve **true** si la cola contiene mensajes del mouse o del teclado.</span><span class="sxs-lookup"><span data-stu-id="87b41-134">**GetInputState** returns **TRUE** if the queue contains mouse or keyboard messages.</span></span> <span data-ttu-id="87b41-135">Ambas funciones se pueden usar para determinar si la cola contiene mensajes que deben procesarse.</span><span class="sxs-lookup"><span data-stu-id="87b41-135">Both of these functions can be used to determine whether the queue contains messages that need to be processed.</span></span>

## <a name="posting-a-message"></a><span data-ttu-id="87b41-136">Publicar un mensaje</span><span class="sxs-lookup"><span data-stu-id="87b41-136">Posting a Message</span></span>

<span data-ttu-id="87b41-137">Puede publicar un mensaje en una cola de mensajes mediante la función [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) .</span><span class="sxs-lookup"><span data-stu-id="87b41-137">You can post a message to a message queue by using the [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) function.</span></span> <span data-ttu-id="87b41-138">**PostMessage** coloca un mensaje al final de la cola de mensajes de un subproceso y vuelve inmediatamente, sin esperar a que el subproceso procese el mensaje.</span><span class="sxs-lookup"><span data-stu-id="87b41-138">**PostMessage** places a message at the end of a thread's message queue and returns immediately, without waiting for the thread to process the message.</span></span> <span data-ttu-id="87b41-139">Los parámetros de la función incluyen un identificador de ventana, un identificador de mensaje y dos parámetros de mensaje.</span><span class="sxs-lookup"><span data-stu-id="87b41-139">The function's parameters include a window handle, a message identifier, and two message parameters.</span></span> <span data-ttu-id="87b41-140">El sistema copia estos parámetros en una estructura [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) , rellena los miembros **Time** y **PT** de la estructura y coloca la estructura en la cola de mensajes.</span><span class="sxs-lookup"><span data-stu-id="87b41-140">The system copies these parameters to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure, fills the **time** and **pt** members of the structure, and places the structure in the message queue.</span></span>

<span data-ttu-id="87b41-141">El sistema utiliza el identificador de ventana que se pasa con la función [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) para determinar qué cola de mensajes de subprocesos debe recibir el mensaje.</span><span class="sxs-lookup"><span data-stu-id="87b41-141">The system uses the window handle passed with the [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) function to determine which thread message queue should receive the message.</span></span> <span data-ttu-id="87b41-142">Si el identificador es **hWnd \_ más** alto, el sistema envía el mensaje a las colas de mensajes de subproceso de todas las ventanas de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="87b41-142">If the handle is **HWND\_TOPMOST**, the system posts the message to the thread message queues of all top-level windows.</span></span>

<span data-ttu-id="87b41-143">Puede usar la función [**PostThreadMessage**](/windows/win32/api/winuser/nf-winuser-postthreadmessagea) para publicar un mensaje en una cola de mensajes de subproceso específica.</span><span class="sxs-lookup"><span data-stu-id="87b41-143">You can use the [**PostThreadMessage**](/windows/win32/api/winuser/nf-winuser-postthreadmessagea) function to post a message to a specific thread message queue.</span></span> <span data-ttu-id="87b41-144">**PostThreadMessage** es similar a [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea), excepto que el primer parámetro es un identificador de subproceso en lugar de un identificador de ventana.</span><span class="sxs-lookup"><span data-stu-id="87b41-144">**PostThreadMessage** is similar to [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea), except the first parameter is a thread identifier rather than a window handle.</span></span> <span data-ttu-id="87b41-145">Puede recuperar el identificador del subproceso llamando a la función [**GetCurrentThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) .</span><span class="sxs-lookup"><span data-stu-id="87b41-145">You can retrieve the thread identifier by calling the [**GetCurrentThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) function.</span></span>

<span data-ttu-id="87b41-146">Utilice la función [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) para salir de un bucle de mensajes.</span><span class="sxs-lookup"><span data-stu-id="87b41-146">Use the [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function to exit a message loop.</span></span> <span data-ttu-id="87b41-147">**PostQuitMessage** envía el mensaje de [**\_ salida de WM**](wm-quit.md) al subproceso que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="87b41-147">**PostQuitMessage** posts the [**WM\_QUIT**](wm-quit.md) message to the currently executing thread.</span></span> <span data-ttu-id="87b41-148">El bucle de mensajes del subproceso finaliza y devuelve el control al sistema cuando encuentra el mensaje de **\_ salida de WM** .</span><span class="sxs-lookup"><span data-stu-id="87b41-148">The thread's message loop terminates and returns control to the system when it encounters the **WM\_QUIT** message.</span></span> <span data-ttu-id="87b41-149">Una aplicación normalmente llama a **PostQuitMessage** en respuesta al mensaje de [**\_ destrucción de WM**](wm-destroy.md) , tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="87b41-149">An application usually calls **PostQuitMessage** in response to the [**WM\_DESTROY**](wm-destroy.md) message, as shown in the following example.</span></span>


```
case WM_DESTROY: 
 
    // Perform cleanup tasks. 
 
    PostQuitMessage(0); 
    break; 
```



## <a name="sending-a-message"></a><span data-ttu-id="87b41-150">Envío de un mensaje</span><span class="sxs-lookup"><span data-stu-id="87b41-150">Sending a Message</span></span>

<span data-ttu-id="87b41-151">La función [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) se utiliza para enviar un mensaje directamente a un procedimiento de ventana.</span><span class="sxs-lookup"><span data-stu-id="87b41-151">The [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function is used to send a message directly to a window procedure.</span></span> <span data-ttu-id="87b41-152">**SendMessage** llama a un procedimiento de ventana y espera a que ese procedimiento procese el mensaje y devuelve un resultado.</span><span class="sxs-lookup"><span data-stu-id="87b41-152">**SendMessage** calls a window procedure and waits for that procedure to process the message and return a result.</span></span>

<span data-ttu-id="87b41-153">Se puede enviar un mensaje a cualquier ventana del sistema; lo único que se necesita es un identificador de ventana.</span><span class="sxs-lookup"><span data-stu-id="87b41-153">A message can be sent to any window in the system; all that is required is a window handle.</span></span> <span data-ttu-id="87b41-154">El sistema utiliza el identificador para determinar qué procedimiento de ventana debe recibir el mensaje.</span><span class="sxs-lookup"><span data-stu-id="87b41-154">The system uses the handle to determine which window procedure should receive the message.</span></span>

<span data-ttu-id="87b41-155">Antes de procesar un mensaje que puede haberse enviado desde otro subproceso, un procedimiento de ventana debe llamar primero a la función [**InSendMessage**](/windows/win32/api/winuser/nf-winuser-insendmessage) .</span><span class="sxs-lookup"><span data-stu-id="87b41-155">Before processing a message that may have been sent from another thread, a window procedure should first call the [**InSendMessage**](/windows/win32/api/winuser/nf-winuser-insendmessage) function.</span></span> <span data-ttu-id="87b41-156">Si esta función devuelve **true**, el procedimiento de ventana debe llamar a [**ReplyMessage**](/windows/win32/api/winuser/nf-winuser-replymessage) antes que cualquier función que haga que el subproceso entregue el control, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="87b41-156">If this function returns **TRUE**, the window procedure should call [**ReplyMessage**](/windows/win32/api/winuser/nf-winuser-replymessage) before any function that causes the thread to yield control, as shown in the following example.</span></span>


```
case WM_USER + 5: 
    if (InSendMessage()) 
        ReplyMessage(TRUE); 
 
    DialogBox(hInst, "MyDialogBox", hwndMain, (DLGPROC) MyDlgProc); 
    break; 
```



<span data-ttu-id="87b41-157">Se pueden enviar varios mensajes a los controles de un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="87b41-157">A number of messages can be sent to controls in a dialog box.</span></span> <span data-ttu-id="87b41-158">Estos mensajes de control establecen el aspecto, el comportamiento y el contenido de los controles o recuperan información sobre los controles.</span><span class="sxs-lookup"><span data-stu-id="87b41-158">These control messages set the appearance, behavior, and content of controls or retrieve information about controls.</span></span> <span data-ttu-id="87b41-159">Por ejemplo, el mensaje [**CB \_ ADDSTRING**](../controls/cb-addstring.md) puede Agregar una cadena a un cuadro combinado y el mensaje [**BM \_ SETCHECK**](../controls/bm-setcheck.md) puede establecer el estado de activación de una casilla o un botón de radio.</span><span class="sxs-lookup"><span data-stu-id="87b41-159">For example, the [**CB\_ADDSTRING**](../controls/cb-addstring.md) message can add a string to a combo box, and the [**BM\_SETCHECK**](../controls/bm-setcheck.md) message can set the check state of a check box or radio button.</span></span>

<span data-ttu-id="87b41-160">Utilice la función [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea) para enviar un mensaje a un control, especificando el identificador del control y el identificador de la ventana del cuadro de diálogo que contiene el control.</span><span class="sxs-lookup"><span data-stu-id="87b41-160">Use the [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea) function to send a message to a control, specifying the identifier of the control and the handle of the dialog box window that contains the control.</span></span> <span data-ttu-id="87b41-161">En el ejemplo siguiente, tomado de un procedimiento de cuadro de diálogo, se copia una cadena del control de edición de un cuadro combinado en el cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="87b41-161">The following example, taken from a dialog box procedure, copies a string from a combo box's edit control into its list box.</span></span> <span data-ttu-id="87b41-162">En el ejemplo se usa **SendDlgItemMessage** para enviar un mensaje [**CB \_ ADDSTRING**](../controls/cb-addstring.md) al cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="87b41-162">The example uses **SendDlgItemMessage** to send a [**CB\_ADDSTRING**](../controls/cb-addstring.md) message to the combo box.</span></span>


```
HWND hwndCombo; 
int cTxtLen; 
PSTR pszMem; 
 
switch (uMsg) 
{ 
    case WM_COMMAND: 
        switch (LOWORD(wParam)) 
        { 
            case IDD_ADDCBITEM: 
                // Get the handle of the combo box and the 
                // length of the string in the edit control 
                // of the combo box. 
 
                hwndCombo = GetDlgItem(hwndDlg, IDD_COMBO); 
                cTxtLen = GetWindowTextLength(hwndCombo); 
 
                // Allocate memory for the string and copy 
                // the string into the memory. 
 
                pszMem = (PSTR) VirtualAlloc((LPVOID) NULL, 
                    (DWORD) (cTxtLen + 1), MEM_COMMIT, 
                    PAGE_READWRITE); 
                GetWindowText(hwndCombo, pszMem, 
                    cTxtLen + 1); 
 
                // Add the string to the list box of the 
                // combo box and remove the string from the 
                // edit control of the combo box. 
 
                if (pszMem != NULL) 
                { 
                    SendDlgItemMessage(hwndDlg, IDD_COMBO, 
                        CB_ADDSTRING, 0, 
                        (DWORD) ((LPSTR) pszMem)); 
                    SetWindowText(hwndCombo, (LPSTR) NULL); 
                } 
 
                // Free the memory and return. 
 
                VirtualFree(pszMem, 0, MEM_RELEASE); 
                return TRUE; 
            // 
            // Process other dialog box commands. 
            // 
 
        } 
    // 
    // Process other dialog box messages. 
    // 
 
}
```



 

 
