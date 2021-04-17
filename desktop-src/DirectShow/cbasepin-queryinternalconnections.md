---
description: 'El método QueryInternalConnections recupera los PIN que están conectados internamente a este pin (dentro del filtro). Este método implementa el método IPin:: QueryInternalConnections.'
ms.assetid: 08344fc5-38b2-4dbe-8ef9-30d2fcd64187
title: Método CBasePin. QueryInternalConnections (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryInternalConnections
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 99a636295fc87347a1735ab028b6de342e887d55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660617"
---
# <a name="cbasepinqueryinternalconnections-method"></a><span data-ttu-id="9aabe-104">CBasePin. QueryInternalConnections, método</span><span class="sxs-lookup"><span data-stu-id="9aabe-104">CBasePin.QueryInternalConnections method</span></span>

<span data-ttu-id="9aabe-105">El `QueryInternalConnections` método recupera los PIN que están conectados internamente a este pin (dentro del filtro).</span><span class="sxs-lookup"><span data-stu-id="9aabe-105">The `QueryInternalConnections` method retrieves the pins that are connected internally to this pin (within the filter).</span></span> <span data-ttu-id="9aabe-106">Este método implementa el método [**IPin:: QueryInternalConnections**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryinternalconnections) .</span><span class="sxs-lookup"><span data-stu-id="9aabe-106">This method implements the [**IPin::QueryInternalConnections**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryinternalconnections) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aabe-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9aabe-107">Syntax</span></span>


```C++
HRESULT QueryInternalConnections(
   IPin  *apPin,
   ULONG *nPin
);
```



## <a name="parameters"></a><span data-ttu-id="9aabe-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9aabe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9aabe-109">*iníciela*</span><span class="sxs-lookup"><span data-stu-id="9aabe-109">*apPin*</span></span> 
</dt> <dd>

<span data-ttu-id="9aabe-110">Dirección de una matriz de punteros [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="9aabe-110">Address of an array of [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) pointers.</span></span>

</dd> <dt>

<span data-ttu-id="9aabe-111">*nPin*</span><span class="sxs-lookup"><span data-stu-id="9aabe-111">*nPin*</span></span> 
</dt> <dd>

<span data-ttu-id="9aabe-112">En la entrada, especifica el tamaño de la matriz.</span><span class="sxs-lookup"><span data-stu-id="9aabe-112">On input, specifies the size of the array.</span></span> <span data-ttu-id="9aabe-113">Cuando el método devuelve, el valor se establece en el número de punteros devueltos en la matriz.</span><span class="sxs-lookup"><span data-stu-id="9aabe-113">When the method returns, the value is set to the number of pointers returned in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9aabe-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9aabe-114">Return value</span></span>

<span data-ttu-id="9aabe-115">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="9aabe-115">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="9aabe-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9aabe-116">Return code</span></span>                                                                               | <span data-ttu-id="9aabe-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="9aabe-117">Description</span></span>                         |
|-------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="9aabe-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="9aabe-118"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="9aabe-119">Tamaño de matriz insuficiente.</span><span class="sxs-lookup"><span data-stu-id="9aabe-119">Insufficient array size.</span></span><br/> |
| <dl> <span data-ttu-id="9aabe-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="9aabe-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="9aabe-121">Correcto.</span><span class="sxs-lookup"><span data-stu-id="9aabe-121">Success.</span></span><br/>                 |
| <dl> <span data-ttu-id="9aabe-122"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="9aabe-122"><dt>**E\_FAIL**</dt></span></span> </dl>    | <span data-ttu-id="9aabe-123">Error.</span><span class="sxs-lookup"><span data-stu-id="9aabe-123">Failure.</span></span><br/>                 |
| <dl> <span data-ttu-id="9aabe-124"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="9aabe-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="9aabe-125">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="9aabe-125">Not implemented.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="9aabe-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9aabe-126">Remarks</span></span>

<span data-ttu-id="9aabe-127">En algunos filtros, los pin de entrada se corresponden con clavijas de salida particulares.</span><span class="sxs-lookup"><span data-stu-id="9aabe-127">On some filters, input pins correspond to particular output pins.</span></span> <span data-ttu-id="9aabe-128">Para cada pin, este método rellena una matriz con punteros a los pin correspondientes.</span><span class="sxs-lookup"><span data-stu-id="9aabe-128">For each pin, this method fills an array with pointers to the corresponding pins.</span></span> <span data-ttu-id="9aabe-129">Si cada pin de entrada proporciona datos para cada pin de salida, devuelva E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="9aabe-129">If every input pin provides data for every output pin, return E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aabe-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9aabe-130">Requirements</span></span>



| <span data-ttu-id="9aabe-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="9aabe-131">Requirement</span></span> | <span data-ttu-id="9aabe-132">Value</span><span class="sxs-lookup"><span data-stu-id="9aabe-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9aabe-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9aabe-133">Header</span></span><br/>  | <dl> <span data-ttu-id="9aabe-134"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9aabe-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9aabe-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9aabe-135">Library</span></span><br/> | <dl> <span data-ttu-id="9aabe-136"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9aabe-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9aabe-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="9aabe-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aabe-138">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="9aabe-138">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




