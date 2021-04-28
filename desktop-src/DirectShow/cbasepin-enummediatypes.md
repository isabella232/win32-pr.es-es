---
description: 'Método CBasePin.EnumMediaTypes: el método EnumMediaTypes enumera los tipos de medios preferidos del pin. Este método implementa el método IPin::EnumMediaTypes.'
ms.assetid: 0360f9fc-6876-4a54-8de1-bf289e0e10ae
title: Método CBasePin.EnumMediaTypes (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c68fe1ab83724149dcd2fb58a60e9c6950d887ca
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099402"
---
# <a name="cbasepinenummediatypes-method"></a><span data-ttu-id="2cf4a-104">Método CBasePin.EnumMediaTypes</span><span class="sxs-lookup"><span data-stu-id="2cf4a-104">CBasePin.EnumMediaTypes method</span></span>

<span data-ttu-id="2cf4a-105">El `EnumMediaTypes` método enumera los tipos de medios preferidos del pin.</span><span class="sxs-lookup"><span data-stu-id="2cf4a-105">The `EnumMediaTypes` method enumerates the pin's preferred media types.</span></span> <span data-ttu-id="2cf4a-106">Este método implementa el [**método IPin::EnumMediaTypes.**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes)</span><span class="sxs-lookup"><span data-stu-id="2cf4a-106">This method implements the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cf4a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2cf4a-107">Syntax</span></span>


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="2cf4a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2cf4a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cf4a-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="2cf4a-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="2cf4a-110">Dirección de una variable que recibe un puntero a la [**interfaz IEnumMediaTypes.**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes)</span><span class="sxs-lookup"><span data-stu-id="2cf4a-110">Address of a variable that receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cf4a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2cf4a-111">Return value</span></span>

<span data-ttu-id="2cf4a-112">Devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="2cf4a-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="2cf4a-113">Los valores posibles incluyen los de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2cf4a-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="2cf4a-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2cf4a-114">Return code</span></span>                                                                                   | <span data-ttu-id="2cf4a-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="2cf4a-115">Description</span></span>                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="2cf4a-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2cf4a-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2cf4a-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="2cf4a-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="2cf4a-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2cf4a-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2cf4a-119">Memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="2cf4a-119">Insufficient memory.</span></span><br/>       |
| <dl> <span data-ttu-id="2cf4a-120"><dt>**PUNTERO \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="2cf4a-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="2cf4a-121">**Argumento de** puntero NULL.</span><span class="sxs-lookup"><span data-stu-id="2cf4a-121">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2cf4a-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2cf4a-122">Remarks</span></span>

<span data-ttu-id="2cf4a-123">Los pines de entrada no son necesarios para enumerar los tipos preferidos.</span><span class="sxs-lookup"><span data-stu-id="2cf4a-123">Input pins are not required to enumerate any preferred types.</span></span> <span data-ttu-id="2cf4a-124">Los pines de salida deben enumerar al menos un tipo preferido.</span><span class="sxs-lookup"><span data-stu-id="2cf4a-124">Output pins must enumerate at least one preferred type.</span></span> <span data-ttu-id="2cf4a-125">De lo contrario, ambos pines podrían carecer de un tipo preferido, lo que imposibilitó una conexión.</span><span class="sxs-lookup"><span data-stu-id="2cf4a-125">Otherwise, both pins could lack a preferred type, making a connection impossible.</span></span>

<span data-ttu-id="2cf4a-126">La **interfaz IEnumMediaTypes** funciona como un enumerador COM estándar.</span><span class="sxs-lookup"><span data-stu-id="2cf4a-126">The **IEnumMediaTypes** interface works like a standard COM enumerator.</span></span> <span data-ttu-id="2cf4a-127">Para obtener más información, [vea Enumerar objetos en un gráfico de filtro.](enumerating-objects-in-a-filter-graph.md)</span><span class="sxs-lookup"><span data-stu-id="2cf4a-127">For more information, see [Enumerating Objects in a Filter Graph](enumerating-objects-in-a-filter-graph.md).</span></span> <span data-ttu-id="2cf4a-128">Si el método se realiza correctamente, la **interfaz IEnumMediaTypes** tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="2cf4a-128">If the method succeeds, the **IEnumMediaTypes** interface has an outstanding reference count.</span></span> <span data-ttu-id="2cf4a-129">Asegúrese de liberarlo cuando haya terminado.</span><span class="sxs-lookup"><span data-stu-id="2cf4a-129">Be sure to release it when you are done.</span></span>

<span data-ttu-id="2cf4a-130">La clase base [**CEnumMediaTypes**](cenummediatypes.md) implementa **IEnumMediaTypes**.</span><span class="sxs-lookup"><span data-stu-id="2cf4a-130">The [**CEnumMediaTypes**](cenummediatypes.md) base class implements **IEnumMediaTypes**.</span></span> <span data-ttu-id="2cf4a-131">Llama al método [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) del pin para enumerar los tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="2cf4a-131">It calls the pin's [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method to enumerate the media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cf4a-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cf4a-132">Requirements</span></span>



| <span data-ttu-id="2cf4a-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cf4a-133">Requirement</span></span> | <span data-ttu-id="2cf4a-134">Value</span><span class="sxs-lookup"><span data-stu-id="2cf4a-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cf4a-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2cf4a-135">Header</span></span><br/>  | <dl> <span data-ttu-id="2cf4a-136"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="2cf4a-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2cf4a-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2cf4a-137">Library</span></span><br/> | <dl> <span data-ttu-id="2cf4a-138"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2cf4a-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cf4a-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2cf4a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cf4a-140">**CBasePin (clase)**</span><span class="sxs-lookup"><span data-stu-id="2cf4a-140">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




