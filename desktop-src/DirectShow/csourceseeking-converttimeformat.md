---
description: 'El método ConvertTimeFormat convierte de un formato de hora a otro. Este método implementa el método IMediaSeeking:: ConvertTimeFormat.'
ms.assetid: d0cb44fa-30c1-41b4-92a4-7169161e3140
title: Método CSourceSeeking. ConvertTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3869ef5bc9656414ca5b465a04d04a4ca4be41e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690132"
---
# <a name="csourceseekingconverttimeformat-method"></a><span data-ttu-id="fab0e-104">CSourceSeeking. ConvertTimeFormat, método</span><span class="sxs-lookup"><span data-stu-id="fab0e-104">CSourceSeeking.ConvertTimeFormat method</span></span>

<span data-ttu-id="fab0e-105">El `ConvertTimeFormat` método convierte de un formato de hora a otro.</span><span class="sxs-lookup"><span data-stu-id="fab0e-105">The `ConvertTimeFormat` method converts from one time format to another.</span></span> <span data-ttu-id="fab0e-106">Este método implementa el método [**IMediaSeeking:: ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) .</span><span class="sxs-lookup"><span data-stu-id="fab0e-106">This method implements the [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fab0e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fab0e-107">Syntax</span></span>


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a><span data-ttu-id="fab0e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fab0e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fab0e-109">*pTarget*</span><span class="sxs-lookup"><span data-stu-id="fab0e-109">*pTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="fab0e-110">Puntero a una variable que recibe la hora convertida.</span><span class="sxs-lookup"><span data-stu-id="fab0e-110">Pointer to a variable that receives the converted time.</span></span>

</dd> <dt>

<span data-ttu-id="fab0e-111">*pTargetFormat*</span><span class="sxs-lookup"><span data-stu-id="fab0e-111">*pTargetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="fab0e-112">Puntero al GUID del formato de destino.</span><span class="sxs-lookup"><span data-stu-id="fab0e-112">Pointer to the GUID of the target format.</span></span> <span data-ttu-id="fab0e-113">Si es **null**, se usa el formato actual.</span><span class="sxs-lookup"><span data-stu-id="fab0e-113">If **NULL**, the current format is used.</span></span> <span data-ttu-id="fab0e-114">Consulte [**GUID de formato de hora**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="fab0e-114">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> <dt>

<span data-ttu-id="fab0e-115">*Origen*</span><span class="sxs-lookup"><span data-stu-id="fab0e-115">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="fab0e-116">Valor de hora que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="fab0e-116">Time value to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="fab0e-117">*pSourceFormat*</span><span class="sxs-lookup"><span data-stu-id="fab0e-117">*pSourceFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="fab0e-118">Puntero al GUID del formato de hora del formato que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="fab0e-118">Pointer to the time format GUID of the format to convert.</span></span> <span data-ttu-id="fab0e-119">Si es **null**, se usa el formato actual.</span><span class="sxs-lookup"><span data-stu-id="fab0e-119">If **NULL**, the current format is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fab0e-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fab0e-120">Return value</span></span>

<span data-ttu-id="fab0e-121">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="fab0e-121">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="fab0e-122">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="fab0e-122">Return code</span></span>                                                                                  | <span data-ttu-id="fab0e-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="fab0e-123">Description</span></span>                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="fab0e-124"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="fab0e-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="fab0e-125">Correcto</span><span class="sxs-lookup"><span data-stu-id="fab0e-125">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="fab0e-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="fab0e-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="fab0e-127">Argumento no válido</span><span class="sxs-lookup"><span data-stu-id="fab0e-127">Invalid argument</span></span><br/>          |
| <dl> <span data-ttu-id="fab0e-128"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="fab0e-128"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="fab0e-129">Argumento de puntero **nulo**</span><span class="sxs-lookup"><span data-stu-id="fab0e-129">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fab0e-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fab0e-130">Remarks</span></span>

<span data-ttu-id="fab0e-131">El único formato de hora admitido por la clase base es el \_ formato \_ de hora \_ tiempo medio (100-nanosegundos).</span><span class="sxs-lookup"><span data-stu-id="fab0e-131">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span> <span data-ttu-id="fab0e-132">Este método devuelve E \_ INVALIDARG, excepto en el caso trivial en el que *PTargetFormat* y *pSourceFormat* especifican el formato de hora de tiempo \_ \_ medio \_ .</span><span class="sxs-lookup"><span data-stu-id="fab0e-132">This method returns E\_INVALIDARG, except in the trivial case where *pTargetFormat* and *pSourceFormat* both specify TIME\_FORMAT\_MEDIA\_TIME.</span></span>

## <a name="requirements"></a><span data-ttu-id="fab0e-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fab0e-133">Requirements</span></span>



| <span data-ttu-id="fab0e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="fab0e-134">Requirement</span></span> | <span data-ttu-id="fab0e-135">Value</span><span class="sxs-lookup"><span data-stu-id="fab0e-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fab0e-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fab0e-136">Header</span></span><br/>  | <dl> <span data-ttu-id="fab0e-137"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fab0e-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fab0e-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fab0e-138">Library</span></span><br/> | <dl> <span data-ttu-id="fab0e-139"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="fab0e-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fab0e-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="fab0e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fab0e-141">**Clase CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="fab0e-141">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




