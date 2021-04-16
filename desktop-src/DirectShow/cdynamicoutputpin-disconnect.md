---
description: El método Disconnect interrumpe la conexión del PIN actual. Este método implementa el método IPin::D Ulta.
ms.assetid: 8d92a504-98ad-4f8f-89a4-f0c80763db44
title: Método CDynamicOutputPin. disconnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 65c61ecc825d703976aa3163be5922da1ac4471a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671472"
---
# <a name="cdynamicoutputpindisconnect-method"></a><span data-ttu-id="1d3cc-104">CDynamicOutputPin. disconnect (método)</span><span class="sxs-lookup"><span data-stu-id="1d3cc-104">CDynamicOutputPin.Disconnect method</span></span>

<span data-ttu-id="1d3cc-105">El `Disconnect` método interrumpe la conexión del PIN actual.</span><span class="sxs-lookup"><span data-stu-id="1d3cc-105">The `Disconnect` method breaks the current pin connection.</span></span> <span data-ttu-id="1d3cc-106">Este método implementa el método [**IPin::D Ulta**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) .</span><span class="sxs-lookup"><span data-stu-id="1d3cc-106">This method implements the [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d3cc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d3cc-107">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="1d3cc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1d3cc-108">Parameters</span></span>

<span data-ttu-id="1d3cc-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1d3cc-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1d3cc-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1d3cc-110">Return value</span></span>

<span data-ttu-id="1d3cc-111">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1d3cc-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1d3cc-112">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="1d3cc-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="1d3cc-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1d3cc-113">Return code</span></span>                                                                             | <span data-ttu-id="1d3cc-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d3cc-114">Description</span></span>                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="1d3cc-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="1d3cc-115"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="1d3cc-116">El PIN no estaba conectado.</span><span class="sxs-lookup"><span data-stu-id="1d3cc-116">The pin was not connected.</span></span><br/> |
| <dl> <span data-ttu-id="1d3cc-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="1d3cc-117"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="1d3cc-118">Correcto.</span><span class="sxs-lookup"><span data-stu-id="1d3cc-118">Success.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="1d3cc-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1d3cc-119">Remarks</span></span>

<span data-ttu-id="1d3cc-120">Este método invalida el método [**CBasePin::D Ulta**](cbasepin-disconnect.md) para habilitar la desconexión mientras el filtro está activo.</span><span class="sxs-lookup"><span data-stu-id="1d3cc-120">This method overrides the [**CBasePin::Disconnect**](cbasepin-disconnect.md) method to enable disconnecting while the filter is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d3cc-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d3cc-121">Requirements</span></span>



| <span data-ttu-id="1d3cc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d3cc-122">Requirement</span></span> | <span data-ttu-id="1d3cc-123">Value</span><span class="sxs-lookup"><span data-stu-id="1d3cc-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d3cc-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d3cc-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1d3cc-125"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d3cc-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1d3cc-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1d3cc-126">Library</span></span><br/> | <dl> <span data-ttu-id="1d3cc-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1d3cc-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d3cc-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d3cc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d3cc-129">**Clase CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="1d3cc-129">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




