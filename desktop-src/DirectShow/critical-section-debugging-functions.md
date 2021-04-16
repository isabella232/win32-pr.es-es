---
description: Funciones de depuración de sección crítica
ms.assetid: 2e58ff06-d9b2-45fe-bd40-d637aa434339
title: Funciones de depuración de sección crítica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098558a97e38168595dc89c3c81175c9d6635c5d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536897"
---
# <a name="critical-section-debugging-functions"></a><span data-ttu-id="9351a-103">Funciones de depuración de sección crítica</span><span class="sxs-lookup"><span data-stu-id="9351a-103">Critical Section Debugging Functions</span></span>

<span data-ttu-id="9351a-104">Estas funciones ayudan a depurar las secciones críticas en el código, lo que puede facilitar la búsqueda de la causa de un interbloqueo.</span><span class="sxs-lookup"><span data-stu-id="9351a-104">These functions help to debug critical sections in your code, which can make it easier to find the cause of a deadlock.</span></span> <span data-ttu-id="9351a-105">Estas funciones usan la clase auxiliar [**CCritSec**](ccritsec.md) .</span><span class="sxs-lookup"><span data-stu-id="9351a-105">These functions use the [**CCritSec**](ccritsec.md) helper class.</span></span>



| <span data-ttu-id="9351a-106">Función</span><span class="sxs-lookup"><span data-stu-id="9351a-106">Function</span></span>                             | <span data-ttu-id="9351a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="9351a-107">Description</span></span>                                                                  |
|--------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="9351a-108">**CritCheckIn**</span><span class="sxs-lookup"><span data-stu-id="9351a-108">**CritCheckIn**</span></span>](critcheckin.md)   | <span data-ttu-id="9351a-109">Devuelve **true** si el subproceso actual posee la sección crítica especificada.</span><span class="sxs-lookup"><span data-stu-id="9351a-109">Returns **TRUE** if the current thread owns the specified critical section.</span></span>  |
| [<span data-ttu-id="9351a-110">**CritCheckOut**</span><span class="sxs-lookup"><span data-stu-id="9351a-110">**CritCheckOut**</span></span>](critcheckout.md) | <span data-ttu-id="9351a-111">Devuelve **false** si el subproceso actual posee la sección crítica especificada.</span><span class="sxs-lookup"><span data-stu-id="9351a-111">Returns **FALSE** if the current thread owns the specified critical section.</span></span> |
| [<span data-ttu-id="9351a-112">**DbgLockTrace**</span><span class="sxs-lookup"><span data-stu-id="9351a-112">**DbgLockTrace**</span></span>](dbglocktrace.md) | <span data-ttu-id="9351a-113">Habilita o deshabilita el registro de depuración de una sección crítica determinada.</span><span class="sxs-lookup"><span data-stu-id="9351a-113">Enables or disables debug logging for a given critical section.</span></span>              |



 

## <a name="related-topics"></a><span data-ttu-id="9351a-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9351a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9351a-115">Herramientas de depuración</span><span class="sxs-lookup"><span data-stu-id="9351a-115">Debugging Utilities</span></span>](debugging-utilities.md)
</dt> </dl>

 

 



