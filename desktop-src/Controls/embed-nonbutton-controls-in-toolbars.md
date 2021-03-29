---
title: Cómo insertar controles que no son de botón en las barras de herramientas
description: Las barras de herramientas solo admiten botones; por lo tanto, si la aplicación requiere un tipo de control diferente, debe crear una ventana secundaria. En la ilustración siguiente se muestra una barra de herramientas con un control de edición incrustado.
ms.assetid: 7B4DACEF-96BB-447E-AE8F-F55401C665E9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8ae2189350b9ea2f4aaa0c3ea0b49727bd3415
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "103904452"
---
# <a name="how-to-embed-nonbutton-controls-in-toolbars"></a><span data-ttu-id="9f1d8-104">Cómo insertar controles que no son de botón en las barras de herramientas</span><span class="sxs-lookup"><span data-stu-id="9f1d8-104">How to Embed Nonbutton Controls in Toolbars</span></span>

<span data-ttu-id="9f1d8-105">Las barras de herramientas solo admiten botones; por lo tanto, si la aplicación requiere un tipo de control diferente, debe crear una ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-105">Toolbars support only buttons; therefore, if your application requires a different kind of control, you must create a child window.</span></span> <span data-ttu-id="9f1d8-106">En la ilustración siguiente se muestra una barra de herramientas con un control de edición incrustado.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-106">The following illustration shows a toolbar with an embedded edit control.</span></span>

![captura de pantalla de un cuadro de diálogo con un control de edición en la barra de herramientas, que precede a tres iconos de barra de herramientas](images/tb-withedit.png)

> [!Note]  
> <span data-ttu-id="9f1d8-108">Considere la posibilidad de utilizar [controles rebar](rebar-controls.md) en lugar de colocar controles en las barras de herramientas.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-108">Consider using [Rebar Controls](rebar-controls.md) instead of placing controls in toolbars.</span></span>

 

<span data-ttu-id="9f1d8-109">Cualquier tipo de ventana se puede colocar en una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-109">Any type of window can be placed on a toolbar.</span></span> <span data-ttu-id="9f1d8-110">En el ejemplo de código siguiente se agrega un control de edición como elemento secundario de la ventana de control de barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-110">The following example code adds an edit control as a child of the toolbar control window.</span></span> <span data-ttu-id="9f1d8-111">Dado que la barra de herramientas se crea y, a continuación, se agrega el control de edición, debe proporcionar espacio para el control de edición.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-111">Because the toolbar is created and then the edit control added, you must provide space for the edit control.</span></span> <span data-ttu-id="9f1d8-112">Una manera de hacerlo es agregar un separador como un marcador de posición en la barra de herramientas, estableciendo el ancho del separador en el número de píxeles que desea reservar.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-112">One way to do this is to add a separator as a placeholder in the toolbar, setting the width of the separator to the number of pixels you want to reserve.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="9f1d8-113">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="9f1d8-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="9f1d8-114">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="9f1d8-114">Technologies</span></span>

-   [<span data-ttu-id="9f1d8-115">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="9f1d8-115">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="9f1d8-116">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9f1d8-116">Prerequisites</span></span>

-   <span data-ttu-id="9f1d8-117">C/C++</span><span class="sxs-lookup"><span data-stu-id="9f1d8-117">C/C++</span></span>
-   <span data-ttu-id="9f1d8-118">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="9f1d8-118">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="9f1d8-119">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="9f1d8-119">Instructions</span></span>

### <a name="embed-a-nonbutton-control-in-a-toolbar"></a><span data-ttu-id="9f1d8-120">Insertar un control no botón en una barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="9f1d8-120">Embed a Nonbutton Control in a Toolbar</span></span>

<span data-ttu-id="9f1d8-121">En el fragmento de código siguiente se crea la barra de herramientas en la ilustración anterior.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-121">The following code snippet creates the toolbar in the preceding illustration.</span></span>


```C++
// IDM_NEW, IDM_OPEN, and IDM_SAVE are application-defined command constants.

HIMAGELIST g_hImageList = NULL;

HWND CreateToolbarWithEdit(HWND hWndParent)
{
    const int ImageListID = 0;    // Define some constants.
    const int bitmapSize  = 16;
    
    const int cx_edit = 100;      // Dimensions of edit control.
    const int cy_edit = 35;  

    TBBUTTON tbButtons[] =        // Toolbar buttons.
    {
        // The separator is set to the width of the edit control. 
        
        {cx_edit, 0, TBSTATE_ENABLED, BTNS_SEP, {0}, 0, -1},
        {STD_FILENEW, IDM_NEW, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {STD_FILEOPEN, IDM_OPEN, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {STD_FILESAVE, IDM_SAVE, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {0, 0, TBSTATE_ENABLED, BTNS_SEP, {0}, 0, 0},
    };

    // Create the toolbar.
    HWND hWndToolbar = CreateWindowEx(0, TOOLBARCLASSNAME, L"Toolbar", 
                                      WS_CHILD | WS_VISIBLE | WS_BORDER, 
                                      0, 0, 0, 0,
                                      hWndParent, NULL, HINST_COMMCTRL, NULL);

    if (!hWndToolbar)
        return NULL;
    
    int numButtons = sizeof(tbButtons) / sizeof(TBBUTTON);

    // Create the image list.
    g_hImageList = ImageList_Create(bitmapSize, bitmapSize, // Dimensions of individual bitmaps.
                                    0,                      // Flags.
                                    numButtons, 0);

    // Set the image list.
    SendMessage(hWndToolbar, TB_SETIMAGELIST, (WPARAM)ImageListID, (LPARAM)g_hImageList);

    // Load the button images.
    SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);

    // Add buttons.
    SendMessage(hWndToolbar, TB_BUTTONSTRUCTSIZE, (WPARAM)sizeof(TBBUTTON), 0);
    SendMessage(hWndToolbar, TB_ADDBUTTONS,       (WPARAM)numButtons,       (LPARAM)&tbButtons);

    // Create the edit control child window.    
    HWND hWndEdit = CreateWindowEx(0L, L"Edit", NULL, 
                                   WS_CHILD | WS_BORDER | WS_VISIBLE | ES_LEFT | ES_AUTOVSCROLL | ES_MULTILINE, 
                                   0, 0, cx_edit, cy_edit, 
                                   hWndToolbar, (HMENU) IDM_EDIT, g_hInst, 0 );
    
    if (!hWndEdit)
    {
        DestroyWindow(hWndToolbar);
        ImageList_Destroy(g_hImageList);
        
        return NULL;
    }
    
    return hWndToolbar;    // Return the toolbar with the embedded edit control.
}
```



<span data-ttu-id="9f1d8-122">En este ejemplo se codifican de forma rígida las dimensiones de la ventana secundaria; sin embargo, para crear una aplicación más sólida, determine el tamaño de la barra de herramientas y haga que la ventana Editar control se ajuste.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-122">This example hard-codes the dimensions of the child window; however, to make a more robust application, determine the size of the toolbar and make the edit control window to fit.</span></span>

<span data-ttu-id="9f1d8-123">Es posible que desee que las notificaciones de control de edición se desplazan a otra ventana, como el elemento primario de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-123">You might want the edit control notifications to go to another window, such as the toolbar's parent.</span></span> <span data-ttu-id="9f1d8-124">Para ello, cree el control de edición como un elemento secundario de la ventana primaria de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-124">To do this, create the edit control as a child of the toolbar's parent window.</span></span> <span data-ttu-id="9f1d8-125">A continuación, cambie el elemento primario del control de edición a la barra de herramientas como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-125">Then change the parent of the edit control to the toolbar as follows.</span></span>


```
SetParent (hWndEdit, hWndToolbar);
```



<span data-ttu-id="9f1d8-126">Las notificaciones se dirigen al elemento primario original.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-126">Notifications go to the original parent.</span></span> <span data-ttu-id="9f1d8-127">Por lo tanto, los mensajes del control de edición van al elemento primario de la barra de herramientas aunque la ventana de edición resida en la ventana de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-127">Therefore, the edit control messages go to the parent of the toolbar even though the edit window resides in the toolbar window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f1d8-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9f1d8-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f1d8-129">Usar controles Toolbar</span><span class="sxs-lookup"><span data-stu-id="9f1d8-129">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="9f1d8-130">[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="9f1d8-130">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




