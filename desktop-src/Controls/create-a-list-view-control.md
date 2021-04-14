---
title: Cómo crear un control de List-View
description: En este tema se muestra cómo crear un control de vista de lista. Para crear un control de vista de lista, use la función CreateWindow o CreateWindowEx y especifique la clase de ventana de ListView de WC \_ .
ms.assetid: FEAA0ACA-A086-46DF-9DD2-A3E32F2CCDA3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3050498b87aaf701249a06cfe2c3ad18afdc1d84
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104488561"
---
# <a name="how-to-create-a-list-view-control"></a><span data-ttu-id="77d80-104">Cómo crear un control de List-View</span><span class="sxs-lookup"><span data-stu-id="77d80-104">How to Create a List-View Control</span></span>

<span data-ttu-id="77d80-105">En este tema se muestra cómo crear un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="77d80-105">This topic demonstrates how to create a list-view control.</span></span> <span data-ttu-id="77d80-106">Para crear un control de vista de lista, use la función [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) y especifique la clase de ventana de [**\_ ListView de WC**](common-control-window-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="77d80-106">To create a list-view control, you use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function and specify the [**WC\_LISTVIEW**](common-control-window-classes.md) window class.</span></span>

<span data-ttu-id="77d80-107">Un control de vista de lista también se puede crear como parte de una plantilla de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="77d80-107">A list-view control can also be created as part of a dialog box template.</span></span> <span data-ttu-id="77d80-108">Debe especificar el [**\_ control de vista de WC**](common-control-window-classes.md) como el nombre de clase.</span><span class="sxs-lookup"><span data-stu-id="77d80-108">You must specify [**WC\_LISTVIEW**](common-control-window-classes.md) as the class name.</span></span> <span data-ttu-id="77d80-109">Para usar un control de vista de lista como parte de una plantilla de cuadro de diálogo, debe llamar a [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) o [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) antes de crear una instancia del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="77d80-109">To use a list-view control as part of a dialog box template, you must call [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) or [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) before you create an instance of the dialog box.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="77d80-110">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="77d80-110">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="77d80-111">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="77d80-111">Technologies</span></span>

-   [<span data-ttu-id="77d80-112">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="77d80-112">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="77d80-113">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="77d80-113">Prerequisites</span></span>

-   <span data-ttu-id="77d80-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="77d80-114">C/C++</span></span>
-   <span data-ttu-id="77d80-115">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="77d80-115">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="77d80-116">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="77d80-116">Instructions</span></span>


<span data-ttu-id="77d80-117">En primer lugar, registre la clase de ventana mediante una llamada a la función [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) y especificando el bit de [**\_ \_ las clases de ListView de ICC**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) en la estructura **InitCommonControlsEx** correspondiente.</span><span class="sxs-lookup"><span data-stu-id="77d80-117">First register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function and specifying the [**ICC\_LISTVIEW\_CLASSES**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) bit in the accompanying **INITCOMMONCONTROLSEX** structure.</span></span> <span data-ttu-id="77d80-118">Esto garantiza que se cargue el archivo DLL de controles comunes.</span><span class="sxs-lookup"><span data-stu-id="77d80-118">This ensures that the common controls DLL is loaded.</span></span> <span data-ttu-id="77d80-119">A continuación, use la función [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) y especifique la clase de ventana de [**\_ ListView de WC**](common-control-window-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="77d80-119">Next, use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function and specify the [**WC\_LISTVIEW**](common-control-window-classes.md) window class.</span></span>

> [!Note]  
> <span data-ttu-id="77d80-120">De forma predeterminada, un control de vista de lista usa la fuente del título del icono.</span><span class="sxs-lookup"><span data-stu-id="77d80-120">By default, a list-view control uses the icon title font.</span></span> <span data-ttu-id="77d80-121">Sin embargo, puede utilizar un mensaje de [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont) para especificar la fuente que se va a usar para el texto.</span><span class="sxs-lookup"><span data-stu-id="77d80-121">However, you can use a [**WM\_SETFONT**](/windows/desktop/winmsg/wm-setfont) message to specify the font to be used for the text.</span></span> <span data-ttu-id="77d80-122">Debe enviar este mensaje antes de insertar elementos.</span><span class="sxs-lookup"><span data-stu-id="77d80-122">You should send this message before inserting any items.</span></span> <span data-ttu-id="77d80-123">El control utiliza las dimensiones de la fuente especificada por el mensaje de **WM \_ SETFONT** para determinar el espaciado y el diseño.</span><span class="sxs-lookup"><span data-stu-id="77d80-123">The control uses the dimensions of the font that is specified by the **WM\_SETFONT** message to determine spacing and layout.</span></span> <span data-ttu-id="77d80-124">También puede personalizar la fuente para cada elemento.</span><span class="sxs-lookup"><span data-stu-id="77d80-124">You can also customize the font for each item.</span></span> <span data-ttu-id="77d80-125">Para obtener más información, vea [dibujo personalizado](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="77d80-125">For more information, see [Custom Draw](custom-draw.md).</span></span>

 

<span data-ttu-id="77d80-126">En el siguiente ejemplo de código de C++ se crea un control de vista de lista en la vista de informe.</span><span class="sxs-lookup"><span data-stu-id="77d80-126">The following C++ code example creates a list-view control in report view.</span></span>


```C++
// CreateListView: Creates a list-view control in report view.
// Returns the handle to the new control
// TO DO:  The calling procedure should determine whether the handle is NULL, in case 
// of an error in creation.
//
// HINST hInst: The global handle to the applicadtion instance.
// HWND  hWndParent: The handle to the control's parent window. 
//
HWND CreateListView (HWND hwndParent) 
{
    INITCOMMONCONTROLSEX icex;           // Structure for control initialization.
    icex.dwICC = ICC_LISTVIEW_CLASSES;
    InitCommonControlsEx(&icex);

    RECT rcClient;                       // The parent window's client area.

    GetClientRect (hwndParent, &rcClient); 

    // Create the list-view window in report view with label editing enabled.
    HWND hWndListView = CreateWindow(WC_LISTVIEW, 
                                     L"",
                                     WS_CHILD | LVS_REPORT | LVS_EDITLABELS,
                                     0, 0,
                                     rcClient.right - rcClient.left,
                                     rcClient.bottom - rcClient.top,
                                     hwndParent,
                                     (HMENU)IDM_CODE_SAMPLES,
                                     g_hInst,
                                     NULL); 

    return (hWndListView);
}

```




<span data-ttu-id="77d80-127">Normalmente, las aplicaciones de vista de lista permiten al usuario cambiar de una vista a otra.</span><span class="sxs-lookup"><span data-stu-id="77d80-127">Typically, list-view applications enable the user to change from one view to another.</span></span>

<span data-ttu-id="77d80-128">En el siguiente ejemplo de código de C++ se cambia el estilo de ventana de la vista de lista, que a su vez cambia la vista.</span><span class="sxs-lookup"><span data-stu-id="77d80-128">The following C++ code example changes the list-view's window style, which in turn changes the view.</span></span>


```C++
// SetView: Sets a list-view's window style to change the view.
// hWndListView: A handle to the list-view control. 
// dwView:       A value specifying the new view style.
//
VOID SetView(HWND hWndListView, DWORD dwView) 
{ 
    // Retrieve the current window style. 
    DWORD dwStyle = GetWindowLong(hWndListView, GWL_STYLE); 
    
    // Set the window style only if the view bits changed.
    if ((dwStyle & LVS_TYPEMASK) != dwView) 
    {
        SetWindowLong(hWndListView,
                      GWL_STYLE,
                      (dwStyle & ~LVS_TYPEMASK) | dwView);
    }               // Logical OR'ing of dwView with the result of 
}                   // a bitwise AND between dwStyle and 
                    // the Unary complenent of LVS_TYPEMASK.

```



## <a name="related-topics"></a><span data-ttu-id="77d80-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="77d80-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77d80-130">Referencia de control de vista de lista</span><span class="sxs-lookup"><span data-stu-id="77d80-130">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="77d80-131">Acerca de los controles List-View</span><span class="sxs-lookup"><span data-stu-id="77d80-131">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="77d80-132">Usar controles List-View</span><span class="sxs-lookup"><span data-stu-id="77d80-132">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 