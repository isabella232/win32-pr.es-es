---
description: Crea un subproceso.
ms.assetid: 40785522-dc6e-41af-8b27-9e8875a0dd84
title: Método CMsgThread. CreateThread (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.CreateThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8951995de18158fe4d1e5f84b1d98da701067ab6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670989"
---
# <a name="cmsgthreadcreatethread-method"></a><span data-ttu-id="e09a6-103">CMsgThread. CreateThread (método)</span><span class="sxs-lookup"><span data-stu-id="e09a6-103">CMsgThread.CreateThread method</span></span>

<span data-ttu-id="e09a6-104">Crea un subproceso.</span><span class="sxs-lookup"><span data-stu-id="e09a6-104">Creates a thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="e09a6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e09a6-105">Syntax</span></span>


```C++
BOOL CreateThread();
```



## <a name="parameters"></a><span data-ttu-id="e09a6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e09a6-106">Parameters</span></span>

<span data-ttu-id="e09a6-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e09a6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e09a6-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e09a6-108">Return value</span></span>

<span data-ttu-id="e09a6-109">Devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="e09a6-109">Returns one of the following values.</span></span>



| <span data-ttu-id="e09a6-110">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e09a6-110">Return code</span></span>                                                                              | <span data-ttu-id="e09a6-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e09a6-111">Description</span></span>                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="e09a6-112"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="e09a6-112"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>  | <span data-ttu-id="e09a6-113">El subproceso se ha creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e09a6-113">Thread was successfully created.</span></span><br/>     |
| <dl> <span data-ttu-id="e09a6-114"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="e09a6-114"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="e09a6-115">El subproceso no se creó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e09a6-115">Thread was not successfully created.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e09a6-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e09a6-116">Remarks</span></span>

<span data-ttu-id="e09a6-117">El subproceso creará un bucle, se bloqueará hasta que una solicitud se pone en cola (a través de la función miembro [**CMsgThread::P utthreadmsg**](cmsgthread-putthreadmsg.md) ) y, a continuación, llama a la función miembro [**CMsgThread:: ThreadMessageProc**](cmsgthread-threadmessageproc.md) con cada mensaje.</span><span class="sxs-lookup"><span data-stu-id="e09a6-117">The thread will loop, blocking until a request is queued (through the [**CMsgThread::PutThreadMsg**](cmsgthread-putthreadmsg.md) member function) and then calling the [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) member function with each message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e09a6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e09a6-118">Requirements</span></span>



| <span data-ttu-id="e09a6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e09a6-119">Requirement</span></span> | <span data-ttu-id="e09a6-120">Value</span><span class="sxs-lookup"><span data-stu-id="e09a6-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e09a6-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e09a6-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e09a6-122"><dt>Msgthrd. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e09a6-122"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e09a6-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e09a6-123">Library</span></span><br/> | <dl> <span data-ttu-id="e09a6-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e09a6-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e09a6-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e09a6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e09a6-126">**Clase CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="e09a6-126">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




