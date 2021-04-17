---
description: Método de constructor. El constructor obtiene acceso al punto de conexión especificado.
ms.assetid: 518d41aa-8361-4769-aa9b-14676b676d6f
title: Constructor CAutoUsingOutputPin. CAutoUsingOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoUsingOutputPin.CAutoUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94bafcdcb6e44a07afdccea382d783c20a9ad2ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661133"
---
# <a name="cautousingoutputpincautousingoutputpin-constructor"></a><span data-ttu-id="ed5e0-104">Constructor CAutoUsingOutputPin. CAutoUsingOutputPin</span><span class="sxs-lookup"><span data-stu-id="ed5e0-104">CAutoUsingOutputPin.CAutoUsingOutputPin constructor</span></span>

<span data-ttu-id="ed5e0-105">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="ed5e0-105">Constructor method.</span></span> <span data-ttu-id="ed5e0-106">El constructor obtiene acceso al punto de conexión especificado.</span><span class="sxs-lookup"><span data-stu-id="ed5e0-106">The constructor obtains access to the specified pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed5e0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed5e0-107">Syntax</span></span>


```C++
CAutoUsingOutputPin(
   CDynamicOutputPin *pOutputPin,
   HRESULT           *phr
);
```



## <a name="parameters"></a><span data-ttu-id="ed5e0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ed5e0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed5e0-109">*pOutputPin*</span><span class="sxs-lookup"><span data-stu-id="ed5e0-109">*pOutputPin*</span></span> 
</dt> <dd>

<span data-ttu-id="ed5e0-110">Puntero a un objeto [**CDynamicOutputPin**](cdynamicoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="ed5e0-110">Pointer to a [**CDynamicOutputPin**](cdynamicoutputpin.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="ed5e0-111">*phr*</span><span class="sxs-lookup"><span data-stu-id="ed5e0-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="ed5e0-112">Puntero a una variable que contiene un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ed5e0-112">Pointer to a variable that contains an **HRESULT** value.</span></span> <span data-ttu-id="ed5e0-113">El valor debe ser S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ed5e0-113">The value must be S\_OK.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed5e0-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed5e0-114">Remarks</span></span>

<span data-ttu-id="ed5e0-115">Cuando el método devuelve un resultado, el valor de *\* PHR* indica si el método se ha ejecutado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="ed5e0-115">When the method returns, the value of *\*phr* indicates the success or failure of the method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed5e0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed5e0-116">Requirements</span></span>



| <span data-ttu-id="ed5e0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed5e0-117">Requirement</span></span> | <span data-ttu-id="ed5e0-118">Value</span><span class="sxs-lookup"><span data-stu-id="ed5e0-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed5e0-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed5e0-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ed5e0-120"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ed5e0-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ed5e0-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ed5e0-121">Library</span></span><br/> | <dl> <span data-ttu-id="ed5e0-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ed5e0-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed5e0-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed5e0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed5e0-124">**Clase CAutoUsingOutputPin**</span><span class="sxs-lookup"><span data-stu-id="ed5e0-124">**CAutoUsingOutputPin Class**</span></span>](cautousingoutputpin-cautousingoutputpin.md)
</dt> </dl>

 

 




