---
description: El método IsIdle determina si el objeto está esperando los datos.
ms.assetid: be1b5633-f9e9-497e-8b6f-5634eae91273
title: Método COutputQueue. IsIdle (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsIdle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9bf8b42189e356659e74398eaa3eefeb5f771a8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671310"
---
# <a name="coutputqueueisidle-method"></a><span data-ttu-id="f33a6-103">COutputQueue. IsIdle, método</span><span class="sxs-lookup"><span data-stu-id="f33a6-103">COutputQueue.IsIdle method</span></span>

<span data-ttu-id="f33a6-104">El `IsIdle` método determina si el objeto está esperando los datos.</span><span class="sxs-lookup"><span data-stu-id="f33a6-104">The `IsIdle` method determines whether the object is waiting for data.</span></span>

## <a name="syntax"></a><span data-ttu-id="f33a6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f33a6-105">Syntax</span></span>


```C++
BOOL IsIdle();
```



## <a name="parameters"></a><span data-ttu-id="f33a6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f33a6-106">Parameters</span></span>

<span data-ttu-id="f33a6-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f33a6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f33a6-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f33a6-108">Return value</span></span>

<span data-ttu-id="f33a6-109">Devuelve **true** si el subproceso está esperando y la matriz de ejemplo está vacía.</span><span class="sxs-lookup"><span data-stu-id="f33a6-109">Returns **TRUE** if the thread is waiting and the sample array is empty.</span></span> <span data-ttu-id="f33a6-110">De lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="f33a6-110">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f33a6-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f33a6-111">Requirements</span></span>



| <span data-ttu-id="f33a6-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f33a6-112">Requirement</span></span> | <span data-ttu-id="f33a6-113">Value</span><span class="sxs-lookup"><span data-stu-id="f33a6-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f33a6-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f33a6-114">Header</span></span><br/>  | <dl> <span data-ttu-id="f33a6-115"><dt>Outputq. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f33a6-115"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f33a6-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f33a6-116">Library</span></span><br/> | <dl> <span data-ttu-id="f33a6-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f33a6-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f33a6-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="f33a6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f33a6-119">**Clase COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="f33a6-119">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




