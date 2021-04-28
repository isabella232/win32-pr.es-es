---
description: 'Constructor CTransInPlaceFilter.CTransInPlaceFilter: método constructor.'
ms.assetid: f0d30125-5d16-470c-a5fb-a7df96814dad
title: Constructor CTransInPlaceFilter.CTransInPlaceFilter (Transip.h)
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
ms.openlocfilehash: d6b14af4b0d1f33933db8ca2fd1835e9711edad9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084783"
---
# <a name="ctransinplacefilterctransinplacefilter-constructor"></a><span data-ttu-id="4ddde-103">Constructor CTransInPlaceFilter.CTransInPlaceFilter</span><span class="sxs-lookup"><span data-stu-id="4ddde-103">CTransInPlaceFilter.CTransInPlaceFilter constructor</span></span>

<span data-ttu-id="4ddde-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="4ddde-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ddde-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ddde-105">Syntax</span></span>


```C++
CTransInPlaceFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   REFCLSID  clsid,
   HRESULT   *phr,
   bool      bModifiesData = TRUE
);
```



## <a name="parameters"></a><span data-ttu-id="4ddde-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4ddde-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ddde-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="4ddde-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="4ddde-108">Cadena que contiene el nombre de depuración del filtro.</span><span class="sxs-lookup"><span data-stu-id="4ddde-108">String containing the debug name of the filter.</span></span> <span data-ttu-id="4ddde-109">Para obtener más información, vea [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="4ddde-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ddde-110">*lpUnk*</span><span class="sxs-lookup"><span data-stu-id="4ddde-110">*lpUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="4ddde-111">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="4ddde-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="4ddde-112">Si el objeto se agrega, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="4ddde-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="4ddde-113">De lo contrario, establezca este parámetro en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="4ddde-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4ddde-114">*Clsid*</span><span class="sxs-lookup"><span data-stu-id="4ddde-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="4ddde-115">Identificador de clase del filtro.</span><span class="sxs-lookup"><span data-stu-id="4ddde-115">Class identifier of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="4ddde-116">*Phr*</span><span class="sxs-lookup"><span data-stu-id="4ddde-116">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="4ddde-117">ignorado.</span><span class="sxs-lookup"><span data-stu-id="4ddde-117">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="4ddde-118">*bModifiesData*</span><span class="sxs-lookup"><span data-stu-id="4ddde-118">*bModifiesData*</span></span> 
</dt> <dd>

<span data-ttu-id="4ddde-119">Valor booleano que especifica si el filtro modifica los datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="4ddde-119">Boolean value that specifies whether the filter modifies the input data.</span></span> <span data-ttu-id="4ddde-120">Si **es TRUE,** el filtro modifica los datos.</span><span class="sxs-lookup"><span data-stu-id="4ddde-120">If **TRUE**, the filter modifies the data.</span></span> <span data-ttu-id="4ddde-121">De lo contrario, el filtro pasa los datos de bajada sin cambios.</span><span class="sxs-lookup"><span data-stu-id="4ddde-121">Otherwise, the filter passes the data downstream unchanged.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4ddde-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ddde-122">Requirements</span></span>



| <span data-ttu-id="4ddde-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ddde-123">Requirement</span></span> | <span data-ttu-id="4ddde-124">Value</span><span class="sxs-lookup"><span data-stu-id="4ddde-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ddde-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4ddde-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4ddde-126"><dt>Transip.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ddde-126"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4ddde-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4ddde-127">Library</span></span><br/> | <dl> <span data-ttu-id="4ddde-128"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="4ddde-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ddde-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4ddde-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ddde-130">**CTransInPlaceFilter (clase)**</span><span class="sxs-lookup"><span data-stu-id="4ddde-130">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




