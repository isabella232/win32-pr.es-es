---
description: Grupo de métodos que se usa para manipular bloqueos.
ms.assetid: ba4cc37c-bd2f-446f-8b3d-bc2a2e2e4de4
title: Métodos CShareLockNH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b16a979c5d1f111c92a64376c48f4c0ed1a165ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659453"
---
# <a name="csharelocknh-methods"></a><span data-ttu-id="a1682-103">Métodos CShareLockNH</span><span class="sxs-lookup"><span data-stu-id="a1682-103">CShareLockNH Methods</span></span>

<span data-ttu-id="a1682-104">Grupo de métodos que se usa para manipular bloqueos.</span><span class="sxs-lookup"><span data-stu-id="a1682-104">A group of methods that is used to manipulate locks.</span></span>

## <a name="methods"></a><span data-ttu-id="a1682-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="a1682-105">Methods</span></span>

<span data-ttu-id="a1682-106">A continuación se muestran los métodos exportados por Rwnh.dll.</span><span class="sxs-lookup"><span data-stu-id="a1682-106">The following are methods exported by Rwnh.dll.</span></span>



| <span data-ttu-id="a1682-107">Método</span><span class="sxs-lookup"><span data-stu-id="a1682-107">Method</span></span>                                                                   | <span data-ttu-id="a1682-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1682-108">Description</span></span>                                                     |
|--------------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="a1682-109">**ExclusiveLock**</span><span class="sxs-lookup"><span data-stu-id="a1682-109">**ExclusiveLock**</span></span>](csharelocknh--exclusivelock.md)                     | <span data-ttu-id="a1682-110">Adquiere un bloqueo de lector/escritor.</span><span class="sxs-lookup"><span data-stu-id="a1682-110">Acquires a reader/writer lock.</span></span>                                  |
| [<span data-ttu-id="a1682-111">**ExclusiveToPartial**</span><span class="sxs-lookup"><span data-stu-id="a1682-111">**ExclusiveToPartial**</span></span>](csharelocknh--exclusivetopartial.md)           | <span data-ttu-id="a1682-112">Cambia el estado.</span><span class="sxs-lookup"><span data-stu-id="a1682-112">Changes the state.</span></span>                                              |
| [<span data-ttu-id="a1682-113">**ExclusiveUnlock**</span><span class="sxs-lookup"><span data-stu-id="a1682-113">**ExclusiveUnlock**</span></span>](csharelocknh--exclusiveunlock.md)                 | <span data-ttu-id="a1682-114">Libera un bloqueo.</span><span class="sxs-lookup"><span data-stu-id="a1682-114">Releases a lock.</span></span>                                                |
| [<span data-ttu-id="a1682-115">**FirstPartialToExclusive**</span><span class="sxs-lookup"><span data-stu-id="a1682-115">**FirstPartialToExclusive**</span></span>](csharelocknh--firstpartialtoexclusive.md) | <span data-ttu-id="a1682-116">Se usa para convertir un bloqueo parcial en un bloqueo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="a1682-116">Used in converting a partial lock to an exclusive lock.</span></span>         |
| [<span data-ttu-id="a1682-117">**PartialLock**</span><span class="sxs-lookup"><span data-stu-id="a1682-117">**PartialLock**</span></span>](csharelocknh--partiallock.md)                         | <span data-ttu-id="a1682-118">Impide que más de un subproceso complete la adquisición de un bloqueo.</span><span class="sxs-lookup"><span data-stu-id="a1682-118">Prevents more than one thread from completing acquiring a lock.</span></span> |
| [<span data-ttu-id="a1682-119">**PartialUnlock**</span><span class="sxs-lookup"><span data-stu-id="a1682-119">**PartialUnlock**</span></span>](csharelocknh--partialunlock.md)                     | <span data-ttu-id="a1682-120">Libera un bloqueo parcial.</span><span class="sxs-lookup"><span data-stu-id="a1682-120">Releases a partial lock.</span></span>                                        |
| [<span data-ttu-id="a1682-121">**ShareLock**</span><span class="sxs-lookup"><span data-stu-id="a1682-121">**ShareLock**</span></span>](csharelocknh--sharelock.md)                             | <span data-ttu-id="a1682-122">Obtiene un bloqueo para el modo compartido.</span><span class="sxs-lookup"><span data-stu-id="a1682-122">Obtains a lock for shared mode.</span></span>                                 |
| [<span data-ttu-id="a1682-123">**ShareUnlock**</span><span class="sxs-lookup"><span data-stu-id="a1682-123">**ShareUnlock**</span></span>](csharelocknh--shareunlock.md)                         | <span data-ttu-id="a1682-124">Libera un bloqueo del modo compartido.</span><span class="sxs-lookup"><span data-stu-id="a1682-124">Releases a lock from shared mode.</span></span>                               |
| [<span data-ttu-id="a1682-125">**SharedToPartial**</span><span class="sxs-lookup"><span data-stu-id="a1682-125">**SharedToPartial**</span></span>](csharelocknh--sharedtopartial.md)                 | <span data-ttu-id="a1682-126">Obtiene un bloqueo parcial.</span><span class="sxs-lookup"><span data-stu-id="a1682-126">Obtains a partial lock.</span></span>                                         |
| [<span data-ttu-id="a1682-127">**TryExclusiveLock**</span><span class="sxs-lookup"><span data-stu-id="a1682-127">**TryExclusiveLock**</span></span>](csharelocknh--tryexclusivelock.md)               | <span data-ttu-id="a1682-128">Obtiene un bloqueo exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="a1682-128">Obtains a lock exclusively.</span></span>                                     |



 

 

 



