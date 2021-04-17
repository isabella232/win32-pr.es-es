---
description: Este ControlEvent, se puede usar para activar o desactivar las funcionalidades de reversión del instalador.
ms.assetid: 5279151c-a7cd-4f66-8d1b-d688b3b1cf82
title: EnableRollback ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc651ef90b46c87431453f50c7ee5a28953e4d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652530"
---
# <a name="enablerollback-controlevent"></a><span data-ttu-id="791e9-103">EnableRollback ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="791e9-103">EnableRollback ControlEvent</span></span>

<span data-ttu-id="791e9-104">Este ControlEvent, se puede usar para activar o desactivar las funcionalidades de reversión del instalador.</span><span class="sxs-lookup"><span data-stu-id="791e9-104">This ControlEvent can be used to turn on or turn off the installer's rollback capabilities.</span></span>

<span data-ttu-id="791e9-105">Este evento puede ser publicado por un [control Pushbutton](pushbutton-control.md)o un [control SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="791e9-105">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="791e9-106">Este evento se debe crear en la [tabla ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="791e9-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="791e9-107">Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="791e9-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="791e9-108">Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida.</span><span class="sxs-lookup"><span data-stu-id="791e9-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="791e9-109">Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="791e9-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="791e9-110">Publicado por</span><span class="sxs-lookup"><span data-stu-id="791e9-110">Published By</span></span>

<span data-ttu-id="791e9-111">Este ControlEvent, lo publica el instalador.</span><span class="sxs-lookup"><span data-stu-id="791e9-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="791e9-112">Argumento</span><span class="sxs-lookup"><span data-stu-id="791e9-112">Argument</span></span>

<span data-ttu-id="791e9-113">False desactiva las funciones de reversión del instalador.</span><span class="sxs-lookup"><span data-stu-id="791e9-113">False turns off the installer's rollback capabilities.</span></span> <span data-ttu-id="791e9-114">True activa las capacidades de reversión del instalador.</span><span class="sxs-lookup"><span data-stu-id="791e9-114">True turns on the installer's rollback capabilities.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="791e9-115">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="791e9-115">Action on Subscribers</span></span>

<span data-ttu-id="791e9-116">Este ControlEvent, no realiza ninguna acción en los suscriptores.</span><span class="sxs-lookup"><span data-stu-id="791e9-116">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="791e9-117">Uso típico</span><span class="sxs-lookup"><span data-stu-id="791e9-117">Typical Use</span></span>

<span data-ttu-id="791e9-118">Se puede usar para desactivar las capacidades de reversión Si el instalador detecta que no hay suficiente espacio en disco disponible para completar la instalación.</span><span class="sxs-lookup"><span data-stu-id="791e9-118">Can be used to turn off rollback capabilities if the installer detects that there is insufficient disk space available to complete the installation.</span></span> <span data-ttu-id="791e9-119">En este caso, se debe usar ControlEvent, con las propiedades [**OutOfDiskSpace**](outofdiskspace.md), [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md)y [**PROMPTROLLBACKCOST**](promptrollbackcost.md) .</span><span class="sxs-lookup"><span data-stu-id="791e9-119">For this case, the ControlEvent should be used with the [**OutOfDiskSpace**](outofdiskspace.md), [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md), and the [**PROMPTROLLBACKCOST**](promptrollbackcost.md) properties.</span></span>

 

 



