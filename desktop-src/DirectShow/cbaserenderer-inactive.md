---
description: Se llama al método Inactive cuando el estado se cambia a Stopped.
ms.assetid: 2bad81ef-d2a4-4c20-a49b-e40e5097b430
title: Método CBaseRenderer. Inactive (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ac328c772b740a0d7ab05be4c6ea9f2a24f852e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670647"
---
# <a name="cbaserendererinactive-method"></a><span data-ttu-id="2fcca-103">CBaseRenderer. Inactive (método)</span><span class="sxs-lookup"><span data-stu-id="2fcca-103">CBaseRenderer.Inactive method</span></span>

<span data-ttu-id="2fcca-104">`Inactive`Se llama al método cuando el estado se cambia a detenido.</span><span class="sxs-lookup"><span data-stu-id="2fcca-104">The `Inactive` method is called when the state is switched to stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fcca-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2fcca-105">Syntax</span></span>


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="2fcca-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2fcca-106">Parameters</span></span>

<span data-ttu-id="2fcca-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2fcca-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2fcca-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2fcca-108">Return value</span></span>

<span data-ttu-id="2fcca-109">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="2fcca-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fcca-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2fcca-110">Remarks</span></span>

<span data-ttu-id="2fcca-111">El PIN de entrada llama a este método desde su propio método [**CRendererInputPin:: Inactive**](crendererinputpin-inactive.md) .</span><span class="sxs-lookup"><span data-stu-id="2fcca-111">The input pin calls this method from its own [**CRendererInputPin::Inactive**](crendererinputpin-inactive.md) method.</span></span> <span data-ttu-id="2fcca-112">El filtro llama al método [**CBaseRenderer:: ClearPendingSample**](cbaserenderer-clearpendingsample.md) para liberar el ejemplo más reciente.</span><span class="sxs-lookup"><span data-stu-id="2fcca-112">The filter calls the [**CBaseRenderer::ClearPendingSample**](cbaserenderer-clearpendingsample.md) method to release the most recent sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fcca-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fcca-113">Requirements</span></span>



| <span data-ttu-id="2fcca-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fcca-114">Requirement</span></span> | <span data-ttu-id="2fcca-115">Value</span><span class="sxs-lookup"><span data-stu-id="2fcca-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fcca-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2fcca-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2fcca-117"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2fcca-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2fcca-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2fcca-118">Library</span></span><br/> | <dl> <span data-ttu-id="2fcca-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2fcca-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fcca-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="2fcca-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fcca-121">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="2fcca-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




