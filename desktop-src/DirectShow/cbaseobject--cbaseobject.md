---
description: Método de destructor.
ms.assetid: 3714d030-f0bd-4826-a3c5-fc206bb88561
title: Destructor CBaseObject. ~ CBaseObject (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject.~CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 908f335105fa88f3ed547eed0e92ea50a6f85f26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660286"
---
# <a name="cbaseobjectcbaseobject-destructor"></a><span data-ttu-id="0b0d6-103">CBaseObject. ~ CBaseObject (destructor)</span><span class="sxs-lookup"><span data-stu-id="0b0d6-103">CBaseObject.~CBaseObject destructor</span></span>

<span data-ttu-id="0b0d6-104">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="0b0d6-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b0d6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b0d6-105">Syntax</span></span>


```C++
~CBaseObject();
```



## <a name="remarks"></a><span data-ttu-id="0b0d6-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0b0d6-106">Remarks</span></span>

<span data-ttu-id="0b0d6-107">Este método disminuye el recuento de objetos activos.</span><span class="sxs-lookup"><span data-stu-id="0b0d6-107">This method decrements the active-object count.</span></span> <span data-ttu-id="0b0d6-108">(Vea [**CBaseObject:: ObjectsActive**](cbaseobject-objectsactive.md)).</span><span class="sxs-lookup"><span data-stu-id="0b0d6-108">(See [**CBaseObject::ObjectsActive**](cbaseobject-objectsactive.md).)</span></span>

## <a name="requirements"></a><span data-ttu-id="0b0d6-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b0d6-109">Requirements</span></span>



| <span data-ttu-id="0b0d6-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b0d6-110">Requirement</span></span> | <span data-ttu-id="0b0d6-111">Value</span><span class="sxs-lookup"><span data-stu-id="0b0d6-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b0d6-112">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b0d6-112">Header</span></span><br/>  | <dl> <span data-ttu-id="0b0d6-113"><dt>ComBase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0b0d6-113"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0b0d6-114">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0b0d6-114">Library</span></span><br/> | <dl> <span data-ttu-id="0b0d6-115"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0b0d6-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b0d6-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b0d6-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b0d6-117">**Clase CBaseObject**</span><span class="sxs-lookup"><span data-stu-id="0b0d6-117">**CBaseObject Class**</span></span>](cbaseobject.md)
</dt> </dl>

 

 




