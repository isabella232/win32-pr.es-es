---
description: 'Método CPosPassThru.ConvertTimeFormat: el método ConvertTimeFormat se convierte de un formato de hora a otro. Este método implementa el método IMediaSeeking::ConvertTimeFormat.'
ms.assetid: e766d112-ee41-4c64-a735-b6317093518a
title: Método CPosPassThru.ConvertTimeFormat (Ctlutil.h)
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
ms.openlocfilehash: fc463cb6dc891e677266289971a1dac8b335a8c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098963"
---
# <a name="cpospassthruconverttimeformat-method"></a><span data-ttu-id="e6e4e-104">Método CPosPassThru.ConvertTimeFormat</span><span class="sxs-lookup"><span data-stu-id="e6e4e-104">CPosPassThru.ConvertTimeFormat method</span></span>

<span data-ttu-id="e6e4e-105">El `ConvertTimeFormat` método convierte de un formato de hora a otro.</span><span class="sxs-lookup"><span data-stu-id="e6e4e-105">The `ConvertTimeFormat` method converts from one time format to another.</span></span> <span data-ttu-id="e6e4e-106">Este método implementa el [**método IMediaSeeking::ConvertTimeFormat.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat)</span><span class="sxs-lookup"><span data-stu-id="e6e4e-106">This method implements the [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6e4e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6e4e-107">Syntax</span></span>


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a><span data-ttu-id="e6e4e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6e4e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6e4e-109">*pTarget*</span><span class="sxs-lookup"><span data-stu-id="e6e4e-109">*pTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="e6e4e-110">Puntero a una variable que recibe la hora convertida.</span><span class="sxs-lookup"><span data-stu-id="e6e4e-110">Pointer to a variable that receives the converted time.</span></span>

</dd> <dt>

<span data-ttu-id="e6e4e-111">*pTargetFormat*</span><span class="sxs-lookup"><span data-stu-id="e6e4e-111">*pTargetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="e6e4e-112">Puntero al GUID de formato de hora del formato de destino.</span><span class="sxs-lookup"><span data-stu-id="e6e4e-112">Pointer to the time format GUID of the target format.</span></span> <span data-ttu-id="e6e4e-113">Si **es NULL,** se usa el formato actual.</span><span class="sxs-lookup"><span data-stu-id="e6e4e-113">If **NULL**, the current format is used.</span></span>

</dd> <dt>

<span data-ttu-id="e6e4e-114">*Origen*</span><span class="sxs-lookup"><span data-stu-id="e6e4e-114">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="e6e4e-115">Valor de hora que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="e6e4e-115">Time value to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="e6e4e-116">*pSourceFormat*</span><span class="sxs-lookup"><span data-stu-id="e6e4e-116">*pSourceFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="e6e4e-117">Puntero al GUID de formato de hora del formato que se convertirá.</span><span class="sxs-lookup"><span data-stu-id="e6e4e-117">Pointer to the time format GUID of the format to convert.</span></span> <span data-ttu-id="e6e4e-118">Si **es NULL,** se usa el formato actual.</span><span class="sxs-lookup"><span data-stu-id="e6e4e-118">If **NULL**, the current format is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6e4e-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6e4e-119">Return value</span></span>

<span data-ttu-id="e6e4e-120">Devuelve el **valor HRESULT** del pin conectado.</span><span class="sxs-lookup"><span data-stu-id="e6e4e-120">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6e4e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6e4e-121">Requirements</span></span>



| <span data-ttu-id="e6e4e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6e4e-122">Requirement</span></span> | <span data-ttu-id="e6e4e-123">Value</span><span class="sxs-lookup"><span data-stu-id="e6e4e-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6e4e-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6e4e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e6e4e-125"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6e4e-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e6e4e-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e6e4e-126">Library</span></span><br/> | <dl> <span data-ttu-id="e6e4e-127"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e6e4e-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6e4e-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e6e4e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6e4e-129">**CPosPassThru (clase)**</span><span class="sxs-lookup"><span data-stu-id="e6e4e-129">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="e6e4e-130">**GUID de formato de hora**</span><span class="sxs-lookup"><span data-stu-id="e6e4e-130">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




