---
title: IReferenceClock AdviseTime, método
description: El método AdviseTime solicita una notificación asincrónica de que ha transcurrido una hora.
ms.assetid: 8f3f8713-b53c-4110-ac7a-724bbc49368e
keywords:
- Método AdviseTime formato de Windows Media
- Método AdviseTime formato de Windows Media, interfaz IReferenceClock
- Interfaz IReferenceClock formato de Windows Media, método AdviseTime
topic_type:
- apiref
api_name:
- IReferenceClock.AdviseTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3fa91338b4bff8f925f00e7159a36089e0de0aa8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105720093"
---
# <a name="ireferenceclockadvisetime-method"></a><span data-ttu-id="86e96-106">IReferenceClock:: AdviseTime (método)</span><span class="sxs-lookup"><span data-stu-id="86e96-106">IReferenceClock::AdviseTime method</span></span>

<span data-ttu-id="86e96-107">El método **AdviseTime** solicita una notificación asincrónica de que ha transcurrido una hora.</span><span class="sxs-lookup"><span data-stu-id="86e96-107">The **AdviseTime** method requests an asynchronous notification that a time has elapsed.</span></span>

## <a name="syntax"></a><span data-ttu-id="86e96-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="86e96-108">Syntax</span></span>


```C++
HRESULT AdviseTime(
  [in]  REFERENCE_TIME rtBaseTime,
  [in]  REFERENCE_TIME rtStreamTime,
  [in]  HEVENT         hEvent,
  [out] DWORD          *pdwAdviseCookie
);
```



## <a name="parameters"></a><span data-ttu-id="86e96-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86e96-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86e96-110">*rtBaseTime* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="86e96-110">*rtBaseTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86e96-111">Tiempo de referencia base, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="86e96-111">Base reference time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="86e96-112">*rtStreamTime* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="86e96-112">*rtStreamTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86e96-113">Tiempo de desplazamiento de flujo, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="86e96-113">Stream offset time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="86e96-114">*hEvent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="86e96-114">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86e96-115">Identificador de un evento creado por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="86e96-115">Handle to an event, created by the caller.</span></span> <span data-ttu-id="86e96-116">Este evento se señalará cuando transcurra la hora especificada.</span><span class="sxs-lookup"><span data-stu-id="86e96-116">This event will be signaled when the time specified elapses.</span></span>

</dd> <dt>

<span data-ttu-id="86e96-117">*pdwAdviseCookie* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="86e96-117">*pdwAdviseCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86e96-118">Puntero a una variable que recibe un identificador para la solicitud.</span><span class="sxs-lookup"><span data-stu-id="86e96-118">Pointer to a variable that receives an identifier for the request.</span></span> <span data-ttu-id="86e96-119">Se usa para identificar esta llamada a **AdviseTime** en el futuro, por ejemplo, para cancelar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="86e96-119">This is used to identify this call to **AdviseTime** in the future for example, to cancel the request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86e96-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="86e96-120">Return value</span></span>

<span data-ttu-id="86e96-121">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="86e96-121">The method returns an **HRESULT**.</span></span> <span data-ttu-id="86e96-122">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="86e96-122">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="86e96-123">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="86e96-123">Return code</span></span>                                                                               | <span data-ttu-id="86e96-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="86e96-124">Description</span></span>                                             |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <span data-ttu-id="86e96-125"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="86e96-125"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="86e96-126">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="86e96-126">The method succeeded.</span></span><br/>                        |
| <dl> <span data-ttu-id="86e96-127"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="86e96-127"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="86e96-128">El parámetro *pdwAdviseCookie* es **null**.</span><span class="sxs-lookup"><span data-stu-id="86e96-128">The *pdwAdviseCookie* parameter is **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="86e96-129"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="86e96-129"><dt>**E\_FAIL**</dt></span></span> </dl>    | <span data-ttu-id="86e96-130">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="86e96-130">Unspecified failure.</span></span><br/>                         |



 

## <a name="see-also"></a><span data-ttu-id="86e96-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="86e96-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86e96-132">**Interfaz IReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="86e96-132">**IReferenceClock Interface**</span></span>](ireferenceclock.md)
</dt> </dl>

 

 





