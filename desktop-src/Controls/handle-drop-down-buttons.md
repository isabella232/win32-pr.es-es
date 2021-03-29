---
title: Cómo controlar botones desplegables
description: Un botón desplegable puede presentar a los usuarios una lista de opciones.
ms.assetid: 2D908D4B-AA8B-4DEF-B656-C37B673ABB4D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35d6f59bfa888d346e196e13ce030d1473a07f0f
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "103789352"
---
# <a name="how-to-handle-drop-down-buttons"></a><span data-ttu-id="fe81f-103">Cómo controlar botones desplegables</span><span class="sxs-lookup"><span data-stu-id="fe81f-103">How to Handle Drop-down Buttons</span></span>

<span data-ttu-id="fe81f-104">Un botón desplegable puede presentar a los usuarios una lista de opciones.</span><span class="sxs-lookup"><span data-stu-id="fe81f-104">A drop-down button can present users with a list of options.</span></span> <span data-ttu-id="fe81f-105">Para crear este estilo de botón, especifique el estilo de [**\_ lista desplegable BTNS**](toolbar-control-and-button-styles.md) (también denominado [**\_ desplegable TBSTYLE**](toolbar-control-and-button-styles.md) para la compatibilidad con versiones anteriores de los controles comunes).</span><span class="sxs-lookup"><span data-stu-id="fe81f-105">To create this style of button, specify the [**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md) style (also called [**TBSTYLE\_DROPDOWN**](toolbar-control-and-button-styles.md) for compatibility with previous versions of the common controls).</span></span> <span data-ttu-id="fe81f-106">Para mostrar un botón desplegable con una flecha, también debe establecer el estilo de la barra de herramientas [**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) mediante el envío de un mensaje [**TB \_ SETEXTENDEDSTYLE**](tb-setextendedstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="fe81f-106">To show a drop-down button with an arrow, you must also set the [**TBSTYLE\_EX\_DRAWDDARROWS**](toolbar-extended-styles.md) toolbar style by sending a [**TB\_SETEXTENDEDSTYLE**](tb-setextendedstyle.md) message.</span></span>

<span data-ttu-id="fe81f-107">En la ilustración siguiente se muestra un botón "abrir" desplegable con el menú contextual abierto que muestra una lista de archivos.</span><span class="sxs-lookup"><span data-stu-id="fe81f-107">The following illustration shows a drop-down "Open" button with the context menu open and showing a list of files.</span></span> <span data-ttu-id="fe81f-108">En este ejemplo, la barra de herramientas tiene el estilo [**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="fe81f-108">In this example, the toolbar has the [**TBSTYLE\_EX\_DRAWDDARROWS**](toolbar-extended-styles.md) style.</span></span>

![captura de pantalla de un cuadro de diálogo con tres elementos de la barra de herramientas representados por iconos; uno tiene una flecha desplegable expandida y un menú contextual de tres elementos](images/tb-dropdown.png)

<span data-ttu-id="fe81f-110">En la ilustración siguiente se muestra la misma barra de herramientas, esta vez sin el estilo [**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="fe81f-110">The following illustration shows the same toolbar, this time without the [**TBSTYLE\_EX\_DRAWDDARROWS**](toolbar-extended-styles.md) style.</span></span>

![captura de pantalla de un cuadro de diálogo anterior, pero el icono con el menú contextual no tiene ninguna flecha de lista desplegable](images/tb-dropdown2.png)

<span data-ttu-id="fe81f-112">Cuando los usuarios hacen clic en un botón de la barra de herramientas que usa el estilo [**\_ desplegable BTNS**](toolbar-control-and-button-styles.md) , el control de barra de herramientas envía a su ventana primaria un código de notificación [ \_ desplegable TBN](tbn-dropdown.md) .</span><span class="sxs-lookup"><span data-stu-id="fe81f-112">When users click a toolbar button that uses the [**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md) style, the toolbar control sends its parent window a [TBN\_DROPDOWN](tbn-dropdown.md) notification code.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="fe81f-113">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="fe81f-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="fe81f-114">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="fe81f-114">Technologies</span></span>

-   [<span data-ttu-id="fe81f-115">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="fe81f-115">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="fe81f-116">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fe81f-116">Prerequisites</span></span>

-   <span data-ttu-id="fe81f-117">C/C++</span><span class="sxs-lookup"><span data-stu-id="fe81f-117">C/C++</span></span>
-   <span data-ttu-id="fe81f-118">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="fe81f-118">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="fe81f-119">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="fe81f-119">Instructions</span></span>

### <a name="handle-a-drop-down-button"></a><span data-ttu-id="fe81f-120">Controlar un botón desplegable</span><span class="sxs-lookup"><span data-stu-id="fe81f-120">Handle a Drop-down Button</span></span>

<span data-ttu-id="fe81f-121">En el ejemplo de código siguiente se muestra cómo una aplicación puede admitir un botón desplegable en un control de barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="fe81f-121">The following code example demonstrates how an application can support a drop-down button in a toolbar control.</span></span>


```C++
BOOL DoNotify(HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam)
{

    #define lpnm   ((LPNMHDR)lParam)
    #define lpnmTB ((LPNMTOOLBAR)lParam)

    switch(lpnm->code)
    {
        case TBN_DROPDOWN:
        {
            // Get the coordinates of the button.
            RECT rc;
            SendMessage(lpnmTB->hdr.hwndFrom, TB_GETRECT, (WPARAM)lpnmTB->iItem, (LPARAM)&rc);

            // Convert to screen coordinates.            
            MapWindowPoints(lpnmTB->hdr.hwndFrom, HWND_DESKTOP, (LPPOINT)&rc, 2);                         
        
            // Get the menu.
            HMENU hMenuLoaded = LoadMenu(g_hinst, MAKEINTRESOURCE(IDR_POPUP)); 
         
            // Get the submenu for the first menu item.
            HMENU hPopupMenu = GetSubMenu(hMenuLoaded, 0);

            // Set up the pop-up menu.
            // In case the toolbar is too close to the bottom of the screen, 
            // set rcExclude equal to the button rectangle and the menu will appear above 
            // the button, and not below it.
         
            TPMPARAMS tpm;
         
            tpm.cbSize    = sizeof(TPMPARAMS);
            tpm.rcExclude = rc;
         
            // Show the menu and wait for input. 
            // If the user selects an item, its WM_COMMAND is sent.
         
            TrackPopupMenuEx(hPopupMenu, 
                             TPM_LEFTALIGN | TPM_LEFTBUTTON | TPM_VERTICAL, 
                             rc.left, rc.bottom, g_hwndMain, &tpm);

            DestroyMenu(hMenuLoaded);
         
        return (FALSE);
      
        }
    }
   
    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="fe81f-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fe81f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe81f-123">Usar controles Toolbar</span><span class="sxs-lookup"><span data-stu-id="fe81f-123">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="fe81f-124">[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="fe81f-124">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




