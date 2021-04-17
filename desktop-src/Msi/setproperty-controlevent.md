---
description: 'La sintaxis del evento SetProperty es diferente de la de otros ControlEvents en lugar del nombre del evento que coloca la propiedad entre corchetes: nombre de \[ la \_ propiedad \] .'
ms.assetid: a8e80d14-8d62-4398-9e53-9a0119a62d70
title: SetProperty ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59326ddd9f576b4871de7c232318ffcdcdb4fb36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678146"
---
# <a name="setproperty-controlevent"></a><span data-ttu-id="f0056-103">SetProperty ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="f0056-103">SetProperty ControlEvent</span></span>

<span data-ttu-id="f0056-104">La sintaxis del evento SetProperty es diferente de la de otros ControlEvents en lugar del nombre del evento que coloca la propiedad entre corchetes: nombre de \[ la \_ propiedad \] .</span><span class="sxs-lookup"><span data-stu-id="f0056-104">The syntax for the SetProperty event is different than for other ControlEvents In place of the name of the event one puts the property in square brackets: \[property\_name\].</span></span> <span data-ttu-id="f0056-105">El argumento es el nuevo valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="f0056-105">The argument is the new value of the property.</span></span> <span data-ttu-id="f0056-106">Para anular la propiedad, el argumento debe ser {} .</span><span class="sxs-lookup"><span data-stu-id="f0056-106">To unset the property, the argument must be {}.</span></span> <span data-ttu-id="f0056-107">Esto es necesario porque el argumento es una clave principal de la tabla y, por tanto, no puede ser null.</span><span class="sxs-lookup"><span data-stu-id="f0056-107">This is necessary, because the argument is a primary key in the table and so cannot be null.</span></span> <span data-ttu-id="f0056-108">Se dará formato al argumento mediante el método FormatText, por lo que el argumento puede contener cualquier expresión que pueda controlar el método FormatText.</span><span class="sxs-lookup"><span data-stu-id="f0056-108">The argument will be formatted using the FormatText method, therefore the argument can contain any expression that the FormatText method can handle.</span></span> <span data-ttu-id="f0056-109">Los valores de propiedad se evalúan en el momento de ControlEvent,.</span><span class="sxs-lookup"><span data-stu-id="f0056-109">The property values are evaluated at the moment of the ControlEvent.</span></span>

<span data-ttu-id="f0056-110">Este evento puede ser publicado por un [control Pushbutton](pushbutton-control.md), un [control CheckBox](checkbox-control.md)o un [control SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="f0056-110">This event can be published by a [PushButton Control](pushbutton-control.md), [CheckBox Control](checkbox-control.md), or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="f0056-111">Este evento se debe crear en la [tabla ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="f0056-111">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="f0056-112">Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="f0056-112">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="f0056-113">Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida.</span><span class="sxs-lookup"><span data-stu-id="f0056-113">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="f0056-114">Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="f0056-114">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="f0056-115">Publicado por</span><span class="sxs-lookup"><span data-stu-id="f0056-115">Published By</span></span>

<span data-ttu-id="f0056-116">Este ControlEvent, lo publica el instalador.</span><span class="sxs-lookup"><span data-stu-id="f0056-116">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="f0056-117">Argumento</span><span class="sxs-lookup"><span data-stu-id="f0056-117">Argument</span></span>

<span data-ttu-id="f0056-118">Nuevo valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="f0056-118">The new value of the property.</span></span> <span data-ttu-id="f0056-119">{} para null.</span><span class="sxs-lookup"><span data-stu-id="f0056-119">{} for null.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="f0056-120">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="f0056-120">Action on Subscribers</span></span>

<span data-ttu-id="f0056-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f0056-121">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="f0056-122">Uso típico</span><span class="sxs-lookup"><span data-stu-id="f0056-122">Typical Use</span></span>

<span data-ttu-id="f0056-123">Control [Pushbutton](pushbutton-control.md) en un cuadro de diálogo vinculado a este evento para que cambie una propiedad cuando se inserte el botón.</span><span class="sxs-lookup"><span data-stu-id="f0056-123">A [PushButton](pushbutton-control.md) control on a dialog box linked to this event so it changes a property when the button is pushed.</span></span>

 

 



