---
description: Obtenga información sobre el método de constructor CMediaPosition. CMediaPosition (Ctlutil. h). Este método usa los parámetros ' pName ', ' pUnk ' y ' PHR '.
ms.assetid: 4074f513-d1e7-4311-8732-4d755e621e55
title: Constructor CMediaPosition. CMediaPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.CMediaPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb9d86a2403cd0e2e71130b51cdb87bad15c4e95
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105670269"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-phr-parameters"></a><span data-ttu-id="87e5c-104">Constructor CMediaPosition. CMediaPosition (Ctlutil. h): parámetros pName, pUnk, PHR</span><span class="sxs-lookup"><span data-stu-id="87e5c-104">CMediaPosition.CMediaPosition constructor (Ctlutil.h) - pName, pUnk, phr parameters</span></span>

<span data-ttu-id="87e5c-105">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="87e5c-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="87e5c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="87e5c-106">Syntax</span></span>


```C++
CMediaPosition(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="87e5c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="87e5c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87e5c-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="87e5c-108">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="87e5c-109">Puntero al nombre del objeto, para la depuración.</span><span class="sxs-lookup"><span data-stu-id="87e5c-109">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="87e5c-110">Asigne este parámetro en la memoria estática.</span><span class="sxs-lookup"><span data-stu-id="87e5c-110">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="87e5c-111">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="87e5c-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="87e5c-112">Puntero al propietario de este objeto, o **null** si no se agrega el objeto.</span><span class="sxs-lookup"><span data-stu-id="87e5c-112">Pointer to the owner of this object, or **NULL** if the object is not aggregated.</span></span>

</dd> <dt>

<span data-ttu-id="87e5c-113">*phr*</span><span class="sxs-lookup"><span data-stu-id="87e5c-113">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="87e5c-114">Puntero a un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="87e5c-114">Pointer to an **HRESULT** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="87e5c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87e5c-115">Requirements</span></span>

| <span data-ttu-id="87e5c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="87e5c-116">Requirement</span></span> | <span data-ttu-id="87e5c-117">Value</span><span class="sxs-lookup"><span data-stu-id="87e5c-117">Value</span></span> |
|-|-|
| <span data-ttu-id="87e5c-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="87e5c-118">Header</span></span> | <span data-ttu-id="87e5c-119">Ctlutil. h (incluir streams. h)</span><span class="sxs-lookup"><span data-stu-id="87e5c-119">Ctlutil.h (include Streams.h)</span></span> |
| <span data-ttu-id="87e5c-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="87e5c-120">Library</span></span>| <span data-ttu-id="87e5c-121">Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración)</span><span class="sxs-lookup"><span data-stu-id="87e5c-121">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="87e5c-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="87e5c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87e5c-123">**Clase CMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="87e5c-123">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




