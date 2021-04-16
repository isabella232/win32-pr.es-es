---
description: Recupera el nivel de aislamiento y el valor de tiempo de espera de una transacción hospedada en el contexto de la transacción raíz.
ms.assetid: bb3ff03e-e69e-4a50-af36-4938eb4323df
title: 'IContextTransactionInfo:: GetTxIsolationLevelAndTimeout (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.GetTxIsolationLevelAndTimeout
api_type:
- COM
api_location: ''
ms.openlocfilehash: b8545a697e672af7206a69ffa19618d5b70e055c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696134"
---
# <a name="icontexttransactioninfogettxisolationlevelandtimeout-method"></a><span data-ttu-id="77c14-103">IContextTransactionInfo:: GetTxIsolationLevelAndTimeout (método)</span><span class="sxs-lookup"><span data-stu-id="77c14-103">IContextTransactionInfo::GetTxIsolationLevelAndTimeout method</span></span>

<span data-ttu-id="77c14-104">Recupera el nivel de aislamiento y el valor de tiempo de espera de una transacción hospedada en el contexto de la transacción raíz.</span><span class="sxs-lookup"><span data-stu-id="77c14-104">Retrieves the isolation level and timeout value of a transaction that is hosted in the root transaction context.</span></span>

## <a name="syntax"></a><span data-ttu-id="77c14-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="77c14-105">Syntax</span></span>


```C++
HRESULT GetTxIsolationLevelAndTimeout(
  [out] ISOLEVEL *pIsoLevel,
  [out] DWORD    *dwTime
);
```



## <a name="parameters"></a><span data-ttu-id="77c14-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="77c14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77c14-107">*pIsoLevel* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="77c14-107">*pIsoLevel* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77c14-108">Valor [ISOLATIONLEVEL](/previous-versions/windows/desktop/ms679234(v=vs.85)) de la transacción.</span><span class="sxs-lookup"><span data-stu-id="77c14-108">The [ISOLATIONLEVEL](/previous-versions/windows/desktop/ms679234(v=vs.85)) value for the transaction.</span></span>

</dd> <dt>

<span data-ttu-id="77c14-109">*dwTime* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="77c14-109">*dwTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77c14-110">Tiempo de espera de la transacción, en segundos.</span><span class="sxs-lookup"><span data-stu-id="77c14-110">The timeout of the transaction, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77c14-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="77c14-111">Return value</span></span>

<span data-ttu-id="77c14-112">Este método puede devolver los valores devueltos estándar E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inesperados y S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="77c14-112">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="77c14-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77c14-113">Requirements</span></span>



| <span data-ttu-id="77c14-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="77c14-114">Requirement</span></span> | <span data-ttu-id="77c14-115">Value</span><span class="sxs-lookup"><span data-stu-id="77c14-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="77c14-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77c14-116">Minimum supported client</span></span><br/> | <span data-ttu-id="77c14-117">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="77c14-117">Windows XP with SP2 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="77c14-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77c14-118">Minimum supported server</span></span><br/> | <span data-ttu-id="77c14-119">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="77c14-119">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="77c14-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="77c14-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77c14-121">**IContextTransactionInfo**</span><span class="sxs-lookup"><span data-stu-id="77c14-121">**IContextTransactionInfo**</span></span>](icontexttransactioninfo.md)
</dt> </dl>

 

