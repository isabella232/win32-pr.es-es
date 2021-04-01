---
description: La tabla ControlEvent, permite al autor especificar los eventos de control iniciados cuando un usuario interactúa con un control PushButton, un control CheckBox o un control SelectionTree.
ms.assetid: e34d17e9-cd6b-4a21-9abc-9562ee648c59
title: Tabla ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 721dc7ac9a729b8df0623a2958a4d0fe32851307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913081"
---
# <a name="controlevent-table"></a><span data-ttu-id="65071-103">Tabla ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="65071-103">ControlEvent Table</span></span>

<span data-ttu-id="65071-104">La tabla ControlEvent, permite al autor especificar los [eventos de control](control-events.md) iniciados cuando un usuario interactúa con un control [Pushbutton](pushbutton-control.md), un [control CheckBox](checkbox-control.md)o un [control SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="65071-104">The ControlEvent table allows the author to specify the [Control Events](control-events.md) started when a user interacts with a [PushButton Control](pushbutton-control.md), [CheckBox Control](checkbox-control.md), or [SelectionTree Control](selectiontree-control.md).</span></span> <span data-ttu-id="65071-105">Estos son los únicos controles que los usuarios pueden usar para iniciar eventos de control.</span><span class="sxs-lookup"><span data-stu-id="65071-105">These are the only controls users can use to initiate control events.</span></span> <span data-ttu-id="65071-106">Cada control puede publicar varios eventos de control.</span><span class="sxs-lookup"><span data-stu-id="65071-106">Each control can publish multiple control events.</span></span> <span data-ttu-id="65071-107">El instalador inicia cada evento en el orden especificado en la columna de ordenación.</span><span class="sxs-lookup"><span data-stu-id="65071-107">The installer starts each event in the order specified in the Ordering column.</span></span> <span data-ttu-id="65071-108">Por ejemplo, un control de botón de control puede publicar eventos para iniciar una transición a otro cuadro de diálogo, salir de la secuencia del cuadro de diálogo e iniciar la instalación del archivo.</span><span class="sxs-lookup"><span data-stu-id="65071-108">For example, a push button control can publish events to initiate a transition to another dialog box, exit the dialog box sequence, and begin file installation.</span></span>

<span data-ttu-id="65071-109">La excepción a tener en cuenta es que cada control puede publicar más de un [NewDialog](newdialog-controlevent.md) o un evento [SpawnDialog](spawndialog-controlevent.md) .</span><span class="sxs-lookup"><span data-stu-id="65071-109">The exception to note is that each control can publish a most one [NewDialog](newdialog-controlevent.md) or one [SpawnDialog](spawndialog-controlevent.md) event.</span></span> <span data-ttu-id="65071-110">Si tiene que crear varios eventos de control NewDialog y SpawnDialog en esta tabla, incluya también instrucciones condicionales en los campos condición que garanticen que se publica como máximo un evento.</span><span class="sxs-lookup"><span data-stu-id="65071-110">If you need to author multiple NewDialog and SpawnDialog control events in this table, also include conditional statements in the Condition fields that ensure at most one event is published.</span></span> <span data-ttu-id="65071-111">Si se seleccionan varios eventos de control NewDialog y SpawnDialog para el mismo control, solo se publica el evento con el valor más grande de la columna de ordenación cuando se activa el control.</span><span class="sxs-lookup"><span data-stu-id="65071-111">If multiple NewDialog and SpawnDialog control events are selected for the same control, only the event with the largest value in the Ordering column gets published when the control is activated.</span></span>

<span data-ttu-id="65071-112">La tabla ControlEvent, tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="65071-112">The ControlEvent table has the following columns.</span></span>



| <span data-ttu-id="65071-113">Columna</span><span class="sxs-lookup"><span data-stu-id="65071-113">Column</span></span>    | <span data-ttu-id="65071-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="65071-114">Type</span></span>                         | <span data-ttu-id="65071-115">Clave</span><span class="sxs-lookup"><span data-stu-id="65071-115">Key</span></span> | <span data-ttu-id="65071-116">Nullable</span><span class="sxs-lookup"><span data-stu-id="65071-116">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="65071-117">Diálogo\_</span><span class="sxs-lookup"><span data-stu-id="65071-117">Dialog\_</span></span>  | [<span data-ttu-id="65071-118">Identificador</span><span class="sxs-lookup"><span data-stu-id="65071-118">Identifier</span></span>](identifier.md) | <span data-ttu-id="65071-119">Y</span><span class="sxs-lookup"><span data-stu-id="65071-119">Y</span></span>   | <span data-ttu-id="65071-120">N</span><span class="sxs-lookup"><span data-stu-id="65071-120">N</span></span>        |
| <span data-ttu-id="65071-121">control\_</span><span class="sxs-lookup"><span data-stu-id="65071-121">Control\_</span></span> | [<span data-ttu-id="65071-122">Identificador</span><span class="sxs-lookup"><span data-stu-id="65071-122">Identifier</span></span>](identifier.md) | <span data-ttu-id="65071-123">Y</span><span class="sxs-lookup"><span data-stu-id="65071-123">Y</span></span>   | <span data-ttu-id="65071-124">N</span><span class="sxs-lookup"><span data-stu-id="65071-124">N</span></span>        |
| <span data-ttu-id="65071-125">Evento</span><span class="sxs-lookup"><span data-stu-id="65071-125">Event</span></span>     | [<span data-ttu-id="65071-126">Formatea</span><span class="sxs-lookup"><span data-stu-id="65071-126">Formatted</span></span>](formatted.md)   | <span data-ttu-id="65071-127">Y</span><span class="sxs-lookup"><span data-stu-id="65071-127">Y</span></span>   | <span data-ttu-id="65071-128">N</span><span class="sxs-lookup"><span data-stu-id="65071-128">N</span></span>        |
| <span data-ttu-id="65071-129">Argumento</span><span class="sxs-lookup"><span data-stu-id="65071-129">Argument</span></span>  | [<span data-ttu-id="65071-130">Formatea</span><span class="sxs-lookup"><span data-stu-id="65071-130">Formatted</span></span>](formatted.md)   | <span data-ttu-id="65071-131">Y</span><span class="sxs-lookup"><span data-stu-id="65071-131">Y</span></span>   | <span data-ttu-id="65071-132">N</span><span class="sxs-lookup"><span data-stu-id="65071-132">N</span></span>        |
| <span data-ttu-id="65071-133">Condición</span><span class="sxs-lookup"><span data-stu-id="65071-133">Condition</span></span> | [<span data-ttu-id="65071-134">Condition</span><span class="sxs-lookup"><span data-stu-id="65071-134">Condition</span></span>](condition.md)   | <span data-ttu-id="65071-135">Y</span><span class="sxs-lookup"><span data-stu-id="65071-135">Y</span></span>   | <span data-ttu-id="65071-136">Y</span><span class="sxs-lookup"><span data-stu-id="65071-136">Y</span></span>        |
| <span data-ttu-id="65071-137">Ordenación</span><span class="sxs-lookup"><span data-stu-id="65071-137">Ordering</span></span>  | [<span data-ttu-id="65071-138">Entero</span><span class="sxs-lookup"><span data-stu-id="65071-138">Integer</span></span>](integer.md)       | <span data-ttu-id="65071-139">N</span><span class="sxs-lookup"><span data-stu-id="65071-139">N</span></span>   | <span data-ttu-id="65071-140">Y</span><span class="sxs-lookup"><span data-stu-id="65071-140">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="65071-141">Columnas</span><span class="sxs-lookup"><span data-stu-id="65071-141">Columns</span></span>

<dl> <dt>

<span data-ttu-id="65071-142"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Diálogo\_</span><span class="sxs-lookup"><span data-stu-id="65071-142"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialog\_</span></span>
</dt> <dd>

<span data-ttu-id="65071-143">Una clave externa a la primera columna de la [tabla del cuadro de diálogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="65071-143">An external key to the first column of the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="65071-144">La combinación de este campo con el campo de control \_ identifica un control único.</span><span class="sxs-lookup"><span data-stu-id="65071-144">Combining this field with the Control\_ field identifies a unique control.</span></span>

</dd> <dt>

<span data-ttu-id="65071-145"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Control\_</span><span class="sxs-lookup"><span data-stu-id="65071-145"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Control\_</span></span>
</dt> <dd>

<span data-ttu-id="65071-146">Una clave externa a la segunda columna de la [tabla de control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="65071-146">An external key to the second column of the [Control table](control-table.md).</span></span> <span data-ttu-id="65071-147">Al combinar este campo con el campo del cuadro de diálogo, se \_ identifica un control único.</span><span class="sxs-lookup"><span data-stu-id="65071-147">Combining this field with the Dialog\_ field identifies a unique control.</span></span>

</dd> <dt>

<span data-ttu-id="65071-148"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Ceso</span><span class="sxs-lookup"><span data-stu-id="65071-148"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="65071-149">Identificador que especifica el tipo de evento que debe tener lugar cuando el usuario interactúa con el control especificado por el cuadro de diálogo \_ y el control \_ .</span><span class="sxs-lookup"><span data-stu-id="65071-149">An identifier that specifies the type of event that should take place when the user interacts with the control specified by Dialog\_ and Control\_.</span></span> <span data-ttu-id="65071-150">Para obtener una lista de los valores posibles, consulte [información general de ControlEvent,](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="65071-150">For a list of possible values see [ControlEvent Overview](controlevent-overview.md).</span></span>

<span data-ttu-id="65071-151">Para establecer una propiedad con un control, coloque \[ el \_ nombre \] de la propiedad en este campo y el nuevo valor en el campo argument.</span><span class="sxs-lookup"><span data-stu-id="65071-151">To set a property with a control, put \[Property\_Name\] in this field and the new value in the argument field.</span></span> <span data-ttu-id="65071-152">Put {} en el campo argument para escribir el valor null.</span><span class="sxs-lookup"><span data-stu-id="65071-152">Put { } into the argument field to enter the null value.</span></span>

</dd> <dt>

<span data-ttu-id="65071-153"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span><span class="sxs-lookup"><span data-stu-id="65071-153"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span></span>
</dt> <dd>

<span data-ttu-id="65071-154">Un valor que se utiliza como modificador al desencadenar un evento determinado.</span><span class="sxs-lookup"><span data-stu-id="65071-154">A value used as a modifier when triggering a particular event.</span></span>

<span data-ttu-id="65071-155">Por ejemplo, el argumento de [NewDialog ControlEvent,](newdialog-controlevent.md) o [SpawnDialog ControlEvent,](spawndialog-controlevent.md) es el nombre del cuadro de diálogo y el argumento de la acción de [instalación](install-action.md) es un número que define el nivel de instalación.</span><span class="sxs-lookup"><span data-stu-id="65071-155">For example, the argument of the [NewDialog ControlEvent](newdialog-controlevent.md) or the [SpawnDialog ControlEvent](spawndialog-controlevent.md) is the name of the dialog box and the argument of the [Install action](install-action.md) is a number defining the install level.</span></span>

</dd> <dt>

<span data-ttu-id="65071-156"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Cumple</span><span class="sxs-lookup"><span data-stu-id="65071-156"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="65071-157">Instrucción condicional que determina si el instalador activa el evento en la columna de eventos.</span><span class="sxs-lookup"><span data-stu-id="65071-157">A conditional statement that determines whether the installer activates the event in the Event column.</span></span> <span data-ttu-id="65071-158">El instalador desencadena el evento si la instrucción condicional en el campo condition se evalúa como true.</span><span class="sxs-lookup"><span data-stu-id="65071-158">The installer triggers the event if the conditional statement in the Condition field evaluates to True.</span></span> <span data-ttu-id="65071-159">Por lo tanto, ponga un 1 en esta columna para asegurarse de que el instalador desencadena el evento.</span><span class="sxs-lookup"><span data-stu-id="65071-159">Therefore put a 1 in this column to ensure that the installer triggers the event.</span></span> <span data-ttu-id="65071-160">El instalador no desencadena el evento si el campo Condition contiene una instrucción que se evalúa como false.</span><span class="sxs-lookup"><span data-stu-id="65071-160">The installer does not trigger the event if the Condition field contains a statement that evaluates to False.</span></span> <span data-ttu-id="65071-161">El instalador no desencadena un evento con un espacio en blanco en el campo condición a menos que ningún otro evento del control se evalúe como true.</span><span class="sxs-lookup"><span data-stu-id="65071-161">The installer does not trigger an event with a blank in the Condition field unless no other events of the control evaluate to True.</span></span> <span data-ttu-id="65071-162">Si ninguno de los campos de condición para el control denominado en el \_ campo de control se evalúa como true, el instalador desencadena que un evento tiene un campo de condición en blanco y, si hay más de un campo de condición en blanco, desencadena el evento con el valor más grande en el campo de ordenación.</span><span class="sxs-lookup"><span data-stu-id="65071-162">If none of the Condition fields for the control named in the Control\_ field evaluate to True, the installer triggers the one event having a blank Condition field, and if more than one Condition field is blank it triggers the one event of these with the largest value in the Ordering field.</span></span> <span data-ttu-id="65071-163">Consulte [Sintaxis de la instrucción condicional](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="65071-163">See [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="65071-164"><span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Pide</span><span class="sxs-lookup"><span data-stu-id="65071-164"><span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Ordering</span></span>
</dt> <dd>

<span data-ttu-id="65071-165">Entero que se usa para ordenar varios eventos enlazados al mismo control.</span><span class="sxs-lookup"><span data-stu-id="65071-165">An integer used to order several events tied to the same control.</span></span> <span data-ttu-id="65071-166">Debe ser un número no negativo.</span><span class="sxs-lookup"><span data-stu-id="65071-166">This must be a non-negative number.</span></span> <span data-ttu-id="65071-167">Este campo puede dejarse en blanco.</span><span class="sxs-lookup"><span data-stu-id="65071-167">This field may be left blank.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65071-168">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65071-168">Remarks</span></span>

<span data-ttu-id="65071-169">En la [tabla EventMapping](eventmapping-table.md) se muestran los controles que se suscriben a algún evento de control y se muestra el atributo de control que se va a cambiar cuando el otro control o el instalador publique ese evento.</span><span class="sxs-lookup"><span data-stu-id="65071-169">The [EventMapping table](eventmapping-table.md) lists the controls that subscribe to some control event and lists the control attribute to be changed when that event is published by the another control or the installer.</span></span>

<span data-ttu-id="65071-170">En Windows XP o sistemas operativos anteriores, los usuarios pueden publicar un evento de control solo interactuando con un [control CheckBox](checkbox-control.md) o un [control Pushbutton](pushbutton-control.md).</span><span class="sxs-lookup"><span data-stu-id="65071-170">On Windows XP or earlier operating systems, users can publish a control event only by interacting with a [Checkbox Control](checkbox-control.md) or [Pushbutton Control](pushbutton-control.md).</span></span> <span data-ttu-id="65071-171">Con Windows Server 2003, los usuarios pueden publicar un evento de control interactuando con un [control CheckBox](checkbox-control.md), un [control SelectionTree](selectiontree-control.md)y un [control Pushbutton](pushbutton-control.md).</span><span class="sxs-lookup"><span data-stu-id="65071-171">With Windows Server 2003, users can publish a control event only by interacting with a [Checkbox Control](checkbox-control.md), [SelectionTree Control](selectiontree-control.md), and [Pushbutton Control](pushbutton-control.md).</span></span> <span data-ttu-id="65071-172">Mostrar otros controles en el campo de control \_ no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="65071-172">Listing other controls in the Control\_ field has no effect.</span></span>

## <a name="validation"></a><span data-ttu-id="65071-173">Validación</span><span class="sxs-lookup"><span data-stu-id="65071-173">Validation</span></span>

<dl>

[<span data-ttu-id="65071-174">ICE03</span><span class="sxs-lookup"><span data-stu-id="65071-174">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="65071-175">ICE06</span><span class="sxs-lookup"><span data-stu-id="65071-175">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="65071-176">ICE17</span><span class="sxs-lookup"><span data-stu-id="65071-176">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="65071-177">ICE20</span><span class="sxs-lookup"><span data-stu-id="65071-177">ICE20</span></span>](ice20.md)  
[<span data-ttu-id="65071-178">ICE32</span><span class="sxs-lookup"><span data-stu-id="65071-178">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="65071-179">ICE44</span><span class="sxs-lookup"><span data-stu-id="65071-179">ICE44</span></span>](ice44.md)  
[<span data-ttu-id="65071-180">ICE46</span><span class="sxs-lookup"><span data-stu-id="65071-180">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="65071-181">ICE79</span><span class="sxs-lookup"><span data-stu-id="65071-181">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="65071-182">ICE86</span><span class="sxs-lookup"><span data-stu-id="65071-182">ICE86</span></span>](ice86.md)  
</dl>

 

 



