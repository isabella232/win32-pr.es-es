---
description: Este evento notifica al instalador, mientras mantiene el cuadro de diálogo presente en ejecución, que una característica o todas las características se van a ejecutar localmente.
ms.assetid: 074f347e-37d3-4365-a25d-caa0392a0dbc
title: AddLocal ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 112975d31e341c06a21609b173b9682283e71610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667053"
---
# <a name="addlocal-controlevent"></a><span data-ttu-id="58702-103">AddLocal ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="58702-103">AddLocal ControlEvent</span></span>

<span data-ttu-id="58702-104">Este evento notifica al instalador, mientras mantiene el cuadro de diálogo presente en ejecución, que una característica o todas las características se van a ejecutar localmente.</span><span class="sxs-lookup"><span data-stu-id="58702-104">This event notifies the installer, while keeping the present dialog running, that a feature or all features are to be run locally.</span></span> <span data-ttu-id="58702-105">Este evento puede ser publicado por un [control Pushbutton](pushbutton-control.md), un [control CheckBox](checkbox-control.md)o un [control SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="58702-105">This event can be published by a [PushButton Control](pushbutton-control.md), [Checkbox Control](checkbox-control.md), or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="58702-106">Este evento se debe crear en la [tabla ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="58702-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="58702-107">Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="58702-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="58702-108">Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida.</span><span class="sxs-lookup"><span data-stu-id="58702-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="58702-109">Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="58702-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="58702-110">Publicado por</span><span class="sxs-lookup"><span data-stu-id="58702-110">Published By</span></span>

<span data-ttu-id="58702-111">Este ControlEvent, lo publica el instalador.</span><span class="sxs-lookup"><span data-stu-id="58702-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="58702-112">Argumento</span><span class="sxs-lookup"><span data-stu-id="58702-112">Argument</span></span>

<span data-ttu-id="58702-113">Una cadena, ya sea el nombre de la característica o "ALL".</span><span class="sxs-lookup"><span data-stu-id="58702-113">A string, either the name of the feature or "ALL".</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="58702-114">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="58702-114">Action on Subscribers</span></span>

<span data-ttu-id="58702-115">Este ControlEvent, no realiza ninguna acción en los suscriptores.</span><span class="sxs-lookup"><span data-stu-id="58702-115">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="58702-116">Uso típico</span><span class="sxs-lookup"><span data-stu-id="58702-116">Typical Use</span></span>

<span data-ttu-id="58702-117">Un control [Pushbutton](pushbutton-control.md) en un cuadro de diálogo modal está asociado a este evento y se utiliza para notificar al instalador sin detener el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="58702-117">A [PushButton](pushbutton-control.md) control on a modal dialog box is tied to this event and used to notify the installer without stopping the dialog box.</span></span>

 

 



