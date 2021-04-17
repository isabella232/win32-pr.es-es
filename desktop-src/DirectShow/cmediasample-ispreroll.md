---
description: 'El método IsPreroll determina si este ejemplo es un ejemplo de relanzamiento. No se debe mostrar un ejemplo de prelanzamiento. Este método implementa el método IMediaSample:: IsPreroll.'
ms.assetid: fbcf7aab-473c-49c1-9a8f-4a619f4e28f4
title: Método CMediaSample. IsPreroll (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b40cf8fd6a1adb5186309f47da0f0ae3dc30412a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670473"
---
# <a name="cmediasampleispreroll-method"></a><span data-ttu-id="b4771-105">CMediaSample. IsPreroll, método</span><span class="sxs-lookup"><span data-stu-id="b4771-105">CMediaSample.IsPreroll method</span></span>

<span data-ttu-id="b4771-106">El `IsPreroll` método determina si este ejemplo es un ejemplo de relanzamiento.</span><span class="sxs-lookup"><span data-stu-id="b4771-106">The `IsPreroll` method determines if this sample is a preroll sample.</span></span> <span data-ttu-id="b4771-107">No se debe mostrar un ejemplo de prelanzamiento.</span><span class="sxs-lookup"><span data-stu-id="b4771-107">A preroll sample should not be displayed.</span></span> <span data-ttu-id="b4771-108">Este método implementa el método [**IMediaSample:: IsPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-ispreroll) .</span><span class="sxs-lookup"><span data-stu-id="b4771-108">This method implements the [**IMediaSample::IsPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-ispreroll) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4771-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4771-109">Syntax</span></span>


```C++
HRESULT IsPreroll();
```



## <a name="parameters"></a><span data-ttu-id="b4771-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b4771-110">Parameters</span></span>

<span data-ttu-id="b4771-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b4771-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b4771-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b4771-112">Return value</span></span>

<span data-ttu-id="b4771-113">Devuelve S \_ OK si el ejemplo es un ejemplo de relanzamiento y S \_ false en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b4771-113">Returns S\_OK if the sample is a preroll sample, and S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4771-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b4771-114">Remarks</span></span>

<span data-ttu-id="b4771-115">La variable miembro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) especifica esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="b4771-115">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4771-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4771-116">Requirements</span></span>



| <span data-ttu-id="b4771-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4771-117">Requirement</span></span> | <span data-ttu-id="b4771-118">Value</span><span class="sxs-lookup"><span data-stu-id="b4771-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4771-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b4771-119">Header</span></span><br/>  | <dl> <span data-ttu-id="b4771-120"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b4771-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b4771-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b4771-121">Library</span></span><br/> | <dl> <span data-ttu-id="b4771-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b4771-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4771-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4771-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4771-124">**Clase CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="b4771-124">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




