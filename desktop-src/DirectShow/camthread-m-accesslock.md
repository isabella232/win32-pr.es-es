---
description: Sección crítica que bloquea el subproceso para que no tenga acceso a otros subprocesos.
ms.assetid: 9bc360be-52d6-4db1-b384-8bc9e25c0914
title: 'Miembro CAMThread:: m_AccessLock (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_AccessLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6edb4b58b630cfdcfd6eefc43b908cf6aeb0f084
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690682"
---
# <a name="camthreadm_accesslock-member"></a><span data-ttu-id="11727-103">Miembro AccessLock CAMThread:: m \_</span><span class="sxs-lookup"><span data-stu-id="11727-103">CAMThread::m\_AccessLock member</span></span>

<span data-ttu-id="11727-104">Sección crítica que bloquea el subproceso para que no tenga acceso a otros subprocesos.</span><span class="sxs-lookup"><span data-stu-id="11727-104">Critical section that locks the thread from being accessed by other threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="11727-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11727-105">Syntax</span></span>


```C++
CCritSec m_AccessLock;
```



## <a name="remarks"></a><span data-ttu-id="11727-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11727-106">Remarks</span></span>

<span data-ttu-id="11727-107">Los métodos [**CAMThread:: Create**](camthread-create.md) y [**CAMThread:: CallWorker**](camthread-callworker.md) incluyen este bloqueo para serializar las operaciones en el subproceso.</span><span class="sxs-lookup"><span data-stu-id="11727-107">The [**CAMThread::Create**](camthread-create.md) and [**CAMThread::CallWorker**](camthread-callworker.md) methods hold this lock, to serialize operations on the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="11727-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11727-108">Requirements</span></span>



| <span data-ttu-id="11727-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="11727-109">Requirement</span></span> | <span data-ttu-id="11727-110">Value</span><span class="sxs-lookup"><span data-stu-id="11727-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11727-111">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11727-111">Header</span></span><br/>  | <dl> <span data-ttu-id="11727-112"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11727-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="11727-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="11727-113">Library</span></span><br/> | <dl> <span data-ttu-id="11727-114"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="11727-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11727-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="11727-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11727-116">**Clase CAMThread**</span><span class="sxs-lookup"><span data-stu-id="11727-116">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




