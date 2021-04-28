---
description: 'Constructor CSourceSeeking.CSourceSeeking: método constructor.'
ms.assetid: a51d90c9-4046-42dc-b7cf-51b904c5f57a
title: Constructor CSourceSeeking.CSourceSeeking (Ctlutil.h)
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
ms.openlocfilehash: 7fcca70408e76466a88c620e3907271d49930973
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098823"
---
# <a name="csourceseekingcsourceseeking-constructor"></a><span data-ttu-id="75135-103">Constructor CSourceSeeking.CSourceSeeking</span><span class="sxs-lookup"><span data-stu-id="75135-103">CSourceSeeking.CSourceSeeking constructor</span></span>

<span data-ttu-id="75135-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="75135-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="75135-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75135-105">Syntax</span></span>


```C++
CSourceSeeking(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         CCritSec  *pLock
);
```



## <a name="parameters"></a><span data-ttu-id="75135-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75135-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75135-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="75135-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="75135-108">Puntero a una cadena que contiene el nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="75135-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="75135-109">Para obtener más información, vea [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="75135-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="75135-110">*Punk*</span><span class="sxs-lookup"><span data-stu-id="75135-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="75135-111">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="75135-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="75135-112">Si el objeto se agrega, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="75135-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="75135-113">De lo contrario, establezca este parámetro en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="75135-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="75135-114">*Phr*</span><span class="sxs-lookup"><span data-stu-id="75135-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="75135-115">Puntero a un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="75135-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="75135-116">ignorado.</span><span class="sxs-lookup"><span data-stu-id="75135-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="75135-117">*Plock*</span><span class="sxs-lookup"><span data-stu-id="75135-117">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="75135-118">Puntero a un [**objeto CCritSec.**](ccritsec.md)</span><span class="sxs-lookup"><span data-stu-id="75135-118">Pointer to a [**CCritSec**](ccritsec.md) object.</span></span> <span data-ttu-id="75135-119">En la clase derivada, declare una variable miembro **CCritSec** y use su dirección para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="75135-119">In your derived class, declare a **CCritSec** member variable and use the address of it for this parameter.</span></span> <span data-ttu-id="75135-120">La clase usa esta sección crítica para sincronizar el acceso a las horas de inicio y de `CSourceSeeking` detenerse, la duración y la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="75135-120">The `CSourceSeeking` class uses this critical section to synchronize access to the start and stop times, duration, and playback rate.</span></span> <span data-ttu-id="75135-121">Siempre que acceda a esas variables en la clase derivada, mantenga este bloqueo.</span><span class="sxs-lookup"><span data-stu-id="75135-121">Whenever you access those variables in your derived class, hold this lock.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="75135-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75135-122">Requirements</span></span>



| <span data-ttu-id="75135-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="75135-123">Requirement</span></span> | <span data-ttu-id="75135-124">Value</span><span class="sxs-lookup"><span data-stu-id="75135-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75135-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="75135-125">Header</span></span><br/>  | <dl> <span data-ttu-id="75135-126"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="75135-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="75135-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="75135-127">Library</span></span><br/> | <dl> <span data-ttu-id="75135-128"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="75135-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75135-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="75135-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75135-130">**CSourceSeeking (clase)**</span><span class="sxs-lookup"><span data-stu-id="75135-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




