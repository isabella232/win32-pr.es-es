---
description: 'Constructor CBaseMediaFilter.CBaseMediaFilter: método constructor.'
ms.assetid: 91290f58-a77b-447f-aa2a-bbee067f5a98
title: Constructor CBaseMediaFilter.CBaseMediaFilter (Amfilter.h)
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
ms.openlocfilehash: f123c7af29c6420de6004132180eba8dbf33fa72
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096332"
---
# <a name="cbasemediafiltercbasemediafilter-constructor"></a><span data-ttu-id="46aff-103">Constructor CBaseMediaFilter.CBaseMediaFilter</span><span class="sxs-lookup"><span data-stu-id="46aff-103">CBaseMediaFilter.CBaseMediaFilter constructor</span></span>

<span data-ttu-id="46aff-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="46aff-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="46aff-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46aff-105">Syntax</span></span>


```C++
CBaseMediaFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="46aff-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46aff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46aff-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="46aff-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="46aff-108">Puntero a una cadena que contiene el nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="46aff-108">Pointer to a string containing the name of the object.</span></span>

</dd> <dt>

<span data-ttu-id="46aff-109">*Punk*</span><span class="sxs-lookup"><span data-stu-id="46aff-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="46aff-110">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="46aff-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="46aff-111">Si el objeto se agrega, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="46aff-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="46aff-112">De lo contrario, establezca este parámetro en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="46aff-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="46aff-113">*Plock*</span><span class="sxs-lookup"><span data-stu-id="46aff-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="46aff-114">Puntero a un [**bloqueo CCritSec,**](ccritsec.md) que se usa para serializar los cambios de estado.</span><span class="sxs-lookup"><span data-stu-id="46aff-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="46aff-115">*Clsid*</span><span class="sxs-lookup"><span data-stu-id="46aff-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="46aff-116">Identificador de clase del objeto.</span><span class="sxs-lookup"><span data-stu-id="46aff-116">Class identifier of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46aff-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="46aff-117">Remarks</span></span>

<span data-ttu-id="46aff-118">Si otro objeto contiene o agrega el `CBaseMediaFilter` objeto, el **bloqueo CCritSec** podría ser externo al `CBaseMediaFilter` objeto .</span><span class="sxs-lookup"><span data-stu-id="46aff-118">If another object contains or aggregates the `CBaseMediaFilter` object, the **CCritSec** lock might be external to the `CBaseMediaFilter` object.</span></span> <span data-ttu-id="46aff-119">En ese caso, pase un puntero al bloqueo en *pLock*.</span><span class="sxs-lookup"><span data-stu-id="46aff-119">In that case, pass a pointer to the lock in *pLock*.</span></span>

<span data-ttu-id="46aff-120">De lo contrario, puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="46aff-120">Otherwise, you can:</span></span>

-   <span data-ttu-id="46aff-121">Derive una clase que hereda y `CBaseMediaFilter` **CCritSec**.</span><span class="sxs-lookup"><span data-stu-id="46aff-121">Derive a class that inherits both `CBaseMediaFilter` and **CCritSec**.</span></span> <span data-ttu-id="46aff-122">Para *pLock*, pase el puntero this.</span><span class="sxs-lookup"><span data-stu-id="46aff-122">For *pLock*, pass the this pointer.</span></span>
-   <span data-ttu-id="46aff-123">Derive una clase que hereda `CBaseMediaFilter` y contiene una variable miembro **CCritSec.**</span><span class="sxs-lookup"><span data-stu-id="46aff-123">Derive a class that inherits `CBaseMediaFilter` and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="46aff-124">Para *pLock*, pase la dirección de esa variable.</span><span class="sxs-lookup"><span data-stu-id="46aff-124">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="46aff-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46aff-125">Requirements</span></span>



| <span data-ttu-id="46aff-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="46aff-126">Requirement</span></span> | <span data-ttu-id="46aff-127">Value</span><span class="sxs-lookup"><span data-stu-id="46aff-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46aff-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="46aff-128">Header</span></span><br/>  | <dl> <span data-ttu-id="46aff-129"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="46aff-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="46aff-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="46aff-130">Library</span></span><br/> | <dl> <span data-ttu-id="46aff-131"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="46aff-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46aff-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="46aff-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46aff-133">**CBaseMediaFilter (clase)**</span><span class="sxs-lookup"><span data-stu-id="46aff-133">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




