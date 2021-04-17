---
title: Implementar patrones de control de UI Automation
description: En esta sección se proporciona información detallada sobre cómo implementar las interfaces del proveedor de automatización de la interfaz de usuario de Microsoft que admiten patrones de control.
ms.assetid: d1baa245-62a1-40b1-a671-e227dd3df60a
keywords:
- Automatización de la interfaz de usuario, implementar patrones de control
- Automatización de la interfaz de usuario, patrones de control
- implementar patrones de control de UI Automation
- patrones de control, implementación de la automatización de la interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfb75b6b275fee9230eb25d9a0b02e1da26ad4d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105704985"
---
# <a name="implementing-ui-automation-control-patterns"></a><span data-ttu-id="38b2b-107">Implementar patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="38b2b-107">Implementing UI Automation Control Patterns</span></span>

<span data-ttu-id="38b2b-108">En esta sección se proporciona información detallada sobre cómo implementar las interfaces del proveedor de automatización de la interfaz de usuario de Microsoft que admiten patrones de control.</span><span class="sxs-lookup"><span data-stu-id="38b2b-108">This section provides detailed information about implementing the Microsoft UI Automation provider interfaces that support control patterns.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="38b2b-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="38b2b-109">In this section</span></span>

-   [<span data-ttu-id="38b2b-110">Patrón de control Annotation</span><span class="sxs-lookup"><span data-stu-id="38b2b-110">Annotation Control Pattern</span></span>](uiauto-implementingannotation.md)
-   [<span data-ttu-id="38b2b-111">Patrón de control CustomNavigation</span><span class="sxs-lookup"><span data-stu-id="38b2b-111">CustomNavigation Control Pattern</span></span>](uiauto-implementingcustomnavigation.md)
-   [<span data-ttu-id="38b2b-112">Dock (patrón de control)</span><span class="sxs-lookup"><span data-stu-id="38b2b-112">Dock Control Pattern</span></span>](uiauto-implementingdock.md)
-   [<span data-ttu-id="38b2b-113">Arrastrar patrón de control</span><span class="sxs-lookup"><span data-stu-id="38b2b-113">Drag Control Pattern</span></span>](/windows/desktop/WinAuto/uiauto-implementingdrag)
-   [<span data-ttu-id="38b2b-114">Patrón de control DropTarget</span><span class="sxs-lookup"><span data-stu-id="38b2b-114">DropTarget Control Pattern</span></span>](/windows/desktop/WinAuto/uiauto-implementingdroptarget)
-   [<span data-ttu-id="38b2b-115">Patrón de control ExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="38b2b-115">ExpandCollapse Control Pattern</span></span>](uiauto-implementingexpandcollapse.md)
-   [<span data-ttu-id="38b2b-116">Grid (patrón de control)</span><span class="sxs-lookup"><span data-stu-id="38b2b-116">Grid Control Pattern</span></span>](uiauto-implementinggrid.md)
-   [<span data-ttu-id="38b2b-117">GridItem (patrón de control)</span><span class="sxs-lookup"><span data-stu-id="38b2b-117">GridItem Control Pattern</span></span>](uiauto-implementinggriditem.md)
-   [<span data-ttu-id="38b2b-118">Invocar patrón de control</span><span class="sxs-lookup"><span data-stu-id="38b2b-118">Invoke Control Pattern</span></span>](uiauto-implementinginvoke.md)
-   [<span data-ttu-id="38b2b-119">Patrón de control ItemContainer</span><span class="sxs-lookup"><span data-stu-id="38b2b-119">ItemContainer Control Pattern</span></span>](uiauto-implementingitemcontainer.md)
-   [<span data-ttu-id="38b2b-120">Patrón de control LegacyIAccessible</span><span class="sxs-lookup"><span data-stu-id="38b2b-120">LegacyIAccessible Control Pattern</span></span>](uiauto-implementinglegacyiaccessible.md)
-   [<span data-ttu-id="38b2b-121">Patrón de control MultipleView</span><span class="sxs-lookup"><span data-stu-id="38b2b-121">MultipleView Control Pattern</span></span>](uiauto-implementingmultipleview.md)
-   [<span data-ttu-id="38b2b-122">ObjectModel (patrón de control)</span><span class="sxs-lookup"><span data-stu-id="38b2b-122">ObjectModel Control Pattern</span></span>](uiauto-implementingobjectmodel.md)
-   [<span data-ttu-id="38b2b-123">Patrón de control RangeValue</span><span class="sxs-lookup"><span data-stu-id="38b2b-123">RangeValue Control Pattern</span></span>](uiauto-implementingrangevalue.md)
-   [<span data-ttu-id="38b2b-124">Scroll (patrón de control)</span><span class="sxs-lookup"><span data-stu-id="38b2b-124">Scroll Control Pattern</span></span>](uiauto-implementingscroll.md)
-   [<span data-ttu-id="38b2b-125">Patrón de control ScrollItem</span><span class="sxs-lookup"><span data-stu-id="38b2b-125">ScrollItem Control Pattern</span></span>](uiauto-implementingscrollitem.md)
-   [<span data-ttu-id="38b2b-126">Selection (patrón de control)</span><span class="sxs-lookup"><span data-stu-id="38b2b-126">Selection Control Pattern</span></span>](uiauto-implementingselection.md)
-   [<span data-ttu-id="38b2b-127">Patrón de control SelectionItem</span><span class="sxs-lookup"><span data-stu-id="38b2b-127">SelectionItem Control Pattern</span></span>](uiauto-implementingselectionitem.md)
-   [<span data-ttu-id="38b2b-128">Patrón de control de hoja de cálculo</span><span class="sxs-lookup"><span data-stu-id="38b2b-128">Spreadsheet Control Pattern</span></span>](uiauto-implementingspreadsheet.md)
-   [<span data-ttu-id="38b2b-129">Patrón de control SpreadsheetItem</span><span class="sxs-lookup"><span data-stu-id="38b2b-129">SpreadsheetItem Control Pattern</span></span>](uiauto-implementingspreadsheetitem.md)
-   [<span data-ttu-id="38b2b-130">Styles (patrón de control)</span><span class="sxs-lookup"><span data-stu-id="38b2b-130">Styles Control Pattern</span></span>](/windows/desktop/WinAuto/uiauto-implementingstyles)
-   [<span data-ttu-id="38b2b-131">Patrón de control SynchronizedInput</span><span class="sxs-lookup"><span data-stu-id="38b2b-131">SynchronizedInput Control Pattern</span></span>](uiauto-implementingsynchronizedinput.md)
-   [<span data-ttu-id="38b2b-132">Table (patrón de control)</span><span class="sxs-lookup"><span data-stu-id="38b2b-132">Table Control Pattern</span></span>](uiauto-implementingtable.md)
-   [<span data-ttu-id="38b2b-133">Patrón de control TableItem</span><span class="sxs-lookup"><span data-stu-id="38b2b-133">TableItem Control Pattern</span></span>](uiauto-implementingtableitem.md)
-   [<span data-ttu-id="38b2b-134">Patrones de control Text y TextRange</span><span class="sxs-lookup"><span data-stu-id="38b2b-134">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
-   [<span data-ttu-id="38b2b-135">Patrón de control TextChild</span><span class="sxs-lookup"><span data-stu-id="38b2b-135">TextChild Control Pattern</span></span>](textchild-control-pattern.md)
-   [<span data-ttu-id="38b2b-136">Patrón de control TextEdit</span><span class="sxs-lookup"><span data-stu-id="38b2b-136">TextEdit Control Pattern</span></span>](textedit-control-pattern.md)
-   [<span data-ttu-id="38b2b-137">Alternar patrón de control</span><span class="sxs-lookup"><span data-stu-id="38b2b-137">Toggle Control Pattern</span></span>](uiauto-implementingtoggle.md)
-   [<span data-ttu-id="38b2b-138">Transform (patrón de control)</span><span class="sxs-lookup"><span data-stu-id="38b2b-138">Transform Control Pattern</span></span>](uiauto-implementingtransform.md)
-   [<span data-ttu-id="38b2b-139">Value (patrón de control)</span><span class="sxs-lookup"><span data-stu-id="38b2b-139">Value Control Pattern</span></span>](uiauto-implementingvalue.md)
-   [<span data-ttu-id="38b2b-140">Patrón de control VirtualizedItem</span><span class="sxs-lookup"><span data-stu-id="38b2b-140">VirtualizedItem Control Pattern</span></span>](uiauto-implementingvirtualizeditem.md)
-   [<span data-ttu-id="38b2b-141">Window (patrón de control)</span><span class="sxs-lookup"><span data-stu-id="38b2b-141">Window Control Pattern</span></span>](uiauto-implementingwindow.md)

## <a name="related-topics"></a><span data-ttu-id="38b2b-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="38b2b-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38b2b-143">Guía del programador del proveedor de UI Automation</span><span class="sxs-lookup"><span data-stu-id="38b2b-143">UI Automation Provider Programmer's Guide</span></span>](uiauto-providerportal.md)
</dt> <dt>

[<span data-ttu-id="38b2b-144">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="38b2b-144">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="38b2b-145">Compatibilidad con tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="38b2b-145">Supporting UI Automation Control Types</span></span>](uiauto-supportinguiautocontroltypes.md)
</dt> </dl>

 

 