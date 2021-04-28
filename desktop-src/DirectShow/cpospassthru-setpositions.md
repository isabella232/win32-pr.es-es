---
description: 'Método CPosPassThru.SetPositions: el método SetPositions establece la posición actual y la posición de detenerse. Este método implementa el método IMediaSeeking::SetPositions.'
ms.assetid: d4425221-e20f-4e51-8a33-a74fa21f9117
title: Método CPosPassThru.SetPositions (Ctlutil.h)
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
ms.openlocfilehash: f8c61f24ab51ffe7fa161830ef9a0c8bdd167256
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085483"
---
# <a name="cpospassthrusetpositions-method"></a><span data-ttu-id="5c691-104">Método CPosPassThru.SetPositions</span><span class="sxs-lookup"><span data-stu-id="5c691-104">CPosPassThru.SetPositions method</span></span>

<span data-ttu-id="5c691-105">El `SetPositions` método establece la posición actual y la posición de detenerse.</span><span class="sxs-lookup"><span data-stu-id="5c691-105">The `SetPositions` method sets the current position and the stop position.</span></span> <span data-ttu-id="5c691-106">Este método implementa el [**método IMediaSeeking::SetPositions.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)</span><span class="sxs-lookup"><span data-stu-id="5c691-106">This method implements the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c691-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c691-107">Syntax</span></span>


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    dwCurrentFlags,
   LONGLONG *pStop,
   DWORD    dwStopFlags
);
```



## <a name="parameters"></a><span data-ttu-id="5c691-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5c691-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c691-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="5c691-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="5c691-110">Puntero a una variable que especifica la posición actual, en unidades del formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="5c691-110">Pointer to a variable that specifies the current position, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="5c691-111">*dwCurrentFlags*</span><span class="sxs-lookup"><span data-stu-id="5c691-111">*dwCurrentFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="5c691-112">Combinación bit a bit de marcas.</span><span class="sxs-lookup"><span data-stu-id="5c691-112">Bitwise combination of flags.</span></span> <span data-ttu-id="5c691-113">Consulte [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="5c691-113">See [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="5c691-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="5c691-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="5c691-115">Puntero a una variable que especifica la hora de detenerse, en unidades del formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="5c691-115">Pointer to a variable that specifies the stop time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="5c691-116">*dwStopFlags*</span><span class="sxs-lookup"><span data-stu-id="5c691-116">*dwStopFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="5c691-117">Combinación bit a bit de marcas.</span><span class="sxs-lookup"><span data-stu-id="5c691-117">Bitwise combination of flags.</span></span> <span data-ttu-id="5c691-118">Consulte [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="5c691-118">See [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) for more information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c691-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5c691-119">Return value</span></span>

<span data-ttu-id="5c691-120">Devuelve el **valor HRESULT** del pin conectado.</span><span class="sxs-lookup"><span data-stu-id="5c691-120">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c691-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c691-121">Requirements</span></span>



| <span data-ttu-id="5c691-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c691-122">Requirement</span></span> | <span data-ttu-id="5c691-123">Value</span><span class="sxs-lookup"><span data-stu-id="5c691-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c691-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5c691-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5c691-125"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="5c691-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5c691-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5c691-126">Library</span></span><br/> | <dl> <span data-ttu-id="5c691-127"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5c691-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c691-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5c691-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c691-129">**CPosPassThru (clase)**</span><span class="sxs-lookup"><span data-stu-id="5c691-129">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




