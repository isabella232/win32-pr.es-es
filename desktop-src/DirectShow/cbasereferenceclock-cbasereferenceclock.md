---
description: Método de constructor.
ms.assetid: 0fbfdc68-e1df-449f-a7d1-739504db8a2f
title: Constructor CBaseReferenceClock. CBaseReferenceClock (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.CBaseReferenceClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5ad593d488e367ad6e902b0c931ffbfc3f741a53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671253"
---
# <a name="cbasereferenceclockcbasereferenceclock-constructor"></a><span data-ttu-id="c25a5-103">Constructor CBaseReferenceClock. CBaseReferenceClock</span><span class="sxs-lookup"><span data-stu-id="c25a5-103">CBaseReferenceClock.CBaseReferenceClock constructor</span></span>

<span data-ttu-id="c25a5-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="c25a5-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c25a5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c25a5-105">Syntax</span></span>


```C++
CBaseReferenceClock(
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr,
   CAMSchedule *pSched = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="c25a5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c25a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c25a5-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="c25a5-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="c25a5-108">Puntero a una cadena que contiene el nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="c25a5-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="c25a5-109">Para obtener más información, vea [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="c25a5-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="c25a5-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="c25a5-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="c25a5-111">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="c25a5-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="c25a5-112">Si se agrega el objeto, pase un puntero a la interfaz IUnknown del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="c25a5-112">If the object is aggregated, pass a pointer to the aggregating object's IUnknown interface.</span></span> <span data-ttu-id="c25a5-113">De lo contrario, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="c25a5-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c25a5-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="c25a5-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="c25a5-115">Puntero a un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c25a5-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="c25a5-116">Si se produce un error, el método devuelve un código de error en este parámetro.</span><span class="sxs-lookup"><span data-stu-id="c25a5-116">If an error occurs, the method returns an error code in this parameter.</span></span> <span data-ttu-id="c25a5-117">No establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="c25a5-117">Do not set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c25a5-118">*pSched*</span><span class="sxs-lookup"><span data-stu-id="c25a5-118">*pSched*</span></span> 
</dt> <dd>

<span data-ttu-id="c25a5-119">Puntero a un objeto [**CAMSchedule**](camschedule.md) .</span><span class="sxs-lookup"><span data-stu-id="c25a5-119">Pointer to a [**CAMSchedule**](camschedule.md) object.</span></span> <span data-ttu-id="c25a5-120">Si **es null**, este método crea un nuevo objeto **CAMSchedule** .</span><span class="sxs-lookup"><span data-stu-id="c25a5-120">If **NULL**, this method creates a new **CAMSchedule** object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c25a5-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c25a5-121">Requirements</span></span>



| <span data-ttu-id="c25a5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c25a5-122">Requirement</span></span> | <span data-ttu-id="c25a5-123">Value</span><span class="sxs-lookup"><span data-stu-id="c25a5-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c25a5-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c25a5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c25a5-125"><dt>Refclock. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c25a5-125"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c25a5-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c25a5-126">Library</span></span><br/> | <dl> <span data-ttu-id="c25a5-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c25a5-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c25a5-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="c25a5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c25a5-129">**Clase CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="c25a5-129">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




