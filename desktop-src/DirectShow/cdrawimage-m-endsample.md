---
description: La \_ variable miembro m EndSample especifica la hora de detención de la muestra más reciente.
ms.assetid: 694815b6-8da5-4174-b2c7-7d686a557c6c
title: 'Miembro CDrawImage:: m_EndSample (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_EndSample
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 78268e8335d6dd8c24497a9e4d74b0caab205a99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671007"
---
# <a name="cdrawimagem_endsample-member"></a><span data-ttu-id="bf318-103">Miembro EndSample CDrawImage:: m \_</span><span class="sxs-lookup"><span data-stu-id="bf318-103">CDrawImage::m\_EndSample member</span></span>

<span data-ttu-id="bf318-104">La `m_EndSample` variable miembro especifica la hora de detención de la muestra más reciente.</span><span class="sxs-lookup"><span data-stu-id="bf318-104">The `m_EndSample` member variable specifies the stop time of the most recent sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf318-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf318-105">Syntax</span></span>


```C++
CRefTime m_EndSample;
```



## <a name="remarks"></a><span data-ttu-id="bf318-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bf318-106">Remarks</span></span>

<span data-ttu-id="bf318-107">El valor solo es válido dentro del método [**CDrawImage::D isplaysampletimes**](cdrawimage-displaysampletimes.md) .</span><span class="sxs-lookup"><span data-stu-id="bf318-107">The value is only valid inside the [**CDrawImage::DisplaySampleTimes**](cdrawimage-displaysampletimes.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf318-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf318-108">Requirements</span></span>



| <span data-ttu-id="bf318-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf318-109">Requirement</span></span> | <span data-ttu-id="bf318-110">Value</span><span class="sxs-lookup"><span data-stu-id="bf318-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf318-111">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf318-111">Header</span></span><br/>  | <dl> <span data-ttu-id="bf318-112"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf318-112"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bf318-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bf318-113">Library</span></span><br/> | <dl> <span data-ttu-id="bf318-114"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="bf318-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf318-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf318-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf318-116">**Clase CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="bf318-116">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




