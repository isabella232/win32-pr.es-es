---
description: El método CheckStreaming determina si el pin puede aceptar ejemplos.
ms.assetid: fa063966-4c72-466e-933c-def6a6818621
title: Método CTransformInputPin. CheckStreaming (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e5c49a00054547193e3f492f0731f77af8331a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660686"
---
# <a name="ctransforminputpincheckstreaming-method"></a><span data-ttu-id="db66b-103">CTransformInputPin. CheckStreaming, método</span><span class="sxs-lookup"><span data-stu-id="db66b-103">CTransformInputPin.CheckStreaming method</span></span>

<span data-ttu-id="db66b-104">El `CheckStreaming` método determina si el pin puede aceptar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="db66b-104">The `CheckStreaming` method determines whether the pin can accept samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="db66b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="db66b-105">Syntax</span></span>


```C++
HRESULT CheckStreaming();
```



## <a name="parameters"></a><span data-ttu-id="db66b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db66b-106">Parameters</span></span>

<span data-ttu-id="db66b-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="db66b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="db66b-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="db66b-108">Return value</span></span>

<span data-ttu-id="db66b-109">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="db66b-109">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="db66b-110">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="db66b-110">Return code</span></span>                                                                                           | <span data-ttu-id="db66b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="db66b-111">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="db66b-112"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="db66b-112"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="db66b-113">Correcto.</span><span class="sxs-lookup"><span data-stu-id="db66b-113">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="db66b-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="db66b-114"><dt>**S\_FALSE**</dt></span></span> </dl>               | <span data-ttu-id="db66b-115">El PIN se está vaciando actualmente.</span><span class="sxs-lookup"><span data-stu-id="db66b-115">Pin is currently flushing.</span></span><br/>       |
| <dl> <span data-ttu-id="db66b-116"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="db66b-116"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="db66b-117">El PIN de salida no está conectado.</span><span class="sxs-lookup"><span data-stu-id="db66b-117">The output pin is not connected.</span></span><br/> |
| <dl> <span data-ttu-id="db66b-118"><dt>**\_error de \_ tiempo de ejecución de VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="db66b-118"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="db66b-119">Se produjo un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="db66b-119">A run-time error occurred.</span></span><br/>       |
| <dl> <span data-ttu-id="db66b-120"><dt>**Estado de VFW \_ E \_ incorrecto \_**</dt></span><span class="sxs-lookup"><span data-stu-id="db66b-120"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>   | <span data-ttu-id="db66b-121">El PIN está detenido.</span><span class="sxs-lookup"><span data-stu-id="db66b-121">The pin is stopped.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="db66b-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db66b-122">Remarks</span></span>

<span data-ttu-id="db66b-123">Este método invalida el método [**CBaseInputPin:: CheckStreaming**](cbaseinputpin-checkstreaming.md) .</span><span class="sxs-lookup"><span data-stu-id="db66b-123">This method overrides the [**CBaseInputPin::CheckStreaming**](cbaseinputpin-checkstreaming.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="db66b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db66b-124">Requirements</span></span>



| <span data-ttu-id="db66b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="db66b-125">Requirement</span></span> | <span data-ttu-id="db66b-126">Value</span><span class="sxs-lookup"><span data-stu-id="db66b-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db66b-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db66b-127">Header</span></span><br/>  | <dl> <span data-ttu-id="db66b-128"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="db66b-128"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="db66b-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="db66b-129">Library</span></span><br/> | <dl> <span data-ttu-id="db66b-130"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="db66b-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




