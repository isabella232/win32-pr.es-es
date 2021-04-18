---
description: Indica el nivel de finalización de las muestras en el representador, en unidades de tiempo de referencia. Sintáctica.
ms.assetid: 7b30fbe1-5e57-4aa4-8e87-ddd584f186e4
title: 'Miembro CVideoTransformFilter:: m_itrLate (Vtrans. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_itrLate
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3ed93a4612d8fa5d4fe79239c6a7f4f5e479717
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660927"
---
# <a name="cvideotransformfilterm_itrlate-member"></a><span data-ttu-id="bfab5-104">Miembro itrLate CVideoTransformFilter:: m \_</span><span class="sxs-lookup"><span data-stu-id="bfab5-104">CVideoTransformFilter::m\_itrLate member</span></span>

<span data-ttu-id="bfab5-105">Indica el nivel de finalización de las muestras en el representador, en unidades de tiempo de referencia.</span><span class="sxs-lookup"><span data-stu-id="bfab5-105">Indicates how late the samples are arriving at the renderer, in reference time units.</span></span> <span data-ttu-id="bfab5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bfab5-106">Syntax</span></span>

## <a name="syntax"></a><span data-ttu-id="bfab5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bfab5-107">Syntax</span></span>


```C++
int m_itrLate;
```



## <a name="remarks"></a><span data-ttu-id="bfab5-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bfab5-108">Remarks</span></span>

<span data-ttu-id="bfab5-109">Cuando el filtro recibe un mensaje de calidad de nivel inferior, almacena el valor de retraso en esta variable.</span><span class="sxs-lookup"><span data-stu-id="bfab5-109">When the filter receives a quality message from downstream, it stores the lateness value in this variable.</span></span> <span data-ttu-id="bfab5-110">A medida que el filtro quita fotogramas, actualiza este valor restando la duración de cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="bfab5-110">As the filter drops frames, it updates this value by subtracting the duration of each frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfab5-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfab5-111">Requirements</span></span>



| <span data-ttu-id="bfab5-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfab5-112">Requirement</span></span> | <span data-ttu-id="bfab5-113">Value</span><span class="sxs-lookup"><span data-stu-id="bfab5-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfab5-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bfab5-114">Header</span></span><br/>  | <dl> <span data-ttu-id="bfab5-115"><dt>Vtrans. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bfab5-115"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="bfab5-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bfab5-116">Library</span></span><br/> | <dl> <span data-ttu-id="bfab5-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="bfab5-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfab5-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="bfab5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfab5-119">**Clase CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="bfab5-119">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




