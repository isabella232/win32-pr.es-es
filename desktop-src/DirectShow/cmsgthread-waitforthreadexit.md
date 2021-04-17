---
description: Se bloquea hasta que el subproceso se cierra.
ms.assetid: 1ee547b5-cd73-4ce8-8e66-c2062714d0f0
title: Método CMsgThread. WaitForThreadExit (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.WaitForThreadExit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8b48573c4297a2d5d5d008eba88fd8ea437333c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671219"
---
# <a name="cmsgthreadwaitforthreadexit-method"></a><span data-ttu-id="79b06-103">CMsgThread. WaitForThreadExit, método</span><span class="sxs-lookup"><span data-stu-id="79b06-103">CMsgThread.WaitForThreadExit method</span></span>

<span data-ttu-id="79b06-104">Se bloquea hasta que el subproceso se cierra.</span><span class="sxs-lookup"><span data-stu-id="79b06-104">Blocks until the thread exits.</span></span>

## <a name="syntax"></a><span data-ttu-id="79b06-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79b06-105">Syntax</span></span>


```C++
BOOL WaitForThreadExit(
   LPDWORD lpdwExitCode
);
```



## <a name="parameters"></a><span data-ttu-id="79b06-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79b06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79b06-107">*lpdwExitCode*</span><span class="sxs-lookup"><span data-stu-id="79b06-107">*lpdwExitCode*</span></span> 
</dt> <dd>

<span data-ttu-id="79b06-108">Puntero al código de salida devuelto por el subproceso.</span><span class="sxs-lookup"><span data-stu-id="79b06-108">Pointer to the exit code returned by the thread.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79b06-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79b06-109">Return value</span></span>

<span data-ttu-id="79b06-110">Devuelve **true** o **false**, cuyo significado viene determinado por la clase que proporciona la función miembro [**CMsgThread:: ThreadMessageProc**](cmsgthread-threadmessageproc.md) reemplazada y la función miembro que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="79b06-110">Returns either **TRUE** or **FALSE**, the meaning of which is determined by the class supplying the overridden [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) member function and the calling member function.</span></span>

## <a name="remarks"></a><span data-ttu-id="79b06-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79b06-111">Remarks</span></span>

<span data-ttu-id="79b06-112">Asegúrese de que el subproceso de trabajo se ha cerrado completamente antes de completar la destrucción de la clase derivada. de lo contrario, es posible que el subproceso se siga ejecutando después de que se haya descargado la biblioteca de vínculos dinámicos (DLL) del espacio de direcciones del proceso.</span><span class="sxs-lookup"><span data-stu-id="79b06-112">Ensure that the worker thread has exited completely before completing the destruction of your derived class; otherwise, the thread might still execute after your dynamic-link library (DLL) has been unloaded from the address space of the process.</span></span> <span data-ttu-id="79b06-113">Incluso si la única instrucción que se deja de salir es una instrucción de devolución única, se produciría una excepción.</span><span class="sxs-lookup"><span data-stu-id="79b06-113">Even if the only instruction left to exit is a single-return instruction, this would cause an exception.</span></span> <span data-ttu-id="79b06-114">La única manera confiable de asegurarse de que el subproceso ha salido es indicar al subproceso que salga (mediante un objeto [**CMsg**](cmsg.md) negociado de forma privada enviado a la función miembro [**CMsgThread::P utthreadmsg**](cmsgthread-putthreadmsg.md) ) y, a continuación, llamar a esta función miembro.</span><span class="sxs-lookup"><span data-stu-id="79b06-114">The only reliable way to ensure that the thread has exited is to signal the thread to exit (using a privately negotiated [**CMsg**](cmsg.md) object sent to the [**CMsgThread::PutThreadMsg**](cmsgthread-putthreadmsg.md) member function) and then call this member function.</span></span> <span data-ttu-id="79b06-115">Debe hacerlo en el destructor de la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="79b06-115">You should do this in the destructor for your derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="79b06-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79b06-116">Requirements</span></span>



| <span data-ttu-id="79b06-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="79b06-117">Requirement</span></span> | <span data-ttu-id="79b06-118">Value</span><span class="sxs-lookup"><span data-stu-id="79b06-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79b06-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79b06-119">Header</span></span><br/>  | <dl> <span data-ttu-id="79b06-120"><dt>Msgthrd. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="79b06-120"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="79b06-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="79b06-121">Library</span></span><br/> | <dl> <span data-ttu-id="79b06-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="79b06-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79b06-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="79b06-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79b06-124">**Clase CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="79b06-124">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




