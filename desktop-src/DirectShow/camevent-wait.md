---
description: El método wait se bloquea hasta que se señale el evento o hasta que se agote el tiempo de espera.
ms.assetid: bcc13723-a59b-4e8a-bfc8-eadb6facf116
title: Método CAMEvent. Wait (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Wait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ab5bc2aabf77fb73739528e99cda7961ae87e9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661053"
---
# <a name="cameventwait-method"></a><span data-ttu-id="9d669-103">CAMEvent. Wait (método)</span><span class="sxs-lookup"><span data-stu-id="9d669-103">CAMEvent.Wait method</span></span>

<span data-ttu-id="9d669-104">El `Wait` método se bloquea hasta que se señale el evento o hasta que se agote el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="9d669-104">The `Wait` method blocks until the event is signaled, or until a time-out occurs.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d669-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9d669-105">Syntax</span></span>


```C++
BOOL Wait(
   DWORD dwTimeout = INFINITE
);
```



## <a name="parameters"></a><span data-ttu-id="9d669-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9d669-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d669-107">*dwTimeout*</span><span class="sxs-lookup"><span data-stu-id="9d669-107">*dwTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="9d669-108">Valor de tiempo de espera opcional, representado en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="9d669-108">Optional time-out value, represented in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d669-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9d669-109">Return value</span></span>

<span data-ttu-id="9d669-110">Devuelve **true** si el evento se señala.</span><span class="sxs-lookup"><span data-stu-id="9d669-110">Returns **TRUE** if the event is signaled.</span></span> <span data-ttu-id="9d669-111">De lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="9d669-111">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d669-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9d669-112">Remarks</span></span>

<span data-ttu-id="9d669-113">En el caso de los eventos de restablecimiento automático, el evento se restablece a un estado no señalizado cuando este método devuelve.</span><span class="sxs-lookup"><span data-stu-id="9d669-113">For auto-reset events, the event is reset to a nonsignaled state when this method returns.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d669-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d669-114">Requirements</span></span>



| <span data-ttu-id="9d669-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d669-115">Requirement</span></span> | <span data-ttu-id="9d669-116">Value</span><span class="sxs-lookup"><span data-stu-id="9d669-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d669-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9d669-117">Header</span></span><br/>  | <dl> <span data-ttu-id="9d669-118"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d669-118"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9d669-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9d669-119">Library</span></span><br/> | <dl> <span data-ttu-id="9d669-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9d669-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d669-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d669-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d669-122">**Clase CAMEvent**</span><span class="sxs-lookup"><span data-stu-id="9d669-122">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




