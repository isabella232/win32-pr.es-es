---
description: Un procedimiento de ventana admite una clase de ventana. La aplicación puede registrar una clase de ventana mediante RegisterClassA o RegisterClassW. Las nuevas aplicaciones normalmente deben usar RegisterClassW.
ms.assetid: 016296ce-6151-4673-ad59-c69a2138a05a
title: Registrar clases de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f508ebdbfa35f2551d723b3ef9a1ffd807917dfe71e503f9d77b2e8fdb136f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040455"
---
# <a name="registering-window-classes"></a>Registrar clases de ventana

Un procedimiento de ventana admite una clase de ventana. La aplicación puede registrar una clase de ventana mediante [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa) o [**RegisterClassW.**](/windows/win32/api/winuser/nf-winuser-registerclassa) Las nuevas aplicaciones normalmente deben **usar RegisterClassW.**

Si la aplicación registra la clase de ventana mediante [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa), la función informa al sistema operativo de que las ventanas de la clase creada esperan que los mensajes con parámetros de texto o caracteres usen un juego de caracteres de página de códigos [Windows (ANSI).](code-pages.md) El registro [**mediante RegisterClassW permite**](/windows/win32/api/winuser/nf-winuser-registerclassa) a la aplicación solicitar al sistema operativo que pase parámetros de texto de mensajes como [Unicode.](unicode.md) La [**función IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode) permite a una aplicación consultar la naturaleza de cada ventana.

En el ejemplo siguiente se muestra cómo registrar una clase Windows ventana de página de códigos y una clase de ventana Unicode y cómo escribir los procedimientos de ventana para ambos casos. Para los fines de este ejemplo, todas las funciones y estructuras se muestran con los tipos de datos específicos "A" (ANSI) o "W" (ancho, Unicode). Con las técnicas [](using-generic-data-types.md)que se explican en Uso de tipos de datos genéricos, también puede escribir este ejemplo para usar tipos de datos genéricos, de modo que se pueda compilar para usar páginas de códigos Windows o Unicode, dependiendo de si se define "UNICODE".


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



En el ejemplo siguiente se muestra la diferencia entre controlar el mensaje [**\_ WM CHAR**](../inputdev/wm-char.md) en un procedimiento Windows ventana de página de códigos y un procedimiento de ventana Unicode.


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



Todo el texto de los mensajes recibidos **por AnsiWndProc** se compone de Windows de página de códigos. Todo el texto de los mensajes recibidos **por UniWndProc** se compone de caracteres Unicode.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Unicode y juegos de caracteres](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
