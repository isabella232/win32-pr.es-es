---
description: Se restablece el cuadro de diálogo. En otras palabras, se llama a todos los controles del cuadro de diálogo para deshacer los cambios de propiedad que han realizado. Este evento restablece todos los valores de propiedad a los que tenían cuando se creó el cuadro de diálogo.
ms.assetid: 6449abb8-54cb-4400-9eb2-b7e7f1564747
title: Restablecer ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 889f1b0f984f14b7522707db4ffbd958bff9c32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667666"
---
# <a name="reset-controlevent"></a><span data-ttu-id="afbec-105">Restablecer ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="afbec-105">Reset ControlEvent</span></span>

<span data-ttu-id="afbec-106">Se restablece el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="afbec-106">The dialog box is reset.</span></span> <span data-ttu-id="afbec-107">En otras palabras, se llama a todos los controles del cuadro de diálogo para deshacer los cambios de propiedad que han realizado.</span><span class="sxs-lookup"><span data-stu-id="afbec-107">In other words, all the controls on the dialog box are called to undo the property changes they have performed.</span></span> <span data-ttu-id="afbec-108">Este evento restablece todos los valores de propiedad a los que tenían cuando se creó el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="afbec-108">This event resets all the property values to what they were when the dialog box was created.</span></span>

<span data-ttu-id="afbec-109">Este evento puede ser publicado por un [control Pushbutton](pushbutton-control.md)o un [control SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="afbec-109">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="afbec-110">Este evento se debe crear en la [tabla ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="afbec-110">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="afbec-111">Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="afbec-111">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="afbec-112">Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida.</span><span class="sxs-lookup"><span data-stu-id="afbec-112">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="afbec-113">Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="afbec-113">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="afbec-114">Hay un caso, que se debe producir en raras ocasiones en la práctica, que no se controla correctamente en este ControlEvent,.</span><span class="sxs-lookup"><span data-stu-id="afbec-114">There is a case, which should occur rarely in practice, that is not handled properly by this ControlEvent.</span></span> <span data-ttu-id="afbec-115">Si hay dos o más controles en el mismo cuadro de diálogo vinculados indirectamente a la misma propiedad y al menos uno de ellos empezó a tener alguna otra propiedad, a veces, este valor de propiedad se restablecerá a su segundo valor.</span><span class="sxs-lookup"><span data-stu-id="afbec-115">If there are two or more controls on the same dialog box linked indirectly to the same property and at least one of them started having some other property, then this property value will sometimes be reset to its second value.</span></span>

## <a name="published-by"></a><span data-ttu-id="afbec-116">Publicado por</span><span class="sxs-lookup"><span data-stu-id="afbec-116">Published By</span></span>

<span data-ttu-id="afbec-117">Este ControlEvent, lo publica el instalador.</span><span class="sxs-lookup"><span data-stu-id="afbec-117">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="afbec-118">Argumento</span><span class="sxs-lookup"><span data-stu-id="afbec-118">Argument</span></span>

<span data-ttu-id="afbec-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="afbec-119">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="afbec-120">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="afbec-120">Action on Subscribers</span></span>

<span data-ttu-id="afbec-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="afbec-121">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="afbec-122">Uso típico</span><span class="sxs-lookup"><span data-stu-id="afbec-122">Typical Use</span></span>

<span data-ttu-id="afbec-123">Se usa un control [Pushbutton](pushbutton-control.md) en un cuadro de diálogo modal para restablecer todos los valores del cuadro de diálogo y cancelar todos los cambios en la página.</span><span class="sxs-lookup"><span data-stu-id="afbec-123">A [PushButton](pushbutton-control.md) control on a modal dialog box is used to reset all the values on the dialog box and to cancel all the changes on the page.</span></span>

 

 



