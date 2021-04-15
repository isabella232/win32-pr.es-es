---
description: El método BlockOutputPin bloquea el código PIN.
ms.assetid: 49f6b8da-a8b2-482d-b70d-2c68a1b45a10
title: Método CDynamicOutputPin. BlockOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.BlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3998774550363b7d22e05ca491f1d76ba7f2ff2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661359"
---
# <a name="cdynamicoutputpinblockoutputpin-method"></a><span data-ttu-id="ef37c-103">CDynamicOutputPin. BlockOutputPin, método</span><span class="sxs-lookup"><span data-stu-id="ef37c-103">CDynamicOutputPin.BlockOutputPin method</span></span>

<span data-ttu-id="ef37c-104">El `BlockOutputPin` método bloquea el código PIN.</span><span class="sxs-lookup"><span data-stu-id="ef37c-104">The `BlockOutputPin` method blocks the pin.</span></span> <span data-ttu-id="ef37c-105">Mientras se bloquea el PIN, el método [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) espera a que el PIN se desbloquee.</span><span class="sxs-lookup"><span data-stu-id="ef37c-105">While the pin is blocked, the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method waits for the pin to become unblocked.</span></span> <span data-ttu-id="ef37c-106">El estado bloqueado impide que la clavija de salida entregue ejemplos, cambie su formato de salida o vuelva a conectarse a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="ef37c-106">The blocked state prevents the output pin from delivering samples, changing its output format, or reconnecting itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef37c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ef37c-107">Syntax</span></span>


```C++
void BlockOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="ef37c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ef37c-108">Parameters</span></span>

<span data-ttu-id="ef37c-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ef37c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ef37c-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef37c-110">Return value</span></span>

<span data-ttu-id="ef37c-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ef37c-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef37c-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef37c-112">Remarks</span></span>

<span data-ttu-id="ef37c-113">Antes de llamar a este método, conserve la sección crítica [**CDynamicOutputPin:: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="ef37c-113">Before calling this method, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span> <span data-ttu-id="ef37c-114">No llame a este método si un subproceso de streaming está utilizando el PIN, ya sea para proporcionar datos o para cambiar la conexión.</span><span class="sxs-lookup"><span data-stu-id="ef37c-114">Do not call this method if a streaming thread is using the pin, either to deliver data or to change the connection.</span></span> <span data-ttu-id="ef37c-115">Para comprobar si un subproceso de streaming está utilizando el PIN, llame al método [**CDynamicOutputPin:: StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="ef37c-115">To check whether a streaming thread is using the pin, call the [**CDynamicOutputPin::StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef37c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef37c-116">Requirements</span></span>



| <span data-ttu-id="ef37c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef37c-117">Requirement</span></span> | <span data-ttu-id="ef37c-118">Value</span><span class="sxs-lookup"><span data-stu-id="ef37c-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef37c-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef37c-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ef37c-120"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef37c-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ef37c-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ef37c-121">Library</span></span><br/> | <dl> <span data-ttu-id="ef37c-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ef37c-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef37c-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef37c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef37c-124">**Clase CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="ef37c-124">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




