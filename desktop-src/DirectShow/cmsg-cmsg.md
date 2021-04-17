---
description: Construye un objeto CMsg.
ms.assetid: b7ee0643-73e4-450d-bff4-ca5006fdcc14
title: Constructor CMsg. CMsg (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsg.CMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b26a9572b51d4a476b70c3dd7ddae8c896a4d648
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680350"
---
# <a name="cmsgcmsg-constructor"></a><span data-ttu-id="11c1a-103">Constructor CMsg. CMsg</span><span class="sxs-lookup"><span data-stu-id="11c1a-103">CMsg.CMsg constructor</span></span>

<span data-ttu-id="11c1a-104">Construye un objeto [**CMsg**](cmsg.md) .</span><span class="sxs-lookup"><span data-stu-id="11c1a-104">Constructs a [**CMsg**](cmsg.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="11c1a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11c1a-105">Syntax</span></span>


```C++
CMsg(
   UINT     u,
   DWORD    dw,
   LPVOID   lp,
   CAMEvent *pEvent
);
```



## <a name="parameters"></a><span data-ttu-id="11c1a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11c1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11c1a-107">*u*</span><span class="sxs-lookup"><span data-stu-id="11c1a-107">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="11c1a-108">Código de solicitud, definido por el cliente de la clase de subproceso y comprensible por la función de subproceso de trabajo invalidada.</span><span class="sxs-lookup"><span data-stu-id="11c1a-108">Request code, defined by the client of the thread class and understood by the overridden worker thread function.</span></span>

</dd> <dt>

<span data-ttu-id="11c1a-109">*dw*</span><span class="sxs-lookup"><span data-stu-id="11c1a-109">*dw*</span></span> 
</dt> <dd>

<span data-ttu-id="11c1a-110">Parámetro de marca para el código de solicitud.</span><span class="sxs-lookup"><span data-stu-id="11c1a-110">Flag parameter to the request code.</span></span>

</dd> <dt>

<span data-ttu-id="11c1a-111">*LP*</span><span class="sxs-lookup"><span data-stu-id="11c1a-111">*lp*</span></span> 
</dt> <dd>

<span data-ttu-id="11c1a-112">Puntero a los datos requeridos por el subproceso de trabajo como parámetros o valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="11c1a-112">Pointer to data required by the worker thread as parameter or return values.</span></span> <span data-ttu-id="11c1a-113">Estos datos no deberían estar basados en la pila, ya que se hará referencia a él después de completar la operación de puesta en cola.</span><span class="sxs-lookup"><span data-stu-id="11c1a-113">This data should not be stack-based, as it will be referenced some time after completing the queuing operation.</span></span>

</dd> <dt>

<span data-ttu-id="11c1a-114">*As*</span><span class="sxs-lookup"><span data-stu-id="11c1a-114">*pEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="11c1a-115">Puntero al objeto de evento que un subproceso de trabajo puede señalar para indicar la finalización de la operación.</span><span class="sxs-lookup"><span data-stu-id="11c1a-115">Pointer to the event object that a worker thread can signal to indicate the completion of the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="11c1a-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11c1a-116">Remarks</span></span>

<span data-ttu-id="11c1a-117">Esta función miembro contiene una solicitud para que un subproceso de trabajo de [**CMsgThread**](cmsgthread.md) actúe.</span><span class="sxs-lookup"><span data-stu-id="11c1a-117">This member function contains a request for a [**CMsgThread**](cmsgthread.md) worker thread to act on.</span></span> <span data-ttu-id="11c1a-118">Todos los parámetros se pasan a la función de subproceso de trabajo como parámetros cuando se procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="11c1a-118">All the parameters are passed to the worker thread function as parameters when this message gets processed.</span></span> <span data-ttu-id="11c1a-119">Los significados de los parámetros se definen mediante la función de cliente que llama al subproceso de trabajo y la clase derivada que proporciona la función de ejecución del subproceso de trabajo.</span><span class="sxs-lookup"><span data-stu-id="11c1a-119">The meanings of the parameters are defined by the client function that calls the worker thread and the derived class that supplies the worker thread's execution function.</span></span>

## <a name="requirements"></a><span data-ttu-id="11c1a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11c1a-120">Requirements</span></span>



| <span data-ttu-id="11c1a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="11c1a-121">Requirement</span></span> | <span data-ttu-id="11c1a-122">Value</span><span class="sxs-lookup"><span data-stu-id="11c1a-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11c1a-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11c1a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="11c1a-124"><dt>Msgthrd. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11c1a-124"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="11c1a-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="11c1a-125">Library</span></span><br/> | <dl> <span data-ttu-id="11c1a-126"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="11c1a-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




