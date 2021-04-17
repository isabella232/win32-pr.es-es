---
description: El método SetDrawContext establece los contextos de dispositivo que se usan para dibujar.
ms.assetid: dd752970-99b3-42bb-95a5-8103cab276da
title: Método CDrawImage. SetDrawContext (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetDrawContext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d329dd45d1a02afd2cbd0daf8d0da8390b0b395
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660424"
---
# <a name="cdrawimagesetdrawcontext-method"></a><span data-ttu-id="39981-103">CDrawImage. SetDrawContext, método</span><span class="sxs-lookup"><span data-stu-id="39981-103">CDrawImage.SetDrawContext method</span></span>

<span data-ttu-id="39981-104">El `SetDrawContext` método establece los contextos de dispositivo que se usan para dibujar.</span><span class="sxs-lookup"><span data-stu-id="39981-104">The `SetDrawContext` method sets the device contexts used for drawing.</span></span>

## <a name="syntax"></a><span data-ttu-id="39981-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39981-105">Syntax</span></span>


```C++
void SetDrawContext();
```



## <a name="parameters"></a><span data-ttu-id="39981-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39981-106">Parameters</span></span>

<span data-ttu-id="39981-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="39981-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="39981-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39981-108">Return value</span></span>

<span data-ttu-id="39981-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="39981-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="39981-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="39981-110">Remarks</span></span>

<span data-ttu-id="39981-111">Este método recupera los contextos de dispositivo de memoria y de ventana del objeto [**CBaseWindow**](cbasewindow.md) propietario.</span><span class="sxs-lookup"><span data-stu-id="39981-111">This method retrieves the window and memory device contexts from the owning [**CBaseWindow**](cbasewindow.md) object.</span></span> <span data-ttu-id="39981-112">Llame a este método después de que se inicialice la ventana, pero antes de comenzar el dibujo.</span><span class="sxs-lookup"><span data-stu-id="39981-112">Call this method after the window is initialized, but before you begin drawing.</span></span>

## <a name="requirements"></a><span data-ttu-id="39981-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39981-113">Requirements</span></span>



| <span data-ttu-id="39981-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="39981-114">Requirement</span></span> | <span data-ttu-id="39981-115">Value</span><span class="sxs-lookup"><span data-stu-id="39981-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39981-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39981-116">Header</span></span><br/>  | <dl> <span data-ttu-id="39981-117"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="39981-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="39981-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="39981-118">Library</span></span><br/> | <dl> <span data-ttu-id="39981-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="39981-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39981-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="39981-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39981-121">**Clase CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="39981-121">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




