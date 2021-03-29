---
description: Permite al autor de especificar el modo de validación o los modos durante una reinstalación y mientras se está ejecutando el cuadro de diálogo actual.
ms.assetid: d7cd41c6-c019-49d6-b593-a1d31c8f5a81
title: ReinstallMode ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ff5ff662b2880a3f4ab0fb79738b49cdeeccd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652665"
---
# <a name="reinstallmode-controlevent"></a><span data-ttu-id="8127a-103">ReinstallMode ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8127a-103">ReinstallMode ControlEvent</span></span>

<span data-ttu-id="8127a-104">El ReinstallMode ControlEventallows el autor para especificar el modo de validación o los modos durante una reinstalación y mientras se está ejecutando el cuadro de diálogo actual.</span><span class="sxs-lookup"><span data-stu-id="8127a-104">The ReinstallMode ControlEventallows the author to specify the validation mode or modes during a reinstallation, and while the current dialog box is running.</span></span>

<span data-ttu-id="8127a-105">Este evento puede ser publicado por un [control Pushbutton](pushbutton-control.md) o un [control SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="8127a-105">This event can be published by a [PushButton Control](pushbutton-control.md) or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="8127a-106">Este evento se debe crear en la [tabla ControlEvent,](controlevent-table.md)y requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="8127a-106">This event should be authored into the [ControlEvent table](controlevent-table.md), and requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="8127a-107">Este evento no funciona con una interfaz de usuario [*básica*](b-gly.md)o no [*reducida*](r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="8127a-107">This event does not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="8127a-108">Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="8127a-108">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="8127a-109">Publicado por</span><span class="sxs-lookup"><span data-stu-id="8127a-109">Published By</span></span>

<span data-ttu-id="8127a-110">Este ControlEvent, lo publica el instalador.</span><span class="sxs-lookup"><span data-stu-id="8127a-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="8127a-111">Argumento</span><span class="sxs-lookup"><span data-stu-id="8127a-111">Argument</span></span>

<span data-ttu-id="8127a-112">Una cadena.</span><span class="sxs-lookup"><span data-stu-id="8127a-112">A string.</span></span> <span data-ttu-id="8127a-113">Para obtener una lista de los valores posibles, vea [**REINSTALLMODE**](reinstallmode.md) (propiedad).</span><span class="sxs-lookup"><span data-stu-id="8127a-113">For a list of possible values, see [**REINSTALLMODE**](reinstallmode.md) property.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="8127a-114">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="8127a-114">Action on Subscribers</span></span>

<span data-ttu-id="8127a-115">Este ControlEvent, no realiza ninguna acción en los suscriptores.</span><span class="sxs-lookup"><span data-stu-id="8127a-115">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="8127a-116">Uso típico</span><span class="sxs-lookup"><span data-stu-id="8127a-116">Typical Use</span></span>

<span data-ttu-id="8127a-117">Este evento está asociado a un control [Pushbutton](pushbutton-control.md) en un cuadro de diálogo modal.</span><span class="sxs-lookup"><span data-stu-id="8127a-117">This event is tied to a [PushButton](pushbutton-control.md) control on a modal dialog box.</span></span> <span data-ttu-id="8127a-118">El mismo control [Pushbutton](pushbutton-control.md) también debe estar vinculado a un ControlEvent, de [reinstalación](reinstall-controlevent.md) .</span><span class="sxs-lookup"><span data-stu-id="8127a-118">The same [PushButton](pushbutton-control.md) control should also be tied to a [Reinstall](reinstall-controlevent.md) ControlEvent.</span></span>

 

 



