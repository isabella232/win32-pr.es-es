---
description: 'El método SetSink establece un administrador de calidad externo. Este método implementa el método IQualityControl:: SetSink.'
ms.assetid: 714e6839-954e-4231-824d-72a45f270f59
title: Método CBasePin. SetSink (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetSink
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4237e342f8f49059cab017b17a1f116ca6e2da67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660482"
---
# <a name="cbasepinsetsink-method"></a><span data-ttu-id="7743f-104">CBasePin. SetSink, método</span><span class="sxs-lookup"><span data-stu-id="7743f-104">CBasePin.SetSink method</span></span>

<span data-ttu-id="7743f-105">El `SetSink` método establece un administrador de calidad externo.</span><span class="sxs-lookup"><span data-stu-id="7743f-105">The `SetSink` method sets an external quality manager.</span></span> <span data-ttu-id="7743f-106">Este método implementa el método [**IQualityControl:: SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) .</span><span class="sxs-lookup"><span data-stu-id="7743f-106">This method implements the [**IQualityControl::SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7743f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7743f-107">Syntax</span></span>


```C++
HRESULT SetSink(
   IQualityControl *piqc
);
```



## <a name="parameters"></a><span data-ttu-id="7743f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7743f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7743f-109">*piqc*</span><span class="sxs-lookup"><span data-stu-id="7743f-109">*piqc*</span></span> 
</dt> <dd>

<span data-ttu-id="7743f-110">Puntero a la interfaz [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) del administrador de calidad.</span><span class="sxs-lookup"><span data-stu-id="7743f-110">Pointer to the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) interface of the quality manager.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7743f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7743f-111">Return value</span></span>

<span data-ttu-id="7743f-112">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="7743f-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="7743f-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7743f-113">Remarks</span></span>

<span data-ttu-id="7743f-114">Llame a este método para redirigir los mensajes de control de calidad a un administrador de calidad externo.</span><span class="sxs-lookup"><span data-stu-id="7743f-114">Call this method to redirect quality-control messages to an external quality manager.</span></span> <span data-ttu-id="7743f-115">Para obtener más información, vea [Administración de control de calidad](quality-control-management.md).</span><span class="sxs-lookup"><span data-stu-id="7743f-115">For more information, see [Quality-Control Management](quality-control-management.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7743f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7743f-116">Requirements</span></span>



| <span data-ttu-id="7743f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7743f-117">Requirement</span></span> | <span data-ttu-id="7743f-118">Value</span><span class="sxs-lookup"><span data-stu-id="7743f-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7743f-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7743f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="7743f-120"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7743f-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7743f-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7743f-121">Library</span></span><br/> | <dl> <span data-ttu-id="7743f-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="7743f-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7743f-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="7743f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7743f-124">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="7743f-124">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




