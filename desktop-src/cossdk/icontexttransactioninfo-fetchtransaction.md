---
description: Recupera el proxy de transacción o de transacción asociado al contexto actual, si existe.
ms.assetid: 2f85f395-3ec5-4c5a-a6db-c902cb8f8486
title: 'IContextTransactionInfo:: FetchTransaction (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.FetchTransaction
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0e753974f93539f051465f13a1ea92d7e0e3bfa1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153203"
---
# <a name="icontexttransactioninfofetchtransaction-method"></a><span data-ttu-id="174df-103">IContextTransactionInfo:: FetchTransaction (método)</span><span class="sxs-lookup"><span data-stu-id="174df-103">IContextTransactionInfo::FetchTransaction method</span></span>

<span data-ttu-id="174df-104">Recupera el proxy de transacción o de transacción asociado al contexto actual, si existe.</span><span class="sxs-lookup"><span data-stu-id="174df-104">Retrieves the transaction or transaction proxy that is associated with the current context, if any.</span></span>

## <a name="syntax"></a><span data-ttu-id="174df-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="174df-105">Syntax</span></span>


```C++
HRESULT FetchTransaction(
  [out, retval] IUnknown **pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="174df-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="174df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="174df-107">*pUnk* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="174df-107">*pUnk* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="174df-108">El proxy de transacción o transacción asociado al contexto actual; de lo contrario, **es null**.</span><span class="sxs-lookup"><span data-stu-id="174df-108">The transaction or transaction proxy that is associated with the current context; otherwise, **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="174df-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="174df-109">Return value</span></span>

<span data-ttu-id="174df-110">Este método puede devolver los valores devueltos estándar E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inesperados y S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="174df-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="174df-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="174df-111">Requirements</span></span>



| <span data-ttu-id="174df-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="174df-112">Requirement</span></span> | <span data-ttu-id="174df-113">Value</span><span class="sxs-lookup"><span data-stu-id="174df-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="174df-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="174df-114">Minimum supported client</span></span><br/> | <span data-ttu-id="174df-115">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="174df-115">Windows XP with SP2 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="174df-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="174df-116">Minimum supported server</span></span><br/> | <span data-ttu-id="174df-117">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="174df-117">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="174df-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="174df-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="174df-119">**IContextTransactionInfo**</span><span class="sxs-lookup"><span data-stu-id="174df-119">**IContextTransactionInfo**</span></span>](icontexttransactioninfo.md)
</dt> </dl>

 

 




