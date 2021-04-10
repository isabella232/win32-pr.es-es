---
description: Acuñó por los pioneros en el procesamiento de transacciones, el ácido acrónimo es atómico, coherente, aislado y duradero.
ms.assetid: 857d145c-710d-4097-8ed6-df11e8d52228
title: Propiedades ACID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2e725cae75b4aa80d25f2959d474e8baa05f70
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153029"
---
# <a name="acid-properties"></a><span data-ttu-id="15fc6-103">Propiedades ACID</span><span class="sxs-lookup"><span data-stu-id="15fc6-103">ACID Properties</span></span>

<span data-ttu-id="15fc6-104">Acuñó por los pioneros en el procesamiento de transacciones, el ácido acrónimo es atómico, coherente, aislado y duradero.</span><span class="sxs-lookup"><span data-stu-id="15fc6-104">Coined by transaction processing pioneers, the acronym ACID stands for atomic, consistent, isolated, and durable.</span></span> <span data-ttu-id="15fc6-105">Para garantizar un comportamiento predecible, todas las transacciones deben poseer estas propiedades básicas, reforzando el rol de las transacciones críticas como proposiciones All-or-none.</span><span class="sxs-lookup"><span data-stu-id="15fc6-105">To ensure predictable behavior, all transactions must possess these basic properties, reinforcing the role of mission-critical transactions as all-or-none propositions.</span></span>

<span data-ttu-id="15fc6-106">La lista siguiente contiene una definición y una descripción de cada propiedad ACID:</span><span class="sxs-lookup"><span data-stu-id="15fc6-106">The following list contains a definition and a description of each ACID property:</span></span>

<dl> <dt>

<span data-ttu-id="15fc6-107"><span id="Atomic"></span><span id="atomic"></span><span id="ATOMIC"></span>Elemental</span><span class="sxs-lookup"><span data-stu-id="15fc6-107"><span id="Atomic"></span><span id="atomic"></span><span id="ATOMIC"></span>Atomic</span></span>
</dt> <dd>

<span data-ttu-id="15fc6-108">Una transacción debe ejecutarse exactamente una vez y debe ser atómica, o bien se realiza todo el trabajo o ninguno de ellos.</span><span class="sxs-lookup"><span data-stu-id="15fc6-108">A transaction must execute exactly once and must be atomic—either all of the work is done or none of it is.</span></span> <span data-ttu-id="15fc6-109">Las operaciones implicadas en una transacción suelen compartir una intención común y son interdependientes.</span><span class="sxs-lookup"><span data-stu-id="15fc6-109">Operations within a transaction usually share a common intent and are interdependent.</span></span> <span data-ttu-id="15fc6-110">Al realizar solo un subconjunto de estas operaciones, el sistema podría poner en peligro la intención general de la transacción.</span><span class="sxs-lookup"><span data-stu-id="15fc6-110">By performing only a subset of these operations, the system could compromise the overall intent of the transaction.</span></span> <span data-ttu-id="15fc6-111">La atomicidad elimina la posibilidad de procesar solo un subconjunto de operaciones.</span><span class="sxs-lookup"><span data-stu-id="15fc6-111">Atomicity eliminates the chance of processing only a subset of operations.</span></span>

</dd> <dt>

<span data-ttu-id="15fc6-112"><span id="Consistent"></span><span id="consistent"></span><span id="CONSISTENT"></span>Ajusta</span><span class="sxs-lookup"><span data-stu-id="15fc6-112"><span id="Consistent"></span><span id="consistent"></span><span id="CONSISTENT"></span>Consistent</span></span>
</dt> <dd>

<span data-ttu-id="15fc6-113">Una transacción debe conservar la coherencia de los datos, transformando un estado coherente de los datos en otro estado coherente de los datos.</span><span class="sxs-lookup"><span data-stu-id="15fc6-113">A transaction must preserve the consistency of data, transforming one consistent state of data into another consistent state of data.</span></span> <span data-ttu-id="15fc6-114">Gran parte de la responsabilidad de mantener la coherencia recae en el desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="15fc6-114">Much of the responsibility for maintaining consistency falls to the application developer.</span></span>

</dd> <dt>

<span data-ttu-id="15fc6-115"><span id="Isolated"></span><span id="isolated"></span><span id="ISOLATED"></span>Determinado</span><span class="sxs-lookup"><span data-stu-id="15fc6-115"><span id="Isolated"></span><span id="isolated"></span><span id="ISOLATED"></span>Isolated</span></span>
</dt> <dd>

<span data-ttu-id="15fc6-116">Una transacción debe ser una unidad de aislamiento, lo que significa que las transacciones simultáneas deben comportarse como si cada fuera la única transacción que se ejecuta en el sistema.</span><span class="sxs-lookup"><span data-stu-id="15fc6-116">A transaction must be a unit of isolation, which means that concurrent transactions should behave as if each were the only transaction running in the system.</span></span> <span data-ttu-id="15fc6-117">Dado que un alto grado de aislamiento puede limitar el número de transacciones simultáneas, algunas aplicaciones reducen el nivel de aislamiento en Exchange para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="15fc6-117">Because a high degree of isolation can limit the number of concurrent transactions, some applications reduce the isolation level in exchange for better throughput.</span></span> <span data-ttu-id="15fc6-118">Consulte [configuración de niveles de aislamiento de transacción](configuring-transaction-isolation-levels.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="15fc6-118">See [Configuring Transaction Isolation Levels](configuring-transaction-isolation-levels.md) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="15fc6-119"><span id="Durable"></span><span id="durable"></span><span id="DURABLE"></span>Durabilidad</span><span class="sxs-lookup"><span data-stu-id="15fc6-119"><span id="Durable"></span><span id="durable"></span><span id="DURABLE"></span>Durable</span></span>
</dt> <dd>

<span data-ttu-id="15fc6-120">Una transacción debe ser recuperable y, por tanto, debe tener durabilidad.</span><span class="sxs-lookup"><span data-stu-id="15fc6-120">A transaction must be recoverable and therefore must have durability.</span></span> <span data-ttu-id="15fc6-121">Si se confirma una transacción, el sistema garantiza que sus actualizaciones pueden persistir incluso si el equipo se bloquea inmediatamente después de la confirmación.</span><span class="sxs-lookup"><span data-stu-id="15fc6-121">If a transaction commits, the system guarantees that its updates can persist even if the computer crashes immediately after the commit.</span></span> <span data-ttu-id="15fc6-122">El registro especializado permite que el procedimiento de reinicio del sistema complete las operaciones sin terminar que requiere la transacción, lo que hace que la transacción sea duradera.</span><span class="sxs-lookup"><span data-stu-id="15fc6-122">Specialized logging allows the system's restart procedure to complete unfinished operations required by the transaction, making the transaction durable.</span></span>

</dd> </dl>

 

 



