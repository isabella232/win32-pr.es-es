---
description: Se llama al método OnWaitEnd cuando finaliza un tiempo de espera.
ms.assetid: 283627bb-599c-4711-abc4-b5f92dfd29a5
title: Método CBaseVideoRenderer. OnWaitEnd (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnWaitEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36377565556a759c9268ef1bf31ff7774933ccc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660246"
---
# <a name="cbasevideorendereronwaitend-method"></a><span data-ttu-id="bfde8-103">CBaseVideoRenderer. OnWaitEnd, método</span><span class="sxs-lookup"><span data-stu-id="bfde8-103">CBaseVideoRenderer.OnWaitEnd method</span></span>

<span data-ttu-id="bfde8-104">Se llama al método OnWaitEnd cuando finaliza un tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="bfde8-104">The OnWaitEnd method is called when a wait time ends.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfde8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bfde8-105">Syntax</span></span>


```C++
void OnWaitEnd();
```



## <a name="parameters"></a><span data-ttu-id="bfde8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bfde8-106">Parameters</span></span>

<span data-ttu-id="bfde8-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="bfde8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bfde8-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bfde8-108">Return value</span></span>

<span data-ttu-id="bfde8-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="bfde8-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfde8-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bfde8-110">Remarks</span></span>

<span data-ttu-id="bfde8-111">Esta función miembro solo realiza el registro de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="bfde8-111">This member function does only performance logging.</span></span> <span data-ttu-id="bfde8-112">Se llama cuando el subproceso se awoken de esperar en la ventana o cuando el ejemplo siguiente se debe representar.</span><span class="sxs-lookup"><span data-stu-id="bfde8-112">It is called when the thread is awoken from waiting in the window, or when the next sample is due to be rendered.</span></span> <span data-ttu-id="bfde8-113">Finalmente, podría usarse para recopilar información que controla la sincronización.</span><span class="sxs-lookup"><span data-stu-id="bfde8-113">It could eventually be used to gather information that controls synchronization.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfde8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfde8-114">Requirements</span></span>



| <span data-ttu-id="bfde8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfde8-115">Requirement</span></span> | <span data-ttu-id="bfde8-116">Value</span><span class="sxs-lookup"><span data-stu-id="bfde8-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfde8-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bfde8-117">Header</span></span><br/>  | <dl> <span data-ttu-id="bfde8-118"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bfde8-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bfde8-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bfde8-119">Library</span></span><br/> | <dl> <span data-ttu-id="bfde8-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="bfde8-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfde8-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="bfde8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfde8-122">**Clase CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="bfde8-122">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




