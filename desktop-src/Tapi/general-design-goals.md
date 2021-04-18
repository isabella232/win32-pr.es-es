---
description: La lista siguiente contiene los objetivos de diseño de TAPI MSP.
ms.assetid: 286b96c1-047b-4cb9-a189-af2818cfec58
title: Objetivos de diseño generales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 052bbf607e71986678acca29d17d587bfa5bccf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686982"
---
# <a name="general-design-goals"></a><span data-ttu-id="4d1c4-103">Objetivos de diseño generales</span><span class="sxs-lookup"><span data-stu-id="4d1c4-103">General Design Goals</span></span>

<span data-ttu-id="4d1c4-104">La lista siguiente contiene los objetivos de diseño de TAPI MSP.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-104">The following list contains the TAPI MSP design goals.</span></span>

-   <span data-ttu-id="4d1c4-105">Las clases base se han mantenido simples, con los miembros y métodos introducidos solo cuando es absolutamente necesario.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-105">Base classes have been kept simple, with members and methods introduced only when absolutely necessary.</span></span>
-   <span data-ttu-id="4d1c4-106">Herencia simple.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-106">Simple inheritance.</span></span> <span data-ttu-id="4d1c4-107">Sin herencia múltiple entre las clases, aunque se utiliza la herencia múltiple para las interfaces.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-107">No multiple inheritance among classes, although multiple inheritance is used for the interfaces.</span></span>
-   <span data-ttu-id="4d1c4-108">El bloqueo solo se produce en una dirección para evitar el interbloqueo.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-108">Locking happens only in one direction to prevent deadlock.</span></span> <span data-ttu-id="4d1c4-109">Los métodos del objeto de llamada que requieren el bloqueo en la llamada podrían llamar a métodos en la secuencia que requieren el bloqueo en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-109">Methods on the call object that require the lock on the call might call methods on the stream that require the lock on the stream.</span></span> <span data-ttu-id="4d1c4-110">Sin embargo, los métodos de la secuencia que requieren el bloqueo en la secuencia nunca llamarán a un método en la llamada que requiere un bloqueo en la llamada.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-110">However, methods on the stream that require the lock on the stream will never call a method on the call that requires a lock on the call.</span></span>
-   <span data-ttu-id="4d1c4-111">RefCounts se usan para proteger el acceso.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-111">Refcounts are used to protect access.</span></span> <span data-ttu-id="4d1c4-112">Todas las devoluciones de llamada publicadas en el grupo de subprocesos contienen refCounts.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-112">All callbacks posted to the thread pool hold refcounts.</span></span> <span data-ttu-id="4d1c4-113">El refcount se cancela cuando se cancela la espera.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-113">The refcount is canceled when the wait is canceled.</span></span> <span data-ttu-id="4d1c4-114">El objeto Address tiene refCounts en los terminales.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-114">The Address object has refcounts on Terminals.</span></span> <span data-ttu-id="4d1c4-115">Los objetos Call tienen refCounts en la dirección y en las secuencias.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-115">Call objects have refcounts on the Address and on Streams.</span></span> <span data-ttu-id="4d1c4-116">Los objetos de secuencia tienen refCounts en llamadas y terminales.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-116">Stream objects have refcounts on Calls and Terminals.</span></span> <span data-ttu-id="4d1c4-117">Los terminales tienen refCounts en las secuencias.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-117">The Terminals have refcounts on Streams.</span></span> <span data-ttu-id="4d1c4-118">La refCounts circular se interrumpe cuando se llama al método shutdown en los objetos address y Call.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-118">The circular refcounts break when the shutdown method on the Address and Call objects is called.</span></span>

 

 



