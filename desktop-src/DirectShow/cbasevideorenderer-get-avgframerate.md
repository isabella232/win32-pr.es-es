---
description: El \_ método get AvgFrameRate calcula y recupera la velocidad media de fotogramas obtenida.
ms.assetid: f36fc020-8c1a-491f-9f55-18265fde8bf8
title: Método CBaseVideoRenderer.get_AvgFrameRate (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_AvgFrameRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56d8fff53f3d56676805eca9029670d51210ef2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661066"
---
# <a name="cbasevideorendererget_avgframerate-method"></a><span data-ttu-id="84a27-103">CBaseVideoRenderer. Get \_ AvgFrameRate (método)</span><span class="sxs-lookup"><span data-stu-id="84a27-103">CBaseVideoRenderer.get\_AvgFrameRate method</span></span>

<span data-ttu-id="84a27-104">El `get_AvgFrameRate` método calcula y recupera la velocidad media de fotogramas obtenida.</span><span class="sxs-lookup"><span data-stu-id="84a27-104">The `get_AvgFrameRate` method calculates and retrieves the average frame rate achieved.</span></span>

## <a name="syntax"></a><span data-ttu-id="84a27-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84a27-105">Syntax</span></span>


```C++
HRESULT get_AvgFrameRate(
   int *piAvgFrameRate
);
```



## <a name="parameters"></a><span data-ttu-id="84a27-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="84a27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84a27-107">*piAvgFrameRate*</span><span class="sxs-lookup"><span data-stu-id="84a27-107">*piAvgFrameRate*</span></span> 
</dt> <dd>

<span data-ttu-id="84a27-108">Puntero al número de fotogramas por segundo desde que comenzó la transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="84a27-108">Pointer to the number of frames per second since streaming began.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84a27-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="84a27-109">Return value</span></span>

<span data-ttu-id="84a27-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="84a27-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="84a27-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="84a27-111">Remarks</span></span>

<span data-ttu-id="84a27-112">Esta función miembro implementa el método [**IQualProp:: get \_ AvgFrameRate**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgframerate) .</span><span class="sxs-lookup"><span data-stu-id="84a27-112">This member function implements the [**IQualProp::get\_AvgFrameRate**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgframerate) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="84a27-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84a27-113">Requirements</span></span>



| <span data-ttu-id="84a27-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="84a27-114">Requirement</span></span> | <span data-ttu-id="84a27-115">Value</span><span class="sxs-lookup"><span data-stu-id="84a27-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84a27-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="84a27-116">Header</span></span><br/>  | <dl> <span data-ttu-id="84a27-117"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="84a27-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="84a27-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="84a27-118">Library</span></span><br/> | <dl> <span data-ttu-id="84a27-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="84a27-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84a27-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="84a27-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84a27-121">**Clase CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="84a27-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




