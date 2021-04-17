---
description: El método GetPaletteVersion recupera la versión de la paleta actual.
ms.assetid: 9f97a810-04a4-4ea3-8918-416e9cd8e5e4
title: Método CDrawImage. GetPaletteVersion (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c86f1a0dad8d33913a52962dfe2ec09b7b8244db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681048"
---
# <a name="cdrawimagegetpaletteversion-method"></a><span data-ttu-id="9a844-103">CDrawImage. GetPaletteVersion, método</span><span class="sxs-lookup"><span data-stu-id="9a844-103">CDrawImage.GetPaletteVersion method</span></span>

<span data-ttu-id="9a844-104">El `GetPaletteVersion` método recupera la versión de la paleta actual.</span><span class="sxs-lookup"><span data-stu-id="9a844-104">The `GetPaletteVersion` method retrieves the current palette version.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a844-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9a844-105">Syntax</span></span>


```C++
LONG GetPaletteVersion();
```



## <a name="parameters"></a><span data-ttu-id="9a844-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9a844-106">Parameters</span></span>

<span data-ttu-id="9a844-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="9a844-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9a844-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a844-108">Return value</span></span>

<span data-ttu-id="9a844-109">Devuelve el valor de la variable de miembro **m \_ PaletteVersion** .</span><span class="sxs-lookup"><span data-stu-id="9a844-109">Returns the value of the **m\_PaletteVersion** member variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a844-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a844-110">Remarks</span></span>

<span data-ttu-id="9a844-111">El valor devuelto por este método solo se aplica cuando el asignador es un objeto [**CImageAllocator**](cimageallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="9a844-111">The value returned by this method applies only when the allocator is a [**CImageAllocator**](cimageallocator.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a844-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a844-112">Requirements</span></span>



| <span data-ttu-id="9a844-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a844-113">Requirement</span></span> | <span data-ttu-id="9a844-114">Value</span><span class="sxs-lookup"><span data-stu-id="9a844-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a844-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9a844-115">Header</span></span><br/>  | <dl> <span data-ttu-id="9a844-116"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9a844-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9a844-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9a844-117">Library</span></span><br/> | <dl> <span data-ttu-id="9a844-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9a844-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a844-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a844-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a844-120">**Clase CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="9a844-120">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="9a844-121">**CDrawImage::IncrementPaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="9a844-121">**CDrawImage::IncrementPaletteVersion**</span></span>](cdrawimage-incrementpaletteversion.md)
</dt> <dt>

[<span data-ttu-id="9a844-122">**CDrawImage::ResetPaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="9a844-122">**CDrawImage::ResetPaletteVersion**</span></span>](cdrawimage-resetpaletteversion.md)
</dt> </dl>

 

 




