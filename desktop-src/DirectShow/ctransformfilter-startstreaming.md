---
description: Se llama al método StartStreaming cuando el filtro cambia al estado de pausa.
ms.assetid: 1e3bbca7-b5b1-41fd-8f70-b7ef39c9491b
title: Método CTransformFilter. StartStreaming (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 50df2db2aada7f96744af5e553f474818594d399
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661022"
---
# <a name="ctransformfilterstartstreaming-method"></a><span data-ttu-id="6cbb8-103">CTransformFilter. StartStreaming, método</span><span class="sxs-lookup"><span data-stu-id="6cbb8-103">CTransformFilter.StartStreaming method</span></span>

<span data-ttu-id="6cbb8-104">`StartStreaming`Se llama al método cuando el filtro cambia al estado de pausa.</span><span class="sxs-lookup"><span data-stu-id="6cbb8-104">The `StartStreaming` method is called when the filter switches to the paused state.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cbb8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6cbb8-105">Syntax</span></span>


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a><span data-ttu-id="6cbb8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6cbb8-106">Parameters</span></span>

<span data-ttu-id="6cbb8-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="6cbb8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6cbb8-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6cbb8-108">Return value</span></span>

<span data-ttu-id="6cbb8-109">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="6cbb8-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cbb8-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6cbb8-110">Remarks</span></span>

<span data-ttu-id="6cbb8-111">Este método no hace nada en la clase base, pero la clase derivada puede invalidarlo.</span><span class="sxs-lookup"><span data-stu-id="6cbb8-111">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cbb8-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cbb8-112">Requirements</span></span>



| <span data-ttu-id="6cbb8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cbb8-113">Requirement</span></span> | <span data-ttu-id="6cbb8-114">Value</span><span class="sxs-lookup"><span data-stu-id="6cbb8-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cbb8-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6cbb8-115">Header</span></span><br/>  | <dl> <span data-ttu-id="6cbb8-116"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6cbb8-116"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6cbb8-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6cbb8-117">Library</span></span><br/> | <dl> <span data-ttu-id="6cbb8-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="6cbb8-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cbb8-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="6cbb8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cbb8-120">**Clase CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="6cbb8-120">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




