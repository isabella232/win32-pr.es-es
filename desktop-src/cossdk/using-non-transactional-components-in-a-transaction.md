---
description: Usar componentes no transaccionales en una transacción
ms.assetid: b83b4bab-1851-48dc-b35a-6467a6dff741
title: Usar componentes no transaccionales en una transacción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75cd8ebc756971a56413e371cf23de2144e5816
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807892"
---
# <a name="using-non-transactional-components-in-a-transaction"></a><span data-ttu-id="e8644-103">Usar componentes no transaccionales en una transacción</span><span class="sxs-lookup"><span data-stu-id="e8644-103">Using Non-Transactional Components in a Transaction</span></span>

<span data-ttu-id="e8644-104">A menudo resulta útil colocar componentes no transaccionales en una transacción para aprovechar las ventajas de las [propiedades ACID](acid-properties.md) de las transacciones.</span><span class="sxs-lookup"><span data-stu-id="e8644-104">It is often useful to place non-transactional components into a transaction to take advantage of the [ACID properties](acid-properties.md) of transactions.</span></span> <span data-ttu-id="e8644-105">Por ejemplo, si tiene componentes heredados no transaccionales que utiliza para actualizar las contraseñas de una red, puede colocar dichos componentes en una transacción para asegurarse de que las actualizaciones de contraseña son coherentes en toda la red.</span><span class="sxs-lookup"><span data-stu-id="e8644-105">For example, if you have non-transactional legacy components that you use to update passwords on a network, you can place those components in a transaction to ensure that password updates are consistent across the network.</span></span>

<span data-ttu-id="e8644-106">El *objeto de contexto de transacción* es un objeto genérico que permite a los clientes no transaccionales combinar el trabajo de varios objetos com en una única transacción, sin necesidad de desarrollar un componente nuevo específicamente para ese propósito.</span><span class="sxs-lookup"><span data-stu-id="e8644-106">The *transaction context object* is a generic object that allows non-transactional clients to combine the work of multiple COM objects into a single transaction, without requiring you to develop a new component specifically for that purpose.</span></span> <span data-ttu-id="e8644-107">A diferencia de una transacción automática, el objeto de contexto de transacción requiere que su cliente confirme o anule explícitamente la transacción.</span><span class="sxs-lookup"><span data-stu-id="e8644-107">In contrast to an automatic transaction, the transaction context object requires its client to explicitly commit or abort the transaction.</span></span>

<span data-ttu-id="e8644-108">De forma predeterminada, el valor de atributo de transacción del objeto de contexto de transacción se establece en requerido.</span><span class="sxs-lookup"><span data-stu-id="e8644-108">By default, the transaction attribute value of the transaction context object is set to Required.</span></span> <span data-ttu-id="e8644-109">COM+ anula la transacción si el cliente libera el objeto de contexto de transacción sin emitir explícitamente una llamada commit o Abort.</span><span class="sxs-lookup"><span data-stu-id="e8644-109">COM+ aborts the transaction if the client releases the transaction context object without explicitly issuing a commit or abort call.</span></span>

<span data-ttu-id="e8644-110">En el siguiente ejemplo de Visual Basic se muestra cómo un cliente no transaccional puede crear el trabajo realizado por más de un objeto en una única transacción:</span><span class="sxs-lookup"><span data-stu-id="e8644-110">The following Visual Basic example shows how a non-transactional client can compose the work done by more than one object into a single transaction:</span></span>


```VB
Dim objTxCtx As TransactionContext
Dim objCat As MyDLL.Ccat  ' Ccat is a user-defined component.
Dim objDog As MyDLL.Cdog  ' Cdog is a user-defined component.

' Get TransactionContext object.
Set objTxCtx = _
  CreateObject ("TxCtx.TransactionContext")

' Create instances of Cat and Dog.
Set objCat = _ 
  objTxCtx.CreateInstance ("MyDLL.Ccat")
Set objDog = _ 
  objTxCtx.CreateInstance ("MyDLL.Cdog")

' Both objects do work.
objDog.Bark
objCat.Hiss

' Commit the transaction.
objTxCtx.Commit

```



## <a name="limitations-of-the-transaction-context-object"></a><span data-ttu-id="e8644-111">Limitaciones del objeto de contexto de transacción</span><span class="sxs-lookup"><span data-stu-id="e8644-111">Limitations of the Transaction Context Object</span></span>

<span data-ttu-id="e8644-112">A continuación se indican algunas limitaciones importantes del objeto de contexto de transacción:</span><span class="sxs-lookup"><span data-stu-id="e8644-112">Following are some important limitations of the transaction context object:</span></span>

-   <span data-ttu-id="e8644-113">Cuando se usa un objeto de contexto de transacción, la lógica de aplicación que combina el trabajo de varios objetos en una única transacción está ligada a una implementación de cliente no transaccional específica y se pierden algunas ventajas del uso de componentes COM.</span><span class="sxs-lookup"><span data-stu-id="e8644-113">When using a transaction context object, the application logic that combines the work of multiple objects into a single transaction is tied to a specific non-transactional client implementation and some advantages of using COM components are lost.</span></span> <span data-ttu-id="e8644-114">Entre las ventajas perdidas se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="e8644-114">These lost advantages include the following:</span></span>
    -   <span data-ttu-id="e8644-115">Capacidad de reutilizar la lógica de la aplicación como parte de una transacción incluso más grande</span><span class="sxs-lookup"><span data-stu-id="e8644-115">Ability to reuse the application logic as part of an even larger transaction</span></span>
    -   <span data-ttu-id="e8644-116">Imposición de seguridad declarativa</span><span class="sxs-lookup"><span data-stu-id="e8644-116">Imposition of declarative security</span></span>
    -   <span data-ttu-id="e8644-117">Flexibilidad para ejecutar la lógica de forma remota desde el cliente</span><span class="sxs-lookup"><span data-stu-id="e8644-117">Flexibility to run the logic remotely from the client</span></span>
-   <span data-ttu-id="e8644-118">El objeto de contexto de transacción se ejecuta en proceso con el cliente no transaccional, lo que significa que COM+ debe estar disponible en el equipo cliente no transaccional.</span><span class="sxs-lookup"><span data-stu-id="e8644-118">The transaction context object runs in-process with the non-transactional client, which means that COM+ must be available on the non-transactional client computer.</span></span> <span data-ttu-id="e8644-119">Esto podría no ser un problema, por ejemplo, cuando se utiliza el objeto de contexto de transacción de una página de Active Server páginas (ASP) que se ejecuta en el mismo servidor que COM+.</span><span class="sxs-lookup"><span data-stu-id="e8644-119">This might not be a problem, for example, when the transaction context object is used from an Active Server Pages (ASP) page that is running on the same server as COM+.</span></span>
-   <span data-ttu-id="e8644-120">No se obtiene un contexto para el cliente no transaccional cuando se crea un objeto de contexto de transacción.</span><span class="sxs-lookup"><span data-stu-id="e8644-120">You do not get a context for the non-transactional client when you create a transaction context object.</span></span> <span data-ttu-id="e8644-121">El trabajo transaccional solo se puede realizar indirectamente, a través de objetos COM creados mediante el objeto de contexto de transacción.</span><span class="sxs-lookup"><span data-stu-id="e8644-121">Transactional work can only be done indirectly, through COM objects created by using the transaction context object.</span></span> <span data-ttu-id="e8644-122">En concreto, el cliente no transaccional no puede utilizar dispensadores de recursos COM+ (como ODBC) y tener el trabajo incluido en la transacción.</span><span class="sxs-lookup"><span data-stu-id="e8644-122">In particular, the non-transactional client cannot use COM+ resource dispensers (such as ODBC) and have the work included in the transaction.</span></span> <span data-ttu-id="e8644-123">Por ejemplo, los desarrolladores pueden estar familiarizados con la sintaxis siguiente para realizar el trabajo transaccional en sistemas de bases de datos relacionales:</span><span class="sxs-lookup"><span data-stu-id="e8644-123">For example, developers may be familiar with the following syntax for doing transactional work on relational database systems:</span></span>

    ``` syntax
    BEGIN TRANSACTION
      DoWork
    COMMIT TRANSACTION
    ```

    <span data-ttu-id="e8644-124">El uso del objeto de contexto de transacción de una manera similar no produce el resultado deseado:</span><span class="sxs-lookup"><span data-stu-id="e8644-124">Using the transaction context object in a similar way does not yield the desired result:</span></span>

    ``` syntax
    Set objTxCtx = CreateObject ("TxCtx.TransactionContext")
      DoWork
      objTxCtx.Commit
    Set objTxCtx = Nothing
    ```

    <span data-ttu-id="e8644-125">La llamada a mi trabajo en este ejemplo no se da de alta en una transacción.</span><span class="sxs-lookup"><span data-stu-id="e8644-125">The call to DoWork in this example is not enlisted in a transaction.</span></span> <span data-ttu-id="e8644-126">En su lugar, debe crear un componente COM que llame a trabajo, crear una instancia de objeto de ese componente mediante el objeto de contexto de transacción y, a continuación, llamar a ese objeto desde el cliente no transaccional para que el trabajo forme parte de la transacción controlada por el cliente.</span><span class="sxs-lookup"><span data-stu-id="e8644-126">Instead, you must build a COM component that calls DoWork, create an object instance of that component using the transaction context object, and then call that object from the non-transactional client for the work to be part of the client-controlled transaction.</span></span>

 

 



