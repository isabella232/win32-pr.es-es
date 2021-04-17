---
description: Este evento notifica al instalador que tiene que comprobar que la ruta de acceso seleccionada es válida. Si la ruta de acceso no es válida, este evento bloquea más ControlEvents asociadas al control.
ms.assetid: b7c1de6e-5738-4ecb-a033-9379d79dddb9
title: CheckTargetPath ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49301dbe1fcc6becc1bc757a0fe487061e1dcdbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666996"
---
# <a name="checktargetpath-controlevent"></a><span data-ttu-id="f1635-104">CheckTargetPath ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="f1635-104">CheckTargetPath ControlEvent</span></span>

<span data-ttu-id="f1635-105">Este evento notifica al instalador que tiene que comprobar que la ruta de acceso seleccionada es válida.</span><span class="sxs-lookup"><span data-stu-id="f1635-105">This event notifies the installer that it has to verify that the selected path is valid.</span></span> <span data-ttu-id="f1635-106">Si la ruta de acceso no es válida, este evento bloquea más ControlEvents asociadas al control.</span><span class="sxs-lookup"><span data-stu-id="f1635-106">If the path is not valid, then this event blocks further ControlEvents associated with the control.</span></span>

<span data-ttu-id="f1635-107">Este evento puede ser publicado por un [control Pushbutton](pushbutton-control.md)o un [control SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="f1635-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="f1635-108">Este evento se debe crear en la [tabla ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="f1635-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="f1635-109">Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="f1635-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="f1635-110">Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida.</span><span class="sxs-lookup"><span data-stu-id="f1635-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="f1635-111">Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="f1635-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="f1635-112">Publicado por</span><span class="sxs-lookup"><span data-stu-id="f1635-112">Published By</span></span>

<span data-ttu-id="f1635-113">Este ControlEvent, lo publica el instalador.</span><span class="sxs-lookup"><span data-stu-id="f1635-113">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="f1635-114">Argumento</span><span class="sxs-lookup"><span data-stu-id="f1635-114">Argument</span></span>

<span data-ttu-id="f1635-115">Nombre de la propiedad que contiene la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="f1635-115">The name of the property containing the path.</span></span> <span data-ttu-id="f1635-116">Si la propiedad está indirecta, el nombre de la propiedad se incluye entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="f1635-116">If the property is indirected, then the property name is enclosed in square brackets.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="f1635-117">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="f1635-117">Action on Subscribers</span></span>

<span data-ttu-id="f1635-118">Este ControlEvent, no realiza ninguna acción en los suscriptores.</span><span class="sxs-lookup"><span data-stu-id="f1635-118">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="f1635-119">Uso típico</span><span class="sxs-lookup"><span data-stu-id="f1635-119">Typical Use</span></span>

<span data-ttu-id="f1635-120">Un control [Pushbutton](pushbutton-control.md) en un cuadro de diálogo examinar está asociado a este evento en la tabla [ControlEvent,](controlevent-table.md) para comprobar la ruta de acceso seleccionada antes de volver al cuadro de diálogo de selección.</span><span class="sxs-lookup"><span data-stu-id="f1635-120">A [PushButton](pushbutton-control.md) control on a browse dialog box is tied to this event in the [ControlEvent](controlevent-table.md) table to check the selected path before returning to the selection dialog box.</span></span>

 

 



