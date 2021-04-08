---
title: Menú de la aplicación
description: El menú aplicación es el menú principal de una aplicación que implementa el marco de la cinta de opciones de Windows.
ms.assetid: 5be93a5b-277b-44c1-be24-a0598a140bfc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99f57045daa35149e5fa074cb59e2f538c589b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904612"
---
# <a name="application-menu"></a><span data-ttu-id="b74df-103">Menú de la aplicación</span><span class="sxs-lookup"><span data-stu-id="b74df-103">Application Menu</span></span>

<span data-ttu-id="b74df-104">El menú aplicación es el menú principal de una aplicación que implementa el marco de la cinta de opciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="b74df-104">The Application Menu is the main menu for an application that implements the Windows Ribbon framework.</span></span>

-   [<span data-ttu-id="b74df-105">Introducción</span><span class="sxs-lookup"><span data-stu-id="b74df-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="b74df-106">Componentes del menú aplicación</span><span class="sxs-lookup"><span data-stu-id="b74df-106">Components of the Application Menu</span></span>](#components-of-the-application-menu)
    -   [<span data-ttu-id="b74df-107">Menú de aplicación MenuGroup</span><span class="sxs-lookup"><span data-stu-id="b74df-107">Application Menu MenuGroup</span></span>](#application-menu-menugroup)
-   [<span data-ttu-id="b74df-108">Ajustar el tamaño del menú de la aplicación</span><span class="sxs-lookup"><span data-stu-id="b74df-108">Sizing the Application Menu</span></span>](#sizing-the-application-menu)
-   [<span data-ttu-id="b74df-109">Propiedades del menú de la aplicación</span><span class="sxs-lookup"><span data-stu-id="b74df-109">Application Menu Properties</span></span>](#application-menu-properties)
-   [<span data-ttu-id="b74df-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b74df-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="b74df-111">Introducción</span><span class="sxs-lookup"><span data-stu-id="b74df-111">Introduction</span></span>

<span data-ttu-id="b74df-112">El menú aplicación se compone de un control de botón desplegable que muestra un menú que contiene comandos que exponen la funcionalidad relacionada con un proyecto completo, como un documento, una imagen o una película completos.</span><span class="sxs-lookup"><span data-stu-id="b74df-112">The Application Menu is composed of a drop-down button control that displays a menu containing Commands that expose functionality related to a complete project, such as an entire document, picture, or movie.</span></span> <span data-ttu-id="b74df-113">Entre los ejemplos se incluyen los comandos **nuevos**, **abrir**, **Guardar** y **salir** .</span><span class="sxs-lookup"><span data-stu-id="b74df-113">Examples include the **New**, **Open**, **Save**, and **Exit** Commands.</span></span>

<span data-ttu-id="b74df-114">En la captura de pantalla siguiente se muestra el menú de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b74df-114">The following screen shot illustrates the Application Menu.</span></span>

![captura de pantalla del menú aplicación y la lista elementos recientes de la cinta de opciones Paint for Windows 7.](images/controls/recentitems.png)

## <a name="components-of-the-application-menu"></a><span data-ttu-id="b74df-116">Componentes del menú aplicación</span><span class="sxs-lookup"><span data-stu-id="b74df-116">Components of the Application Menu</span></span>

<span data-ttu-id="b74df-117">El menú aplicación es un elemento obligatorio en cualquier aplicación de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="b74df-117">The Application Menu is a mandatory element in any Ribbon application.</span></span> <span data-ttu-id="b74df-118">El punto de entrada en el menú de la aplicación es un botón distintivo que aparece como el primer elemento de la fila de [pestañas](windowsribbon-controls-tab.md) , como se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="b74df-118">The entry point into the Application Menu is a distinctive button that appears as the first item in the [Tab](windowsribbon-controls-tab.md) row, as shown in the following screen shot.</span></span>

> [!Note]  
> <span data-ttu-id="b74df-119">Windows 8 y versiones más recientes: imagen del botón de menú de la aplicación cambiada a etiqueta: **archivo**.</span><span class="sxs-lookup"><span data-stu-id="b74df-119">Windows 8 and newer: Application Menu button image changed to label: **File**.</span></span> <span data-ttu-id="b74df-120">Se recomienda no usar archivo como etiqueta para ninguna de sus propias pestañas.</span><span class="sxs-lookup"><span data-stu-id="b74df-120">We recommend that you do not use File as the label for any of your own tabs.</span></span>

 

![captura de pantalla del botón de menú aplicación de WordPad para Windows 7.](images/overviews/applicationmenu-button.png)

<span data-ttu-id="b74df-122">Al hacer clic en este botón, se muestra el menú enriquecido que se muestra en la siguiente captura de pantalla (menú aplicación de WordPad para Windows 7).</span><span class="sxs-lookup"><span data-stu-id="b74df-122">When clicked, this button displays the rich menu that is shown in the following screen shot (the Application Menu from WordPad for Windows 7).</span></span>

![captura de pantalla del menú de menú de la aplicación de WordPad para Windows 7.](images/overviews/applicationmenu-menu.png)

> [!Note]  
> <span data-ttu-id="b74df-124">No se produce ningún impacto en el conjunto de pestañas cuando se hace clic en el botón de menú de la aplicación. en su lugar, el foco entra en el menú.</span><span class="sxs-lookup"><span data-stu-id="b74df-124">There is no impact on the tab set when the Application Menu button is clicked; instead, the focus enters the menu.</span></span>

 

<span data-ttu-id="b74df-125">El menú aplicación contiene dos paneles: una lista de comandos representados por uno o varios elementos [**MenuGroup**](windowsribbon-element-menugroup.md) y una lista de [elementos recientes](windowsribbon-controls-recentitems.md) representada por un elemento [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="b74df-125">The Application Menu contains two panes: a list of Commands represented by one or more [**MenuGroup**](windowsribbon-element-menugroup.md) elements, and a [Recent Items](windowsribbon-controls-recentitems.md) list represented by an [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) element.</span></span>

### <a name="application-menu-menugroup"></a><span data-ttu-id="b74df-126">Menú de aplicación MenuGroup</span><span class="sxs-lookup"><span data-stu-id="b74df-126">Application Menu MenuGroup</span></span>

<span data-ttu-id="b74df-127">El elemento [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) debe contener al menos un elemento secundario [**MenuGroup**](windowsribbon-element-menugroup.md) que exponga una lista de comandos de nivel de aplicación.</span><span class="sxs-lookup"><span data-stu-id="b74df-127">The [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) element must contain at least one [**MenuGroup**](windowsribbon-element-menugroup.md) child element that exposes a list of application-level commands.</span></span> <span data-ttu-id="b74df-128">Si se declaran varios elementos **MenuGroup** , se dibuja una línea divisoria entre los grupos, tal y como se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="b74df-128">If multiple **MenuGroup** elements are declared, a divider line is drawn between the groups, as shown in the following screen shot.</span></span>

![captura de pantalla de un menú de aplicación menugroup.](images/overviews/applicationmenu-menugroup.png)

<span data-ttu-id="b74df-130">A continuación se muestra una lista de restricciones para un elemento [**MenuGroup**](windowsribbon-element-menugroup.md) de un menú de la aplicación:</span><span class="sxs-lookup"><span data-stu-id="b74df-130">The following is a list of constraints for a [**MenuGroup**](windowsribbon-element-menugroup.md) element of an Application Menu:</span></span>

-   <span data-ttu-id="b74df-131">Todos los elementos [**MenuGroup**](windowsribbon-element-menugroup.md) se deben declarar con un valor de atributo de *clase* de `MajorItems` .</span><span class="sxs-lookup"><span data-stu-id="b74df-131">All [**MenuGroup**](windowsribbon-element-menugroup.md) items must be declared with a *Class* attribute value of `MajorItems`.</span></span>
-   <span data-ttu-id="b74df-132">Un menú de aplicación  [**MenuGroup**](windowsribbon-element-menugroup.md) solo admite el [botón](windowsribbon-controls-button.md), [botón](windowsribbon-controls-togglebutton.md)de alternancia [, botón](windowsribbon-controls-dropdownbutton.md)desplegable, [botón de expansión](windowsribbon-controls-splitbutton.md), [Galería desplegable](windowsribbon-controls-dropdowngallery.md)y controles de la [Galería de botones de expansión](windowsribbon-controls-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="b74df-132">An Application Menu  [**MenuGroup**](windowsribbon-element-menugroup.md) supports only the [Button](windowsribbon-controls-button.md), [Toggle Button](windowsribbon-controls-togglebutton.md), [Drop-Down Button](windowsribbon-controls-dropdownbutton.md), [Split Button](windowsribbon-controls-splitbutton.md), [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md), and [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) controls.</span></span>
    > <span data-ttu-id="b74df-133">\[! Aún\]</span><span class="sxs-lookup"><span data-stu-id="b74df-133">\[!Important\]</span></span>  
    > <span data-ttu-id="b74df-134">Las galerías de comandos son el único tipo de galería que se admiten en el menú de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b74df-134">Command galleries are the only type of gallery that are supported in the Application Menu.</span></span> <span data-ttu-id="b74df-135">Vea [trabajar con galerías](./ribbon-controls-galleries.md)para obtener más información sobre los controles de la galería.</span><span class="sxs-lookup"><span data-stu-id="b74df-135">See [Working with Galleries](./ribbon-controls-galleries.md), for more information on gallery controls.</span></span>

     

<span data-ttu-id="b74df-136">Cuando se usa un [botón o un](windowsribbon-controls-button.md) botón de [alternancia](windowsribbon-controls-togglebutton.md) en un [**MenuGroup**](windowsribbon-element-menugroup.md), el valor de [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) se muestra en el menú y los valores de [**Command. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md) y [**Command. TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) se muestran como la información sobre herramientas, como se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="b74df-136">When a [Button](windowsribbon-controls-button.md) or [Toggle Button](windowsribbon-controls-togglebutton.md) is used in a [**MenuGroup**](windowsribbon-element-menugroup.md), the value of [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) is displayed in the menu and the values of [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md) and [**Command.TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) are displayed as the tooltip, as shown in the following screen shot.</span></span>

![captura de pantalla de un control de botón en un menú de la aplicación.](images/overviews/applicationmenu-menubutton.png)

<span data-ttu-id="b74df-138">Cuando se usa un [botón](windowsribbon-controls-dropdownbutton.md)desplegable, un [botón de expansión](windowsribbon-controls-splitbutton.md), una [Galería](windowsribbon-controls-dropdowngallery.md)desplegable o una galería de [botones de expansión](windowsribbon-controls-splitbuttongallery.md) en el menú aplicación, la parte del menú se muestra como un control flotante que cubre y oculta el panel **elementos recientes** .</span><span class="sxs-lookup"><span data-stu-id="b74df-138">When a [Drop-Down Button](windowsribbon-controls-dropdownbutton.md), [Split Button](windowsribbon-controls-splitbutton.md), [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md), or [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) is used in the Application Menu, the menu portion is displayed as a flyout that covers and conceals the **Recent items** pane.</span></span>

<span data-ttu-id="b74df-139">En el caso de los controles de botón de [expansión](windowsribbon-controls-splitbutton.md) y de [botón](windowsribbon-controls-dropdownbutton.md) desplegable, el valor de [**Command. LabelDescription**](windowsribbon-element-command-labeldescription.md) se muestra en línea en el menú flotante para ayudar visualmente a los usuarios a detectar la funcionalidad del comando.</span><span class="sxs-lookup"><span data-stu-id="b74df-139">For [Split Button](windowsribbon-controls-splitbutton.md) and [Drop-Down Button](windowsribbon-controls-dropdownbutton.md) controls, the value of [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md) is shown inline in the flyout menu to visually assist users with discovering the Command functionality.</span></span> <span data-ttu-id="b74df-140">El valor mostrado de **Command. LabelDescription** se divide mediante programación en un intervalo de dos líneas, y se realiza un intento de ajustar el valor exactamente encima del panel **elementos recientes** de.</span><span class="sxs-lookup"><span data-stu-id="b74df-140">The displayed value of **Command.LabelDescription** is programmatically broken over a two-line span, and an attempt is made to fit the value exactly over the **Recent items** pane beneath.</span></span> <span data-ttu-id="b74df-141">Si el valor de **Command. LabelDescription** no cabe, el control flotante se expandirá para alojar el valor del comando más largo [**. Comment**](windowsribbon-element-command-comment.md) en el [**MenuGroup**](windowsribbon-element-menugroup.md).</span><span class="sxs-lookup"><span data-stu-id="b74df-141">If the **Command.LabelDescription** value does not fit, the flyout will expand to accommodate the longest [**Command.Comment**](windowsribbon-element-command-comment.md) value in the [**MenuGroup**](windowsribbon-element-menugroup.md).</span></span>

<span data-ttu-id="b74df-142">En la siguiente captura de pantalla se muestran estos comportamientos en un control flotante de [botón de expansión](windowsribbon-controls-splitbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="b74df-142">The following screen shot illustrates these behaviors in a [Split Button](windowsribbon-controls-splitbutton.md) flyout.</span></span>

![captura de pantalla de un control flotante de control de lista en un menú de la aplicación.](images/overviews/applicationmenu-menuflyout.png)

<span data-ttu-id="b74df-144">Con una [Galería desplegable](windowsribbon-controls-dropdowngallery.md) y una [Galería de botones de división](windowsribbon-controls-splitbuttongallery.md), solo se muestran una etiqueta y una imagen.</span><span class="sxs-lookup"><span data-stu-id="b74df-144">With a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) and a [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md), only a label and an image are shown.</span></span>

## <a name="sizing-the-application-menu"></a><span data-ttu-id="b74df-145">Ajustar el tamaño del menú de la aplicación</span><span class="sxs-lookup"><span data-stu-id="b74df-145">Sizing the Application Menu</span></span>

<span data-ttu-id="b74df-146">El marco de la cinta de opciones controla el tamaño del menú de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b74df-146">Sizing of the Application Menu is handled by the Ribbon framework.</span></span> <span data-ttu-id="b74df-147">Si se proporcionan cadenas muy largas para el valor de [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) o [**Command. LabelDescription**](windowsribbon-element-command-labeldescription.md), o si se usa una larga lista de comandos, el menú ajustará su tamaño para dar cabida al contenido.</span><span class="sxs-lookup"><span data-stu-id="b74df-147">If very long strings are supplied for the value of [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md), or a long list of Commands is used, the menu will adjust its size to accommodate the contents.</span></span> <span data-ttu-id="b74df-148">Algunas formas de ajuste incluyen expandir el tamaño de los controles flotantes o paneles de menús, y agregar visores de desplazamiento cuando es necesario desplazarse.</span><span class="sxs-lookup"><span data-stu-id="b74df-148">Some forms of adjustment include expanding the size of flyouts or menu panes, and adding pan viewers when scrolling is required.</span></span>

## <a name="application-menu-properties"></a><span data-ttu-id="b74df-149">Propiedades del menú de la aplicación</span><span class="sxs-lookup"><span data-stu-id="b74df-149">Application Menu Properties</span></span>

<span data-ttu-id="b74df-150">El marco de cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control de menú de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b74df-150">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Application Menu control.</span></span>

<span data-ttu-id="b74df-151">Normalmente, una propiedad de menú de la aplicación se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control a través de una llamada al método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="b74df-151">Typically, an Application Menu property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="b74df-152">El evento de invalidación se controla y las actualizaciones de las propiedades se definen mediante el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="b74df-152">The invalidation event is handled and the property updates are defined by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="b74df-153">No se ejecuta el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y no se consulta la aplicación para obtener un valor de propiedad actualizado hasta que el marco de trabajo requiera la propiedad.</span><span class="sxs-lookup"><span data-stu-id="b74df-153">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed and the application is not queried for an updated property value until the property is required by the framework.</span></span> <span data-ttu-id="b74df-154">Por ejemplo, el marco de trabajo requiere la propiedad cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones o cuando se muestra una información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="b74df-154">For example, the framework requires the property when a tab is activated and a control is revealed in the ribbon UI, or when a tooltip is displayed.</span></span>



| <span data-ttu-id="b74df-155">Clave de propiedad</span><span class="sxs-lookup"><span data-stu-id="b74df-155">Property key</span></span>                                                                                     | <span data-ttu-id="b74df-156">Notas</span><span class="sxs-lookup"><span data-stu-id="b74df-156">Notes</span></span>                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="b74df-157">UI \_ PKEY \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="b74df-157">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="b74df-158">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="b74df-158">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="b74df-159">UI \_ PKEY \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="b74df-159">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="b74df-160">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="b74df-160">Can only be updated through invalidation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b74df-161">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b74df-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b74df-162">Biblioteca de controles de Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="b74df-162">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="b74df-163">**Elemento de marcado ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="b74df-163">**ApplicationMenu markup element**</span></span>](windowsribbon-element-applicationmenu.md)
</dt> </dl>

 

 