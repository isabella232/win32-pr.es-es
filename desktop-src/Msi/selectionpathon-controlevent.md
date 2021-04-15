---
description: El control SelectionTree usa el evento SelectionPathOn para publicar un valor booleano que indica si hay una ruta de acceso de selección asociada a la característica seleccionada actualmente. Este evento debe crearse en la tabla EventMapping.
ms.assetid: 441b9416-066a-429b-92d2-555584a20fa2
title: SelectionPathOn ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9882ea534a0d4c91a0107ce3949363350a17fbea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669921"
---
# <a name="selectionpathon-controlevent"></a><span data-ttu-id="ae010-104">SelectionPathOn ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="ae010-104">SelectionPathOn ControlEvent</span></span>

<span data-ttu-id="ae010-105">El [control SelectionTree](selectiontree-control.md) usa el evento SelectionPathOn para publicar un valor booleano que indica si hay una ruta de acceso de selección asociada a la característica seleccionada actualmente.</span><span class="sxs-lookup"><span data-stu-id="ae010-105">The [SelectionTree control](selectiontree-control.md) uses the SelectionPathOn event to publish a Boolean value indicating whether there is a selection path associated with the currently selected feature.</span></span> <span data-ttu-id="ae010-106">Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="ae010-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="ae010-107">Este evento solo puede afectar a los controles que se encuentran en el mismo cuadro de diálogo que el control SelectionTree.</span><span class="sxs-lookup"><span data-stu-id="ae010-107">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

<span data-ttu-id="ae010-108">Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="ae010-108">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="ae010-109">Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida.</span><span class="sxs-lookup"><span data-stu-id="ae010-109">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="ae010-110">Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="ae010-110">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="ae010-111">La SelectionPathOn ControlEvent, no se publica nunca durante una [instalación de mantenimiento](maintenance-installation.md).</span><span class="sxs-lookup"><span data-stu-id="ae010-111">The SelectionPathOn ControlEvent is never published during a [Maintenance Installation](maintenance-installation.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="ae010-112">Publicado por</span><span class="sxs-lookup"><span data-stu-id="ae010-112">Published By</span></span>

[<span data-ttu-id="ae010-113">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="ae010-113">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="ae010-114">Argumento</span><span class="sxs-lookup"><span data-stu-id="ae010-114">Argument</span></span>

<span data-ttu-id="ae010-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ae010-115">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="ae010-116">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="ae010-116">Action on Subscribers</span></span>

<span data-ttu-id="ae010-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ae010-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="ae010-118">Uso típico</span><span class="sxs-lookup"><span data-stu-id="ae010-118">Typical Use</span></span>

<span data-ttu-id="ae010-119">Un control de [texto](text-control.md) en el mismo cuadro de diálogo modal que el SelectionTree debe suscribirse al evento a través de la [tabla EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="ae010-119">A [Text](text-control.md) control on the same modal dialog as the SelectionTree should subscribe to the event via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="ae010-120">El control de texto muestra el título de la ruta de acceso de la selección.</span><span class="sxs-lookup"><span data-stu-id="ae010-120">The Text Control displays the caption of the selection path.</span></span> <span data-ttu-id="ae010-121">Este control de texto está visible u oculto dependiendo del evento.</span><span class="sxs-lookup"><span data-stu-id="ae010-121">This text control is visible or hidden depending on the event.</span></span>

 

 



