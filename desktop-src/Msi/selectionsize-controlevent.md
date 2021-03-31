---
description: El control SelectionTree usa el evento SelectionSize para publicar el tamaño del elemento resaltado.
ms.assetid: 1ef161b6-f127-45ad-a312-d2adcb5124ef
title: SelectionSize ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c11829661f0120fa5906a04f081e6c979b37180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277159"
---
# <a name="selectionsize-controlevent"></a><span data-ttu-id="7fe28-103">SelectionSize ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="7fe28-103">SelectionSize ControlEvent</span></span>

<span data-ttu-id="7fe28-104">El [control SelectionTree](selectiontree-control.md) usa el evento SelectionSize para publicar el tamaño del elemento resaltado.</span><span class="sxs-lookup"><span data-stu-id="7fe28-104">The [SelectionTree control](selectiontree-control.md) uses the SelectionSize event to publish the size of the highlighted item.</span></span> <span data-ttu-id="7fe28-105">Si es un elemento primario, también se publica el número de elementos secundarios seleccionados.</span><span class="sxs-lookup"><span data-stu-id="7fe28-105">If it is a parent item, then the number of children selected is also published.</span></span> <span data-ttu-id="7fe28-106">La cadena es una de las cadenas **SelChildCostPos**, **SelChildCostNeg**, **SelParentCostPosPos**, **SelParentCostPosNeg**, **SelParentCostNegPos** o **SelParentCostNegNeg** de la [tabla UIText](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="7fe28-106">The string is one of the **SelChildCostPos**, **SelChildCostNeg**, **SelParentCostPosPos**, **SelParentCostPosNeg**, **SelParentCostNegPos** or **SelParentCostNegNeg** strings from the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="7fe28-107">Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="7fe28-107">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="7fe28-108">Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="7fe28-108">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="7fe28-109">Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida.</span><span class="sxs-lookup"><span data-stu-id="7fe28-109">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="7fe28-110">Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="7fe28-110">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="7fe28-111">Este evento solo puede afectar a los controles que se encuentran en el mismo cuadro de diálogo que el control SelectionTree.</span><span class="sxs-lookup"><span data-stu-id="7fe28-111">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

## <a name="published-by"></a><span data-ttu-id="7fe28-112">Publicado por</span><span class="sxs-lookup"><span data-stu-id="7fe28-112">Published By</span></span>

[<span data-ttu-id="7fe28-113">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="7fe28-113">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="7fe28-114">Argumento</span><span class="sxs-lookup"><span data-stu-id="7fe28-114">Argument</span></span>

<span data-ttu-id="7fe28-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7fe28-115">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="7fe28-116">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="7fe28-116">Action on Subscribers</span></span>

<span data-ttu-id="7fe28-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7fe28-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="7fe28-118">Uso típico</span><span class="sxs-lookup"><span data-stu-id="7fe28-118">Typical Use</span></span>

<span data-ttu-id="7fe28-119">Control de [texto](text-control.md) en el mismo cuadro de diálogo modal que el control SelectionTree a través de la [tabla EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="7fe28-119">A [Text](text-control.md) control on the same modal dialog as the SelectionTree Control via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="7fe28-120">El control de texto utiliza este evento para mostrar el tamaño del elemento resaltado.</span><span class="sxs-lookup"><span data-stu-id="7fe28-120">The Text Control uses this event to display the size of the highlighted item.</span></span>

 

 



