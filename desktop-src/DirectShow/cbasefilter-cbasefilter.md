---
description: 'Constructor CBaseFilter.CBaseFilter(const TCHAR \* , LNOWNOWN, CCritSec, \* REFCLSID, HRESULT \* ): método constructor.'
ms.assetid: 705a075e-3f0f-4e7d-94b6-3458f87b6718
title: Constructor CBaseFilter.CBaseFilter(const *TCHAR, LNOWNOWN, CCritSec,* REFCLSID, HRESULT*) (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.CBaseFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f85fc666d299d5e120f71cfeaec5fc2f88e72761
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120113"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-hresult-constructor"></a><span data-ttu-id="56ca2-103">Constructor CBaseFilter.CBaseFilter(const \* TCHAR, LNOWNOWN, CCritSec, \* REFCLSID, HRESULT \* )</span><span class="sxs-lookup"><span data-stu-id="56ca2-103">CBaseFilter.CBaseFilter(const TCHAR\*, LPUNKNOWN, CCritSec\*, REFCLSID, HRESULT\*) constructor</span></span>

<span data-ttu-id="56ca2-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="56ca2-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="56ca2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56ca2-105">Syntax</span></span>


```C++
CBaseFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid,
         HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="56ca2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="56ca2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56ca2-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="56ca2-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="56ca2-108">Puntero a una cadena que contiene el nombre del filtro, con fines de depuración.</span><span class="sxs-lookup"><span data-stu-id="56ca2-108">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="56ca2-109">*Punk*</span><span class="sxs-lookup"><span data-stu-id="56ca2-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="56ca2-110">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="56ca2-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="56ca2-111">Si el objeto se agrega, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="56ca2-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="56ca2-112">De lo contrario, establezca este parámetro en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="56ca2-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="56ca2-113">*Plock*</span><span class="sxs-lookup"><span data-stu-id="56ca2-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="56ca2-114">Puntero a un [**bloqueo CCritSec,**](ccritsec.md) que se usa para serializar los cambios de estado.</span><span class="sxs-lookup"><span data-stu-id="56ca2-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="56ca2-115">*Clsid*</span><span class="sxs-lookup"><span data-stu-id="56ca2-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="56ca2-116">Identificador de clase (CLSID) del filtro.</span><span class="sxs-lookup"><span data-stu-id="56ca2-116">Class identifier (CLSID) of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="56ca2-117">*Phr*</span><span class="sxs-lookup"><span data-stu-id="56ca2-117">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="56ca2-118">Puntero a un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="56ca2-118">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="56ca2-119">El constructor omite este parámetro.</span><span class="sxs-lookup"><span data-stu-id="56ca2-119">The constructor ignores this parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56ca2-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="56ca2-120">Remarks</span></span>

<span data-ttu-id="56ca2-121">Para el objeto de sección crítica, normalmente realizaría una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="56ca2-121">For the critical section object, you would typically do one of the following:</span></span>

-   <span data-ttu-id="56ca2-122">Derive una clase que herede **tanto CBaseFilter** como **CCritSec.**</span><span class="sxs-lookup"><span data-stu-id="56ca2-122">Derive a class that inherits both **CBaseFilter** and **CCritSec**.</span></span> <span data-ttu-id="56ca2-123">Para *pLock*, pase el `this` puntero.</span><span class="sxs-lookup"><span data-stu-id="56ca2-123">For *pLock*, pass the `this` pointer.</span></span>
-   <span data-ttu-id="56ca2-124">Derive una clase que hereda **CBaseFilter** y contiene una variable **miembro CCritSec.**</span><span class="sxs-lookup"><span data-stu-id="56ca2-124">Derive a class that inherits **CBaseFilter** and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="56ca2-125">Para *pLock*, pase la dirección de esa variable.</span><span class="sxs-lookup"><span data-stu-id="56ca2-125">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="56ca2-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56ca2-126">Requirements</span></span>



| <span data-ttu-id="56ca2-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="56ca2-127">Requirement</span></span> | <span data-ttu-id="56ca2-128">Value</span><span class="sxs-lookup"><span data-stu-id="56ca2-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56ca2-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56ca2-129">Header</span></span><br/>  | <dl> <span data-ttu-id="56ca2-130"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="56ca2-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="56ca2-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="56ca2-131">Library</span></span><br/> | <dl> <span data-ttu-id="56ca2-132"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="56ca2-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56ca2-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="56ca2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56ca2-134">**CBaseFilter (clase)**</span><span class="sxs-lookup"><span data-stu-id="56ca2-134">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




