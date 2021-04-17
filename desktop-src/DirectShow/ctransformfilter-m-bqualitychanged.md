---
description: Marca que indica si ha cambiado la calidad.
ms.assetid: 9084ab1d-b6a0-4e87-a653-86e64c74b07f
title: 'Miembro CTransformFilter:: m_bQualityChanged (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bQualityChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abd0371389d6c17a074580643a06c3fe25bdf433
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680827"
---
# <a name="ctransformfilterm_bqualitychanged-member"></a><span data-ttu-id="ba387-103">Miembro bQualityChanged CTransformFilter:: m \_</span><span class="sxs-lookup"><span data-stu-id="ba387-103">CTransformFilter::m\_bQualityChanged member</span></span>

<span data-ttu-id="ba387-104">Marca que indica si ha cambiado la calidad.</span><span class="sxs-lookup"><span data-stu-id="ba387-104">Flag that indicates whether the quality has changed.</span></span> <span data-ttu-id="ba387-105">La primera vez que el filtro quita un ejemplo, envía un evento [**de \_ \_ cambio de calidad EC**](ec-quality-change.md) al administrador de gráficos de filtro y establece esta marca en **true**.</span><span class="sxs-lookup"><span data-stu-id="ba387-105">The first time that the filter drops a sample, it sends an [**EC\_QUALITY\_CHANGE**](ec-quality-change.md) event to the filter graph manager and sets this flag to **TRUE**.</span></span> <span data-ttu-id="ba387-106">No envía este evento de nuevo hasta que el filtro se detenga y se reinicie, incluso si continúa quitando muestras mientras tanto.</span><span class="sxs-lookup"><span data-stu-id="ba387-106">It does not send this event again until the filter stops and restarts, even if it continues to drop samples in the meantime.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba387-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ba387-107">Syntax</span></span>


```C++
BOOL m_bQualityChanged;
```



## <a name="requirements"></a><span data-ttu-id="ba387-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba387-108">Requirements</span></span>



| <span data-ttu-id="ba387-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba387-109">Requirement</span></span> | <span data-ttu-id="ba387-110">Value</span><span class="sxs-lookup"><span data-stu-id="ba387-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba387-111">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ba387-111">Header</span></span><br/>  | <dl> <span data-ttu-id="ba387-112"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba387-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ba387-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ba387-113">Library</span></span><br/> | <dl> <span data-ttu-id="ba387-114"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ba387-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba387-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba387-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba387-116">**Clase CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="ba387-116">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




