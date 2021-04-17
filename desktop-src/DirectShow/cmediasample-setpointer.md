---
description: El método SetPointer establece el puntero en el búfer de memoria.
ms.assetid: 60627600-c982-462e-b540-327a58e57615
title: Método CMediaSample. SetPointer (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetPointer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67d9fc5d260cc627919a458593328c36f0de9a94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679075"
---
# <a name="cmediasamplesetpointer-method"></a><span data-ttu-id="c9a90-103">CMediaSample. SetPointer, método</span><span class="sxs-lookup"><span data-stu-id="c9a90-103">CMediaSample.SetPointer method</span></span>

<span data-ttu-id="c9a90-104">El `SetPointer` método establece el puntero en el búfer de memoria.</span><span class="sxs-lookup"><span data-stu-id="c9a90-104">The `SetPointer` method sets the pointer to the memory buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9a90-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9a90-105">Syntax</span></span>


```C++
HRESULT SetPointer(
   BYTE *ptr,
   LONG cBytes
);
```



## <a name="parameters"></a><span data-ttu-id="c9a90-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9a90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9a90-107">*ptr*</span><span class="sxs-lookup"><span data-stu-id="c9a90-107">*ptr*</span></span> 
</dt> <dd>

<span data-ttu-id="c9a90-108">Puntero a un búfer de memoria asignado por el autor de la llamada, de tamaño *cBytes*.</span><span class="sxs-lookup"><span data-stu-id="c9a90-108">Pointer to a memory buffer allocated by the caller, of size *cBytes*.</span></span>

</dd> <dt>

<span data-ttu-id="c9a90-109">*cBytes*</span><span class="sxs-lookup"><span data-stu-id="c9a90-109">*cBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="c9a90-110">Longitud del búfer, en bytes.</span><span class="sxs-lookup"><span data-stu-id="c9a90-110">Length of the buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9a90-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9a90-111">Return value</span></span>

<span data-ttu-id="c9a90-112">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="c9a90-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9a90-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c9a90-113">Remarks</span></span>

<span data-ttu-id="c9a90-114">Este método permite al asignador establecer un nuevo puntero para el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c9a90-114">This method enables the allocator to set a new pointer for the sample.</span></span>

<span data-ttu-id="c9a90-115">Este método no está disponible a través de la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) .</span><span class="sxs-lookup"><span data-stu-id="c9a90-115">This method is not available through the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span> <span data-ttu-id="c9a90-116">El objeto que crea el ejemplo puede tener acceso a este método (a través de **CMediaSample**), pero otros objetos no pueden.</span><span class="sxs-lookup"><span data-stu-id="c9a90-116">The object that creates the sample can access this method (through **CMediaSample**), but other objects cannot.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9a90-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9a90-117">Requirements</span></span>



| <span data-ttu-id="c9a90-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9a90-118">Requirement</span></span> | <span data-ttu-id="c9a90-119">Value</span><span class="sxs-lookup"><span data-stu-id="c9a90-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9a90-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9a90-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c9a90-121"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9a90-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c9a90-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c9a90-122">Library</span></span><br/> | <dl> <span data-ttu-id="c9a90-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c9a90-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9a90-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9a90-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9a90-125">**Clase CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="c9a90-125">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




