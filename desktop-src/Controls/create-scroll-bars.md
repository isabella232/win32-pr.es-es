---
title: Cómo crear barras de desplazamiento
description: Al crear una ventana superpuesta, emergente o secundaria, puede Agregar barras de desplazamiento estándar mediante la función CreateWindowEx y especificando WS \_ HSCROLL, WS \_ VSCROLL o ambos estilos.
ms.assetid: 58353030-DCF5-4368-9658-BB282B8B5EF0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06b27e3e6d9495492f46567633cc53b0f3f7c5bd
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488378"
---
# <a name="how-to-create-scroll-bars"></a><span data-ttu-id="ea0c3-103">Cómo crear barras de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="ea0c3-103">How to Create Scroll Bars</span></span>

<span data-ttu-id="ea0c3-104">Al crear una ventana superpuesta, emergente o secundaria, puede Agregar barras de desplazamiento estándar mediante la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) y especificando WS \_ HSCROLL, WS \_ VSCROLL o ambos estilos.</span><span class="sxs-lookup"><span data-stu-id="ea0c3-104">When creating an overlapped, pop-up, or child window, you can add standard scroll bars by using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function and specifying WS\_HSCROLL, WS\_VSCROLL, or both styles.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ea0c3-105">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="ea0c3-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ea0c3-106">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="ea0c3-106">Technologies</span></span>

-   [<span data-ttu-id="ea0c3-107">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="ea0c3-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="ea0c3-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ea0c3-108">Prerequisites</span></span>

-   <span data-ttu-id="ea0c3-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="ea0c3-109">C/C++</span></span>
-   <span data-ttu-id="ea0c3-110">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="ea0c3-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="ea0c3-111">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="ea0c3-111">Instructions</span></span>

### <a name="create-a-scroll-bar"></a><span data-ttu-id="ea0c3-112">Crear una barra de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="ea0c3-112">Create a Scroll Bar</span></span>

<span data-ttu-id="ea0c3-113">En el ejemplo siguiente se crea una ventana con barras de desplazamiento horizontal y vertical estándar.</span><span class="sxs-lookup"><span data-stu-id="ea0c3-113">The following example creates a window with standard horizontal and vertical scroll bars.</span></span>


```C++
    hwnd = CreateWindowEx( 
        0,                     // no extended styles 
        g_szWindowClass,       // global string containing name of window class
        g_szTitle,             // global string containing title bar text 
        WS_OVERLAPPEDWINDOW |  
            WS_HSCROLL | WS_VSCROLL, // window styles 
        CW_USEDEFAULT,         // default horizontal position 
        CW_USEDEFAULT,         // default vertical position 
        CW_USEDEFAULT,         // default width 
        CW_USEDEFAULT,         // default height 
        (HWND) NULL,           // no parent for overlapped windows 
        (HMENU) NULL,          // use the window class menu 
        g_hInst,               // global instance handle  
        (PVOID) NULL           // pointer not needed 
    ); 
```



<span data-ttu-id="ea0c3-114">Para procesar los mensajes de la barra de desplazamiento para estas barras de desplazamiento, debe incluir el código adecuado en el procedimiento de ventana principal.</span><span class="sxs-lookup"><span data-stu-id="ea0c3-114">To process scroll bar messages for these scroll bars, you must include appropriate code in the main window procedure.</span></span>

<span data-ttu-id="ea0c3-115">Puede usar la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para crear una barra de desplazamiento especificando la clase de ventana de la barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="ea0c3-115">You can use the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create a scroll bar by specifying the SCROLLBAR window class.</span></span> <span data-ttu-id="ea0c3-116">Esto crea una barra de desplazamiento horizontal o vertical, en función de si se especifica [**SBS \_ horizontal**](scroll-bar-control-styles.md) o [**SBS \_ Vert**](scroll-bar-control-styles.md) como estilo de ventana.</span><span class="sxs-lookup"><span data-stu-id="ea0c3-116">This creates a horizontal or vertical scroll bar, depending on whether [**SBS\_HORZ**](scroll-bar-control-styles.md) or [**SBS\_VERT**](scroll-bar-control-styles.md) is specified as the window style.</span></span> <span data-ttu-id="ea0c3-117">También se puede especificar el tamaño de la barra de desplazamiento y su posición en relación con su ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="ea0c3-117">The scroll bar size and its position relative to its parent window can also be specified.</span></span>

<span data-ttu-id="ea0c3-118">En el ejemplo siguiente se crea una barra de desplazamiento horizontal que se coloca a lo largo de la parte inferior del área de cliente de la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="ea0c3-118">The following example creates a horizontal scroll bar that is positioned along the bottom of the parent window's client area.</span></span>


```C++
// Description:
//   Creates a horizontal scroll bar along the bottom of the parent 
//   window's area.
// Parameters:
//   hwndParent - handle to the parent window.
//   sbHeight - height, in pixels, of the scroll bar.
// Returns:
//   The handle to the scroll bar.
HWND CreateAHorizontalScrollBar(HWND hwndParent, int sbHeight)
{
    RECT rect;

    // Get the dimensions of the parent window's client area;
    if (!GetClientRect(hwndParent, &rect))
        return NULL;

    // Create the scroll bar.
    return (CreateWindowEx( 
            0,                      // no extended styles 
            L"SCROLLBAR",           // scroll bar control class 
            (PTSTR) NULL,           // no window text 
            WS_CHILD | WS_VISIBLE   // window styles  
                | SBS_HORZ,         // horizontal scroll bar style 
            rect.left,              // horizontal position 
            rect.bottom - sbHeight, // vertical position 
            rect.right,             // width of the scroll bar 
            sbHeight,               // height of the scroll bar
            hwndParent,             // handle to main window 
            (HMENU) NULL,           // no menu 
            g_hInst,                // instance owning this window 
            (PVOID) NULL            // pointer not needed 
        )); 
}
```



## <a name="related-topics"></a><span data-ttu-id="ea0c3-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ea0c3-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea0c3-120">Usar barras de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="ea0c3-120">Using Scroll Bars</span></span>](using-scroll-bars.md)
</dt> <dt>

<span data-ttu-id="ea0c3-121">[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="ea0c3-121">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 