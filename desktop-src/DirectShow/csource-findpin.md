---
description: 'El método FindPin recupera el pin con el identificador especificado. Este método implementa el método IBaseFilter:: FindPin.'
ms.assetid: ad593dbf-ca56-4409-ac6e-1b88908c8cee
title: CSource. FindPin (método) (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fac8df1e53e4a129b42d1284a19392bc7b58aa2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670399"
---
# <a name="csourcefindpin-method"></a><span data-ttu-id="e0f06-104">CSource. FindPin, método</span><span class="sxs-lookup"><span data-stu-id="e0f06-104">CSource.FindPin method</span></span>

<span data-ttu-id="e0f06-105">El `FindPin` método recupera el pin con el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="e0f06-105">The `FindPin` method retrieves the pin with the specified identifier.</span></span> <span data-ttu-id="e0f06-106">Este método implementa el método [**IBaseFilter:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) .</span><span class="sxs-lookup"><span data-stu-id="e0f06-106">This method implements the [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0f06-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0f06-107">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="e0f06-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e0f06-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0f06-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="e0f06-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="e0f06-110">Puntero a una cadena terminada en null que identifica el PIN.</span><span class="sxs-lookup"><span data-stu-id="e0f06-110">Pointer to a null-terminated string that identifies the pin.</span></span>

</dd> <dt>

<span data-ttu-id="e0f06-111">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="e0f06-111">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="e0f06-112">Recibe un puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN.</span><span class="sxs-lookup"><span data-stu-id="e0f06-112">Receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span> <span data-ttu-id="e0f06-113">Si se produce un error en el método, \* *ppPin* se establece en **null** .</span><span class="sxs-lookup"><span data-stu-id="e0f06-113">If the method fails, \**ppPin* is set to **NULL**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0f06-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0f06-114">Return value</span></span>

<span data-ttu-id="e0f06-115">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e0f06-115">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="e0f06-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e0f06-116">Return code</span></span>                                                                                       | <span data-ttu-id="e0f06-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="e0f06-117">Description</span></span>                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="e0f06-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e0f06-118"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="e0f06-119">Correcto.</span><span class="sxs-lookup"><span data-stu-id="e0f06-119">Success.</span></span><br/>                                   |
| <dl> <span data-ttu-id="e0f06-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="e0f06-120"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="e0f06-121">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="e0f06-121">**NULL** pointer argument.</span></span><br/>                 |
| <dl> <span data-ttu-id="e0f06-122"><dt>**VFW \_ E \_ no \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="e0f06-122"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="e0f06-123">No se encontró un pin con este identificador.</span><span class="sxs-lookup"><span data-stu-id="e0f06-123">Could not find a pin with this identifier.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e0f06-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e0f06-124">Remarks</span></span>

<span data-ttu-id="e0f06-125">El primer PIN siempre se denomina "1"; el segundo PIN se denomina "2"; etc.</span><span class="sxs-lookup"><span data-stu-id="e0f06-125">The first pin is always named "1"; the second pin is named "2"; and so forth.</span></span> <span data-ttu-id="e0f06-126">Para obtener más información, vea [**CSourceStream:: queryId**](csourcestream-queryid.md).</span><span class="sxs-lookup"><span data-stu-id="e0f06-126">For more information, see [**CSourceStream::QueryId**](csourcestream-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0f06-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0f06-127">Requirements</span></span>



| <span data-ttu-id="e0f06-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0f06-128">Requirement</span></span> | <span data-ttu-id="e0f06-129">Value</span><span class="sxs-lookup"><span data-stu-id="e0f06-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0f06-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0f06-130">Header</span></span><br/>  | <dl> <span data-ttu-id="e0f06-131"><dt>Source. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e0f06-131"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="e0f06-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e0f06-132">Library</span></span><br/> | <dl> <span data-ttu-id="e0f06-133"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e0f06-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0f06-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0f06-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0f06-135">**Clase CSource**</span><span class="sxs-lookup"><span data-stu-id="e0f06-135">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




