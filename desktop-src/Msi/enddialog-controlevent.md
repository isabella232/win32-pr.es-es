---
description: Este evento notifica al instalador que quite un cuadro de diálogo modal. En todos los casos, el instalador quita el cuadro de diálogo presente.
ms.assetid: 74a28696-6387-4d62-8955-4708ba5872bb
title: EndDialog ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08449bffe29093e32066e92e1b8fc739efa02d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277180"
---
# <a name="enddialog-controlevent"></a><span data-ttu-id="e60b1-104">EndDialog ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="e60b1-104">EndDialog ControlEvent</span></span>

<span data-ttu-id="e60b1-105">Este evento notifica al instalador que quite un cuadro de diálogo modal.</span><span class="sxs-lookup"><span data-stu-id="e60b1-105">This event notifies the installer to remove a modal dialog box.</span></span> <span data-ttu-id="e60b1-106">En todos los casos, el instalador quita el cuadro de diálogo presente.</span><span class="sxs-lookup"><span data-stu-id="e60b1-106">In all cases the installer removes the present dialog box.</span></span>

<span data-ttu-id="e60b1-107">Este evento puede ser publicado por un [control Pushbutton](pushbutton-control.md)o un [control SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="e60b1-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="e60b1-108">Este evento se debe crear en la [tabla ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="e60b1-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="e60b1-109">Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="e60b1-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="e60b1-110">Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida.</span><span class="sxs-lookup"><span data-stu-id="e60b1-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="e60b1-111">Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="e60b1-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="e60b1-112">En la tabla siguiente se muestra la acción del evento resultante de los distintos argumentos especificados en la [tabla ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="e60b1-112">The following table lists the action of the event resulting from different arguments entered into the [ControlEvent table](controlevent-table.md).</span></span>



| <span data-ttu-id="e60b1-113">Argumento</span><span class="sxs-lookup"><span data-stu-id="e60b1-113">Argument</span></span> | <span data-ttu-id="e60b1-114">Acción del instalador</span><span class="sxs-lookup"><span data-stu-id="e60b1-114">Action by the installer</span></span>                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e60b1-115">Salir</span><span class="sxs-lookup"><span data-stu-id="e60b1-115">Exit</span></span>     | <span data-ttu-id="e60b1-116">La secuencia del asistente está cerrada y el control vuelve al instalador con el valor UserExit.</span><span class="sxs-lookup"><span data-stu-id="e60b1-116">The wizard sequence is closed and the control returns to the installer with the UserExit value.</span></span> <span data-ttu-id="e60b1-117">Este argumento no se puede usar en un cuadro de diálogo que sea un elemento secundario de otro cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e60b1-117">This argument cannot be used in a dialog box that is a child of another dialog box.</span></span> |
| <span data-ttu-id="e60b1-118">Volver a intentar</span><span class="sxs-lookup"><span data-stu-id="e60b1-118">Retry</span></span>    | <span data-ttu-id="e60b1-119">La secuencia del asistente está cerrada y el control vuelve al instalador con el valor Suspend.</span><span class="sxs-lookup"><span data-stu-id="e60b1-119">The wizard sequence is closed and the control returns to the installer with the Suspend value.</span></span> <span data-ttu-id="e60b1-120">Este argumento no se puede usar en un cuadro de diálogo que sea un elemento secundario de otro cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e60b1-120">This argument cannot be used in a dialog box that is a child of another dialog box.</span></span>  |
| <span data-ttu-id="e60b1-121">Ignorar</span><span class="sxs-lookup"><span data-stu-id="e60b1-121">Ignore</span></span>   | <span data-ttu-id="e60b1-122">La secuencia del asistente está cerrada y el control vuelve al instalador con el valor terminado.</span><span class="sxs-lookup"><span data-stu-id="e60b1-122">The wizard sequence is closed and the control returns to the installer with the Finished value.</span></span> <span data-ttu-id="e60b1-123">Este argumento no se puede usar en un cuadro de diálogo que sea un elemento secundario de otro cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e60b1-123">This argument cannot be used in a dialog box that is a child of another dialog box.</span></span> |
| <span data-ttu-id="e60b1-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e60b1-124">Return</span></span>   | <span data-ttu-id="e60b1-125">El control vuelve al elemento primario del cuadro de diálogo actual, o si no hay ningún elemento primario, el control vuelve al instalador con el valor Success.</span><span class="sxs-lookup"><span data-stu-id="e60b1-125">The control returns to the parent of the present dialog box, or if there is no parent, the control returns to the installer with the Success value.</span></span>                                 |



 

## <a name="published-by"></a><span data-ttu-id="e60b1-126">Publicado por</span><span class="sxs-lookup"><span data-stu-id="e60b1-126">Published By</span></span>

<span data-ttu-id="e60b1-127">Este ControlEvent, lo publica el instalador.</span><span class="sxs-lookup"><span data-stu-id="e60b1-127">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="e60b1-128">Argumento</span><span class="sxs-lookup"><span data-stu-id="e60b1-128">Argument</span></span>

<span data-ttu-id="e60b1-129">En los cuadros de diálogo normales, la columna argument de la [tabla ControlEvent,](controlevent-table.md) puede ser "Return", "Exit", "Retry" u "ignore".</span><span class="sxs-lookup"><span data-stu-id="e60b1-129">On regular dialog boxes the Argument column of the [ControlEvent table](controlevent-table.md) can be "Return", "Exit", "Retry", or "Ignore".</span></span>

<span data-ttu-id="e60b1-130">En los cuadros de diálogo de error, la columna argument de la [tabla ControlEvent,](controlevent-table.md) puede ser ' ErrorOk ', ' ErrorCancel ', ' ErrorAbort ', ' ErrorRetry ', ' ErrorIgnore ', ' ErrorYes ' o ' ErrorNo '.</span><span class="sxs-lookup"><span data-stu-id="e60b1-130">On error dialog boxes the Argument column of the [ControlEvent table](controlevent-table.md) can be "ErrorOk", "ErrorCancel", "ErrorAbort", "ErrorRetry", "ErrorIgnore", "ErrorYes", or "ErrorNo".</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="e60b1-131">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="e60b1-131">Action on Subscribers</span></span>

<span data-ttu-id="e60b1-132">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e60b1-132">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="e60b1-133">Uso típico</span><span class="sxs-lookup"><span data-stu-id="e60b1-133">Typical Use</span></span>

<span data-ttu-id="e60b1-134">Un control [Pushbutton](pushbutton-control.md) en un cuadro de diálogo modal está asociado a este evento en la tabla [ControlEvent,](controlevent-table.md) para cerrar un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e60b1-134">A [PushButton](pushbutton-control.md) control on a modal dialog is tied to this event in the [ControlEvent](controlevent-table.md) table to close a dialog box.</span></span>

 

 



