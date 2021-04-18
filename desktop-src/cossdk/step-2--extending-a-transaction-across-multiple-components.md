---
description: 'Paso 2: extensión de una transacción en varios componentes'
ms.assetid: 20a30e87-e209-45ae-bf1b-722568758c47
title: 'Paso 2: extensión de una transacción en varios componentes'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c6fc80016904a3ea51b7aea7fa0ec93edc47a6
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "104361786"
---
# <a name="step-2-extending-a-transaction-across-components"></a><span data-ttu-id="cb466-103">Paso 2: extensión de una transacción entre componentes</span><span class="sxs-lookup"><span data-stu-id="cb466-103">Step 2: Extending a Transaction Across Components</span></span>

## <a name="objectives"></a><span data-ttu-id="cb466-104">Objetivos</span><span class="sxs-lookup"><span data-stu-id="cb466-104">Objectives</span></span>

<span data-ttu-id="cb466-105">En este paso, obtendrá información sobre lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cb466-105">In this step, you will learn about the following:</span></span>

-   <span data-ttu-id="cb466-106">Flujo de transacción</span><span class="sxs-lookup"><span data-stu-id="cb466-106">Transaction flow</span></span>
-   <span data-ttu-id="cb466-107">Cómo votan varios objetos en una transacción</span><span class="sxs-lookup"><span data-stu-id="cb466-107">How multiple objects vote in a transaction</span></span>

## <a name="description"></a><span data-ttu-id="cb466-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="cb466-108">Description</span></span>

<span data-ttu-id="cb466-109">[Paso 1: crear un componente transaccional](step-1--creating-a-transactional-component.md) muestra cómo escribir un componente transaccional simple que actualiza la información de autor en la base de datos de Microsoft SQL Server pubs.</span><span class="sxs-lookup"><span data-stu-id="cb466-109">[Step 1: Creating a Transactional Component](step-1--creating-a-transactional-component.md) shows how to write a simple transactional component that updates author information in the Microsoft SQL Server Pubs database.</span></span> <span data-ttu-id="cb466-110">En el paso 2 se muestra lo que sucede cuando una transacción se extiende por varios componentes.</span><span class="sxs-lookup"><span data-stu-id="cb466-110">Step 2 shows what happens when a transaction is extended across multiple components.</span></span>

<span data-ttu-id="cb466-111">En consonancia con el modelo de programación COM+, `UpdateAuthorAddress` llama a otro componente en el transcurso de la finalización de su trabajo.</span><span class="sxs-lookup"><span data-stu-id="cb466-111">In keeping with the COM+ programming model, `UpdateAuthorAddress` calls another component in the course of completing its work.</span></span> <span data-ttu-id="cb466-112">El segundo componente, `ValidateAuthorAddress` , valida la dirección del autor y devuelve los resultados a su llamador, `UpdateAuthorAddress` .</span><span class="sxs-lookup"><span data-stu-id="cb466-112">The second component, `ValidateAuthorAddress`, validates the author's address and returns the results to its caller, `UpdateAuthorAddress`.</span></span>

<span data-ttu-id="cb466-113">A diferencia de su llamador, no `ValidateAuthorAddress` requiere una transacción, pero todavía puede participar en la transacción del llamador.</span><span class="sxs-lookup"><span data-stu-id="cb466-113">Unlike its caller, `ValidateAuthorAddress` does not require a transaction, but it can still participate in its caller's transaction.</span></span> <span data-ttu-id="cb466-114">En este paso, su valor de atributo de transacción se establece en **compatible**, tal como se muestra en la siguiente ilustración, que extiende la transacción existente al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="cb466-114">In this step, its transaction attribute value is set to **Supported**, as shown in the following illustration, which extends the existing transaction to the new object.</span></span>

![Diagrama que muestra la extensión de la transacción existente al nuevo objeto.](images/f58acb34-55db-40a4-8c48-f51ad024ff7e.png)

<span data-ttu-id="cb466-116">El valor de atributo **compatible** extiende (o fluye) una transacción existente solo cuando el autor de la llamada es transaccional.</span><span class="sxs-lookup"><span data-stu-id="cb466-116">The **Supported** attribute value extends (or flows) an existing transaction only when the caller is transactional.</span></span> <span data-ttu-id="cb466-117">Cuando `UpdateAuthorAddress` llama a `ValidateAuthorAddress` , com+ busca primero en el contexto del autor de la llamada para ver si es transaccional.</span><span class="sxs-lookup"><span data-stu-id="cb466-117">When `UpdateAuthorAddress` calls `ValidateAuthorAddress`, COM+ first looks at the caller's context to see whether it is transactional.</span></span> <span data-ttu-id="cb466-118">Después, COM+ examina los atributos de servicio que están establecidos en `ValidateAuthorAddress` y asigna al nuevo objeto el mismo identificador de transacción que se asigna al objeto de llamador.</span><span class="sxs-lookup"><span data-stu-id="cb466-118">COM+ then looks at the service attributes that are set on `ValidateAuthorAddress` and assigns the new object the same transaction identifier that is assigned to the caller object.</span></span> <span data-ttu-id="cb466-119">Para comprender mejor este proceso, consulte [activación de contexto](context-activation.md).</span><span class="sxs-lookup"><span data-stu-id="cb466-119">To better understand this process, see [Context Activation](context-activation.md).</span></span>

<span data-ttu-id="cb466-120">Dado que comparten el mismo identificador de transacción, ambos objetos deben completar su trabajo correctamente o COM+ anula la transacción (deshaciendo los cambios realizados en la base de datos pubs).</span><span class="sxs-lookup"><span data-stu-id="cb466-120">Because they share the same transaction identifier, both objects must complete their work successfully or COM+ aborts the transaction (undoing any changes made to the Pubs database).</span></span>

<span data-ttu-id="cb466-121">Todos los objetos que participan en una transacción votan para confirmar o anular la transacción.</span><span class="sxs-lookup"><span data-stu-id="cb466-121">All objects participating in a transaction vote to either commit or abort the transaction.</span></span> <span data-ttu-id="cb466-122">La votación se produce explícitamente cuando se incluyen instrucciones de votación en el código, tal y como se muestra en la siguiente extracción del código de ejemplo del paso 1, que crea el `UpdateAuthorAddress` componente:</span><span class="sxs-lookup"><span data-stu-id="cb466-122">Voting occurs explicitly when you include voting instructions in your code, as shown in the following extraction from the Step 1 Sample Code, which creates the `UpdateAuthorAddress` component:</span></span>


```VB
  ' Everything works.
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn True
  Exit Sub
  
UnexpectedError:
  ' There's an error.
  contextstate.SetMyTransactionVote TxAbort
  contextstate.SetDeactivateOnReturn True
```



<span data-ttu-id="cb466-123">La votación también se produce implícitamente, como se hace en el `ValidateAuthorAddress` componente.</span><span class="sxs-lookup"><span data-stu-id="cb466-123">Voting also occurs implicitly, as is done in the `ValidateAuthorAddress` component.</span></span> <span data-ttu-id="cb466-124">A menos que el objeto declare lo contrario, COM+ supone que un objeto ha completado su trabajo correctamente, pero que no está listo para desactivarse.</span><span class="sxs-lookup"><span data-stu-id="cb466-124">Unless the object declares otherwise, COM+ assumes an object has completed its work successfully but that it is not ready to be deactivated.</span></span> <span data-ttu-id="cb466-125">COM+ hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cb466-125">COM+ makes the following assumption:</span></span>


```VB
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn False
```



<span data-ttu-id="cb466-126">Cuando `ValidateAuthorAddress` vuelve a su llamador, com+ lee su votación como confirmación.</span><span class="sxs-lookup"><span data-stu-id="cb466-126">When `ValidateAuthorAddress` returns to its caller, COM+ reads its vote as a commit.</span></span> <span data-ttu-id="cb466-127">COM+ no cuenta los votos hasta que desactiva el objeto raíz, que es el primer objeto de la transacción en este caso, el `UpdateAuthorAddress` objeto.</span><span class="sxs-lookup"><span data-stu-id="cb466-127">COM+ doesn't count the votes until it deactivates the root object, which is the first object in the transaction in this case, the `UpdateAuthorAddress` object.</span></span>

## <a name="sample-code"></a><span data-ttu-id="cb466-128">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="cb466-128">Sample code</span></span>

<span data-ttu-id="cb466-129">El `ValidateAuthorAddress` componente realiza una comprobación simple de la dirección del autor.</span><span class="sxs-lookup"><span data-stu-id="cb466-129">The `ValidateAuthorAddress` component makes a simple check of the author's address.</span></span> <span data-ttu-id="cb466-130">Dado `UpdateAuthorAddress` que no vota explícitamente, com+ usa la configuración de votación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="cb466-130">Because `UpdateAuthorAddress` does not vote explicitly, COM+ uses the default vote settings.</span></span>


```VB
Option Explicit
'
'   Purpose:   This class is used for validating an author's address
'              (presumably right before updating that address in the
'              database).
'
'   Notes:   This component could be in a transaction or not; it doesn't 
'            matter because it doesn't touch any data in a database.
'
Public Function ValidateAuthorAddress( _
                        ByVal strAddress As String, _
                        ByVal strCity As String, _
                        ByVal strState As String, _
                        ByVal strZip As String) As Boolean
  ' Default is to validate unless something is found to be wrong.
  ValidateAuthorAddress = True
                                                  
  '  Invalidate authors who live in New York City
  '  and authors who live in Montana.
  '
  If strCity = "New York" And strState = "New York" Then
    ValidateAuthorAddress = False
  ElseIf strState = "Montana" Then
    ValidateAuthorAddress = False
  End If
  ' Done
End Function
```



## <a name="summary"></a><span data-ttu-id="cb466-131">Resumen</span><span class="sxs-lookup"><span data-stu-id="cb466-131">Summary</span></span>

-   <span data-ttu-id="cb466-132">Establecer el atributo de transacción de un componente en **compatible** puede dar lugar a que se cree el nuevo objeto en la transacción del objeto que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="cb466-132">Setting a component's transaction attribute to **Supported** can result in the new object being created in the calling object's transaction.</span></span> <span data-ttu-id="cb466-133">COM+ examina el contexto del llamador para determinar el estado transaccional del nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="cb466-133">COM+ looks at the caller's context to determine the transactional status of the new object.</span></span> <span data-ttu-id="cb466-134">Si el autor de la llamada es transaccional, COM+ transfiere la transacción al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="cb466-134">If the caller is transactional, COM+ flows the transaction to the new object.</span></span>
-   <span data-ttu-id="cb466-135">Todos los objetos que participan en la misma transacción comparten un identificador de transacción común, que COM+ lee en el contexto del objeto.</span><span class="sxs-lookup"><span data-stu-id="cb466-135">All objects participating in the same transaction share a common transaction identifier, which COM+ reads from the object's context.</span></span>
-   <span data-ttu-id="cb466-136">Cada objeto de una transacción vota independientemente de otros objetos.</span><span class="sxs-lookup"><span data-stu-id="cb466-136">Each object in a transaction votes independently of other objects.</span></span> <span data-ttu-id="cb466-137">COM+ cuenta los votos cuando se desactiva el objeto raíz.</span><span class="sxs-lookup"><span data-stu-id="cb466-137">COM+ counts the votes when the root object is deactivated.</span></span>
-   <span data-ttu-id="cb466-138">Puede alternar el voto de transacciones de un objeto entre commit y Abort hasta que COM+ desactive el objeto o hasta que COM+ desactive el objeto raíz y finalice la transacción.</span><span class="sxs-lookup"><span data-stu-id="cb466-138">You can toggle an object's transaction vote between commit and abort until COM+ deactivates the object or until COM+ deactivates the root object and ends the transaction.</span></span> <span data-ttu-id="cb466-139">Solo el último valor de votación es Count.</span><span class="sxs-lookup"><span data-stu-id="cb466-139">Only the last vote setting counts.</span></span> <span data-ttu-id="cb466-140">Las interfaces [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) y [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) proporcionan métodos y que generan resultados de votación similares, tal como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="cb466-140">The [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) and [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) interfaces provide methods and that produce similar voting results as shown in the following table.</span></span> <span data-ttu-id="cb466-141">Puede utilizar cualquiera de las interfaces para votar explícitamente en una transacción.</span><span class="sxs-lookup"><span data-stu-id="cb466-141">You can use either interface to vote explicitly in a transaction.</span></span> 

    | <span data-ttu-id="cb466-142">Métodos de combinación de [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)</span><span class="sxs-lookup"><span data-stu-id="cb466-142">[**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) combination methods</span></span>                                                                                                                                                      | <span data-ttu-id="cb466-143">Método equivalente de [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)</span><span class="sxs-lookup"><span data-stu-id="cb466-143">[**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) equivalent method</span></span>       |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
    | <span data-ttu-id="cb466-144">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxCommit**</span><span class="sxs-lookup"><span data-stu-id="cb466-144">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = **TxCommit**</span></span><br/> <span data-ttu-id="cb466-145">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **true**</span><span class="sxs-lookup"><span data-stu-id="cb466-145">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = **True**</span></span><br/>  | [<span data-ttu-id="cb466-146">**SetComplete**</span><span class="sxs-lookup"><span data-stu-id="cb466-146">**SetComplete**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)<br/>     |
    | <span data-ttu-id="cb466-147">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxCommit**</span><span class="sxs-lookup"><span data-stu-id="cb466-147">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = **TxCommit**</span></span><br/> <span data-ttu-id="cb466-148">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **false**</span><span class="sxs-lookup"><span data-stu-id="cb466-148">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = **False**</span></span><br/> | [<span data-ttu-id="cb466-149">**EnableCommit**</span><span class="sxs-lookup"><span data-stu-id="cb466-149">**EnableCommit**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit)<br/>   |
    | <span data-ttu-id="cb466-150">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxAbort**</span><span class="sxs-lookup"><span data-stu-id="cb466-150">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = **TxAbort**</span></span><br/> <span data-ttu-id="cb466-151">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **true**</span><span class="sxs-lookup"><span data-stu-id="cb466-151">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = **True**</span></span><br/>   | [<span data-ttu-id="cb466-152">**Tabor**</span><span class="sxs-lookup"><span data-stu-id="cb466-152">**SetAbort**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)<br/>           |
    | <span data-ttu-id="cb466-153">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxAbort**</span><span class="sxs-lookup"><span data-stu-id="cb466-153">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = **TxAbort**</span></span><br/> <span data-ttu-id="cb466-154">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **false**</span><span class="sxs-lookup"><span data-stu-id="cb466-154">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = **False**</span></span><br/>  | [<span data-ttu-id="cb466-155">**DisableCommit**</span><span class="sxs-lookup"><span data-stu-id="cb466-155">**DisableCommit**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)<br/> |

    

     

-   <span data-ttu-id="cb466-156">COM+ establece el voto de un objeto en el equivalente de [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) a menos que el componente vote explícitamente.</span><span class="sxs-lookup"><span data-stu-id="cb466-156">COM+ sets an object's vote to the equivalent of [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) unless the component votes explicitly.</span></span>
-   <span data-ttu-id="cb466-157">La votación explícitamente puede reducir la duración total de la transacción y liberar bloqueos de recursos costosos.</span><span class="sxs-lookup"><span data-stu-id="cb466-157">Voting explicitly can reduce the overall duration of the transaction and release expensive resource locks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb466-158">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cb466-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb466-159">Paso 1: crear un componente transaccional</span><span class="sxs-lookup"><span data-stu-id="cb466-159">Step 1: Creating a Transactional Component</span></span>](step-1--creating-a-transactional-component.md)
</dt> <dt>

[<span data-ttu-id="cb466-160">Paso 3: reutilización de componentes</span><span class="sxs-lookup"><span data-stu-id="cb466-160">Step 3: Reusing Components</span></span>](step-3--reusing-components.md)
</dt> <dt>

[<span data-ttu-id="cb466-161">Activación de contexto</span><span class="sxs-lookup"><span data-stu-id="cb466-161">Context Activation</span></span>](context-activation.md)
</dt> <dt>

[<span data-ttu-id="cb466-162">Administrar transacciones automáticas en COM+</span><span class="sxs-lookup"><span data-stu-id="cb466-162">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 




