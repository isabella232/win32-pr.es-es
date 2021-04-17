---
description: Método de constructor.
ms.assetid: b6433ec9-6710-4c2f-968f-00e0d9f8c7a5
title: Constructor CBaseFilter. CBaseFilter (const TCHAR *, LPUNKNOWN, CCritSec*, REFCLSID) (Amfilter. h)
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
ms.openlocfilehash: 40ac48a1fd28b9b50a8f1fa9c698ea5db49d97b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660205"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-constructor"></a><span data-ttu-id="4ee83-103">Constructor CBaseFilter. CBaseFilter (const TCHAR \* , LPUNKNOWN, CCritSec \* , REFCLSID)</span><span class="sxs-lookup"><span data-stu-id="4ee83-103">CBaseFilter.CBaseFilter(const TCHAR\*, LPUNKNOWN, CCritSec\*, REFCLSID) constructor</span></span>

<span data-ttu-id="4ee83-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="4ee83-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ee83-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ee83-105">Syntax</span></span>


```C++
CBaseFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="4ee83-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4ee83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ee83-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="4ee83-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="4ee83-108">Puntero a una cadena que contiene el nombre del filtro, con fines de depuración.</span><span class="sxs-lookup"><span data-stu-id="4ee83-108">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="4ee83-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="4ee83-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="4ee83-110">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="4ee83-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="4ee83-111">Si se agrega el objeto, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="4ee83-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="4ee83-112">De lo contrario, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="4ee83-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4ee83-113">*pLock*</span><span class="sxs-lookup"><span data-stu-id="4ee83-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="4ee83-114">Puntero a un bloqueo de [**CCritSec**](ccritsec.md) , que se usa para serializar los cambios de estado.</span><span class="sxs-lookup"><span data-stu-id="4ee83-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="4ee83-115">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="4ee83-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="4ee83-116">Identificador de clase (CLSID) del filtro.</span><span class="sxs-lookup"><span data-stu-id="4ee83-116">Class identifier (CLSID) of the filter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ee83-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4ee83-117">Remarks</span></span>

<span data-ttu-id="4ee83-118">En el objeto de sección crítica, normalmente realizará una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="4ee83-118">For the critical section object, you would typically do one of the following:</span></span>

-   <span data-ttu-id="4ee83-119">Derive una clase que herede tanto **CBaseFilter** como **CCritSec**.</span><span class="sxs-lookup"><span data-stu-id="4ee83-119">Derive a class that inherits both **CBaseFilter** and **CCritSec**.</span></span> <span data-ttu-id="4ee83-120">En el caso de *Plock*, pase el `this` puntero.</span><span class="sxs-lookup"><span data-stu-id="4ee83-120">For *pLock*, pass the `this` pointer.</span></span>
-   <span data-ttu-id="4ee83-121">Derive una clase que herede **CBaseFilter** y contenga una variable miembro de **CCritSec** .</span><span class="sxs-lookup"><span data-stu-id="4ee83-121">Derive a class that inherits **CBaseFilter** and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="4ee83-122">En el caso de *Plock*, pase la dirección de esa variable.</span><span class="sxs-lookup"><span data-stu-id="4ee83-122">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ee83-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ee83-123">Requirements</span></span>



| <span data-ttu-id="4ee83-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ee83-124">Requirement</span></span> | <span data-ttu-id="4ee83-125">Value</span><span class="sxs-lookup"><span data-stu-id="4ee83-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ee83-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4ee83-126">Header</span></span><br/>  | <dl> <span data-ttu-id="4ee83-127"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ee83-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4ee83-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4ee83-128">Library</span></span><br/> | <dl> <span data-ttu-id="4ee83-129"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="4ee83-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ee83-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ee83-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ee83-131">**Clase CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="4ee83-131">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




