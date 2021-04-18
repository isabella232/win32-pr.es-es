---
description: 'El método Run ejecuta el objeto. Este método implementa el método IMediaFilter:: Run.'
ms.assetid: a59180df-46b4-4c23-973f-2931d95ace55
title: Método CBaseMediaFilter. Run (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c4023be7731f9bae60576bc7002010eb0b51823
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660203"
---
# <a name="cbasemediafilterrun-method"></a><span data-ttu-id="4325e-104">CBaseMediaFilter. Run (método)</span><span class="sxs-lookup"><span data-stu-id="4325e-104">CBaseMediaFilter.Run method</span></span>

<span data-ttu-id="4325e-105">El `Run` método ejecuta el objeto.</span><span class="sxs-lookup"><span data-stu-id="4325e-105">The `Run` method runs the object.</span></span> <span data-ttu-id="4325e-106">Este método implementa el método [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) .</span><span class="sxs-lookup"><span data-stu-id="4325e-106">This method implements the [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4325e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4325e-107">Syntax</span></span>


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a><span data-ttu-id="4325e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4325e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4325e-109">*tStart*</span><span class="sxs-lookup"><span data-stu-id="4325e-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="4325e-110">Hora de referencia correspondiente al tiempo de secuencia 0.</span><span class="sxs-lookup"><span data-stu-id="4325e-110">Reference time corresponding to stream time 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4325e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4325e-111">Return value</span></span>

<span data-ttu-id="4325e-112">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="4325e-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4325e-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4325e-113">Remarks</span></span>

<span data-ttu-id="4325e-114">Si se detiene el objeto, este método pausa el objeto llamando al método [**CBaseMediaFilter::P ause**](cbasemediafilter-pause.md) .</span><span class="sxs-lookup"><span data-stu-id="4325e-114">If the object is stopped, this method pauses the object by calling the [**CBaseMediaFilter::Pause**](cbasemediafilter-pause.md) method.</span></span> <span data-ttu-id="4325e-115">A continuación, establece la variable miembro de [**\_ Estado CBaseMediaFilter:: m**](cbasemediafilter-m-state.md) en el estado en \_ ejecución.</span><span class="sxs-lookup"><span data-stu-id="4325e-115">It then sets the [**CBaseMediaFilter::m\_State**](cbasemediafilter-m-state.md) member variable to State\_Running.</span></span>

<span data-ttu-id="4325e-116">El tiempo de secuencia se calcula como el tiempo de referencia actual menos *tStart*.</span><span class="sxs-lookup"><span data-stu-id="4325e-116">Stream time is calculated as the current reference time minus *tStart*.</span></span> <span data-ttu-id="4325e-117">Un ejemplo multimedia con una marca de tiempo de cero se debe representar a la hora *tStart*.</span><span class="sxs-lookup"><span data-stu-id="4325e-117">A media sample with a time stamp of zero should be rendered at time *tStart*.</span></span>

## <a name="requirements"></a><span data-ttu-id="4325e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4325e-118">Requirements</span></span>



| <span data-ttu-id="4325e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4325e-119">Requirement</span></span> | <span data-ttu-id="4325e-120">Value</span><span class="sxs-lookup"><span data-stu-id="4325e-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4325e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4325e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="4325e-122"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4325e-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4325e-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4325e-123">Library</span></span><br/> | <dl> <span data-ttu-id="4325e-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="4325e-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4325e-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="4325e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4325e-126">**Clase CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="4325e-126">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




