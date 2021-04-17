---
description: 'El método SetPositions establece la posición actual y la posición de detención. Este método implementa el método IMediaSeeking:: SetPositions.'
ms.assetid: 4359fe1f-f922-4a4d-beaa-8e13c72f407c
title: Método CSourceSeeking. SetPositions (Ctlutil. h)
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
ms.openlocfilehash: 342ca7d85fe9358b914709b7887216b62e03521d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660640"
---
# <a name="csourceseekingsetpositions-method"></a><span data-ttu-id="4a390-104">CSourceSeeking. SetPositions, método</span><span class="sxs-lookup"><span data-stu-id="4a390-104">CSourceSeeking.SetPositions method</span></span>

<span data-ttu-id="4a390-105">El `SetPositions` método establece la posición actual y la posición de detención.</span><span class="sxs-lookup"><span data-stu-id="4a390-105">The `SetPositions` method sets the current position and the stop position.</span></span> <span data-ttu-id="4a390-106">Este método implementa el método [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="4a390-106">This method implements the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a390-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a390-107">Syntax</span></span>


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    CurrentFlags,
   LONGLONG *pStop,
   DWORD    StopFlags
);
```



## <a name="parameters"></a><span data-ttu-id="4a390-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a390-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a390-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="4a390-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="4a390-110">Puntero a una variable que especifica la posición actual.</span><span class="sxs-lookup"><span data-stu-id="4a390-110">Pointer to a variable that specifies the current position.</span></span>

</dd> <dt>

<span data-ttu-id="4a390-111">*CurrentFlags*</span><span class="sxs-lookup"><span data-stu-id="4a390-111">*CurrentFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="4a390-112">Combinación bit a bit de marcas.</span><span class="sxs-lookup"><span data-stu-id="4a390-112">Bitwise combination of flags.</span></span> <span data-ttu-id="4a390-113">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="4a390-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4a390-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="4a390-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="4a390-115">Puntero a una variable que especifica la hora de detención, en unidades del formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="4a390-115">Pointer to a variable that specifies the stop time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="4a390-116">*StopFlags*</span><span class="sxs-lookup"><span data-stu-id="4a390-116">*StopFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="4a390-117">Combinación bit a bit de marcas.</span><span class="sxs-lookup"><span data-stu-id="4a390-117">Bitwise combination of flags.</span></span> <span data-ttu-id="4a390-118">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="4a390-118">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a390-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a390-119">Return value</span></span>

<span data-ttu-id="4a390-120">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4a390-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4a390-121">Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="4a390-121">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="4a390-122">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4a390-122">Return code</span></span>                                                                                  | <span data-ttu-id="4a390-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a390-123">Description</span></span>                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="4a390-124"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="4a390-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="4a390-125">Correcto</span><span class="sxs-lookup"><span data-stu-id="4a390-125">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="4a390-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4a390-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="4a390-127">Marcas no válidas</span><span class="sxs-lookup"><span data-stu-id="4a390-127">Invalid flags</span></span><br/>             |
| <dl> <span data-ttu-id="4a390-128"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="4a390-128"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="4a390-129">Argumento de puntero **nulo**</span><span class="sxs-lookup"><span data-stu-id="4a390-129">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4a390-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4a390-130">Remarks</span></span>

<span data-ttu-id="4a390-131">Se admiten las marcas siguientes:</span><span class="sxs-lookup"><span data-stu-id="4a390-131">The following flags are supported:</span></span>

-   <span data-ttu-id="4a390-132">\_Busca \_ nopositioning</span><span class="sxs-lookup"><span data-stu-id="4a390-132">AM\_SEEKING\_NoPositioning</span></span>
-   <span data-ttu-id="4a390-133">\_Búsqueda de \_ AbsolutePositioning</span><span class="sxs-lookup"><span data-stu-id="4a390-133">AM\_SEEKING\_AbsolutePositioning</span></span>
-   <span data-ttu-id="4a390-134">\_Búsqueda de \_ RelativePositioning</span><span class="sxs-lookup"><span data-stu-id="4a390-134">AM\_SEEKING\_RelativePositioning</span></span>
-   <span data-ttu-id="4a390-135">AM \_ Buscar \_ IncrementalPositioning (solo *pStop* )</span><span class="sxs-lookup"><span data-stu-id="4a390-135">AM\_SEEKING\_IncrementalPositioning (*pStop* only)</span></span>

<span data-ttu-id="4a390-136">Para obtener más información, vea [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span><span class="sxs-lookup"><span data-stu-id="4a390-136">For more information, see [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span></span>

<span data-ttu-id="4a390-137">Este método actualiza los valores de las variables de miembro [**CSourceSeeking:: m \_ RtStart**](csourceseeking-m-rtstart.md) y [**CSourceSeeking:: m \_ rtStop**](csourceseeking-m-rtstop.md) y, a continuación, llama a los métodos virtuales puros [**CSourceSeeking:: cambie las**](csourceseeking-changestart.md) y [**CSourceSeeking:: ChangeStop**](csourceseeking-changestop.md).</span><span class="sxs-lookup"><span data-stu-id="4a390-137">This method updates the values of the [**CSourceSeeking::m\_rtStart**](csourceseeking-m-rtstart.md) and [**CSourceSeeking::m\_rtStop**](csourceseeking-m-rtstop.md) member variables, and then calls the pure virtual methods [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md) and [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4a390-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a390-138">Requirements</span></span>



| <span data-ttu-id="4a390-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a390-139">Requirement</span></span> | <span data-ttu-id="4a390-140">Value</span><span class="sxs-lookup"><span data-stu-id="4a390-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a390-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a390-141">Header</span></span><br/>  | <dl> <span data-ttu-id="4a390-142"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a390-142"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4a390-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4a390-143">Library</span></span><br/> | <dl> <span data-ttu-id="4a390-144"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="4a390-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a390-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a390-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a390-146">**Clase CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="4a390-146">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




