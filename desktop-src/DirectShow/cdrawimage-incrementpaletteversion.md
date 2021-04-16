---
description: El método IncrementPaletteVersion incrementa la versión de la paleta. Llame a este método si el tipo de medio cambia a un nuevo formato de paleta.
ms.assetid: 1ce77f97-d225-45f5-a259-1dcca1272d15
title: Método CDrawImage. IncrementPaletteVersion (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.IncrementPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21b4220ec98c5b083913e92f5749866f629a4854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671485"
---
# <a name="cdrawimageincrementpaletteversion-method"></a><span data-ttu-id="3e530-104">CDrawImage. IncrementPaletteVersion, método</span><span class="sxs-lookup"><span data-stu-id="3e530-104">CDrawImage.IncrementPaletteVersion method</span></span>

<span data-ttu-id="3e530-105">El `IncrementPaletteVersion` método incrementa la versión de la paleta.</span><span class="sxs-lookup"><span data-stu-id="3e530-105">The `IncrementPaletteVersion` method increments the palette version.</span></span> <span data-ttu-id="3e530-106">Llame a este método si el tipo de medio cambia a un nuevo formato de paleta.</span><span class="sxs-lookup"><span data-stu-id="3e530-106">Call this method if the media type changes to a new palettized format.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e530-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e530-107">Syntax</span></span>


```C++
void IncrementPaletteVersion();
```



## <a name="parameters"></a><span data-ttu-id="3e530-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3e530-108">Parameters</span></span>

<span data-ttu-id="3e530-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="3e530-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3e530-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3e530-110">Return value</span></span>

<span data-ttu-id="3e530-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3e530-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e530-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e530-112">Remarks</span></span>

<span data-ttu-id="3e530-113">Este método incrementa el valor de la variable de miembro **m \_ PaletteVersion** .</span><span class="sxs-lookup"><span data-stu-id="3e530-113">This method increments the value of the **m\_PaletteVersion** member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e530-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e530-114">Requirements</span></span>



| <span data-ttu-id="3e530-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e530-115">Requirement</span></span> | <span data-ttu-id="3e530-116">Value</span><span class="sxs-lookup"><span data-stu-id="3e530-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e530-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e530-117">Header</span></span><br/>  | <dl> <span data-ttu-id="3e530-118"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e530-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3e530-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3e530-119">Library</span></span><br/> | <dl> <span data-ttu-id="3e530-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3e530-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e530-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e530-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e530-122">**Clase CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="3e530-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="3e530-123">**CDrawImage::GetPaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="3e530-123">**CDrawImage::GetPaletteVersion**</span></span>](cdrawimage-getpaletteversion.md)
</dt> <dt>

[<span data-ttu-id="3e530-124">**CDrawImage::ResetPaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="3e530-124">**CDrawImage::ResetPaletteVersion**</span></span>](cdrawimage-resetpaletteversion.md)
</dt> </dl>

 

 




