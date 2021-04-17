---
description: El método SetSyncSource establece el reloj usado para el control de tiempo.
ms.assetid: 646d4d24-f9b7-438a-b842-58e90eb6a945
title: Método CCmdQueue. SetSyncSource (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 995df3afa5185d8f50278899ac6a5d67dc6d230e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660128"
---
# <a name="ccmdqueuesetsyncsource-method"></a><span data-ttu-id="0f04a-103">CCmdQueue. SetSyncSource, método</span><span class="sxs-lookup"><span data-stu-id="0f04a-103">CCmdQueue.SetSyncSource method</span></span>

<span data-ttu-id="0f04a-104">El `SetSyncSource` método establece el reloj usado para el control de tiempo.</span><span class="sxs-lookup"><span data-stu-id="0f04a-104">The `SetSyncSource` method sets the clock used for timing.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f04a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f04a-105">Syntax</span></span>


```C++
virtual HRESULT SetSyncSource(
   IReferenceClock *pIrc
);
```



## <a name="parameters"></a><span data-ttu-id="0f04a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f04a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f04a-107">*pIrc*</span><span class="sxs-lookup"><span data-stu-id="0f04a-107">*pIrc*</span></span> 
</dt> <dd>

<span data-ttu-id="0f04a-108">Puntero a la interfaz [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) .</span><span class="sxs-lookup"><span data-stu-id="0f04a-108">Pointer to the [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f04a-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0f04a-109">Return value</span></span>

<span data-ttu-id="0f04a-110">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="0f04a-110">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f04a-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f04a-111">Requirements</span></span>



| <span data-ttu-id="0f04a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f04a-112">Requirement</span></span> | <span data-ttu-id="0f04a-113">Value</span><span class="sxs-lookup"><span data-stu-id="0f04a-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f04a-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f04a-114">Header</span></span><br/>  | <dl> <span data-ttu-id="0f04a-115"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0f04a-115"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0f04a-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0f04a-116">Library</span></span><br/> | <dl> <span data-ttu-id="0f04a-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0f04a-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f04a-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f04a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f04a-119">**Clase CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="0f04a-119">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




