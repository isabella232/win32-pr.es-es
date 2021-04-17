---
description: Permite al autor iniciar una reinstalación de algunas o todas las características, mientras el cuadro de diálogo actual se está ejecutando.
ms.assetid: bc667f20-3abe-4ef3-b51e-dc74da63f651
title: Reinstalar ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1d2adece3f89dbe57b77f2345d1714ece64b271
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667150"
---
# <a name="reinstall-controlevent"></a><span data-ttu-id="1ba2e-103">Reinstalar ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="1ba2e-103">Reinstall ControlEvent</span></span>

<span data-ttu-id="1ba2e-104">La reinstalación ControlEventallows el autor para iniciar una reinstalación de algunas o todas las características, mientras se ejecuta el cuadro de diálogo actual.</span><span class="sxs-lookup"><span data-stu-id="1ba2e-104">The Reinstall ControlEventallows the author to initiate a reinstall of some or all features, while the current dialog box is running.</span></span>

<span data-ttu-id="1ba2e-105">Este evento puede ser publicado por un [control Pushbutton](pushbutton-control.md) o un [control SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="1ba2e-105">This event can be published by a [PushButton control](pushbutton-control.md) or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="1ba2e-106">Este evento se debe crear en la [tabla ControlEvent,](controlevent-table.md)y requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="1ba2e-106">This event should be authored into the [ControlEvent table](controlevent-table.md), and requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="1ba2e-107">Este evento no funciona con una interfaz de usuario [*básica*](b-gly.md)o no [*reducida*](r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="1ba2e-107">This event does not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="1ba2e-108">Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="1ba2e-108">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="1ba2e-109">Publicado por</span><span class="sxs-lookup"><span data-stu-id="1ba2e-109">Published By</span></span>

<span data-ttu-id="1ba2e-110">Este ControlEvent, lo publica el instalador.</span><span class="sxs-lookup"><span data-stu-id="1ba2e-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="1ba2e-111">Argumento</span><span class="sxs-lookup"><span data-stu-id="1ba2e-111">Argument</span></span>

<span data-ttu-id="1ba2e-112">Cadena que es el nombre de la característica o "ALL".</span><span class="sxs-lookup"><span data-stu-id="1ba2e-112">A string that is either the name of the feature or "ALL".</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="1ba2e-113">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="1ba2e-113">Action on Subscribers</span></span>

<span data-ttu-id="1ba2e-114">Este ControlEvent, no realiza ninguna acción en los suscriptores.</span><span class="sxs-lookup"><span data-stu-id="1ba2e-114">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="1ba2e-115">Uso típico</span><span class="sxs-lookup"><span data-stu-id="1ba2e-115">Typical Use</span></span>

<span data-ttu-id="1ba2e-116">Este evento está asociado a un control [Pushbutton](pushbutton-control.md) en un cuadro de diálogo modal.</span><span class="sxs-lookup"><span data-stu-id="1ba2e-116">This event is tied to a [PushButton](pushbutton-control.md) control on a modal dialog box.</span></span> <span data-ttu-id="1ba2e-117">El mismo control [Pushbutton](pushbutton-control.md) también debe estar vinculado a un [ReinstallMode](reinstallmode-controlevent.md) ControlEvent,.</span><span class="sxs-lookup"><span data-stu-id="1ba2e-117">The same [PushButton](pushbutton-control.md) control should also be tied to a [ReinstallMode](reinstallmode-controlevent.md) ControlEvent.</span></span>

 

 



