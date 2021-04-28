---
description: 'Método CSourceSeeking.SetTimeFormat: el método SetTimeFormat establece el formato de hora. Este método implementa el método IMediaSeeking::SetTimeFormat.'
ms.assetid: dbc7c950-8cc2-4f8e-adfa-8f5cdc1b56c7
title: Método CSourceSeeking.SetTimeFormat (Ctlutil.h)
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
ms.openlocfilehash: fdb3889ecfa5bdcd49b4054822a2b2d09df58fa6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085203"
---
# <a name="csourceseekingsettimeformat-method"></a><span data-ttu-id="d45f3-104">Método CSourceSeeking.SetTimeFormat</span><span class="sxs-lookup"><span data-stu-id="d45f3-104">CSourceSeeking.SetTimeFormat method</span></span>

<span data-ttu-id="d45f3-105">El `SetTimeFormat` método establece el formato de hora.</span><span class="sxs-lookup"><span data-stu-id="d45f3-105">The `SetTimeFormat` method sets the time format.</span></span> <span data-ttu-id="d45f3-106">Este método implementa el [**método IMediaSeeking::SetTimeFormat.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)</span><span class="sxs-lookup"><span data-stu-id="d45f3-106">This method implements the [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d45f3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d45f3-107">Syntax</span></span>


```C++
HRESULT SetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="d45f3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d45f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d45f3-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="d45f3-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="d45f3-110">Puntero a un GUID de formato de hora.</span><span class="sxs-lookup"><span data-stu-id="d45f3-110">Pointer to a time format GUID.</span></span> <span data-ttu-id="d45f3-111">Consulte [**GUID de formato de hora.**](time-format-guids.md)</span><span class="sxs-lookup"><span data-stu-id="d45f3-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d45f3-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d45f3-112">Return value</span></span>

<span data-ttu-id="d45f3-113">Devuelve uno de los **valores HRESULT** enumerados en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="d45f3-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="d45f3-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d45f3-114">Return code</span></span>                                                                                  | <span data-ttu-id="d45f3-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="d45f3-115">Description</span></span>                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="d45f3-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d45f3-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="d45f3-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="d45f3-117">Success.</span></span><br/>                           |
| <dl> <span data-ttu-id="d45f3-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d45f3-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="d45f3-119">No se admite el formato especificado.</span><span class="sxs-lookup"><span data-stu-id="d45f3-119">Specified format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="d45f3-120"><dt>**PUNTERO \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="d45f3-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="d45f3-121">Argumento de puntero **NULL.**</span><span class="sxs-lookup"><span data-stu-id="d45f3-121">**NULL** pointer argument.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="d45f3-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d45f3-122">Remarks</span></span>

<span data-ttu-id="d45f3-123">El único formato de hora admitido por la clase base es TIME \_ FORMAT \_ MEDIA TIME \_ (unidades de 100 nanosegundos).</span><span class="sxs-lookup"><span data-stu-id="d45f3-123">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="d45f3-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d45f3-124">Requirements</span></span>



| <span data-ttu-id="d45f3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d45f3-125">Requirement</span></span> | <span data-ttu-id="d45f3-126">Value</span><span class="sxs-lookup"><span data-stu-id="d45f3-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d45f3-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d45f3-127">Header</span></span><br/>  | <dl> <span data-ttu-id="d45f3-128"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="d45f3-128"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d45f3-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d45f3-129">Library</span></span><br/> | <dl> <span data-ttu-id="d45f3-130"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d45f3-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d45f3-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d45f3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d45f3-132">**CSourceSeeking (clase)**</span><span class="sxs-lookup"><span data-stu-id="d45f3-132">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




