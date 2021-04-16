---
description: Se llama al método ChangeRate cuando cambia la velocidad de reproducción.
ms.assetid: c4f1f9d0-6c09-4cab-8a37-dd1ff3f5619f
title: Método CSourceSeeking. ChangeRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02fab05d65929233b97f7d53e497bae6593c472a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690148"
---
# <a name="csourceseekingchangerate-method"></a><span data-ttu-id="c9723-103">CSourceSeeking. ChangeRate, método</span><span class="sxs-lookup"><span data-stu-id="c9723-103">CSourceSeeking.ChangeRate method</span></span>

<span data-ttu-id="c9723-104">`ChangeRate`Se llama al método cuando cambia la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="c9723-104">The `ChangeRate` method is called when the playback rate changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9723-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9723-105">Syntax</span></span>


```C++
virtual HRESULT ChangeRate() = 0;
```



## <a name="parameters"></a><span data-ttu-id="c9723-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9723-106">Parameters</span></span>

<span data-ttu-id="c9723-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c9723-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c9723-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9723-108">Return value</span></span>

<span data-ttu-id="c9723-109">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c9723-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9723-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c9723-110">Remarks</span></span>

<span data-ttu-id="c9723-111">El método [**CSourceSeeking:: SetRate**](csourceseeking-setrate.md) llama a este método, que la clase derivada debe implementar.</span><span class="sxs-lookup"><span data-stu-id="c9723-111">The [**CSourceSeeking::SetRate**](csourceseeking-setrate.md) method calls this method, which the derived class must implement.</span></span> <span data-ttu-id="c9723-112">El método **SetRate** actualiza la variable miembro [**CSourceSeeking:: m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) , pero no valida el nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="c9723-112">The **SetRate** method updates the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable, but does not validate the new value.</span></span> <span data-ttu-id="c9723-113">Siempre se debe rechazar una tasa de cero.</span><span class="sxs-lookup"><span data-stu-id="c9723-113">A rate of zero should always be rejected.</span></span> <span data-ttu-id="c9723-114">Las velocidades menores que cero indican una reproducción negativa.</span><span class="sxs-lookup"><span data-stu-id="c9723-114">Rates less than zero indicate negative playback.</span></span> <span data-ttu-id="c9723-115">La mayoría de los filtros no admiten las tasas negativas.</span><span class="sxs-lookup"><span data-stu-id="c9723-115">Most filters do not support negative rates.</span></span>

<span data-ttu-id="c9723-116">En el ejemplo siguiente se muestra una posible implementación:</span><span class="sxs-lookup"><span data-stu-id="c9723-116">The following example shows a possible implementation:</span></span>


```C++
HRESULT CMyStream::ChangeRate( )
{
    {   // Scope for critical section lock.
        CAutoLock cAutoLockSeeking(CSourceSeeking::m_pLock);
        if( m_dRateSeeking <= 0 ) {
            m_dRateSeeking = 1.0;  // Reset to a reasonable value.
            return E_FAIL;
        }
    }
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="c9723-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9723-117">Requirements</span></span>



| <span data-ttu-id="c9723-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9723-118">Requirement</span></span> | <span data-ttu-id="c9723-119">Value</span><span class="sxs-lookup"><span data-stu-id="c9723-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9723-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9723-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c9723-121"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9723-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c9723-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c9723-122">Library</span></span><br/> | <dl> <span data-ttu-id="c9723-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c9723-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9723-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9723-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9723-125">**Clase CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="c9723-125">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




