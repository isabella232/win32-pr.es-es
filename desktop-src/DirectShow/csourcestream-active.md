---
description: 'El método activo notifica al pin que el filtro está activo ahora. Este método invalida el método CBasePin:: active. Si el PIN está conectado, este método inicia el subproceso de streaming.'
ms.assetid: ea32b602-2583-4de6-96ec-6ea875c49d14
title: Método CSourceStream. Active (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a161c82621f29b916e03fbc2e59ec762871940b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690509"
---
# <a name="csourcestreamactive-method"></a><span data-ttu-id="c9f9a-105">CSourceStream. Active (método)</span><span class="sxs-lookup"><span data-stu-id="c9f9a-105">CSourceStream.Active method</span></span>

<span data-ttu-id="c9f9a-106">El `Active` método notifica al pin que el filtro está activo ahora.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-106">The `Active` method notifies the pin that the filter is now active.</span></span> <span data-ttu-id="c9f9a-107">Este método invalida el método [**CBasePin:: Active**](cbasepin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="c9f9a-107">This method overrides the [**CBasePin::Active**](cbasepin-active.md) method.</span></span> <span data-ttu-id="c9f9a-108">Si el PIN está conectado, este método inicia el subproceso de streaming.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-108">If the pin is connected, this method starts the streaming thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9f9a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9f9a-109">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="c9f9a-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9f9a-110">Parameters</span></span>

<span data-ttu-id="c9f9a-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c9f9a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9f9a-112">Return value</span></span>

<span data-ttu-id="c9f9a-113">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c9f9a-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c9f9a-114">Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-114">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="c9f9a-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c9f9a-115">Return code</span></span>                                                                             | <span data-ttu-id="c9f9a-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9f9a-116">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="c9f9a-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="c9f9a-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="c9f9a-118">El PIN ya está activo.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-118">The pin is already active.</span></span><br/>  |
| <dl> <span data-ttu-id="c9f9a-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="c9f9a-119"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="c9f9a-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-120">Success.</span></span><br/>                    |
| <dl> <span data-ttu-id="c9f9a-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="c9f9a-121"><dt>**E\_FAIL**</dt></span></span> </dl>  | <span data-ttu-id="c9f9a-122">No se pudo iniciar el subproceso.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-122">Could not start the thread.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c9f9a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9f9a-123">Requirements</span></span>



| <span data-ttu-id="c9f9a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9f9a-124">Requirement</span></span> | <span data-ttu-id="c9f9a-125">Value</span><span class="sxs-lookup"><span data-stu-id="c9f9a-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9f9a-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9f9a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c9f9a-127"><dt>Source. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9f9a-127"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c9f9a-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c9f9a-128">Library</span></span><br/> | <dl> <span data-ttu-id="c9f9a-129"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c9f9a-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9f9a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9f9a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9f9a-131">**Clase CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="c9f9a-131">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




