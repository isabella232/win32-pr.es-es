---
description: El método IncrementTypeVersion incrementa el número de versión en el conjunto de tipos de medios preferidos.
ms.assetid: 30cad0ae-58e7-47f6-94ee-75e24ce0a7e9
title: Método CBasePin. IncrementTypeVersion (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IncrementTypeVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6db3c08972bebbaf1172c44412ae9c8652100da8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661255"
---
# <a name="cbasepinincrementtypeversion-method"></a><span data-ttu-id="22994-103">CBasePin. IncrementTypeVersion, método</span><span class="sxs-lookup"><span data-stu-id="22994-103">CBasePin.IncrementTypeVersion method</span></span>

<span data-ttu-id="22994-104">El `IncrementTypeVersion` método incrementa el número de versión en el conjunto de tipos de medios preferidos.</span><span class="sxs-lookup"><span data-stu-id="22994-104">The `IncrementTypeVersion` method increments the version number on the set of preferred media types.</span></span>

## <a name="syntax"></a><span data-ttu-id="22994-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22994-105">Syntax</span></span>


```C++
void IncrementTypeVersion();
```



## <a name="parameters"></a><span data-ttu-id="22994-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22994-106">Parameters</span></span>

<span data-ttu-id="22994-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="22994-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="22994-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22994-108">Return value</span></span>

<span data-ttu-id="22994-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="22994-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="22994-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="22994-110">Remarks</span></span>

<span data-ttu-id="22994-111">Este método incrementa la variable miembro [**CBasePin:: m \_ TypeVersion**](cbasepin-m-typeversion.md) .</span><span class="sxs-lookup"><span data-stu-id="22994-111">This method increments the [**CBasePin::m\_TypeVersion**](cbasepin-m-typeversion.md) member variable.</span></span> <span data-ttu-id="22994-112">Si el PIN cambia dinámicamente la lista de tipos de medios preferidos, llame a este método cada vez que cambie la lista.</span><span class="sxs-lookup"><span data-stu-id="22994-112">If the pin dynamically changes the list of preferred media types, call this method whenever the list changes.</span></span> <span data-ttu-id="22994-113">Para obtener más información, vea [**CBasePin:: GetMediaTypeVersion**](cbasepin-getmediatypeversion.md).</span><span class="sxs-lookup"><span data-stu-id="22994-113">For more information, see [**CBasePin::GetMediaTypeVersion**](cbasepin-getmediatypeversion.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="22994-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22994-114">Requirements</span></span>



| <span data-ttu-id="22994-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="22994-115">Requirement</span></span> | <span data-ttu-id="22994-116">Value</span><span class="sxs-lookup"><span data-stu-id="22994-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22994-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22994-117">Header</span></span><br/>  | <dl> <span data-ttu-id="22994-118"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="22994-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="22994-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="22994-119">Library</span></span><br/> | <dl> <span data-ttu-id="22994-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="22994-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22994-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="22994-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22994-122">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="22994-122">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




