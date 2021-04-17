---
description: 'El método SetPositions establece la posición actual y la posición de detención. Este método implementa el método IMediaSeeking:: SetPositions.'
ms.assetid: d4425221-e20f-4e51-8a33-a74fa21f9117
title: Método CPosPassThru. SetPositions (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 409b4a63f02e6751f987a53dad2836adecd27607
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661292"
---
# <a name="cpospassthrusetpositions-method"></a><span data-ttu-id="18522-104">CPosPassThru. SetPositions, método</span><span class="sxs-lookup"><span data-stu-id="18522-104">CPosPassThru.SetPositions method</span></span>

<span data-ttu-id="18522-105">El `SetPositions` método establece la posición actual y la posición de detención.</span><span class="sxs-lookup"><span data-stu-id="18522-105">The `SetPositions` method sets the current position and the stop position.</span></span> <span data-ttu-id="18522-106">Este método implementa el método [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="18522-106">This method implements the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="18522-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18522-107">Syntax</span></span>


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    dwCurrentFlags,
   LONGLONG *pStop,
   DWORD    dwStopFlags
);
```



## <a name="parameters"></a><span data-ttu-id="18522-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="18522-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18522-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="18522-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="18522-110">Puntero a una variable que especifica la posición actual, en unidades del formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="18522-110">Pointer to a variable that specifies the current position, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="18522-111">*dwCurrentFlags*</span><span class="sxs-lookup"><span data-stu-id="18522-111">*dwCurrentFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="18522-112">Combinación bit a bit de marcas.</span><span class="sxs-lookup"><span data-stu-id="18522-112">Bitwise combination of flags.</span></span> <span data-ttu-id="18522-113">Vea [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="18522-113">See [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="18522-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="18522-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="18522-115">Puntero a una variable que especifica la hora de detención, en unidades del formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="18522-115">Pointer to a variable that specifies the stop time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="18522-116">*dwStopFlags*</span><span class="sxs-lookup"><span data-stu-id="18522-116">*dwStopFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="18522-117">Combinación bit a bit de marcas.</span><span class="sxs-lookup"><span data-stu-id="18522-117">Bitwise combination of flags.</span></span> <span data-ttu-id="18522-118">Vea [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="18522-118">See [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) for more information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18522-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="18522-119">Return value</span></span>

<span data-ttu-id="18522-120">Devuelve el valor **HRESULT** del PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="18522-120">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="18522-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18522-121">Requirements</span></span>



| <span data-ttu-id="18522-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="18522-122">Requirement</span></span> | <span data-ttu-id="18522-123">Value</span><span class="sxs-lookup"><span data-stu-id="18522-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18522-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="18522-124">Header</span></span><br/>  | <dl> <span data-ttu-id="18522-125"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="18522-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="18522-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="18522-126">Library</span></span><br/> | <dl> <span data-ttu-id="18522-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="18522-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18522-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="18522-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18522-129">**Clase CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="18522-129">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




