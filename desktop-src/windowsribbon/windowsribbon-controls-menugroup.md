---
title: Grupo de menús
description: El grupo de menús organiza los comandos y controles relacionados dentro de un menú o una barra de herramientas.
ms.assetid: 5454f2a3-275b-47f4-ae97-d10dd12da5ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9862e78cbedf84b92c7540bec4de58288af5c9ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995522"
---
# <a name="menu-group"></a><span data-ttu-id="d08c6-103">Grupo de menús</span><span class="sxs-lookup"><span data-stu-id="d08c6-103">Menu Group</span></span>

<span data-ttu-id="d08c6-104">El grupo de menús organiza los comandos y controles relacionados dentro de un menú o una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="d08c6-104">The Menu Group organizes related Commands and controls within a menu or toolbar.</span></span>

-   [<span data-ttu-id="d08c6-105">Introducción</span><span class="sxs-lookup"><span data-stu-id="d08c6-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="d08c6-106">Propiedades del grupo de menús</span><span class="sxs-lookup"><span data-stu-id="d08c6-106">Menu Group Properties</span></span>](#menu-group-properties)
-   [<span data-ttu-id="d08c6-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d08c6-107">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="d08c6-108">Introducción</span><span class="sxs-lookup"><span data-stu-id="d08c6-108">Introduction</span></span>

<span data-ttu-id="d08c6-109">El control de grupo de menús, expuesto a través del elemento de marcado [**MenuGroup**](windowsribbon-element-menugroup.md) , es un contenedor lógico para grupos de elementos o comandos en controles basados en menús, incluida la minibarra de herramientas [emergente contextual](windowsribbon-controls-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="d08c6-109">The Menu Group control, exposed through the [**MenuGroup**](windowsribbon-element-menugroup.md) markup element, is a logical container for groups of items or Commands in menu-based controls, including the [Context Popup](windowsribbon-controls-contextpopup.md) Mini-Toolbar.</span></span>

<span data-ttu-id="d08c6-110">Se puede especificar una etiqueta para un grupo de menús mediante el atributo *LabelTitle* o la propiedad [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) de una declaración de comando asociada.</span><span class="sxs-lookup"><span data-stu-id="d08c6-110">A label can be specified for a Menu Group through the *LabelTitle* attribute or [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) property of an associated Command declaration.</span></span> <span data-ttu-id="d08c6-111">El valor asignado a *LabelTitle* se representa como un encabezado de categoría.</span><span class="sxs-lookup"><span data-stu-id="d08c6-111">The value assigned to *LabelTitle* is rendered as a category header.</span></span>

<span data-ttu-id="d08c6-112">En el ejemplo siguiente se muestra el marcado de comandos de un control de [botón de expansión](windowsribbon-controls-splitbutton.md) que incluye dos declaraciones de comandos de grupo de menús.</span><span class="sxs-lookup"><span data-stu-id="d08c6-112">The following example demonstrates the Command markup for a [Split Button](windowsribbon-controls-splitbutton.md) control that includes two Menu Group Command declarations.</span></span>


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



<span data-ttu-id="d08c6-113">En el ejemplo siguiente se muestra el marcado necesario para un elemento [**splitButton**](windowsribbon-element-splitbutton.md) con tres declaraciones de elementos [**MenuGroup**](windowsribbon-element-menugroup.md) , dos de las cuales están asociadas a los comandos del grupo de menús del ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="d08c6-113">The following example demonstrates the markup required for a [**SplitButton**](windowsribbon-element-splitbutton.md) element with three [**MenuGroup**](windowsribbon-element-menugroup.md) element declarations, two of which are associated with the Menu Group Commands from the previous example.</span></span> <span data-ttu-id="d08c6-114">El atributo *Class* del elemento **MenuGroup** se usa para especificar el tamaño de los elementos de menú.</span><span class="sxs-lookup"><span data-stu-id="d08c6-114">The *Class* attribute of the **MenuGroup** element is used to specify the size of the menu items.</span></span>


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



<span data-ttu-id="d08c6-115">En la siguiente captura de pantalla se muestra el menú (con tres controles de grupo de menús) que se genera a partir del marcado en los ejemplos anteriores.</span><span class="sxs-lookup"><span data-stu-id="d08c6-115">The following screen shot illustrates the menu (with three Menu Group controls) that is generated from the markup in the previous examples.</span></span>

![captura de pantalla de un menú con tres controles de grupo de menús.](images/controls/menugroup.png)

## <a name="menu-group-properties"></a><span data-ttu-id="d08c6-117">Propiedades del grupo de menús</span><span class="sxs-lookup"><span data-stu-id="d08c6-117">Menu Group Properties</span></span>

<span data-ttu-id="d08c6-118">El marco de cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control de grupo de menús.</span><span class="sxs-lookup"><span data-stu-id="d08c6-118">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Menu Group control.</span></span>

<span data-ttu-id="d08c6-119">Normalmente, una propiedad de grupo de menús se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control a través de una llamada al método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="d08c6-119">Typically, a Menu Group property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="d08c6-120">Se controla el evento de invalidación y las actualizaciones de propiedades definidas por el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="d08c6-120">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="d08c6-121">No se ejecuta el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y la aplicación solicitó un valor de propiedad actualizado hasta que el marco de trabajo requiera la propiedad.</span><span class="sxs-lookup"><span data-stu-id="d08c6-121">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="d08c6-122">Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="d08c6-122">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="d08c6-123">En algunos casos, una propiedad se puede recuperar a través del método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="d08c6-123">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="d08c6-124">En la tabla siguiente se enumeran las claves de propiedad que están asociadas al control de grupo de menús.</span><span class="sxs-lookup"><span data-stu-id="d08c6-124">The following table lists the property keys that are associated with the Menu Group control.</span></span>



| <span data-ttu-id="d08c6-125">Clave de propiedad</span><span class="sxs-lookup"><span data-stu-id="d08c6-125">Property Key</span></span>                                                                                     | <span data-ttu-id="d08c6-126">Notas</span><span class="sxs-lookup"><span data-stu-id="d08c6-126">Notes</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d08c6-127">PKEY de IU \_ \_ habilitada</span><span class="sxs-lookup"><span data-stu-id="d08c6-127">UI\_PKEY\_Enabled</span></span>](windowsribbon-reference-properties-uipkey-enabled.md)                       | <span data-ttu-id="d08c6-128">Admite [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="d08c6-128">Supports [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) and [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> |
| [<span data-ttu-id="d08c6-129">KeyTip de UI \_ PKEY \_</span><span class="sxs-lookup"><span data-stu-id="d08c6-129">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                         | <span data-ttu-id="d08c6-130">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="d08c6-130">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="d08c6-131">\_Etiqueta PKEY de IU \_</span><span class="sxs-lookup"><span data-stu-id="d08c6-131">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                           | <span data-ttu-id="d08c6-132">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="d08c6-132">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="d08c6-133">UI \_ PKEY \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="d08c6-133">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="d08c6-134">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="d08c6-134">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="d08c6-135">UI \_ PKEY \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="d08c6-135">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="d08c6-136">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="d08c6-136">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="d08c6-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d08c6-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d08c6-138">Biblioteca de controles de Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="d08c6-138">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="d08c6-139">**Elemento de marcado MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="d08c6-139">**MenuGroup markup element**</span></span>](windowsribbon-element-menugroup.md)
</dt> </dl>

 

 