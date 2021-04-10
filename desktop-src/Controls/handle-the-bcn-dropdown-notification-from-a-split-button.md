---
title: Control de las notificaciones de BCN_DROPDOWN de SplitButtons
description: En este tema se describe una posible manera de responder a la \_ notificación de la lista desplegable BCN en un procedimiento de cuadro de diálogo.
ms.assetid: 847DD645-AE29-4F62-BC32-F235BA409E1E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a368dd28c5347f438feff75fbddb129a420caae7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149675"
---
# <a name="how-to-handle-the-bcn_dropdown-notification-from-a-split-button"></a><span data-ttu-id="f7fe3-103">Cómo controlar la \_ notificación de la lista desplegable BCN desde un botón de expansión</span><span class="sxs-lookup"><span data-stu-id="f7fe3-103">How to Handle the BCN\_DROPDOWN Notification from a Split Button</span></span>

<span data-ttu-id="f7fe3-104">En este tema se describe una posible manera de responder a la notificación de la [ \_ lista desplegable BCN](bcn-dropdown.md) en un procedimiento de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f7fe3-104">This topic describes one possible way of responding to the [BCN\_DROPDOWN](bcn-dropdown.md) notification in a dialog procedure.</span></span>

<span data-ttu-id="f7fe3-105">La aplicación de C++ recupera las coordenadas de cliente del botón del encabezado de notificación y las convierte en coordenadas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="f7fe3-105">The C++ application retrieves the client coordinates of the button from the notification header and converts them to screen coordinates.</span></span> <span data-ttu-id="f7fe3-106">Después, crea un menú emergente y lo muestra en la parte inferior del botón.</span><span class="sxs-lookup"><span data-stu-id="f7fe3-106">It then creates a popup menu and displays it at the bottom of the button.</span></span> <span data-ttu-id="f7fe3-107">Para simplificar el ejemplo, los métodos abreviados de teclado no se implementan para el menú.</span><span class="sxs-lookup"><span data-stu-id="f7fe3-107">To keep the example simple, keyboard shortcuts are not implemented for the menu.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="f7fe3-108">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="f7fe3-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="f7fe3-109">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="f7fe3-109">Technologies</span></span>

-   [<span data-ttu-id="f7fe3-110">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="f7fe3-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="f7fe3-111">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f7fe3-111">Prerequisites</span></span>

-   <span data-ttu-id="f7fe3-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="f7fe3-112">C/C++</span></span>
-   <span data-ttu-id="f7fe3-113">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="f7fe3-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="f7fe3-114">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="f7fe3-114">Instructions</span></span>

### <a name="step-1-wait-for-the-bcn_dropdown-notification"></a><span data-ttu-id="f7fe3-115">Paso 1: Espere a la notificación de la *\_ lista desplegable BCN* .</span><span class="sxs-lookup"><span data-stu-id="f7fe3-115">Step 1: Wait for the *BCN\_DROPDOWN* notification.</span></span>


```C++
case BCN_DROPDOWN:
{
    NMBCDROPDOWN* pDropDown = (NMBCDROPDOWN*)lParam;
    if (pDropDown->hdr.hwndFrom = GetDlgItem(hDlg, IDC_SPLIT))
    {
```



### <a name="step-2-get-the-screen-coordinates-of-the-button"></a><span data-ttu-id="f7fe3-116">Paso 2: obtener las coordenadas de pantalla del botón.</span><span class="sxs-lookup"><span data-stu-id="f7fe3-116">Step 2: Get the screen coordinates of the button.</span></span>

<span data-ttu-id="f7fe3-117">Use la función [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) para convertir las coordenadas de la ventana del borde izquierdo inferior del botón en coordenadas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="f7fe3-117">Use the [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) function to convert the window coordinates of the button's lower left edge to screen coordinates.</span></span>


```C++
POINT pt;
pt.x = pDropDown->rcButton.left;
pt.y = pDropDown->rcButton.bottom;
ClientToScreen(pDropDown->hdr.hwndFrom, &pt);
```



### <a name="step-3-create-a-menu-and-add-items"></a><span data-ttu-id="f7fe3-118">Paso 3: crear un menú y agregar elementos.</span><span class="sxs-lookup"><span data-stu-id="f7fe3-118">Step 3: Create a menu and add items.</span></span>

<span data-ttu-id="f7fe3-119">Utilice la función [**CreatePopupMenu**](/windows/desktop/api/winuser/nf-winuser-createpopupmenu) para crear un menú.</span><span class="sxs-lookup"><span data-stu-id="f7fe3-119">Use the [**CreatePopupMenu**](/windows/desktop/api/winuser/nf-winuser-createpopupmenu) function to create a menu.</span></span> <span data-ttu-id="f7fe3-120">Utilice la función [**AppendMenu**](/windows/desktop/menurc/u) para agregar elementos al menú.</span><span class="sxs-lookup"><span data-stu-id="f7fe3-120">Use the [**AppendMenu**](/windows/desktop/menurc/u) function to add items to the menu.</span></span> <span data-ttu-id="f7fe3-121">IDC \_ MENUCOMMAND1 e IDC \_ MENUCOMMAND2 son constantes definidas por la aplicación para los comandos de menú.</span><span class="sxs-lookup"><span data-stu-id="f7fe3-121">IDC\_MENUCOMMAND1 and IDC\_MENUCOMMAND2 are application-defined constants for menu commands.</span></span>


```C++
HMENU hSplitMenu = CreatePopupMenu();
AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND1, L"Menu item 1");
AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND2, L"Menu item 2");
```



### <a name="step-4-display-the-menu"></a><span data-ttu-id="f7fe3-122">Paso 4: mostrar el menú.</span><span class="sxs-lookup"><span data-stu-id="f7fe3-122">Step 4: Display the menu.</span></span>

<span data-ttu-id="f7fe3-123">La función [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) muestra un menú contextual en la ubicación especificada y realiza un seguimiento de la selección de elementos en el menú.</span><span class="sxs-lookup"><span data-stu-id="f7fe3-123">The [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) function displays a shortcut menu at the specified location and tracks the selection of items on the menu.</span></span>


```C++
TrackPopupMenu(hSplitMenu, TPM_LEFTALIGN | TPM_TOPALIGN, pt.x, pt.y, 0, hDlg, NULL);
```



## <a name="complete-example"></a><span data-ttu-id="f7fe3-124">Ejemplo completo</span><span class="sxs-lookup"><span data-stu-id="f7fe3-124">Complete example</span></span>


```C++
case WM_NOTIFY:
    switch (((LPNMHDR)lParam)->code)
    {
        case BCN_DROPDOWN:
        {
            NMBCDROPDOWN* pDropDown = (NMBCDROPDOWN*)lParam;
            if (pDropDown->hdr.hwndFrom = GetDlgItem(hDlg, IDC_SPLIT))
            {

                // Get screen coordinates of the button.
                POINT pt;
                pt.x = pDropDown->rcButton.left;
                pt.y = pDropDown->rcButton.bottom;
                ClientToScreen(pDropDown->hdr.hwndFrom, &pt);
        
                // Create a menu and add items.
                HMENU hSplitMenu = CreatePopupMenu();
                AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND1, L"Menu item 1");
                AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND2, L"Menu item 2");
        
                // Display the menu.
                TrackPopupMenu(hSplitMenu, TPM_LEFTALIGN | TPM_TOPALIGN, pt.x, pt.y, 0, hDlg, NULL);
                return TRUE;
            }
            break;
        }
    }
    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="f7fe3-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f7fe3-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7fe3-126">\_Código de notificación de desplegable BCN</span><span class="sxs-lookup"><span data-stu-id="f7fe3-126">BCN\_DROPDOWN Notification Code</span></span>](bcn-dropdown.md)
</dt> <dt>

[<span data-ttu-id="f7fe3-127">Acerca de los botones</span><span class="sxs-lookup"><span data-stu-id="f7fe3-127">About Buttons</span></span>](about-buttons.md)
</dt> <dt>

[<span data-ttu-id="f7fe3-128">Referencia de control de botón</span><span class="sxs-lookup"><span data-stu-id="f7fe3-128">Button Control Reference</span></span>](bumper-button-button-control-reference.md)
</dt> <dt>

[<span data-ttu-id="f7fe3-129">Usar botones</span><span class="sxs-lookup"><span data-stu-id="f7fe3-129">Using Buttons</span></span>](using-buttons.md)
</dt> <dt>

[<span data-ttu-id="f7fe3-130">Botón</span><span class="sxs-lookup"><span data-stu-id="f7fe3-130">Button</span></span>](buttons.md)
</dt> </dl>

 

 