---
description: Determina si el pin puede aceptar ejemplos.
ms.assetid: bc66ab4c-99de-4031-bdac-b1430f736e20
title: Método CBaseInputPin. CheckStreaming (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.CheckStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba07d28ac93f7dc511390a851d3c737a833ef3f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660145"
---
# <a name="cbaseinputpincheckstreaming-method"></a><span data-ttu-id="1b31a-103">CBaseInputPin. CheckStreaming, método</span><span class="sxs-lookup"><span data-stu-id="1b31a-103">CBaseInputPin.CheckStreaming method</span></span>

<span data-ttu-id="1b31a-104">Determina si el pin puede aceptar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="1b31a-104">Determines whether the pin can accept samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b31a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1b31a-105">Syntax</span></span>


```C++
virtual HRESULT CheckStreaming();
```



## <a name="parameters"></a><span data-ttu-id="1b31a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1b31a-106">Parameters</span></span>

<span data-ttu-id="1b31a-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1b31a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1b31a-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b31a-108">Return value</span></span>

<span data-ttu-id="1b31a-109">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="1b31a-109">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="1b31a-110">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1b31a-110">Return code</span></span>                                                                                           | <span data-ttu-id="1b31a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b31a-111">Description</span></span>                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="1b31a-112"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="1b31a-112"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="1b31a-113">Correcto.</span><span class="sxs-lookup"><span data-stu-id="1b31a-113">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="1b31a-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="1b31a-114"><dt>**S\_FALSE**</dt></span></span> </dl>               | <span data-ttu-id="1b31a-115">El PIN se está vaciando actualmente.</span><span class="sxs-lookup"><span data-stu-id="1b31a-115">Pin is currently flushing.</span></span><br/> |
| <dl> <span data-ttu-id="1b31a-116"><dt>**\_error de \_ tiempo de ejecución de VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1b31a-116"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="1b31a-117">Se produjo un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="1b31a-117">A run-time error occurred.</span></span><br/> |
| <dl> <span data-ttu-id="1b31a-118"><dt>**Estado de VFW \_ E \_ incorrecto \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1b31a-118"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>   | <span data-ttu-id="1b31a-119">El PIN está detenido.</span><span class="sxs-lookup"><span data-stu-id="1b31a-119">The pin is stopped.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="1b31a-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1b31a-120">Remarks</span></span>

<span data-ttu-id="1b31a-121">La clase derivada puede invalidar este método para realizar comprobaciones adicionales.</span><span class="sxs-lookup"><span data-stu-id="1b31a-121">The derived class can override this method to perform further checks.</span></span> <span data-ttu-id="1b31a-122">En el método de reemplazo, llame también a la implementación de la clase base.</span><span class="sxs-lookup"><span data-stu-id="1b31a-122">In the overriding method, also call the base class implementation.</span></span>

<span data-ttu-id="1b31a-123">El método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) llama a este método.</span><span class="sxs-lookup"><span data-stu-id="1b31a-123">The [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method calls this method.</span></span> <span data-ttu-id="1b31a-124">Debe reemplazar el método [**CBasePin:: EndOfStream**](cbasepin-endofstream.md) para llamar también a este método.</span><span class="sxs-lookup"><span data-stu-id="1b31a-124">You should override the [**CBasePin::EndOfStream**](cbasepin-endofstream.md) method to call this method as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b31a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b31a-125">Requirements</span></span>



| <span data-ttu-id="1b31a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b31a-126">Requirement</span></span> | <span data-ttu-id="1b31a-127">Value</span><span class="sxs-lookup"><span data-stu-id="1b31a-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b31a-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1b31a-128">Header</span></span><br/>  | <dl> <span data-ttu-id="1b31a-129"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1b31a-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1b31a-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1b31a-130">Library</span></span><br/> | <dl> <span data-ttu-id="1b31a-131"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1b31a-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b31a-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b31a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b31a-133">**Clase CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="1b31a-133">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




