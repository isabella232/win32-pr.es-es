---
description: Crea un objeto transaccional genérico que comienza una transacción. Al llamar a los métodos de esta clase, puede crear el trabajo de varios objetos COM en una única transacción y confirmar o anular explícitamente la transacción.
ms.assetid: 5f3f83e0-33fc-4c43-9327-59485c0d8bd3
title: Clase TransactionContextEx (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransactionContextEx
api_type:
- COM
ms.openlocfilehash: 8cf5c3aaa7ffe126124a909498a7c54cfb012c65
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807778"
---
# <a name="transactioncontextex-class"></a><span data-ttu-id="3e18f-104">Clase TransactionContextEx</span><span class="sxs-lookup"><span data-stu-id="3e18f-104">TransactionContextEx class</span></span>

<span data-ttu-id="3e18f-105">Crea un objeto transaccional genérico que comienza una transacción.</span><span class="sxs-lookup"><span data-stu-id="3e18f-105">Creates a generic transactional object that begins a transaction.</span></span> <span data-ttu-id="3e18f-106">Al llamar a los métodos de esta clase, puede crear el trabajo de varios objetos COM en una única transacción y confirmar o anular explícitamente la transacción.</span><span class="sxs-lookup"><span data-stu-id="3e18f-106">By calling the methods of this class, you can compose the work of multiple COM objects in a single transaction and explicitly commit or abort the transaction.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="3e18f-107">Cuándo implementar</span><span class="sxs-lookup"><span data-stu-id="3e18f-107">When to implement</span></span>

<span data-ttu-id="3e18f-108">Esta clase se implementa mediante COM+.</span><span class="sxs-lookup"><span data-stu-id="3e18f-108">This class is implemented by COM+.</span></span>



| <span data-ttu-id="3e18f-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e18f-109">Requirement</span></span> | <span data-ttu-id="3e18f-110">Value</span><span class="sxs-lookup"><span data-stu-id="3e18f-110">Value</span></span> |
|------------|--------------------------------------------------------|
| <span data-ttu-id="3e18f-111">CLSID</span><span class="sxs-lookup"><span data-stu-id="3e18f-111">CLSID</span></span>      | <span data-ttu-id="3e18f-112">CLSID \_ TransactionContextEx</span><span class="sxs-lookup"><span data-stu-id="3e18f-112">CLSID\_TransactionContextEx</span></span>                            |
| <span data-ttu-id="3e18f-113">ProgID</span><span class="sxs-lookup"><span data-stu-id="3e18f-113">ProgID</span></span>     | <span data-ttu-id="3e18f-114">L "TxCTx. TransactionContextEx"</span><span class="sxs-lookup"><span data-stu-id="3e18f-114">L"TxCTx.TransactionContextEx"</span></span>                          |
| <span data-ttu-id="3e18f-115">Interfaces</span><span class="sxs-lookup"><span data-stu-id="3e18f-115">Interfaces</span></span> | [<span data-ttu-id="3e18f-116">**ITransactionContextEx**</span><span class="sxs-lookup"><span data-stu-id="3e18f-116">**ITransactionContextEx**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontextex) |



 

## <a name="when-to-use"></a><span data-ttu-id="3e18f-117">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="3e18f-117">When to use</span></span>

<span data-ttu-id="3e18f-118">Un cliente no transaccional utiliza esta clase para iniciar una transacción.</span><span class="sxs-lookup"><span data-stu-id="3e18f-118">A non-transactional client uses this class to begin a transaction.</span></span> <span data-ttu-id="3e18f-119">Mediante los métodos de esta clase, el cliente puede llamar a objetos COM adicionales que, si están configurados para participar en una transacción, se ejecutan dentro del límite de la transacción del objeto de contexto de transacción.</span><span class="sxs-lookup"><span data-stu-id="3e18f-119">Using the methods of this class, the client can call additional COM objects that, if configured to participate in a transaction, run within the transaction boundary of the transaction context object.</span></span> <span data-ttu-id="3e18f-120">En función de su lógica de negocios, el cliente puede confirmar o anular explícitamente la transacción.</span><span class="sxs-lookup"><span data-stu-id="3e18f-120">Based on its business logic, the client can explicitly commit or abort the transaction.</span></span>

<span data-ttu-id="3e18f-121">La clase **TransactionContextEx** limita la reutilización de la lógica de negocios que conduce a la transacción.</span><span class="sxs-lookup"><span data-stu-id="3e18f-121">The **TransactionContextEx** class limits reuse of the business logic driving the transaction.</span></span> <span data-ttu-id="3e18f-122">Por esta razón, se recomienda que los objetos con instancias de la clase **TransactionContextEx** se utilicen con moderación.</span><span class="sxs-lookup"><span data-stu-id="3e18f-122">For this reason, it is recommended that objects instantiated from the **TransactionContextEx** class be used sparingly.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e18f-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e18f-123">Remarks</span></span>

<span data-ttu-id="3e18f-124">Para crear este objeto, llame a [**IObjectContext:: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span><span class="sxs-lookup"><span data-stu-id="3e18f-124">To create this object, call [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span></span>

<span data-ttu-id="3e18f-125">La clase **TransactionContextEx** no está diseñada para utilizarse en Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3e18f-125">The **TransactionContextEx** class was not designed to be used in Visual Basic.</span></span> <span data-ttu-id="3e18f-126">En su lugar, use la clase [**TransactionContext**](transactioncontext.md) .</span><span class="sxs-lookup"><span data-stu-id="3e18f-126">Use the [**TransactionContext**](transactioncontext.md) class instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e18f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e18f-127">Requirements</span></span>



| <span data-ttu-id="3e18f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e18f-128">Requirement</span></span> | <span data-ttu-id="3e18f-129">Value</span><span class="sxs-lookup"><span data-stu-id="3e18f-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3e18f-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e18f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3e18f-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3e18f-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3e18f-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e18f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3e18f-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3e18f-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3e18f-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e18f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e18f-135"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e18f-135"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e18f-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e18f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e18f-137">Configuración de transacciones</span><span class="sxs-lookup"><span data-stu-id="3e18f-137">Configuring Transactions</span></span>](configuring-transactions.md)
</dt> <dt>

[<span data-ttu-id="3e18f-138">**ITransactionContextEx**</span><span class="sxs-lookup"><span data-stu-id="3e18f-138">**ITransactionContextEx**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontextex)
</dt> <dt>

[<span data-ttu-id="3e18f-139">**TransactionContext**</span><span class="sxs-lookup"><span data-stu-id="3e18f-139">**TransactionContext**</span></span>](transactioncontext.md)
</dt> </dl>

 

 




