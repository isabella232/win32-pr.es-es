---
description: El método ScaleSourceRect escala un rectángulo, si hay una diferencia entre el tamaño de vídeo nativo y el formato de tipo de medio.
ms.assetid: 7bd4d555-5782-4ce5-9f0d-928b199ef897
title: Método CDrawImage. ScaleSourceRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.ScaleSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9800f405c0002fb58ca68ebd2369eb068f6319a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670532"
---
# <a name="cdrawimagescalesourcerect-method"></a><span data-ttu-id="c9c7a-103">CDrawImage. ScaleSourceRect, método</span><span class="sxs-lookup"><span data-stu-id="c9c7a-103">CDrawImage.ScaleSourceRect method</span></span>

<span data-ttu-id="c9c7a-104">El `ScaleSourceRect` método escala un rectángulo, si hay una diferencia entre el tamaño de vídeo nativo y el formato de tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="c9c7a-104">The `ScaleSourceRect` method scales a rectangle, if there is a difference between the native video size and the media type format.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9c7a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9c7a-105">Syntax</span></span>


```C++
virtual RECT ScaleSourceRect(
   const RECT *pSource
);
```



## <a name="parameters"></a><span data-ttu-id="c9c7a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9c7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9c7a-107">*pSource*</span><span class="sxs-lookup"><span data-stu-id="c9c7a-107">*pSource*</span></span> 
</dt> <dd>

<span data-ttu-id="c9c7a-108">Puntero a un rectángulo sin escala.</span><span class="sxs-lookup"><span data-stu-id="c9c7a-108">Pointer to an unscaled rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9c7a-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9c7a-109">Return value</span></span>

<span data-ttu-id="c9c7a-110">Devuelve el rectángulo escalado.</span><span class="sxs-lookup"><span data-stu-id="c9c7a-110">Returns the scaled rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9c7a-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c9c7a-111">Remarks</span></span>

<span data-ttu-id="c9c7a-112">En la clase **CDrawImage** , este método devuelve *pSource* sin ningún cambio.</span><span class="sxs-lookup"><span data-stu-id="c9c7a-112">In the **CDrawImage** class, this method returns *pSource* without any change.</span></span> <span data-ttu-id="c9c7a-113">Puede invalidar este método si el filtro estira la imagen de vídeo entrante.</span><span class="sxs-lookup"><span data-stu-id="c9c7a-113">You can override this method if the filter stretches the incoming video image.</span></span> <span data-ttu-id="c9c7a-114">Por ejemplo, el tamaño de vídeo nativo podría ser 320 240, pero el tipo de medio en el PIN de entrada podría ser 640 480.</span><span class="sxs-lookup"><span data-stu-id="c9c7a-114">For example, the native video size might be 320   240, but the media type on the input pin might be 640   480.</span></span> <span data-ttu-id="c9c7a-115">En ese caso, el filtro tendría que escalar el rectángulo de origen en un factor de 2.</span><span class="sxs-lookup"><span data-stu-id="c9c7a-115">In that case the filter would need to scale the source rectangle by a factor of 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9c7a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9c7a-116">Requirements</span></span>



| <span data-ttu-id="c9c7a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9c7a-117">Requirement</span></span> | <span data-ttu-id="c9c7a-118">Value</span><span class="sxs-lookup"><span data-stu-id="c9c7a-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9c7a-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9c7a-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c9c7a-120"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9c7a-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c9c7a-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c9c7a-121">Library</span></span><br/> | <dl> <span data-ttu-id="c9c7a-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c9c7a-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9c7a-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9c7a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9c7a-124">**Clase CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="c9c7a-124">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




