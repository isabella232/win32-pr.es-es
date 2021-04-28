---
title: Módulo 1. Su primer programa de Windows
description: Módulo 1. Su primer programa de Windows
ms.assetid: 73848144-bf02-4382-a476-7f5a35447727
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6515b012f968707379ebf24023c3d282c50d6fd6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110953"
---
# <a name="module-1-your-first-windows-program"></a><span data-ttu-id="68553-105">Módulo 1.</span><span class="sxs-lookup"><span data-stu-id="68553-105">Module 1.</span></span> <span data-ttu-id="68553-106">Su primer programa de Windows</span><span class="sxs-lookup"><span data-stu-id="68553-106">Your First Windows Program</span></span>

<span data-ttu-id="68553-107">En este módulo, escribiremos un programa de escritorio mínimo de Windows.</span><span class="sxs-lookup"><span data-stu-id="68553-107">In this module, we will write a minimal Windows desktop program.</span></span> <span data-ttu-id="68553-108">Todo lo que hace es crear y mostrar una ventana en blanco.</span><span class="sxs-lookup"><span data-stu-id="68553-108">All it does is create and show a blank window.</span></span> <span data-ttu-id="68553-109">Este primer programa contiene unas 50 líneas de código, sin contar las líneas en blanco y los comentarios.</span><span class="sxs-lookup"><span data-stu-id="68553-109">This first program contains about 50 lines of code, not counting blank lines and comments.</span></span> <span data-ttu-id="68553-110">Será nuestro punto de partida; más adelante agregaremos gráficos, texto, datos de entrada del usuario y otras características.</span><span class="sxs-lookup"><span data-stu-id="68553-110">It will be our starting point; later we'll add graphics, text, user input, and other features.</span></span>

<span data-ttu-id="68553-111">Si busca más detalles sobre cómo crear una aplicación de escritorio de Windows tradicional en Visual Studio, consulte Tutorial: Crear una aplicación de escritorio de [Windows tradicional (C++).](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019)</span><span class="sxs-lookup"><span data-stu-id="68553-111">If you are looking for more details on how to create a traditional Windows desktop application in Visual Studio, check out  [Walkthrough: Create a traditional Windows Desktop application (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019).</span></span>

![captura de pantalla del programa de ejemplo](images/window01.png)

<span data-ttu-id="68553-113">Este es el código completo del programa:</span><span class="sxs-lookup"><span data-stu-id="68553-113">Here is the complete code for the program:</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif 

#include <windows.h>

LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam);

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, PWSTR pCmdLine, int nCmdShow)
{
    // Register the window class.
    const wchar_t CLASS_NAME[]  = L"Sample Window Class";
    
    WNDCLASS wc = { };

    wc.lpfnWndProc   = WindowProc;
    wc.hInstance     = hInstance;
    wc.lpszClassName = CLASS_NAME;

    RegisterClass(&wc);

    // Create the window.

    HWND hwnd = CreateWindowEx(
        0,                              // Optional window styles.
        CLASS_NAME,                     // Window class
        L"Learn to Program Windows",    // Window text
        WS_OVERLAPPEDWINDOW,            // Window style

        // Size and position
        CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT,

        NULL,       // Parent window    
        NULL,       // Menu
        hInstance,  // Instance handle
        NULL        // Additional application data
        );

    if (hwnd == NULL)
    {
        return 0;
    }

    ShowWindow(hwnd, nCmdShow);

    // Run the message loop.

    MSG msg = { };
    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }

    return 0;
}

LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_DESTROY:
        PostQuitMessage(0);
        return 0;

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            HDC hdc = BeginPaint(hwnd, &ps);



            FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));

            EndPaint(hwnd, &ps);
        }
        return 0;

    }
    return DefWindowProc(hwnd, uMsg, wParam, lParam);
}
```





<span data-ttu-id="68553-114">Puede descargar el proyecto de Visual Studio completo desde [Windows Hello World Sample](windows-hello-world-sample.md).</span><span class="sxs-lookup"><span data-stu-id="68553-114">You can download the complete Visual Studio project from [Windows Hello World Sample](windows-hello-world-sample.md).</span></span>

<span data-ttu-id="68553-115">Puede ser útil proporcionar un breve esquema de lo que hace este código.</span><span class="sxs-lookup"><span data-stu-id="68553-115">It may be useful to give a brief outline of what this code does.</span></span> <span data-ttu-id="68553-116">Los temas posteriores examinarán el código en detalle.</span><span class="sxs-lookup"><span data-stu-id="68553-116">Later topics will examine the code in detail.</span></span>

1.  <span data-ttu-id="68553-117">**wWinMain es** el punto de entrada del programa.</span><span class="sxs-lookup"><span data-stu-id="68553-117">**wWinMain** is the program entry point.</span></span> <span data-ttu-id="68553-118">Cuando se inicia el programa, registra información sobre el comportamiento de la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="68553-118">When the program starts, it registers some information about the behavior of the application window.</span></span> <span data-ttu-id="68553-119">Uno de los elementos más importantes es la dirección de una función, denominada `WindowProc` en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="68553-119">One of the most important items is the address of a function, named `WindowProc` in this example.</span></span> <span data-ttu-id="68553-120">Esta función define el comportamiento de la ventana: su apariencia, cómo interactúa con el usuario, etc.</span><span class="sxs-lookup"><span data-stu-id="68553-120">This function defines the behavior of the window—its appearance, how it interacts with the user, and so forth.</span></span>
2.  <span data-ttu-id="68553-121">A continuación, el programa crea la ventana y recibe un identificador que identifica de forma única la ventana.</span><span class="sxs-lookup"><span data-stu-id="68553-121">Next, the program creates the window and receives a handle that uniquely identifies the window.</span></span>
3.  <span data-ttu-id="68553-122">Si la ventana se crea correctamente, el programa entra en un **bucle while.**</span><span class="sxs-lookup"><span data-stu-id="68553-122">If the window is created successfully, the program enters a **while** loop.</span></span> <span data-ttu-id="68553-123">El programa permanece en este bucle hasta que el usuario cierra la ventana y sale de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="68553-123">The program remains in this loop until the user closes the window and exits the application.</span></span>

<span data-ttu-id="68553-124">Observe que el programa no llama explícitamente a la función, aunque se haya dicho que aquí es donde se define la mayor parte de `WindowProc` la lógica de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="68553-124">Notice that the program does not explicitly call the `WindowProc` function, even though we said this is where most of the application logic is defined.</span></span> <span data-ttu-id="68553-125">Windows se comunica con el programa al pasarle una serie de *mensajes*.</span><span class="sxs-lookup"><span data-stu-id="68553-125">Windows communicates with your program by passing it a series of *messages*.</span></span> <span data-ttu-id="68553-126">El código dentro del **bucle while** impulsa este proceso.</span><span class="sxs-lookup"><span data-stu-id="68553-126">The code inside the **while** loop drives this process.</span></span> <span data-ttu-id="68553-127">Cada vez que el programa llama a [**la función DispatchMessage,**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) hace que Windows invoque indirectamente la función WindowProc, una vez para cada mensaje.</span><span class="sxs-lookup"><span data-stu-id="68553-127">Each time the program calls the [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) function, it indirectly causes Windows to invoke the WindowProc function, once for each message.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="68553-128">En esta sección</span><span class="sxs-lookup"><span data-stu-id="68553-128">In this section</span></span>

-   [<span data-ttu-id="68553-129">Crear una ventana</span><span class="sxs-lookup"><span data-stu-id="68553-129">Creating a Window</span></span>](creating-a-window.md)
-   [<span data-ttu-id="68553-130">Mensajes de ventana</span><span class="sxs-lookup"><span data-stu-id="68553-130">Window Messages</span></span>](window-messages.md)
-   [<span data-ttu-id="68553-131">Escribir el procedimiento de ventana</span><span class="sxs-lookup"><span data-stu-id="68553-131">Writing the Window Procedure</span></span>](writing-the-window-procedure.md)
-   [<span data-ttu-id="68553-132">Pintar la ventana</span><span class="sxs-lookup"><span data-stu-id="68553-132">Painting the Window</span></span>](painting-the-window.md)
-   [<span data-ttu-id="68553-133">Cerrar la ventana</span><span class="sxs-lookup"><span data-stu-id="68553-133">Closing the Window</span></span>](closing-the-window.md)
-   [<span data-ttu-id="68553-134">Administración del estado de la aplicación</span><span class="sxs-lookup"><span data-stu-id="68553-134">Managing Application State</span></span>](managing-application-state-.md)

## <a name="related-topics"></a><span data-ttu-id="68553-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="68553-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68553-136">Aprender a programar para Windows en C++</span><span class="sxs-lookup"><span data-stu-id="68553-136">Learn to Program for Windows in C++</span></span>](learn-to-program-for-windows.md)
</dt> <dt>

[<span data-ttu-id="68553-137">Windows Hello World Sample</span><span class="sxs-lookup"><span data-stu-id="68553-137">Windows Hello World Sample</span></span>](windows-hello-world-sample.md)
</dt> </dl>

 

 
