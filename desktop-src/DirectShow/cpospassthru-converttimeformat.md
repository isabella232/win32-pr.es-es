---
description: 'El método ConvertTimeFormat convierte de un formato de hora a otro. Este método implementa el método IMediaSeeking:: ConvertTimeFormat.'
ms.assetid: e766d112-ee41-4c64-a735-b6317093518a
title: Método CPosPassThru. ConvertTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bcce3e24c46e3e59c6bad6b4fbd60b139806de73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680473"
---
# <a name="cpospassthruconverttimeformat-method"></a><span data-ttu-id="811b6-104">CPosPassThru. ConvertTimeFormat, método</span><span class="sxs-lookup"><span data-stu-id="811b6-104">CPosPassThru.ConvertTimeFormat method</span></span>

<span data-ttu-id="811b6-105">El `ConvertTimeFormat` método convierte de un formato de hora a otro.</span><span class="sxs-lookup"><span data-stu-id="811b6-105">The `ConvertTimeFormat` method converts from one time format to another.</span></span> <span data-ttu-id="811b6-106">Este método implementa el método [**IMediaSeeking:: ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) .</span><span class="sxs-lookup"><span data-stu-id="811b6-106">This method implements the [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="811b6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="811b6-107">Syntax</span></span>


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a><span data-ttu-id="811b6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="811b6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="811b6-109">*pTarget*</span><span class="sxs-lookup"><span data-stu-id="811b6-109">*pTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="811b6-110">Puntero a una variable que recibe la hora convertida.</span><span class="sxs-lookup"><span data-stu-id="811b6-110">Pointer to a variable that receives the converted time.</span></span>

</dd> <dt>

<span data-ttu-id="811b6-111">*pTargetFormat*</span><span class="sxs-lookup"><span data-stu-id="811b6-111">*pTargetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="811b6-112">Puntero al GUID del formato de hora del formato de destino.</span><span class="sxs-lookup"><span data-stu-id="811b6-112">Pointer to the time format GUID of the target format.</span></span> <span data-ttu-id="811b6-113">Si es **null**, se usa el formato actual.</span><span class="sxs-lookup"><span data-stu-id="811b6-113">If **NULL**, the current format is used.</span></span>

</dd> <dt>

<span data-ttu-id="811b6-114">*Origen*</span><span class="sxs-lookup"><span data-stu-id="811b6-114">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="811b6-115">Valor de hora que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="811b6-115">Time value to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="811b6-116">*pSourceFormat*</span><span class="sxs-lookup"><span data-stu-id="811b6-116">*pSourceFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="811b6-117">Puntero al GUID del formato de hora del formato que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="811b6-117">Pointer to the time format GUID of the format to convert.</span></span> <span data-ttu-id="811b6-118">Si es **null**, se usa el formato actual.</span><span class="sxs-lookup"><span data-stu-id="811b6-118">If **NULL**, the current format is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="811b6-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="811b6-119">Return value</span></span>

<span data-ttu-id="811b6-120">Devuelve el valor **HRESULT** del PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="811b6-120">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="811b6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="811b6-121">Requirements</span></span>



| <span data-ttu-id="811b6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="811b6-122">Requirement</span></span> | <span data-ttu-id="811b6-123">Value</span><span class="sxs-lookup"><span data-stu-id="811b6-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="811b6-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="811b6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="811b6-125"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="811b6-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="811b6-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="811b6-126">Library</span></span><br/> | <dl> <span data-ttu-id="811b6-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="811b6-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="811b6-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="811b6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="811b6-129">**Clase CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="811b6-129">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="811b6-130">**GUID de formato de hora**</span><span class="sxs-lookup"><span data-stu-id="811b6-130">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




