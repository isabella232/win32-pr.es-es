---
description: 'El método FindPin obtiene el pin con el identificador especificado. Este método implementa el método IBaseFilter:: FindPin.'
ms.assetid: 56ee3e0d-9e3f-4d25-846b-50119b55a122
title: Método CTransformFilter. FindPin (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1631651932d5adbc49fb59d44291dccea55fd41f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660621"
---
# <a name="ctransformfilterfindpin-method"></a><span data-ttu-id="61ca9-104">CTransformFilter. FindPin, método</span><span class="sxs-lookup"><span data-stu-id="61ca9-104">CTransformFilter.FindPin method</span></span>

<span data-ttu-id="61ca9-105">El método **FindPin** obtiene el pin con el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="61ca9-105">The **FindPin** method gets the pin with the specified identifier.</span></span> <span data-ttu-id="61ca9-106">Este método implementa el método [**IBaseFilter:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) .</span><span class="sxs-lookup"><span data-stu-id="61ca9-106">This method implements the [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="61ca9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61ca9-107">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="61ca9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="61ca9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61ca9-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="61ca9-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="61ca9-110">Cadena de caracteres anchos que contiene el identificador del PIN.</span><span class="sxs-lookup"><span data-stu-id="61ca9-110">Wide-character string that contains the pin identifier.</span></span>

</dd> <dt>

<span data-ttu-id="61ca9-111">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="61ca9-111">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="61ca9-112">Recibe un puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN.</span><span class="sxs-lookup"><span data-stu-id="61ca9-112">Receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span> <span data-ttu-id="61ca9-113">Si se produce un error en el método, `*ppPin` se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="61ca9-113">If the method fails, `*ppPin` is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61ca9-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61ca9-114">Return value</span></span>

<span data-ttu-id="61ca9-115">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="61ca9-115">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="61ca9-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="61ca9-116">Return code</span></span>                                                                                       | <span data-ttu-id="61ca9-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="61ca9-117">Description</span></span>                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="61ca9-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="61ca9-118"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="61ca9-119">Correcto.</span><span class="sxs-lookup"><span data-stu-id="61ca9-119">Success.</span></span><br/>                                   |
| <dl> <span data-ttu-id="61ca9-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="61ca9-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>     | <span data-ttu-id="61ca9-121">Memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="61ca9-121">Insufficient memory.</span></span><br/>                       |
| <dl> <span data-ttu-id="61ca9-122"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="61ca9-122"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="61ca9-123">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="61ca9-123">**NULL** pointer argument.</span></span><br/>                 |
| <dl> <span data-ttu-id="61ca9-124"><dt>**VFW \_ E \_ no \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="61ca9-124"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="61ca9-125">No se encontró un pin con este identificador.</span><span class="sxs-lookup"><span data-stu-id="61ca9-125">Could not find a pin with this identifier.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="61ca9-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61ca9-126">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="61ca9-127">La implementación de este método no llama a [**IPin:: queryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) para que coincida con el identificador del PIN.</span><span class="sxs-lookup"><span data-stu-id="61ca9-127">The implementation of this method does not call [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) to match the pin identifier.</span></span> <span data-ttu-id="61ca9-128">En su lugar, el método supone que el PIN de entrada se denomina "in" y el PIN de salida se denomina "out".</span><span class="sxs-lookup"><span data-stu-id="61ca9-128">Instead, the method assumes that the input pin is named "In", and the output pin is named "Out".</span></span> <span data-ttu-id="61ca9-129">Si usa un conjunto de identificadores de PIN diferente, Invalide este método.</span><span class="sxs-lookup"><span data-stu-id="61ca9-129">If you use a different set of pin identifiers, override this method.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="61ca9-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61ca9-130">Requirements</span></span>



| <span data-ttu-id="61ca9-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="61ca9-131">Requirement</span></span> | <span data-ttu-id="61ca9-132">Value</span><span class="sxs-lookup"><span data-stu-id="61ca9-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61ca9-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="61ca9-133">Header</span></span><br/>  | <dl> <span data-ttu-id="61ca9-134"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="61ca9-134"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="61ca9-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="61ca9-135">Library</span></span><br/> | <dl> <span data-ttu-id="61ca9-136"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="61ca9-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61ca9-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="61ca9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61ca9-138">**Clase CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="61ca9-138">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




