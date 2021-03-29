---
title: Cómo crear barras de herramientas verticales
description: La clave para crear una barra de herramientas vertical consiste en incluir CCS \_ Vert en el estilo de ventana y establecer el \_ estilo de ajuste de TBSTATE para cada botón.
ms.assetid: C2EAB160-0D8D-4BB9-AD41-D5175FBE81AB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd32609e81196a94f4298197c33a4cc6e21d117
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "103995042"
---
# <a name="how-to-create-vertical-toolbars"></a><span data-ttu-id="0d6ef-103">Cómo crear barras de herramientas verticales</span><span class="sxs-lookup"><span data-stu-id="0d6ef-103">How to Create Vertical Toolbars</span></span>

<span data-ttu-id="0d6ef-104">La clave para crear una barra de herramientas vertical consiste en incluir [**CCS \_ Vert**](common-control-styles.md) en el estilo de ventana y establecer el estilo de [**\_ ajuste de TBSTATE**](toolbar-button-states.md) para cada botón.</span><span class="sxs-lookup"><span data-stu-id="0d6ef-104">The key to creating a vertical toolbar is to include [**CCS\_VERT**](common-control-styles.md) in the window style, and to set the [**TBSTATE\_WRAP**](toolbar-button-states.md) style for each button.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="0d6ef-105">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="0d6ef-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="0d6ef-106">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="0d6ef-106">Technologies</span></span>

-   [<span data-ttu-id="0d6ef-107">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="0d6ef-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="0d6ef-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0d6ef-108">Prerequisites</span></span>

-   <span data-ttu-id="0d6ef-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="0d6ef-109">C/C++</span></span>
-   <span data-ttu-id="0d6ef-110">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="0d6ef-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="0d6ef-111">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="0d6ef-111">Instructions</span></span>

### <a name="create-a-vertical-toolbar"></a><span data-ttu-id="0d6ef-112">Crear una barra de herramientas vertical</span><span class="sxs-lookup"><span data-stu-id="0d6ef-112">Create a Vertical Toolbar</span></span>

<span data-ttu-id="0d6ef-113">En el código de ejemplo siguiente se crea la barra de herramientas vertical que se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="0d6ef-113">The following example code creates the vertical toolbar shown in the following illustration.</span></span>

![captura de pantalla que muestra un cuadro de diálogo con tres elementos de la barra de herramientas organizados verticalmente, cada uno de los cuales solo tiene un icono](images/tb-vertical.png)


```C++
HIMAGELIST g_hImageList = NULL;

HWND CreateVerticalToolbar(HWND hWndParent)
{
    // Define the buttons.
    // IDM_NEW, IDM_0PEN, and IDM_SAVE are application-defined command IDs.
    
    TBBUTTON tbButtons3[numButtons] = 
    {
        {STD_FILENEW,  IDM_NEW,  TBSTATE_ENABLED | TBSTATE_WRAP, BTNS_BUTTON, {0}, 0L, 0},
        {STD_FILEOPEN, IDM_OPEN, TBSTATE_ENABLED | TBSTATE_WRAP, BTNS_BUTTON, {0}, 0L, 0},
        {STD_FILESAVE, IDM_SAVE, TBSTATE_ENABLED | TBSTATE_WRAP, BTNS_BUTTON, {0}, 0L, 0}
    };

    // Create the toolbar window.
    HWND hWndToolbar = CreateWindowEx(0, TOOLBARCLASSNAME, NULL, 
                                      WS_CHILD | WS_VISIBLE | CCS_VERT | WS_BORDER, 0, 0, 0, 0,
                                      hWndParent, NULL, g_hInst, NULL);

    // Create the image list.
    g_hImageList = ImageList_Create(24, 24,                   // Dimensions of individual bitmaps.  
                                    ILC_COLOR16 | ILC_MASK,   // Ensures transparent background.
                                    numButtons, 0);

    // Set the image list.
    SendMessage(hWndToolbar, TB_SETIMAGELIST, 0, (LPARAM)g_hImageList);

    // Load the button images.
    SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_LARGE_COLOR, (LPARAM)HINST_COMMCTRL);

    // Add them to the toolbar.
    SendMessage(hWndToolbar, TB_BUTTONSTRUCTSIZE,       (WPARAM)sizeof(TBBUTTON), 0);
    SendMessage(hWndToolbar, TB_ADDBUTTONS, numButtons, (LPARAM)&tbButtons3);

    return hWndToolbar;
} 
```



## <a name="related-topics"></a><span data-ttu-id="0d6ef-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0d6ef-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d6ef-116">Usar controles Toolbar</span><span class="sxs-lookup"><span data-stu-id="0d6ef-116">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="0d6ef-117">[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="0d6ef-117">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




