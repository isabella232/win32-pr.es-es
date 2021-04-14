---
title: Compatibilidad con tipos de control de UI Automation
description: Esta sección contiene información detallada sobre la estructura de árbol, las propiedades, los patrones de control y los eventos que debe admitir cada tipo de control de automatización de la interfaz de usuario de Microsoft.
ms.assetid: 35232907-6c54-47cd-b82a-0daee279ef17
keywords:
- Automatización de la interfaz de usuario, acerca de los tipos de control
- UI Automation, información general sobre el tipo de control
- compatibilidad con el tipo de control
- tipos de control, compatibilidad
- tipos de controles, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ac6f857da87691428c747cfe5dbff5102218f6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421221"
---
# <a name="supporting-ui-automation-control-types"></a><span data-ttu-id="ac2ee-108">Compatibilidad con tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="ac2ee-108">Supporting UI Automation Control Types</span></span>

<span data-ttu-id="ac2ee-109">Esta sección contiene información detallada sobre la estructura de árbol, las propiedades, los patrones de control y los eventos que debe admitir cada tipo de control de automatización de la interfaz de usuario de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ac2ee-109">This section contains detailed information about the tree structure, properties, control patterns, and events that each Microsoft UI Automation control type is required to support.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ac2ee-110">En esta sección</span><span class="sxs-lookup"><span data-stu-id="ac2ee-110">In this section</span></span>

-   [<span data-ttu-id="ac2ee-111">AppBar (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-111">AppBar Control Type</span></span>](uiauto-supportappbarcontroltype.md)
-   [<span data-ttu-id="ac2ee-112">Button (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-112">Button Control Type</span></span>](uiauto-supportbuttoncontroltype.md)
-   [<span data-ttu-id="ac2ee-113">Calendar (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-113">Calendar Control Type</span></span>](uiauto-supportcalendarcontroltype.md)
-   [<span data-ttu-id="ac2ee-114">CheckBox (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-114">CheckBox Control Type</span></span>](uiauto-supportcheckboxcontroltype.md)
-   [<span data-ttu-id="ac2ee-115">ComboBox (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-115">ComboBox Control Type</span></span>](uiauto-supportcomboboxcontroltype.md)
-   [<span data-ttu-id="ac2ee-116">DataGrid (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-116">DataGrid Control Type</span></span>](uiauto-supportdatagridcontroltype.md)
-   [<span data-ttu-id="ac2ee-117">DataItem (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-117">DataItem Control Type</span></span>](uiauto-supportdataitemcontroltype.md)
-   [<span data-ttu-id="ac2ee-118">Document (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-118">Document Control Type</span></span>](uiauto-supportdocumentcontroltype.md)
-   [<span data-ttu-id="ac2ee-119">Editar tipo de control</span><span class="sxs-lookup"><span data-stu-id="ac2ee-119">Edit Control Type</span></span>](uiauto-supporteditcontroltype.md)
-   [<span data-ttu-id="ac2ee-120">Group (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-120">Group Control Type</span></span>](uiauto-supportgroupcontroltype.md)
-   [<span data-ttu-id="ac2ee-121">Header (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-121">Header Control Type</span></span>](uiauto-supportheadercontroltype.md)
-   [<span data-ttu-id="ac2ee-122">HeaderItem (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-122">HeaderItem Control Type</span></span>](uiauto-supportheaderitemcontroltype.md)
-   [<span data-ttu-id="ac2ee-123">HYPERLINK (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-123">Hyperlink Control Type</span></span>](uiauto-supporthyperlinkcontroltype.md)
-   [<span data-ttu-id="ac2ee-124">Image (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-124">Image Control Type</span></span>](uiauto-supportimagecontroltype.md)
-   [<span data-ttu-id="ac2ee-125">List (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-125">List Control Type</span></span>](uiauto-supportlistcontroltype.md)
-   [<span data-ttu-id="ac2ee-126">ListItem (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-126">ListItem Control Type</span></span>](uiauto-supportlistitemcontroltype.md)
-   [<span data-ttu-id="ac2ee-127">Menu (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-127">Menu Control Type</span></span>](uiauto-supportmenucontroltype.md)
-   [<span data-ttu-id="ac2ee-128">MenuBar (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-128">MenuBar Control Type</span></span>](uiauto-supportmenubarcontroltype.md)
-   [<span data-ttu-id="ac2ee-129">MenuItem (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-129">MenuItem Control Type</span></span>](uiauto-supportmenuitemcontroltype.md)
-   [<span data-ttu-id="ac2ee-130">Pane (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-130">Pane Control Type</span></span>](uiauto-supportpanecontroltype.md)
-   [<span data-ttu-id="ac2ee-131">ProgressBar (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-131">ProgressBar Control Type</span></span>](uiauto-supportprogressbarcontroltype.md)
-   [<span data-ttu-id="ac2ee-132">RadioButton (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-132">RadioButton Control Type</span></span>](uiauto-supportradiobuttoncontroltype.md)
-   [<span data-ttu-id="ac2ee-133">ScrollBar (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-133">ScrollBar Control Type</span></span>](uiauto-supportscrollbarcontroltype.md)
-   [<span data-ttu-id="ac2ee-134">SemanticZoom (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-134">SemanticZoom Control Type</span></span>](/windows/desktop/WinAuto/uiauto-supportsemanticzoomcontroltype)
-   [<span data-ttu-id="ac2ee-135">Separator (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-135">Separator Control Type</span></span>](uiauto-supportseparatorcontroltype.md)
-   [<span data-ttu-id="ac2ee-136">Slide (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-136">Slider Control Type</span></span>](uiauto-supportslidercontroltype.md)
-   [<span data-ttu-id="ac2ee-137">Spinner (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-137">Spinner Control Type</span></span>](uiauto-supportspinnercontroltype.md)
-   [<span data-ttu-id="ac2ee-138">SplitButton (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-138">SplitButton Control Type</span></span>](uiauto-supportsplitbuttoncontroltype.md)
-   [<span data-ttu-id="ac2ee-139">StatusBar (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-139">StatusBar Control Type</span></span>](uiauto-supportstatusbarcontroltype.md)
-   [<span data-ttu-id="ac2ee-140">Tab (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-140">Tab Control Type</span></span>](uiauto-supporttabcontroltype.md)
-   [<span data-ttu-id="ac2ee-141">TabItem (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-141">TabItem Control Type</span></span>](uiauto-supporttabitemcontroltype.md)
-   [<span data-ttu-id="ac2ee-142">Table (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-142">Table Control Type</span></span>](uiauto-supporttablecontroltype.md)
-   [<span data-ttu-id="ac2ee-143">Text (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-143">Text Control Type</span></span>](uiauto-supporttextcontroltype.md)
-   [<span data-ttu-id="ac2ee-144">Thumb (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-144">Thumb Control Type</span></span>](uiauto-supportthumbcontroltype.md)
-   [<span data-ttu-id="ac2ee-145">TitleBar (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-145">TitleBar Control Type</span></span>](uiauto-supporttitlebarcontroltype.md)
-   [<span data-ttu-id="ac2ee-146">ToolBar (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-146">ToolBar Control Type</span></span>](uiauto-supporttoolbarcontroltype.md)
-   [<span data-ttu-id="ac2ee-147">ToolTip (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-147">ToolTip Control Type</span></span>](uiauto-supporttooltipcontroltype.md)
-   [<span data-ttu-id="ac2ee-148">Tree (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-148">Tree Control Type</span></span>](uiauto-supporttreecontroltype.md)
-   [<span data-ttu-id="ac2ee-149">Tipo de control TreeItem</span><span class="sxs-lookup"><span data-stu-id="ac2ee-149">TreeItem Control Type</span></span>](uiauto-supporttreeitemcontroltype.md)
-   [<span data-ttu-id="ac2ee-150">Window (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ac2ee-150">Window Control Type</span></span>](uiauto-supportwindowcontroltype.md)

## <a name="related-topics"></a><span data-ttu-id="ac2ee-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ac2ee-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac2ee-152">Guía del programador del proveedor de UI Automation</span><span class="sxs-lookup"><span data-stu-id="ac2ee-152">UI Automation Provider Programmer's Guide</span></span>](uiauto-providerportal.md)
</dt> </dl>

 

 