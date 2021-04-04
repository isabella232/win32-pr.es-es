---
description: El evento SetTargetPath notifica al instalador que compruebe y establezca la ruta de acceso seleccionada. Si la ruta de acceso no es válida en la que se va a escribir, el instalador bloquea más ControlEvents asociadas al control.
ms.assetid: 5649da99-1541-47ab-9d2e-b33a705998ec
title: SetTargetPath ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36812d291ab4410b08c577e6d118c3ff9e5dc0b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277739"
---
# <a name="settargetpath-controlevent"></a><span data-ttu-id="53a00-104">SetTargetPath ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="53a00-104">SetTargetPath ControlEvent</span></span>

<span data-ttu-id="53a00-105">El evento SetTargetPath notifica al instalador que compruebe y establezca la ruta de acceso seleccionada.</span><span class="sxs-lookup"><span data-stu-id="53a00-105">The SetTargetPath event notifies the installer to check and set the selected path.</span></span> <span data-ttu-id="53a00-106">Si la ruta de acceso no es válida en la que se va a escribir, el instalador bloquea más ControlEvents asociadas al control.</span><span class="sxs-lookup"><span data-stu-id="53a00-106">If the path is not valid to be written to, then the installer blocks further ControlEvents associated with the control.</span></span>

<span data-ttu-id="53a00-107">Este evento puede ser publicado por un [control Pushbutton](pushbutton-control.md)o un [control SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="53a00-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="53a00-108">Este evento se debe crear en la [tabla ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="53a00-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="53a00-109">Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="53a00-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="53a00-110">Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida.</span><span class="sxs-lookup"><span data-stu-id="53a00-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="53a00-111">Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="53a00-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="53a00-112">Publicado por</span><span class="sxs-lookup"><span data-stu-id="53a00-112">Published By</span></span>

<span data-ttu-id="53a00-113">Este ControlEvent, lo publica el instalador.</span><span class="sxs-lookup"><span data-stu-id="53a00-113">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="53a00-114">Argumento</span><span class="sxs-lookup"><span data-stu-id="53a00-114">Argument</span></span>

<span data-ttu-id="53a00-115">Nombre de la propiedad que contiene la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="53a00-115">The name of the property containing the path.</span></span> <span data-ttu-id="53a00-116">Si la propiedad está indirecta, el nombre de la propiedad se incluye entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="53a00-116">If the property is indirected, then the property name is enclosed in square brackets.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="53a00-117">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="53a00-117">Action on Subscribers</span></span>

<span data-ttu-id="53a00-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="53a00-118">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="53a00-119">Uso típico</span><span class="sxs-lookup"><span data-stu-id="53a00-119">Typical Use</span></span>

<span data-ttu-id="53a00-120">Un control [Pushbutton](pushbutton-control.md) en un cuadro de diálogo de exploración está asociado a este evento en la tabla [ControlEvent,](controlevent-table.md) para comprobar la ruta de acceso seleccionada antes de volver al cuadro de diálogo de selección.</span><span class="sxs-lookup"><span data-stu-id="53a00-120">A [PushButton](pushbutton-control.md) control on a browse dialog is tied to this event in the [ControlEvent](controlevent-table.md) table to check the selected path before returning to the selection dialog.</span></span>

## <a name="remarks"></a><span data-ttu-id="53a00-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53a00-121">Remarks</span></span>

<span data-ttu-id="53a00-122">No intente configurar la ruta de acceso de destino si los componentes que usan esas rutas ya están instalados para el usuario actual o para otro usuario.</span><span class="sxs-lookup"><span data-stu-id="53a00-122">Do not attempt to configure the target path if the components using those paths are already installed for the current user or for a different user.</span></span> <span data-ttu-id="53a00-123">Compruebe la propiedad [**ProductState**](productstate.md) antes de publicar el SetTargetPath ControlEvent, para determinar si el producto que contiene el componente está instalado.</span><span class="sxs-lookup"><span data-stu-id="53a00-123">Check the [**ProductState**](productstate.md) property before publishing the SetTargetPath ControlEvent to determine if the product containing the component is installed.</span></span>

 

 



