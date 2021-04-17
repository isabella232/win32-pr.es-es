---
description: El método STOP indica al subproceso de streaming que debe detenerse.
ms.assetid: 79bc528a-cf53-43f3-aa17-c459063c99ab
title: CSourceStream. STOP (método) (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 44c9f845c092280ef5fafa808036654bd868a796
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679499"
---
# <a name="csourcestreamstop-method"></a><span data-ttu-id="f226a-103">CSourceStream. STOP (método)</span><span class="sxs-lookup"><span data-stu-id="f226a-103">CSourceStream.Stop method</span></span>

<span data-ttu-id="f226a-104">El `Stop` método indica al subproceso de streaming que se detenga.</span><span class="sxs-lookup"><span data-stu-id="f226a-104">The `Stop` method signals the streaming thread to stop.</span></span>

## <a name="syntax"></a><span data-ttu-id="f226a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f226a-105">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="f226a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f226a-106">Parameters</span></span>

<span data-ttu-id="f226a-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f226a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f226a-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f226a-108">Return value</span></span>

<span data-ttu-id="f226a-109">Devuelve S \_ correcto o E \_ inesperados.</span><span class="sxs-lookup"><span data-stu-id="f226a-109">Returns S\_OK or E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="f226a-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f226a-110">Remarks</span></span>

<span data-ttu-id="f226a-111">El método [**CSourceStream:: Inactive**](csourcestream-inactive.md) llama a este método.</span><span class="sxs-lookup"><span data-stu-id="f226a-111">The [**CSourceStream::Inactive**](csourcestream-inactive.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f226a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f226a-112">Requirements</span></span>



| <span data-ttu-id="f226a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f226a-113">Requirement</span></span> | <span data-ttu-id="f226a-114">Value</span><span class="sxs-lookup"><span data-stu-id="f226a-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f226a-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f226a-115">Header</span></span><br/>  | <dl> <span data-ttu-id="f226a-116"><dt>Source. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f226a-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f226a-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f226a-117">Library</span></span><br/> | <dl> <span data-ttu-id="f226a-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f226a-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f226a-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="f226a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f226a-120">**Clase CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="f226a-120">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




