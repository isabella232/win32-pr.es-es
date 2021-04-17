---
description: El \_ método get vibración recupera la desviación estándar de tiempo en milisegundos entre cada fotograma y el siguiente para todos los fotogramas desde que se inició el streaming.
ms.assetid: 629e725e-7dee-4824-8f79-cd3335f4901b
title: Método CBaseVideoRenderer.get_Jitter (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_Jitter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef39cdb1b7a77dab22db9728268bf7b23b9fcefb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679303"
---
# <a name="cbasevideorendererget_jitter-method"></a><span data-ttu-id="543eb-103">CBaseVideoRenderer. Get \_ vibración (método)</span><span class="sxs-lookup"><span data-stu-id="543eb-103">CBaseVideoRenderer.get\_Jitter method</span></span>

<span data-ttu-id="543eb-104">El `get_Jitter` método recupera la desviación estándar de tiempo en milisegundos entre cada fotograma y el siguiente para todos los fotogramas desde que se inició el streaming.</span><span class="sxs-lookup"><span data-stu-id="543eb-104">The `get_Jitter` method retrieves the standard deviation of time in milliseconds between each frame and the next for all frames since streaming started.</span></span>

## <a name="syntax"></a><span data-ttu-id="543eb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="543eb-105">Syntax</span></span>


```C++
HRESULT get_Jitter(
   int *piJitter
);
```



## <a name="parameters"></a><span data-ttu-id="543eb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="543eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="543eb-107">*piJitter*</span><span class="sxs-lookup"><span data-stu-id="543eb-107">*piJitter*</span></span> 
</dt> <dd>

<span data-ttu-id="543eb-108">Puntero a la desviación estándar del tiempo de INTERMARCO, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="543eb-108">Pointer to the standard deviation of the interframe time, in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="543eb-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="543eb-109">Return value</span></span>

<span data-ttu-id="543eb-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="543eb-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="543eb-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="543eb-111">Remarks</span></span>

<span data-ttu-id="543eb-112">Esta función miembro implementa el método [**IQualProp:: get \_ vibración**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_jitter) .</span><span class="sxs-lookup"><span data-stu-id="543eb-112">This member function implements the [**IQualProp::get\_Jitter**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_jitter) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="543eb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="543eb-113">Requirements</span></span>



| <span data-ttu-id="543eb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="543eb-114">Requirement</span></span> | <span data-ttu-id="543eb-115">Value</span><span class="sxs-lookup"><span data-stu-id="543eb-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="543eb-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="543eb-116">Header</span></span><br/>  | <dl> <span data-ttu-id="543eb-117"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="543eb-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="543eb-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="543eb-118">Library</span></span><br/> | <dl> <span data-ttu-id="543eb-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="543eb-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="543eb-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="543eb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="543eb-121">**Clase CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="543eb-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




