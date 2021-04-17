---
description: El método DoRenderSample representa un ejemplo.
ms.assetid: cf06192c-44c0-4d88-a20e-6501ea48cbfd
title: Método CBaseRenderer. DoRenderSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.DoRenderSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 935fd7b92cef5d51056b2eb2daa9d2fb775647b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660755"
---
# <a name="cbaserendererdorendersample-method"></a><span data-ttu-id="faf1c-103">CBaseRenderer. DoRenderSample, método</span><span class="sxs-lookup"><span data-stu-id="faf1c-103">CBaseRenderer.DoRenderSample method</span></span>

<span data-ttu-id="faf1c-104">El `DoRenderSample` método representa un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="faf1c-104">The `DoRenderSample` method renders a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="faf1c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="faf1c-105">Syntax</span></span>


```C++
virtual HRESULT DoRenderSample(
   IMediaSample *pMediaSample
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="faf1c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="faf1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="faf1c-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="faf1c-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="faf1c-108">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="faf1c-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="faf1c-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="faf1c-109">Return value</span></span>

<span data-ttu-id="faf1c-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="faf1c-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="faf1c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="faf1c-111">Remarks</span></span>

<span data-ttu-id="faf1c-112">La clase derivada debe implementar este método.</span><span class="sxs-lookup"><span data-stu-id="faf1c-112">The derived class must implement this method.</span></span> <span data-ttu-id="faf1c-113">El comportamiento depende por completo del tipo de filtro que se está implementando.</span><span class="sxs-lookup"><span data-stu-id="faf1c-113">The behavior depends entirely on the type of filter being implemented.</span></span> <span data-ttu-id="faf1c-114">Un representador de vídeo, por ejemplo, dibujaría la imagen de vídeo incluida en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="faf1c-114">A video renderer, for example, would draw the video image contained in the sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="faf1c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="faf1c-115">Requirements</span></span>



| <span data-ttu-id="faf1c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="faf1c-116">Requirement</span></span> | <span data-ttu-id="faf1c-117">Value</span><span class="sxs-lookup"><span data-stu-id="faf1c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="faf1c-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="faf1c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="faf1c-119"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="faf1c-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="faf1c-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="faf1c-120">Library</span></span><br/> | <dl> <span data-ttu-id="faf1c-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="faf1c-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faf1c-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="faf1c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faf1c-123">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="faf1c-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




