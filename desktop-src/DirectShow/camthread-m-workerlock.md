---
description: Sección crítica que bloquea los datos compartidos entre subprocesos.
ms.assetid: 87966d7d-6677-462f-93bc-fedda7f0bdcf
title: 'Miembro CAMThread:: m_WorkerLock (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_WorkerLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fce6c2ff2a7857f6cb69ce3bb92fe2b6f24bcbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690584"
---
# <a name="camthreadm_workerlock-member"></a><span data-ttu-id="c84a4-103">Miembro WorkerLock CAMThread:: m \_</span><span class="sxs-lookup"><span data-stu-id="c84a4-103">CAMThread::m\_WorkerLock member</span></span>

<span data-ttu-id="c84a4-104">Sección crítica que bloquea los datos compartidos entre subprocesos.</span><span class="sxs-lookup"><span data-stu-id="c84a4-104">Critical section that locks data shared among threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="c84a4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c84a4-105">Syntax</span></span>


```C++
CCritSec m_WorkerLock;
```



## <a name="requirements"></a><span data-ttu-id="c84a4-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c84a4-106">Requirements</span></span>



| <span data-ttu-id="c84a4-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="c84a4-107">Requirement</span></span> | <span data-ttu-id="c84a4-108">Value</span><span class="sxs-lookup"><span data-stu-id="c84a4-108">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c84a4-109">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c84a4-109">Header</span></span><br/>  | <dl> <span data-ttu-id="c84a4-110"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c84a4-110"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c84a4-111">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c84a4-111">Library</span></span><br/> | <dl> <span data-ttu-id="c84a4-112"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c84a4-112"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c84a4-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="c84a4-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c84a4-114">**Clase CAMThread**</span><span class="sxs-lookup"><span data-stu-id="c84a4-114">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




