---
description: 'El método SetSyncSource establece un reloj de referencia para el filtro. Este método implementa el método IMediaFilter:: SetSyncSource.'
ms.assetid: 298039fc-dd38-4063-8752-2669b134b8ef
title: Método CBaseFilter. SetSyncSource (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8eaab23f1afd7e7b502d6828bc3f10cbfec49410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661101"
---
# <a name="cbasefiltersetsyncsource-method"></a><span data-ttu-id="077c3-104">CBaseFilter. SetSyncSource, método</span><span class="sxs-lookup"><span data-stu-id="077c3-104">CBaseFilter.SetSyncSource method</span></span>

<span data-ttu-id="077c3-105">El método **SetSyncSource** establece un reloj de referencia para el filtro.</span><span class="sxs-lookup"><span data-stu-id="077c3-105">The **SetSyncSource** method sets a reference clock for the filter.</span></span> <span data-ttu-id="077c3-106">Este método implementa el método [**IMediaFilter:: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) .</span><span class="sxs-lookup"><span data-stu-id="077c3-106">This method implements the [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="077c3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="077c3-107">Syntax</span></span>


```C++
HRESULT SetSyncSource(
   IReferenceClock *pClock
);
```



## <a name="parameters"></a><span data-ttu-id="077c3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="077c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="077c3-109">*pClock*</span><span class="sxs-lookup"><span data-stu-id="077c3-109">*pClock*</span></span> 
</dt> <dd>

<span data-ttu-id="077c3-110">Puntero a la interfaz [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) del reloj o **null**.</span><span class="sxs-lookup"><span data-stu-id="077c3-110">Pointer to the clock's [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="077c3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="077c3-111">Return value</span></span>

<span data-ttu-id="077c3-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="077c3-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="077c3-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="077c3-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="077c3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="077c3-114">Requirements</span></span>



| <span data-ttu-id="077c3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="077c3-115">Requirement</span></span> | <span data-ttu-id="077c3-116">Value</span><span class="sxs-lookup"><span data-stu-id="077c3-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="077c3-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="077c3-117">Header</span></span><br/>  | <dl> <span data-ttu-id="077c3-118"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="077c3-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="077c3-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="077c3-119">Library</span></span><br/> | <dl> <span data-ttu-id="077c3-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="077c3-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="077c3-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="077c3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="077c3-122">**Clase CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="077c3-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




