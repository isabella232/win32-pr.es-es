---
description: Método de constructor.
ms.assetid: f0d30125-5d16-470c-a5fb-a7df96814dad
title: Constructor CTransInPlaceFilter. CTransInPlaceFilter (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CTransInPlaceFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 091ea6e6a52d4cc9221ddb29db34b4823111a395
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661259"
---
# <a name="ctransinplacefilterctransinplacefilter-constructor"></a><span data-ttu-id="685e5-103">Constructor CTransInPlaceFilter. CTransInPlaceFilter</span><span class="sxs-lookup"><span data-stu-id="685e5-103">CTransInPlaceFilter.CTransInPlaceFilter constructor</span></span>

<span data-ttu-id="685e5-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="685e5-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="685e5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="685e5-105">Syntax</span></span>


```C++
CTransInPlaceFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   REFCLSID  clsid,
   HRESULT   *phr,
   bool      bModifiesData = TRUE
);
```



## <a name="parameters"></a><span data-ttu-id="685e5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="685e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="685e5-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="685e5-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="685e5-108">Cadena que contiene el nombre de depuración del filtro.</span><span class="sxs-lookup"><span data-stu-id="685e5-108">String containing the debug name of the filter.</span></span> <span data-ttu-id="685e5-109">Para obtener más información, vea [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="685e5-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="685e5-110">*lpUnk*</span><span class="sxs-lookup"><span data-stu-id="685e5-110">*lpUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="685e5-111">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="685e5-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="685e5-112">Si se agrega el objeto, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="685e5-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="685e5-113">De lo contrario, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="685e5-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="685e5-114">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="685e5-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="685e5-115">Identificador de clase del filtro.</span><span class="sxs-lookup"><span data-stu-id="685e5-115">Class identifier of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="685e5-116">*phr*</span><span class="sxs-lookup"><span data-stu-id="685e5-116">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="685e5-117">ignorado.</span><span class="sxs-lookup"><span data-stu-id="685e5-117">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="685e5-118">*bModifiesData*</span><span class="sxs-lookup"><span data-stu-id="685e5-118">*bModifiesData*</span></span> 
</dt> <dd>

<span data-ttu-id="685e5-119">Valor booleano que especifica si el filtro modifica los datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="685e5-119">Boolean value that specifies whether the filter modifies the input data.</span></span> <span data-ttu-id="685e5-120">Si **es true**, el filtro modifica los datos.</span><span class="sxs-lookup"><span data-stu-id="685e5-120">If **TRUE**, the filter modifies the data.</span></span> <span data-ttu-id="685e5-121">De lo contrario, el filtro pasa los datos de nivel inferior sin cambios.</span><span class="sxs-lookup"><span data-stu-id="685e5-121">Otherwise, the filter passes the data downstream unchanged.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="685e5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="685e5-122">Requirements</span></span>



| <span data-ttu-id="685e5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="685e5-123">Requirement</span></span> | <span data-ttu-id="685e5-124">Value</span><span class="sxs-lookup"><span data-stu-id="685e5-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="685e5-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="685e5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="685e5-126"><dt>TRANSip. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="685e5-126"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="685e5-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="685e5-127">Library</span></span><br/> | <dl> <span data-ttu-id="685e5-128"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="685e5-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="685e5-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="685e5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="685e5-130">**Clase CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="685e5-130">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




