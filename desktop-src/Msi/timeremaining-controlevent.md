---
description: El instalador usa el evento TimeRemaining para publicar el tiempo restante aproximado, en segundos, para la secuencia de progreso actual.
ms.assetid: ec5fc2b3-13a9-4681-89f0-fd39bab1de5f
title: TimeRemaining ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c8978dfb7ed3be855921ad66af8554ea50972a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083302"
---
# <a name="timeremaining-controlevent"></a><span data-ttu-id="8f92f-103">TimeRemaining ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8f92f-103">TimeRemaining ControlEvent</span></span>

<span data-ttu-id="8f92f-104">El instalador usa el evento TimeRemaining para publicar el tiempo restante aproximado, en segundos, para la secuencia de progreso actual.</span><span class="sxs-lookup"><span data-stu-id="8f92f-104">The installer uses the TimeRemaining event to publish the approximate time remaining, in seconds, for the current progress sequence.</span></span> <span data-ttu-id="8f92f-105">El tiempo restante se puede mostrar en un cuadro de diálogo mediante un [control de texto](text-control.md) que se suscribe a este ControlEvent,.</span><span class="sxs-lookup"><span data-stu-id="8f92f-105">The time remaining can be displayed on a dialog box by a [Text Control](text-control.md) that subscribes to this ControlEvent.</span></span> <span data-ttu-id="8f92f-106">Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="8f92f-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="8f92f-107">Este ControlEvent, se puede controlar mediante una interfaz de usuario que se ejecuta en la interfaz de usuario [*básica*](b-gly.md), la interfaz de usuario [*reducida*](r-gly.md)o los niveles de [*IU completos*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="8f92f-107">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="8f92f-108">Para obtener información sobre los niveles de interfaz de usuario, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="8f92f-108">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="8f92f-109">Publicado por</span><span class="sxs-lookup"><span data-stu-id="8f92f-109">Published By</span></span>

<span data-ttu-id="8f92f-110">Este ControlEvent, lo publica el instalador.</span><span class="sxs-lookup"><span data-stu-id="8f92f-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="8f92f-111">Argumento</span><span class="sxs-lookup"><span data-stu-id="8f92f-111">Argument</span></span>

<span data-ttu-id="8f92f-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8f92f-112">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="8f92f-113">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="8f92f-113">Action on Subscribers</span></span>

<span data-ttu-id="8f92f-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8f92f-114">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="8f92f-115">Uso típico</span><span class="sxs-lookup"><span data-stu-id="8f92f-115">Typical Use</span></span>

<span data-ttu-id="8f92f-116">Un [control de texto](text-control.md) en un cuadro de diálogo no modal se suscribe a este evento a través de la [tabla EventMapping](eventmapping-table.md) y usa el [atributo TimeRemaining](timeremaining-control-attribute.md) para mostrar el tiempo restante.</span><span class="sxs-lookup"><span data-stu-id="8f92f-116">A [Text Control](text-control.md) on a modeless dialog box subscribes to this event through the [EventMapping table](eventmapping-table.md) and uses the [TimeRemaining attribute](timeremaining-control-attribute.md) to display the time remaining.</span></span>

<span data-ttu-id="8f92f-117">El mismo control de texto que se suscribe a TimeRemaining ControlEvent, también puede suscribirse a [ScriptInProgress ControlEvent,](scriptinprogress-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="8f92f-117">The same text control that subscribes to the TimeRemaining ControlEvent can also subscribe to the [ScriptInProgress ControlEvent](scriptinprogress-controlevent.md).</span></span> <span data-ttu-id="8f92f-118">En este caso, como la cadena de mensaje de ScriptInProgress preliminar, se reemplaza por la cadena "tiempo restante: XX minutos".</span><span class="sxs-lookup"><span data-stu-id="8f92f-118">In this case, as the preliminary ScriptInProgress message string, it is replaced by the "Time Remaining: xx minutes" string.</span></span>

 

 



