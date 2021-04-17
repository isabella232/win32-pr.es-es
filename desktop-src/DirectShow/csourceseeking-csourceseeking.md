---
description: Método de constructor.
ms.assetid: a51d90c9-4046-42dc-b7cf-51b904c5f57a
title: Constructor CSourceSeeking. CSourceSeeking (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.CSourceSeeking
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 309e926ddf001cf9933b19334992f5210fc7f17b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661038"
---
# <a name="csourceseekingcsourceseeking-constructor"></a><span data-ttu-id="056a6-103">Constructor CSourceSeeking. CSourceSeeking</span><span class="sxs-lookup"><span data-stu-id="056a6-103">CSourceSeeking.CSourceSeeking constructor</span></span>

<span data-ttu-id="056a6-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="056a6-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="056a6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="056a6-105">Syntax</span></span>


```C++
CSourceSeeking(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         CCritSec  *pLock
);
```



## <a name="parameters"></a><span data-ttu-id="056a6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="056a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="056a6-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="056a6-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="056a6-108">Puntero a una cadena que contiene el nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="056a6-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="056a6-109">Para obtener más información, vea [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="056a6-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="056a6-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="056a6-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="056a6-111">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="056a6-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="056a6-112">Si se agrega el objeto, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="056a6-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="056a6-113">De lo contrario, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="056a6-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="056a6-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="056a6-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="056a6-115">Puntero a un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="056a6-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="056a6-116">ignorado.</span><span class="sxs-lookup"><span data-stu-id="056a6-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="056a6-117">*pLock*</span><span class="sxs-lookup"><span data-stu-id="056a6-117">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="056a6-118">Puntero a un objeto [**CCritSec**](ccritsec.md) .</span><span class="sxs-lookup"><span data-stu-id="056a6-118">Pointer to a [**CCritSec**](ccritsec.md) object.</span></span> <span data-ttu-id="056a6-119">En la clase derivada, declare una variable de miembro **CCritSec** y use la dirección de esta para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="056a6-119">In your derived class, declare a **CCritSec** member variable and use the address of it for this parameter.</span></span> <span data-ttu-id="056a6-120">La `CSourceSeeking` clase utiliza esta sección crítica para sincronizar el acceso a las horas de inicio y de finalización, la duración y la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="056a6-120">The `CSourceSeeking` class uses this critical section to synchronize access to the start and stop times, duration, and playback rate.</span></span> <span data-ttu-id="056a6-121">Siempre que obtenga acceso a esas variables en la clase derivada, conserve este bloqueo.</span><span class="sxs-lookup"><span data-stu-id="056a6-121">Whenever you access those variables in your derived class, hold this lock.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="056a6-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="056a6-122">Requirements</span></span>



| <span data-ttu-id="056a6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="056a6-123">Requirement</span></span> | <span data-ttu-id="056a6-124">Value</span><span class="sxs-lookup"><span data-stu-id="056a6-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="056a6-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="056a6-125">Header</span></span><br/>  | <dl> <span data-ttu-id="056a6-126"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="056a6-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="056a6-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="056a6-127">Library</span></span><br/> | <dl> <span data-ttu-id="056a6-128"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="056a6-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="056a6-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="056a6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="056a6-130">**Clase CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="056a6-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




