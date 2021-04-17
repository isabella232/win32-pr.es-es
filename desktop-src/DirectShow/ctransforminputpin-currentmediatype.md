---
description: El método CurrentMediaType recupera el tipo de medio para la conexión del PIN actual.
ms.assetid: d46f4d8e-9e9d-49d3-b823-f2f0fcf25383
title: Método CTransformInputPin. CurrentMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CurrentMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 59feca88e896b2a81a352b693e57ceaa5388d452
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680338"
---
# <a name="ctransforminputpincurrentmediatype-method"></a><span data-ttu-id="104e4-103">CTransformInputPin. CurrentMediaType, método</span><span class="sxs-lookup"><span data-stu-id="104e4-103">CTransformInputPin.CurrentMediaType method</span></span>

<span data-ttu-id="104e4-104">El `CurrentMediaType` método recupera el tipo de medio para la conexión del PIN actual.</span><span class="sxs-lookup"><span data-stu-id="104e4-104">The `CurrentMediaType` method retrieves the media type for the current pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="104e4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="104e4-105">Syntax</span></span>


```C++
CMediaType& CurrentMediaType();
```



## <a name="parameters"></a><span data-ttu-id="104e4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="104e4-106">Parameters</span></span>

<span data-ttu-id="104e4-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="104e4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="104e4-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="104e4-108">Return value</span></span>

<span data-ttu-id="104e4-109">Devuelve una referencia a la variable miembro [**CBasePin:: m \_ MT**](cbasepin-m-mt.md) .</span><span class="sxs-lookup"><span data-stu-id="104e4-109">Returns a reference to the [**CBasePin::m\_mt**](cbasepin-m-mt.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="104e4-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="104e4-110">Requirements</span></span>



| <span data-ttu-id="104e4-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="104e4-111">Requirement</span></span> | <span data-ttu-id="104e4-112">Value</span><span class="sxs-lookup"><span data-stu-id="104e4-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="104e4-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="104e4-113">Header</span></span><br/>  | <dl> <span data-ttu-id="104e4-114"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="104e4-114"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="104e4-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="104e4-115">Library</span></span><br/> | <dl> <span data-ttu-id="104e4-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="104e4-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




