---
description: Proporciona la inicialización en un subproceso.
ms.assetid: a9c330bb-0a2b-45bf-9b24-d03dd61d7dbf
title: Método CMsgThread. OnThreadInit (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.OnThreadInit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 80e15d6430da77c0f22f5566375394b8fe6994ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679214"
---
# <a name="cmsgthreadonthreadinit-method"></a><span data-ttu-id="2b6fb-103">CMsgThread. OnThreadInit, método</span><span class="sxs-lookup"><span data-stu-id="2b6fb-103">CMsgThread.OnThreadInit method</span></span>

<span data-ttu-id="2b6fb-104">Proporciona la inicialización en un subproceso.</span><span class="sxs-lookup"><span data-stu-id="2b6fb-104">Provides initialization on a thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b6fb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b6fb-105">Syntax</span></span>


```C++
virtual void OnThreadInit();
```



## <a name="parameters"></a><span data-ttu-id="2b6fb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b6fb-106">Parameters</span></span>

<span data-ttu-id="2b6fb-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2b6fb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2b6fb-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b6fb-108">Return value</span></span>

<span data-ttu-id="2b6fb-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2b6fb-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b6fb-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b6fb-110">Remarks</span></span>

<span data-ttu-id="2b6fb-111">Invalide esta función si desea realizar su propia inicialización específica en el inicio del subproceso.</span><span class="sxs-lookup"><span data-stu-id="2b6fb-111">Override this function if you want to do your own specific initialization on thread startup.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b6fb-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b6fb-112">Requirements</span></span>



| <span data-ttu-id="2b6fb-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b6fb-113">Requirement</span></span> | <span data-ttu-id="2b6fb-114">Value</span><span class="sxs-lookup"><span data-stu-id="2b6fb-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b6fb-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2b6fb-115">Header</span></span><br/>  | <dl> <span data-ttu-id="2b6fb-116"><dt>Msgthrd. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2b6fb-116"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2b6fb-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2b6fb-117">Library</span></span><br/> | <dl> <span data-ttu-id="2b6fb-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2b6fb-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b6fb-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b6fb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b6fb-120">**Clase CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="2b6fb-120">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




