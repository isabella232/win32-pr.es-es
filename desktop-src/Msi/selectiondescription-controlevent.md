---
description: El control SelectionTree usa el evento SelectionDescription para publicar una cadena que contiene la descripción del elemento resaltado. Esta cadena es el campo de descripción de la tabla de características. Este evento debe crearse en la tabla EventMapping.
ms.assetid: 29ae9aec-764f-4ff2-9c08-805538130cb1
title: SelectionDescription ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901db4efbed03341243d1b978dab0b8759fbc02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667619"
---
# <a name="selectiondescription-controlevent"></a><span data-ttu-id="8d931-105">SelectionDescription ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8d931-105">SelectionDescription ControlEvent</span></span>

<span data-ttu-id="8d931-106">El [control SelectionTree](selectiontree-control.md) usa el evento SelectionDescription para publicar una cadena que contiene la descripción del elemento resaltado.</span><span class="sxs-lookup"><span data-stu-id="8d931-106">The [SelectionTree control](selectiontree-control.md) uses the SelectionDescription event to publish a string that contains the description for the highlighted item.</span></span> <span data-ttu-id="8d931-107">Esta cadena es el campo de **Descripción** de la [tabla de características](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="8d931-107">This string is the **Description** field of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="8d931-108">Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="8d931-108">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="8d931-109">Este evento solo puede afectar a los controles que se encuentran en el mismo cuadro de diálogo que el [control SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="8d931-109">This event can only affect controls that are located on the same dialog box as the [SelectionTree control](selectiontree-control.md).</span></span>

<span data-ttu-id="8d931-110">Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="8d931-110">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="8d931-111">Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida.</span><span class="sxs-lookup"><span data-stu-id="8d931-111">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="8d931-112">Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="8d931-112">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="8d931-113">Publicado por</span><span class="sxs-lookup"><span data-stu-id="8d931-113">Published By</span></span>

[<span data-ttu-id="8d931-114">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="8d931-114">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="8d931-115">Argumento</span><span class="sxs-lookup"><span data-stu-id="8d931-115">Argument</span></span>

<span data-ttu-id="8d931-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8d931-116">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="8d931-117">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="8d931-117">Action on Subscribers</span></span>

<span data-ttu-id="8d931-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8d931-118">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="8d931-119">Uso típico</span><span class="sxs-lookup"><span data-stu-id="8d931-119">Typical Use</span></span>

<span data-ttu-id="8d931-120">Un control de [texto](text-control.md) en el mismo cuadro de diálogo modal que el SelectionTree se suscribe a este ControlEvent, a través de la [tabla EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="8d931-120">A [Text](text-control.md) control on the same modal dialog as the SelectionTree subscribes to this ControlEvent via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="8d931-121">El control de texto utiliza este evento para mostrar la descripción del elemento resaltado.</span><span class="sxs-lookup"><span data-stu-id="8d931-121">The Text Control uses this event to display the description of the highlighted item.</span></span>

 

 



