---
description: Transacciones y activación JIT de COM+
ms.assetid: f7fad383-4081-4a49-aa03-59861fcefc97
title: Transacciones y activación JIT de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281691ebc9c8d5c654ea6ff0c3035d7e285f62c5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907441"
---
# <a name="transactions-and-com-jit-activation"></a><span data-ttu-id="cc39b-103">Transacciones y activación JIT de COM+</span><span class="sxs-lookup"><span data-stu-id="cc39b-103">Transactions and COM+ JIT Activation</span></span>

<span data-ttu-id="cc39b-104">La activación JIT de COM+ está estrechamente enlazada a transacciones automáticas.</span><span class="sxs-lookup"><span data-stu-id="cc39b-104">COM+ JIT Activation is closely bound to automatic transactions.</span></span> <span data-ttu-id="cc39b-105">Cuando se configura un componente para que requiera una transacción o se requiera una nueva transacción, la activación JIT también se habilita automáticamente.</span><span class="sxs-lookup"><span data-stu-id="cc39b-105">When you configure a component so that it requires a transaction or requires a new transaction, JIT Activation is automatically enabled as well.</span></span> <span data-ttu-id="cc39b-106">Las dos características funcionan de forma natural en conjunción.</span><span class="sxs-lookup"><span data-stu-id="cc39b-106">The two features naturally work in conjunction.</span></span> <span data-ttu-id="cc39b-107">Los componentes transaccionales y activados en JIT comparten las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="cc39b-107">Transactional, JIT-activated components share the following characteristics:</span></span>

-   <span data-ttu-id="cc39b-108">Estados.</span><span class="sxs-lookup"><span data-stu-id="cc39b-108">Statelessness.</span></span> <span data-ttu-id="cc39b-109">No contendría el estado que infringiría el aislamiento de transacción ni contenía el estado que se perdería en la desactivación de objetos.</span><span class="sxs-lookup"><span data-stu-id="cc39b-109">You would not hold state that would violate transaction isolation nor would you hold state that would be lost on object deactivation.</span></span>

-   <span data-ttu-id="cc39b-110">Uso rápido.</span><span class="sxs-lookup"><span data-stu-id="cc39b-110">Rapid use.</span></span> <span data-ttu-id="cc39b-111">El patrón de uso canónico para un objeto que realiza el trabajo en una transacción automática consiste en realizar una pequeña unidad de trabajo, votación y salida.</span><span class="sxs-lookup"><span data-stu-id="cc39b-111">The canonical use pattern for an object performing work in an automatic transaction is to do some small unit of work, vote, and exit.</span></span>

    > [!Note]  
    > <span data-ttu-id="cc39b-112">Las formas de votar en las transacciones COM+ y la realización de señales para la activación JIT también están estrechamente enlazadas.</span><span class="sxs-lookup"><span data-stu-id="cc39b-112">The ways that you vote in COM+ transactions and signal doneness for JIT Activation are also closely bound together.</span></span> <span data-ttu-id="cc39b-113">Para obtener más información, vea [establecer el bit Done](setting-the-done-bit.md).</span><span class="sxs-lookup"><span data-stu-id="cc39b-113">For more information, see [Setting the Done Bit](setting-the-done-bit.md).</span></span>

     

-   <span data-ttu-id="cc39b-114">Uso repetido.</span><span class="sxs-lookup"><span data-stu-id="cc39b-114">Repeated use.</span></span> <span data-ttu-id="cc39b-115">Cuando el trabajo transaccional se ha dividido correctamente, los clientes utilizan los mismos objetos una y otra vez para realizar pocas parcelas de trabajo atómico.</span><span class="sxs-lookup"><span data-stu-id="cc39b-115">When transactional work is properly broken up, clients use the same objects over and over to perform little parcels of atomic work.</span></span>

-   <span data-ttu-id="cc39b-116">Desactivado al confirmar o anular.</span><span class="sxs-lookup"><span data-stu-id="cc39b-116">Deactivated on commit or abort.</span></span> <span data-ttu-id="cc39b-117">En COM+, todos los objetos dentro del límite de la transacción se desactivan cuando la transacción se confirma o se anula.</span><span class="sxs-lookup"><span data-stu-id="cc39b-117">In COM+, all objects within the transaction boundary are deactivated when the transaction commits or aborts.</span></span>

<span data-ttu-id="cc39b-118">Junto con los componentes transaccionales de COM+, la activación JIT sirve como una mejora de gran rendimiento al mantener el canal abierto como los clientes contienen referencias de larga duración a objetos transaccionales.</span><span class="sxs-lookup"><span data-stu-id="cc39b-118">In conjunction with COM+ transactional components, JIT activation serves as a big performance enhancement by keeping the channel open as clients hold long-lived references to transactional objects.</span></span> <span data-ttu-id="cc39b-119">Como mejora adicional, puede agrupar los objetos transaccionales para reutilizar los recursos que contienen, acelerar el tiempo de reactivación de objetos y administrar de cerca cómo se usan los recursos de memoria para los objetos especificados.</span><span class="sxs-lookup"><span data-stu-id="cc39b-119">As further enhancements, you can elect to pool the transactional objects to reuse the resources they hold, speed object reactivation time, and closely manage how you use memory resources for given objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc39b-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cc39b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc39b-121">Conceptos de activación Just-in-Time de COM+</span><span class="sxs-lookup"><span data-stu-id="cc39b-121">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="cc39b-122">Habilitar la activación JIT para un componente</span><span class="sxs-lookup"><span data-stu-id="cc39b-122">Enabling JIT Activation for a Component</span></span>](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="cc39b-123">Agrupación de objetos y activación JIT de COM+</span><span class="sxs-lookup"><span data-stu-id="cc39b-123">Object Pooling and COM+ JIT Activation</span></span>](object-pooling-and-com--jit-activation.md)
</dt> </dl>

 

 



