---
description: 'El método SetPreroll especifica si este ejemplo es un ejemplo de relanzamiento. No se debe mostrar un ejemplo de prelanzamiento. Este método implementa el método IMediaSample:: SetPreroll.'
ms.assetid: 2887e627-5999-407a-88d3-811c803c9a43
title: Método CMediaSample. SetPreroll (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 594f26ebb738a986c85a14b88f8896b122b58f47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679072"
---
# <a name="cmediasamplesetpreroll-method"></a><span data-ttu-id="ca583-105">CMediaSample. SetPreroll, método</span><span class="sxs-lookup"><span data-stu-id="ca583-105">CMediaSample.SetPreroll method</span></span>

<span data-ttu-id="ca583-106">El `SetPreroll` método especifica si este ejemplo es un ejemplo de relanzamiento.</span><span class="sxs-lookup"><span data-stu-id="ca583-106">The `SetPreroll` method specifies whether this sample is a preroll sample.</span></span> <span data-ttu-id="ca583-107">No se debe mostrar un ejemplo de prelanzamiento.</span><span class="sxs-lookup"><span data-stu-id="ca583-107">A preroll sample should not be displayed.</span></span> <span data-ttu-id="ca583-108">Este método implementa el método [**IMediaSample:: SetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setpreroll) .</span><span class="sxs-lookup"><span data-stu-id="ca583-108">This method implements the [**IMediaSample::SetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setpreroll) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca583-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ca583-109">Syntax</span></span>


```C++
HRESULT SetPreroll(
   BOOL bIsPreroll
);
```



## <a name="parameters"></a><span data-ttu-id="ca583-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ca583-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca583-111">*bIsPreroll*</span><span class="sxs-lookup"><span data-stu-id="ca583-111">*bIsPreroll*</span></span> 
</dt> <dd>

<span data-ttu-id="ca583-112">Valor booleano que especifica si se trata de un ejemplo de relanzamiento.</span><span class="sxs-lookup"><span data-stu-id="ca583-112">Boolean value that specifies whether this is a preroll sample.</span></span> <span data-ttu-id="ca583-113">Si es **true**, se trata de un ejemplo de relanzamiento.</span><span class="sxs-lookup"><span data-stu-id="ca583-113">If **TRUE**, this is a preroll sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca583-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ca583-114">Return value</span></span>

<span data-ttu-id="ca583-115">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="ca583-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca583-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ca583-116">Remarks</span></span>

<span data-ttu-id="ca583-117">Este método actualiza la variable miembro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) , que especifica la propiedad preroll.</span><span class="sxs-lookup"><span data-stu-id="ca583-117">This method updates the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies the preroll property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca583-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca583-118">Requirements</span></span>



| <span data-ttu-id="ca583-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca583-119">Requirement</span></span> | <span data-ttu-id="ca583-120">Value</span><span class="sxs-lookup"><span data-stu-id="ca583-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca583-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ca583-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ca583-122"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca583-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ca583-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ca583-123">Library</span></span><br/> | <dl> <span data-ttu-id="ca583-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ca583-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca583-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca583-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca583-126">**Clase CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="ca583-126">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




