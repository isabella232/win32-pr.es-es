---
description: Hora de detención. De forma predeterminada, el valor se establece en un número muy grande. La clase derivada puede restablecer el valor en su constructor o cuando se inicializa el filtro.
ms.assetid: 1fddcf84-fd9a-4dad-892c-1b0abbb0ca55
title: 'Miembro CSourceSeeking:: m_rtStop (Ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtStop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 28031f245ef877eca38129df2a86210f90093db4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660931"
---
# <a name="csourceseekingm_rtstop-member"></a><span data-ttu-id="b5726-105">Miembro rtStop CSourceSeeking:: m \_</span><span class="sxs-lookup"><span data-stu-id="b5726-105">CSourceSeeking::m\_rtStop member</span></span>

<span data-ttu-id="b5726-106">Hora de detención.</span><span class="sxs-lookup"><span data-stu-id="b5726-106">Stop time.</span></span> <span data-ttu-id="b5726-107">De forma predeterminada, el valor se establece en un número muy grande.</span><span class="sxs-lookup"><span data-stu-id="b5726-107">By default, the value is set to a very large number.</span></span> <span data-ttu-id="b5726-108">La clase derivada puede restablecer el valor en su constructor o cuando se inicializa el filtro.</span><span class="sxs-lookup"><span data-stu-id="b5726-108">The derived class can reset the value in its constructor, or when the filter is initialized.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5726-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5726-109">Syntax</span></span>


```C++
CRefTime m_rtStop;
```



## <a name="remarks"></a><span data-ttu-id="b5726-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b5726-110">Remarks</span></span>

<span data-ttu-id="b5726-111">Mantenga presionada la sección **m \_ Plock** Critical antes de tener acceso a esta variable.</span><span class="sxs-lookup"><span data-stu-id="b5726-111">Hold the **m\_pLock** critical section before accessing this variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5726-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5726-112">Requirements</span></span>



| <span data-ttu-id="b5726-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5726-113">Requirement</span></span> | <span data-ttu-id="b5726-114">Value</span><span class="sxs-lookup"><span data-stu-id="b5726-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5726-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5726-115">Header</span></span><br/>  | <dl> <span data-ttu-id="b5726-116"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b5726-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b5726-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b5726-117">Library</span></span><br/> | <dl> <span data-ttu-id="b5726-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b5726-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5726-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5726-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5726-120">**Clase CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="b5726-120">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




