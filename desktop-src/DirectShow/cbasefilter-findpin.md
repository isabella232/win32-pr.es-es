---
description: 'Método CBaseFilter.FindPin: el método FindPin recupera el pin con el identificador especificado. Este método implementa el método IBaseFilter::FindPin.'
ms.assetid: 152e4ff3-2809-4c57-b9c8-f51fc50b3703
title: Método CBaseFilter.FindPin (Amfilter.h)
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
ms.openlocfilehash: 2bbef9b051a42597b2585a432f544eead4e2e0a1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099823"
---
# <a name="cbasefilterfindpin-method"></a><span data-ttu-id="b5a63-104">Método CBaseFilter.FindPin</span><span class="sxs-lookup"><span data-stu-id="b5a63-104">CBaseFilter.FindPin method</span></span>

<span data-ttu-id="b5a63-105">El `FindPin` método recupera el pin con el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="b5a63-105">The `FindPin` method retrieves the pin with the specified identifier.</span></span> <span data-ttu-id="b5a63-106">Este método implementa el [**método IBaseFilter::FindPin.**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin)</span><span class="sxs-lookup"><span data-stu-id="b5a63-106">This method implements the [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5a63-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5a63-107">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="b5a63-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5a63-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5a63-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="b5a63-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="b5a63-110">Puntero a una cadena Unicode constante terminada en NULL que identifica el pin.</span><span class="sxs-lookup"><span data-stu-id="b5a63-110">Pointer to a constant, null-terminated Unicode string that identifies the pin.</span></span>

</dd> <dt>

<span data-ttu-id="b5a63-111">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="b5a63-111">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="b5a63-112">Dirección de una variable que recibe un puntero a la interfaz [**IPin del**](/windows/desktop/api/Strmif/nn-strmif-ipin) pin.</span><span class="sxs-lookup"><span data-stu-id="b5a63-112">Address of a variable that receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5a63-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5a63-113">Return value</span></span>

<span data-ttu-id="b5a63-114">Devuelve uno de los siguientes **valores HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="b5a63-114">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="b5a63-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b5a63-115">Return code</span></span>                                                                                       | <span data-ttu-id="b5a63-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5a63-116">Description</span></span>                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="b5a63-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b5a63-117"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="b5a63-118">Correcto.</span><span class="sxs-lookup"><span data-stu-id="b5a63-118">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="b5a63-119"><dt>**PUNTERO \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="b5a63-119"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="b5a63-120">**Argumento de** puntero NULL.</span><span class="sxs-lookup"><span data-stu-id="b5a63-120">**NULL** pointer argument.</span></span><br/>     |
| <dl> <span data-ttu-id="b5a63-121"><dt>**VFW \_ E \_ NO \_ ENCONTRADO**</dt></span><span class="sxs-lookup"><span data-stu-id="b5a63-121"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="b5a63-122">No se encontró un pin correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b5a63-122">Could not find a matching pin.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b5a63-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b5a63-123">Remarks</span></span>

<span data-ttu-id="b5a63-124">Este método llama al [**método CBasePin::Name**](cbasepin-name.md) para comparar el nombre de cada pin con la cadena especificada por el *parámetro Id.*</span><span class="sxs-lookup"><span data-stu-id="b5a63-124">This method calls the [**CBasePin::Name**](cbasepin-name.md) method to compare each pin's name against the string specified by the *Id* parameter.</span></span>

<span data-ttu-id="b5a63-125">Si el método se realiza correctamente, la **interfaz IPin** tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="b5a63-125">If the method succeeds, the **IPin** interface has an outstanding reference count.</span></span> <span data-ttu-id="b5a63-126">Asegúrese de liberarlo cuando haya terminado.</span><span class="sxs-lookup"><span data-stu-id="b5a63-126">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5a63-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5a63-127">Requirements</span></span>



| <span data-ttu-id="b5a63-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5a63-128">Requirement</span></span> | <span data-ttu-id="b5a63-129">Value</span><span class="sxs-lookup"><span data-stu-id="b5a63-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5a63-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5a63-130">Header</span></span><br/>  | <dl> <span data-ttu-id="b5a63-131"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="b5a63-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b5a63-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b5a63-132">Library</span></span><br/> | <dl> <span data-ttu-id="b5a63-133"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b5a63-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5a63-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b5a63-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5a63-135">**CBaseFilter (clase)**</span><span class="sxs-lookup"><span data-stu-id="b5a63-135">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




