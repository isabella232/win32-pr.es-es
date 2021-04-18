---
description: El método StreamingThreadUsingOutputPin determina si algún subproceso está realizando una operación de transmisión por secuencias en el código PIN.
ms.assetid: b6432a11-4e8b-4eb4-ad8e-aaff9398641b
title: Método CDynamicOutputPin. StreamingThreadUsingOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.StreamingThreadUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 797dcb94e227861642de2a05e6edf24f675bb4e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671460"
---
# <a name="cdynamicoutputpinstreamingthreadusingoutputpin-method"></a><span data-ttu-id="f1ecb-103">CDynamicOutputPin. StreamingThreadUsingOutputPin, método</span><span class="sxs-lookup"><span data-stu-id="f1ecb-103">CDynamicOutputPin.StreamingThreadUsingOutputPin method</span></span>

<span data-ttu-id="f1ecb-104">El método StreamingThreadUsingOutputPin determina si algún subproceso está realizando una operación de transmisión por secuencias en el código PIN.</span><span class="sxs-lookup"><span data-stu-id="f1ecb-104">The StreamingThreadUsingOutputPin method determines whether any thread is performing a streaming operation on the pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1ecb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f1ecb-105">Syntax</span></span>


```C++
virtual bool StreamingThreadUsingOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="f1ecb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f1ecb-106">Parameters</span></span>

<span data-ttu-id="f1ecb-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f1ecb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f1ecb-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f1ecb-108">Return value</span></span>

<span data-ttu-id="f1ecb-109">Devuelve **true** si un subproceso está realizando una operación de transmisión por secuencias en el código PIN.</span><span class="sxs-lookup"><span data-stu-id="f1ecb-109">Returns **TRUE** if a thread is performing a streaming operation on the pin.</span></span> <span data-ttu-id="f1ecb-110">De lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="f1ecb-110">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1ecb-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f1ecb-111">Remarks</span></span>

<span data-ttu-id="f1ecb-112">Si algún subproceso ha devuelto correctamente desde el método [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) y no ha realizado una llamada correspondiente al método [**CDynamicOutputPin:: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) , este método devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="f1ecb-112">If any threads have successfully returned from the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method and have not made a corresponding call to the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method, this method returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1ecb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1ecb-113">Requirements</span></span>



| <span data-ttu-id="f1ecb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1ecb-114">Requirement</span></span> | <span data-ttu-id="f1ecb-115">Value</span><span class="sxs-lookup"><span data-stu-id="f1ecb-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1ecb-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f1ecb-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f1ecb-117"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1ecb-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f1ecb-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f1ecb-118">Library</span></span><br/> | <dl> <span data-ttu-id="f1ecb-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f1ecb-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1ecb-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1ecb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1ecb-121">**Clase CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="f1ecb-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




