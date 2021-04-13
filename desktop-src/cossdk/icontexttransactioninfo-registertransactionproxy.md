---
description: Asocia una implementación de ITransactionProxy con el contexto actual.
ms.assetid: 64009632-b536-41fb-95ac-b23e2cbf18da
title: 'IContextTransactionInfo:: RegisterTransactionProxy (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.RegisterTransactionProxy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7b559453b0d4ed75f92f7a421be4c3a47e07fdf7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360077"
---
# <a name="icontexttransactioninforegistertransactionproxy-method"></a><span data-ttu-id="1b67d-103">IContextTransactionInfo:: RegisterTransactionProxy (método)</span><span class="sxs-lookup"><span data-stu-id="1b67d-103">IContextTransactionInfo::RegisterTransactionProxy method</span></span>

<span data-ttu-id="1b67d-104">Asocia una implementación de [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) con el contexto actual.</span><span class="sxs-lookup"><span data-stu-id="1b67d-104">Associates an [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) implementation with the current context.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b67d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1b67d-105">Syntax</span></span>


```C++
HRESULT RegisterTransactionProxy(
  [in]  ITransactionProxy *pProxy,
  [out] GUID              *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="1b67d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1b67d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b67d-107">*pProxy* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1b67d-107">*pProxy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b67d-108">Implementación de [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) que se va a asociar al contexto actual.</span><span class="sxs-lookup"><span data-stu-id="1b67d-108">An [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) implementation to associate with the current context.</span></span>

</dd> <dt>

<span data-ttu-id="1b67d-109">*pGuid* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1b67d-109">*pGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b67d-110">GUID que identifica el proxy de transacción.</span><span class="sxs-lookup"><span data-stu-id="1b67d-110">A GUID that identifies the transaction proxy.</span></span> <span data-ttu-id="1b67d-111">COM+ usa este GUID al llamar a [**ITransactionProxy:: commit**](/windows/desktop/api/ComSvcs/nf-comsvcs-itransactionproxy-commit) en el proxy de transacción.</span><span class="sxs-lookup"><span data-stu-id="1b67d-111">COM+ uses this GUID when calling [**ITransactionProxy::Commit**](/windows/desktop/api/ComSvcs/nf-comsvcs-itransactionproxy-commit) on the transaction proxy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b67d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b67d-112">Return value</span></span>

<span data-ttu-id="1b67d-113">Este método puede devolver los valores devueltos estándar E \_ INVALIDARG, e \_ OUTOFMEMORY e e \_ inesperados, así como los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="1b67d-113">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, and E\_UNEXPECTED, as well as the following values.</span></span>



| <span data-ttu-id="1b67d-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1b67d-114">Return code</span></span>                                                                                                     | <span data-ttu-id="1b67d-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b67d-115">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1b67d-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="1b67d-116"><dt>**S\_OK**</dt></span></span> </dl>                            | <span data-ttu-id="1b67d-117">El método se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="1b67d-117">The method completed successfully.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="1b67d-118"><dt>**CONTEXTO \_ E \_ ALREADYINTRANSACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="1b67d-118"><dt>**CONTEXT\_E\_ALREADYINTRANSACTION**</dt></span></span> </dl> | <span data-ttu-id="1b67d-119">El contexto actual ya tiene una implementación de [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) asociada.</span><span class="sxs-lookup"><span data-stu-id="1b67d-119">The current context already has an associated [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) implementation.</span></span><br/> |
| <dl> <span data-ttu-id="1b67d-120"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="1b67d-120"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                       | <span data-ttu-id="1b67d-121">El contexto actual hospeda una transacción de traiga su propia transacción o una transacción que no es raíz.</span><span class="sxs-lookup"><span data-stu-id="1b67d-121">The current context is hosting a Bring Your Own Transaction (BYOT) transaction or a non-root transaction.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="1b67d-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1b67d-122">Remarks</span></span>

<span data-ttu-id="1b67d-123">Solo se puede llamar al método **RegisterTransactionProxy** si el contexto actual es un contexto de transacción raíz.</span><span class="sxs-lookup"><span data-stu-id="1b67d-123">The **RegisterTransactionProxy** method can only be called if the current context is a root transaction context.</span></span> <span data-ttu-id="1b67d-124">No se puede llamar si el contexto hospeda una transacción de transacciones o no raíz.</span><span class="sxs-lookup"><span data-stu-id="1b67d-124">It cannot be called if the context is hosting a BYOT transaction or a non-root transaction.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b67d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b67d-125">Requirements</span></span>



| <span data-ttu-id="1b67d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b67d-126">Requirement</span></span> | <span data-ttu-id="1b67d-127">Value</span><span class="sxs-lookup"><span data-stu-id="1b67d-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="1b67d-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b67d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1b67d-129">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1b67d-129">Windows XP with SP2 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="1b67d-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b67d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1b67d-131">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="1b67d-131">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1b67d-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b67d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b67d-133">**IContextTransactionInfo**</span><span class="sxs-lookup"><span data-stu-id="1b67d-133">**IContextTransactionInfo**</span></span>](icontexttransactioninfo.md)
</dt> </dl>

 

 




