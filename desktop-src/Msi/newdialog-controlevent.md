---
description: Este evento notifica al instalador que se va a pasar un cuadro de diálogo modal a otro cuadro de diálogo. El instalador quita el cuadro de diálogo presente y crea el nuevo con el nombre indicado en el argumento.
ms.assetid: bd1aa465-55a0-4983-8c71-7e7075ee9dfb
title: NewDialog ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 439c459bc5bfe061cc7f888d9c0a3374afa9098b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155520"
---
# <a name="newdialog-controlevent"></a><span data-ttu-id="b808b-104">NewDialog ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b808b-104">NewDialog ControlEvent</span></span>

<span data-ttu-id="b808b-105">Este evento notifica al instalador que se va a pasar un cuadro de diálogo modal a otro cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b808b-105">This event notifies the installer to transition a modal dialog box to another dialog box.</span></span> <span data-ttu-id="b808b-106">El instalador quita el cuadro de diálogo presente y crea el nuevo con el nombre indicado en el argumento.</span><span class="sxs-lookup"><span data-stu-id="b808b-106">The installer removes the present dialog box and creates the new one with the name indicated in the argument.</span></span>

<span data-ttu-id="b808b-107">Este evento puede ser publicado por un [control Pushbutton](pushbutton-control.md)o un [control SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="b808b-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="b808b-108">Este evento se debe crear en la [tabla ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="b808b-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="b808b-109">Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b808b-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="b808b-110">Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida.</span><span class="sxs-lookup"><span data-stu-id="b808b-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="b808b-111">Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="b808b-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="b808b-112">Publicado por</span><span class="sxs-lookup"><span data-stu-id="b808b-112">Published By</span></span>

<span data-ttu-id="b808b-113">Este ControlEvent, lo publica el instalador.</span><span class="sxs-lookup"><span data-stu-id="b808b-113">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="b808b-114">Argumento</span><span class="sxs-lookup"><span data-stu-id="b808b-114">Argument</span></span>

<span data-ttu-id="b808b-115">Cadena que es el nombre del nuevo cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b808b-115">A string that is the name of the new dialog.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="b808b-116">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="b808b-116">Action on Subscribers</span></span>

<span data-ttu-id="b808b-117">Este ControlEvent, no realiza ninguna acción en los suscriptores.</span><span class="sxs-lookup"><span data-stu-id="b808b-117">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="b808b-118">Uso típico</span><span class="sxs-lookup"><span data-stu-id="b808b-118">Typical Use</span></span>

<span data-ttu-id="b808b-119">Un control [Pushbutton](pushbutton-control.md) en un cuadro de diálogo modal está asociado a este evento en la tabla [ControlEvent,](controlevent-table.md) para indicar una transición al cuadro de diálogo siguiente o anterior de la misma secuencia del asistente.</span><span class="sxs-lookup"><span data-stu-id="b808b-119">A [PushButton](pushbutton-control.md) control on a modal dialog box is tied to this event in the [ControlEvent](controlevent-table.md) table to signal a transition to the next or previous dialog box of the same wizard sequence.</span></span>

 

 



