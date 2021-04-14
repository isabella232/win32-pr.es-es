---
description: El método UsingImageAllocator indica si el asignador actual es un objeto CImageAllocator.
ms.assetid: 842bbcbc-2cc8-4e9d-b6c0-e07f7e472ca1
title: Método CDrawImage. UsingImageAllocator (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.UsingImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a61b4ece94c9c52a0f769a29ec32a26c08b33ee0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661394"
---
# <a name="cdrawimageusingimageallocator-method"></a><span data-ttu-id="7846b-103">CDrawImage. UsingImageAllocator, método</span><span class="sxs-lookup"><span data-stu-id="7846b-103">CDrawImage.UsingImageAllocator method</span></span>

<span data-ttu-id="7846b-104">El `UsingImageAllocator` método indica si el asignador actual es un objeto [**CImageAllocator**](cimageallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="7846b-104">The `UsingImageAllocator` method indicates whether the current allocator is a [**CImageAllocator**](cimageallocator.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7846b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7846b-105">Syntax</span></span>


```C++
BOOL UsingImageAllocator();
```



## <a name="parameters"></a><span data-ttu-id="7846b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7846b-106">Parameters</span></span>

<span data-ttu-id="7846b-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7846b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7846b-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7846b-108">Return value</span></span>

<span data-ttu-id="7846b-109">Devuelve **true** si el asignador actual es un objeto **CImageAllocator** o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7846b-109">Returns **TRUE** if the current allocator is a **CImageAllocator** object, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7846b-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7846b-110">Requirements</span></span>



| <span data-ttu-id="7846b-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="7846b-111">Requirement</span></span> | <span data-ttu-id="7846b-112">Value</span><span class="sxs-lookup"><span data-stu-id="7846b-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7846b-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7846b-113">Header</span></span><br/>  | <dl> <span data-ttu-id="7846b-114"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7846b-114"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7846b-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7846b-115">Library</span></span><br/> | <dl> <span data-ttu-id="7846b-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="7846b-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7846b-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="7846b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7846b-118">**Clase CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="7846b-118">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="7846b-119">**CDrawImage::NotifyAllocator**</span><span class="sxs-lookup"><span data-stu-id="7846b-119">**CDrawImage::NotifyAllocator**</span></span>](cdrawimage-notifyallocator.md)
</dt> </dl>

 

 




