---
description: Una clase de ventana es compatible con un procedimiento de ventana. La aplicación puede registrar una clase de ventana mediante RegisterClassA o RegisterClassW. Las aplicaciones nuevas normalmente deben usar RegisterClassW.
ms.assetid: 016296ce-6151-4673-ad59-c69a2138a05a
title: Registrar clases de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57c82e9daead566e5bcb5419fccc234014005f6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156888"
---
# <a name="registering-window-classes"></a>Registrar clases de ventana

Una clase de ventana es compatible con un procedimiento de ventana. La aplicación puede registrar una clase de ventana mediante [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa) o [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa). Las aplicaciones nuevas normalmente deben usar **RegisterClassW**.

Si la aplicación registra la clase de ventana mediante [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa), la función informa al sistema operativo de que las ventanas de la clase creada esperan mensajes con texto o parámetros de carácter para usar un juego de caracteres de [Página de códigos de Windows (ANSI)](code-pages.md) . El registro mediante [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) permite a la aplicación solicitar al sistema operativo que pase los parámetros de texto de los mensajes como [Unicode](unicode.md). La función [**IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode) permite a una aplicación consultar la naturaleza de cada ventana.

En el ejemplo siguiente se muestra cómo registrar una clase de ventana de página de códigos de Windows y una clase de ventana Unicode y cómo escribir los procedimientos de ventana para ambos casos. Para los fines de este ejemplo, todas las funciones y estructuras se muestran con los tipos de datos "A" (ANSI) o "W" (ancho, Unicode) específicos. Con las técnicas explicadas en el [uso de tipos de datos genéricos](using-generic-data-types.md), puede escribir este ejemplo de forma alternativa para usar tipos de datos genéricos, de modo que se pueda compilar para usar páginas de códigos de Windows o Unicode, dependiendo de si se define "Unicode".


```C++
// Register a Windows code page window class.

WNDCLASSA AnsiWndCls;

AnsiWndCls.style         = CS_DBLCLKS | CS_PARENTDC;
AnsiWndCls.lpfnWndProc   = (WNDPROC)AnsiWndProc;
AnsiWndCls.cbClsExtra    = 0;
AnsiWndCls.cbWndExtra    = 0;
AnsiWndCls.hInstance     = hInstance;
AnsiWndCls.hIcon         = NULL;
AnsiWndCls.hCursor       = LoadCursor(NULL, (LPTSTR)IDC_IBEAM);
AnsiWndCls.hbrBackground = NULL;
AnsiWndCls.lpszMenuName  = NULL;
AnsiWndCls.lpszClassName = "TestAnsi";

RegisterClassA(&AnsiWndCls);

// Register a Unicode window class.

WNDCLASSW UnicodeWndCls;

UnicodeWndCls.style         = CS_DBLCLKS | CS_PARENTDC;
UnicodeWndCls.lpfnWndProc   = (WNDPROC)UniWndProc;
UnicodeWndCls.cbClsExtra    = 0;
UnicodeWndCls.cbWndExtra    = 0;
UnicodeWndCls.hInstance     = hInstance;
UnicodeWndCls.hIcon         = NULL;
UnicodeWndCls.hCursor       = LoadCursor(NULL,(LPTSTR)IDC_IBEAM);
UnicodeWndCls.hbrBackground = NULL;
UnicodeWndCls.lpszMenuName  = NULL;
UnicodeWndCls.lpszClassName = L"TestUnicode";

RegisterClassW(&UnicodeWndCls);
```



En el ejemplo siguiente se muestra la diferencia entre [**controlar \_ el mensaje de tipo de salida**](../inputdev/wm-char.md) en un procedimiento de ventana de página de códigos de Windows y un procedimiento de ventana Unicode.


```C++
// "ANSI" Window Procedure

LRESULT CALLBACK AnsiWndProc(HWND hWnd, UINT message,
                             WPARAM wParam, LPARAM lParam)
{

    // Dispatch the messages that can be received.

    switch (message)
    {
        case WM_CHAR:

            // wParam - the value of the key
            // lParam - (not used in this example)

            if (lstrcmpA("Q", (LPCSTR) wParam))
            {
                // ...
            }
            else
            {
                // ...
            }
            break;
        // Process other messages.
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}

// Unicode Window Procedure

LRESULT CALLBACK UniWndProc(HWND hWnd, UINT message,
                            WPARAM wParam, LPARAM lParam)
{

    // Dispatch the messages that can be received.

    switch (message)
    {
        case WM_CHAR:

            // wParam - the value of the key
            // lParam - (not used in this example)

            if (lstrcmpW(L"Q", (LPCWSTR) wParam))
            {
                // ...
            }
            else
            {
                // ...
            }
            break;
        // Process other messages.
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



Todo el texto de los mensajes recibidos por **AnsiWndProc** se compone de caracteres de página de códigos de Windows. Todo el texto de los mensajes recibidos por **UniWndProc** se compone de caracteres Unicode.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar Unicode y juegos de caracteres](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
