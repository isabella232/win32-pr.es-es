---
description: El método pStateLock recupera un puntero al objeto de sección crítica del filtro.
ms.assetid: 10a2e74b-a5aa-4d68-958e-d86f4b78037e
title: CSource. pStateLock (método) (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.pStateLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c0705584a513d64dfd1cd17075d95617234f7f8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690000"
---
# <a name="csourcepstatelock-method"></a><span data-ttu-id="f20fb-103">CSource. pStateLock, método</span><span class="sxs-lookup"><span data-stu-id="f20fb-103">CSource.pStateLock method</span></span>

<span data-ttu-id="f20fb-104">El método **pStateLock** recupera un puntero al objeto de sección crítica del filtro.</span><span class="sxs-lookup"><span data-stu-id="f20fb-104">The **pStateLock** method retrieves a pointer to the filter's critical section object.</span></span>

> [!Note]  
> <span data-ttu-id="f20fb-105">Aunque se denomina como una variable miembro, **pStateLock** es un método.</span><span class="sxs-lookup"><span data-stu-id="f20fb-105">Although named like a member variable, **pStateLock** is a method.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f20fb-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f20fb-106">Syntax</span></span>


```C++
CCritSec* pStateLock();
```



## <a name="parameters"></a><span data-ttu-id="f20fb-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f20fb-107">Parameters</span></span>

<span data-ttu-id="f20fb-108">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f20fb-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f20fb-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f20fb-109">Return value</span></span>

<span data-ttu-id="f20fb-110">Devuelve un puntero a la variable miembro [**CSource:: m \_ cStateLock**](csource-m-cstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="f20fb-110">Returns a pointer to the [**CSource::m\_cStateLock**](csource-m-cstatelock.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="f20fb-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f20fb-111">Requirements</span></span>



| <span data-ttu-id="f20fb-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f20fb-112">Requirement</span></span> | <span data-ttu-id="f20fb-113">Value</span><span class="sxs-lookup"><span data-stu-id="f20fb-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f20fb-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f20fb-114">Header</span></span><br/>  | <dl> <span data-ttu-id="f20fb-115"><dt>Source. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f20fb-115"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f20fb-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f20fb-116">Library</span></span><br/> | <dl> <span data-ttu-id="f20fb-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f20fb-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f20fb-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="f20fb-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f20fb-119">**Clase CSource**</span><span class="sxs-lookup"><span data-stu-id="f20fb-119">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




