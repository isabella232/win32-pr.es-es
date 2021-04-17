---
description: 'El método ConnectTo recupera un puntero al pin conectado, si existe. Este método implementa el método IPin:: ConnectTo.'
ms.assetid: d8978c9a-e498-4411-a052-f3c2fca570ef
title: Método CBasePin. ConnectTo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ConnectedTo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5003154011f93b2b70ddd49dab00dcc1659eb2f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670845"
---
# <a name="cbasepinconnectedto-method"></a><span data-ttu-id="5a09f-104">CBasePin. ConnectTo (método)</span><span class="sxs-lookup"><span data-stu-id="5a09f-104">CBasePin.ConnectedTo method</span></span>

<span data-ttu-id="5a09f-105">El `ConnectedTo` método recupera un puntero al pin conectado, si existe.</span><span class="sxs-lookup"><span data-stu-id="5a09f-105">The `ConnectedTo` method retrieves a pointer to the connected pin, if any.</span></span> <span data-ttu-id="5a09f-106">Este método implementa el método [**IPin:: ConnectTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) .</span><span class="sxs-lookup"><span data-stu-id="5a09f-106">This method implements the [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a09f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5a09f-107">Syntax</span></span>


```C++
HRESULT ConnectedTo(
   IPin **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="5a09f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5a09f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a09f-109">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="5a09f-109">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="5a09f-110">Dirección de una variable que recibe un puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del otro PIN.</span><span class="sxs-lookup"><span data-stu-id="5a09f-110">Address of a variable that receives a pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a09f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5a09f-111">Return value</span></span>

<span data-ttu-id="5a09f-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5a09f-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="5a09f-113">Entre los valores posibles se incluyen los de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="5a09f-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="5a09f-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="5a09f-114">Return code</span></span>                                                                                           | <span data-ttu-id="5a09f-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="5a09f-115">Description</span></span>                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="5a09f-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="5a09f-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="5a09f-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="5a09f-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="5a09f-118"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="5a09f-118"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="5a09f-119">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="5a09f-119">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="5a09f-120"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="5a09f-120"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="5a09f-121">El PIN no está conectado.</span><span class="sxs-lookup"><span data-stu-id="5a09f-121">Pin is not connected.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="5a09f-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5a09f-122">Remarks</span></span>

<span data-ttu-id="5a09f-123">Si el método se ejecuta correctamente, la interfaz **IPin** que devuelve tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="5a09f-123">If the method succeeds, the **IPin** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="5a09f-124">Asegúrese de liberarlo cuando haya terminado.</span><span class="sxs-lookup"><span data-stu-id="5a09f-124">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a09f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a09f-125">Requirements</span></span>



| <span data-ttu-id="5a09f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a09f-126">Requirement</span></span> | <span data-ttu-id="5a09f-127">Value</span><span class="sxs-lookup"><span data-stu-id="5a09f-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a09f-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5a09f-128">Header</span></span><br/>  | <dl> <span data-ttu-id="5a09f-129"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5a09f-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5a09f-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5a09f-130">Library</span></span><br/> | <dl> <span data-ttu-id="5a09f-131"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5a09f-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a09f-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a09f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a09f-133">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="5a09f-133">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




