---
description: 'Constructor CBaseFilter.CBaseFilter(const \* TCHAR, LNOWN, CCritSec \* , REFCLSID): método constructor.'
ms.assetid: b6433ec9-6710-4c2f-968f-00e0d9f8c7a5
title: Constructor CBaseFilter.CBaseFilter(const *TCHAR, LNOWN, CCritSec*, REFCLSID) (Amfilter.h)
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
ms.openlocfilehash: b621bdb3f6a15ae950959a65eba8841bde399b81
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099833"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-constructor"></a><span data-ttu-id="95244-103">Constructor CBaseFilter.CBaseFilter(const \* TCHAR, LNOWN, CCritSec \* , REFCLSID)</span><span class="sxs-lookup"><span data-stu-id="95244-103">CBaseFilter.CBaseFilter(const TCHAR\*, LPUNKNOWN, CCritSec\*, REFCLSID) constructor</span></span>

<span data-ttu-id="95244-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="95244-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="95244-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95244-105">Syntax</span></span>


```C++
CBaseFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="95244-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="95244-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95244-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="95244-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="95244-108">Puntero a una cadena que contiene el nombre del filtro, con fines de depuración.</span><span class="sxs-lookup"><span data-stu-id="95244-108">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="95244-109">*Punk*</span><span class="sxs-lookup"><span data-stu-id="95244-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="95244-110">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="95244-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="95244-111">Si el objeto se agrega, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="95244-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="95244-112">De lo contrario, establezca este parámetro en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="95244-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="95244-113">*Plock*</span><span class="sxs-lookup"><span data-stu-id="95244-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="95244-114">Puntero a un [**bloqueo CCritSec,**](ccritsec.md) que se usa para serializar los cambios de estado.</span><span class="sxs-lookup"><span data-stu-id="95244-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="95244-115">*Clsid*</span><span class="sxs-lookup"><span data-stu-id="95244-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="95244-116">Identificador de clase (CLSID) del filtro.</span><span class="sxs-lookup"><span data-stu-id="95244-116">Class identifier (CLSID) of the filter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95244-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="95244-117">Remarks</span></span>

<span data-ttu-id="95244-118">Para el objeto de sección crítica, normalmente haría una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="95244-118">For the critical section object, you would typically do one of the following:</span></span>

-   <span data-ttu-id="95244-119">Derive una clase que herede **tanto CBaseFilter** como **CCritSec.**</span><span class="sxs-lookup"><span data-stu-id="95244-119">Derive a class that inherits both **CBaseFilter** and **CCritSec**.</span></span> <span data-ttu-id="95244-120">Para *pLock*, pase el `this` puntero.</span><span class="sxs-lookup"><span data-stu-id="95244-120">For *pLock*, pass the `this` pointer.</span></span>
-   <span data-ttu-id="95244-121">Derive una clase que hereda **CBaseFilter** y contiene una variable **miembro CCritSec.**</span><span class="sxs-lookup"><span data-stu-id="95244-121">Derive a class that inherits **CBaseFilter** and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="95244-122">Para *pLock*, pase la dirección de esa variable.</span><span class="sxs-lookup"><span data-stu-id="95244-122">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="95244-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95244-123">Requirements</span></span>



| <span data-ttu-id="95244-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="95244-124">Requirement</span></span> | <span data-ttu-id="95244-125">Value</span><span class="sxs-lookup"><span data-stu-id="95244-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95244-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="95244-126">Header</span></span><br/>  | <dl> <span data-ttu-id="95244-127"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="95244-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="95244-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="95244-128">Library</span></span><br/> | <dl> <span data-ttu-id="95244-129"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="95244-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95244-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="95244-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95244-131">**CBaseFilter (clase)**</span><span class="sxs-lookup"><span data-stu-id="95244-131">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




