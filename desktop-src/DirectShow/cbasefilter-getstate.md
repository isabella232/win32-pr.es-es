---
description: 'El método GetState recupera el estado de los filtros (en ejecución, detenido o en pausa). Este método implementa el método IMediaFilter:: GetState.'
ms.assetid: e32e3a1d-857f-4db3-b52c-5b6b802ded42
title: Método CBaseFilter. GetState (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c9470e5d71bf71f4e37e6eef84015becdf05f65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661082"
---
# <a name="cbasefiltergetstate-method"></a><span data-ttu-id="a23fe-104">CBaseFilter. GetState, método</span><span class="sxs-lookup"><span data-stu-id="a23fe-104">CBaseFilter.GetState method</span></span>

<span data-ttu-id="a23fe-105">El `GetState` método recupera el estado del filtro (en ejecución, detenido o en pausa).</span><span class="sxs-lookup"><span data-stu-id="a23fe-105">The `GetState` method retrieves the filters's state (running, stopped, or paused).</span></span> <span data-ttu-id="a23fe-106">Este método implementa el método [**IMediaFilter:: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) .</span><span class="sxs-lookup"><span data-stu-id="a23fe-106">This method implements the [**IMediaFilter::GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a23fe-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a23fe-107">Syntax</span></span>


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a><span data-ttu-id="a23fe-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a23fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a23fe-109">*dwMilliSecsTimeout*</span><span class="sxs-lookup"><span data-stu-id="a23fe-109">*dwMilliSecsTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="a23fe-110">Intervalo de tiempo de espera, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="a23fe-110">Time-out interval, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="a23fe-111">*State*</span><span class="sxs-lookup"><span data-stu-id="a23fe-111">*State*</span></span> 
</dt> <dd>

<span data-ttu-id="a23fe-112">Puntero a una variable que recibe un miembro del tipo enumerado de [**\_ Estado de filtro**](/windows/win32/api/strmif/ne-strmif-filter_state) , que indica el estado del filtro.</span><span class="sxs-lookup"><span data-stu-id="a23fe-112">Pointer to a variable that receives a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type, indicating the filter's state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a23fe-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a23fe-113">Return value</span></span>

<span data-ttu-id="a23fe-114">Devuelve el \_ puntero S o E \_ .</span><span class="sxs-lookup"><span data-stu-id="a23fe-114">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="a23fe-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a23fe-115">Remarks</span></span>

<span data-ttu-id="a23fe-116">En la clase base, todas las transiciones de estado son sincrónicas y se omite el parámetro *dwMilliSecsTimeout* .</span><span class="sxs-lookup"><span data-stu-id="a23fe-116">In the base class, all state transitions are synchronous and the *dwMilliSecsTimeout* parameter is ignored.</span></span> <span data-ttu-id="a23fe-117">Si una clase derivada realiza transiciones de estado asincrónicas, debe invalidar este método para esperar durante las transiciones de estado, con un tiempo de espera de *dwMilliSecsTimeout* milisegundos.</span><span class="sxs-lookup"><span data-stu-id="a23fe-117">If a derived class performs asynchronous state transitions, it should override this method to wait during state transitions, with a time-out of *dwMilliSecsTimeout* milliseconds.</span></span>

<span data-ttu-id="a23fe-118">Si el filtro no entrega datos mientras están en pausa, invalide el `GetState` método para que devuelva el valor VFW S no se cumple la \_ \_ \_ indicación cuando el filtro esté en pausa (consulte [entrega de muestras](delivering-samples.md)).</span><span class="sxs-lookup"><span data-stu-id="a23fe-118">If your filter does not deliver data while paused, override the `GetState` method to return the value VFW\_S\_CANT\_CUE when the filter is paused (see [Delivering Samples](delivering-samples.md)).</span></span> <span data-ttu-id="a23fe-119">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="a23fe-119">For example:</span></span>


```C++
CMyFilter::GetState(DWORD dw, FILTER_STATE *pState)
{
    CheckPointer(pState, E_POINTER);
    *pState = m_State;
    if (m_State == State_Paused)
        return VFW_S_CANT_CUE;
    else
        return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="a23fe-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a23fe-120">Requirements</span></span>



| <span data-ttu-id="a23fe-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a23fe-121">Requirement</span></span> | <span data-ttu-id="a23fe-122">Value</span><span class="sxs-lookup"><span data-stu-id="a23fe-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a23fe-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a23fe-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a23fe-124"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a23fe-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a23fe-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a23fe-125">Library</span></span><br/> | <dl> <span data-ttu-id="a23fe-126"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a23fe-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a23fe-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="a23fe-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a23fe-128">**Clase CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="a23fe-128">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




