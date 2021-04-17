---
description: El método RecordFrameLateness registra el tiempo que se produce la representación y recopila las estadísticas de la página de propiedades.
ms.assetid: 9d4b90d7-b529-40cc-a0fd-6635163fb7dd
title: Método CBaseVideoRenderer. RecordFrameLateness (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.RecordFrameLateness
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10ae7069ceedbe43f9614ea3fd1c7c901d7023cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679101"
---
# <a name="cbasevideorendererrecordframelateness-method"></a><span data-ttu-id="5f1ad-103">CBaseVideoRenderer. RecordFrameLateness, método</span><span class="sxs-lookup"><span data-stu-id="5f1ad-103">CBaseVideoRenderer.RecordFrameLateness method</span></span>

<span data-ttu-id="5f1ad-104">El `RecordFrameLateness` método registra el tiempo que se produce la representación y recopila estadísticas de la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="5f1ad-104">The `RecordFrameLateness` method records how timely the rendering occurred and gathers statistics for the property page.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f1ad-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5f1ad-105">Syntax</span></span>


```C++
virtual void RecordFrameLateness(
   int trLate,
   int trFrame
);
```



## <a name="parameters"></a><span data-ttu-id="5f1ad-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f1ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f1ad-107">*trLate*</span><span class="sxs-lookup"><span data-stu-id="5f1ad-107">*trLate*</span></span> 
</dt> <dd>

<span data-ttu-id="5f1ad-108">Valor que indica el retraso de la muestra más allá de su tiempo de espera, en unidades de tiempo de referencia.</span><span class="sxs-lookup"><span data-stu-id="5f1ad-108">Value indicating how late the sample was beyond its due time, in reference time units.</span></span>

</dd> <dt>

<span data-ttu-id="5f1ad-109">*trFrame*</span><span class="sxs-lookup"><span data-stu-id="5f1ad-109">*trFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="5f1ad-110">Tiempo de INTERMARCO, en unidades de tiempo de referencia.</span><span class="sxs-lookup"><span data-stu-id="5f1ad-110">Interframe time, in reference time units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f1ad-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f1ad-111">Return value</span></span>

<span data-ttu-id="5f1ad-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="5f1ad-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f1ad-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f1ad-113">Requirements</span></span>



| <span data-ttu-id="5f1ad-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f1ad-114">Requirement</span></span> | <span data-ttu-id="5f1ad-115">Value</span><span class="sxs-lookup"><span data-stu-id="5f1ad-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f1ad-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f1ad-116">Header</span></span><br/>  | <dl> <span data-ttu-id="5f1ad-117"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f1ad-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5f1ad-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5f1ad-118">Library</span></span><br/> | <dl> <span data-ttu-id="5f1ad-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5f1ad-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f1ad-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f1ad-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f1ad-121">**Clase CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="5f1ad-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




