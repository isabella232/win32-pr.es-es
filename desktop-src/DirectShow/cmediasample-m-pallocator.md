---
description: Puntero al asignador que creó este ejemplo.
ms.assetid: b4faccec-9124-4ae6-8662-ac5eb017328a
title: 'Miembro CMediaSample:: m_pAllocator (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAllocator
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ac2943c08b881badd8e15ea0633952ccc973a534
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670463"
---
# <a name="cmediasamplem_pallocator-member"></a><span data-ttu-id="b504f-103">Miembro pAllocator CMediaSample:: m \_</span><span class="sxs-lookup"><span data-stu-id="b504f-103">CMediaSample::m\_pAllocator member</span></span>

<span data-ttu-id="b504f-104">Puntero al asignador que creó este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b504f-104">Pointer to the allocator that created this sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="b504f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b504f-105">Syntax</span></span>


```C++
CBaseAllocator *m_pAllocator;
```



## <a name="remarks"></a><span data-ttu-id="b504f-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b504f-106">Remarks</span></span>

<span data-ttu-id="b504f-107">Aunque el ejemplo mantiene un puntero al asignador, no contiene un recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="b504f-107">Although the sample keeps a pointer to the allocator, it does not hold a reference count.</span></span> <span data-ttu-id="b504f-108">En su lugar, el asignador incrementa su propio recuento de referencias en el método [**IMemAllocator:: getBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) y se publica en el método [**IMemAllocator:: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) .</span><span class="sxs-lookup"><span data-stu-id="b504f-108">Instead, the allocator increments its own reference count in the [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) method, and releases itself in the [**IMemAllocator::ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) method.</span></span> <span data-ttu-id="b504f-109">Esto garantiza que el asignador estará disponible siempre que otro objeto esté usando el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b504f-109">This guarantees that the allocator will be available as long as another object is using the sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="b504f-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b504f-110">Requirements</span></span>



| <span data-ttu-id="b504f-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="b504f-111">Requirement</span></span> | <span data-ttu-id="b504f-112">Value</span><span class="sxs-lookup"><span data-stu-id="b504f-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b504f-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b504f-113">Header</span></span><br/>  | <dl> <span data-ttu-id="b504f-114"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b504f-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b504f-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b504f-115">Library</span></span><br/> | <dl> <span data-ttu-id="b504f-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b504f-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b504f-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="b504f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b504f-118">**Clase CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="b504f-118">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




