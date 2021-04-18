---
description: El método FindPin recupera el pin con el identificador especificado.
ms.assetid: d07a298f-ddb0-44eb-85ca-81735875cdf3
title: Método CBaseRenderer. FindPin (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6e6789a91f34d95933ae7869e1588eeb14b6006
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671071"
---
# <a name="cbaserendererfindpin-method"></a><span data-ttu-id="df270-103">CBaseRenderer. FindPin, método</span><span class="sxs-lookup"><span data-stu-id="df270-103">CBaseRenderer.FindPin method</span></span>

<span data-ttu-id="df270-104">El `FindPin` método recupera el pin con el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="df270-104">The `FindPin` method retrieves the pin with the specified identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="df270-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="df270-105">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="df270-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="df270-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df270-107">*Id*</span><span class="sxs-lookup"><span data-stu-id="df270-107">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="df270-108">Puntero a una constante con una cadena de caracteres anchos terminada en null que identifica el PIN.</span><span class="sxs-lookup"><span data-stu-id="df270-108">Pointer to a constant, null-terminated wide-character string that identifies the pin.</span></span> <span data-ttu-id="df270-109">Debe ser L "in".</span><span class="sxs-lookup"><span data-stu-id="df270-109">Must be L"In".</span></span>

</dd> <dt>

<span data-ttu-id="df270-110">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="df270-110">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="df270-111">Dirección de una variable que recibe un puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN.</span><span class="sxs-lookup"><span data-stu-id="df270-111">Address of a variable that receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span> <span data-ttu-id="df270-112">Si se produce un error en el método, *\* ppPin* se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="df270-112">If the method fails, *\*ppPin* is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df270-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="df270-113">Return value</span></span>

<span data-ttu-id="df270-114">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="df270-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="df270-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="df270-115">Return code</span></span>                                                                                       | <span data-ttu-id="df270-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="df270-116">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="df270-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="df270-117"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="df270-118">Correcto.</span><span class="sxs-lookup"><span data-stu-id="df270-118">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="df270-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="df270-119"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="df270-120">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="df270-120">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="df270-121"><dt>**VFW \_ E \_ no \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="df270-121"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="df270-122">Not found.</span><span class="sxs-lookup"><span data-stu-id="df270-122">Not found.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="df270-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="df270-123">Remarks</span></span>

<span data-ttu-id="df270-124">Este método invalida el método [**CBaseFilter:: FindPin**](cbasefilter-findpin.md) .</span><span class="sxs-lookup"><span data-stu-id="df270-124">This method overrides the [**CBaseFilter::FindPin**](cbasefilter-findpin.md) method.</span></span> <span data-ttu-id="df270-125">El PIN del filtro solo (el PIN de entrada) se denomina "in".</span><span class="sxs-lookup"><span data-stu-id="df270-125">The filter's only pin (the input pin) is named "In".</span></span>

## <a name="requirements"></a><span data-ttu-id="df270-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df270-126">Requirements</span></span>



| <span data-ttu-id="df270-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="df270-127">Requirement</span></span> | <span data-ttu-id="df270-128">Value</span><span class="sxs-lookup"><span data-stu-id="df270-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df270-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="df270-129">Header</span></span><br/>  | <dl> <span data-ttu-id="df270-130"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="df270-130"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="df270-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="df270-131">Library</span></span><br/> | <dl> <span data-ttu-id="df270-132"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="df270-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df270-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="df270-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df270-134">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="df270-134">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




