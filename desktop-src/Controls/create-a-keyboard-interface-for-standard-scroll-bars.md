---
title: Cómo crear una interfaz de teclado para las barras de desplazamiento estándar
description: Aunque un control de barra de desplazamiento proporciona una interfaz de teclado integrada, no existe una barra de desplazamiento estándar.
ms.assetid: 249D0077-6E61-479A-91D5-A4BD9752B82E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b739638d95d9f3e530718f8e9b9e6168069420
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103904846"
---
# <a name="how-to-create-a-keyboard-interface-for-standard-scroll-bars"></a><span data-ttu-id="0821b-103">Cómo crear una interfaz de teclado para las barras de desplazamiento estándar</span><span class="sxs-lookup"><span data-stu-id="0821b-103">How to Create a Keyboard Interface for Standard Scroll Bars</span></span>

<span data-ttu-id="0821b-104">Aunque un control de barra de desplazamiento proporciona una interfaz de teclado integrada, no existe una barra de desplazamiento estándar.</span><span class="sxs-lookup"><span data-stu-id="0821b-104">Although a scroll bar control provides a built-in keyboard interface, a standard scroll bar does not.</span></span> <span data-ttu-id="0821b-105">Para implementar una interfaz de teclado para una barra de desplazamiento estándar, un procedimiento de ventana debe procesar el mensaje de [**\_ KEYDOWN de WM**](/windows/desktop/inputdev/wm-keydown) y examinar el código de la clave virtual especificado por el parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="0821b-105">To implement a keyboard interface for a standard scroll bar, a window procedure must process the [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message and examine the virtual-key code specified by the *wParam* parameter.</span></span> <span data-ttu-id="0821b-106">Si el código de la clave virtual corresponde a una tecla de dirección, el procedimiento de ventana se envía a sí mismo un mensaje de [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) con la palabra de orden inferior del parámetro *wParam* establecida en el código de solicitud de la barra de desplazamiento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="0821b-106">If the virtual-key code corresponds to an arrow key, the window procedure sends itself a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the low-order word of the *wParam* parameter set to the appropriate scroll bar request code.</span></span>

<span data-ttu-id="0821b-107">Por ejemplo, cuando el usuario presiona la tecla de dirección arriba, el procedimiento de ventana recibe un mensaje [**\_ KEYDOWN de WM**](/windows/desktop/inputdev/wm-keydown) con *wParam* igual a VK \_ up.</span><span class="sxs-lookup"><span data-stu-id="0821b-107">For example, when the user presses the UP arrow key, the window procedure receives a [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message with *wParam* equal to VK\_UP.</span></span> <span data-ttu-id="0821b-108">En respuesta, el procedimiento de ventana se envía a sí mismo un mensaje de [**WM \_ VSCROLL**](wm-vscroll.md) con la palabra de orden inferior de *wParam* establecida en el código de solicitud de la línea de SB \_ .</span><span class="sxs-lookup"><span data-stu-id="0821b-108">In response, the window procedure sends itself a [**WM\_VSCROLL**](wm-vscroll.md) message with the low-order word of *wParam* set to the SB\_LINEUP request code.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="0821b-109">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="0821b-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="0821b-110">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="0821b-110">Technologies</span></span>

-   [<span data-ttu-id="0821b-111">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="0821b-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="0821b-112">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0821b-112">Prerequisites</span></span>

-   <span data-ttu-id="0821b-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="0821b-113">C/C++</span></span>
-   <span data-ttu-id="0821b-114">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="0821b-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="0821b-115">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="0821b-115">Instructions</span></span>

### <a name="create-a-keyboard-interface-for-a-standard-scroll-bar"></a><span data-ttu-id="0821b-116">Crear una interfaz de teclado para una barra de desplazamiento estándar</span><span class="sxs-lookup"><span data-stu-id="0821b-116">Create a Keyboard Interface for a Standard Scroll Bar</span></span>

<span data-ttu-id="0821b-117">En el ejemplo de código siguiente se muestra cómo incluir una interfaz de teclado para una barra de desplazamiento estándar.</span><span class="sxs-lookup"><span data-stu-id="0821b-117">The following code example demonstrates how to include a keyboard interface for a standard scroll bar.</span></span>


```C++
    case WM_KEYDOWN: 
    {
        WORD wScrollNotify = 0xFFFF;

        switch (wParam) 
        { 
            case VK_UP: 
                wScrollNotify = SB_LINEUP; 
                break; 
 
            case VK_PRIOR: 
                wScrollNotify = SB_PAGEUP; 
                break; 
 
            case VK_NEXT: 
                wScrollNotify = SB_PAGEDOWN; 
                break; 
 
            case VK_DOWN: 
                wScrollNotify = SB_LINEDOWN; 
                break; 
 
            case VK_HOME: 
                wScrollNotify = SB_TOP; 
                break; 
 
            case VK_END: 
                wScrollNotify = SB_BOTTOM; 
                break; 
        } 
 
        if (wScrollNotify != -1) 
            SendMessage(hwnd, WM_VSCROLL, MAKELONG(wScrollNotify, 0), 0L); 
 
        break; 
    }
```



## <a name="related-topics"></a><span data-ttu-id="0821b-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0821b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0821b-119">Usar barras de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="0821b-119">Using Scroll Bars</span></span>](using-scroll-bars.md)
</dt> <dt>

<span data-ttu-id="0821b-120">[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="0821b-120">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 