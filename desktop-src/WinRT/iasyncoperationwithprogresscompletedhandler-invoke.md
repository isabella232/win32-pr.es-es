---
description: Invoca el método al que se llama cuando la operación asincrónica especificada informa del progreso.
ms.assetid: FB60DDC0-7521-4999-8DD8-175556004198
title: 'IAsyncOperationWithProgressCompletedHandler<TResult, TProgress>:: Invoke (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>.Invoke
api_type:
- COM
api_location: ''
ms.openlocfilehash: 469686cbd96dedc7f816fdd1f482d3474362688e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154305"
---
# <a name="iasyncoperationwithprogresscompletedhandlertresulttprogressinvoke-method"></a><span data-ttu-id="f2258-103">IAsyncOperationWithProgressCompletedHandler<TResult, TProgress>:: Invoke (método)</span><span class="sxs-lookup"><span data-stu-id="f2258-103">IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>::Invoke method</span></span>

<span data-ttu-id="f2258-104">Invoca el método al que se llama cuando la operación asincrónica especificada informa del progreso.</span><span class="sxs-lookup"><span data-stu-id="f2258-104">Invokes the method that is called when the specified asynchronous operation reports progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2258-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2258-105">Syntax</span></span>


```C++
HRESULT Invoke(
  [in] IAsyncOperationWithProgress<TResult,TProgress> *asyncInfo
);
```



## <a name="parameters"></a><span data-ttu-id="f2258-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2258-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2258-107">*asyncInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f2258-107">*asyncInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2258-108">Tipo: \**[**IAsyncOperationWithProgress<TResult, TProgress>**](/previous-versions//br205807(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="f2258-108">Type: \**[**IAsyncOperationWithProgress<TResult,TProgress>**](/previous-versions//br205807(v=vs.85))\** _</span></span>

<span data-ttu-id="f2258-109">La acción asincrónica que informa de la finalización.</span><span class="sxs-lookup"><span data-stu-id="f2258-109">The asynchronous action that reports completion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2258-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2258-110">Return value</span></span>

<span data-ttu-id="f2258-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="f2258-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="f2258-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f2258-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f2258-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f2258-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2258-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2258-114">Requirements</span></span>



| <span data-ttu-id="f2258-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2258-115">Requirement</span></span> | <span data-ttu-id="f2258-116">Value</span><span class="sxs-lookup"><span data-stu-id="f2258-116">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="f2258-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2258-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f2258-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f2258-118">Windows 8</span></span><br/>           |
| <span data-ttu-id="f2258-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2258-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f2258-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f2258-120">Windows Server 2012</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f2258-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2258-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="f2258-122">[**IAsyncOperationWithProgressCompletedHandler<TResult, TProgress>**](/previous-versions//br205808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f2258-122">[**IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>**](/previous-versions//br205808(v=vs.85))</span></span>
</dt> </dl>

 

 
