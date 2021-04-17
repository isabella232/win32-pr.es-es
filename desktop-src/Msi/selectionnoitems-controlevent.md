---
description: El control SelectionTree usa el evento SelectionNoItems para eliminar el texto de Descripción del elemento obsoleto o para deshabilitar los botones que han dejado de ser útiles. Este evento debe crearse en la tabla EventMapping.
ms.assetid: a79abd77-a6e5-4a1f-8a63-51644151404a
title: SelectionNoItems ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6544dfcaad3d22b63d71703ea95d1aa4f09a1efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653081"
---
# <a name="selectionnoitems-controlevent"></a><span data-ttu-id="3dd12-104">SelectionNoItems ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="3dd12-104">SelectionNoItems ControlEvent</span></span>

<span data-ttu-id="3dd12-105">El [control SelectionTree](selectiontree-control.md) usa el evento SelectionNoItems para eliminar el texto de Descripción del elemento obsoleto o para deshabilitar los botones que han dejado de ser útiles.</span><span class="sxs-lookup"><span data-stu-id="3dd12-105">The [SelectionTree control](selectiontree-control.md) uses the SelectionNoItems event to delete obsolete item description text or to disable buttons that have become useless.</span></span> <span data-ttu-id="3dd12-106">Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="3dd12-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="3dd12-107">Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="3dd12-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="3dd12-108">Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida.</span><span class="sxs-lookup"><span data-stu-id="3dd12-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="3dd12-109">Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="3dd12-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="3dd12-110">Este evento solo puede afectar a los controles que se encuentran en el mismo cuadro de diálogo que el control SelectionTree.</span><span class="sxs-lookup"><span data-stu-id="3dd12-110">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

## <a name="published-by"></a><span data-ttu-id="3dd12-111">Publicado por</span><span class="sxs-lookup"><span data-stu-id="3dd12-111">Published By</span></span>

<span data-ttu-id="3dd12-112">[Control SelectionTree](selectiontree-control.md) si la selección no tiene ningún nodo.</span><span class="sxs-lookup"><span data-stu-id="3dd12-112">[SelectionTree control](selectiontree-control.md) if the selection has no nodes.</span></span>

## <a name="argument"></a><span data-ttu-id="3dd12-113">Argumento</span><span class="sxs-lookup"><span data-stu-id="3dd12-113">Argument</span></span>

<span data-ttu-id="3dd12-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3dd12-114">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="3dd12-115">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="3dd12-115">Action on Subscribers</span></span>

<span data-ttu-id="3dd12-116">Elimina el texto de Descripción del elemento obsoleto o deshabilita los botones obsoletos.</span><span class="sxs-lookup"><span data-stu-id="3dd12-116">Deletes obsolete item description text or disables obsolete buttons.</span></span>

## <a name="typical-use"></a><span data-ttu-id="3dd12-117">Uso típico</span><span class="sxs-lookup"><span data-stu-id="3dd12-117">Typical Use</span></span>

<span data-ttu-id="3dd12-118">Se puede usar para deshabilitar los botones siguiente, restablecer y DiskCost en el [cuadro de diálogo de selección](selection-dialog.md) cuando una selección no tiene ningún nodo y estos botones pasan a ser inservibles.</span><span class="sxs-lookup"><span data-stu-id="3dd12-118">May be used to disable the Next, Reset, and DiskCost buttons on the [Selection Dialog](selection-dialog.md) when a selection has no nodes and these buttons become useless.</span></span>

 

 



