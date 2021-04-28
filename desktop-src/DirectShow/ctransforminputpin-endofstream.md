---
description: 'Método CTransformInputPin.EndOfStream: el método EndOfStream notifica al pin que no se espera ningún dato adicional. Este método implementa el método IPin::EndOfStream.'
ms.assetid: db9896eb-3db2-4d58-a787-4d80ce8f0d0e
title: Método CTransformInputPin.EndOfStream (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2035d0261447826098162f480ddc959544b101b7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084983"
---
# <a name="ctransforminputpinendofstream-method"></a><span data-ttu-id="42b33-104">Método CTransformInputPin.EndOfStream</span><span class="sxs-lookup"><span data-stu-id="42b33-104">CTransformInputPin.EndOfStream method</span></span>

<span data-ttu-id="42b33-105">El `EndOfStream` método notifica al pin que no se espera ningún dato adicional.</span><span class="sxs-lookup"><span data-stu-id="42b33-105">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="42b33-106">Este método implementa el [**método IPin::EndOfStream.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)</span><span class="sxs-lookup"><span data-stu-id="42b33-106">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="42b33-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42b33-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="42b33-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="42b33-108">Parameters</span></span>

<span data-ttu-id="42b33-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="42b33-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="42b33-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="42b33-110">Return value</span></span>

<span data-ttu-id="42b33-111">Devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="42b33-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="42b33-112">Los valores posibles incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="42b33-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="42b33-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="42b33-113">Return code</span></span>                                                                                           | <span data-ttu-id="42b33-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="42b33-114">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="42b33-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="42b33-115"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="42b33-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="42b33-116">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="42b33-117"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="42b33-117"><dt>**S\_FALSE**</dt></span></span> </dl>               | <span data-ttu-id="42b33-118">El pin se está vacíando actualmente.</span><span class="sxs-lookup"><span data-stu-id="42b33-118">Pin is currently flushing.</span></span><br/>       |
| <dl> <span data-ttu-id="42b33-119"><dt>**VFW \_ E \_ NO \_ CONECTADO**</dt></span><span class="sxs-lookup"><span data-stu-id="42b33-119"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="42b33-120">El pin de salida no está conectado.</span><span class="sxs-lookup"><span data-stu-id="42b33-120">The output pin is not connected.</span></span><br/> |
| <dl> <span data-ttu-id="42b33-121"><dt>**ERROR EN TIEMPO DE EJECUCIÓN DE VFW \_ E \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="42b33-121"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="42b33-122">Se produjo un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="42b33-122">A run-time error occurred.</span></span><br/>       |
| <dl> <span data-ttu-id="42b33-123"><dt>**VFW \_ E \_ ESTADO \_ INCORRECTO**</dt></span><span class="sxs-lookup"><span data-stu-id="42b33-123"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>   | <span data-ttu-id="42b33-124">El pin se detiene.</span><span class="sxs-lookup"><span data-stu-id="42b33-124">The pin is stopped.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="42b33-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="42b33-125">Remarks</span></span>

<span data-ttu-id="42b33-126">Este método llama al método [**CTransformFilter::EndOfStream**](ctransformfilter-endofstream.md) del filtro para entregar la notificación de fin de flujo de bajada.</span><span class="sxs-lookup"><span data-stu-id="42b33-126">This method calls the filter's [**CTransformFilter::EndOfStream**](ctransformfilter-endofstream.md) method to deliver the end-of-stream notification downstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="42b33-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42b33-127">Requirements</span></span>



| <span data-ttu-id="42b33-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="42b33-128">Requirement</span></span> | <span data-ttu-id="42b33-129">Value</span><span class="sxs-lookup"><span data-stu-id="42b33-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42b33-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42b33-130">Header</span></span><br/>  | <dl> <span data-ttu-id="42b33-131"><dt>Transfrm.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="42b33-131"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="42b33-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="42b33-132">Library</span></span><br/> | <dl> <span data-ttu-id="42b33-133"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="42b33-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




