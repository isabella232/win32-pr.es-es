---
description: Consulta si el asignador usa ejemplos de medios de solo lectura.
ms.assetid: 2cb692da-f030-4265-afe4-b1608b51fd47
title: Método CBaseInputPin. IsReadOnly (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.IsReadOnly
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93d1e7930631328a277ce7332f483ee264b2d525
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661012"
---
# <a name="cbaseinputpinisreadonly-method"></a><span data-ttu-id="487a2-103">CBaseInputPin. IsReadOnly (método)</span><span class="sxs-lookup"><span data-stu-id="487a2-103">CBaseInputPin.IsReadOnly method</span></span>

<span data-ttu-id="487a2-104">Consulta si el asignador usa ejemplos de medios de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="487a2-104">Queries whether the allocator uses read-only media samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="487a2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="487a2-105">Syntax</span></span>


```C++
BOOL IsReadOnly();
```



## <a name="parameters"></a><span data-ttu-id="487a2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="487a2-106">Parameters</span></span>

<span data-ttu-id="487a2-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="487a2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="487a2-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="487a2-108">Return value</span></span>

<span data-ttu-id="487a2-109">Devuelve el valor de la variable miembro [**CBaseInputPin:: m \_ bReadOnly**](cbaseinputpin-m-breadonly.md) .</span><span class="sxs-lookup"><span data-stu-id="487a2-109">Returns the value of the [**CBaseInputPin::m\_bReadOnly**](cbaseinputpin-m-breadonly.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="487a2-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="487a2-110">Requirements</span></span>



| <span data-ttu-id="487a2-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="487a2-111">Requirement</span></span> | <span data-ttu-id="487a2-112">Value</span><span class="sxs-lookup"><span data-stu-id="487a2-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="487a2-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="487a2-113">Header</span></span><br/>  | <dl> <span data-ttu-id="487a2-114"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="487a2-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="487a2-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="487a2-115">Library</span></span><br/> | <dl> <span data-ttu-id="487a2-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="487a2-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="487a2-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="487a2-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="487a2-118">**Clase CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="487a2-118">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




