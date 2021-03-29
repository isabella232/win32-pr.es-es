---
description: El método Run cambia al modo de ejecución para que se puedan ejecutar los comandos diferidos por tiempo de secuencia.
ms.assetid: c529ae84-c9b7-46f1-a1e4-716fc9e9df13
title: Método CCmdQueue. Run (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 424914e53a12ff0f43e8b7e2a3345c28d84437d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678957"
---
# <a name="ccmdqueuerun-method"></a><span data-ttu-id="0d592-103">CCmdQueue. Run (método)</span><span class="sxs-lookup"><span data-stu-id="0d592-103">CCmdQueue.Run method</span></span>

<span data-ttu-id="0d592-104">El `Run` método cambia al modo de ejecución para que se puedan ejecutar los comandos diferidos por tiempo de secuencia.</span><span class="sxs-lookup"><span data-stu-id="0d592-104">The `Run` method switches to running mode so that commands that are deferred by the stream time can be run.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d592-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d592-105">Syntax</span></span>


```C++
virtual HRESULT Run(
   REFERENCE_TIME tStreamTimeOffset
);
```



## <a name="parameters"></a><span data-ttu-id="0d592-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0d592-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d592-107">*tStreamTimeOffset*</span><span class="sxs-lookup"><span data-stu-id="0d592-107">*tStreamTimeOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="0d592-108">Hora de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="0d592-108">Offset time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d592-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0d592-109">Return value</span></span>

<span data-ttu-id="0d592-110">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="0d592-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d592-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0d592-111">Remarks</span></span>

<span data-ttu-id="0d592-112">Durante el modo de ejecución, se conoce la asignación del tiempo de espera de la presentación de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="0d592-112">During running mode, stream-time-to-presentation-time mapping is known.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d592-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d592-113">Requirements</span></span>



| <span data-ttu-id="0d592-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d592-114">Requirement</span></span> | <span data-ttu-id="0d592-115">Value</span><span class="sxs-lookup"><span data-stu-id="0d592-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d592-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d592-116">Header</span></span><br/>  | <dl> <span data-ttu-id="0d592-117"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0d592-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0d592-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0d592-118">Library</span></span><br/> | <dl> <span data-ttu-id="0d592-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0d592-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d592-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d592-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d592-121">**Clase CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="0d592-121">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




