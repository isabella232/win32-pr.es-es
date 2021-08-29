---
title: Módulo 1. Su primer Windows programa
description: Módulo 1. Su primer Windows programa
ms.assetid: 73848144-bf02-4382-a476-7f5a35447727
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1e09b4caf81f3498a5c36eaaf0dbc3a95f52f7dd2ba8c64d0f0f9b53d19fe2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086445"
---
# <a name="module-1-your-first-windows-program"></a>Módulo 1. Su primer Windows programa

En este módulo, escribiremos un programa de escritorio Windows mínimo. Lo único que hace es crear y mostrar una ventana en blanco. Este primer programa contiene unas 50 líneas de código, sin contar las líneas en blanco y los comentarios. Será nuestro punto de partida; Más adelante agregaremos gráficos, texto, datos de entrada del usuario y otras características.

Si busca más detalles sobre cómo crear una aplicación de escritorio Windows tradicional en Visual Studio, consulte Tutorial: Crear una aplicación de escritorio de Windows [tradicional (C++).](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019)

![captura de pantalla del programa de ejemplo](images/window01.png)

Este es el código completo del programa:


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





Puede descargar el proyecto de Visual Studio completo desde [Windows Hello World Sample](windows-hello-world-sample.md).

Puede ser útil proporcionar un breve esquema de lo que hace este código. Los temas posteriores examinarán el código en detalle.

1.  **wWinMain es** el punto de entrada del programa. Cuando se inicia el programa, registra cierta información sobre el comportamiento de la ventana de la aplicación. Uno de los elementos más importantes es la dirección de una función, denominada `WindowProc` en este ejemplo. Esta función define el comportamiento de la ventana: su apariencia, cómo interactúa con el usuario, etc.
2.  A continuación, el programa crea la ventana y recibe un identificador que identifica de forma única la ventana.
3.  Si la ventana se crea correctamente, el programa entra en un **bucle while.** El programa permanece en este bucle hasta que el usuario cierra la ventana y sale de la aplicación.

Observe que el programa no llama explícitamente a la función, aunque se haya dicho que aquí es donde se define la mayor parte de `WindowProc` la lógica de la aplicación. Windows se comunica con el programa pasando una serie de *mensajes*. El código dentro del **bucle while** impulsa este proceso. Cada vez que el programa llama a la función [**DispatchMessage,**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) hace que Windows invoque la función WindowProc, una vez para cada mensaje.

## <a name="in-this-section"></a>En esta sección

-   [Crear una ventana](creating-a-window.md)
-   [Mensajes de ventana](window-messages.md)
-   [Escribir el procedimiento de ventana](writing-the-window-procedure.md)
-   [Pintar la ventana](painting-the-window.md)
-   [Cerrar la ventana](closing-the-window.md)
-   [Administración del estado de la aplicación](managing-application-state-.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aprender a programar para Windows en C++](learn-to-program-for-windows.md)
</dt> <dt>

[Windows Hello Ejemplo mundial](windows-hello-world-sample.md)
</dt> </dl>

 

 
