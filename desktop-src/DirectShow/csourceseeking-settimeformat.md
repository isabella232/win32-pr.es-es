---
description: 'El método SetTimeFormat establece el formato de hora. Este método implementa el método IMediaSeeking:: SetTimeFormat.'
ms.assetid: dbc7c950-8cc2-4f8e-adfa-8f5cdc1b56c7
title: Método CSourceSeeking. SetTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 61ab0cdf7c954e0fa5f370127f00529bb9ef7b16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661393"
---
# <a name="csourceseekingsettimeformat-method"></a><span data-ttu-id="db55f-104">CSourceSeeking. SetTimeFormat, método</span><span class="sxs-lookup"><span data-stu-id="db55f-104">CSourceSeeking.SetTimeFormat method</span></span>

<span data-ttu-id="db55f-105">El `SetTimeFormat` método establece el formato de hora.</span><span class="sxs-lookup"><span data-stu-id="db55f-105">The `SetTimeFormat` method sets the time format.</span></span> <span data-ttu-id="db55f-106">Este método implementa el método [**IMediaSeeking:: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) .</span><span class="sxs-lookup"><span data-stu-id="db55f-106">This method implements the [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="db55f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="db55f-107">Syntax</span></span>


```C++
HRESULT SetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="db55f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db55f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db55f-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="db55f-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="db55f-110">Puntero a un GUID de formato de hora.</span><span class="sxs-lookup"><span data-stu-id="db55f-110">Pointer to a time format GUID.</span></span> <span data-ttu-id="db55f-111">Consulte [**GUID de formato de hora**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="db55f-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db55f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="db55f-112">Return value</span></span>

<span data-ttu-id="db55f-113">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="db55f-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="db55f-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="db55f-114">Return code</span></span>                                                                                  | <span data-ttu-id="db55f-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="db55f-115">Description</span></span>                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="db55f-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="db55f-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="db55f-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="db55f-117">Success.</span></span><br/>                           |
| <dl> <span data-ttu-id="db55f-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="db55f-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="db55f-119">No se admite el formato especificado.</span><span class="sxs-lookup"><span data-stu-id="db55f-119">Specified format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="db55f-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="db55f-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="db55f-121">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="db55f-121">**NULL** pointer argument.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="db55f-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db55f-122">Remarks</span></span>

<span data-ttu-id="db55f-123">El único formato de hora admitido por la clase base es el \_ formato \_ de hora \_ tiempo medio (100-nanosegundos).</span><span class="sxs-lookup"><span data-stu-id="db55f-123">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="db55f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db55f-124">Requirements</span></span>



| <span data-ttu-id="db55f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="db55f-125">Requirement</span></span> | <span data-ttu-id="db55f-126">Value</span><span class="sxs-lookup"><span data-stu-id="db55f-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db55f-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db55f-127">Header</span></span><br/>  | <dl> <span data-ttu-id="db55f-128"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="db55f-128"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="db55f-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="db55f-129">Library</span></span><br/> | <dl> <span data-ttu-id="db55f-130"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="db55f-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db55f-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="db55f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db55f-132">**Clase CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="db55f-132">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




