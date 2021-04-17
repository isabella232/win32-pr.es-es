---
description: Método de constructor.
ms.assetid: 3f758c45-21ec-4728-ba7d-41da7b2fa02f
title: Constructor CMsgThread. CMsgThread (Msgthrd. h)
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
ms.openlocfilehash: e77d3a84e349ab370b6319cd973f6ba86d632366
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680348"
---
# <a name="cmsgthreadcmsgthread-constructor"></a><span data-ttu-id="cd863-103">Constructor CMsgThread. CMsgThread</span><span class="sxs-lookup"><span data-stu-id="cd863-103">CMsgThread.CMsgThread constructor</span></span>

<span data-ttu-id="cd863-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="cd863-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd863-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd863-105">Syntax</span></span>


```C++
CMsgThread();
```



## <a name="parameters"></a><span data-ttu-id="cd863-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd863-106">Parameters</span></span>

<span data-ttu-id="cd863-107">Este constructor no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="cd863-107">This constructor has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd863-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd863-108">Remarks</span></span>

<span data-ttu-id="cd863-109">La construcción de un objeto de subproceso de mensaje no crea automáticamente el subproceso.</span><span class="sxs-lookup"><span data-stu-id="cd863-109">Constructing a message thread object does not automatically create the thread.</span></span> <span data-ttu-id="cd863-110">Debe llamar a la función miembro [**CMsgThread:: CreateThread**](cmsgthread-createthread.md) para crear el subproceso.</span><span class="sxs-lookup"><span data-stu-id="cd863-110">You must call the [**CMsgThread::CreateThread**](cmsgthread-createthread.md) member function to create the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd863-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd863-111">Requirements</span></span>



| <span data-ttu-id="cd863-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd863-112">Requirement</span></span> | <span data-ttu-id="cd863-113">Value</span><span class="sxs-lookup"><span data-stu-id="cd863-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd863-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cd863-114">Header</span></span><br/>  | <dl> <span data-ttu-id="cd863-115"><dt>Msgthrd. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd863-115"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cd863-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cd863-116">Library</span></span><br/> | <dl> <span data-ttu-id="cd863-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="cd863-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd863-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd863-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd863-119">**Clase CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="cd863-119">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




