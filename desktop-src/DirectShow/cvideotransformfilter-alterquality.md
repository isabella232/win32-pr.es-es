---
description: 'El método AlterQuality notifica al filtro que se ha solicitado un cambio de calidad. Este método invalida el método CTransformFilter:: AlterQuality.'
ms.assetid: 9a1d1379-8557-4b33-ab49-b5c6a684f685
title: Método CVideoTransformFilter. AlterQuality (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.AlterQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1de0985b8cb3a8db6f45c247e717042cf344655f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660125"
---
# <a name="cvideotransformfilteralterquality-method"></a><span data-ttu-id="b3bc1-104">CVideoTransformFilter. AlterQuality, método</span><span class="sxs-lookup"><span data-stu-id="b3bc1-104">CVideoTransformFilter.AlterQuality method</span></span>

<span data-ttu-id="b3bc1-105">El `AlterQuality` método notifica al filtro que se ha solicitado un cambio de calidad.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-105">The `AlterQuality` method notifies the filter that a quality change is requested.</span></span> <span data-ttu-id="b3bc1-106">Este método invalida el método [**CTransformFilter:: AlterQuality**](ctransformfilter-alterquality.md) .</span><span class="sxs-lookup"><span data-stu-id="b3bc1-106">This method overrides the [**CTransformFilter::AlterQuality**](ctransformfilter-alterquality.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3bc1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3bc1-107">Syntax</span></span>


```C++
virtual HRESULT AlterQuality(
   Quality q
);
```



## <a name="parameters"></a><span data-ttu-id="b3bc1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3bc1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3bc1-109">*respuestas*</span><span class="sxs-lookup"><span data-stu-id="b3bc1-109">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="b3bc1-110">Estructura de [**calidad**](/windows/win32/api/strmif/ns-strmif-quality) que contiene el mensaje de control de calidad.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-110">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3bc1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3bc1-111">Return value</span></span>

<span data-ttu-id="b3bc1-112">Devuelve E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-112">Returns E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3bc1-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3bc1-113">Remarks</span></span>

<span data-ttu-id="b3bc1-114">Se llama a este método cuando el PIN de salida recibe un mensaje de calidad (a través del método [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) ).</span><span class="sxs-lookup"><span data-stu-id="b3bc1-114">This method is called when the output pin receives a quality message (through the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method).</span></span>

<span data-ttu-id="b3bc1-115">El valor de retraso de *q* se almacena en la variable de miembro **m \_ itrLate** .</span><span class="sxs-lookup"><span data-stu-id="b3bc1-115">The lateness value from *q* is stored in the **m\_itrLate** member variable.</span></span> <span data-ttu-id="b3bc1-116">El valor devuelto de E \_ FAIL indica que el representador debe ponerse al día soltando fotogramas, aunque la clase **CVideoTransformFilter** también quitará los fotogramas en las condiciones correctas.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-116">The return value of E\_FAIL indicates that the renderer should catch up by dropping frames, although the **CVideoTransformFilter** class will also drop frames under the right conditions.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3bc1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3bc1-117">Requirements</span></span>



| <span data-ttu-id="b3bc1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3bc1-118">Requirement</span></span> | <span data-ttu-id="b3bc1-119">Value</span><span class="sxs-lookup"><span data-stu-id="b3bc1-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3bc1-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3bc1-120">Header</span></span><br/>  | <dl> <span data-ttu-id="b3bc1-121"><dt>Vtrans. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b3bc1-121"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b3bc1-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b3bc1-122">Library</span></span><br/> | <dl> <span data-ttu-id="b3bc1-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b3bc1-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3bc1-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3bc1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3bc1-125">**Clase CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="b3bc1-125">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> <dt>

[<span data-ttu-id="b3bc1-126">**CVideoTransformFilter::ShouldSkipFrame**</span><span class="sxs-lookup"><span data-stu-id="b3bc1-126">**CVideoTransformFilter::ShouldSkipFrame**</span></span>](cvideotransformfilter-shouldskipframe.md)
</dt> </dl>

 

 




