---
description: 'Constructor CVideoTransformFilter.CVideoTransformFilter: método constructor.'
ms.assetid: 4dad635f-4637-4f40-9f02-a91b59d05278
title: Constructor CVideoTransformFilter.CVideoTransformFilter (Vtrans.h)
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
ms.openlocfilehash: 59609e09b252e56aded1669264bb98cdbe823e89
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084593"
---
# <a name="cvideotransformfiltercvideotransformfilter-constructor"></a><span data-ttu-id="b1416-103">Constructor CVideoTransformFilter.CVideoTransformFilter</span><span class="sxs-lookup"><span data-stu-id="b1416-103">CVideoTransformFilter.CVideoTransformFilter constructor</span></span>

<span data-ttu-id="b1416-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="b1416-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1416-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1416-105">Syntax</span></span>


```C++
CVideoTransformFilter(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="b1416-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b1416-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1416-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="b1416-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="b1416-108">Cadena que contiene el nombre de depuración del filtro.</span><span class="sxs-lookup"><span data-stu-id="b1416-108">String containing the debug name of the filter.</span></span> <span data-ttu-id="b1416-109">Para obtener más información, [**vea CBaseObject::CBaseObject**](cbaseobject-cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="b1416-109">For more information, see [**CBaseObject::CBaseObject**](cbaseobject-cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1416-110">*Punk*</span><span class="sxs-lookup"><span data-stu-id="b1416-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="b1416-111">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="b1416-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="b1416-112">Si el objeto se agrega, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="b1416-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="b1416-113">De lo contrario, establezca este parámetro en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="b1416-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b1416-114">*Clsid*</span><span class="sxs-lookup"><span data-stu-id="b1416-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="b1416-115">Identificador de clase del filtro.</span><span class="sxs-lookup"><span data-stu-id="b1416-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1416-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1416-116">Requirements</span></span>



| <span data-ttu-id="b1416-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1416-117">Requirement</span></span> | <span data-ttu-id="b1416-118">Value</span><span class="sxs-lookup"><span data-stu-id="b1416-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1416-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b1416-119">Header</span></span><br/>  | <dl> <span data-ttu-id="b1416-120"><dt>Vtrans.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="b1416-120"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b1416-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b1416-121">Library</span></span><br/> | <dl> <span data-ttu-id="b1416-122"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b1416-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1416-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b1416-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1416-124">**CVideoTransformFilter (clase)**</span><span class="sxs-lookup"><span data-stu-id="b1416-124">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




