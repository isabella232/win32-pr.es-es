---
description: 'El método FindPin recupera el pin con el identificador especificado. Este método implementa el método IBaseFilter:: FindPin.'
ms.assetid: 152e4ff3-2809-4c57-b9c8-f51fc50b3703
title: Método CBaseFilter. FindPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98b49c547ec59a74185f7f719da660220de8480f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660962"
---
# <a name="cbasefilterfindpin-method"></a><span data-ttu-id="d5940-104">CBaseFilter. FindPin, método</span><span class="sxs-lookup"><span data-stu-id="d5940-104">CBaseFilter.FindPin method</span></span>

<span data-ttu-id="d5940-105">El `FindPin` método recupera el pin con el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="d5940-105">The `FindPin` method retrieves the pin with the specified identifier.</span></span> <span data-ttu-id="d5940-106">Este método implementa el método [**IBaseFilter:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) .</span><span class="sxs-lookup"><span data-stu-id="d5940-106">This method implements the [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5940-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5940-107">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="d5940-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5940-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5940-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="d5940-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="d5940-110">Puntero a una constante de cadena Unicode terminada en null que identifica el PIN.</span><span class="sxs-lookup"><span data-stu-id="d5940-110">Pointer to a constant, null-terminated Unicode string that identifies the pin.</span></span>

</dd> <dt>

<span data-ttu-id="d5940-111">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="d5940-111">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="d5940-112">Dirección de una variable que recibe un puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN.</span><span class="sxs-lookup"><span data-stu-id="d5940-112">Address of a variable that receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5940-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5940-113">Return value</span></span>

<span data-ttu-id="d5940-114">Devuelve uno de los siguientes valores **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d5940-114">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="d5940-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d5940-115">Return code</span></span>                                                                                       | <span data-ttu-id="d5940-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5940-116">Description</span></span>                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="d5940-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="d5940-117"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="d5940-118">Correcto.</span><span class="sxs-lookup"><span data-stu-id="d5940-118">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="d5940-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="d5940-119"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="d5940-120">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="d5940-120">**NULL** pointer argument.</span></span><br/>     |
| <dl> <span data-ttu-id="d5940-121"><dt>**VFW \_ E \_ no \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="d5940-121"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="d5940-122">No se encontró ningún PIN coincidente.</span><span class="sxs-lookup"><span data-stu-id="d5940-122">Could not find a matching pin.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d5940-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5940-123">Remarks</span></span>

<span data-ttu-id="d5940-124">Este método llama al método [**CBasePin:: Name**](cbasepin-name.md) para comparar el nombre de cada pin con la cadena especificada por el parámetro *ID* .</span><span class="sxs-lookup"><span data-stu-id="d5940-124">This method calls the [**CBasePin::Name**](cbasepin-name.md) method to compare each pin's name against the string specified by the *Id* parameter.</span></span>

<span data-ttu-id="d5940-125">Si el método se ejecuta correctamente, la interfaz **IPin** tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="d5940-125">If the method succeeds, the **IPin** interface has an outstanding reference count.</span></span> <span data-ttu-id="d5940-126">Asegúrese de liberarlo cuando haya terminado.</span><span class="sxs-lookup"><span data-stu-id="d5940-126">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5940-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5940-127">Requirements</span></span>



| <span data-ttu-id="d5940-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5940-128">Requirement</span></span> | <span data-ttu-id="d5940-129">Value</span><span class="sxs-lookup"><span data-stu-id="d5940-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5940-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5940-130">Header</span></span><br/>  | <dl> <span data-ttu-id="d5940-131"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5940-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d5940-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d5940-132">Library</span></span><br/> | <dl> <span data-ttu-id="d5940-133"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d5940-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5940-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5940-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5940-135">**Clase CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="d5940-135">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




