---
description: El método OnDisplayChange envía un \_ evento de visualización de \_ modificación de EC al administrador de gráficos de filtro.
ms.assetid: e4cdcdf2-7fc2-4893-9897-97bcf2c12610
title: Método CBaseRenderer. OnDisplayChange (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnDisplayChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1e99a8626d523e8b14b013acc9d2ead462f48df3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661334"
---
# <a name="cbaserendererondisplaychange-method"></a><span data-ttu-id="521d1-103">CBaseRenderer. OnDisplayChange, método</span><span class="sxs-lookup"><span data-stu-id="521d1-103">CBaseRenderer.OnDisplayChange method</span></span>

<span data-ttu-id="521d1-104">El `OnDisplayChange` método envía un evento de [**\_ visualización de \_ modificación de EC**](ec-display-changed.md) al administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="521d1-104">The `OnDisplayChange` method posts an [**EC\_DISPLAY\_CHANGED**](ec-display-changed.md) event to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="521d1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="521d1-105">Syntax</span></span>


```C++
BOOL OnDisplayChange();
```



## <a name="parameters"></a><span data-ttu-id="521d1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="521d1-106">Parameters</span></span>

<span data-ttu-id="521d1-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="521d1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="521d1-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="521d1-108">Return value</span></span>

<span data-ttu-id="521d1-109">Devuelve **true** si se ha expuesto el evento o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="521d1-109">Returns **TRUE** if the event was posted, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="521d1-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="521d1-110">Remarks</span></span>

<span data-ttu-id="521d1-111">Los representadores de vídeo deben llamar a este método en respuesta a \_ los mensajes de WM DISPLAYCHANGE.</span><span class="sxs-lookup"><span data-stu-id="521d1-111">Video renderers should call this method in response to WM\_DISPLAYCHANGE messages.</span></span> <span data-ttu-id="521d1-112">Si el PIN de entrada está conectado, el método envía un \_ evento de visualización de \_ modificación de EC al administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="521d1-112">If the input pin is connected, the method sends an EC\_DISPLAY\_CHANGED event to the filter graph manager.</span></span>

## <a name="requirements"></a><span data-ttu-id="521d1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="521d1-113">Requirements</span></span>



| <span data-ttu-id="521d1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="521d1-114">Requirement</span></span> | <span data-ttu-id="521d1-115">Value</span><span class="sxs-lookup"><span data-stu-id="521d1-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="521d1-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="521d1-116">Header</span></span><br/>  | <dl> <span data-ttu-id="521d1-117"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="521d1-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="521d1-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="521d1-118">Library</span></span><br/> | <dl> <span data-ttu-id="521d1-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="521d1-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="521d1-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="521d1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="521d1-121">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="521d1-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




