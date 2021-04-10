---
description: Crea un objeto transaccional genérico que comienza una transacción.
ms.assetid: efaf1468-4973-472f-af91-85957a52b7df
title: Clase TransactionContext (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransactionContext
api_type:
- COM
ms.openlocfilehash: 595b5a3192b87420855eb43f1e1e33df37a45c23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275066"
---
# <a name="transactioncontext-class"></a><span data-ttu-id="8ca19-103">Clase TransactionContext</span><span class="sxs-lookup"><span data-stu-id="8ca19-103">TransactionContext class</span></span>

<span data-ttu-id="8ca19-104">Crea un objeto transaccional genérico que comienza una transacción.</span><span class="sxs-lookup"><span data-stu-id="8ca19-104">Creates a generic transactional object that begins a transaction.</span></span> <span data-ttu-id="8ca19-105">Al llamar a los métodos de esta clase, puede crear el trabajo de varios objetos COM en una única transacción y confirmar o anular explícitamente la transacción.</span><span class="sxs-lookup"><span data-stu-id="8ca19-105">By calling the methods of this class, you can compose the work of multiple COM objects in a single transaction and explicitly commit or abort the transaction.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="8ca19-106">Cuándo implementar</span><span class="sxs-lookup"><span data-stu-id="8ca19-106">When to implement</span></span>

<span data-ttu-id="8ca19-107">Esta clase se implementa mediante COM+.</span><span class="sxs-lookup"><span data-stu-id="8ca19-107">This class is implemented by COM+.</span></span>



| <span data-ttu-id="8ca19-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ca19-108">Requirement</span></span> | <span data-ttu-id="8ca19-109">Value</span><span class="sxs-lookup"><span data-stu-id="8ca19-109">Value</span></span> |
|------------|----------------------------------------------------|
| <span data-ttu-id="8ca19-110">CLSID</span><span class="sxs-lookup"><span data-stu-id="8ca19-110">CLSID</span></span>      | <span data-ttu-id="8ca19-111">CLSID \_ TransactionContext</span><span class="sxs-lookup"><span data-stu-id="8ca19-111">CLSID\_TransactionContext</span></span>                          |
| <span data-ttu-id="8ca19-112">ProgID</span><span class="sxs-lookup"><span data-stu-id="8ca19-112">ProgID</span></span>     | <span data-ttu-id="8ca19-113">L "TxCTx. TransactionContext"</span><span class="sxs-lookup"><span data-stu-id="8ca19-113">L"TxCTx.TransactionContext"</span></span>                        |
| <span data-ttu-id="8ca19-114">Interfaces</span><span class="sxs-lookup"><span data-stu-id="8ca19-114">Interfaces</span></span> | [<span data-ttu-id="8ca19-115">**ITransactionContext**</span><span class="sxs-lookup"><span data-stu-id="8ca19-115">**ITransactionContext**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext) |



 

## <a name="when-to-use"></a><span data-ttu-id="8ca19-116">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="8ca19-116">When to use</span></span>

<span data-ttu-id="8ca19-117">Un cliente no transaccional utiliza esta clase para iniciar una transacción.</span><span class="sxs-lookup"><span data-stu-id="8ca19-117">A non-transactional client uses this class to begin a transaction.</span></span> <span data-ttu-id="8ca19-118">Mediante los métodos de esta clase, el cliente puede llamar a objetos COM adicionales que, si están configurados para participar en una transacción, se ejecutan dentro del límite de la transacción del objeto de contexto de transacción.</span><span class="sxs-lookup"><span data-stu-id="8ca19-118">Using the methods of this class, the client can call additional COM objects that, if configured to participate in a transaction, run within the transaction boundary of the transaction context object.</span></span> <span data-ttu-id="8ca19-119">En función de su lógica de negocios, el cliente puede confirmar o anular explícitamente la transacción.</span><span class="sxs-lookup"><span data-stu-id="8ca19-119">Based on its business logic, the client can explicitly commit or abort the transaction.</span></span>

<span data-ttu-id="8ca19-120">La clase **TransactionContext** limita la reutilización de la lógica de negocios que conduce a la transacción.</span><span class="sxs-lookup"><span data-stu-id="8ca19-120">The **TransactionContext** class limits reuse of the business logic driving the transaction.</span></span> <span data-ttu-id="8ca19-121">Por esta razón, se recomienda que los objetos con instancias de la clase **TransactionContext** se utilicen con moderación.</span><span class="sxs-lookup"><span data-stu-id="8ca19-121">For this reason, it is recommended that objects instantiated from the **TransactionContext** class be used sparingly.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ca19-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ca19-122">Remarks</span></span>

<span data-ttu-id="8ca19-123">Para crear este objeto, llame a [**IObjectContext:: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span><span class="sxs-lookup"><span data-stu-id="8ca19-123">To create this object, call [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span></span>

<span data-ttu-id="8ca19-124">Para usar esta clase desde Microsoft Visual Basic, agregue una referencia a la biblioteca de tipos de servicios COM+.</span><span class="sxs-lookup"><span data-stu-id="8ca19-124">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="8ca19-125">Un objeto TransactionContext se puede declarar con "COMSVCSLib. TransactionContext" como nombre de clase.</span><span class="sxs-lookup"><span data-stu-id="8ca19-125">A TransactionContext object can be declared using "COMSVCSLib.TransactionContext" as the class name.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ca19-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ca19-126">Requirements</span></span>



| <span data-ttu-id="8ca19-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ca19-127">Requirement</span></span> | <span data-ttu-id="8ca19-128">Value</span><span class="sxs-lookup"><span data-stu-id="8ca19-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca19-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ca19-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8ca19-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8ca19-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8ca19-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ca19-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8ca19-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8ca19-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8ca19-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ca19-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ca19-134"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ca19-134"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ca19-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ca19-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ca19-136">Configuración de transacciones</span><span class="sxs-lookup"><span data-stu-id="8ca19-136">Configuring Transactions</span></span>](configuring-transactions.md)
</dt> <dt>

[<span data-ttu-id="8ca19-137">**ITransactionContext**</span><span class="sxs-lookup"><span data-stu-id="8ca19-137">**ITransactionContext**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext)
</dt> <dt>

[<span data-ttu-id="8ca19-138">**TransactionContextEx**</span><span class="sxs-lookup"><span data-stu-id="8ca19-138">**TransactionContextEx**</span></span>](transactioncontextex.md)
</dt> </dl>

 

 




