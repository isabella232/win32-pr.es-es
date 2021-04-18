---
description: Se llama al método StopStreaming cuando el filtro cambia al estado Stopped.
ms.assetid: cfebfed2-4105-4dea-8d47-60d6160ee337
title: Método CTransformFilter. StopStreaming (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.StopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4990b55ad87a4eb754af7101e762ce227a090993
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660887"
---
# <a name="ctransformfilterstopstreaming-method"></a><span data-ttu-id="34165-103">CTransformFilter. StopStreaming, método</span><span class="sxs-lookup"><span data-stu-id="34165-103">CTransformFilter.StopStreaming method</span></span>

<span data-ttu-id="34165-104">`StopStreaming`Se llama al método cuando el filtro cambia al estado Stopped.</span><span class="sxs-lookup"><span data-stu-id="34165-104">The `StopStreaming` method is called when the filter switches to the stopped state.</span></span>

## <a name="syntax"></a><span data-ttu-id="34165-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="34165-105">Syntax</span></span>


```C++
virtual HRESULT StopStreaming();
```



## <a name="parameters"></a><span data-ttu-id="34165-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="34165-106">Parameters</span></span>

<span data-ttu-id="34165-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="34165-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="34165-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="34165-108">Return value</span></span>

<span data-ttu-id="34165-109">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="34165-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="34165-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="34165-110">Remarks</span></span>

<span data-ttu-id="34165-111">Este método no hace nada en la clase base, pero la clase derivada puede invalidarlo.</span><span class="sxs-lookup"><span data-stu-id="34165-111">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="34165-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34165-112">Requirements</span></span>



| <span data-ttu-id="34165-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="34165-113">Requirement</span></span> | <span data-ttu-id="34165-114">Value</span><span class="sxs-lookup"><span data-stu-id="34165-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34165-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="34165-115">Header</span></span><br/>  | <dl> <span data-ttu-id="34165-116"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34165-116"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="34165-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="34165-117">Library</span></span><br/> | <dl> <span data-ttu-id="34165-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="34165-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34165-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="34165-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34165-120">**Clase CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="34165-120">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




