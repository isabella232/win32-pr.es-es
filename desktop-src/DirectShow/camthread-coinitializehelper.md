---
description: El método CoInitializeHelper llama a la función CoInitializeEx al inicio del subproceso.
ms.assetid: 1a981e1e-c059-4e51-81d8-33bcb39ee580
title: Método CAMThread. CoInitializeHelper (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CoInitializeHelper
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6c3eb7fbcb9e4abada43098339a29d208ded0d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660437"
---
# <a name="camthreadcoinitializehelper-method"></a><span data-ttu-id="0f421-103">CAMThread. CoInitializeHelper, método</span><span class="sxs-lookup"><span data-stu-id="0f421-103">CAMThread.CoInitializeHelper method</span></span>

<span data-ttu-id="0f421-104">El `CoInitializeHelper` método llama a la función CoInitializeEx al inicio del subproceso.</span><span class="sxs-lookup"><span data-stu-id="0f421-104">The `CoInitializeHelper` method calls the CoInitializeEx function at the start of the thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f421-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f421-105">Syntax</span></span>


```C++
static HRESULT CoInitializeHelper();
```



## <a name="parameters"></a><span data-ttu-id="0f421-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f421-106">Parameters</span></span>

<span data-ttu-id="0f421-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="0f421-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0f421-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0f421-108">Return value</span></span>

<span data-ttu-id="0f421-109">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0f421-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0f421-110">Los valores posibles son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="0f421-110">The following are possible values.</span></span>



| <span data-ttu-id="0f421-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0f421-111">Return code</span></span>                                                                             | <span data-ttu-id="0f421-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="0f421-112">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="0f421-113"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="0f421-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="0f421-114">La función CoInitializeEx no está disponible.</span><span class="sxs-lookup"><span data-stu-id="0f421-114">The CoInitializeEx function is not available.</span></span><br/> |
| <dl> <span data-ttu-id="0f421-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0f421-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="0f421-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="0f421-116">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="0f421-117"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="0f421-117"><dt>**E\_FAIL**</dt></span></span> </dl>  | <span data-ttu-id="0f421-118">Error.</span><span class="sxs-lookup"><span data-stu-id="0f421-118">Failure.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="0f421-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f421-119">Remarks</span></span>

<span data-ttu-id="0f421-120">El método [**CAMThread:: InitialThreadProc**](camthread-initialthreadproc.md) llama a este método auxiliar, que llama a la función CoInitializeEx.</span><span class="sxs-lookup"><span data-stu-id="0f421-120">The [**CAMThread::InitialThreadProc**](camthread-initialthreadproc.md) method calls this helper method, which calls the CoInitializeEx function.</span></span> <span data-ttu-id="0f421-121">Usa la marca coinit \_ Disable \_ OLE1DDE para deshabilitar intercambio dinámico de datos (DDE).</span><span class="sxs-lookup"><span data-stu-id="0f421-121">It uses the COINIT\_DISABLE\_OLE1DDE flag, to disable Dynamic Data Exchange (DDE).</span></span> <span data-ttu-id="0f421-122">Para obtener más información, vea el SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="0f421-122">For more information, see the Platform SDK.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f421-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f421-123">Requirements</span></span>



| <span data-ttu-id="0f421-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f421-124">Requirement</span></span> | <span data-ttu-id="0f421-125">Value</span><span class="sxs-lookup"><span data-stu-id="0f421-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f421-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f421-126">Header</span></span><br/>  | <dl> <span data-ttu-id="0f421-127"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0f421-127"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0f421-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0f421-128">Library</span></span><br/> | <dl> <span data-ttu-id="0f421-129"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0f421-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f421-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f421-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f421-131">**Clase CAMThread**</span><span class="sxs-lookup"><span data-stu-id="0f421-131">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




