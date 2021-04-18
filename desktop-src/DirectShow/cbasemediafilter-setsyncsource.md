---
description: 'El método SetSyncSource establece un reloj de referencia para el objeto. Este método implementa el método IMediaFilter:: SetSyncSource.'
ms.assetid: ae296741-e3da-4376-a88a-8470f0a414ed
title: Método CBaseMediaFilter. SetSyncSource (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 01597228ddbadec6c1b0db481719fb690584b7fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660202"
---
# <a name="cbasemediafiltersetsyncsource-method"></a><span data-ttu-id="282a9-104">CBaseMediaFilter. SetSyncSource, método</span><span class="sxs-lookup"><span data-stu-id="282a9-104">CBaseMediaFilter.SetSyncSource method</span></span>

<span data-ttu-id="282a9-105">El `SetSyncSource` método establece un reloj de referencia para el objeto.</span><span class="sxs-lookup"><span data-stu-id="282a9-105">The `SetSyncSource` method sets a reference clock for the object.</span></span> <span data-ttu-id="282a9-106">Este método implementa el método [**IMediaFilter:: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) .</span><span class="sxs-lookup"><span data-stu-id="282a9-106">This method implements the [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="282a9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="282a9-107">Syntax</span></span>


```C++
HRESULT SetSyncSource(
   IReferenceClock *pClock
);
```



## <a name="parameters"></a><span data-ttu-id="282a9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="282a9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="282a9-109">*pClock*</span><span class="sxs-lookup"><span data-stu-id="282a9-109">*pClock*</span></span> 
</dt> <dd>

<span data-ttu-id="282a9-110">Puntero a la interfaz [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) del reloj o **null**.</span><span class="sxs-lookup"><span data-stu-id="282a9-110">Pointer to the clock's [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="282a9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="282a9-111">Return value</span></span>

<span data-ttu-id="282a9-112">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="282a9-112">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="282a9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="282a9-113">Requirements</span></span>



| <span data-ttu-id="282a9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="282a9-114">Requirement</span></span> | <span data-ttu-id="282a9-115">Value</span><span class="sxs-lookup"><span data-stu-id="282a9-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="282a9-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="282a9-116">Header</span></span><br/>  | <dl> <span data-ttu-id="282a9-117"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="282a9-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="282a9-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="282a9-118">Library</span></span><br/> | <dl> <span data-ttu-id="282a9-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="282a9-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="282a9-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="282a9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="282a9-121">**Clase CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="282a9-121">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




