---
description: En la tabla EventMapping se muestran los controles que se suscriben a algunos eventos de control y se enumera el atributo que se va a cambiar cuando otro control o el Windows Installer publiquen el evento.
ms.assetid: 63c9ba3e-aa8a-475b-8360-4aec78ed19db
title: Tabla EventMapping
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e9a7b5b4283b5d70102123dcb11e3e9e844221
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908857"
---
# <a name="eventmapping-table"></a><span data-ttu-id="83881-103">Tabla EventMapping</span><span class="sxs-lookup"><span data-stu-id="83881-103">EventMapping Table</span></span>

<span data-ttu-id="83881-104">En la tabla EventMapping se muestran los controles que se suscriben a algunos eventos de control y se enumera el atributo que se va a cambiar cuando otro control o el Windows Installer publiquen el evento.</span><span class="sxs-lookup"><span data-stu-id="83881-104">The EventMapping Table lists the controls that subscribe to some control events, and lists the attribute to be changed when the event is published by another control or the Windows Installer.</span></span>

<span data-ttu-id="83881-105">La tabla EventMapping tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="83881-105">The EventMapping Table has the following columns.</span></span>



| <span data-ttu-id="83881-106">Columna</span><span class="sxs-lookup"><span data-stu-id="83881-106">Column</span></span>    | <span data-ttu-id="83881-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="83881-107">Type</span></span>                         | <span data-ttu-id="83881-108">Clave</span><span class="sxs-lookup"><span data-stu-id="83881-108">Key</span></span> | <span data-ttu-id="83881-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="83881-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="83881-110">Diálogo\_</span><span class="sxs-lookup"><span data-stu-id="83881-110">Dialog\_</span></span>  | [<span data-ttu-id="83881-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="83881-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="83881-112">Y</span><span class="sxs-lookup"><span data-stu-id="83881-112">Y</span></span>   | <span data-ttu-id="83881-113">N</span><span class="sxs-lookup"><span data-stu-id="83881-113">N</span></span>        |
| <span data-ttu-id="83881-114">control\_</span><span class="sxs-lookup"><span data-stu-id="83881-114">Control\_</span></span> | [<span data-ttu-id="83881-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="83881-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="83881-116">Y</span><span class="sxs-lookup"><span data-stu-id="83881-116">Y</span></span>   | <span data-ttu-id="83881-117">N</span><span class="sxs-lookup"><span data-stu-id="83881-117">N</span></span>        |
| <span data-ttu-id="83881-118">Evento</span><span class="sxs-lookup"><span data-stu-id="83881-118">Event</span></span>     | [<span data-ttu-id="83881-119">Identificador</span><span class="sxs-lookup"><span data-stu-id="83881-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="83881-120">Y</span><span class="sxs-lookup"><span data-stu-id="83881-120">Y</span></span>   | <span data-ttu-id="83881-121">N</span><span class="sxs-lookup"><span data-stu-id="83881-121">N</span></span>        |
| <span data-ttu-id="83881-122">Atributo</span><span class="sxs-lookup"><span data-stu-id="83881-122">Attribute</span></span> | [<span data-ttu-id="83881-123">Identificador</span><span class="sxs-lookup"><span data-stu-id="83881-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="83881-124">N</span><span class="sxs-lookup"><span data-stu-id="83881-124">N</span></span>   | <span data-ttu-id="83881-125">N</span><span class="sxs-lookup"><span data-stu-id="83881-125">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="83881-126">Columnas</span><span class="sxs-lookup"><span data-stu-id="83881-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="83881-127"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Diálogo\_</span><span class="sxs-lookup"><span data-stu-id="83881-127"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialog\_</span></span>
</dt> <dd>

<span data-ttu-id="83881-128">Una clave externa a la primera columna de la [tabla del cuadro de diálogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="83881-128">An external key to the first column of the [Dialog Table](dialog-table.md).</span></span> <span data-ttu-id="83881-129">Este campo y el campo de control \_ identifican un control.</span><span class="sxs-lookup"><span data-stu-id="83881-129">This field and the Control\_ field together identify a control.</span></span>

</dd> <dt>

<span data-ttu-id="83881-130"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Control\_</span><span class="sxs-lookup"><span data-stu-id="83881-130"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Control\_</span></span>
</dt> <dd>

<span data-ttu-id="83881-131">Una clave externa a la segunda columna de la [tabla de control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="83881-131">An external key to the second column of the [Control Table](control-table.md).</span></span> <span data-ttu-id="83881-132">Este campo y el campo de diálogo \_ juntos identifican un control.</span><span class="sxs-lookup"><span data-stu-id="83881-132">This field and the Dialog\_ field together identify a control.</span></span>

</dd> <dt>

<span data-ttu-id="83881-133"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Ceso</span><span class="sxs-lookup"><span data-stu-id="83881-133"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="83881-134">Este campo es un identificador que especifica el tipo de evento al que se suscribe el control.</span><span class="sxs-lookup"><span data-stu-id="83881-134">This field is an identifier that specifies the type of event that is subscribed to by the control.</span></span> <span data-ttu-id="83881-135">Para obtener más información, consulte [información general de ControlEvent,](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="83881-135">For more information, see [ControlEvent Overview](controlevent-overview.md).</span></span>

</dd> <dt>

<span data-ttu-id="83881-136"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Atribui</span><span class="sxs-lookup"><span data-stu-id="83881-136"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span></span>
</dt> <dd>

<span data-ttu-id="83881-137">Nombre del atributo de control \_ que se establece cuando se recibe el evento en la columna de evento.</span><span class="sxs-lookup"><span data-stu-id="83881-137">The name of the Control\_ attribute that is set when the event in the Event column is received.</span></span> <span data-ttu-id="83881-138">El argumento del evento se pasa como argumento de la llamada de atributo para cambiar este atributo del control.</span><span class="sxs-lookup"><span data-stu-id="83881-138">The Argument of the event is passed as the argument of the attribute call to change this attribute of the control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83881-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="83881-139">Remarks</span></span>

<span data-ttu-id="83881-140">La [tabla ControlEvent,](controlevent-table.md) especifica los eventos de control que se inician cuando un usuario interactúa con un control [Pushbutton](pushbutton-control.md), un [control CheckBox](checkbox-control.md)o un [control SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="83881-140">The [ControlEvent Table](controlevent-table.md) specifies the control events that are started when a user interacts with a [PushButton Control](pushbutton-control.md), [CheckBox Control](checkbox-control.md), or [SelectionTree Control](selectiontree-control.md).</span></span> <span data-ttu-id="83881-141">Estos son los únicos controles que un usuario puede usar para iniciar eventos de control.</span><span class="sxs-lookup"><span data-stu-id="83881-141">These are the only controls that a user can use to initiate control events.</span></span>

<span data-ttu-id="83881-142">Hay más de un control en un cuadro de diálogo que se puede suscribir al mismo evento.</span><span class="sxs-lookup"><span data-stu-id="83881-142">More than one control on a dialog box can subscribe to the same event.</span></span>

<span data-ttu-id="83881-143">En la lista siguiente se identifican los usos típicos de la tabla EventMapping:</span><span class="sxs-lookup"><span data-stu-id="83881-143">The following list identifies the typical uses for the EventMapping Table:</span></span>

-   <span data-ttu-id="83881-144">Para suscribir [un control de texto](text-control.md) a un ControlEvent, de [ActionText](actiontext-controlevent.md), [ActionData ControlEvent,](actiondata-controlevent.md), [ScriptInProgress controlevent,](scriptinprogress-controlevent.md) o [TimeRemaining ControlEvent,](timeremaining-controlevent.md) publicado por el Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="83881-144">To subscribe a [Text Control](text-control.md) to an [ActionText ControlEvent](actiontext-controlevent.md), [ActionData ControlEvent](actiondata-controlevent.md), [ScriptInProgress ControlEvent](scriptinprogress-controlevent.md) or [TimeRemaining ControlEvent](timeremaining-controlevent.md) published by the Windows Installer.</span></span>
-   <span data-ttu-id="83881-145">Para suscribir un control [ProgressBar](progressbar-control.md) o un control de la [cartelera](billboard-control.md) a un [ControlEvent, de SetProgress](setprogress-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="83881-145">To subscribe a [ProgressBar Control](progressbar-control.md) or [Billboard Control](billboard-control.md) to a [SetProgress ControlEvent](setprogress-controlevent.md).</span></span>
-   <span data-ttu-id="83881-146">Para suscribir un [control DirectoryCombo](directorycombo-control.md) a un [ControlEvent, de IgnoreChange](ignorechange-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="83881-146">To subscribe a [DirectoryCombo Control](directorycombo-control.md) to an [IgnoreChange ControlEvent](ignorechange-controlevent.md).</span></span>
-   <span data-ttu-id="83881-147">Para deshabilitar automáticamente un [control Pushbutton](pushbutton-control.md) situado en el mismo cuadro de diálogo con un [control SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="83881-147">To automatically disable a [PushButton Control](pushbutton-control.md) located on the same dialog with a [SelectionTree Control](selectiontree-control.md).</span></span> <span data-ttu-id="83881-148">Para deshabilitar el botón de control cuando no aparezca ninguna característica en el [control SelectionTree](selectiontree-control.md), use la tabla EventMapping para suscribir el control Pushbutton a un [SelectionNoItems ControlEvent,](selectionnoitems-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="83881-148">To disable the push button when no features are listed in the [SelectionTree Control](selectiontree-control.md), use the EventMapping Table to subscribe the PushButton control to a [SelectionNoItems ControlEvent](selectionnoitems-controlevent.md).</span></span> <span data-ttu-id="83881-149">Escriba **enable** en el campo Attributes de la tabla EventMapping.</span><span class="sxs-lookup"><span data-stu-id="83881-149">Enter **Enable** in the Attributes field of the EventMapping Table.</span></span>
-   <span data-ttu-id="83881-150">Para mostrar un [control de texto](text-control.md) que muestra la ruta de acceso a la ubicación de instalación de la característica seleccionada en un [control SelectionTree](selectiontree-control.md) en el mismo cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="83881-150">To display a [Text Control](text-control.md) that shows the path to the installation location for the feature that is selected in a [SelectionTree Control](selectiontree-control.md) on the same dialog.</span></span> <span data-ttu-id="83881-151">Use la tabla EventMapping para suscribir [el control de texto](text-control.md) a [SelectionPathOn ControlEvent,](selectionpathon-controlevent.md) y [SelectionPath ControlEvent,](selectionpath-controlevent.md) publicado por el [control SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="83881-151">Use the EventMapping Table to subscribe the [Text Control](text-control.md) to both a [SelectionPathOn ControlEvent](selectionpathon-controlevent.md) and [SelectionPath ControlEvent](selectionpath-controlevent.md) published by the [SelectionTree Control](selectiontree-control.md).</span></span>
-   <span data-ttu-id="83881-152">Para mostrar un [control de texto](text-control.md) que muestre una descripción del elemento resaltado en un [control SelectionTree](selectiontree-control.md) ubicado en el mismo cuadro de diálogo, use la tabla EventMapping para suscribir el [control de texto](text-control.md) a [SelectionDescription ControlEvent,](selectiondescription-controlevent.md), [SelectionSize ControlEvent,](selectionsize-controlevent.md) o [SelectionAction ControlEvent,](selectionaction-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="83881-152">To display a [Text Control](text-control.md) that shows a description of the item highlighted in a [SelectionTree Control](selectiontree-control.md) located on the same dialog, use the EventMapping Table to subscribe the [Text Control](text-control.md) to a [SelectionDescription ControlEvent](selectiondescription-controlevent.md), [SelectionSize ControlEvent](selectionsize-controlevent.md) or [SelectionAction ControlEvent](selectionaction-controlevent.md).</span></span> <span data-ttu-id="83881-153">Escriba el **texto** en el campo atributo de la tabla EventMapping.</span><span class="sxs-lookup"><span data-stu-id="83881-153">Enter **Text** in the Attribute field of the EventMapping Table.</span></span>

## <a name="validation"></a><span data-ttu-id="83881-154">Validación</span><span class="sxs-lookup"><span data-stu-id="83881-154">Validation</span></span>

<dl>

[<span data-ttu-id="83881-155">ICE03</span><span class="sxs-lookup"><span data-stu-id="83881-155">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="83881-156">ICE06</span><span class="sxs-lookup"><span data-stu-id="83881-156">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="83881-157">ICE32</span><span class="sxs-lookup"><span data-stu-id="83881-157">ICE32</span></span>](ice32.md)  
</dl>

 

 



