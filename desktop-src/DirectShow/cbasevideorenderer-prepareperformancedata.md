---
description: El método PreparePerformanceData establece los \_ valores m trLate y m \_ trFrame del marco actual.
ms.assetid: c4c5701b-eccd-4259-a1d1-7c5000f6b2df
title: Método CBaseVideoRenderer. PreparePerformanceData (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.PreparePerformanceData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 12dd61dee7416ce8ca7ac07cba62cbc769df5973
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660244"
---
# <a name="cbasevideorendererprepareperformancedata-method"></a><span data-ttu-id="995e3-103">CBaseVideoRenderer. PreparePerformanceData, método</span><span class="sxs-lookup"><span data-stu-id="995e3-103">CBaseVideoRenderer.PreparePerformanceData method</span></span>

<span data-ttu-id="995e3-104">El `PreparePerformanceData` método establece los valores **m \_ trLate** y **m \_ trFrame** del marco actual.</span><span class="sxs-lookup"><span data-stu-id="995e3-104">The `PreparePerformanceData` method sets the **m\_trLate** and **m\_trFrame** values of the current frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="995e3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="995e3-105">Syntax</span></span>


```C++
void PreparePerformanceData(
   int trLate,
   int trFrame
);
```



## <a name="parameters"></a><span data-ttu-id="995e3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="995e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="995e3-107">*trLate*</span><span class="sxs-lookup"><span data-stu-id="995e3-107">*trLate*</span></span> 
</dt> <dd>

<span data-ttu-id="995e3-108">Valor que indica el retraso de la muestra más allá de su tiempo de espera, en unidades de tiempo de referencia.</span><span class="sxs-lookup"><span data-stu-id="995e3-108">Value indicating how late the sample was beyond its due time, in reference time units.</span></span>

</dd> <dt>

<span data-ttu-id="995e3-109">*trFrame*</span><span class="sxs-lookup"><span data-stu-id="995e3-109">*trFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="995e3-110">Tiempo de INTERMARCO, en unidades de tiempo de referencia.</span><span class="sxs-lookup"><span data-stu-id="995e3-110">Interframe time, in reference time units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="995e3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="995e3-111">Return value</span></span>

<span data-ttu-id="995e3-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="995e3-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="995e3-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="995e3-113">Remarks</span></span>

<span data-ttu-id="995e3-114">Esta función miembro establece **m \_ trLate** en el valor de *trLate* y **m \_ trFrame** en el valor de *trFrame*.</span><span class="sxs-lookup"><span data-stu-id="995e3-114">This member function sets **m\_trLate** to the value of *trLate* and **m\_trFrame** to the value of *trFrame*.</span></span>

<span data-ttu-id="995e3-115">Cuando se llama a la función miembro [**CBaseVideoRenderer:: RecordFrameLateness**](cbasevideorenderer-recordframelateness.md) desde [**CBaseVideoRenderer:: OnRenderStart**](cbasevideorenderer-onrenderstart.md) o [**CBaseVideoRenderer:: OnDirectRender**](cbasevideorenderer-ondirectrender.md), pasa los valores de **m \_ trLate** y **m \_ trFrame** para que actualice las estadísticas.</span><span class="sxs-lookup"><span data-stu-id="995e3-115">When the [**CBaseVideoRenderer::RecordFrameLateness**](cbasevideorenderer-recordframelateness.md) member function is called from either [**CBaseVideoRenderer::OnRenderStart**](cbasevideorenderer-onrenderstart.md) or [**CBaseVideoRenderer::OnDirectRender**](cbasevideorenderer-ondirectrender.md), it passes the values of **m\_trLate** and **m\_trFrame** for it to update the statistics.</span></span> <span data-ttu-id="995e3-116">`PreparePerformanceData` se llama desde [**CBaseVideoRenderer:: OnWaitEnd**](cbasevideorenderer-onwaitend.md) para establecer estos valores de miembro de datos.</span><span class="sxs-lookup"><span data-stu-id="995e3-116">`PreparePerformanceData` is called from [**CBaseVideoRenderer::OnWaitEnd**](cbasevideorenderer-onwaitend.md) to set these data member values.</span></span>

## <a name="requirements"></a><span data-ttu-id="995e3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="995e3-117">Requirements</span></span>



| <span data-ttu-id="995e3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="995e3-118">Requirement</span></span> | <span data-ttu-id="995e3-119">Value</span><span class="sxs-lookup"><span data-stu-id="995e3-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="995e3-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="995e3-120">Header</span></span><br/>  | <dl> <span data-ttu-id="995e3-121"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="995e3-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="995e3-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="995e3-122">Library</span></span><br/> | <dl> <span data-ttu-id="995e3-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="995e3-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="995e3-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="995e3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="995e3-125">**Clase CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="995e3-125">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




