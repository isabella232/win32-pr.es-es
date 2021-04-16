---
description: El método SetSyncSource notifica a la clase base del reloj de referencia actual.
ms.assetid: 056385ac-682c-456e-9a5f-86490bd6e05f
title: Método CBaseStreamControl. SetSyncSource (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60832d1bf7ceca59089875f10579d52cf2cfec4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678892"
---
# <a name="cbasestreamcontrolsetsyncsource-method"></a><span data-ttu-id="13237-103">CBaseStreamControl. SetSyncSource, método</span><span class="sxs-lookup"><span data-stu-id="13237-103">CBaseStreamControl.SetSyncSource method</span></span>

<span data-ttu-id="13237-104">El `SetSyncSource` método notifica a la clase base del reloj de referencia actual.</span><span class="sxs-lookup"><span data-stu-id="13237-104">The `SetSyncSource` method notifies the base class of the current reference clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="13237-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13237-105">Syntax</span></span>


```C++
void SetSyncSource(
   IReferenceClock *pRefClock
);
```



## <a name="parameters"></a><span data-ttu-id="13237-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13237-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13237-107">*pRefClock*</span><span class="sxs-lookup"><span data-stu-id="13237-107">*pRefClock*</span></span> 
</dt> <dd>

<span data-ttu-id="13237-108">Puntero a la interfaz [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) del reloj de referencia.</span><span class="sxs-lookup"><span data-stu-id="13237-108">Pointer to the [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface of the reference clock.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13237-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13237-109">Return value</span></span>

<span data-ttu-id="13237-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="13237-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="13237-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13237-111">Remarks</span></span>

<span data-ttu-id="13237-112">Llame a este método desde dentro del método [**IMediaFilter:: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) del filtro.</span><span class="sxs-lookup"><span data-stu-id="13237-112">Call this method from inside the filter's [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method.</span></span> <span data-ttu-id="13237-113">La clase **CBaseStreamControl** usa la interfaz **IReferenceClock** para asegurarse de que no descarta los ejemplos demasiado rápidamente.</span><span class="sxs-lookup"><span data-stu-id="13237-113">The **CBaseStreamControl** class uses the **IReferenceClock** interface to ensure that it does not discard samples too quickly.</span></span>

## <a name="examples"></a><span data-ttu-id="13237-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="13237-114">Examples</span></span>


```C++
STDMETHODIMP CMyFilter::SetSyncSource(IReferenceClock *pClock)
{
    // Note: It's OK if pClock is NULL.

    m_pMyPin->SetSyncSource(pClock);
    return CBaseFilter::SetSyncSource(pClock);
}
```



## <a name="requirements"></a><span data-ttu-id="13237-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13237-115">Requirements</span></span>



| <span data-ttu-id="13237-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="13237-116">Requirement</span></span> | <span data-ttu-id="13237-117">Value</span><span class="sxs-lookup"><span data-stu-id="13237-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13237-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="13237-118">Header</span></span><br/>  | <dl> <span data-ttu-id="13237-119"><dt>Strmctl. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="13237-119"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="13237-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="13237-120">Library</span></span><br/> | <dl> <span data-ttu-id="13237-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="13237-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13237-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="13237-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13237-123">**Clase CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="13237-123">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




