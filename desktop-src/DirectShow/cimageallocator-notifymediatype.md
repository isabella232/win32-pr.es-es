---
description: El método NotifyMediaType informa al objeto del tipo de medio actual.
ms.assetid: 6fb708ff-e968-4867-baca-ebe2515c9fab
title: Método CImageAllocator. NotifyMediaType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.NotifyMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb9261884b8940b571876502741fcc52e1c40a33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661043"
---
# <a name="cimageallocatornotifymediatype-method"></a><span data-ttu-id="e67a8-103">CImageAllocator. NotifyMediaType, método</span><span class="sxs-lookup"><span data-stu-id="e67a8-103">CImageAllocator.NotifyMediaType method</span></span>

<span data-ttu-id="e67a8-104">El `NotifyMediaType` método informa al objeto del tipo de medio actual.</span><span class="sxs-lookup"><span data-stu-id="e67a8-104">The `NotifyMediaType` method informs the object of the current media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="e67a8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e67a8-105">Syntax</span></span>


```C++
void NotifyMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="e67a8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e67a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e67a8-107">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="e67a8-107">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="e67a8-108">Puntero a un objeto [**CMediaType**](cmediatype.md) o **null** para borrar el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="e67a8-108">Pointer to a [**CMediaType**](cmediatype.md) object, or **NULL** to clear the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e67a8-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e67a8-109">Return value</span></span>

<span data-ttu-id="e67a8-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e67a8-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e67a8-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e67a8-111">Remarks</span></span>

<span data-ttu-id="e67a8-112">El filtro propietario debe llamar a este método cada vez que cambie el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="e67a8-112">The owning filter should call this method whenever the media type changes.</span></span> <span data-ttu-id="e67a8-113">Normalmente esto se produce cuando el PIN se conecta por primera vez y después de un cambio de formato dinámico.</span><span class="sxs-lookup"><span data-stu-id="e67a8-113">Typically this occurs when the pin first connects, and after a dynamic format change.</span></span> <span data-ttu-id="e67a8-114">El asignador usa el tipo de medio para validar las propiedades de asignador propuesto y también cuando crea ejemplos de medios.</span><span class="sxs-lookup"><span data-stu-id="e67a8-114">The allocator uses the media type to validate proposed allocator properties, and also when it creates media samples.</span></span>

<span data-ttu-id="e67a8-115">El objeto **CImageAllocator** almacena el puntero *pMediaType* en la variable miembro **m \_ pMediaType** .</span><span class="sxs-lookup"><span data-stu-id="e67a8-115">The **CImageAllocator** object stores the *pMediaType* pointer in the **m\_pMediaType** member variable.</span></span> <span data-ttu-id="e67a8-116">Por consiguiente, si el autor de la llamada necesita liberar el objeto **CMediaType** , debe actualizar el asignador llamando de nuevo a este método, ya sea con un puntero nuevo o con un valor **null** .</span><span class="sxs-lookup"><span data-stu-id="e67a8-116">Therefore, if the caller needs to release the **CMediaType** object, it should update the allocator by calling this method again, either with a new pointer or with a **NULL** value.</span></span> <span data-ttu-id="e67a8-117">De lo contrario, se puede producir un error cuando el asignador intenta hacer referencia al puntero anterior.</span><span class="sxs-lookup"><span data-stu-id="e67a8-117">Otherwise, an error can occur when the allocator attempts to reference the old pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="e67a8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e67a8-118">Requirements</span></span>



| <span data-ttu-id="e67a8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e67a8-119">Requirement</span></span> | <span data-ttu-id="e67a8-120">Value</span><span class="sxs-lookup"><span data-stu-id="e67a8-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e67a8-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e67a8-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e67a8-122"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e67a8-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e67a8-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e67a8-123">Library</span></span><br/> | <dl> <span data-ttu-id="e67a8-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e67a8-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e67a8-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e67a8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e67a8-126">**Clase CImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="e67a8-126">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




