---
description: El método ResetPaletteVersion restablece la versión de la paleta. Llame a este método si el PIN del filtro propietario se vuelve a conectar.
ms.assetid: c9e5588c-5501-4356-bdec-a339d33f9eb5
title: Método CDrawImage. ResetPaletteVersion (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.ResetPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a94cd04de428a29308ead8fa33ccfe1792e021a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660423"
---
# <a name="cdrawimageresetpaletteversion-method"></a><span data-ttu-id="38aec-104">CDrawImage. ResetPaletteVersion, método</span><span class="sxs-lookup"><span data-stu-id="38aec-104">CDrawImage.ResetPaletteVersion method</span></span>

<span data-ttu-id="38aec-105">El `ResetPaletteVersion` método restablece la versión de la paleta.</span><span class="sxs-lookup"><span data-stu-id="38aec-105">The `ResetPaletteVersion` method resets the palette version.</span></span> <span data-ttu-id="38aec-106">Llame a este método si el PIN del filtro propietario se vuelve a conectar.</span><span class="sxs-lookup"><span data-stu-id="38aec-106">Call this method if the owning filter's pin reconnects.</span></span>

## <a name="syntax"></a><span data-ttu-id="38aec-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38aec-107">Syntax</span></span>


```C++
void ResetPaletteVersion();
```



## <a name="parameters"></a><span data-ttu-id="38aec-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="38aec-108">Parameters</span></span>

<span data-ttu-id="38aec-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="38aec-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="38aec-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="38aec-110">Return value</span></span>

<span data-ttu-id="38aec-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="38aec-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="38aec-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="38aec-112">Remarks</span></span>

<span data-ttu-id="38aec-113">Este método establece el valor de **m \_ PaletteVersion** en una constante predefinida, **\_ versión** de la paleta.</span><span class="sxs-lookup"><span data-stu-id="38aec-113">This method sets the value of **m\_PaletteVersion** to a predefined constant, **PALETTE\_VERSION**.</span></span>

## <a name="requirements"></a><span data-ttu-id="38aec-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38aec-114">Requirements</span></span>



| <span data-ttu-id="38aec-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="38aec-115">Requirement</span></span> | <span data-ttu-id="38aec-116">Value</span><span class="sxs-lookup"><span data-stu-id="38aec-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38aec-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="38aec-117">Header</span></span><br/>  | <dl> <span data-ttu-id="38aec-118"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="38aec-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="38aec-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="38aec-119">Library</span></span><br/> | <dl> <span data-ttu-id="38aec-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="38aec-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38aec-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="38aec-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38aec-122">**Clase CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="38aec-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="38aec-123">**CDrawImage::GetPaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="38aec-123">**CDrawImage::GetPaletteVersion**</span></span>](cdrawimage-getpaletteversion.md)
</dt> <dt>

[<span data-ttu-id="38aec-124">**CDrawImage::IncrementPaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="38aec-124">**CDrawImage::IncrementPaletteVersion**</span></span>](cdrawimage-incrementpaletteversion.md)
</dt> </dl>

 

 




