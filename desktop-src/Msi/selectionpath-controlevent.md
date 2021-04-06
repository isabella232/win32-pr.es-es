---
description: El control SelectionTree usa el evento SelectionPath para publicar la ruta de acceso del elemento resaltado.
ms.assetid: 755e5bf2-42c4-4213-9bb7-4f15ad22041f
title: SelectionPath ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8314b12d14e10ccf96c7db9db32e63172050c0bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002139"
---
# <a name="selectionpath-controlevent"></a><span data-ttu-id="5908e-103">SelectionPath ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="5908e-103">SelectionPath ControlEvent</span></span>

<span data-ttu-id="5908e-104">El [control SelectionTree](selectiontree-control.md) usa el evento SelectionPath para publicar la ruta de acceso del elemento resaltado.</span><span class="sxs-lookup"><span data-stu-id="5908e-104">The [SelectionTree control](selectiontree-control.md) uses the SelectionPath event to publish the path for the highlighted item.</span></span> <span data-ttu-id="5908e-105">Si el elemento está seleccionado para ejecutarse desde el origen, se trata de la ruta de acceso del origen.</span><span class="sxs-lookup"><span data-stu-id="5908e-105">If the item is selected to run from source, then this is the path of the source.</span></span> <span data-ttu-id="5908e-106">Si el elemento está seleccionado para estar ausente, la cadena es la cadena **AbsentPath** de la [tabla UIText](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="5908e-106">If the item is selected to be absent, then the string is the **AbsentPath** string from the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="5908e-107">Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="5908e-107">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="5908e-108">Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="5908e-108">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="5908e-109">Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida.</span><span class="sxs-lookup"><span data-stu-id="5908e-109">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="5908e-110">Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="5908e-110">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="5908e-111">Este evento solo puede afectar a los controles que se encuentran en el mismo cuadro de diálogo que el control SelectionTree.</span><span class="sxs-lookup"><span data-stu-id="5908e-111">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

## <a name="published-by"></a><span data-ttu-id="5908e-112">Publicado por</span><span class="sxs-lookup"><span data-stu-id="5908e-112">Published By</span></span>

[<span data-ttu-id="5908e-113">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="5908e-113">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="5908e-114">Argumento</span><span class="sxs-lookup"><span data-stu-id="5908e-114">Argument</span></span>

<span data-ttu-id="5908e-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5908e-115">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="5908e-116">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="5908e-116">Action on Subscribers</span></span>

<span data-ttu-id="5908e-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5908e-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="5908e-118">Uso típico</span><span class="sxs-lookup"><span data-stu-id="5908e-118">Typical Use</span></span>

<span data-ttu-id="5908e-119">Un control de [texto](text-control.md) en el mismo cuadro de diálogo modal que el SelectionTree debe suscribirse al evento a través de la [tabla EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="5908e-119">A [Text](text-control.md) control on the same modal dialog as the SelectionTree should subscribe to the event via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="5908e-120">El control de texto muestra la ruta de acceso del elemento resaltado.</span><span class="sxs-lookup"><span data-stu-id="5908e-120">The Text Control displays the path of the highlighted item.</span></span>

 

 



