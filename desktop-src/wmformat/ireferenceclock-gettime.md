---
title: IReferenceClock GetTime (método)
description: El método GetTime recupera la hora de referencia actual.
ms.assetid: 9bf5050a-ae09-4a72-a3f2-3df8339d99b9
keywords:
- Método GetTime formato de Windows Media
- Método GetTime formato de Windows Media, interfaz IReferenceClock
- Interfaz IReferenceClock formato de Windows Media, método GetTime
topic_type:
- apiref
api_name:
- IReferenceClock.GetTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c679ce0adbbc6cc7ddc014c12f1b0ace4be6b4b0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419737"
---
# <a name="ireferenceclockgettime-method"></a><span data-ttu-id="977aa-106">IReferenceClock:: GetTime (método)</span><span class="sxs-lookup"><span data-stu-id="977aa-106">IReferenceClock::GetTime method</span></span>

<span data-ttu-id="977aa-107">El método **getTime** recupera la hora de referencia actual.</span><span class="sxs-lookup"><span data-stu-id="977aa-107">The **GetTime** method retrieves the current reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="977aa-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="977aa-108">Syntax</span></span>


```C++
HRESULT GetTime(
  [out] REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a><span data-ttu-id="977aa-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="977aa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="977aa-110">*pTime* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="977aa-110">*pTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="977aa-111">Puntero a una variable que recibe la hora actual, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="977aa-111">Pointer to a variable that receives the current time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="977aa-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="977aa-112">Return value</span></span>

<span data-ttu-id="977aa-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="977aa-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="977aa-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="977aa-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="977aa-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="977aa-115">Return code</span></span>                                                                               | <span data-ttu-id="977aa-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="977aa-116">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="977aa-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="977aa-117"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="977aa-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="977aa-118">The method succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="977aa-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="977aa-119"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="977aa-120">El parámetro *pTime* es **null**.</span><span class="sxs-lookup"><span data-stu-id="977aa-120">The *pTime* parameter is **NULL**.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="977aa-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="977aa-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="977aa-122">**Interfaz IReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="977aa-122">**IReferenceClock Interface**</span></span>](ireferenceclock.md)
</dt> </dl>

 

 





