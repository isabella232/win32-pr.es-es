---
description: El método CancelNotification cancela el evento de temporizador que programa la representación.
ms.assetid: 56ddf692-a2e3-40f2-848f-2d592601ec00
title: Método CBaseRenderer. CancelNotification (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CancelNotification
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3330f369c5fcc45fe051a1964a504d5d40fcd091
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671079"
---
# <a name="cbaserenderercancelnotification-method"></a><span data-ttu-id="39c4d-103">CBaseRenderer. CancelNotification, método</span><span class="sxs-lookup"><span data-stu-id="39c4d-103">CBaseRenderer.CancelNotification method</span></span>

<span data-ttu-id="39c4d-104">El `CancelNotification` método cancela el evento de temporizador que programa la representación.</span><span class="sxs-lookup"><span data-stu-id="39c4d-104">The `CancelNotification` method cancels the timer event that schedules rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="39c4d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39c4d-105">Syntax</span></span>


```C++
virtual HRESULT CancelNotification();
```



## <a name="parameters"></a><span data-ttu-id="39c4d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39c4d-106">Parameters</span></span>

<span data-ttu-id="39c4d-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="39c4d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="39c4d-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39c4d-108">Return value</span></span>

<span data-ttu-id="39c4d-109">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="39c4d-109">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="39c4d-110">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="39c4d-110">Return code</span></span>                                                                             | <span data-ttu-id="39c4d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="39c4d-111">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="39c4d-112"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="39c4d-112"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="39c4d-113">No había ningún evento de temporizador pendiente.</span><span class="sxs-lookup"><span data-stu-id="39c4d-113">There was no pending timer event.</span></span><br/> |
| <dl> <span data-ttu-id="39c4d-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="39c4d-114"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="39c4d-115">Correcto.</span><span class="sxs-lookup"><span data-stu-id="39c4d-115">Success.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="39c4d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="39c4d-116">Remarks</span></span>

<span data-ttu-id="39c4d-117">El filtro llama a este método cuando se detiene el streaming.</span><span class="sxs-lookup"><span data-stu-id="39c4d-117">The filter calls this method when streaming stops.</span></span> <span data-ttu-id="39c4d-118">El método cancela cualquier representación programada.</span><span class="sxs-lookup"><span data-stu-id="39c4d-118">The method cancels any scheduled rendering.</span></span>

## <a name="requirements"></a><span data-ttu-id="39c4d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39c4d-119">Requirements</span></span>



| <span data-ttu-id="39c4d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="39c4d-120">Requirement</span></span> | <span data-ttu-id="39c4d-121">Value</span><span class="sxs-lookup"><span data-stu-id="39c4d-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39c4d-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39c4d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="39c4d-123"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="39c4d-123"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="39c4d-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="39c4d-124">Library</span></span><br/> | <dl> <span data-ttu-id="39c4d-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="39c4d-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39c4d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="39c4d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39c4d-127">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="39c4d-127">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




