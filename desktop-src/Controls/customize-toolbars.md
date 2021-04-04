---
title: Cómo personalizar las barras de herramientas
description: La mayoría de las aplicaciones basadas en Windows usan controles de barra de herramientas para proporcionar a los usuarios un acceso cómodo a la funcionalidad del programa.
ms.assetid: 0CE2988E-D887-433B-BFB2-5F3442E8E1B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 091451a139cf846b1106916f28c165d6640699eb
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "104077468"
---
# <a name="how-to-customize-toolbars"></a><span data-ttu-id="bf198-103">Cómo personalizar las barras de herramientas</span><span class="sxs-lookup"><span data-stu-id="bf198-103">How to Customize Toolbars</span></span>

<span data-ttu-id="bf198-104">La mayoría de las aplicaciones basadas en Windows usan controles de barra de herramientas para proporcionar a los usuarios un acceso cómodo a la funcionalidad del programa.</span><span class="sxs-lookup"><span data-stu-id="bf198-104">Most Windows-based applications use toolbar controls to provide users with convenient access to the program functionality.</span></span> <span data-ttu-id="bf198-105">Sin embargo, las barras de herramientas estáticas tienen algunas deficiencias, como un poco de espacio para mostrar eficazmente todas las herramientas disponibles.</span><span class="sxs-lookup"><span data-stu-id="bf198-105">However, static toolbars have some shortcomings—such as too little space to effectively display all the available tools.</span></span> <span data-ttu-id="bf198-106">La solución a este problema consiste en hacer que las barras de herramientas de la aplicación sean personalizables por el usuario.</span><span class="sxs-lookup"><span data-stu-id="bf198-106">The solution to this problem is to make your application's toolbars user-customizable.</span></span> <span data-ttu-id="bf198-107">A continuación, los usuarios pueden elegir mostrar solo las herramientas que necesitan y pueden organizarlas de forma que se adapten a su estilo de estilo personal.</span><span class="sxs-lookup"><span data-stu-id="bf198-107">Then, users can choose to display only the tools they need, and they can organize them in a way that suits their personal workstyle.</span></span>

> [!Note]  
> <span data-ttu-id="bf198-108">Las barras de herramientas de los cuadros de diálogo no se pueden personalizar.</span><span class="sxs-lookup"><span data-stu-id="bf198-108">Toolbars in dialog boxes cannot be customized.</span></span>

 

<span data-ttu-id="bf198-109">Para habilitar la personalización, incluya la marca de estilo de los controles comunes de [**CCS \_ ajustable**](common-control-styles.md) al crear el control de barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="bf198-109">To enable customization, include the [**CCS\_ADJUSTABLE**](common-control-styles.md) common controls style flag when you create the toolbar control.</span></span> <span data-ttu-id="bf198-110">Hay dos enfoques básicos para la personalización:</span><span class="sxs-lookup"><span data-stu-id="bf198-110">There are two basic approaches to customization:</span></span>

-   <span data-ttu-id="bf198-111">Cuadro de diálogo de personalización.</span><span class="sxs-lookup"><span data-stu-id="bf198-111">The customization dialog box.</span></span> <span data-ttu-id="bf198-112">Este cuadro de diálogo proporcionado por el sistema es el enfoque más sencillo.</span><span class="sxs-lookup"><span data-stu-id="bf198-112">This system-provided dialog box is the simplest approach.</span></span> <span data-ttu-id="bf198-113">Ofrece a los usuarios una interfaz gráfica de usuario que les permite agregar, eliminar o mover iconos.</span><span class="sxs-lookup"><span data-stu-id="bf198-113">It gives users a graphical user interface that allows them to add, delete, or move icons.</span></span>
-   <span data-ttu-id="bf198-114">Arrastrar y colocar herramientas.</span><span class="sxs-lookup"><span data-stu-id="bf198-114">Dragging and dropping tools.</span></span> <span data-ttu-id="bf198-115">La implementación de la funcionalidad de arrastrar y colocar permite a los usuarios mover herramientas a otra ubicación de la barra de herramientas o eliminarlas arrastrándolas fuera de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="bf198-115">Implementing drag-and-drop functionality allows users to move tools to another location on the toolbar or delete them by dragging them off the toolbar.</span></span> <span data-ttu-id="bf198-116">Proporciona a los usuarios una manera rápida y sencilla de organizar su barra de herramientas, pero no les permite agregar herramientas.</span><span class="sxs-lookup"><span data-stu-id="bf198-116">It provides users a quick and easy way to organize their toolbar, but does not allow them to add tools.</span></span>

<span data-ttu-id="bf198-117">Puede implementar cualquier enfoque o ambos, en función de las necesidades de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bf198-117">You can implement either approach or both, depending on the needs of the application.</span></span> <span data-ttu-id="bf198-118">Ninguno de estos dos enfoques para la personalización proporciona un mecanismo integrado, como un botón Cancelar o deshacer, para devolver la barra de herramientas a su estado anterior.</span><span class="sxs-lookup"><span data-stu-id="bf198-118">Neither of these two approaches to customization provides a built-in mechanism, such as a Cancel or Undo button, to return the toolbar to its former state.</span></span> <span data-ttu-id="bf198-119">Debe utilizar explícitamente la API de control de barra de herramientas para almacenar el estado de prepersonalización de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="bf198-119">You must explicitly use the toolbar control API to store the toolbar's precustomization state.</span></span> <span data-ttu-id="bf198-120">Si es necesario, puede utilizar posteriormente esta información almacenada para restaurar la barra de herramientas a su estado original.</span><span class="sxs-lookup"><span data-stu-id="bf198-120">If necessary, you can later use this stored information to restore the toolbar to its original state.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="bf198-121">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="bf198-121">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="bf198-122">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="bf198-122">Technologies</span></span>

-   [<span data-ttu-id="bf198-123">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="bf198-123">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="bf198-124">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bf198-124">Prerequisites</span></span>

-   <span data-ttu-id="bf198-125">C/C++</span><span class="sxs-lookup"><span data-stu-id="bf198-125">C/C++</span></span>
-   <span data-ttu-id="bf198-126">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="bf198-126">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="bf198-127">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="bf198-127">Instructions</span></span>

### <a name="customization-dialog-box"></a><span data-ttu-id="bf198-128">Cuadro de diálogo Personalización</span><span class="sxs-lookup"><span data-stu-id="bf198-128">Customization Dialog Box</span></span>

<span data-ttu-id="bf198-129">El cuadro de diálogo de personalización lo proporciona el control de barra de herramientas para proporcionar a los usuarios una manera sencilla de agregar, quitar o eliminar herramientas.</span><span class="sxs-lookup"><span data-stu-id="bf198-129">The customization dialog box is provided by the toolbar control to give users a simple way to add, move, or delete tools.</span></span> <span data-ttu-id="bf198-130">Los usuarios pueden iniciarlo haciendo doble clic en la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="bf198-130">Users can launch it by double-clicking the toolbar.</span></span> <span data-ttu-id="bf198-131">Las aplicaciones pueden iniciar el cuadro de diálogo de personalización mediante programación enviando el control de barra de herramientas a un mensaje de [**\_ Personalización de TB**](tb-customize.md) .</span><span class="sxs-lookup"><span data-stu-id="bf198-131">Applications can launch the customization dialog box programmatically by sending the toolbar control a [**TB\_CUSTOMIZE**](tb-customize.md) message.</span></span>

<span data-ttu-id="bf198-132">En la ilustración siguiente se muestra un ejemplo del cuadro de diálogo de personalización de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="bf198-132">The following illustration shows an example of the toolbar customization dialog box.</span></span>

![captura de pantalla de una ventana con una barra de herramientas de tres elementos y un cuadro de diálogo con listas de los botones de la barra de herramientas disponibles y actuales](images/tb-customdlg.png)

<span data-ttu-id="bf198-134">Las herramientas del cuadro de lista de la derecha son las que están actualmente en la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="bf198-134">The tools in the list box on the right are those currently on the toolbar.</span></span> <span data-ttu-id="bf198-135">Inicialmente, esta lista contendrá las herramientas que se especifican al crear la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="bf198-135">Initially, this list will contain the tools that you specify when you create the toolbar.</span></span> <span data-ttu-id="bf198-136">El cuadro de lista de la izquierda contiene las herramientas que están disponibles para agregarse a la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="bf198-136">The list box in the left contains the tools that are available to add to the toolbar.</span></span> <span data-ttu-id="bf198-137">La aplicación es responsable de rellenar esa lista (excepto con el separador, que aparece automáticamente).</span><span class="sxs-lookup"><span data-stu-id="bf198-137">Your application is responsible for populating that list (other than with the Separator, which appears automatically).</span></span>

<span data-ttu-id="bf198-138">El control de barra de herramientas notifica a la aplicación que está iniciando un cuadro de diálogo de personalización mediante el envío de su ventana primaria a un código de notificación [TBN \_ BEGINADJUST](tbn-beginadjust.md) seguido de un código de notificación [TBN \_ INITCUSTOMIZE](tbn-initcustomize.md) .</span><span class="sxs-lookup"><span data-stu-id="bf198-138">The toolbar control notifies your application that it is launching a customization dialog box by sending its parent window a [TBN\_BEGINADJUST](tbn-beginadjust.md) notification code followed by a [TBN\_INITCUSTOMIZE](tbn-initcustomize.md) notification code.</span></span> <span data-ttu-id="bf198-139">En la mayoría de los casos, la aplicación no necesita responder a estos códigos de notificación.</span><span class="sxs-lookup"><span data-stu-id="bf198-139">In most cases, the application does not need to respond to these notification codes.</span></span> <span data-ttu-id="bf198-140">Sin embargo, si no desea que el cuadro de diálogo Personalizar barra de herramientas muestre un botón ayuda, controle TBN \_ INITCUSTOMIZE devolviendo TBNRF \_ HIDEHELP.</span><span class="sxs-lookup"><span data-stu-id="bf198-140">However, if you do not want the Customize Toolbar dialog box to display a Help button, handle TBN\_INITCUSTOMIZE by returning TBNRF\_HIDEHELP.</span></span>

<span data-ttu-id="bf198-141">A continuación, el control de barra de herramientas recopila la información que necesita para inicializar el cuadro de diálogo mediante el envío de tres series de códigos de notificación, en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="bf198-141">The toolbar control then collects the information it needs to initialize the dialog box by sending three series of notification codes, in the following order:</span></span>

-   <span data-ttu-id="bf198-142">Un código de notificación de [TBN \_ QUERYINSERT](tbn-queryinsert.md) para cada botón de la barra de herramientas para determinar dónde se pueden insertar los botones.</span><span class="sxs-lookup"><span data-stu-id="bf198-142">A [TBN\_QUERYINSERT](tbn-queryinsert.md) notification code for each button on the toolbar to determine where buttons can be inserted.</span></span> <span data-ttu-id="bf198-143">Devuelve **false** para evitar que un botón se inserte a la izquierda del botón especificado en el mensaje de notificación.</span><span class="sxs-lookup"><span data-stu-id="bf198-143">Return **FALSE** to prevent a button from being inserted to the left of the button specified in the notification message.</span></span> <span data-ttu-id="bf198-144">Si devuelve **false** a todos los códigos de notificación de TBN \_ QUERYINSERT, no se mostrará el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="bf198-144">If you return **FALSE** to all TBN\_QUERYINSERT notification codes, the dialog box will not be displayed.</span></span>
-   <span data-ttu-id="bf198-145">Un código de notificación de [TBN \_ QUERYDELETE](tbn-querydelete.md) para cada herramienta que se encuentra actualmente en la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="bf198-145">A [TBN\_QUERYDELETE](tbn-querydelete.md) notification code for each tool that is currently on the toolbar.</span></span> <span data-ttu-id="bf198-146">Devuelve **true** si se puede eliminar una herramienta o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bf198-146">Return **TRUE** if a tool can be deleted, or **FALSE** if not.</span></span>
-   <span data-ttu-id="bf198-147">Una serie de códigos de notificación de [ \_ GETBUTTONINFO de TBN](tbn-getbuttoninfo.md) para rellenar la lista de botones disponibles.</span><span class="sxs-lookup"><span data-stu-id="bf198-147">A series of [TBN\_GETBUTTONINFO](tbn-getbuttoninfo.md) notification codes to populate the list of available buttons.</span></span> <span data-ttu-id="bf198-148">Para agregar un botón a la lista, rellene la estructura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) que se pasa con el código de notificación y devuelva **true**.</span><span class="sxs-lookup"><span data-stu-id="bf198-148">To add a button to the list, fill in the [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure that is passed with the notification code and return **TRUE**.</span></span> <span data-ttu-id="bf198-149">Si no tiene más herramientas para agregar, devuelva **false**.</span><span class="sxs-lookup"><span data-stu-id="bf198-149">When you have no more tools to add, return **FALSE**.</span></span> <span data-ttu-id="bf198-150">Tenga en cuenta que puede devolver información de los botones que ya están en la barra de herramientas; Estos botones no se agregarán a la lista.</span><span class="sxs-lookup"><span data-stu-id="bf198-150">Note that you can return information for buttons that are already on the toolbar; these buttons will not be added to the list.</span></span>

<span data-ttu-id="bf198-151">A continuación, se muestra el cuadro de diálogo y el usuario puede empezar a personalizar la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="bf198-151">The dialog box is then displayed, and the user can begin to customize the toolbar.</span></span>

<span data-ttu-id="bf198-152">Cuando el cuadro de diálogo está abierto, la aplicación puede recibir diversos códigos de notificación, en función de las acciones del usuario:</span><span class="sxs-lookup"><span data-stu-id="bf198-152">When the dialog box is open, your application can receive a variety of notification codes, depending on the user's actions:</span></span>

-   <span data-ttu-id="bf198-153">[TBN \_ QUERYINSERT](tbn-queryinsert.md).</span><span class="sxs-lookup"><span data-stu-id="bf198-153">[TBN\_QUERYINSERT](tbn-queryinsert.md).</span></span> <span data-ttu-id="bf198-154">El usuario ha cambiado la ubicación de una herramienta en la barra de herramientas o ha agregado una herramienta.</span><span class="sxs-lookup"><span data-stu-id="bf198-154">The user has changed the location of a tool on the toolbar or added a tool.</span></span> <span data-ttu-id="bf198-155">Devuelve **false** para evitar que la herramienta se inserte en esa ubicación.</span><span class="sxs-lookup"><span data-stu-id="bf198-155">Return **FALSE** to prevent the tool from being inserted at that location.</span></span>
-   <span data-ttu-id="bf198-156">[TBN \_ DELETINGBUTTON](tbn-deletingbutton.md).</span><span class="sxs-lookup"><span data-stu-id="bf198-156">[TBN\_DELETINGBUTTON](tbn-deletingbutton.md).</span></span> <span data-ttu-id="bf198-157">El usuario está a punto de quitar una herramienta de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="bf198-157">The user is about to remove a tool from the toolbar.</span></span>
-   <span data-ttu-id="bf198-158">[TBN \_ CUSTHELP](tbn-custhelp.md).</span><span class="sxs-lookup"><span data-stu-id="bf198-158">[TBN\_CUSTHELP](tbn-custhelp.md).</span></span> <span data-ttu-id="bf198-159">El usuario hizo clic en el botón ayuda.</span><span class="sxs-lookup"><span data-stu-id="bf198-159">The user has clicked the Help button.</span></span>
-   <span data-ttu-id="bf198-160">[TBN \_ TOOLBARCHANGE](tbn-toolbarchange.md).</span><span class="sxs-lookup"><span data-stu-id="bf198-160">[TBN\_TOOLBARCHANGE](tbn-toolbarchange.md).</span></span> <span data-ttu-id="bf198-161">El usuario ha agregado, cambiado o eliminado una herramienta.</span><span class="sxs-lookup"><span data-stu-id="bf198-161">The user has added, moved, or deleted a tool.</span></span>
-   <span data-ttu-id="bf198-162">[TBN \_ RESTABLECER](tbn-reset.md).</span><span class="sxs-lookup"><span data-stu-id="bf198-162">[TBN\_RESET](tbn-reset.md).</span></span> <span data-ttu-id="bf198-163">El usuario hizo clic en el botón Restablecer.</span><span class="sxs-lookup"><span data-stu-id="bf198-163">The user has clicked the Reset button.</span></span>

<span data-ttu-id="bf198-164">Una vez destruido el cuadro de diálogo, la aplicación recibirá un código de notificación [TBN \_ ENDADJUST](tbn-endadjust.md) .</span><span class="sxs-lookup"><span data-stu-id="bf198-164">After the dialog box is destroyed, your application will receive a [TBN\_ENDADJUST](tbn-endadjust.md) notification code.</span></span>

<span data-ttu-id="bf198-165">En el ejemplo de código siguiente se muestra una manera de implementar la personalización de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="bf198-165">The following code example shows one way to implement toolbar customization.</span></span>


```C++
// The buttons are stored in an array of TBBUTTON structures. 
//
// Constants such as STD_FILENEW are identifiers for the 
// built-in bitmaps that have already been assigned as the toolbar's 
// image list.
//
// Constants such as IDM_NEW are application-defined command identifiers.

TBBUTTON allButtons[] = 
    {
        { MAKELONG(STD_FILENEW,  ImageListID), IDM_NEW,   TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"New" },
        { MAKELONG(STD_FILEOPEN, ImageListID), IDM_OPEN,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Open"},
        { MAKELONG(STD_FILESAVE, ImageListID), IDM_SAVE,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Save"},
        { MAKELONG(STD_CUT,      ImageListID), IDM_CUT,   TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Cut" },
        { MAKELONG(STD_COPY,     ImageListID), IDM_COPY,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Copy"},
        { MAKELONG(STD_PASTE,    ImageListID), IDM_PASTE, TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Paste"}
    };

// The following appears in the window's message handler.

case WM_NOTIFY: 
    {
        switch (((LPNMHDR)lParam)->code) 
        {
        
        case TBN_GETBUTTONINFO:  
            {
                LPTBNOTIFY lpTbNotify = (LPTBNOTIFY)lParam;

                // Pass the next button from the array. There is no need to filter out buttons
                // that are already used—they will be ignored.
                
                int buttonCount = sizeof(allButtons) / sizeof(TBBUTTON);
                
                if (lpTbNotify->iItem < buttonCount)
                {
                    lpTbNotify->tbButton = allButtons[lpTbNotify->iItem];
                    return TRUE;
                }
                
                else
                
                {
                    return FALSE;  // No more buttons.
                }
            }
            
            break;

            case TBN_QUERYINSERT:
            
            case TBN_QUERYDELETE:
                return TRUE; 
        }
    }
```



### <a name="dragging-and-dropping-tools"></a><span data-ttu-id="bf198-166">Arrastrar y colocar herramientas</span><span class="sxs-lookup"><span data-stu-id="bf198-166">Dragging and Dropping Tools</span></span>

<span data-ttu-id="bf198-167">Los usuarios también pueden reorganizar los botones de una barra de herramientas presionando la tecla Mayús y arrastrando el botón hasta otra ubicación.</span><span class="sxs-lookup"><span data-stu-id="bf198-167">Users can also rearrange the buttons on a toolbar by pressing the SHIFT key and dragging the button to another location.</span></span> <span data-ttu-id="bf198-168">El proceso de arrastrar y colocar se controla automáticamente mediante el control de barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="bf198-168">The drag-and-drop process is handled automatically by the toolbar control.</span></span> <span data-ttu-id="bf198-169">Muestra una imagen fantasma del botón mientras se arrastra y reorganiza la barra de herramientas después de quitarla.</span><span class="sxs-lookup"><span data-stu-id="bf198-169">It displays a ghost image of the button as it is dragged, and rearranges the toolbar after it is dropped.</span></span> <span data-ttu-id="bf198-170">Los usuarios no pueden agregar botones de esta manera, pero pueden eliminar un botón colocándolo fuera de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="bf198-170">Users cannot add buttons in this way, but they can delete a button by dropping it off the toolbar.</span></span>

<span data-ttu-id="bf198-171">Aunque el control de barra de herramientas realiza normalmente esta operación automáticamente, también envía la aplicación dos códigos de notificación: [TBN \_ QUERYDELETE](tbn-querydelete.md) y [TBN \_ QUERYINSERT](tbn-queryinsert.md).</span><span class="sxs-lookup"><span data-stu-id="bf198-171">Although the toolbar control normally does this operation automatically, it also sends your application two notification codes: [TBN\_QUERYDELETE](tbn-querydelete.md) and [TBN\_QUERYINSERT](tbn-queryinsert.md).</span></span> <span data-ttu-id="bf198-172">Para controlar el proceso de arrastrar y colocar, controle estos códigos de notificación de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="bf198-172">To control the drag-and-drop process, handle these notification codes as follows:</span></span>

-   <span data-ttu-id="bf198-173">El código de notificación [TBN \_ QUERYDELETE](tbn-querydelete.md) se envía tan pronto como el usuario intenta quitar el botón, antes de que se muestre el botón fantasma.</span><span class="sxs-lookup"><span data-stu-id="bf198-173">The [TBN\_QUERYDELETE](tbn-querydelete.md) notification code is sent as soon as the user attempts to move the button, before the ghost button is displayed.</span></span> <span data-ttu-id="bf198-174">Devuelve **false** para evitar que el botón se mueva.</span><span class="sxs-lookup"><span data-stu-id="bf198-174">Return **FALSE** to prevent the button from being moved.</span></span> <span data-ttu-id="bf198-175">Si devuelve **true**, el usuario podrá quitar la herramienta o eliminarla colocándolo fuera de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="bf198-175">If you return **TRUE**, the user will be able to either move the tool or delete it by dropping it off the toolbar.</span></span> <span data-ttu-id="bf198-176">Si se puede moverse una herramienta, puede eliminarse.</span><span class="sxs-lookup"><span data-stu-id="bf198-176">If a tool can be moved, it can be deleted.</span></span> <span data-ttu-id="bf198-177">Sin embargo, si el usuario elimina una herramienta, el control de barra de herramientas enviará a la aplicación un código de notificación [TBN \_ DELETINGBUTTON](tbn-deletingbutton.md) , momento en el cual podrá optar por volver a insertar el botón en su ubicación original, con lo que se cancelará la eliminación.</span><span class="sxs-lookup"><span data-stu-id="bf198-177">However, if the user deletes a tool, the toolbar control will send your application a [TBN\_DELETINGBUTTON](tbn-deletingbutton.md) notification code, at which point you can choose to reinsert the button at its original location, thereby canceling the deletion.</span></span>
-   <span data-ttu-id="bf198-178">El código de notificación [ \_ QUERYINSERT de TBN](tbn-queryinsert.md) se envía cuando el usuario intenta quitar el botón de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="bf198-178">The [TBN\_QUERYINSERT](tbn-queryinsert.md) notification code is sent when the user attempts to drop the button on the toolbar.</span></span> <span data-ttu-id="bf198-179">Para evitar que el botón que se está moviendo a la izquierda del botón especificado en la notificación, devuelva **false**.</span><span class="sxs-lookup"><span data-stu-id="bf198-179">To prevent the button that is being moved from being dropped to the left of the button specified in the notification, return **FALSE**.</span></span> <span data-ttu-id="bf198-180">Este código de notificación no se envía si el usuario quita la herramienta de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="bf198-180">This notification code is not sent if the user drops the tool off the toolbar.</span></span>

<span data-ttu-id="bf198-181">Si el usuario intenta arrastrar un botón sin presionar también la tecla Mayús, el control de barra de herramientas no controlará la operación de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="bf198-181">If the user attempts to drag a button without also pressing the SHIFT key, the toolbar control will not handle the drag-and-drop operation.</span></span> <span data-ttu-id="bf198-182">Sin embargo, enviará a la aplicación un código de notificación [TBN \_ BEGINDRAG](tbn-begindrag.md) para indicar el inicio de una operación de arrastre y un código de notificación de [TBN \_ ENDDRAG](tbn-enddrag.md) para indicar el final.</span><span class="sxs-lookup"><span data-stu-id="bf198-182">However, it will send your application a [TBN\_BEGINDRAG](tbn-begindrag.md) notification code to indicate the start of a drag operation, and a [TBN\_ENDDRAG](tbn-enddrag.md) notification code to indicate the end.</span></span> <span data-ttu-id="bf198-183">Si desea habilitar esta forma de arrastrar y colocar, la aplicación debe controlar estos códigos de notificación, proporcionar la interfaz de usuario necesaria y modificar la barra de herramientas para reflejar los cambios.</span><span class="sxs-lookup"><span data-stu-id="bf198-183">If you want to enable this form of drag-and-drop, your application must handle these notification codes, provide the necessary user interface, and modify the toolbar to reflect any changes.</span></span>

### <a name="saving-and-restoring-toolbars"></a><span data-ttu-id="bf198-184">Guardar y restaurar barras de herramientas</span><span class="sxs-lookup"><span data-stu-id="bf198-184">Saving and Restoring Toolbars</span></span>

<span data-ttu-id="bf198-185">En el proceso de personalización de una barra de herramientas, es posible que la aplicación tenga que guardar la información para que pueda restaurar la barra de herramientas a su estado original.</span><span class="sxs-lookup"><span data-stu-id="bf198-185">In the process of customizing a toolbar, your application might need to save information so that you can restore the toolbar to its original state.</span></span> <span data-ttu-id="bf198-186">Para iniciar el guardado o la restauración de un estado de la barra de herramientas, envíe el control de barra de herramientas a un mensaje de [**TB \_ SAVERESTORE**](tb-saverestore.md) con el valor de *lParam* establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="bf198-186">To initiate saving or restoring a toolbar state, send the toolbar control a [**TB\_SAVERESTORE**](tb-saverestore.md) message with the *lParam* set to **TRUE**.</span></span> <span data-ttu-id="bf198-187">El valor *lParam* de este mensaje especifica si se solicita una operación de guardar o de restauración.</span><span class="sxs-lookup"><span data-stu-id="bf198-187">The *lParam* value of this message specifies whether you are requesting a save or a restore operation.</span></span> <span data-ttu-id="bf198-188">Una vez enviado el mensaje, hay dos formas de controlar la operación de guardar y restaurar:</span><span class="sxs-lookup"><span data-stu-id="bf198-188">After the message is sent, there are two ways to handle the save/restore operation:</span></span>

-   <span data-ttu-id="bf198-189">Con los controles comunes [versión 4,72](common-control-versions.md) y versiones anteriores, debe implementar un controlador de [ \_ GETBUTTONINFO de TBN](tbn-getbuttoninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="bf198-189">With common controls [version 4.72](common-control-versions.md) and earlier, you must implement a [TBN\_GETBUTTONINFO](tbn-getbuttoninfo.md) handler.</span></span> <span data-ttu-id="bf198-190">El control de barra de herramientas envía este código de notificación para solicitar información sobre cada botón a medida que se restaura.</span><span class="sxs-lookup"><span data-stu-id="bf198-190">The toolbar control sends this notification code to request information about each button as it is restored.</span></span>
-   <span data-ttu-id="bf198-191">La versión 5,80 incluye una opción guardar/restaurar.</span><span class="sxs-lookup"><span data-stu-id="bf198-191">Version 5.80 includes a save/restore option.</span></span> <span data-ttu-id="bf198-192">Al principio del proceso y, a medida que se guarda o se restaura cada botón, la aplicación recibirá un código de notificación [TBN \_ Save](tbn-save.md) o [TBN \_ restore](tbn-restore.md) .</span><span class="sxs-lookup"><span data-stu-id="bf198-192">At the beginning of the process, and as each button is saved or restored, your application will receive a [TBN\_SAVE](tbn-save.md) or [TBN\_RESTORE](tbn-restore.md) notification code.</span></span> <span data-ttu-id="bf198-193">Para usar esta opción, debe implementar controladores de notificación para proporcionar el mapa de bits y la información de estado necesaria para guardar o restaurar correctamente el estado de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="bf198-193">To use this option, you must implement notification handlers to provide the bitmap and state information that is needed to successfully save or restore the toolbar state.</span></span>

<span data-ttu-id="bf198-194">Los Estados de la barra de herramientas se guardan en un flujo de datos que consta de bloques de datos definidos por el shell que alternan con bloques de datos definidos por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bf198-194">Toolbar states are saved in a data stream that consists of blocks of Shell-defined data alternating with blocks of application-defined data.</span></span> <span data-ttu-id="bf198-195">Un bloque de datos de cada tipo se almacena para cada botón, junto con un bloque opcional de datos globales que las aplicaciones pueden colocar al principio de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="bf198-195">One data block of each type is stored for each button, along with an optional block of global data that applications can place at the beginning of the stream.</span></span> <span data-ttu-id="bf198-196">Durante el proceso de almacenamiento, el controlador de [ \_ guardado de TBN](tbn-save.md) agrega los bloques definidos por la aplicación al flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="bf198-196">During the save process, your [TBN\_SAVE](tbn-save.md) handler adds the application-defined blocks to the data stream.</span></span> <span data-ttu-id="bf198-197">Durante el proceso de restauración, el controlador de [ \_ restauración TBN](tbn-restore.md) Lee cada bloque y proporciona al shell la información que necesita para reconstruir la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="bf198-197">During the restore process, the [TBN\_RESTORE](tbn-restore.md) handler reads each block and gives the Shell the information it needs to reconstruct the toolbar.</span></span>

### <a name="how-to-handle-a-tbn_save-notification"></a><span data-ttu-id="bf198-198">Cómo controlar una notificación de \_ guardado de TBN</span><span class="sxs-lookup"><span data-stu-id="bf198-198">How to Handle a TBN\_SAVE Notification</span></span>

<span data-ttu-id="bf198-199">El primer código de notificación de [ \_ guardar de TBN](tbn-save.md) se envía al principio del proceso de guardar.</span><span class="sxs-lookup"><span data-stu-id="bf198-199">The first [TBN\_SAVE](tbn-save.md) notification code is sent at the beginning of the save process.</span></span> <span data-ttu-id="bf198-200">Antes de guardar cualquier botón, los miembros de la estructura [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) se establecen como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="bf198-200">Before any buttons are saved, the members of the [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) structure are set as shown in the following table.</span></span>



| <span data-ttu-id="bf198-201">Miembro</span><span class="sxs-lookup"><span data-stu-id="bf198-201">Member</span></span>       | <span data-ttu-id="bf198-202">Configuración</span><span class="sxs-lookup"><span data-stu-id="bf198-202">Setting</span></span>                                                                                                                                                                                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf198-203">**iItem**</span><span class="sxs-lookup"><span data-stu-id="bf198-203">**iItem**</span></span>    | <span data-ttu-id="bf198-204">–1</span><span class="sxs-lookup"><span data-stu-id="bf198-204">–1</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="bf198-205">**cbData**</span><span class="sxs-lookup"><span data-stu-id="bf198-205">**cbData**</span></span>   | <span data-ttu-id="bf198-206">Cantidad de memoria necesaria para los datos definidos por el shell.</span><span class="sxs-lookup"><span data-stu-id="bf198-206">The amount of memory needed for Shell-defined data.</span></span>                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="bf198-207">**cButtons**</span><span class="sxs-lookup"><span data-stu-id="bf198-207">**cButtons**</span></span> | <span data-ttu-id="bf198-208">Número de botones.</span><span class="sxs-lookup"><span data-stu-id="bf198-208">The number of buttons.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="bf198-209">**pData**</span><span class="sxs-lookup"><span data-stu-id="bf198-209">**pData**</span></span>    | <span data-ttu-id="bf198-210">Cantidad calculada de memoria necesaria para los datos definidos por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bf198-210">The calculated amount of memory needed for application-defined data.</span></span> <span data-ttu-id="bf198-211">Normalmente, se incluyen algunos datos globales, además de los datos de cada botón.</span><span class="sxs-lookup"><span data-stu-id="bf198-211">Typically, you include some global data, plus data for each button.</span></span> <span data-ttu-id="bf198-212">Agregue ese valor a **cbData** y asigne suficiente memoria a **pdata** para mantenerlo todo.</span><span class="sxs-lookup"><span data-stu-id="bf198-212">Add that value to **cbData** and allocate enough memory to **pData** to hold it all.</span></span>                                                                                                                      |
| <span data-ttu-id="bf198-213">**pCurrent**</span><span class="sxs-lookup"><span data-stu-id="bf198-213">**pCurrent**</span></span> | <span data-ttu-id="bf198-214">Primer byte no utilizado en el flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="bf198-214">The first unused byte in the data stream.</span></span> <span data-ttu-id="bf198-215">Si no necesita información de la barra de herramientas global, establezca **pCurrent**  =  **pdata** para que apunte al inicio del flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="bf198-215">If you do not require global toolbar information, set **pCurrent** = **pData** so that it points to the start of the data stream.</span></span> <span data-ttu-id="bf198-216">Si requiere información de la barra de herramientas global, almacénela en **pdata** y, a continuación, establezca **pCurrent** en el principio de la parte sin usar del flujo de datos antes de volver.</span><span class="sxs-lookup"><span data-stu-id="bf198-216">If you do require global toolbar information, store it at **pData**, then set **pCurrent** to the beginning of the unused portion of the data stream before returning.</span></span> |



 

<span data-ttu-id="bf198-217">Si desea agregar información de la barra de herramientas global, colóquela al principio del flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="bf198-217">If you want to add some global toolbar information, put it at the start of the data stream.</span></span> <span data-ttu-id="bf198-218">Avance **pCurrent** hasta el final de los datos globales para que apunte al principio de la parte sin usar del flujo de datos y devuelva.</span><span class="sxs-lookup"><span data-stu-id="bf198-218">Advance **pCurrent** to the end of the global data so that it points to the beginning of the unused portion of the data stream, and return.</span></span>

<span data-ttu-id="bf198-219">Después de devolver, el shell comienza a guardar la información del botón.</span><span class="sxs-lookup"><span data-stu-id="bf198-219">After you return, the Shell starts saving button information.</span></span> <span data-ttu-id="bf198-220">Agrega los datos definidos por el shell para el primer botón en **pCurrent** y, a continuación, avanza **pCurrent** al principio de la parte no utilizada.</span><span class="sxs-lookup"><span data-stu-id="bf198-220">It adds the Shell-defined data for the first button at **pCurrent** and then advances **pCurrent** to the start of the unused portion.</span></span>

<span data-ttu-id="bf198-221">Después de guardar cada botón, se envía un código de notificación [TBN \_ Guardar](tbn-save.md) y se devuelve [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) con estos miembros establecidos como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="bf198-221">After each button is saved, a [TBN\_SAVE](tbn-save.md) notification code is sent and [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) is returned with these members set as follows.</span></span>



| <span data-ttu-id="bf198-222">Miembro</span><span class="sxs-lookup"><span data-stu-id="bf198-222">Member</span></span>                       | <span data-ttu-id="bf198-223">Configuración</span><span class="sxs-lookup"><span data-stu-id="bf198-223">Setting</span></span>                                                                                                                                                                                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf198-224">**iItem**</span><span class="sxs-lookup"><span data-stu-id="bf198-224">**iItem**</span></span>                    | <span data-ttu-id="bf198-225">Índice de base cero del número de botón.</span><span class="sxs-lookup"><span data-stu-id="bf198-225">The zero-based index of the button number.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="bf198-226">**pCurrent**</span><span class="sxs-lookup"><span data-stu-id="bf198-226">**pCurrent**</span></span>                 | <span data-ttu-id="bf198-227">Puntero al primer byte no utilizado en el flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="bf198-227">A pointer to the first unused byte in the data stream.</span></span> <span data-ttu-id="bf198-228">Si desea almacenar información adicional sobre el botón, almacénelo en la ubicación a la que señala **pCurrent** y actualice **pCurrent** para que apunte a la primera parte sin usar del flujo de datos después.</span><span class="sxs-lookup"><span data-stu-id="bf198-228">If you want to store additional information about the button, store it at the location pointed to by **pCurrent** and update **pCurrent** to point to the first unused portion of the data stream after that.</span></span> |
| [<span data-ttu-id="bf198-229">**TBBUTTON**</span><span class="sxs-lookup"><span data-stu-id="bf198-229">**TBBUTTON**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) | <span data-ttu-id="bf198-230">Estructura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) que describe el botón que se va a guardar.</span><span class="sxs-lookup"><span data-stu-id="bf198-230">A [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure that describes the button that is being saved.</span></span>                                                                                                                                                                              |



 

<span data-ttu-id="bf198-231">Cuando reciba el código de notificación, debe extraer cualquier información específica del botón que necesite de [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton).</span><span class="sxs-lookup"><span data-stu-id="bf198-231">When you receive the notification code, you should extract any button-specific information you need from [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton).</span></span> <span data-ttu-id="bf198-232">Recuerde que al agregar un botón, puede usar el miembro **dwData** de **TBBUTTON** para almacenar los datos específicos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bf198-232">Remember that when you add a button, you can use the **dwData** member of **TBBUTTON** to hold application-specific data.</span></span> <span data-ttu-id="bf198-233">Cargue los datos en el flujo de datos en **pCurrent**.</span><span class="sxs-lookup"><span data-stu-id="bf198-233">Load your data into the data stream at **pCurrent**.</span></span> <span data-ttu-id="bf198-234">Avance **pCurrent** hasta el final de los datos, señalando de nuevo al principio de la parte no utilizada del flujo y devuelva.</span><span class="sxs-lookup"><span data-stu-id="bf198-234">Advance **pCurrent** to the end of your data, again pointing to the beginning of the unused portion of the stream, and return.</span></span>

<span data-ttu-id="bf198-235">A continuación, el shell va al botón siguiente, agrega su información a **pdata**, avanza **PCurrent**, carga [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)y envía otro código de notificación [TBN \_ Guardar](tbn-save.md) .</span><span class="sxs-lookup"><span data-stu-id="bf198-235">The Shell then goes to the next button, adds its information to **pData**, advances **pCurrent**, loads [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton), and sends another [TBN\_SAVE](tbn-save.md) notification code.</span></span> <span data-ttu-id="bf198-236">Este proceso continúa hasta que se guardan todos los botones.</span><span class="sxs-lookup"><span data-stu-id="bf198-236">This process continues until all buttons are saved.</span></span>

### <a name="restoring-saved-toolbars"></a><span data-ttu-id="bf198-237">Restaurar barras de herramientas guardadas</span><span class="sxs-lookup"><span data-stu-id="bf198-237">Restoring Saved Toolbars</span></span>

<span data-ttu-id="bf198-238">Básicamente, el proceso de restauración invierte el proceso de guardar.</span><span class="sxs-lookup"><span data-stu-id="bf198-238">The restore process basically reverses the save process.</span></span> <span data-ttu-id="bf198-239">Al principio, la aplicación recibirá un código de notificación [TBN \_ restore](tbn-restore.md) con el miembro **IItem** de la estructura [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) establecido en – 1.</span><span class="sxs-lookup"><span data-stu-id="bf198-239">At the beginning, your application will receive a [TBN\_RESTORE](tbn-restore.md) notification code with the **iItem** member of the [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) structure set to –1.</span></span> <span data-ttu-id="bf198-240">El miembro **cbData** se establece en el tamaño de **pdata** y **cButtons** se establece en el número de botones.</span><span class="sxs-lookup"><span data-stu-id="bf198-240">The **cbData** member is set to the size of **pData**, and **cButtons** is set to the number of buttons.</span></span>

<span data-ttu-id="bf198-241">El controlador de notificación debe extraer la información global que se colocó al principio de **pdata** durante el guardado y avanzar **pCurrent** al principio del primer bloque de datos definidos por el shell.</span><span class="sxs-lookup"><span data-stu-id="bf198-241">Your notification handler should extract the global information that was placed at the beginning of **pData** during the save, and advance **pCurrent** to the start of the first block of Shell-defined data.</span></span> <span data-ttu-id="bf198-242">Establezca **cBytesPerRecord** en el tamaño de los bloques de datos que usó para guardar los datos del botón.</span><span class="sxs-lookup"><span data-stu-id="bf198-242">Set **cBytesPerRecord** to the size of the data blocks you used to save the button data.</span></span> <span data-ttu-id="bf198-243">Establezca **cButtons** en el número de botones y devuelva.</span><span class="sxs-lookup"><span data-stu-id="bf198-243">Set **cButtons** to the number of buttons, and return.</span></span>

<span data-ttu-id="bf198-244">El siguiente [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) es para el primer botón.</span><span class="sxs-lookup"><span data-stu-id="bf198-244">The next [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) is for the first button.</span></span> <span data-ttu-id="bf198-245">El miembro **pCurrent** apunta al principio del primer bloque de datos del botón y **iItem** se establece en el índice del botón.</span><span class="sxs-lookup"><span data-stu-id="bf198-245">The **pCurrent** member points to the start of your first block of button data, and **iItem** is set to the button index.</span></span> <span data-ttu-id="bf198-246">Extraiga los datos y avance **pCurrent**.</span><span class="sxs-lookup"><span data-stu-id="bf198-246">Extract that data and advance **pCurrent**.</span></span> <span data-ttu-id="bf198-247">Cargue los datos en [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)y devuelva.</span><span class="sxs-lookup"><span data-stu-id="bf198-247">Load the data into [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton), and return.</span></span> <span data-ttu-id="bf198-248">Para omitir un botón de la barra de herramientas restaurada, establezca el miembro **idCommand** de **TBBUTTON** en cero.</span><span class="sxs-lookup"><span data-stu-id="bf198-248">To omit a button from the restored toolbar, set the **idCommand** member of **TBBUTTON** to zero.</span></span> <span data-ttu-id="bf198-249">El shell repetirá el proceso para los botones restantes.</span><span class="sxs-lookup"><span data-stu-id="bf198-249">The Shell will repeat the process for the remaining buttons.</span></span> <span data-ttu-id="bf198-250">Además de los mensajes [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) y **NMTBRESTORE** , también puede usar mensajes como [TBN \_ RESET](tbn-reset.md) para guardar y restaurar una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="bf198-250">In addition to the [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) and **NMTBRESTORE** messages, you can also use messages such as [TBN\_RESET](tbn-reset.md) to save and restore a toolbar.</span></span>

<span data-ttu-id="bf198-251">En el ejemplo de código siguiente se guarda una barra de herramientas antes de personalizarla y se restaura si la aplicación recibe un mensaje de [ \_ restablecimiento de TBN](tbn-reset.md) .</span><span class="sxs-lookup"><span data-stu-id="bf198-251">The following code example saves a toolbar before it is customized, and restores it if the application receives a [TBN\_RESET](tbn-reset.md) message.</span></span>


```C++
int               i;
LPNMHDR           lpnmhdr;
static int        nResetCount;
static LPTBBUTTON lpSaveButtons;
LPARAM            lParam;

switch( lpnmhdr->code)
{
    case TBN_BEGINADJUST: // Begin customizing the toolbar.
    {
        LPTBNOTIFY  lpTB = (LPTBNOTIFY)lparam;
       
        // Allocate memory for the button information.
        
        nResetCount   = SendMessage(lpTB->hdr.hwndFrom, TB_BUTTONCOUNT, 0, 0);
        lpSaveButtons = (LPTBBUTTON)GlobalAlloc(GPTR, sizeof(TBBUTTON) * nResetCount);
      
        // In case the user presses reset, save the current configuration 
        // so the original toolbar can be restored.
        
        for(i = 0; i < nResetCount; i++)
        {
            SendMessage(lpTB->hdr.hwndFrom, 
                        TB_GETBUTTON, i, 
                        (LPARAM)(lpSaveButtons + i));
        }
    }
    
    return TRUE;
   
    case TBN_RESET:
    {
        LPTBNOTIFY lpTB = (LPTBNOTIFY)lparam;
        
        int nCount, i;
    
        // Remove all of the existing buttons, starting with the last one.
        
        nCount = SendMessage(lpTB->hdr.hwndFrom, TB_BUTTONCOUNT, 0, 0);
        
        for(i = nCount - 1; i >= 0; i--)
        {
            SendMessage(lpTB->hdr.hwndFrom, TB_DELETEBUTTON, i, 0);
        }
      
        SendMessage(lpTB->hdr.hwndFrom,      // Restore the saved buttons.
                    TB_ADDBUTTONS, 
                    (WPARAM)nResetCount, 
                    (LPARAM)lpSaveButtons);
    }
    
    return TRUE;
   
    case TBN_ENDADJUST:                // Free up the memory you allocated.
        GlobalFree((HGLOBAL)lpSaveButtons);
        
        return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="bf198-252">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bf198-252">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf198-253">Usar controles Toolbar</span><span class="sxs-lookup"><span data-stu-id="bf198-253">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

[<span data-ttu-id="bf198-254">**Valores de índice de imagen de botón estándar de la barra de herramientas**</span><span class="sxs-lookup"><span data-stu-id="bf198-254">**Toolbar Standard Button Image Index Values**</span></span>](toolbar-standard-button-image-index-values.md)
</dt> <dt>

<span data-ttu-id="bf198-255">[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="bf198-255">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




