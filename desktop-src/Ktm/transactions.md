---
description: Una transacción es un objeto que define una unidad lógica de trabajo.
ms.assetid: 29661a58-ada9-4b7c-8d85-ab65b824c7cd
title: Transacciones (Administrador de transacciones de kernel)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bff77ae0d89f5e334319ea0b7b73c27a4b34b57e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677691"
---
# <a name="transactions"></a><span data-ttu-id="53a35-103">Transacciones</span><span class="sxs-lookup"><span data-stu-id="53a35-103">Transactions</span></span>

<span data-ttu-id="53a35-104">Una transacción es un objeto que define una unidad lógica de trabajo.</span><span class="sxs-lookup"><span data-stu-id="53a35-104">A transaction is an object that defines a logical unit of work.</span></span> <span data-ttu-id="53a35-105">La transacción está activa siempre que haya un identificador que haga referencia a la transacción y se considere activo si aún no se ha confirmado o revertido la transacción.</span><span class="sxs-lookup"><span data-stu-id="53a35-105">The transaction is alive as long as there is a handle referencing the transaction and it is considered active if the transaction has not yet been committed or rolled back.</span></span> <span data-ttu-id="53a35-106">Si se crea una transacción y se cierran todos los identificadores antes de que se produzca una confirmación o una reversión, la transacción se revertirá.</span><span class="sxs-lookup"><span data-stu-id="53a35-106">If a transaction is created and all handles to it have been closed before a commit or rollback occurs, the transaction will be rolled back.</span></span>

<span data-ttu-id="53a35-107">Considere el caso de un cliente transaccional en modo de usuario que crea una transacción para el ámbito de sus operaciones y, a continuación, realiza actualizaciones en uno o varios administradores de recursos.</span><span class="sxs-lookup"><span data-stu-id="53a35-107">Consider the case of a user-mode transactional client that creates a transaction to scope its operations, then performs updates on one or more resource managers.</span></span> <span data-ttu-id="53a35-108">Ocurre lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="53a35-108">The following occurs:</span></span>

1.  <span data-ttu-id="53a35-109">El cliente llama a la función [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction) para crear la transacción y recibe un identificador a esa transacción como el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="53a35-109">The client calls the [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction) function to create the transaction and receives a handle to that transaction as the return value.</span></span>

    <span data-ttu-id="53a35-110">La transacción se puede abrir o heredar en cualquier número de procesos; por tanto, cada proceso está implicado en la transacción.</span><span class="sxs-lookup"><span data-stu-id="53a35-110">The transaction can be opened or inherited by any number of processes; each process is thus involved in the transaction.</span></span> <span data-ttu-id="53a35-111">Si se produce un error en cualquiera de estos procesos, se anulará la transacción.</span><span class="sxs-lookup"><span data-stu-id="53a35-111">The failure of any of these processes will cause the transaction to abort.</span></span>

    <span data-ttu-id="53a35-112">Es posible que esta transacción aún no sea persistente.</span><span class="sxs-lookup"><span data-stu-id="53a35-112">This transaction may not yet be persistent.</span></span> <span data-ttu-id="53a35-113">Solo las transacciones que han alcanzado el estado preparado deben recuperarse en los errores del sistema si la transacción utiliza el registro supuesto que se ha anulado.</span><span class="sxs-lookup"><span data-stu-id="53a35-113">Only transactions that have reached the prepared state must be recovered across system failures if the transaction uses presumed-abort logging.</span></span>

2.  <span data-ttu-id="53a35-114">El cliente debe pasar una transacción al administrador de recursos explícitamente.</span><span class="sxs-lookup"><span data-stu-id="53a35-114">The client must pass a transaction to the resource manager explicitly.</span></span>
3.  <span data-ttu-id="53a35-115">El cliente realiza todas las operaciones transaccionales con uno o más RMs, como los sistemas de archivos de transacciones.</span><span class="sxs-lookup"><span data-stu-id="53a35-115">The client performs all its transactional operations with one or more RMs, such as transacted file systems.</span></span>
4.  <span data-ttu-id="53a35-116">El cliente llama a la función [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) .</span><span class="sxs-lookup"><span data-stu-id="53a35-116">The client calls the [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) function.</span></span>
5.  <span data-ttu-id="53a35-117">El administrador de recursos recibe notificaciones de KTM para preparar y confirmar sus datos.</span><span class="sxs-lookup"><span data-stu-id="53a35-117">The resource manager receives notifications from KTM to prepare and commit its data.</span></span>

## <a name="transactions-and-threads"></a><span data-ttu-id="53a35-118">Transacciones y subprocesos</span><span class="sxs-lookup"><span data-stu-id="53a35-118">Transactions and Threads</span></span>

<span data-ttu-id="53a35-119">Las transacciones no son las mismas que los subprocesos.</span><span class="sxs-lookup"><span data-stu-id="53a35-119">Transactions are not the same as threads.</span></span> <span data-ttu-id="53a35-120">Varios subprocesos o procesos pueden formar parte de una única transacción.</span><span class="sxs-lookup"><span data-stu-id="53a35-120">Multiple threads or processes can be a part of a single transaction.</span></span> <span data-ttu-id="53a35-121">Por el contrario, un subproceso puede formar parte de varias transacciones diferentes en momentos diferentes.</span><span class="sxs-lookup"><span data-stu-id="53a35-121">Conversely, a thread can be a part of several different transactions at different times.</span></span>

## <a name="transaction-functions"></a><span data-ttu-id="53a35-122">Funciones de transacción</span><span class="sxs-lookup"><span data-stu-id="53a35-122">Transaction Functions</span></span>

<span data-ttu-id="53a35-123">Las siguientes funciones se usan con transacciones.</span><span class="sxs-lookup"><span data-stu-id="53a35-123">The following functions are used with transactions.</span></span>



| <span data-ttu-id="53a35-124">Función</span><span class="sxs-lookup"><span data-stu-id="53a35-124">Function</span></span>                                                            | <span data-ttu-id="53a35-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="53a35-125">Description</span></span>                                                                                   |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53a35-126">**CommitTransaction**</span><span class="sxs-lookup"><span data-stu-id="53a35-126">**CommitTransaction**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)                      | <span data-ttu-id="53a35-127">Solicita que se confirme la transacción especificada.</span><span class="sxs-lookup"><span data-stu-id="53a35-127">Requests that the specified transaction be committed.</span></span>                                         |
| [<span data-ttu-id="53a35-128">**CommitTransactionAsync**</span><span class="sxs-lookup"><span data-stu-id="53a35-128">**CommitTransactionAsync**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-committransactionasync)            | <span data-ttu-id="53a35-129">Solicita que se confirme la transacción especificada.</span><span class="sxs-lookup"><span data-stu-id="53a35-129">Requests that the specified transaction be committed.</span></span>                                         |
| [<span data-ttu-id="53a35-130">**CreateTransaction**</span><span class="sxs-lookup"><span data-stu-id="53a35-130">**CreateTransaction**</span></span>](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)                      | <span data-ttu-id="53a35-131">Crea un nuevo objeto de transacción.</span><span class="sxs-lookup"><span data-stu-id="53a35-131">Creates a new transaction object.</span></span>                                                             |
| [<span data-ttu-id="53a35-132">**GetTransactionInformation**</span><span class="sxs-lookup"><span data-stu-id="53a35-132">**GetTransactionInformation**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactioninformation) | <span data-ttu-id="53a35-133">Devuelve la información solicitada sobre la transacción especificada.</span><span class="sxs-lookup"><span data-stu-id="53a35-133">Returns the requested information about the specified transaction.</span></span>                            |
| [<span data-ttu-id="53a35-134">**OpenTransaction**</span><span class="sxs-lookup"><span data-stu-id="53a35-134">**OpenTransaction**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction)                          | <span data-ttu-id="53a35-135">Abre una transacción existente.</span><span class="sxs-lookup"><span data-stu-id="53a35-135">Opens an existing transaction.</span></span>                                                                |
| [<span data-ttu-id="53a35-136">**RollbackTransaction**</span><span class="sxs-lookup"><span data-stu-id="53a35-136">**RollbackTransaction**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)                  | <span data-ttu-id="53a35-137">Solicita que se revierta la transacción especificada.</span><span class="sxs-lookup"><span data-stu-id="53a35-137">Requests that the specified transaction be rolled back.</span></span>                                       |
| [<span data-ttu-id="53a35-138">**RollbackTransactionAsync**</span><span class="sxs-lookup"><span data-stu-id="53a35-138">**RollbackTransactionAsync**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransactionasync)        | <span data-ttu-id="53a35-139">Solicita que se revierta la transacción especificada.</span><span class="sxs-lookup"><span data-stu-id="53a35-139">Requests that the specified transaction be rolled back.</span></span> <span data-ttu-id="53a35-140">Esta función devuelve de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="53a35-140">This function returns asynchronously.</span></span> |
| [<span data-ttu-id="53a35-141">**SetTransactionInformation**</span><span class="sxs-lookup"><span data-stu-id="53a35-141">**SetTransactionInformation**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-settransactioninformation)      | <span data-ttu-id="53a35-142">Establece la información de transacción para la transacción especificada.</span><span class="sxs-lookup"><span data-stu-id="53a35-142">Sets the transaction information for the specified transaction.</span></span>                               |



 

 

 



