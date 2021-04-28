---
description: 'Método CSourceSeeking.SetPositions: el método SetPositions establece la posición actual y la posición de detenerse. Este método implementa el método IMediaSeeking::SetPositions.'
ms.assetid: 4359fe1f-f922-4a4d-beaa-8e13c72f407c
title: Método CSourceSeeking.SetPositions (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b09dd92b97166b8d973328ec95e466abbda116bd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085173"
---
# <a name="csourceseekingsetpositions-method"></a><span data-ttu-id="2dbc6-104">Método CSourceSeeking.SetPositions</span><span class="sxs-lookup"><span data-stu-id="2dbc6-104">CSourceSeeking.SetPositions method</span></span>

<span data-ttu-id="2dbc6-105">El `SetPositions` método establece la posición actual y la posición de detenerse.</span><span class="sxs-lookup"><span data-stu-id="2dbc6-105">The `SetPositions` method sets the current position and the stop position.</span></span> <span data-ttu-id="2dbc6-106">Este método implementa el [**método IMediaSeeking::SetPositions.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)</span><span class="sxs-lookup"><span data-stu-id="2dbc6-106">This method implements the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dbc6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2dbc6-107">Syntax</span></span>


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    CurrentFlags,
   LONGLONG *pStop,
   DWORD    StopFlags
);
```



## <a name="parameters"></a><span data-ttu-id="2dbc6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2dbc6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dbc6-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="2dbc6-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="2dbc6-110">Puntero a una variable que especifica la posición actual.</span><span class="sxs-lookup"><span data-stu-id="2dbc6-110">Pointer to a variable that specifies the current position.</span></span>

</dd> <dt>

<span data-ttu-id="2dbc6-111">*CurrentFlags*</span><span class="sxs-lookup"><span data-stu-id="2dbc6-111">*CurrentFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="2dbc6-112">Combinación bit a bit de marcas.</span><span class="sxs-lookup"><span data-stu-id="2dbc6-112">Bitwise combination of flags.</span></span> <span data-ttu-id="2dbc6-113">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="2dbc6-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2dbc6-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="2dbc6-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="2dbc6-115">Puntero a una variable que especifica la hora de detenerse, en unidades del formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="2dbc6-115">Pointer to a variable that specifies the stop time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="2dbc6-116">*StopFlags*</span><span class="sxs-lookup"><span data-stu-id="2dbc6-116">*StopFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="2dbc6-117">Combinación bit a bit de marcas.</span><span class="sxs-lookup"><span data-stu-id="2dbc6-117">Bitwise combination of flags.</span></span> <span data-ttu-id="2dbc6-118">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="2dbc6-118">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dbc6-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2dbc6-119">Return value</span></span>

<span data-ttu-id="2dbc6-120">Devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="2dbc6-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="2dbc6-121">Los valores posibles incluyen los enumerados en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2dbc6-121">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="2dbc6-122">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2dbc6-122">Return code</span></span>                                                                                  | <span data-ttu-id="2dbc6-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="2dbc6-123">Description</span></span>                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="2dbc6-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2dbc6-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="2dbc6-125">Correcto</span><span class="sxs-lookup"><span data-stu-id="2dbc6-125">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="2dbc6-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2dbc6-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="2dbc6-127">Marcas no válidas</span><span class="sxs-lookup"><span data-stu-id="2dbc6-127">Invalid flags</span></span><br/>             |
| <dl> <span data-ttu-id="2dbc6-128"><dt>**PUNTERO \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="2dbc6-128"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="2dbc6-129">**Argumento de** puntero NULL</span><span class="sxs-lookup"><span data-stu-id="2dbc6-129">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2dbc6-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2dbc6-130">Remarks</span></span>

<span data-ttu-id="2dbc6-131">Se admiten las marcas siguientes:</span><span class="sxs-lookup"><span data-stu-id="2dbc6-131">The following flags are supported:</span></span>

-   <span data-ttu-id="2dbc6-132">NoPositioning de AM \_ SEEKING \_</span><span class="sxs-lookup"><span data-stu-id="2dbc6-132">AM\_SEEKING\_NoPositioning</span></span>
-   <span data-ttu-id="2dbc6-133">AM \_ SEEKING \_ AbsolutePositioning</span><span class="sxs-lookup"><span data-stu-id="2dbc6-133">AM\_SEEKING\_AbsolutePositioning</span></span>
-   <span data-ttu-id="2dbc6-134">AM \_ SEEKING \_ RelativePositioning</span><span class="sxs-lookup"><span data-stu-id="2dbc6-134">AM\_SEEKING\_RelativePositioning</span></span>
-   <span data-ttu-id="2dbc6-135">AM \_ SEEKING \_ IncrementalPositioning *(solo pStop)*</span><span class="sxs-lookup"><span data-stu-id="2dbc6-135">AM\_SEEKING\_IncrementalPositioning (*pStop* only)</span></span>

<span data-ttu-id="2dbc6-136">Para obtener más información, [**vea IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span><span class="sxs-lookup"><span data-stu-id="2dbc6-136">For more information, see [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span></span>

<span data-ttu-id="2dbc6-137">Este método actualiza los valores de las variables miembro [**CSourceSeeking::m \_ rtStart**](csourceseeking-m-rtstart.md) y [**CSourceSeeking::m \_ rtStop**](csourceseeking-m-rtstop.md) y, a continuación, llama a los métodos virtuales puros [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md) y [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md).</span><span class="sxs-lookup"><span data-stu-id="2dbc6-137">This method updates the values of the [**CSourceSeeking::m\_rtStart**](csourceseeking-m-rtstart.md) and [**CSourceSeeking::m\_rtStop**](csourceseeking-m-rtstop.md) member variables, and then calls the pure virtual methods [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md) and [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2dbc6-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2dbc6-138">Requirements</span></span>



| <span data-ttu-id="2dbc6-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dbc6-139">Requirement</span></span> | <span data-ttu-id="2dbc6-140">Value</span><span class="sxs-lookup"><span data-stu-id="2dbc6-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dbc6-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2dbc6-141">Header</span></span><br/>  | <dl> <span data-ttu-id="2dbc6-142"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="2dbc6-142"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2dbc6-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2dbc6-143">Library</span></span><br/> | <dl> <span data-ttu-id="2dbc6-144"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2dbc6-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dbc6-145">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2dbc6-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dbc6-146">**CSourceSeeking (clase)**</span><span class="sxs-lookup"><span data-stu-id="2dbc6-146">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




