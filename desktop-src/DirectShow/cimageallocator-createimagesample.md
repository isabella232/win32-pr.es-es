---
description: El método CreateImageSample crea un ejemplo multimedia.
ms.assetid: dae71692-5cbc-4bc7-a363-41766ef17c58
title: Método CImageAllocator. CreateImageSample (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CreateImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57463a7025ea816b6fe6bcaa8b964231458903de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660820"
---
# <a name="cimageallocatorcreateimagesample-method"></a><span data-ttu-id="3e0b5-103">CImageAllocator. CreateImageSample, método</span><span class="sxs-lookup"><span data-stu-id="3e0b5-103">CImageAllocator.CreateImageSample method</span></span>

<span data-ttu-id="3e0b5-104">El `CreateImageSample` método crea un ejemplo multimedia.</span><span class="sxs-lookup"><span data-stu-id="3e0b5-104">The `CreateImageSample` method creates a media sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e0b5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e0b5-105">Syntax</span></span>


```C++
virtual CImageSample* CreateImageSample(
   LPBYTE pData,
   LONG   Length
);
```



## <a name="parameters"></a><span data-ttu-id="3e0b5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3e0b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e0b5-107">*pData*</span><span class="sxs-lookup"><span data-stu-id="3e0b5-107">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="3e0b5-108">Puntero a un búfer de *longitud* de tamaño, asignado por el llamador.</span><span class="sxs-lookup"><span data-stu-id="3e0b5-108">Pointer to a buffer of size *Length*, allocated by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="3e0b5-109">*Duración*</span><span class="sxs-lookup"><span data-stu-id="3e0b5-109">*Length*</span></span> 
</dt> <dd>

<span data-ttu-id="3e0b5-110">Longitud del búfer.</span><span class="sxs-lookup"><span data-stu-id="3e0b5-110">Length of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e0b5-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3e0b5-111">Return value</span></span>

<span data-ttu-id="3e0b5-112">Devuelve un objeto [**CImageSample**](cimagesample.md) .</span><span class="sxs-lookup"><span data-stu-id="3e0b5-112">Returns a [**CImageSample**](cimagesample.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e0b5-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e0b5-113">Remarks</span></span>

<span data-ttu-id="3e0b5-114">Este método crea un nuevo ejemplo multimedia, implementado como un objeto **CImageSample** .</span><span class="sxs-lookup"><span data-stu-id="3e0b5-114">This method creates a new media sample, implemented as a **CImageSample** object.</span></span> <span data-ttu-id="3e0b5-115">El método [**IMediaSample:: GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) del ejemplo devuelve un puntero al búfer especificado en el parámetro *pdata* .</span><span class="sxs-lookup"><span data-stu-id="3e0b5-115">The sample's [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) method returns a pointer to the buffer specified in the *pData* parameter.</span></span>

<span data-ttu-id="3e0b5-116">Si deriva una nueva clase de asignador de [**CImageAllocator**](cimageallocator.md) y una nueva clase de ejemplo multimedia de [**CImageSample**](cimagesample.md), debe invalidar este método para crear una instancia de la clase de ejemplo multimedia.</span><span class="sxs-lookup"><span data-stu-id="3e0b5-116">If you derive a new allocator class from [**CImageAllocator**](cimageallocator.md) and a new media sample class from [**CImageSample**](cimagesample.md), you should override this method to create an instance of your media sample class.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e0b5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e0b5-117">Requirements</span></span>



| <span data-ttu-id="3e0b5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e0b5-118">Requirement</span></span> | <span data-ttu-id="3e0b5-119">Value</span><span class="sxs-lookup"><span data-stu-id="3e0b5-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e0b5-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e0b5-120">Header</span></span><br/>  | <dl> <span data-ttu-id="3e0b5-121"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e0b5-121"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3e0b5-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3e0b5-122">Library</span></span><br/> | <dl> <span data-ttu-id="3e0b5-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3e0b5-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e0b5-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e0b5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e0b5-125">**Clase CImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="3e0b5-125">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> <dt>

[<span data-ttu-id="3e0b5-126">**CImageAllocator:: Alloc**</span><span class="sxs-lookup"><span data-stu-id="3e0b5-126">**CImageAllocator::Alloc**</span></span>](cimageallocator-alloc.md)
</dt> </dl>

 

 




