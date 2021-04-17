---
description: El método NotifyAllocator informa al objeto CDrawImage de si el asignador de la conexión es un objeto CImageAllocator.
ms.assetid: cc1604e7-f755-4a7a-9294-6fd06bb434d4
title: Método CDrawImage. NotifyAllocator (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7bab7d1d00b70317a7cbb0b79f8a430a603a757
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680947"
---
# <a name="cdrawimagenotifyallocator-method"></a><span data-ttu-id="7b8b0-103">CDrawImage. NotifyAllocator, método</span><span class="sxs-lookup"><span data-stu-id="7b8b0-103">CDrawImage.NotifyAllocator method</span></span>

<span data-ttu-id="7b8b0-104">El `NotifyAllocator` método informa al objeto **CDrawImage** de si el asignador de la conexión es un objeto [**CImageAllocator**](cimageallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="7b8b0-104">The `NotifyAllocator` method informs the **CDrawImage** object whether the allocator for the connection is a [**CImageAllocator**](cimageallocator.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b8b0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b8b0-105">Syntax</span></span>


```C++
void NotifyAllocator(
   BOOL bUsingImageAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="7b8b0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7b8b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b8b0-107">*bUsingImageAllocator*</span><span class="sxs-lookup"><span data-stu-id="7b8b0-107">*bUsingImageAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="7b8b0-108">Valor booleano que indica el tipo de asignador que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-108">Boolean value that indicates what kind of allocator is being used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b8b0-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7b8b0-109">Return value</span></span>

<span data-ttu-id="7b8b0-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b8b0-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7b8b0-111">Remarks</span></span>

<span data-ttu-id="7b8b0-112">El filtro propietario debe llamar a este método después de que los pin acepten un asignador.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-112">The owning filter should call this method after the pins agree to an allocator.</span></span> <span data-ttu-id="7b8b0-113">Si el filtro sabe que el asignador es un objeto **CImageAllocator** , debe llamar a este método con el valor **true**.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-113">If the filter knows the allocator is a **CImageAllocator** object, it should call this method with the value **TRUE**.</span></span> <span data-ttu-id="7b8b0-114">(Normalmente, el filtro solo lo sabrá si posee el asignador en cuestión). De lo contrario, debería llamar a este método con el valor **false**.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-114">(Typically, the filter will know this only if it owns the allocator in question.) Otherwise, it should call this method with the value **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b8b0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b8b0-115">Requirements</span></span>



| <span data-ttu-id="7b8b0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b8b0-116">Requirement</span></span> | <span data-ttu-id="7b8b0-117">Value</span><span class="sxs-lookup"><span data-stu-id="7b8b0-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b8b0-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7b8b0-118">Header</span></span><br/>  | <dl> <span data-ttu-id="7b8b0-119"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7b8b0-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7b8b0-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7b8b0-120">Library</span></span><br/> | <dl> <span data-ttu-id="7b8b0-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="7b8b0-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b8b0-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b8b0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b8b0-123">**Clase CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="7b8b0-123">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="7b8b0-124">**CDrawImage::D rawImage**</span><span class="sxs-lookup"><span data-stu-id="7b8b0-124">**CDrawImage::DrawImage**</span></span>](cdrawimage-drawimage.md)
</dt> </dl>

 

 




