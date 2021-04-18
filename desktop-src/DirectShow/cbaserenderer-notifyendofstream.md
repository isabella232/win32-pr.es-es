---
description: El método NotifyEndOfStream publica un \_ evento de finalización de EC en el administrador de gráficos de filtro.
ms.assetid: 9eec5b65-654d-4b2e-be39-93225a7674a5
title: Método CBaseRenderer. NotifyEndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.NotifyEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f1187705bfa678252237bd95d9a4cb21a0f97d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660976"
---
# <a name="cbaserenderernotifyendofstream-method"></a><span data-ttu-id="827ee-103">CBaseRenderer. NotifyEndOfStream, método</span><span class="sxs-lookup"><span data-stu-id="827ee-103">CBaseRenderer.NotifyEndOfStream method</span></span>

<span data-ttu-id="827ee-104">El `NotifyEndOfStream` método envía un evento de [**\_ finalización de EC**](ec-complete.md) al administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="827ee-104">The `NotifyEndOfStream` method posts an [**EC\_COMPLETE**](ec-complete.md) event to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="827ee-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="827ee-105">Syntax</span></span>


```C++
void NotifyEndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="827ee-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="827ee-106">Parameters</span></span>

<span data-ttu-id="827ee-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="827ee-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="827ee-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="827ee-108">Return value</span></span>

<span data-ttu-id="827ee-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="827ee-109">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="827ee-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="827ee-110">Requirements</span></span>



| <span data-ttu-id="827ee-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="827ee-111">Requirement</span></span> | <span data-ttu-id="827ee-112">Value</span><span class="sxs-lookup"><span data-stu-id="827ee-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="827ee-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="827ee-113">Header</span></span><br/>  | <dl> <span data-ttu-id="827ee-114"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="827ee-114"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="827ee-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="827ee-115">Library</span></span><br/> | <dl> <span data-ttu-id="827ee-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="827ee-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="827ee-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="827ee-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="827ee-118">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="827ee-118">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="827ee-119">**CBaseRenderer:: EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="827ee-119">**CBaseRenderer::EndOfStream**</span></span>](cbaserenderer-endofstream.md)
</dt> <dt>

[<span data-ttu-id="827ee-120">**CBaseRenderer::SendEndOfStream**</span><span class="sxs-lookup"><span data-stu-id="827ee-120">**CBaseRenderer::SendEndOfStream**</span></span>](cbaserenderer-sendendofstream.md)
</dt> </dl>

 

 




