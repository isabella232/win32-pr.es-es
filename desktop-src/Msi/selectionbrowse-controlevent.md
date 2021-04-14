---
description: El control SelectionTree usa el evento SelectionBrowse para generar un cuadro de diálogo de exploración que permita modificar la ruta de acceso del elemento resaltado.
ms.assetid: 10a5af2e-3144-4b51-8295-294e56cdf801
title: SelectionBrowse ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 754f69f939f7c90dca705a2669a37af1fce0e79a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361644"
---
# <a name="selectionbrowse-controlevent"></a><span data-ttu-id="e0b47-103">SelectionBrowse ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="e0b47-103">SelectionBrowse ControlEvent</span></span>

<span data-ttu-id="e0b47-104">El [control SelectionTree](selectiontree-control.md) usa el evento SelectionBrowse para generar un cuadro de diálogo de **exploración** que permita modificar la ruta de acceso del elemento resaltado.</span><span class="sxs-lookup"><span data-stu-id="e0b47-104">The [SelectionTree control](selectiontree-control.md) uses the SelectionBrowse event to spawn a **Browse** dialog box making it possible to modify the path of the highlighted item.</span></span>

<span data-ttu-id="e0b47-105">Este evento debe publicarse con un [control Pushbutton](pushbutton-control.md) situado en el mismo cuadro de diálogo que el control que se suscribe a este evento.</span><span class="sxs-lookup"><span data-stu-id="e0b47-105">This event should be published by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the control subscribing to this event.</span></span> <span data-ttu-id="e0b47-106">El evento debe crearse en la [tabla ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="e0b47-106">The event should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="e0b47-107">Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="e0b47-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="e0b47-108">Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida.</span><span class="sxs-lookup"><span data-stu-id="e0b47-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="e0b47-109">Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="e0b47-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="e0b47-110">Los controles que publican un evento SelectionBrowse se deshabilitan si se ha seleccionado una característica que ya está instalada, no es configurable o no se ha seleccionado para la instalación local.</span><span class="sxs-lookup"><span data-stu-id="e0b47-110">Any controls that publish a SelectionBrowse event become disabled if a feature has been selected that is already installed, not configurable, or not selected for local installation.</span></span> <span data-ttu-id="e0b47-111">Para ser configurables, la característica debe tener una [propiedad pública](public-properties.md) especificada en el \_ campo directorio de la [tabla de características](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="e0b47-111">To be configurable, the feature must have a [public property](public-properties.md) entered in the Directory\_ field of the [Feature table](feature-table.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="e0b47-112">Publicado por</span><span class="sxs-lookup"><span data-stu-id="e0b47-112">Published By</span></span>

[<span data-ttu-id="e0b47-113">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="e0b47-113">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="e0b47-114">Argumento</span><span class="sxs-lookup"><span data-stu-id="e0b47-114">Argument</span></span>

<span data-ttu-id="e0b47-115">Nombre del cuadro de diálogo que se va a generar.</span><span class="sxs-lookup"><span data-stu-id="e0b47-115">The name of the dialog to be spawned.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="e0b47-116">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="e0b47-116">Action on Subscribers</span></span>

<span data-ttu-id="e0b47-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e0b47-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="e0b47-118">Uso típico</span><span class="sxs-lookup"><span data-stu-id="e0b47-118">Typical Use</span></span>

<span data-ttu-id="e0b47-119">Un control [Pushbutton](pushbutton-control.md) en el mismo cuadro de diálogo modal que el SelectionTree usa este evento para desencadenar el cuadro de diálogo **examinar** .</span><span class="sxs-lookup"><span data-stu-id="e0b47-119">A [PushButton](pushbutton-control.md) control on the same modal dialog box as the SelectionTree uses this event to trigger the **Browse** dialog box.</span></span>

 

 



