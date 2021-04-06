---
description: Los ControlEvents son análogos a los mensajes de Microsoft Windows en aplicaciones basadas en Win32.
ms.assetid: ac62bb94-0605-4145-996a-e91fb1a42a77
title: Información general de ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b92f8662a87bf9040b6a811fc170c25a5cf62ad7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913082"
---
# <a name="controlevent-overview"></a><span data-ttu-id="8c416-103">Información general de ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-103">ControlEvent Overview</span></span>

<span data-ttu-id="8c416-104">Los ControlEvents son análogos a los mensajes de Microsoft Windows en aplicaciones basadas en Win32.</span><span class="sxs-lookup"><span data-stu-id="8c416-104">ControlEvents are analogous to Microsoft Windows messages in Win32-based applications.</span></span> <span data-ttu-id="8c416-105">Sin embargo, en lugar de crear una función de devolución de llamada para recibir mensajes de Windows y enviar mensajes de Windows con la función [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) , el instalador de la interfaz de usuario (IU) y los controles publican [ControlEvents](control-events.md).</span><span class="sxs-lookup"><span data-stu-id="8c416-105">However, rather than creating a callback function to receive Windows messages and sending Windows messages with the [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) function, the user interface (UI) installer and controls publish [ControlEvents](control-events.md).</span></span> <span data-ttu-id="8c416-106">Se pueden especificar otros controles y el instalador para suscribirse a ControlEvents particulares que, a continuación, cambiarán los atributos del control de suscripción.</span><span class="sxs-lookup"><span data-stu-id="8c416-106">Other controls and the installer can be specified to subscribe to particular ControlEvents that will then change attributes of the subscribing control.</span></span> <span data-ttu-id="8c416-107">Para agregar controles de trabajo a los cuadros de diálogo, el autor de la interfaz de usuario especifica la publicación de ControlEvents en la [tabla ControlEvent,](controlevent-table.md) y suscribe los controles a ControlEvents en la [tabla EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="8c416-107">To add working controls to dialog boxes, the author of the UI specifies the publication of ControlEvents in the [ControlEvent table](controlevent-table.md) and subscribes controls to ControlEvents in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="8c416-108">El instalador publicará los siguientes eventos en los controles de suscripción que se enumeran en la [tabla EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="8c416-108">The installer will publish the following events to subscribing controls listed in the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="8c416-109">Un control [ProgressBar](progressbar-control.md) o un [control](billboard-control.md) de la cartelera normalmente se suscribe a SetProgress, el resto se suscribe a por [los controles de texto](text-control.md).</span><span class="sxs-lookup"><span data-stu-id="8c416-109">A [ProgressBar control](progressbar-control.md) or [Billboard control](billboard-control.md) typically subscribes to SetProgress, the rest are subscribed to by [Text controls](text-control.md).</span></span>

[<span data-ttu-id="8c416-110">ActionData ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-110">ActionData ControlEvent</span></span>](actiondata-controlevent.md)

[<span data-ttu-id="8c416-111">ActionText ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-111">ActionText ControlEvent</span></span>](actiontext-controlevent.md)

[<span data-ttu-id="8c416-112">SetProgress ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-112">SetProgress ControlEvent</span></span>](setprogress-controlevent.md)

[<span data-ttu-id="8c416-113">TimeRemaining ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-113">TimeRemaining ControlEvent</span></span>](timeremaining-controlevent.md)

[<span data-ttu-id="8c416-114">ScriptInProgress ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-114">ScriptInProgress ControlEvent</span></span>](scriptinprogress-controlevent.md)

<span data-ttu-id="8c416-115">El control publica los siguientes eventos cuando la selección de elementos se mueve en un control [SelectionTree](selectiontree-control.md) o [DirectoryList](directorylist-control.md).</span><span class="sxs-lookup"><span data-stu-id="8c416-115">The following events are published by the control when the item selection is moved in a [SelectionTree control](selectiontree-control.md) or [DirectoryList Control](directorylist-control.md).</span></span> <span data-ttu-id="8c416-116">Los controles de suscripción deben estar ubicados en el mismo cuadro de diálogo y se muestran en la tabla EventMapping.</span><span class="sxs-lookup"><span data-stu-id="8c416-116">Subscribing controls must be located on the same dialog box and listed in the EventMapping table.</span></span>

[<span data-ttu-id="8c416-117">IgnoreChange ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-117">IgnoreChange ControlEvent</span></span>](ignorechange-controlevent.md)

[<span data-ttu-id="8c416-118">SelectionDescription ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-118">SelectionDescription ControlEvent</span></span>](selectiondescription-controlevent.md)

[<span data-ttu-id="8c416-119">SelectionSize ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-119">SelectionSize ControlEvent</span></span>](selectionsize-controlevent.md)

[<span data-ttu-id="8c416-120">SelectionPath ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-120">SelectionPath ControlEvent</span></span>](selectionpath-controlevent.md)

[<span data-ttu-id="8c416-121">SelectionAction ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-121">SelectionAction ControlEvent</span></span>](selectionaction-controlevent.md)

[<span data-ttu-id="8c416-122">SelectionNoItems ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-122">SelectionNoItems ControlEvent</span></span>](selectionnoitems-controlevent.md)

<span data-ttu-id="8c416-123">Los siguientes ControlEvents se pueden publicar a la discreción de un usuario mediante la interacción con un [control de pulsador](pushbutton-control.md) o un [control de casilla](checkbox-control.md) en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8c416-123">The following ControlEvents can be published at the discretion of a user by interacting with a [PushButton control](pushbutton-control.md) or [CheckBox control](checkbox-control.md) on a dialog box.</span></span> <span data-ttu-id="8c416-124">El control CheckBox solo puede publicar los eventos AddLocal, AddSource, Remove, OnAction y SetProperty.</span><span class="sxs-lookup"><span data-stu-id="8c416-124">The Checkbox control can only publish the AddLocal, AddSource, Remove, DoAction, and SetProperty events.</span></span> <span data-ttu-id="8c416-125">Con Windows Installer versiones que se suministran con Windows Server 2003 y versiones posteriores, el [control SelectionTree](selectiontree-control.md) puede publicar la acción OnAction, ControlEvent, y SetProperty ControlEvents.</span><span class="sxs-lookup"><span data-stu-id="8c416-125">With Windows Installer versions that shipped with Windows Server 2003 and later, the [SelectionTree control](selectiontree-control.md) can publish the DoAction, ControlEvent and SetProperty ControlEvents.</span></span> <span data-ttu-id="8c416-126">El autor de la interfaz de usuario debe enumerar ControlEvent, en la [tabla ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="8c416-126">The author of the UI should list the ControlEvent in the [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="8c416-127">El controlador de la interfaz de usuario del instalador es el suscriptor a estos eventos.</span><span class="sxs-lookup"><span data-stu-id="8c416-127">The UI handler of the installer is the subscriber to these events.</span></span>

[<span data-ttu-id="8c416-128">AddLocal ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-128">AddLocal ControlEvent</span></span>](addlocal-controlevent.md)

[<span data-ttu-id="8c416-129">AddSource ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-129">AddSource ControlEvent</span></span>](addsource-controlevent.md)

[<span data-ttu-id="8c416-130">CheckExistingTargetPath ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-130">CheckExistingTargetPath ControlEvent</span></span>](checkexistingtargetpath-controlevent.md)

[<span data-ttu-id="8c416-131">CheckTargetPath ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-131">CheckTargetPath ControlEvent</span></span>](checktargetpath-controlevent.md)

[<span data-ttu-id="8c416-132">ControlEvent, de acción</span><span class="sxs-lookup"><span data-stu-id="8c416-132">DoAction ControlEvent</span></span>](doaction-controlevent.md)

[<span data-ttu-id="8c416-133">EnableRollback ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-133">EnableRollback ControlEvent</span></span>](enablerollback-controlevent.md)

[<span data-ttu-id="8c416-134">EndDialog ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-134">EndDialog ControlEvent</span></span>](enddialog-controlevent.md)

[<span data-ttu-id="8c416-135">NewDialog ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-135">NewDialog ControlEvent</span></span>](newdialog-controlevent.md)

[<span data-ttu-id="8c416-136">Reinstalar ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-136">Reinstall ControlEvent</span></span>](reinstall-controlevent.md)

[<span data-ttu-id="8c416-137">ReinstallMode ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-137">ReinstallMode ControlEvent</span></span>](reinstallmode-controlevent.md)

[<span data-ttu-id="8c416-138">Quitar ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-138">Remove ControlEvent</span></span>](remove-controlevent.md)

[<span data-ttu-id="8c416-139">Restablecer ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-139">Reset ControlEvent</span></span>](reset-controlevent.md)

[<span data-ttu-id="8c416-140">SetInstallLevel ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-140">SetInstallLevel ControlEvent</span></span>](setinstalllevel-controlevent.md)

[<span data-ttu-id="8c416-141">SetProperty ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-141">SetProperty ControlEvent</span></span>](setproperty-controlevent.md)

[<span data-ttu-id="8c416-142">SetTargetPath ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-142">SetTargetPath ControlEvent</span></span>](settargetpath-controlevent.md)

[<span data-ttu-id="8c416-143">SpawnDialog ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-143">SpawnDialog ControlEvent</span></span>](spawndialog-controlevent.md)

[<span data-ttu-id="8c416-144">SpawnWaitDialog ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-144">SpawnWaitDialog ControlEvent</span></span>](spawnwaitdialog-controlevent.md)

[<span data-ttu-id="8c416-145">ValidateProductID ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-145">ValidateProductID ControlEvent</span></span>](validateproductid-controlevent.md)

<span data-ttu-id="8c416-146">Un [control Pushbutton](pushbutton-control.md) puede publicar los eventos siguientes en un control [SelectionTree](selectiontree-control.md) de suscripción o en un [control DirectoryList](directorylist-control.md) ubicado en el mismo cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8c416-146">A [PushButton control](pushbutton-control.md) can publish the following events to a subscribing [SelectionTree control](selectiontree-control.md) or [DirectoryList control](directorylist-control.md) located in the same dialog box.</span></span> <span data-ttu-id="8c416-147">El control PushButton debe aparecer en la tabla ControlEvent, y los controles de suscripción deben aparecer en la tabla EventMapping.</span><span class="sxs-lookup"><span data-stu-id="8c416-147">The PushButton Control should be listed in the ControlEvent table and the subscribing controls should be listed in the EventMapping table.</span></span>

[<span data-ttu-id="8c416-148">SelectionBrowse ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-148">SelectionBrowse ControlEvent</span></span>](selectionbrowse-controlevent.md)

[<span data-ttu-id="8c416-149">DirectoryListUp ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-149">DirectoryListUp ControlEvent</span></span>](directorylistup-controlevent.md)

[<span data-ttu-id="8c416-150">DirectoryListNew ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-150">DirectoryListNew ControlEvent</span></span>](directorylistnew-controlevent.md)

[<span data-ttu-id="8c416-151">DirectoryListOpen ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8c416-151">DirectoryListOpen ControlEvent</span></span>](directorylistopen-controlevent.md)

<span data-ttu-id="8c416-152">Normalmente, los eventos de control requieren que la interfaz de usuario se ejecute en el nivel de [*interfaz de usuario completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="8c416-152">Control events generally require that the UI be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="8c416-153">La mayoría de ControlEvents no funcionará con una interfaz de usuario [*básica*](b-gly.md) o una [*reducida*](r-gly.md) porque estos niveles solo muestran cuadros de diálogo no modales.</span><span class="sxs-lookup"><span data-stu-id="8c416-153">Most ControlEvents will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md) because these levels only display modeless dialog boxes.</span></span> <span data-ttu-id="8c416-154">Los eventos ActionText, AddSource, SetProgress, TimeRemaining y ScriptInProgress son excepciones y funcionarán en la interfaz de usuario básica o reducida.</span><span class="sxs-lookup"><span data-stu-id="8c416-154">The ActionText, AddSource, SetProgress, TimeRemaining, and ScriptInProgress events are exceptions and will work in reduced or basic UI.</span></span> <span data-ttu-id="8c416-155">Para obtener más información sobre los niveles de interfaz de usuario, vea niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="8c416-155">For more information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="8c416-156">Puede ejecutar [acciones personalizadas](custom-actions.md) mediante la publicación de un ControlEvent, desde un [control Pushbutton](pushbutton-control.md) o un [control CheckBox](checkbox-control.md).</span><span class="sxs-lookup"><span data-stu-id="8c416-156">You can run [custom actions](custom-actions.md) by publishing a ControlEvent from a [PushButton control](pushbutton-control.md) or [Checkbox control](checkbox-control.md).</span></span> <span data-ttu-id="8c416-157">Agregue un registro a la [tabla ControlEvent,](controlevent-table.md) con los nombres del cuadro de diálogo y el control que publica ControlEvent,.</span><span class="sxs-lookup"><span data-stu-id="8c416-157">Add a record to the [ControlEvent table](controlevent-table.md) with the names of the dialog and the control publishing the ControlEvent.</span></span> <span data-ttu-id="8c416-158">Este control debe publicar un [ControlEvent, de acción](doaction-controlevent.md) que notifique al instalador que ejecute la acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="8c416-158">This control should publish a [DoAction ControlEvent](doaction-controlevent.md) notifying the installer to run the custom action.</span></span> <span data-ttu-id="8c416-159">En Windows XP o sistemas anteriores, no se puede ejecutar una acción personalizada mediante la publicación de un ControlEvent, desde un [control SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="8c416-159">On Windows XP or earlier systems, you cannot run a custom action by publishing a ControlEvent from a [SelectionTree control](selectiontree-control.md).</span></span>

<span data-ttu-id="8c416-160">Para obtener más información sobre ControlEvents concretos, consulte la lista de [ControlEvents](control-events.md) estándar en [referencia](user-interface-reference.md)de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="8c416-160">For a more information about particular ControlEvents, see the list of standard [ControlEvents](control-events.md) in [User Interface Reference](user-interface-reference.md).</span></span>

 

 
