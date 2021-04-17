---
description: Identificador del subproceso.
ms.assetid: 93d1182a-58f0-4570-8568-fe0fded762cb
title: 'Miembro CAMThread:: m_hThread (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hThread
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e83dd225da0c3673f9c7f423e0bf56da7431b097
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691040"
---
# <a name="camthreadm_hthread-member"></a><span data-ttu-id="c9608-103">Miembro hThread CAMThread:: m \_</span><span class="sxs-lookup"><span data-stu-id="c9608-103">CAMThread::m\_hThread member</span></span>

<span data-ttu-id="c9608-104">Identificador del subproceso.</span><span class="sxs-lookup"><span data-stu-id="c9608-104">Handle to the thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9608-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9608-105">Syntax</span></span>


```C++
HANDLE m_hThread;
```



## <a name="remarks"></a><span data-ttu-id="c9608-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c9608-106">Remarks</span></span>

<span data-ttu-id="c9608-107">Esta variable se inicializa como **null**.</span><span class="sxs-lookup"><span data-stu-id="c9608-107">This variable is initialized as **NULL**.</span></span> <span data-ttu-id="c9608-108">El método [**CAMThread:: Create**](camthread-create.md) establece esta variable en el identificador del subproceso.</span><span class="sxs-lookup"><span data-stu-id="c9608-108">The [**CAMThread::Create**](camthread-create.md) method sets this variable to the thread handle.</span></span> <span data-ttu-id="c9608-109">Para determinar si el subproceso existe, llame al método [**CAMThread:: ThreadExists**](camthread-threadexists.md) .</span><span class="sxs-lookup"><span data-stu-id="c9608-109">To determine whether the thread exists, call the [**CAMThread::ThreadExists**](camthread-threadexists.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9608-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9608-110">Requirements</span></span>



| <span data-ttu-id="c9608-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9608-111">Requirement</span></span> | <span data-ttu-id="c9608-112">Value</span><span class="sxs-lookup"><span data-stu-id="c9608-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9608-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9608-113">Header</span></span><br/>  | <dl> <span data-ttu-id="c9608-114"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9608-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c9608-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c9608-115">Library</span></span><br/> | <dl> <span data-ttu-id="c9608-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c9608-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9608-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9608-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9608-118">**Clase CAMThread**</span><span class="sxs-lookup"><span data-stu-id="c9608-118">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




