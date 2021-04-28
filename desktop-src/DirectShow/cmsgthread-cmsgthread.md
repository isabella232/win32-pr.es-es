---
description: 'Constructor CMsgThread.CMsgThread: método constructor.'
ms.assetid: 3f758c45-21ec-4728-ba7d-41da7b2fa02f
title: Constructor CMsgThread.CMsgThread (Msgthrd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.CMsgThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08d76ebecd09d95b7ba0fca22b300c1e402f5302
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095373"
---
# <a name="cmsgthreadcmsgthread-constructor"></a><span data-ttu-id="b8695-103">Constructor CMsgThread.CMsgThread</span><span class="sxs-lookup"><span data-stu-id="b8695-103">CMsgThread.CMsgThread constructor</span></span>

<span data-ttu-id="b8695-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="b8695-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8695-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8695-105">Syntax</span></span>


```C++
CMsgThread();
```



## <a name="parameters"></a><span data-ttu-id="b8695-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8695-106">Parameters</span></span>

<span data-ttu-id="b8695-107">Este constructor no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b8695-107">This constructor has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8695-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b8695-108">Remarks</span></span>

<span data-ttu-id="b8695-109">La construcción de un objeto de subproceso de mensaje no crea automáticamente el subproceso.</span><span class="sxs-lookup"><span data-stu-id="b8695-109">Constructing a message thread object does not automatically create the thread.</span></span> <span data-ttu-id="b8695-110">Debe llamar a la [**función miembro CMsgThread::CreateThread**](cmsgthread-createthread.md) para crear el subproceso.</span><span class="sxs-lookup"><span data-stu-id="b8695-110">You must call the [**CMsgThread::CreateThread**](cmsgthread-createthread.md) member function to create the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8695-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8695-111">Requirements</span></span>



| <span data-ttu-id="b8695-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8695-112">Requirement</span></span> | <span data-ttu-id="b8695-113">Value</span><span class="sxs-lookup"><span data-stu-id="b8695-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8695-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b8695-114">Header</span></span><br/>  | <dl> <span data-ttu-id="b8695-115"><dt>Msgthrd.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="b8695-115"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b8695-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b8695-116">Library</span></span><br/> | <dl> <span data-ttu-id="b8695-117"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b8695-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8695-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b8695-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8695-119">**CMsgThread (clase)**</span><span class="sxs-lookup"><span data-stu-id="b8695-119">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




