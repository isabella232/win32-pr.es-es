---
description: Marca que indica si el filtro ha enviado una notificación de final de secuencia.
ms.assetid: 93f897de-04bb-4de4-a612-39b27c7d6f6c
title: 'Miembro CTransformFilter:: m_bEOSDelivered (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bEOSDelivered
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f24b87f9808c53b5f64f66031a8ee2a4e9449089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661032"
---
# <a name="ctransformfilterm_beosdelivered-member"></a><span data-ttu-id="1f4d7-103">Miembro bEOSDelivered CTransformFilter:: m \_</span><span class="sxs-lookup"><span data-stu-id="1f4d7-103">CTransformFilter::m\_bEOSDelivered member</span></span>

<span data-ttu-id="1f4d7-104">Marca que indica si el filtro ha enviado una notificación de final de secuencia.</span><span class="sxs-lookup"><span data-stu-id="1f4d7-104">Flag that indicates whether the filter has sent an end-of-stream notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f4d7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1f4d7-105">Syntax</span></span>


```C++
BOOL m_bEOSDelivered;
```



## <a name="remarks"></a><span data-ttu-id="1f4d7-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1f4d7-106">Remarks</span></span>

<span data-ttu-id="1f4d7-107">Si el filtro se detiene cuando no tiene una conexión de entrada, envía una notificación de final de secuencia de nivel inferior y establece esta marca en **true**.</span><span class="sxs-lookup"><span data-stu-id="1f4d7-107">If the filter pauses when it does not have an input connection, it sends an end-of-stream notification downstream and sets this flag to **TRUE**.</span></span> <span data-ttu-id="1f4d7-108">La notificación de final de secuencia garantiza que el filtro de nivel inferior no espera los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="1f4d7-108">The end-of-stream notification ensures that the downstream filter does not wait for samples.</span></span> <span data-ttu-id="1f4d7-109">Tenga en cuenta que el método [**EndOfStream**](ctransformfilter-endofstream.md) del filtro no establece esta marca.</span><span class="sxs-lookup"><span data-stu-id="1f4d7-109">Note that the filter's [**EndOfStream**](ctransformfilter-endofstream.md) method does not set this flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f4d7-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f4d7-110">Requirements</span></span>



| <span data-ttu-id="1f4d7-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f4d7-111">Requirement</span></span> | <span data-ttu-id="1f4d7-112">Value</span><span class="sxs-lookup"><span data-stu-id="1f4d7-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f4d7-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1f4d7-113">Header</span></span><br/>  | <dl> <span data-ttu-id="1f4d7-114"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1f4d7-114"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1f4d7-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1f4d7-115">Library</span></span><br/> | <dl> <span data-ttu-id="1f4d7-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1f4d7-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f4d7-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f4d7-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f4d7-118">**Clase CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="1f4d7-118">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




