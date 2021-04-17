---
description: Método de constructor.
ms.assetid: 91290f58-a77b-447f-aa2a-bbee067f5a98
title: Constructor CBaseMediaFilter. CBaseMediaFilter (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.CBaseMediaFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8498e9da88804291fc5cdb900ff1dbda212e8b0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670585"
---
# <a name="cbasemediafiltercbasemediafilter-constructor"></a><span data-ttu-id="e863c-103">Constructor CBaseMediaFilter. CBaseMediaFilter</span><span class="sxs-lookup"><span data-stu-id="e863c-103">CBaseMediaFilter.CBaseMediaFilter constructor</span></span>

<span data-ttu-id="e863c-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="e863c-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e863c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e863c-105">Syntax</span></span>


```C++
CBaseMediaFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="e863c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e863c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e863c-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="e863c-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="e863c-108">Puntero a una cadena que contiene el nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="e863c-108">Pointer to a string containing the name of the object.</span></span>

</dd> <dt>

<span data-ttu-id="e863c-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="e863c-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="e863c-110">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="e863c-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="e863c-111">Si se agrega el objeto, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="e863c-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="e863c-112">De lo contrario, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="e863c-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e863c-113">*pLock*</span><span class="sxs-lookup"><span data-stu-id="e863c-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="e863c-114">Puntero a un bloqueo de [**CCritSec**](ccritsec.md) , que se usa para serializar los cambios de estado.</span><span class="sxs-lookup"><span data-stu-id="e863c-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="e863c-115">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="e863c-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="e863c-116">Identificador de clase del objeto.</span><span class="sxs-lookup"><span data-stu-id="e863c-116">Class identifier of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e863c-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e863c-117">Remarks</span></span>

<span data-ttu-id="e863c-118">Si otro objeto contiene o agrega el `CBaseMediaFilter` objeto, el bloqueo **CCritSec** podría ser externo al `CBaseMediaFilter` objeto.</span><span class="sxs-lookup"><span data-stu-id="e863c-118">If another object contains or aggregates the `CBaseMediaFilter` object, the **CCritSec** lock might be external to the `CBaseMediaFilter` object.</span></span> <span data-ttu-id="e863c-119">En ese caso, pase un puntero al bloqueo en *Plock*.</span><span class="sxs-lookup"><span data-stu-id="e863c-119">In that case, pass a pointer to the lock in *pLock*.</span></span>

<span data-ttu-id="e863c-120">De lo contrario, puede:</span><span class="sxs-lookup"><span data-stu-id="e863c-120">Otherwise, you can:</span></span>

-   <span data-ttu-id="e863c-121">Derive una clase que herede `CBaseMediaFilter` y **CCritSec**.</span><span class="sxs-lookup"><span data-stu-id="e863c-121">Derive a class that inherits both `CBaseMediaFilter` and **CCritSec**.</span></span> <span data-ttu-id="e863c-122">En el caso de *Plock*, pase el puntero this.</span><span class="sxs-lookup"><span data-stu-id="e863c-122">For *pLock*, pass the this pointer.</span></span>
-   <span data-ttu-id="e863c-123">Derive una clase que herede `CBaseMediaFilter` y contenga una variable miembro **CCritSec** .</span><span class="sxs-lookup"><span data-stu-id="e863c-123">Derive a class that inherits `CBaseMediaFilter` and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="e863c-124">En el caso de *Plock*, pase la dirección de esa variable.</span><span class="sxs-lookup"><span data-stu-id="e863c-124">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="e863c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e863c-125">Requirements</span></span>



| <span data-ttu-id="e863c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e863c-126">Requirement</span></span> | <span data-ttu-id="e863c-127">Value</span><span class="sxs-lookup"><span data-stu-id="e863c-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e863c-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e863c-128">Header</span></span><br/>  | <dl> <span data-ttu-id="e863c-129"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e863c-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e863c-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e863c-130">Library</span></span><br/> | <dl> <span data-ttu-id="e863c-131"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e863c-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e863c-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="e863c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e863c-133">**Clase CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="e863c-133">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




