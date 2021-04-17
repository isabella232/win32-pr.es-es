---
description: La función WaitDispatchingMessages espera a que se señalice un objeto, mientras se envían mensajes de ventana.
ms.assetid: d15f6736-d141-47a3-b767-fbf774982fb4
title: Función WaitDispatchingMessages (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WaitDispatchingMessages
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e509a081243f28293dc2d8abf8311f69eaf9a44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690249"
---
# <a name="waitdispatchingmessages-function"></a><span data-ttu-id="55307-103">WaitDispatchingMessages función)</span><span class="sxs-lookup"><span data-stu-id="55307-103">WaitDispatchingMessages function</span></span>

<span data-ttu-id="55307-104">La `WaitDispatchingMessages` función espera a que se señale un objeto mientras se envían mensajes de ventana.</span><span class="sxs-lookup"><span data-stu-id="55307-104">The `WaitDispatchingMessages` function waits for an object to be signaled, while dispatching window messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="55307-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55307-105">Syntax</span></span>


```C++
DWORD WINAPI WaitDispatchingMessages(
   HANDLE hObject,
   DWORD  dwWait,
   HWND   hwnd = NULL,
   UINT   uMsg = 0,
   HANDLE hEvent = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="55307-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55307-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55307-107">*hObject*</span><span class="sxs-lookup"><span data-stu-id="55307-107">*hObject*</span></span> 
</dt> <dd>

<span data-ttu-id="55307-108">Identificador del objeto que se va a esperar.</span><span class="sxs-lookup"><span data-stu-id="55307-108">Handle of the object to wait for.</span></span>

</dd> <dt>

<span data-ttu-id="55307-109">*dwWait*</span><span class="sxs-lookup"><span data-stu-id="55307-109">*dwWait*</span></span> 
</dt> <dd>

<span data-ttu-id="55307-110">Intervalo de tiempo de espera, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="55307-110">Time-out interval, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="55307-111">*identificador*</span><span class="sxs-lookup"><span data-stu-id="55307-111">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="55307-112">Identificador opcional de una ventana.</span><span class="sxs-lookup"><span data-stu-id="55307-112">Optional handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="55307-113">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="55307-113">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="55307-114">Mensaje de ventana opcional que especifica un mensaje para enviar.</span><span class="sxs-lookup"><span data-stu-id="55307-114">Optional window message, specifying a message to dispatch.</span></span>

</dd> <dt>

<span data-ttu-id="55307-115">*hEvent*</span><span class="sxs-lookup"><span data-stu-id="55307-115">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="55307-116">Identificador opcional de un evento que se va a esperar.</span><span class="sxs-lookup"><span data-stu-id="55307-116">Optional handle to an event to wait for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55307-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55307-117">Return value</span></span>

<span data-ttu-id="55307-118">Devuelve el valor de la función **WaitForMultipleObjects** .</span><span class="sxs-lookup"><span data-stu-id="55307-118">Returns the value from the **WaitForMultipleObjects** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="55307-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55307-119">Remarks</span></span>

<span data-ttu-id="55307-120">Si un objeto posee una ventana, debe enviar los mensajes de ventana mientras se espera.</span><span class="sxs-lookup"><span data-stu-id="55307-120">If an object owns a window, it should dispatch window messages while waiting.</span></span> <span data-ttu-id="55307-121">Esta función permite al objeto esperar a un evento, semáforo u otro objeto de exclusión mutua durante el envío de mensajes.</span><span class="sxs-lookup"><span data-stu-id="55307-121">This function enables the object to wait for an event, semaphore, or other mutual exclusion object while dispatching messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="55307-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55307-122">Requirements</span></span>



| <span data-ttu-id="55307-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="55307-123">Requirement</span></span> | <span data-ttu-id="55307-124">Value</span><span class="sxs-lookup"><span data-stu-id="55307-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55307-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55307-125">Header</span></span><br/>  | <dl> <span data-ttu-id="55307-126"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="55307-126"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="55307-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="55307-127">Library</span></span><br/> | <dl> <span data-ttu-id="55307-128"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="55307-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55307-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="55307-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55307-130">Funciones auxiliares misceláneas</span><span class="sxs-lookup"><span data-stu-id="55307-130">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




