---
description: El control SelectionTree usa este evento para publicar una cadena que describe el elemento resaltado. La cadena es una de las &\# 0034; SEL \* & \# 0034; cadenas de la tabla UIText. Este evento debe crearse en la tabla EventMapping.
ms.assetid: 7770b46f-21c7-459f-9778-a86de70d467f
title: SelectionAction ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eda06826f6ac649e2278441c944cdea0332689af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669922"
---
# <a name="selectionaction-controlevent"></a><span data-ttu-id="b5a21-105">SelectionAction ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b5a21-105">SelectionAction ControlEvent</span></span>

<span data-ttu-id="b5a21-106">El [control SelectionTree](selectiontree-control.md) usa este evento para publicar una cadena que describe el elemento resaltado.</span><span class="sxs-lookup"><span data-stu-id="b5a21-106">The [SelectionTree control](selectiontree-control.md) uses this event to publish a string describing the highlighted item.</span></span> <span data-ttu-id="b5a21-107">La cadena es una de las cadenas "SEL \* " de la [tabla UIText](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="b5a21-107">The string is one of the "Sel\*" strings from the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="b5a21-108">Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="b5a21-108">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="b5a21-109">Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b5a21-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="b5a21-110">Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida.</span><span class="sxs-lookup"><span data-stu-id="b5a21-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="b5a21-111">Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="b5a21-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="b5a21-112">Este evento solo puede afectar a los controles que se encuentran en el mismo cuadro de diálogo que el control SelectionTree.</span><span class="sxs-lookup"><span data-stu-id="b5a21-112">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

## <a name="published-by"></a><span data-ttu-id="b5a21-113">Publicado por</span><span class="sxs-lookup"><span data-stu-id="b5a21-113">Published By</span></span>

[<span data-ttu-id="b5a21-114">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="b5a21-114">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="b5a21-115">Argumento</span><span class="sxs-lookup"><span data-stu-id="b5a21-115">Argument</span></span>

<span data-ttu-id="b5a21-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b5a21-116">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="b5a21-117">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="b5a21-117">Action on Subscribers</span></span>

<span data-ttu-id="b5a21-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b5a21-118">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="b5a21-119">Uso típico</span><span class="sxs-lookup"><span data-stu-id="b5a21-119">Typical Use</span></span>

<span data-ttu-id="b5a21-120">Un control de [texto](text-control.md) en el mismo cuadro de diálogo modal que el SelectionTree debería suscribirse a este evento a través de la [tabla EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="b5a21-120">A [Text](text-control.md) control in the same modal dialog box as the SelectionTree should subscribe to this event via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="b5a21-121">El control de texto muestra la explicación del elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="b5a21-121">The Text Control displays the explanation of the selected item.</span></span>

 

 



