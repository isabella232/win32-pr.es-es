---
title: Cómo crear barras de herramientas
description: Para crear una barra de herramientas, utilice la función CreateWindowEx, especificando la clase de ventana TOOLBARCLASSNAME.
ms.assetid: 5D060291-6ACF-478C-97EC-CD8BD55D1FFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a69cd40338eaebc0d9de852519dce34dc9bc8aa4
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793960"
---
# <a name="how-to-create-toolbars"></a><span data-ttu-id="daa68-103">Cómo crear barras de herramientas</span><span class="sxs-lookup"><span data-stu-id="daa68-103">How to Create Toolbars</span></span>

<span data-ttu-id="daa68-104">Para crear una barra de herramientas, utilice la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando la clase de ventana [**TOOLBARCLASSNAME**](common-control-window-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="daa68-104">To create a toolbar, use the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the [**TOOLBARCLASSNAME**](common-control-window-classes.md) window class.</span></span> <span data-ttu-id="daa68-105">La barra de herramientas resultante no contiene inicialmente ningún botón.</span><span class="sxs-lookup"><span data-stu-id="daa68-105">The resulting toolbar initially contains no buttons.</span></span> <span data-ttu-id="daa68-106">Agregue botones a la barra de herramientas mediante el mensaje [**TB \_ ADDBUTTONS**](tb-addbuttons.md) o [**TB \_ INSERTBUTTON**](tb-insertbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="daa68-106">Add buttons to the toolbar by using the [**TB\_ADDBUTTONS**](tb-addbuttons.md) or [**TB\_INSERTBUTTON**](tb-insertbutton.md) message.</span></span> <span data-ttu-id="daa68-107">Debe enviar el mensaje [**de \_ tamaño de TB automático**](tb-autosize.md) después de que todos los elementos y las cadenas se hayan insertado en el control para que la barra de herramientas recalcule su tamaño en función de su contenido.</span><span class="sxs-lookup"><span data-stu-id="daa68-107">You must send the [**TB\_AUTOSIZE**](tb-autosize.md) message after all the items and strings have been inserted into the control, to cause the toolbar to recalculate its size based on its content.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="daa68-108">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="daa68-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="daa68-109">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="daa68-109">Technologies</span></span>

-   [<span data-ttu-id="daa68-110">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="daa68-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="daa68-111">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="daa68-111">Prerequisites</span></span>

-   <span data-ttu-id="daa68-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="daa68-112">C/C++</span></span>
-   <span data-ttu-id="daa68-113">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="daa68-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="daa68-114">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="daa68-114">Instructions</span></span>

### <a name="create-a-toolbar"></a><span data-ttu-id="daa68-115">Crear una barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="daa68-115">Create a Toolbar</span></span>

<span data-ttu-id="daa68-116">En el código de ejemplo siguiente se crea la barra de herramientas que se muestra en la ilustración, utilizando los iconos del sistema estándar.</span><span class="sxs-lookup"><span data-stu-id="daa68-116">The following example code creates the toolbar shown in the illustration, using standard system icons.</span></span> <span data-ttu-id="daa68-117">El botón **Guardar** está deshabilitado inicialmente.</span><span class="sxs-lookup"><span data-stu-id="daa68-117">The **Save** button is initially disabled.</span></span>

![captura de pantalla que muestra un cuadro de diálogo con tres elementos de la barra de herramientas dispuestos horizontalmente, cada uno de los cuales tiene un icono y una etiqueta de texto](images/tb-codesample1.png)


```C++
HIMAGELIST g_hImageList = NULL;

HWND CreateSimpleToolbar(HWND hWndParent)
{
    // Declare and initialize local constants.
    const int ImageListID    = 0;
    const int numButtons     = 3;
    const int bitmapSize     = 16;
    
    const DWORD buttonStyles = BTNS_AUTOSIZE;

    // Create the toolbar.
    HWND hWndToolbar = CreateWindowEx(0, TOOLBARCLASSNAME, NULL, 
                                      WS_CHILD | TBSTYLE_WRAPABLE, 0, 0, 0, 0, 
                                      hWndParent, NULL, g_hInst, NULL);
        
    if (hWndToolbar == NULL)
        return NULL;

    // Create the image list.
    g_hImageList = ImageList_Create(bitmapSize, bitmapSize,   // Dimensions of individual bitmaps.
                                    ILC_COLOR16 | ILC_MASK,   // Ensures transparent background.
                                    numButtons, 0);

    // Set the image list.
    SendMessage(hWndToolbar, TB_SETIMAGELIST, 
                (WPARAM)ImageListID, 
                (LPARAM)g_hImageList);

    // Load the button images.
    SendMessage(hWndToolbar, TB_LOADIMAGES, 
                (WPARAM)IDB_STD_SMALL_COLOR, 
                (LPARAM)HINST_COMMCTRL);

    // Initialize button info.
    // IDM_NEW, IDM_OPEN, and IDM_SAVE are application-defined command constants.
    
    TBBUTTON tbButtons[numButtons] = 
    {
        { MAKELONG(STD_FILENEW,  ImageListID), IDM_NEW,  TBSTATE_ENABLED, buttonStyles, {0}, 0, (INT_PTR)L"New" },
        { MAKELONG(STD_FILEOPEN, ImageListID), IDM_OPEN, TBSTATE_ENABLED, buttonStyles, {0}, 0, (INT_PTR)L"Open"},
        { MAKELONG(STD_FILESAVE, ImageListID), IDM_SAVE, 0,               buttonStyles, {0}, 0, (INT_PTR)L"Save"}
    };

    // Add buttons.
    SendMessage(hWndToolbar, TB_BUTTONSTRUCTSIZE, (WPARAM)sizeof(TBBUTTON), 0);
    SendMessage(hWndToolbar, TB_ADDBUTTONS,       (WPARAM)numButtons,       (LPARAM)&tbButtons);

    // Resize the toolbar, and then show it.
    SendMessage(hWndToolbar, TB_AUTOSIZE, 0, 0); 
    ShowWindow(hWndToolbar,  TRUE);
    
    return hWndToolbar;
}
```



<span data-ttu-id="daa68-119">En el ejemplo siguiente se crea la misma barra de herramientas prácticamente de la misma manera, pero en este caso, las cadenas se leen desde un recurso.</span><span class="sxs-lookup"><span data-stu-id="daa68-119">The following example creates the same toolbar in much the same way, but in this case, the strings are read from a resource.</span></span>


```C++
HIMAGELIST g_hImageList = NULL;

HWND CreateToolbarFromResource(HWND hWndParent)
{
    // Declare and initialize local constants.
    const int ImageListID    = 0;
    const int numButtons     = 3;
    const int bitmapSize     = 16;
    
    const DWORD buttonStyles = BTNS_AUTOSIZE;

    // Create the toolbar.
    HWND hWndToolbar = CreateWindowEx(0, TOOLBARCLASSNAME, NULL, 
                                      WS_CHILD | TBSTYLE_WRAPABLE, 0, 0, 0, 0,
                                      hWndParent, NULL, g_hInst, NULL);
    if (hWndToolbar == NULL)
        return NULL;

    // Create the image list.
    g_hImageList = ImageList_Create(bitmapSize, bitmapSize, // Dimensions of individual bitmaps.
                                    ILC_COLOR16 | ILC_MASK, // Ensures transparent background.
                                    numButtons, 0);

    // Set the image list.
    SendMessage(hWndToolbar, TB_SETIMAGELIST, 
                (WPARAM)ImageListID, 
                (LPARAM)g_hImageList);

    // Load the button images.
    SendMessage(hWndToolbar, TB_LOADIMAGES, 
                (WPARAM)IDB_STD_SMALL_COLOR, 
                (LPARAM)HINST_COMMCTRL);

    // Load the text from a resource.
    
    // In the string table, the text for all buttons is a single entry that 
    // appears as "~New~Open~Save~~". The separator character is arbitrary, 
    // but it must appear as the first character of the string. The message 
    // returns the index of the first item, and the items are numbered 
    // consecutively.
    
    int iNew = SendMessage(hWndToolbar, TB_ADDSTRING, 
                           (WPARAM)g_hInst, (LPARAM)IDS_NEW); 
 
    // Initialize button info.
    // IDM_NEW, IDM_OPEN, and IDM_SAVE are application-defined command constants.
    
    TBBUTTON tbButtons[numButtons] = 
    {
        { MAKELONG(STD_FILENEW,  ImageListID), IDM_NEW,  TBSTATE_ENABLED, buttonStyles, {0}, 0, iNew },
        { MAKELONG(STD_FILEOPEN, ImageListID), IDM_OPEN, TBSTATE_ENABLED, buttonStyles, {0}, 0, iNew + 1},
        { MAKELONG(STD_FILESAVE, ImageListID), IDM_SAVE, 0,               buttonStyles, {0}, 0, iNew + 2}
    };

    // Add buttons.
    SendMessage(hWndToolbar, TB_BUTTONSTRUCTSIZE, (WPARAM)sizeof(TBBUTTON), 0);
    SendMessage(hWndToolbar, TB_ADDBUTTONS,       (WPARAM)numButtons,       (LPARAM)&tbButtons);

    // Resize the toolbar, and then show it.
    SendMessage(hWndToolbar, TB_AUTOSIZE, 0, 0); 
    ShowWindow(hWndToolbar,  TRUE);
    
    return hWndToolbar;
}
```



## <a name="related-topics"></a><span data-ttu-id="daa68-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="daa68-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="daa68-121">Usar controles Toolbar</span><span class="sxs-lookup"><span data-stu-id="daa68-121">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="daa68-122">[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="daa68-122">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 