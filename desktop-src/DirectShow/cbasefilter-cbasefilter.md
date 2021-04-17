---
description: Método de constructor.
ms.assetid: 705a075e-3f0f-4e7d-94b6-3458f87b6718
title: Constructor CBaseFilter. CBaseFilter (const TCHAR *, LPUNKNOWN, CCritSec*, REFCLSID, HRESULT *) (Amfilter. h)
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
ms.openlocfilehash: b4d8806c9b4103c06eb58e11547e83fc933d5d3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660575"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-hresult-constructor"></a><span data-ttu-id="6a219-103">Constructor CBaseFilter. CBaseFilter (const TCHAR \* , LPUNKNOWN, CCritSec \* , REFCLSID, HRESULT \* )</span><span class="sxs-lookup"><span data-stu-id="6a219-103">CBaseFilter.CBaseFilter(const TCHAR\*, LPUNKNOWN, CCritSec\*, REFCLSID, HRESULT\*) constructor</span></span>

<span data-ttu-id="6a219-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="6a219-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a219-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a219-105">Syntax</span></span>


```C++
CBaseFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid,
         HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="6a219-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6a219-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a219-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="6a219-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="6a219-108">Puntero a una cadena que contiene el nombre del filtro, con fines de depuración.</span><span class="sxs-lookup"><span data-stu-id="6a219-108">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="6a219-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="6a219-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="6a219-110">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="6a219-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="6a219-111">Si se agrega el objeto, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="6a219-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="6a219-112">De lo contrario, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="6a219-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6a219-113">*pLock*</span><span class="sxs-lookup"><span data-stu-id="6a219-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="6a219-114">Puntero a un bloqueo de [**CCritSec**](ccritsec.md) , que se usa para serializar los cambios de estado.</span><span class="sxs-lookup"><span data-stu-id="6a219-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="6a219-115">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="6a219-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="6a219-116">Identificador de clase (CLSID) del filtro.</span><span class="sxs-lookup"><span data-stu-id="6a219-116">Class identifier (CLSID) of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="6a219-117">*phr*</span><span class="sxs-lookup"><span data-stu-id="6a219-117">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="6a219-118">Puntero a un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6a219-118">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="6a219-119">El constructor omite este parámetro.</span><span class="sxs-lookup"><span data-stu-id="6a219-119">The constructor ignores this parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a219-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a219-120">Remarks</span></span>

<span data-ttu-id="6a219-121">En el objeto de sección crítica, normalmente realizará una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="6a219-121">For the critical section object, you would typically do one of the following:</span></span>

-   <span data-ttu-id="6a219-122">Derive una clase que herede tanto **CBaseFilter** como **CCritSec**.</span><span class="sxs-lookup"><span data-stu-id="6a219-122">Derive a class that inherits both **CBaseFilter** and **CCritSec**.</span></span> <span data-ttu-id="6a219-123">En el caso de *Plock*, pase el `this` puntero.</span><span class="sxs-lookup"><span data-stu-id="6a219-123">For *pLock*, pass the `this` pointer.</span></span>
-   <span data-ttu-id="6a219-124">Derive una clase que herede **CBaseFilter** y contenga una variable miembro de **CCritSec** .</span><span class="sxs-lookup"><span data-stu-id="6a219-124">Derive a class that inherits **CBaseFilter** and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="6a219-125">En el caso de *Plock*, pase la dirección de esa variable.</span><span class="sxs-lookup"><span data-stu-id="6a219-125">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a219-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a219-126">Requirements</span></span>



| <span data-ttu-id="6a219-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a219-127">Requirement</span></span> | <span data-ttu-id="6a219-128">Value</span><span class="sxs-lookup"><span data-stu-id="6a219-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a219-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6a219-129">Header</span></span><br/>  | <dl> <span data-ttu-id="6a219-130"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6a219-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6a219-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6a219-131">Library</span></span><br/> | <dl> <span data-ttu-id="6a219-132"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="6a219-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a219-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a219-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a219-134">**Clase CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="6a219-134">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




