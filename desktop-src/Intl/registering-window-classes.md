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
# <a name="registering-window-classes"></a><span data-ttu-id="8d446-105">Registrar clases de ventana</span><span class="sxs-lookup"><span data-stu-id="8d446-105">Registering Window Classes</span></span>

<span data-ttu-id="8d446-106">Una clase de ventana es compatible con un procedimiento de ventana.</span><span class="sxs-lookup"><span data-stu-id="8d446-106">A window class is supported by a window procedure.</span></span> <span data-ttu-id="8d446-107">La aplicación puede registrar una clase de ventana mediante [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa) o [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa).</span><span class="sxs-lookup"><span data-stu-id="8d446-107">Your application can register a window class by using either [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa) or [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa).</span></span> <span data-ttu-id="8d446-108">Las aplicaciones nuevas normalmente deben usar **RegisterClassW**.</span><span class="sxs-lookup"><span data-stu-id="8d446-108">New applications should typically use **RegisterClassW**.</span></span>

<span data-ttu-id="8d446-109">Si la aplicación registra la clase de ventana mediante [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa), la función informa al sistema operativo de que las ventanas de la clase creada esperan mensajes con texto o parámetros de carácter para usar un juego de caracteres de [Página de códigos de Windows (ANSI)](code-pages.md) .</span><span class="sxs-lookup"><span data-stu-id="8d446-109">If the application registers the window class using [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa), the function informs the operating system that the windows of the created class expect messages with text or character parameters to use a [Windows (ANSI) code page](code-pages.md) character set.</span></span> <span data-ttu-id="8d446-110">El registro mediante [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) permite a la aplicación solicitar al sistema operativo que pase los parámetros de texto de los mensajes como [Unicode](unicode.md).</span><span class="sxs-lookup"><span data-stu-id="8d446-110">Registration using [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) allows the application to request the operating system to pass text parameters of messages as [Unicode](unicode.md).</span></span> <span data-ttu-id="8d446-111">La función [**IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode) permite a una aplicación consultar la naturaleza de cada ventana.</span><span class="sxs-lookup"><span data-stu-id="8d446-111">The [**IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode) function enables an application to query the nature of each window.</span></span>

<span data-ttu-id="8d446-112">En el ejemplo siguiente se muestra cómo registrar una clase de ventana de página de códigos de Windows y una clase de ventana Unicode y cómo escribir los procedimientos de ventana para ambos casos.</span><span class="sxs-lookup"><span data-stu-id="8d446-112">The following example shows how to register a Windows code page window class and a Unicode window class and how to write the window procedures for both cases.</span></span> <span data-ttu-id="8d446-113">Para los fines de este ejemplo, todas las funciones y estructuras se muestran con los tipos de datos "A" (ANSI) o "W" (ancho, Unicode) específicos.</span><span class="sxs-lookup"><span data-stu-id="8d446-113">For the purposes of this example, all functions and structures are shown with the specific "A" (ANSI) or "W" (wide, Unicode) data types.</span></span> <span data-ttu-id="8d446-114">Con las técnicas explicadas en el [uso de tipos de datos genéricos](using-generic-data-types.md), puede escribir este ejemplo de forma alternativa para usar tipos de datos genéricos, de modo que se pueda compilar para usar páginas de códigos de Windows o Unicode, dependiendo de si se define "Unicode".</span><span class="sxs-lookup"><span data-stu-id="8d446-114">Using the techniques explained in [Using Generic Data Types](using-generic-data-types.md), you can alternatively write this example to use generic data types, so that it can be compiled to use either Windows code pages or Unicode, depending on whether "UNICODE" is defined.</span></span>


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



<span data-ttu-id="8d446-115">En el ejemplo siguiente se muestra la diferencia entre [**controlar \_ el mensaje de tipo de salida**](../inputdev/wm-char.md) en un procedimiento de ventana de página de códigos de Windows y un procedimiento de ventana Unicode.</span><span class="sxs-lookup"><span data-stu-id="8d446-115">The following example shows the difference between handling the [**WM\_CHAR**](../inputdev/wm-char.md) message in a Windows code page window procedure and a Unicode window procedure.</span></span>


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



<span data-ttu-id="8d446-116">Todo el texto de los mensajes recibidos por **AnsiWndProc** se compone de caracteres de página de códigos de Windows.</span><span class="sxs-lookup"><span data-stu-id="8d446-116">All text in messages received by **AnsiWndProc** is composed of Windows code page characters.</span></span> <span data-ttu-id="8d446-117">Todo el texto de los mensajes recibidos por **UniWndProc** se compone de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="8d446-117">All text in messages received by **UniWndProc** is composed of Unicode characters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d446-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8d446-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d446-119">Usar Unicode y juegos de caracteres</span><span class="sxs-lookup"><span data-stu-id="8d446-119">Using Unicode and Character Sets</span></span>](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
