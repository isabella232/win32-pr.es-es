---
description: 'Destructor CBaseObject.~CBaseObject: método Destructor.'
ms.assetid: 3714d030-f0bd-4826-a3c5-fc206bb88561
title: Destructor CBaseObject.~CBaseObject (Combase.h)
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
ms.openlocfilehash: 552dbcc764f335e639cb50e2e01411dee200068f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096243"
---
# <a name="cbaseobjectcbaseobject-destructor"></a><span data-ttu-id="3379f-103">Destructor CBaseObject.~CBaseObject</span><span class="sxs-lookup"><span data-stu-id="3379f-103">CBaseObject.~CBaseObject destructor</span></span>

<span data-ttu-id="3379f-104">Método destructor.</span><span class="sxs-lookup"><span data-stu-id="3379f-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3379f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3379f-105">Syntax</span></span>


```C++
~CBaseObject();
```



## <a name="remarks"></a><span data-ttu-id="3379f-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3379f-106">Remarks</span></span>

<span data-ttu-id="3379f-107">Este método disminuye el recuento de objetos activos.</span><span class="sxs-lookup"><span data-stu-id="3379f-107">This method decrements the active-object count.</span></span> <span data-ttu-id="3379f-108">(Vea [**CBaseObject::ObjectsActive).**](cbaseobject-objectsactive.md)</span><span class="sxs-lookup"><span data-stu-id="3379f-108">(See [**CBaseObject::ObjectsActive**](cbaseobject-objectsactive.md).)</span></span>

## <a name="requirements"></a><span data-ttu-id="3379f-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3379f-109">Requirements</span></span>



| <span data-ttu-id="3379f-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="3379f-110">Requirement</span></span> | <span data-ttu-id="3379f-111">Value</span><span class="sxs-lookup"><span data-stu-id="3379f-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3379f-112">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3379f-112">Header</span></span><br/>  | <dl> <span data-ttu-id="3379f-113"><dt>Combase.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="3379f-113"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3379f-114">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3379f-114">Library</span></span><br/> | <dl> <span data-ttu-id="3379f-115"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3379f-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3379f-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3379f-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3379f-117">**CBaseObject (clase)**</span><span class="sxs-lookup"><span data-stu-id="3379f-117">**CBaseObject Class**</span></span>](cbaseobject.md)
</dt> </dl>

 

 




