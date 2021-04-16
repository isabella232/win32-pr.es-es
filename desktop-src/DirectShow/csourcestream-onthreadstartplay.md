---
description: Se llama al método OnThreadStartPlay al principio del método CSourceStream::D oBufferProcessingLoop.
ms.assetid: 16d3b28f-bfae-49af-b8e4-8cc8cb15ecab
title: CSourceStream. OnThreadStartPlay (método) (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadStartPlay
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 857f27ad39fb9169e1ef67253d5232c7cbc3dbb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690592"
---
# <a name="csourcestreamonthreadstartplay-method"></a><span data-ttu-id="4e346-103">CSourceStream. OnThreadStartPlay, método</span><span class="sxs-lookup"><span data-stu-id="4e346-103">CSourceStream.OnThreadStartPlay method</span></span>

<span data-ttu-id="4e346-104">`OnThreadStartPlay`Se llama al método al principio del método [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) .</span><span class="sxs-lookup"><span data-stu-id="4e346-104">The `OnThreadStartPlay` method is called at the start of the [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e346-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e346-105">Syntax</span></span>


```C++
virtual HRESULT OnThreadStartPlay();
```



## <a name="parameters"></a><span data-ttu-id="4e346-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4e346-106">Parameters</span></span>

<span data-ttu-id="4e346-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="4e346-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4e346-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4e346-108">Return value</span></span>

<span data-ttu-id="4e346-109">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="4e346-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e346-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e346-110">Remarks</span></span>

<span data-ttu-id="4e346-111">Este método no hace nada en la clase base; está disponible para que la clase derivada se invalide.</span><span class="sxs-lookup"><span data-stu-id="4e346-111">This method does nothing in the base class; it is available for the derived class to override.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e346-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e346-112">Requirements</span></span>



| <span data-ttu-id="4e346-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e346-113">Requirement</span></span> | <span data-ttu-id="4e346-114">Value</span><span class="sxs-lookup"><span data-stu-id="4e346-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e346-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4e346-115">Header</span></span><br/>  | <dl> <span data-ttu-id="4e346-116"><dt>Source. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e346-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4e346-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4e346-117">Library</span></span><br/> | <dl> <span data-ttu-id="4e346-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="4e346-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e346-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e346-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e346-120">**Clase CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="4e346-120">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




