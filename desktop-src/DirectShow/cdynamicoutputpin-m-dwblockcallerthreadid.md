---
description: 'El identificador del subproceso que llamó por última vez al método IPinFlowControl:: Block en este pin. Esta variable miembro solo es válida mientras el PIN está bloqueado.'
ms.assetid: 7f8429c5-7e58-49a1-9f36-01088379a193
title: 'Miembro CDynamicOutputPin:: m_dwBlockCallerThreadID (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwBlockCallerThreadID
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9aa2de66f1afe690715ab658483c01cdfeb3f451
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661354"
---
# <a name="cdynamicoutputpinm_dwblockcallerthreadid-member"></a><span data-ttu-id="5546e-104">Miembro dwBlockCallerThreadID CDynamicOutputPin:: m \_</span><span class="sxs-lookup"><span data-stu-id="5546e-104">CDynamicOutputPin::m\_dwBlockCallerThreadID member</span></span>

<span data-ttu-id="5546e-105">El identificador del subproceso que llamó por última vez al método [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) en este pin.</span><span class="sxs-lookup"><span data-stu-id="5546e-105">The identifier of the thread that last called the [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) method on this pin.</span></span> <span data-ttu-id="5546e-106">Esta variable miembro solo es válida mientras el PIN está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="5546e-106">This member variable is only valid while the pin is blocked.</span></span>

## <a name="syntax"></a><span data-ttu-id="5546e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5546e-107">Syntax</span></span>


```C++
DWORD m_dwBlockCallerThreadID;
```



## <a name="remarks"></a><span data-ttu-id="5546e-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5546e-108">Remarks</span></span>

<span data-ttu-id="5546e-109">Antes de tener acceso a esta variable, conserve la sección crítica [**CDynamicOutputPin:: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="5546e-109">Before accessing this variable, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="5546e-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5546e-110">Requirements</span></span>



| <span data-ttu-id="5546e-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5546e-111">Requirement</span></span> | <span data-ttu-id="5546e-112">Value</span><span class="sxs-lookup"><span data-stu-id="5546e-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5546e-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5546e-113">Header</span></span><br/>  | <dl> <span data-ttu-id="5546e-114"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5546e-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5546e-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5546e-115">Library</span></span><br/> | <dl> <span data-ttu-id="5546e-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5546e-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5546e-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="5546e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5546e-118">**Clase CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="5546e-118">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




