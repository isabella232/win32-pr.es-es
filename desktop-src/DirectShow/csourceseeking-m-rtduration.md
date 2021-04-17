---
description: 'Duración de la secuencia. De forma predeterminada, el valor se establece en el valor de la variable miembro CSourceSeeking:: m \_ rtStop.'
ms.assetid: a87b321e-3179-4485-969b-bf12cb634b43
title: 'Miembro CSourceSeeking:: m_rtDuration (Ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtDuration
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e188a29689a6dd1a54ef401f8bd2677e30989972
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660773"
---
# <a name="csourceseekingm_rtduration-member"></a><span data-ttu-id="3d52a-104">Miembro rtDuration CSourceSeeking:: m \_</span><span class="sxs-lookup"><span data-stu-id="3d52a-104">CSourceSeeking::m\_rtDuration member</span></span>

<span data-ttu-id="3d52a-105">Duración de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="3d52a-105">Duration of the stream.</span></span> <span data-ttu-id="3d52a-106">De forma predeterminada, el valor se establece en el valor de la variable miembro [**CSourceSeeking:: m \_ rtStop**](csourceseeking-m-rtstop.md) .</span><span class="sxs-lookup"><span data-stu-id="3d52a-106">By default, the value is set to the value of the [**CSourceSeeking::m\_rtStop**](csourceseeking-m-rtstop.md) member variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d52a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d52a-107">Syntax</span></span>


```C++
CRefTime m_rtDuration;
```



## <a name="remarks"></a><span data-ttu-id="3d52a-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3d52a-108">Remarks</span></span>

<span data-ttu-id="3d52a-109">Mantenga presionada la sección **m \_ Plock** Critical antes de tener acceso a esta variable.</span><span class="sxs-lookup"><span data-stu-id="3d52a-109">Hold the **m\_pLock** critical section before accessing this variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d52a-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d52a-110">Requirements</span></span>



| <span data-ttu-id="3d52a-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d52a-111">Requirement</span></span> | <span data-ttu-id="3d52a-112">Value</span><span class="sxs-lookup"><span data-stu-id="3d52a-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d52a-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3d52a-113">Header</span></span><br/>  | <dl> <span data-ttu-id="3d52a-114"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d52a-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3d52a-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3d52a-115">Library</span></span><br/> | <dl> <span data-ttu-id="3d52a-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3d52a-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d52a-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d52a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d52a-118">**Clase CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="3d52a-118">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




