---
description: El método SetTimeAdvise configura un evento de temporizador con el reloj de referencia.
ms.assetid: d0ab5c21-3585-413b-ba75-8591ed4527e4
title: Método CCmdQueue. SetTimeAdvise (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.SetTimeAdvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 24313b908f1271f270e28b08058c415ed82396fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678889"
---
# <a name="ccmdqueuesettimeadvise-method"></a><span data-ttu-id="35d8a-103">CCmdQueue. SetTimeAdvise, método</span><span class="sxs-lookup"><span data-stu-id="35d8a-103">CCmdQueue.SetTimeAdvise method</span></span>

<span data-ttu-id="35d8a-104">El `SetTimeAdvise` método configura un evento de temporizador con el reloj de referencia.</span><span class="sxs-lookup"><span data-stu-id="35d8a-104">The `SetTimeAdvise` method sets up a timer event with the reference clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="35d8a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35d8a-105">Syntax</span></span>


```C++
void SetTimeAdvise();
```



## <a name="parameters"></a><span data-ttu-id="35d8a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35d8a-106">Parameters</span></span>

<span data-ttu-id="35d8a-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="35d8a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="35d8a-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35d8a-108">Return value</span></span>

<span data-ttu-id="35d8a-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="35d8a-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="35d8a-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="35d8a-110">Remarks</span></span>

<span data-ttu-id="35d8a-111">Esta función miembro llama al método [**IReferenceClock:: AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) para configurar una notificación para el tiempo más antiguo necesario en la cola.</span><span class="sxs-lookup"><span data-stu-id="35d8a-111">This member function calls the [**IReferenceClock::AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) method to set up a notification for the earliest time required in the queue.</span></span> <span data-ttu-id="35d8a-112">Los comandos en tiempo de presentación que se difieren siempre se comprueban.</span><span class="sxs-lookup"><span data-stu-id="35d8a-112">Presentation-time commands that are deferred are always checked.</span></span> <span data-ttu-id="35d8a-113">Si el gráfico de filtros está en modo de ejecución, también se comprueban los comandos diferidos que usan el tiempo de flujo.</span><span class="sxs-lookup"><span data-stu-id="35d8a-113">If the filter graph is in running mode, deferred commands using stream time are also checked.</span></span>

## <a name="requirements"></a><span data-ttu-id="35d8a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35d8a-114">Requirements</span></span>



| <span data-ttu-id="35d8a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="35d8a-115">Requirement</span></span> | <span data-ttu-id="35d8a-116">Value</span><span class="sxs-lookup"><span data-stu-id="35d8a-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35d8a-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="35d8a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="35d8a-118"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35d8a-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="35d8a-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="35d8a-119">Library</span></span><br/> | <dl> <span data-ttu-id="35d8a-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="35d8a-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35d8a-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="35d8a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35d8a-122">**Clase CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="35d8a-122">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




