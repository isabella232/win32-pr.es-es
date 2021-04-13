---
description: Notificar los cambios de estado de filtro de CBasePin
ms.assetid: 521ba95b-1f2d-4ad0-ab9b-4f1e3343a2d3
title: Notificar los cambios de estado de filtro de CBasePin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49dad6fabc162eb2384283ce2fc8914f76707036
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104359949"
---
# <a name="notifying-cbasepin-of-filter-state-changes"></a><span data-ttu-id="8e5c9-103">Notificar los cambios de estado de filtro de CBasePin</span><span class="sxs-lookup"><span data-stu-id="8e5c9-103">Notifying CBasePin of Filter State Changes</span></span>

<span data-ttu-id="8e5c9-104">La clase **CBasePin** se notifica cada vez que cambia el estado del filtro propietario.</span><span class="sxs-lookup"><span data-stu-id="8e5c9-104">The **CBasePin** class is notified whenever the state of the owning filter changes.</span></span> <span data-ttu-id="8e5c9-105">Para cada transición de estado, el filtro llama al método correspondiente en el código PIN, como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8e5c9-105">For each state transition, the filter calls a corresponding method on the pin, as shown in the following table.</span></span>



| <span data-ttu-id="8e5c9-106">Nuevo estado de filtro</span><span class="sxs-lookup"><span data-stu-id="8e5c9-106">New Filter State</span></span> | <span data-ttu-id="8e5c9-107">Método CBasePin</span><span class="sxs-lookup"><span data-stu-id="8e5c9-107">CBasePin Method</span></span>                                 |
|------------------|-------------------------------------------------|
| <span data-ttu-id="8e5c9-108">Detenido</span><span class="sxs-lookup"><span data-stu-id="8e5c9-108">Stopped</span></span>          | [<span data-ttu-id="8e5c9-109">**CBasePin:: inactivo**</span><span class="sxs-lookup"><span data-stu-id="8e5c9-109">**CBasePin::Inactive**</span></span>](cbasepin-inactive.md) |
| <span data-ttu-id="8e5c9-110">En pausa</span><span class="sxs-lookup"><span data-stu-id="8e5c9-110">Paused</span></span>           | [<span data-ttu-id="8e5c9-111">**CBasePin:: Active**</span><span class="sxs-lookup"><span data-stu-id="8e5c9-111">**CBasePin::Active**</span></span>](cbasepin-active.md)     |
| <span data-ttu-id="8e5c9-112">En ejecución</span><span class="sxs-lookup"><span data-stu-id="8e5c9-112">Running</span></span>          | [<span data-ttu-id="8e5c9-113">**CBasePin:: Run**</span><span class="sxs-lookup"><span data-stu-id="8e5c9-113">**CBasePin::Run**</span></span>](cbasepin-run.md)           |



 

<span data-ttu-id="8e5c9-114">La clase derivada debe invalidar estos métodos para responder al cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="8e5c9-114">The derived class should override these methods to respond to the state change.</span></span> <span data-ttu-id="8e5c9-115">Dependiendo del filtro, el pin puede iniciar un subproceso de trabajo que entregue ejemplos, confirme o desconfirme su asignador de memoria, etc.</span><span class="sxs-lookup"><span data-stu-id="8e5c9-115">Depending on the filter, the pin might start a worker thread that delivers samples, commit or decommit its memory allocator, and so forth.</span></span>

 

 



