---
description: Método de constructor.
ms.assetid: a64c3e29-91f2-455f-aac1-1e4ecce6958d
title: Constructor CTransformFilter. CTransformFilter (Transfrm. h)
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
ms.openlocfilehash: 39569dff69c2ab1ebb635cb69a4c71602a7400d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660729"
---
# <a name="ctransformfilterctransformfilter-constructor"></a><span data-ttu-id="94f31-103">Constructor CTransformFilter. CTransformFilter</span><span class="sxs-lookup"><span data-stu-id="94f31-103">CTransformFilter.CTransformFilter constructor</span></span>

<span data-ttu-id="94f31-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="94f31-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="94f31-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94f31-105">Syntax</span></span>


```C++
CTransformFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   CLSID     clsid
);
```



## <a name="parameters"></a><span data-ttu-id="94f31-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="94f31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94f31-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="94f31-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="94f31-108">Cadena que contiene el nombre de depuración del filtro.</span><span class="sxs-lookup"><span data-stu-id="94f31-108">String containing the debug name of the filter.</span></span> <span data-ttu-id="94f31-109">Para obtener más información, vea [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="94f31-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="94f31-110">*lpUnk*</span><span class="sxs-lookup"><span data-stu-id="94f31-110">*lpUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="94f31-111">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="94f31-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="94f31-112">Si se agrega el objeto, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="94f31-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="94f31-113">De lo contrario, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="94f31-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="94f31-114">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="94f31-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="94f31-115">Identificador de clase del filtro.</span><span class="sxs-lookup"><span data-stu-id="94f31-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94f31-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94f31-116">Remarks</span></span>

<span data-ttu-id="94f31-117">El constructor no crea los PIN del filtro.</span><span class="sxs-lookup"><span data-stu-id="94f31-117">The constructor does not create the filter's pins.</span></span> <span data-ttu-id="94f31-118">Esto sucede durante la primera llamada al método [**GetPin**](ctransformfilter-getpin.md) .</span><span class="sxs-lookup"><span data-stu-id="94f31-118">That happens during the first call to the [**GetPin**](ctransformfilter-getpin.md) method.</span></span> <span data-ttu-id="94f31-119">El constructor inicializa las variables de miembro [**m \_ pInput**](ctransformfilter-m-pinput.md) y [**m \_ pOutput**](ctransformfilter-m-poutput.md) en **null**.</span><span class="sxs-lookup"><span data-stu-id="94f31-119">The constructor initializes the [**m\_pInput**](ctransformfilter-m-pinput.md) and [**m\_pOutput**](ctransformfilter-m-poutput.md) member variables to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="94f31-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94f31-120">Requirements</span></span>



| <span data-ttu-id="94f31-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="94f31-121">Requirement</span></span> | <span data-ttu-id="94f31-122">Value</span><span class="sxs-lookup"><span data-stu-id="94f31-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94f31-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="94f31-123">Header</span></span><br/>  | <dl> <span data-ttu-id="94f31-124"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94f31-124"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="94f31-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="94f31-125">Library</span></span><br/> | <dl> <span data-ttu-id="94f31-126"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="94f31-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94f31-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="94f31-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94f31-128">**Clase CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="94f31-128">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




