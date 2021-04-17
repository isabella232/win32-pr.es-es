---
description: Obtenga información sobre el método de constructor CMediaPosition. CMediaPosition (Ctlutil. h). Este método usa los parámetros ' pName ' y ' pUnk '.
ms.assetid: 18a7785c-30c6-43b8-9a41-542a8424522c
title: Constructor CMediaPosition. CMediaPosition (Ctlutil. h)-pName, parámetros pUnk
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
ms.openlocfilehash: e65f034e5f8857b21bc706bce45aa74c3c3cf966
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105670271"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-parameters"></a><span data-ttu-id="fa8ce-104">Constructor CMediaPosition. CMediaPosition (Ctlutil. h)-pName, parámetros pUnk</span><span class="sxs-lookup"><span data-stu-id="fa8ce-104">CMediaPosition.CMediaPosition constructor (Ctlutil.h) - pName, pUnk parameters</span></span>

<span data-ttu-id="fa8ce-105">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="fa8ce-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa8ce-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fa8ce-106">Syntax</span></span>


```C++
CMediaPosition(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="fa8ce-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fa8ce-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa8ce-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="fa8ce-108">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="fa8ce-109">Puntero al nombre del objeto, para la depuración.</span><span class="sxs-lookup"><span data-stu-id="fa8ce-109">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="fa8ce-110">Asigne este parámetro en la memoria estática.</span><span class="sxs-lookup"><span data-stu-id="fa8ce-110">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="fa8ce-111">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="fa8ce-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="fa8ce-112">Puntero al propietario de este objeto, o **null** si no se agrega el objeto.</span><span class="sxs-lookup"><span data-stu-id="fa8ce-112">Pointer to the owner of this object, or **NULL** if the object is not aggregated.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa8ce-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa8ce-113">Requirements</span></span>

| <span data-ttu-id="fa8ce-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa8ce-114">Requirement</span></span> | <span data-ttu-id="fa8ce-115">Value</span><span class="sxs-lookup"><span data-stu-id="fa8ce-115">Value</span></span> |
|-|-|
| <span data-ttu-id="fa8ce-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fa8ce-116">Header</span></span> | <span data-ttu-id="fa8ce-117">Ctlutil. h (incluir streams. h)</span><span class="sxs-lookup"><span data-stu-id="fa8ce-117">Ctlutil.h (include Streams.h)</span></span> |
| <span data-ttu-id="fa8ce-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fa8ce-118">Library</span></span>| <span data-ttu-id="fa8ce-119">Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración)</span><span class="sxs-lookup"><span data-stu-id="fa8ce-119">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="fa8ce-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa8ce-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa8ce-121">**Clase CMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="fa8ce-121">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




