---
title: Cómo crear barras de desplazamiento
description: Al crear una ventana superpuesta, emergente o secundaria, puede agregar barras de desplazamiento estándar mediante la función CreateWindowEx y especificando WS \_ HSCROLL, WS VSCROLL o ambos \_ estilos.
ms.assetid: 58353030-DCF5-4368-9658-BB282B8B5EF0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06b27e3e6d9495492f46567633cc53b0f3f7c5bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061394"
---
# <a name="how-to-create-scroll-bars"></a>Cómo crear barras de desplazamiento

Al crear una ventana superpuesta, emergente o secundaria, puede agregar barras de desplazamiento estándar mediante la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) y especificando WS \_ HSCROLL, WS VSCROLL o ambos \_ estilos.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="create-a-scroll-bar"></a>Crear una barra de desplazamiento

En el ejemplo siguiente se crea una ventana con barras de desplazamiento horizontales y verticales estándar.


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



Para procesar los mensajes de la barra de desplazamiento de estas barras de desplazamiento, debe incluir el código adecuado en el procedimiento de la ventana principal.

Puede usar la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para crear una barra de desplazamiento especificando la clase de ventana SCROLLBAR. Esto crea una barra de desplazamiento horizontal o vertical, dependiendo de si [**SBS \_ HORZ**](scroll-bar-control-styles.md) o [**SBS \_ VERT**](scroll-bar-control-styles.md) se especifica como estilo de ventana. También se puede especificar el tamaño de la barra de desplazamiento y su posición con respecto a su ventana primaria.

En el ejemplo siguiente se crea una barra de desplazamiento horizontal que se coloca a lo largo de la parte inferior del área de cliente de la ventana primaria.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar barras de desplazamiento](using-scroll-bars.md)
</dt> <dt>

[Windows demostración de controles comunes (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 