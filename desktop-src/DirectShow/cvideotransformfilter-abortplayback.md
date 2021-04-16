---
description: El método AbortPlayback se usa para indicar un error de streaming. Envía un \_ evento ERRORABORT de EC al administrador de gráficos de filtro y envía una notificación de final de secuencia de nivel inferior.
ms.assetid: b48ec72f-d220-4b27-98fc-88eaa4f663eb
title: Método CVideoTransformFilter. AbortPlayback (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.AbortPlayback
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 952987dec315408920e92d79003480a01640d14e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678929"
---
# <a name="cvideotransformfilterabortplayback-method"></a><span data-ttu-id="a8e31-104">CVideoTransformFilter. AbortPlayback, método</span><span class="sxs-lookup"><span data-stu-id="a8e31-104">CVideoTransformFilter.AbortPlayback method</span></span>

<span data-ttu-id="a8e31-105">El `AbortPlayback` método se usa para indicar un error de streaming.</span><span class="sxs-lookup"><span data-stu-id="a8e31-105">The `AbortPlayback` method is used to signal a streaming error.</span></span> <span data-ttu-id="a8e31-106">Envía un evento [**\_ ERRORABORT de EC**](ec-errorabort.md) al administrador de gráficos de filtro y envía una notificación de final de secuencia de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="a8e31-106">It sends an [**EC\_ERRORABORT**](ec-errorabort.md) event to the Filter Graph Manager, and sends an end-of-stream notification downstream.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8e31-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8e31-107">Syntax</span></span>


```C++
HRESULT AbortPlayback(
   HRESULT hr
);
```



## <a name="parameters"></a><span data-ttu-id="a8e31-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8e31-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8e31-109">*h*</span><span class="sxs-lookup"><span data-stu-id="a8e31-109">*hr*</span></span> 
</dt> <dd>

<span data-ttu-id="a8e31-110">Valor **HRESULT** de la operación en la que se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="a8e31-110">**HRESULT** value of the operation that failed.</span></span> <span data-ttu-id="a8e31-111">Este valor se usa como el primer parámetro de evento para el \_ evento ERRORABORT de EC.</span><span class="sxs-lookup"><span data-stu-id="a8e31-111">This value is used as the first event parameter for the EC\_ERRORABORT event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8e31-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8e31-112">Return value</span></span>

<span data-ttu-id="a8e31-113">Devuelve el valor del parámetro *HR* .</span><span class="sxs-lookup"><span data-stu-id="a8e31-113">Returns the value of the *hr* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8e31-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8e31-114">Requirements</span></span>



| <span data-ttu-id="a8e31-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8e31-115">Requirement</span></span> | <span data-ttu-id="a8e31-116">Value</span><span class="sxs-lookup"><span data-stu-id="a8e31-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8e31-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8e31-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a8e31-118"><dt>Vtrans. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8e31-118"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a8e31-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a8e31-119">Library</span></span><br/> | <dl> <span data-ttu-id="a8e31-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a8e31-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8e31-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8e31-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8e31-122">**Clase CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="a8e31-122">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




