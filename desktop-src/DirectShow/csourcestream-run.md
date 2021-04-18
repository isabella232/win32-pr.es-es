---
description: El método Run indica al subproceso de streaming que se ejecute.
ms.assetid: 9aef7801-dcfb-4597-bccb-5ba19327b2d5
title: Método CSourceStream. Run (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39093654677ab4828f8a1d5a01a8cf7deaf42507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681012"
---
# <a name="csourcestreamrun-method"></a><span data-ttu-id="e59c2-103">CSourceStream. Run (método)</span><span class="sxs-lookup"><span data-stu-id="e59c2-103">CSourceStream.Run method</span></span>

<span data-ttu-id="e59c2-104">El `Run` método indica al subproceso de streaming que se ejecute.</span><span class="sxs-lookup"><span data-stu-id="e59c2-104">The `Run` method signals the streaming thread to run.</span></span>

## <a name="syntax"></a><span data-ttu-id="e59c2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e59c2-105">Syntax</span></span>


```C++
HRESULT Run();
```



## <a name="parameters"></a><span data-ttu-id="e59c2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e59c2-106">Parameters</span></span>

<span data-ttu-id="e59c2-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e59c2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e59c2-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e59c2-108">Return value</span></span>

<span data-ttu-id="e59c2-109">Devuelve S \_ correcto o E \_ inesperados.</span><span class="sxs-lookup"><span data-stu-id="e59c2-109">Returns S\_OK or E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="e59c2-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e59c2-110">Remarks</span></span>

<span data-ttu-id="e59c2-111">En la clase base, este método tiene el mismo efecto que la solicitud [**CSourceStream::P ause**](csourcestream-pause.md) , y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="e59c2-111">In the base class, this method has the same effect as the [**CSourceStream::Pause**](csourcestream-pause.md) request, and is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="e59c2-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e59c2-112">Requirements</span></span>



| <span data-ttu-id="e59c2-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e59c2-113">Requirement</span></span> | <span data-ttu-id="e59c2-114">Value</span><span class="sxs-lookup"><span data-stu-id="e59c2-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e59c2-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e59c2-115">Header</span></span><br/>  | <dl> <span data-ttu-id="e59c2-116"><dt>Source. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e59c2-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="e59c2-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e59c2-117">Library</span></span><br/> | <dl> <span data-ttu-id="e59c2-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e59c2-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e59c2-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="e59c2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e59c2-120">**Clase CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="e59c2-120">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




