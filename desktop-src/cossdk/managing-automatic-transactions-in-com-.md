---
description: En el modelo de programación COM+, puede diseñar los componentes para hacer lo que mejor&\# 8212; habilitar la lógica de negocios o establecer una conexión de base de datos&\# 8212; y basarse en el marco de procesamiento de transacciones de Microsoft Windows para automatizar las transacciones.
ms.assetid: 50086e6e-024b-4a09-b8be-8f55b6bfadb2
title: Administrar transacciones automáticas en COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371730173acd4943f460afbf2feab7ada83078fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539195"
---
# <a name="managing-automatic-transactions-in-com"></a><span data-ttu-id="e2c17-103">Administrar transacciones automáticas en COM+</span><span class="sxs-lookup"><span data-stu-id="e2c17-103">Managing Automatic Transactions in COM+</span></span>

<span data-ttu-id="e2c17-104">En el modelo de programación de COM+, puede diseñar los componentes para hacer lo que mejor se adapte a la lógica de negocios o al establecer una conexión de base de datos, y basarse en el marco de procesamiento de transacciones de Microsoft Windows para automatizar las transacciones.</span><span class="sxs-lookup"><span data-stu-id="e2c17-104">In the COM+ programming model, you can design your components to do what they do best—enabling business logic or establishing a database connection—and rely on the transaction processing framework of Microsoft Windows to automate transactions.</span></span>

## <a name="starting-a-transaction"></a><span data-ttu-id="e2c17-105">Iniciar una transacción</span><span class="sxs-lookup"><span data-stu-id="e2c17-105">Starting a Transaction</span></span>

<span data-ttu-id="e2c17-106">COM+ inicia automáticamente una transacción cuando encuentra cualquiera de las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="e2c17-106">COM+ automatically begins a transaction when it encounters either of the following conditions:</span></span>

-   <span data-ttu-id="e2c17-107">Cuando un cliente no transaccional llama a un componente que requiere una transacción o requiere una nueva transacción.</span><span class="sxs-lookup"><span data-stu-id="e2c17-107">When a non-transactional client calls a component that requires a transaction or requires a new transaction.</span></span>
-   <span data-ttu-id="e2c17-108">Cuando un cliente transaccional llama a un componente que requiere una nueva transacción.</span><span class="sxs-lookup"><span data-stu-id="e2c17-108">When a transactional client calls a component that requires a new transaction.</span></span>

<span data-ttu-id="e2c17-109">Si COM+ determina que un objeto debe tener una nueva transacción, comienza primero la transacción y, a continuación, coloca el objeto en ella.</span><span class="sxs-lookup"><span data-stu-id="e2c17-109">If COM+ determines that an object should have a new transaction, it begins the transaction first and then places the object in it.</span></span> <span data-ttu-id="e2c17-110">El proceso consta de los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="e2c17-110">The process includes the following steps:</span></span>

1.  <span data-ttu-id="e2c17-111">COM+ crea un objeto de contexto, establece los atributos de [activación](com--just-in-time-activation.md) y [sincronización](com--synchronization.md) JIT en Required y establece las [marcas coherente y](consistent-and-done-flags.md) final en true y false, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e2c17-111">COM+ creates a context object, sets both the [JIT activation](com--just-in-time-activation.md) and [Synchronization](com--synchronization.md) attributes to Required, and sets the [consistent and done flags](consistent-and-done-flags.md) to True and False, respectively.</span></span>
2.  <span data-ttu-id="e2c17-112">COM+ se comunica con el Coordinador de transacciones distribuidas (DTC) para iniciar una transacción.</span><span class="sxs-lookup"><span data-stu-id="e2c17-112">COM+ communicates with the Distributed Transaction Coordinator (DTC) to begin a transaction.</span></span> <span data-ttu-id="e2c17-113">El DTC coordina la transacción física.</span><span class="sxs-lookup"><span data-stu-id="e2c17-113">The DTC coordinates the physical transaction.</span></span>
3.  <span data-ttu-id="e2c17-114">El DTC genera un identificador de transacción y lo pasa de nuevo a COM+.</span><span class="sxs-lookup"><span data-stu-id="e2c17-114">The DTC generates a transaction identifier and passes it back to COM+.</span></span> <span data-ttu-id="e2c17-115">El identificador de transacción establece un límite de transacción.</span><span class="sxs-lookup"><span data-stu-id="e2c17-115">The transaction identifier establishes a transaction boundary.</span></span> <span data-ttu-id="e2c17-116">Todos los objetos que participan en la transacción comparten el mismo identificador.</span><span class="sxs-lookup"><span data-stu-id="e2c17-116">All objects participating in the transaction share the same identifier.</span></span>
4.  <span data-ttu-id="e2c17-117">Cuando el cliente crea el objeto, COM+ lo activa en el límite de la transacción.</span><span class="sxs-lookup"><span data-stu-id="e2c17-117">When the client creates the object, COM+ activates it within the transaction boundary.</span></span>

## <a name="ending-a-transaction"></a><span data-ttu-id="e2c17-118">Finalizar una transacción</span><span class="sxs-lookup"><span data-stu-id="e2c17-118">Ending a Transaction</span></span>

<span data-ttu-id="e2c17-119">COM+ finaliza una transacción automática mediante la confirmación o la anulación cuando se produce una de las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="e2c17-119">COM+ ends an automatic transaction by committing or aborting it when one of the following conditions occurs:</span></span>

-   <span data-ttu-id="e2c17-120">El objeto raíz de la transacción completa su trabajo y COM+ lo libera.</span><span class="sxs-lookup"><span data-stu-id="e2c17-120">The root object of the transaction completes its work and COM+ releases it.</span></span> <span data-ttu-id="e2c17-121">Una vez desactivado el objeto raíz, la transacción intenta confirmarse.</span><span class="sxs-lookup"><span data-stu-id="e2c17-121">After the root object deactivates, the transaction attempts to commit.</span></span>
-   <span data-ttu-id="e2c17-122">El cliente libera el objeto raíz.</span><span class="sxs-lookup"><span data-stu-id="e2c17-122">The client releases the root object.</span></span> <span data-ttu-id="e2c17-123">Sin una referencia, el objeto raíz se desactiva y la transacción intenta confirmarse.</span><span class="sxs-lookup"><span data-stu-id="e2c17-123">Without a reference, the root object deactivates and the transaction attempts to commit.</span></span>
-   <span data-ttu-id="e2c17-124">La transacción supera el umbral de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="e2c17-124">The transaction exceeds its time-out threshold.</span></span> <span data-ttu-id="e2c17-125">La transacción se anula automáticamente si no se confirma en el período de tiempo de espera de la transacción, desactivando todos los objetos asociados a la transacción.</span><span class="sxs-lookup"><span data-stu-id="e2c17-125">The transaction aborts automatically if not committed within the transaction time-out period, deactivating all objects associated with the transaction.</span></span> <span data-ttu-id="e2c17-126">El período de tiempo de espera predeterminado de la transacción es de 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="e2c17-126">The default transaction time-out period is 60 seconds.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2c17-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e2c17-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2c17-128">Marcas de coherencia y de realización</span><span class="sxs-lookup"><span data-stu-id="e2c17-128">Consistent and Done Flags</span></span>](consistent-and-done-flags.md)
</dt> <dt>

[<span data-ttu-id="e2c17-129">Acelerar las transacciones mediante la notificación del objeto raíz</span><span class="sxs-lookup"><span data-stu-id="e2c17-129">Speeding Transactions by Notifying the Root Object</span></span>](speeding-transactions-by-notifying-the-root-object.md)
</dt> <dt>

[<span data-ttu-id="e2c17-130">Finalizar una transacción automática llamando a SetComplete</span><span class="sxs-lookup"><span data-stu-id="e2c17-130">Terminating an Automatic Transaction by Calling SetComplete</span></span>](terminating-an-automatic-transaction-by-calling-setcomplete.md)
</dt> </dl>

 

 



