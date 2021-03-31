---
title: Cómo crear un control ComboBoxEx
description: En este tema se muestra cómo crear un control ComboBoxEx.
ms.assetid: E3D577AF-3290-431E-AA6C-1E9A9ED6448C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73989124982cb563fc008d7f3c543388cca685a5
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103995772"
---
# <a name="how-to-create-a-comboboxex-control"></a><span data-ttu-id="cee81-103">Cómo crear un control ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="cee81-103">How to Create a ComboBoxEx Control</span></span>

<span data-ttu-id="cee81-104">En este tema se muestra cómo crear un control ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="cee81-104">This topic demonstrates how to create a ComboBoxEx control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="cee81-105">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="cee81-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="cee81-106">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="cee81-106">Technologies</span></span>

-   [<span data-ttu-id="cee81-107">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="cee81-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="cee81-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cee81-108">Prerequisites</span></span>

-   <span data-ttu-id="cee81-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="cee81-109">C/C++</span></span>
-   <span data-ttu-id="cee81-110">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="cee81-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="cee81-111">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="cee81-111">Instructions</span></span>


<span data-ttu-id="cee81-112">Para crear un control ComboBoxEx, llame a la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , usando [**WC \_ ComboBoxEx**](common-control-window-classes.md) como clase de ventana.</span><span class="sxs-lookup"><span data-stu-id="cee81-112">To create a ComboBoxEx control, call the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, using [**WC\_COMBOBOXEX**](common-control-window-classes.md) as the window class.</span></span> <span data-ttu-id="cee81-113">Primero debe registrar la clase de ventana mediante una llamada a la función [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , al tiempo que especifica el \_ \_ bit de las clases USEREX de ICC en la estructura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="cee81-113">You must first register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function, while specifying the ICC\_USEREX\_CLASSES bit in the accompanying [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>

## <a name="complete-example"></a><span data-ttu-id="cee81-114">Ejemplo completo</span><span class="sxs-lookup"><span data-stu-id="cee81-114">Complete example</span></span>

<span data-ttu-id="cee81-115">La siguiente función definida por la aplicación crea un control ComboBoxEx con el estilo de [**\_ lista desplegable CBS**](combo-box-styles.md) en la ventana principal.</span><span class="sxs-lookup"><span data-stu-id="cee81-115">The following application-defined function creates a ComboBoxEx control with the [**CBS\_DROPDOWN**](combo-box-styles.md) style in the main window.</span></span>


```C++
// CreateComboEx - Registers the ComboBoxEx window class and creates
// a ComboBoxEx control in the client area of the main window.
//
// g_hwndMain - A handle to the main window.
// g_hinst    - A handle to the program instance.
HWND WINAPI CreateComboEx(void)
{
    HWND hwnd;
    INITCOMMONCONTROLSEX icex;

    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC = ICC_USEREX_CLASSES;

    InitCommonControlsEx(&icex);

    hwnd = CreateWindowEx(0, WC_COMBOBOXEX, NULL,
                    WS_BORDER | WS_VISIBLE |
                    WS_CHILD | CBS_DROPDOWN,
                    // No size yet--resize after setting image list.
                    0,      // Vertical position of Combobox
                    0,      // Horizontal position of Combobox
                    0,      // Sets the width of Combobox
                    100,    // Sets the height of Combobox
                    g_hwndMain,
                    NULL,
                    g_hinst,
                    NULL);

    return (hwnd);
}
```



## <a name="related-topics"></a><span data-ttu-id="cee81-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cee81-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cee81-117">Acerca de los controles ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="cee81-117">About ComboBoxEx Controls</span></span>](comboboxex-controls.md)
</dt> <dt>

[<span data-ttu-id="cee81-118">Referencia de control ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="cee81-118">ComboBoxEx Control Reference</span></span>](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[<span data-ttu-id="cee81-119">Usar controles ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="cee81-119">Using ComboBoxEx Controls</span></span>](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[<span data-ttu-id="cee81-120">ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="cee81-120">ComboBoxEx</span></span>](comboboxex-control-reference.md)
</dt> </dl>

 

 