---
title: Módulo 1. Su primer programa de Windows
description: .
ms.assetid: 73848144-bf02-4382-a476-7f5a35447727
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27749cddabaefb4fd83b836887fbb2dac017d238
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/09/2021
ms.locfileid: "104566209"
---
# <a name="module-1-your-first-windows-program"></a>Módulo 1. Su primer programa de Windows

En este módulo, se escribirá un programa de escritorio de Windows mínimo. Lo único que hace es crear y mostrar una ventana en blanco. Este primer programa contiene aproximadamente 50 líneas de código, sin contar los comentarios y las líneas en blanco. Será nuestro punto de partida; más adelante agregaremos gráficos, texto, entrada de usuario y otras características.

Si busca más detalles sobre cómo crear una aplicación de escritorio tradicional de Windows en Visual Studio, consulte  [Tutorial: crear una aplicación de escritorio tradicional de Windows (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019).

![captura de pantalla del programa de ejemplo](images/window01.png)

Este es el código completo para el programa:


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





Puede descargar el proyecto completo de Visual Studio desde el [ejemplo de Windows Hola mundo](windows-hello-world-sample.md).

Puede ser útil proporcionar una breve descripción de lo que hace este código. En los temas posteriores se examinará el código en detalle.

1.  **wWinMain** es el punto de entrada del programa. Cuando el programa se inicia, registra información sobre el comportamiento de la ventana de la aplicación. Uno de los elementos más importantes es la dirección de una función, denominada `WindowProc` en este ejemplo. Esta función define el comportamiento de la ventana (su apariencia, cómo interactúa con el usuario, etc.).
2.  A continuación, el programa crea la ventana y recibe un identificador que identifica de forma única la ventana.
3.  Si la ventana se crea correctamente, el programa entra en un bucle **While** . El programa permanece en este bucle hasta que el usuario cierra la ventana y sale de la aplicación.

Tenga en cuenta que el programa no llama explícitamente a la `WindowProc` función, aunque dijimos esto es donde se define la mayoría de la lógica de la aplicación. Windows se comunica con el programa pasándole una serie de *mensajes*. El código dentro del bucle **While** impulsa este proceso. Cada vez que el programa llama a la función [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) , provoca indirectamente que Windows invoque la función WindowProc, una vez para cada mensaje.

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

[Ejemplo de Hola mundo de Windows](windows-hello-world-sample.md)
</dt> </dl>

 

 
