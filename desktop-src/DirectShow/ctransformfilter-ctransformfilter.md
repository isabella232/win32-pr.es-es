---
description: 'Constructor CTransformFilter.CTransformFilter: método constructor.'
ms.assetid: a64c3e29-91f2-455f-aac1-1e4ecce6958d
title: Constructor CTransformFilter.CTransformFilter (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CTransformFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fce67bbe22361bdbae0cd3e51768e0cf0743d97d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098723"
---
# <a name="ctransformfilterctransformfilter-constructor"></a><span data-ttu-id="9d567-103">Constructor CTransformFilter.CTransformFilter</span><span class="sxs-lookup"><span data-stu-id="9d567-103">CTransformFilter.CTransformFilter constructor</span></span>

<span data-ttu-id="9d567-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="9d567-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d567-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9d567-105">Syntax</span></span>


```C++
CTransformFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   CLSID     clsid
);
```



## <a name="parameters"></a><span data-ttu-id="9d567-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9d567-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d567-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="9d567-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="9d567-108">Cadena que contiene el nombre de depuración del filtro.</span><span class="sxs-lookup"><span data-stu-id="9d567-108">String containing the debug name of the filter.</span></span> <span data-ttu-id="9d567-109">Para obtener más información, vea [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="9d567-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="9d567-110">*lpUnk*</span><span class="sxs-lookup"><span data-stu-id="9d567-110">*lpUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="9d567-111">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="9d567-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="9d567-112">Si el objeto se agrega, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="9d567-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="9d567-113">De lo contrario, establezca este parámetro en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="9d567-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9d567-114">*Clsid*</span><span class="sxs-lookup"><span data-stu-id="9d567-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="9d567-115">Identificador de clase del filtro.</span><span class="sxs-lookup"><span data-stu-id="9d567-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9d567-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9d567-116">Remarks</span></span>

<span data-ttu-id="9d567-117">El constructor no crea los pines del filtro.</span><span class="sxs-lookup"><span data-stu-id="9d567-117">The constructor does not create the filter's pins.</span></span> <span data-ttu-id="9d567-118">Esto sucede durante la primera llamada al [**método GetPin.**](ctransformfilter-getpin.md)</span><span class="sxs-lookup"><span data-stu-id="9d567-118">That happens during the first call to the [**GetPin**](ctransformfilter-getpin.md) method.</span></span> <span data-ttu-id="9d567-119">El constructor inicializa las variables [**miembro m \_ pInput**](ctransformfilter-m-pinput.md) y [**m \_ pOutput**](ctransformfilter-m-poutput.md) en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="9d567-119">The constructor initializes the [**m\_pInput**](ctransformfilter-m-pinput.md) and [**m\_pOutput**](ctransformfilter-m-poutput.md) member variables to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d567-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d567-120">Requirements</span></span>



| <span data-ttu-id="9d567-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d567-121">Requirement</span></span> | <span data-ttu-id="9d567-122">Value</span><span class="sxs-lookup"><span data-stu-id="9d567-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d567-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9d567-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9d567-124"><dt>Transfrm.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d567-124"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9d567-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9d567-125">Library</span></span><br/> | <dl> <span data-ttu-id="9d567-126"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9d567-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d567-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9d567-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d567-128">**CTransformFilter (clase)**</span><span class="sxs-lookup"><span data-stu-id="9d567-128">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




