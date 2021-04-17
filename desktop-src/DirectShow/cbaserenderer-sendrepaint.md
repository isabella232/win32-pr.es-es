---
description: El método SendRepaint envía un evento Repaint al administrador de gráficos de filtro.
ms.assetid: 78e5c46c-ca5d-4c5d-9dfc-992ce6b150ad
title: Método CBaseRenderer. SendRepaint (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendRepaint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b3a88f0c1dae54cb5d9be1e4e9ad3e9677bdd958
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671100"
---
# <a name="cbaserenderersendrepaint-method"></a><span data-ttu-id="cee34-103">CBaseRenderer. SendRepaint, método</span><span class="sxs-lookup"><span data-stu-id="cee34-103">CBaseRenderer.SendRepaint method</span></span>

<span data-ttu-id="cee34-104">El `SendRepaint` método envía un evento Repaint al administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="cee34-104">The `SendRepaint` method sends a repaint event to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="cee34-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cee34-105">Syntax</span></span>


```C++
void SendRepaint();
```



## <a name="parameters"></a><span data-ttu-id="cee34-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cee34-106">Parameters</span></span>

<span data-ttu-id="cee34-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="cee34-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cee34-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cee34-108">Return value</span></span>

<span data-ttu-id="cee34-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="cee34-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cee34-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cee34-110">Remarks</span></span>

<span data-ttu-id="cee34-111">Este método envía un [**evento \_ Repaint de EC**](ec-repaint.md) al administrador de gráficos de filtro si se cumplen las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="cee34-111">This method sends an [**EC\_REPAINT**](ec-repaint.md) event to the filter graph manager if the following conditions are true:</span></span>

-   <span data-ttu-id="cee34-112">El PIN de entrada está conectado.</span><span class="sxs-lookup"><span data-stu-id="cee34-112">The input pin is connected.</span></span>
-   <span data-ttu-id="cee34-113">El filtro no está vaciando datos.</span><span class="sxs-lookup"><span data-stu-id="cee34-113">The filter is not flushing data.</span></span>
-   <span data-ttu-id="cee34-114">No se ha alcanzado el final de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="cee34-114">The end-of-stream was not reached.</span></span>
-   <span data-ttu-id="cee34-115">La marca [**CBaseRenderer:: m \_ BAbort**](cbaserenderer-m-babort.md) es **false**.</span><span class="sxs-lookup"><span data-stu-id="cee34-115">The [**CBaseRenderer::m\_bAbort**](cbaserenderer-m-babort.md) flag is **FALSE**.</span></span>
-   <span data-ttu-id="cee34-116">La marca [**CBaseRenderer:: m \_ BRepaintStatus**](cbaserenderer-m-brepaintstatus.md) es **true**.</span><span class="sxs-lookup"><span data-stu-id="cee34-116">The [**CBaseRenderer::m\_bRepaintStatus**](cbaserenderer-m-brepaintstatus.md) flag is **TRUE**.</span></span>

<span data-ttu-id="cee34-117">Dependiendo del estado del gráfico, el \_ evento de Repaint de EC puede hacer que el filtro de nivel superior vuelva a enviar una muestra, el gráfico de filtro para buscar en su ubicación actual o el administrador de gráficos de filtro para que se PAUSE momentáneamente.</span><span class="sxs-lookup"><span data-stu-id="cee34-117">Depending on the state of the graph, the EC\_REPAINT event can cause the upstream filter to re-send a sample; the filter graph to seek to its current location; or the filter graph manager to pause momentarily.</span></span> <span data-ttu-id="cee34-118">(Consulte [**EC \_ Repaint**](ec-repaint.md)). Este evento es potencialmente ineficaz, por lo que debe usarse con moderación.</span><span class="sxs-lookup"><span data-stu-id="cee34-118">(See [**EC\_REPAINT**](ec-repaint.md).) This event is potentially inefficient, so it should be used sparingly.</span></span> <span data-ttu-id="cee34-119">Sin embargo, en ocasiones, los representadores de vídeo necesitan actualizar la pantalla.</span><span class="sxs-lookup"><span data-stu-id="cee34-119">However, video renderers sometimes need to refresh the display.</span></span>

## <a name="requirements"></a><span data-ttu-id="cee34-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cee34-120">Requirements</span></span>



| <span data-ttu-id="cee34-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="cee34-121">Requirement</span></span> | <span data-ttu-id="cee34-122">Value</span><span class="sxs-lookup"><span data-stu-id="cee34-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cee34-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cee34-123">Header</span></span><br/>  | <dl> <span data-ttu-id="cee34-124"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cee34-124"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cee34-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cee34-125">Library</span></span><br/> | <dl> <span data-ttu-id="cee34-126"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="cee34-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cee34-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="cee34-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cee34-128">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="cee34-128">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




