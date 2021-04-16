---
description: El método UnblockOutputPin desbloquea el código PIN. Cuando el PIN está desbloqueado, puede proporcionar ejemplos, cambiar su formato de salida y volver a conectarse a sí mismo.
ms.assetid: ea6e6312-8c7f-44db-ac7f-165dc45dec23
title: Método CDynamicOutputPin. UnblockOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.UnblockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60bcde3ccad01e19f3802e2cd19f0f6b873380ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671459"
---
# <a name="cdynamicoutputpinunblockoutputpin-method"></a><span data-ttu-id="cb035-104">CDynamicOutputPin. UnblockOutputPin, método</span><span class="sxs-lookup"><span data-stu-id="cb035-104">CDynamicOutputPin.UnblockOutputPin method</span></span>

<span data-ttu-id="cb035-105">El `UnblockOutputPin` método desbloquea el código PIN.</span><span class="sxs-lookup"><span data-stu-id="cb035-105">The `UnblockOutputPin` method unblocks the pin.</span></span> <span data-ttu-id="cb035-106">Cuando el PIN está desbloqueado, puede proporcionar ejemplos, cambiar su formato de salida y volver a conectarse a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="cb035-106">When the pin is unblocked, it can deliver samples, change its output format, and reconnect itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb035-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb035-107">Syntax</span></span>


```C++
HRESULT UnblockOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="cb035-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb035-108">Parameters</span></span>

<span data-ttu-id="cb035-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="cb035-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cb035-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb035-110">Return value</span></span>

<span data-ttu-id="cb035-111">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="cb035-111">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="cb035-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="cb035-112">Return code</span></span>                                                                             | <span data-ttu-id="cb035-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="cb035-113">Description</span></span>                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="cb035-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="cb035-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="cb035-115">El PIN ya estaba desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="cb035-115">Pin was already unblocked.</span></span><br/> |
| <dl> <span data-ttu-id="cb035-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="cb035-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="cb035-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="cb035-117">Success.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="cb035-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb035-118">Requirements</span></span>



| <span data-ttu-id="cb035-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb035-119">Requirement</span></span> | <span data-ttu-id="cb035-120">Value</span><span class="sxs-lookup"><span data-stu-id="cb035-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb035-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cb035-121">Header</span></span><br/>  | <dl> <span data-ttu-id="cb035-122"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb035-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cb035-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cb035-123">Library</span></span><br/> | <dl> <span data-ttu-id="cb035-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="cb035-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb035-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb035-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb035-126">**Clase CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="cb035-126">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




