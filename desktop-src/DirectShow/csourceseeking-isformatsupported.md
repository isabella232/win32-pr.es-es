---
description: 'Método CSourceSeeking.IsFormatSupported: el método IsFormatSupported determina si se admite un formato de hora especificado. Este método implementa el método IMediaSeeking::IsFormatSupported.'
ms.assetid: 79b6dfd4-7f03-479b-b855-8f389bf6cbc7
title: Método CSourceSeeking.IsFormatSupported (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.IsFormatSupported
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c58e8edd908c101c3045e221cc86420cbb5cb94
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098753"
---
# <a name="csourceseekingisformatsupported-method"></a><span data-ttu-id="fde12-104">Método CSourceSeeking.IsFormatSupported</span><span class="sxs-lookup"><span data-stu-id="fde12-104">CSourceSeeking.IsFormatSupported method</span></span>

<span data-ttu-id="fde12-105">El `IsFormatSupported` método determina si se admite un formato de hora especificado.</span><span class="sxs-lookup"><span data-stu-id="fde12-105">The `IsFormatSupported` method determines whether a specified time format is supported.</span></span> <span data-ttu-id="fde12-106">Este método implementa el [**método IMediaSeeking::IsFormatSupported.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported)</span><span class="sxs-lookup"><span data-stu-id="fde12-106">This method implements the [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fde12-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fde12-107">Syntax</span></span>


```C++
HRESULT IsFormatSupported(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="fde12-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fde12-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fde12-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="fde12-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="fde12-110">Puntero a un GUID de formato de hora.</span><span class="sxs-lookup"><span data-stu-id="fde12-110">Pointer to a time format GUID.</span></span> <span data-ttu-id="fde12-111">Consulte [**GUID de formato de hora.**](time-format-guids.md)</span><span class="sxs-lookup"><span data-stu-id="fde12-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fde12-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fde12-112">Return value</span></span>

<span data-ttu-id="fde12-113">Devuelve uno de los **valores HRESULT** enumerados en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="fde12-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="fde12-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="fde12-114">Return code</span></span>                                                                               | <span data-ttu-id="fde12-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="fde12-115">Description</span></span>                             |
|-------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="fde12-116"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="fde12-116"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="fde12-117">No se admite el formato.</span><span class="sxs-lookup"><span data-stu-id="fde12-117">The format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="fde12-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fde12-118"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="fde12-119">Se admite el formato .</span><span class="sxs-lookup"><span data-stu-id="fde12-119">The format is supported.</span></span><br/>     |
| <dl> <span data-ttu-id="fde12-120"><dt>**PUNTERO \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="fde12-120"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="fde12-121">**Argumento de** puntero NULL.</span><span class="sxs-lookup"><span data-stu-id="fde12-121">**NULL** pointer argument.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="fde12-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fde12-122">Remarks</span></span>

<span data-ttu-id="fde12-123">El único formato de hora admitido por la clase base es TIME \_ FORMAT \_ MEDIA TIME \_ (unidades de 100 nanosegundos).</span><span class="sxs-lookup"><span data-stu-id="fde12-123">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="fde12-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fde12-124">Requirements</span></span>



| <span data-ttu-id="fde12-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="fde12-125">Requirement</span></span> | <span data-ttu-id="fde12-126">Value</span><span class="sxs-lookup"><span data-stu-id="fde12-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fde12-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fde12-127">Header</span></span><br/>  | <dl> <span data-ttu-id="fde12-128"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="fde12-128"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fde12-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fde12-129">Library</span></span><br/> | <dl> <span data-ttu-id="fde12-130"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="fde12-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fde12-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fde12-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fde12-132">**CSourceSeeking (clase)**</span><span class="sxs-lookup"><span data-stu-id="fde12-132">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




