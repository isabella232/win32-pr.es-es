---
description: El método SetStretchMode calcula si se debe ajustar la imagen de vídeo.
ms.assetid: ffdcaf9c-e157-4557-9193-8430c1c451bf
title: Método CDrawImage. SetStretchMode (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetStretchMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 33a4b3a6b104b9e2888776cc59183835f412fdcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661396"
---
# <a name="cdrawimagesetstretchmode-method"></a><span data-ttu-id="648fe-103">CDrawImage. SetStretchMode, método</span><span class="sxs-lookup"><span data-stu-id="648fe-103">CDrawImage.SetStretchMode method</span></span>

<span data-ttu-id="648fe-104">El `SetStretchMode` método calcula si se debe ajustar la imagen de vídeo.</span><span class="sxs-lookup"><span data-stu-id="648fe-104">The `SetStretchMode` method calculates whether the video image must be stretched.</span></span>

## <a name="syntax"></a><span data-ttu-id="648fe-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="648fe-105">Syntax</span></span>


```C++
void SetStretchMode();
```



## <a name="parameters"></a><span data-ttu-id="648fe-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="648fe-106">Parameters</span></span>

<span data-ttu-id="648fe-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="648fe-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="648fe-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="648fe-108">Return value</span></span>

<span data-ttu-id="648fe-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="648fe-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="648fe-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="648fe-110">Remarks</span></span>

<span data-ttu-id="648fe-111">La clase **CDrawImage** llama automáticamente a este método cada vez que cambia el rectángulo de origen o de destino.</span><span class="sxs-lookup"><span data-stu-id="648fe-111">The **CDrawImage** class automatically calls this method whenever the source or target rectangle changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="648fe-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="648fe-112">Requirements</span></span>



| <span data-ttu-id="648fe-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="648fe-113">Requirement</span></span> | <span data-ttu-id="648fe-114">Value</span><span class="sxs-lookup"><span data-stu-id="648fe-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="648fe-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="648fe-115">Header</span></span><br/>  | <dl> <span data-ttu-id="648fe-116"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="648fe-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="648fe-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="648fe-117">Library</span></span><br/> | <dl> <span data-ttu-id="648fe-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="648fe-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="648fe-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="648fe-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="648fe-120">**Clase CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="648fe-120">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




