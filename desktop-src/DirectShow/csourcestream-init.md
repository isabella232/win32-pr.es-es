---
description: El método init inicializa el subproceso de streaming.
ms.assetid: c746e595-de97-478c-8b22-5c4dd5594a8f
title: Método CSourceStream.Init (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Init
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a3abf2b4637385616862c0613f72afd676f5b79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690594"
---
# <a name="csourcestreaminit-method"></a><span data-ttu-id="86dbb-103">CSourceStream.Init (método)</span><span class="sxs-lookup"><span data-stu-id="86dbb-103">CSourceStream.Init method</span></span>

<span data-ttu-id="86dbb-104">El `Init` método inicializa el subproceso de streaming.</span><span class="sxs-lookup"><span data-stu-id="86dbb-104">The `Init` method initializes the streaming thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="86dbb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="86dbb-105">Syntax</span></span>


```C++
HRESULT Init();
```



## <a name="parameters"></a><span data-ttu-id="86dbb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86dbb-106">Parameters</span></span>

<span data-ttu-id="86dbb-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="86dbb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="86dbb-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="86dbb-108">Return value</span></span>

<span data-ttu-id="86dbb-109">Devuelve S \_ OK u otro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="86dbb-109">Returns S\_OK, or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="86dbb-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86dbb-110">Remarks</span></span>

<span data-ttu-id="86dbb-111">Este método debe ser la primera solicitud de subproceso enviada al método [**CSourceStream:: ThreadProc**](csourcestream-threadproc.md) .</span><span class="sxs-lookup"><span data-stu-id="86dbb-111">This method must be the first thread request sent to the [**CSourceStream::ThreadProc**](csourcestream-threadproc.md) method.</span></span> <span data-ttu-id="86dbb-112">El método [**CSourceStream:: Active**](csourcestream-active.md) llama a este método.</span><span class="sxs-lookup"><span data-stu-id="86dbb-112">The [**CSourceStream::Active**](csourcestream-active.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="86dbb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86dbb-113">Requirements</span></span>



| <span data-ttu-id="86dbb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="86dbb-114">Requirement</span></span> | <span data-ttu-id="86dbb-115">Value</span><span class="sxs-lookup"><span data-stu-id="86dbb-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86dbb-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="86dbb-116">Header</span></span><br/>  | <dl> <span data-ttu-id="86dbb-117"><dt>Source. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86dbb-117"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="86dbb-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="86dbb-118">Library</span></span><br/> | <dl> <span data-ttu-id="86dbb-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="86dbb-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86dbb-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="86dbb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86dbb-121">**Clase CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="86dbb-121">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




