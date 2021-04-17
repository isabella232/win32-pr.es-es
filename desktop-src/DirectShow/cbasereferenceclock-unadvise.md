---
description: 'El método Unadvise quita una solicitud de notificación pendiente. Este método implementa el método IReferenceClock:: unvise.'
ms.assetid: b137234a-e260-42f9-b583-9e6a5fd7bca4
title: Método CBaseReferenceClock. unvise (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.Unadvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 14daf1d34c8a6a923ec7e181ac69f9ecbae0160a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661185"
---
# <a name="cbasereferenceclockunadvise-method"></a><span data-ttu-id="8159f-104">CBaseReferenceClock. Unadvise (método)</span><span class="sxs-lookup"><span data-stu-id="8159f-104">CBaseReferenceClock.Unadvise method</span></span>

<span data-ttu-id="8159f-105">El `Unadvise` método quita una solicitud de notificación pendiente.</span><span class="sxs-lookup"><span data-stu-id="8159f-105">The `Unadvise` method removes a pending advise request.</span></span> <span data-ttu-id="8159f-106">Este método implementa el método [**IReferenceClock:: unvise**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-unadvise) .</span><span class="sxs-lookup"><span data-stu-id="8159f-106">This method implements the [**IReferenceClock::Unadvise**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-unadvise) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8159f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8159f-107">Syntax</span></span>


```C++
HRESULT Unadvise(
   DWORD_PTR dwAdviseToken
);
```



## <a name="parameters"></a><span data-ttu-id="8159f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8159f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8159f-109">*dwAdviseToken*</span><span class="sxs-lookup"><span data-stu-id="8159f-109">*dwAdviseToken*</span></span> 
</dt> <dd>

<span data-ttu-id="8159f-110">Identificador de la solicitud que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="8159f-110">Identifier of the request to remove.</span></span> <span data-ttu-id="8159f-111">Use el valor devuelto por los métodos [**CBaseReferenceClock:: AdviseTime**](cbasereferenceclock-advisetime.md) o [**CBaseReferenceClock:: AdvisePeriodic**](cbasereferenceclock-adviseperiodic.md) en el parámetro *pdwAdviseToken* .</span><span class="sxs-lookup"><span data-stu-id="8159f-111">Use the value returned by the [**CBaseReferenceClock::AdviseTime**](cbasereferenceclock-advisetime.md) or [**CBaseReferenceClock::AdvisePeriodic**](cbasereferenceclock-adviseperiodic.md) methods in the *pdwAdviseToken* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8159f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8159f-112">Return value</span></span>

<span data-ttu-id="8159f-113">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8159f-113">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="8159f-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8159f-114">Return code</span></span>                                                                             | <span data-ttu-id="8159f-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="8159f-115">Description</span></span>           |
|-----------------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="8159f-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="8159f-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="8159f-117">Not found.</span><span class="sxs-lookup"><span data-stu-id="8159f-117">Not found.</span></span><br/> |
| <dl> <span data-ttu-id="8159f-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="8159f-118"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="8159f-119">Correcto.</span><span class="sxs-lookup"><span data-stu-id="8159f-119">Success.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="8159f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8159f-120">Requirements</span></span>



| <span data-ttu-id="8159f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8159f-121">Requirement</span></span> | <span data-ttu-id="8159f-122">Value</span><span class="sxs-lookup"><span data-stu-id="8159f-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8159f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8159f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="8159f-124"><dt>Refclock. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8159f-124"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8159f-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8159f-125">Library</span></span><br/> | <dl> <span data-ttu-id="8159f-126"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="8159f-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8159f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="8159f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8159f-128">**Clase CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="8159f-128">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




