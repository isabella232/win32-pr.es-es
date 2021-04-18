---
description: Método de constructor.
ms.assetid: 4dad635f-4637-4f40-9f02-a91b59d05278
title: Constructor CVideoTransformFilter. CVideoTransformFilter (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.CVideoTransformFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63e642182a0f968db5bda06e0af410d02455eb19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680874"
---
# <a name="cvideotransformfiltercvideotransformfilter-constructor"></a><span data-ttu-id="28844-103">Constructor CVideoTransformFilter. CVideoTransformFilter</span><span class="sxs-lookup"><span data-stu-id="28844-103">CVideoTransformFilter.CVideoTransformFilter constructor</span></span>

<span data-ttu-id="28844-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="28844-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="28844-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28844-105">Syntax</span></span>


```C++
CVideoTransformFilter(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="28844-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28844-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28844-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="28844-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="28844-108">Cadena que contiene el nombre de depuración del filtro.</span><span class="sxs-lookup"><span data-stu-id="28844-108">String containing the debug name of the filter.</span></span> <span data-ttu-id="28844-109">Para obtener más información, vea [**CBaseObject:: CBaseObject**](cbaseobject-cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="28844-109">For more information, see [**CBaseObject::CBaseObject**](cbaseobject-cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="28844-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="28844-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="28844-111">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="28844-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="28844-112">Si se agrega el objeto, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="28844-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="28844-113">De lo contrario, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="28844-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="28844-114">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="28844-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="28844-115">Identificador de clase del filtro.</span><span class="sxs-lookup"><span data-stu-id="28844-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="28844-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28844-116">Requirements</span></span>



| <span data-ttu-id="28844-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="28844-117">Requirement</span></span> | <span data-ttu-id="28844-118">Value</span><span class="sxs-lookup"><span data-stu-id="28844-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28844-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28844-119">Header</span></span><br/>  | <dl> <span data-ttu-id="28844-120"><dt>Vtrans. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="28844-120"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="28844-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="28844-121">Library</span></span><br/> | <dl> <span data-ttu-id="28844-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="28844-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28844-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="28844-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28844-124">**Clase CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="28844-124">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




