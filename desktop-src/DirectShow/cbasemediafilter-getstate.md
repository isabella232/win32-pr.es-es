---
description: 'El método GetState recupera el estado del objeto (en ejecución, detenido o en pausa). Este método implementa el método IMediaFilter:: GetState.'
ms.assetid: d4cc7e2b-5ea5-4165-842f-becc3a81cbce
title: Método CBaseMediaFilter. GetState (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eeda91433e0e1474e936902da115e15c37e32e09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670539"
---
# <a name="cbasemediafiltergetstate-method"></a><span data-ttu-id="d8c14-104">CBaseMediaFilter. GetState, método</span><span class="sxs-lookup"><span data-stu-id="d8c14-104">CBaseMediaFilter.GetState method</span></span>

<span data-ttu-id="d8c14-105">El `GetState` método recupera el estado del objeto (en ejecución, detenido o en pausa).</span><span class="sxs-lookup"><span data-stu-id="d8c14-105">The `GetState` method retrieves the object's state (running, stopped, or paused).</span></span> <span data-ttu-id="d8c14-106">Este método implementa el método [**IMediaFilter:: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) .</span><span class="sxs-lookup"><span data-stu-id="d8c14-106">This method implements the [**IMediaFilter::GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8c14-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d8c14-107">Syntax</span></span>


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a><span data-ttu-id="d8c14-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d8c14-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8c14-109">*dwMilliSecsTimeout*</span><span class="sxs-lookup"><span data-stu-id="d8c14-109">*dwMilliSecsTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="d8c14-110">Intervalo de tiempo de espera, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="d8c14-110">Time-out interval, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="d8c14-111">*State*</span><span class="sxs-lookup"><span data-stu-id="d8c14-111">*State*</span></span> 
</dt> <dd>

<span data-ttu-id="d8c14-112">Puntero a una variable que recibe un miembro del tipo enumerado de [**\_ Estado de filtro**](/windows/win32/api/strmif/ne-strmif-filter_state) , que indica el estado del objeto.</span><span class="sxs-lookup"><span data-stu-id="d8c14-112">Pointer to a variable that receives a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type, indicating the object's state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8c14-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8c14-113">Return value</span></span>

<span data-ttu-id="d8c14-114">Devuelve el \_ puntero S o E \_ .</span><span class="sxs-lookup"><span data-stu-id="d8c14-114">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8c14-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d8c14-115">Remarks</span></span>

<span data-ttu-id="d8c14-116">En la clase base, todas las transiciones de estado son sincrónicas y se omite el parámetro *dwMilliSecsTimeout* .</span><span class="sxs-lookup"><span data-stu-id="d8c14-116">In the base class, all state transitions are synchronous and the *dwMilliSecsTimeout* parameter is ignored.</span></span> <span data-ttu-id="d8c14-117">Si una clase derivada realiza transiciones de estado asincrónicas, debe invalidar este método para esperar durante las transiciones de estado, con un tiempo de espera de *dwMilliSecsTimeout* milisegundos.</span><span class="sxs-lookup"><span data-stu-id="d8c14-117">If a derived class performs asynchronous state transitions, it should override this method to wait during state transitions, with a time-out of *dwMilliSecsTimeout* milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8c14-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8c14-118">Requirements</span></span>



| <span data-ttu-id="d8c14-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8c14-119">Requirement</span></span> | <span data-ttu-id="d8c14-120">Value</span><span class="sxs-lookup"><span data-stu-id="d8c14-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8c14-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d8c14-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d8c14-122"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8c14-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d8c14-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d8c14-123">Library</span></span><br/> | <dl> <span data-ttu-id="d8c14-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d8c14-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8c14-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8c14-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8c14-126">**Clase CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="d8c14-126">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




