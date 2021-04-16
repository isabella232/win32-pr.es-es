---
description: El método SetPopEvent especifica un evento que se señaliza cada vez que el objeto quita un ejemplo de la cola.
ms.assetid: 147a09b9-14d3-4739-843a-1bfb19d2d052
title: Método COutputQueue. SetPopEvent (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.SetPopEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 764abf76265fce66c5798923ca1fa522edd682af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678971"
---
# <a name="coutputqueuesetpopevent-method"></a><span data-ttu-id="3d020-103">COutputQueue. SetPopEvent, método</span><span class="sxs-lookup"><span data-stu-id="3d020-103">COutputQueue.SetPopEvent method</span></span>

<span data-ttu-id="3d020-104">El `SetPopEvent` método especifica un evento que se señaliza cada vez que el objeto quita un ejemplo de la cola.</span><span class="sxs-lookup"><span data-stu-id="3d020-104">The `SetPopEvent` method specifies an event that is signaled whenever the object removes a sample from the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d020-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d020-105">Syntax</span></span>


```C++
void SetPopEvent(
   HANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="3d020-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d020-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d020-107">*hEvent*</span><span class="sxs-lookup"><span data-stu-id="3d020-107">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="3d020-108">Identificador de un evento creado por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="3d020-108">Handle to an event created by the caller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d020-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d020-109">Return value</span></span>

<span data-ttu-id="3d020-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3d020-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d020-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d020-111">Requirements</span></span>



| <span data-ttu-id="3d020-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d020-112">Requirement</span></span> | <span data-ttu-id="3d020-113">Value</span><span class="sxs-lookup"><span data-stu-id="3d020-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d020-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3d020-114">Header</span></span><br/>  | <dl> <span data-ttu-id="3d020-115"><dt>Outputq. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d020-115"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3d020-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3d020-116">Library</span></span><br/> | <dl> <span data-ttu-id="3d020-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3d020-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d020-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d020-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d020-119">**Clase COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="3d020-119">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




