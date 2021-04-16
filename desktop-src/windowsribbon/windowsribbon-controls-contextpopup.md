---
title: Cuadro emergente de contexto
description: Un elemento emergente de contexto es el control principal en la vista ContextPopup del marco de la cinta de opciones de Windows.
ms.assetid: c41b888a-15aa-4c47-ad73-5dc30b5fa6f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c77441cc3cdcc9212d27d2230d76d2618f1831ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676423"
---
# <a name="context-popup"></a><span data-ttu-id="f8403-103">Cuadro emergente de contexto</span><span class="sxs-lookup"><span data-stu-id="f8403-103">Context Popup</span></span>

<span data-ttu-id="f8403-104">Un elemento emergente de contexto es el control principal en la [**vista ContextPopup**](windowsribbon-element-contextpopup.md) del marco de la cinta de opciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="f8403-104">A Context Popup is the principal control in the [**ContextPopup View**](windowsribbon-element-contextpopup.md) of the Windows Ribbon framework.</span></span> <span data-ttu-id="f8403-105">Se trata de un sistema de menús contextuales enriquecido que solo expone el marco de trabajo como una extensión a una implementación de la cinta de opciones; el marco no expone el elemento emergente de contexto como control independiente.</span><span class="sxs-lookup"><span data-stu-id="f8403-105">It is a rich context menu system that is only exposed by the framework as an extension to a Ribbon implementation—the framework does not expose the Context Popup as an independent control.</span></span>

-   [<span data-ttu-id="f8403-106">Componentes del elemento emergente de contexto</span><span class="sxs-lookup"><span data-stu-id="f8403-106">Components of the Context Popup</span></span>](#context-popup)
-   [<span data-ttu-id="f8403-107">Implementar el elemento emergente de contexto</span><span class="sxs-lookup"><span data-stu-id="f8403-107">Implement the Context Popup</span></span>](#implement-the-context-popup)
    -   [<span data-ttu-id="f8403-108">marcado</span><span class="sxs-lookup"><span data-stu-id="f8403-108">Markup</span></span>](#markup)
    -   [<span data-ttu-id="f8403-109">Código</span><span class="sxs-lookup"><span data-stu-id="f8403-109">Code</span></span>](#code)
-   [<span data-ttu-id="f8403-110">Propiedades de elemento emergente de contexto</span><span class="sxs-lookup"><span data-stu-id="f8403-110">Context Popup Properties</span></span>](#context-popup-properties)
-   [<span data-ttu-id="f8403-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f8403-111">Related topics</span></span>](#related-topics)

## <a name="components-of-the-context-popup"></a><span data-ttu-id="f8403-112">Componentes del elemento emergente de contexto</span><span class="sxs-lookup"><span data-stu-id="f8403-112">Components of the Context Popup</span></span>

<span data-ttu-id="f8403-113">El elemento emergente de contexto es un contenedor lógico para el menú contextual y Mini-Toolbar los subcontrols que se exponen a través de los elementos de marcado [**ContextMenu**](windowsribbon-element-contextmenu.md) y [**MiniToolbar**](windowsribbon-element-minitoolbar.md) , respectivamente:</span><span class="sxs-lookup"><span data-stu-id="f8403-113">The Context Popup is a logical container for the Context Menu and Mini-Toolbar sub-controls that are exposed through the [**ContextMenu**](windowsribbon-element-contextmenu.md) and [**MiniToolbar**](windowsribbon-element-minitoolbar.md) markup elements, respectively:</span></span>

-   <span data-ttu-id="f8403-114">El [**ContextMenu**](windowsribbon-element-contextmenu.md) expone un menú de comandos y galerías.</span><span class="sxs-lookup"><span data-stu-id="f8403-114">The [**ContextMenu**](windowsribbon-element-contextmenu.md) exposes a menu of Commands and galleries.</span></span>
-   <span data-ttu-id="f8403-115">[**MiniToolbar**](windowsribbon-element-minitoolbar.md) expone una barra de herramientas flotante de varios comandos, galerías y controles complejos, como el [control de fuente](windowsribbon-controls-fontcontrol.md) y el [cuadro combinado](windowsribbon-controls-combobox.md).</span><span class="sxs-lookup"><span data-stu-id="f8403-115">The [**MiniToolbar**](windowsribbon-element-minitoolbar.md) exposes a floating toolbar of various Commands, galleries, and complex controls such as the [Font Control](windowsribbon-controls-fontcontrol.md) and the [Combo Box](windowsribbon-controls-combobox.md).</span></span>

<span data-ttu-id="f8403-116">Cada subcontrol puede aparecer como máximo una vez en una ventana emergente de contexto.</span><span class="sxs-lookup"><span data-stu-id="f8403-116">Each sub-control can appear at most once in a Context Popup.</span></span>

<span data-ttu-id="f8403-117">La siguiente captura de pantalla muestra el contexto emergente y sus subcontrols constituyentes.</span><span class="sxs-lookup"><span data-stu-id="f8403-117">The following screen shot illustrates the Context Popup and its constituent sub-controls.</span></span>

![captura de pantalla con llamadas que muestran los componentes de interfaz de usuario contextual de la cinta.](images/controls/contextpopup.png)

<span data-ttu-id="f8403-119">El elemento emergente de contexto es puramente conceptual y no expone ninguna funcionalidad de la interfaz de usuario, como la posición o el ajuste de tamaño.</span><span class="sxs-lookup"><span data-stu-id="f8403-119">The Context Popup is purely conceptual and does not expose any UI functionality itself, such as positioning or sizing.</span></span>

> [!Note]  
> <span data-ttu-id="f8403-120">La ventana emergente contextual se muestra normalmente al hacer clic con el botón secundario en el mouse (o mediante el método abreviado de teclado Mayús + F10) en un objeto de interés.</span><span class="sxs-lookup"><span data-stu-id="f8403-120">The Context Popup is typically displayed by right-clicking the mouse (or through the keyboard shortcut SHIFT+F10) on an object of interest.</span></span> <span data-ttu-id="f8403-121">Sin embargo, la aplicación define los pasos necesarios para mostrar el elemento emergente de contexto.</span><span class="sxs-lookup"><span data-stu-id="f8403-121">However, the steps required to display the Context Popup are defined by the application.</span></span>

 

## <a name="implement-the-context-popup"></a><span data-ttu-id="f8403-122">Implementar el elemento emergente de contexto</span><span class="sxs-lookup"><span data-stu-id="f8403-122">Implement the Context Popup</span></span>

<span data-ttu-id="f8403-123">De forma similar a otros controles de marcos de cinta de Windows, el elemento emergente de contexto se implementa a través de un componente de marcado que especifica los detalles de presentación y un componente de código que rige su funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="f8403-123">In similar fashion to other Windows Ribbon framework controls, the Context Popup is implemented through a markup component that specifies its presentation details and a code component that governs its functionality.</span></span>

<span data-ttu-id="f8403-124">En la tabla siguiente se enumeran los controles que admite cada subcontrol emergente de contexto.</span><span class="sxs-lookup"><span data-stu-id="f8403-124">The following table lists the controls that are supported by each Context Popup sub-control.</span></span>



| <span data-ttu-id="f8403-125">Control</span><span class="sxs-lookup"><span data-stu-id="f8403-125">Control</span></span>                                                                  | <span data-ttu-id="f8403-126">Mini-Toolbar</span><span class="sxs-lookup"><span data-stu-id="f8403-126">Mini-Toolbar</span></span> | <span data-ttu-id="f8403-127">Menú contextual</span><span class="sxs-lookup"><span data-stu-id="f8403-127">Context Menu</span></span> |
|--------------------------------------------------------------------------|--------------|--------------|
| [<span data-ttu-id="f8403-128">Botón</span><span class="sxs-lookup"><span data-stu-id="f8403-128">Button</span></span>](windowsribbon-controls-button.md)                              | <span data-ttu-id="f8403-129">x</span><span class="sxs-lookup"><span data-stu-id="f8403-129">x</span></span>            | <span data-ttu-id="f8403-130">x</span><span class="sxs-lookup"><span data-stu-id="f8403-130">x</span></span>            |
| [<span data-ttu-id="f8403-131">Casilla de verificación</span><span class="sxs-lookup"><span data-stu-id="f8403-131">Check Box</span></span>](windowsribbon-controls-checkbox.md)                         | <span data-ttu-id="f8403-132">x</span><span class="sxs-lookup"><span data-stu-id="f8403-132">x</span></span>            | <span data-ttu-id="f8403-133">x</span><span class="sxs-lookup"><span data-stu-id="f8403-133">x</span></span>            |
| [<span data-ttu-id="f8403-134">Cuadro combinado</span><span class="sxs-lookup"><span data-stu-id="f8403-134">Combo Box</span></span>](windowsribbon-controls-combobox.md)                         | <span data-ttu-id="f8403-135">x</span><span class="sxs-lookup"><span data-stu-id="f8403-135">x</span></span>            |              |
| [<span data-ttu-id="f8403-136">Botón desplegable</span><span class="sxs-lookup"><span data-stu-id="f8403-136">Drop-Down Button</span></span>](windowsribbon-controls-dropdownbutton.md)            | <span data-ttu-id="f8403-137">x</span><span class="sxs-lookup"><span data-stu-id="f8403-137">x</span></span>            | <span data-ttu-id="f8403-138">x</span><span class="sxs-lookup"><span data-stu-id="f8403-138">x</span></span>            |
| [<span data-ttu-id="f8403-139">Selector de colores desplegables</span><span class="sxs-lookup"><span data-stu-id="f8403-139">Drop-Down Color Picker</span></span>](windowsribbon-controls-dropdowncolorpicker.md) | <span data-ttu-id="f8403-140">x</span><span class="sxs-lookup"><span data-stu-id="f8403-140">x</span></span>            | <span data-ttu-id="f8403-141">x</span><span class="sxs-lookup"><span data-stu-id="f8403-141">x</span></span>            |
| [<span data-ttu-id="f8403-142">Galería desplegable</span><span class="sxs-lookup"><span data-stu-id="f8403-142">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)          | <span data-ttu-id="f8403-143">x</span><span class="sxs-lookup"><span data-stu-id="f8403-143">x</span></span>            | <span data-ttu-id="f8403-144">x</span><span class="sxs-lookup"><span data-stu-id="f8403-144">x</span></span>            |
| [<span data-ttu-id="f8403-145">Control de fuente</span><span class="sxs-lookup"><span data-stu-id="f8403-145">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)                   | <span data-ttu-id="f8403-146">x</span><span class="sxs-lookup"><span data-stu-id="f8403-146">x</span></span>            |              |
| [<span data-ttu-id="f8403-147">Botón ayuda</span><span class="sxs-lookup"><span data-stu-id="f8403-147">Help Button</span></span>](windowsribbon-controls-helpbutton.md)                     |              |              |
| [<span data-ttu-id="f8403-148">En la galería de la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="f8403-148">In-Ribbon Gallery</span></span>](windowsribbon-controls-inribbongallery.md)          |              |              |
| [<span data-ttu-id="f8403-149">Spinner</span><span class="sxs-lookup"><span data-stu-id="f8403-149">Spinner</span></span>](windowsribbon-controls-spinner.md)                            |              |              |
| [<span data-ttu-id="f8403-150">Botón de expansión</span><span class="sxs-lookup"><span data-stu-id="f8403-150">Split Button</span></span>](windowsribbon-controls-splitbutton.md)                   | <span data-ttu-id="f8403-151">x</span><span class="sxs-lookup"><span data-stu-id="f8403-151">x</span></span>            | <span data-ttu-id="f8403-152">x</span><span class="sxs-lookup"><span data-stu-id="f8403-152">x</span></span>            |
| [<span data-ttu-id="f8403-153">Galería de botones de expansión</span><span class="sxs-lookup"><span data-stu-id="f8403-153">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md)    | <span data-ttu-id="f8403-154">x</span><span class="sxs-lookup"><span data-stu-id="f8403-154">x</span></span>            | <span data-ttu-id="f8403-155">x</span><span class="sxs-lookup"><span data-stu-id="f8403-155">x</span></span>            |
| [<span data-ttu-id="f8403-156">Botón de alternancia</span><span class="sxs-lookup"><span data-stu-id="f8403-156">Toggle Button</span></span>](windowsribbon-controls-togglebutton.md)                 | <span data-ttu-id="f8403-157">x</span><span class="sxs-lookup"><span data-stu-id="f8403-157">x</span></span>            | <span data-ttu-id="f8403-158">x</span><span class="sxs-lookup"><span data-stu-id="f8403-158">x</span></span>            |



 

### <a name="markup"></a><span data-ttu-id="f8403-159">marcado</span><span class="sxs-lookup"><span data-stu-id="f8403-159">Markup</span></span>

<span data-ttu-id="f8403-160">Cada subcontrol emergente de contexto debe declararse individualmente en el marcado.</span><span class="sxs-lookup"><span data-stu-id="f8403-160">Each Context Popup sub-control must be declared individually in markup.</span></span>

### <a name="mini-toolbar"></a><span data-ttu-id="f8403-161">Mini-Toolbar</span><span class="sxs-lookup"><span data-stu-id="f8403-161">Mini-Toolbar</span></span>

<span data-ttu-id="f8403-162">Al agregar controles a una minibarra de herramientas emergente de contexto, se deben tener en cuenta las dos recomendaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="f8403-162">When adding controls to a Context Popup Mini-Toolbar, the following two recommendations should be considered:</span></span>

-   <span data-ttu-id="f8403-163">Los controles deben ser muy reconocibles y proporcionar una funcionalidad obvia.</span><span class="sxs-lookup"><span data-stu-id="f8403-163">Controls should be highly recognizable and provide obvious functionality.</span></span> <span data-ttu-id="f8403-164">La familiaridad es la clave, ya que las etiquetas e información sobre herramientas no se exponen para los controles de Mini-Toolbar.</span><span class="sxs-lookup"><span data-stu-id="f8403-164">Familiarity is key, as labels and tooltips are not exposed for Mini-Toolbar controls.</span></span>
-   <span data-ttu-id="f8403-165">Cada comando expuesto por un control se debe presentar en otro lugar de la interfaz de usuario de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="f8403-165">Each Command exposed by a control should be presented elsewhere in the ribbon UI.</span></span> <span data-ttu-id="f8403-166">La Mini-Toolbar no admite la navegación con el teclado.</span><span class="sxs-lookup"><span data-stu-id="f8403-166">The Mini-Toolbar does not support keyboard navigation.</span></span>

<span data-ttu-id="f8403-167">En el ejemplo siguiente se muestra el marcado básico de un elemento [**MiniToolbar**](windowsribbon-element-minitoolbar.md) que contiene tres controles [Button](windowsribbon-controls-button.md) .</span><span class="sxs-lookup"><span data-stu-id="f8403-167">The following example demonstrates the basic markup for a [**MiniToolbar**](windowsribbon-element-minitoolbar.md) element that contains three [Button](windowsribbon-controls-button.md) controls.</span></span>

> [!Note]  
> <span data-ttu-id="f8403-168">Se especifica un elemento [**MenuGroup**](windowsribbon-element-menugroup.md) para cada fila de controles de la minibarra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="f8403-168">One [**MenuGroup**](windowsribbon-element-menugroup.md) element is specified for each row of controls in the Mini-Toolbar.</span></span>

 


```C++
<MiniToolbar Name="MiniToolbar">
  <MenuGroup>
    <Button CommandName="cmdButton1" />
    <Button CommandName="cmdButton2" />
    <Button CommandName="cmdButton3" />
  </MenuGroup>
</MiniToolbar>
```



### <a name="context-menu"></a><span data-ttu-id="f8403-169">Menú contextual</span><span class="sxs-lookup"><span data-stu-id="f8403-169">Context Menu</span></span>

<span data-ttu-id="f8403-170">En el ejemplo siguiente se muestra el marcado básico para un elemento [**ContextMenu**](windowsribbon-element-contextmenu.md) que contiene tres controles de [botón](windowsribbon-controls-button.md) .</span><span class="sxs-lookup"><span data-stu-id="f8403-170">The following example demonstrates the basic markup for a [**ContextMenu**](windowsribbon-element-contextmenu.md) element that contains three [Button](windowsribbon-controls-button.md) controls.</span></span>

> [!Note]  
> <span data-ttu-id="f8403-171">Cada conjunto de controles del elemento [**MenuGroup**](windowsribbon-element-menugroup.md) está separado por una barra horizontal en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="f8403-171">Each set of controls in the [**MenuGroup**](windowsribbon-element-menugroup.md) element is separated by a horizontal bar in the Context Menu.</span></span>

 


```C++
<ContextMenu Name="ContextMenu">
  <MenuGroup>
    <Button CommandName="cmdCut" />
    <Button CommandName="cmdCopy" />
    <Button CommandName="cmdPaste" />
  </MenuGroup>
</ContextMenu>
```



<span data-ttu-id="f8403-172">Aunque un elemento emergente de contexto puede contener como máximo uno de cada subcontrol, son válidos varias declaraciones de elementos [**ContextMenu**](windowsribbon-element-contextmenu.md) y [**MiniToolbar**](windowsribbon-element-minitoolbar.md) en el marcado de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="f8403-172">Although a Context Popup can contain at most one of each sub-control, multiple [**ContextMenu**](windowsribbon-element-contextmenu.md) and [**MiniToolbar**](windowsribbon-element-minitoolbar.md) element declarations in the Ribbon markup are valid.</span></span> <span data-ttu-id="f8403-173">Esto permite que una aplicación admita varias combinaciones de controles de menú contextual y Mini-Toolbar, en función de los criterios definidos por la aplicación, como el contexto del área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="f8403-173">This allows an application to support various combinations of Context Menu and Mini-Toolbar controls, based on criteria defined by the application, such as workspace context.</span></span>

<span data-ttu-id="f8403-174">Para obtener más información, vea el elemento [**ContextMap**](windowsribbon-element-contextmap.md) .</span><span class="sxs-lookup"><span data-stu-id="f8403-174">For more information, see the [**ContextMap**](windowsribbon-element-contextmap.md) element.</span></span>

<span data-ttu-id="f8403-175">En el ejemplo siguiente se muestra el marcado básico para el elemento [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="f8403-175">The following example demonstrates the basic markup for the [**ContextPopup**](windowsribbon-element-contextpopup.md) element.</span></span>


```C++
<ContextPopup>
  <ContextPopup.MiniToolbars>
    <MiniToolbar Name="MiniToolbar">
      <MenuGroup>
        <Button CommandName="cmdButton1" />
        <Button CommandName="cmdButton2" />
        <Button CommandName="cmdButton3" />
      </MenuGroup>
    </MiniToolbar>
  </ContextPopup.MiniToolbars>
  <ContextPopup.ContextMenus>
    <ContextMenu Name="ContextMenu">
      <MenuGroup>
        <Button CommandName="cmdCut" />
        <Button CommandName="cmdCopy" />
        <Button CommandName="cmdPaste" />
      </MenuGroup>
    </ContextMenu>
  </ContextPopup.ContextMenus>
  <ContextPopup.ContextMaps>
    <ContextMap CommandName="cmdContextMap" ContextMenu="ContextMenu" MiniToolbar="MiniToolbar"/>
  </ContextPopup.ContextMaps>
</ContextPopup>
```



### <a name="code"></a><span data-ttu-id="f8403-176">Código</span><span class="sxs-lookup"><span data-stu-id="f8403-176">Code</span></span>

<span data-ttu-id="f8403-177">Para invocar un elemento emergente de contexto, se llama al método [**IUIContextualUI:: ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) cuando la ventana de nivel superior de la aplicación de cinta recibe una notificación de CONTEXTMENU de WM \_ .</span><span class="sxs-lookup"><span data-stu-id="f8403-177">To invoke a Context Popup, the [**IUIContextualUI::ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) method is called when the top-level window of the Ribbon application receives a WM\_CONTEXTMENU notification.</span></span>

<span data-ttu-id="f8403-178">En este ejemplo se muestra cómo controlar la \_ notificación de CONTEXTMENU de WM en el método WndProc () de la aplicación de cinta.</span><span class="sxs-lookup"><span data-stu-id="f8403-178">This example demonstrates how to handle the WM\_CONTEXTMENU notification in the WndProc() method of the Ribbon application.</span></span>


```C++
case WM_CONTEXTMENU:
  POINT pt;
  POINTSTOPOINT(pt, lParam);

  // ShowContextualUI method defined by the application.
  ShowContextualUI (pt, hWnd);
  break;
```



<span data-ttu-id="f8403-179">En el ejemplo siguiente se muestra cómo una aplicación de la cinta de opciones puede mostrar el elemento emergente de contexto en una ubicación de pantalla específica mediante el método [**IUIContextualUI:: ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) .</span><span class="sxs-lookup"><span data-stu-id="f8403-179">The following example demonstrates how a Ribbon application can show the Context Popup at a specific screen location using the [**IUIContextualUI::ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) method.</span></span>

<span data-ttu-id="f8403-180">GetCurrentContext () tiene un valor de `cmdContextMap` tal y como se define en el ejemplo de marcación anterior.</span><span class="sxs-lookup"><span data-stu-id="f8403-180">GetCurrentContext() has a value of `cmdContextMap` as defined in the preceding markup example.</span></span>

<span data-ttu-id="f8403-181">g \_ pApplication es una referencia a la interfaz [**IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework) .</span><span class="sxs-lookup"><span data-stu-id="f8403-181">g\_pApplication is a reference to the [**IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework) interface.</span></span>


```C++
HRESULT ShowContextualUI(POINT& ptLocation, HWND hWnd)
{
  GetDisplayLocation(ptLocation, hWnd);

  HRESULT hr = E_FAIL;

  IUIContextualUI* pContextualUI = NULL;
 
  if (SUCCEEDED(g_pFramework->GetView(
                                g_pApplication->GetCurrentContext(), 
                                IID_PPV_ARGS(&pContextualUI))))
  {
    hr = pContextualUI->ShowAtLocation(ptLocation.x, ptLocation.y);
    pContextualUI->Release();
  }

  return hr;
}
```



<span data-ttu-id="f8403-182">La referencia a [**IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui) se puede liberar antes de que se descarte el elemento emergente de contexto, tal como se muestra en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="f8403-182">The reference to [**IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui) can be released before the Context Popup is dismissed, as shown in the preceding example.</span></span> <span data-ttu-id="f8403-183">Sin embargo, se debe liberar la referencia en algún momento para evitar pérdidas de memoria.</span><span class="sxs-lookup"><span data-stu-id="f8403-183">However, the reference must be released at some point to avoid memory leaks.</span></span>

> [!Caution]  
> <span data-ttu-id="f8403-184">El Mini-Toolbar tiene un efecto de atenuación integrado que se basa en la proximidad del puntero del mouse.</span><span class="sxs-lookup"><span data-stu-id="f8403-184">The Mini-Toolbar has a built-in fade effect that is based on the proximity of the mouse pointer.</span></span> <span data-ttu-id="f8403-185">Por esta razón, se recomienda que el Mini-Toolbar se muestre lo más cerca posible del puntero del mouse.</span><span class="sxs-lookup"><span data-stu-id="f8403-185">For this reason, it is recommended that the Mini-Toolbar be displayed as close to the mouse pointer as possible.</span></span> <span data-ttu-id="f8403-186">De lo contrario, debido a los mecanismos de presentación conflictivos, es posible que el Mini-Toolbar no se represente de la manera esperada.</span><span class="sxs-lookup"><span data-stu-id="f8403-186">Otherwise, due to the conflicting display mechanisms, the Mini-Toolbar may not render as expected.</span></span>

 

## <a name="context-popup-properties"></a><span data-ttu-id="f8403-187">Propiedades de elemento emergente de contexto</span><span class="sxs-lookup"><span data-stu-id="f8403-187">Context Popup Properties</span></span>

<span data-ttu-id="f8403-188">No hay claves de propiedad asociadas al control emergente de contexto.</span><span class="sxs-lookup"><span data-stu-id="f8403-188">There are no property keys associated with the Context Popup control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8403-189">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f8403-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8403-190">Biblioteca de controles de Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="f8403-190">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="f8403-191">Ejemplo de ContextPopup</span><span class="sxs-lookup"><span data-stu-id="f8403-191">ContextPopup Sample</span></span>](windowsribbon-contextpopupsample.md)
</dt> </dl>

 

 