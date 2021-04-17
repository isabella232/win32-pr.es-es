---
description: El método NotifyFilterState notifica al pin cuando cambia el estado del filtro.
ms.assetid: 0eb3b0e5-9c44-464e-b4ca-bcded731e813
title: Método CBaseStreamControl. NotifyFilterState (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.NotifyFilterState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ccb96361c8f4938bd95ffdc29229a035a239cc25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661096"
---
# <a name="cbasestreamcontrolnotifyfilterstate-method"></a><span data-ttu-id="65d3c-103">CBaseStreamControl. NotifyFilterState, método</span><span class="sxs-lookup"><span data-stu-id="65d3c-103">CBaseStreamControl.NotifyFilterState method</span></span>

<span data-ttu-id="65d3c-104">El `NotifyFilterState` método notifica al pin cuando cambia el estado del filtro.</span><span class="sxs-lookup"><span data-stu-id="65d3c-104">The `NotifyFilterState` method notifies the pin when the filter's state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="65d3c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65d3c-105">Syntax</span></span>


```C++
void NotifyFilterState(
   FILTER_STATE   new_state,
   REFERENCE_TIME tStart = 0
);
```



## <a name="parameters"></a><span data-ttu-id="65d3c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="65d3c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65d3c-107">*nuevo \_ Estado*</span><span class="sxs-lookup"><span data-stu-id="65d3c-107">*new\_state*</span></span> 
</dt> <dd>

<span data-ttu-id="65d3c-108">Especifica el nuevo estado, como miembro de la enumeración de [**\_ Estado del filtro**](/windows/win32/api/strmif/ne-strmif-filter_state) .</span><span class="sxs-lookup"><span data-stu-id="65d3c-108">Specifies the new state, as a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="65d3c-109">*tStart*</span><span class="sxs-lookup"><span data-stu-id="65d3c-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="65d3c-110">Especifica la hora de inicio.</span><span class="sxs-lookup"><span data-stu-id="65d3c-110">Specifies the start time.</span></span> <span data-ttu-id="65d3c-111">Si el nuevo estado del filtro es State \_ Running, pase el valor del método [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) .</span><span class="sxs-lookup"><span data-stu-id="65d3c-111">If the new filter state is State\_Running, pass in the value from the [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span> <span data-ttu-id="65d3c-112">De lo contrario, use el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="65d3c-112">Otherwise, use the default value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65d3c-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65d3c-113">Return value</span></span>

<span data-ttu-id="65d3c-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="65d3c-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="65d3c-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65d3c-115">Remarks</span></span>

<span data-ttu-id="65d3c-116">Este método hace que el método [**CBaseStreamControl:: CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) deje de esperar.</span><span class="sxs-lookup"><span data-stu-id="65d3c-116">This method causes the [**CBaseStreamControl::CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) method to stop waiting.</span></span> <span data-ttu-id="65d3c-117">Llame a este método cada vez que el filtro propietario cambie de estado.</span><span class="sxs-lookup"><span data-stu-id="65d3c-117">Call this method whenever the owning filter changes state.</span></span>

## <a name="examples"></a><span data-ttu-id="65d3c-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="65d3c-118">Examples</span></span>


```C++
STDMETHODIMP CMyFilter::Run(REFERENCE_TIME tStart)
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Running, tStart);
   return CBaseFilter::Run(tStart); // Call the filter base class.
}

STDMETHODIMP CMyFilter::Pause()
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Paused);
   return CBaseFilter::Pause();
}

STDMETHODIMP CMyFilter::Stop()
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Stopped);
   return CBaseFilter::Stop();
}
```



## <a name="requirements"></a><span data-ttu-id="65d3c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65d3c-119">Requirements</span></span>



| <span data-ttu-id="65d3c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="65d3c-120">Requirement</span></span> | <span data-ttu-id="65d3c-121">Value</span><span class="sxs-lookup"><span data-stu-id="65d3c-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65d3c-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65d3c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="65d3c-123"><dt>Strmctl. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="65d3c-123"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="65d3c-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="65d3c-124">Library</span></span><br/> | <dl> <span data-ttu-id="65d3c-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="65d3c-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65d3c-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="65d3c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65d3c-127">**Clase CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="65d3c-127">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




