---
description: El instalador usa este evento para publicar el nombre de la acción actual. Un control de texto que se suscribe a este ControlEvent, puede mostrar el nombre en un cuadro de diálogo. Este evento debe crearse en la tabla EventMapping.
ms.assetid: 2b4928fe-2d5c-46c1-8a31-cbebbc78d304
title: ActionText ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caf03829818ea7ce7732ca5f51f1710a11e8d07f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001765"
---
# <a name="actiontext-controlevent"></a><span data-ttu-id="bc54c-105">ActionText ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="bc54c-105">ActionText ControlEvent</span></span>

<span data-ttu-id="bc54c-106">El instalador usa este evento para publicar el nombre de la acción actual.</span><span class="sxs-lookup"><span data-stu-id="bc54c-106">The installer uses this event to publish the name of the present action.</span></span> <span data-ttu-id="bc54c-107">Un [control de texto](text-control.md) que se suscribe a este ControlEvent, puede mostrar el nombre en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="bc54c-107">The name can be displayed on a dialog box by a [Text Control](text-control.md) that subscribes to this ControlEvent.</span></span> <span data-ttu-id="bc54c-108">Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="bc54c-108">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="bc54c-109">Este ControlEvent, se puede controlar mediante una interfaz de usuario que se ejecuta en la interfaz de usuario [*básica*](b-gly.md), la interfaz de usuario [*reducida*](r-gly.md)o los niveles de [*IU completos*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="bc54c-109">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="bc54c-110">Para obtener información sobre los niveles de interfaz de usuario, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="bc54c-110">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="bc54c-111">Publicado por</span><span class="sxs-lookup"><span data-stu-id="bc54c-111">Published By</span></span>

<span data-ttu-id="bc54c-112">Este ControlEvent, lo publica el instalador.</span><span class="sxs-lookup"><span data-stu-id="bc54c-112">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="bc54c-113">Argumento</span><span class="sxs-lookup"><span data-stu-id="bc54c-113">Argument</span></span>

<span data-ttu-id="bc54c-114">Este ControlEvent, no utiliza un argumento.</span><span class="sxs-lookup"><span data-stu-id="bc54c-114">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="bc54c-115">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="bc54c-115">Action on Subscribers</span></span>

<span data-ttu-id="bc54c-116">Los suscriptores se muestran cuando llegan nuevos datos de progreso desde el instalador.</span><span class="sxs-lookup"><span data-stu-id="bc54c-116">The subscribers are shown when a new progress data arrives from the installer.</span></span>

## <a name="typical-use"></a><span data-ttu-id="bc54c-117">Uso típico</span><span class="sxs-lookup"><span data-stu-id="bc54c-117">Typical Use</span></span>

<span data-ttu-id="bc54c-118">Un [control de texto](text-control.md) en un cuadro de diálogo no modal se suscribe a este evento a través de la [tabla EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="bc54c-118">A [Text Control](text-control.md) on a modeless dialog subscribes to this event through the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="bc54c-119">El [atributo control de texto](text-control-attribute.md) debe aparecer en el campo atributos de esta tabla para recibir el nombre de la acción actual.</span><span class="sxs-lookup"><span data-stu-id="bc54c-119">The [Text Control Attribute](text-control-attribute.md) should be listed in the Attributes field of this table to receive the name of the current action.</span></span>

 

 



