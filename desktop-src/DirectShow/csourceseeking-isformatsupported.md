---
description: 'El método IsFormatSupported determina si se admite un formato de hora especificado. Este método implementa el método IMediaSeeking:: IsFormatSupported.'
ms.assetid: 79b6dfd4-7f03-479b-b855-8f389bf6cbc7
title: Método CSourceSeeking. IsFormatSupported (Ctlutil. h)
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
ms.openlocfilehash: 7d027a2ee6e94e4ccf4944c27e77f02d1d1c5edb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690553"
---
# <a name="csourceseekingisformatsupported-method"></a><span data-ttu-id="16987-104">CSourceSeeking. IsFormatSupported, método</span><span class="sxs-lookup"><span data-stu-id="16987-104">CSourceSeeking.IsFormatSupported method</span></span>

<span data-ttu-id="16987-105">El `IsFormatSupported` método determina si se admite un formato de hora especificado.</span><span class="sxs-lookup"><span data-stu-id="16987-105">The `IsFormatSupported` method determines whether a specified time format is supported.</span></span> <span data-ttu-id="16987-106">Este método implementa el método [**IMediaSeeking:: IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) .</span><span class="sxs-lookup"><span data-stu-id="16987-106">This method implements the [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="16987-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="16987-107">Syntax</span></span>


```C++
HRESULT IsFormatSupported(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="16987-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="16987-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16987-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="16987-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="16987-110">Puntero a un GUID de formato de hora.</span><span class="sxs-lookup"><span data-stu-id="16987-110">Pointer to a time format GUID.</span></span> <span data-ttu-id="16987-111">Consulte [**GUID de formato de hora**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="16987-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16987-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="16987-112">Return value</span></span>

<span data-ttu-id="16987-113">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="16987-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="16987-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="16987-114">Return code</span></span>                                                                               | <span data-ttu-id="16987-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="16987-115">Description</span></span>                             |
|-------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="16987-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="16987-116"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="16987-117">No se admite el formato.</span><span class="sxs-lookup"><span data-stu-id="16987-117">The format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="16987-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="16987-118"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="16987-119">Se admite el formato.</span><span class="sxs-lookup"><span data-stu-id="16987-119">The format is supported.</span></span><br/>     |
| <dl> <span data-ttu-id="16987-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="16987-120"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="16987-121">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="16987-121">**NULL** pointer argument.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="16987-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="16987-122">Remarks</span></span>

<span data-ttu-id="16987-123">El único formato de hora admitido por la clase base es el \_ formato \_ de hora \_ tiempo medio (100-nanosegundos).</span><span class="sxs-lookup"><span data-stu-id="16987-123">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="16987-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16987-124">Requirements</span></span>



| <span data-ttu-id="16987-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="16987-125">Requirement</span></span> | <span data-ttu-id="16987-126">Value</span><span class="sxs-lookup"><span data-stu-id="16987-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16987-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="16987-127">Header</span></span><br/>  | <dl> <span data-ttu-id="16987-128"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="16987-128"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="16987-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="16987-129">Library</span></span><br/> | <dl> <span data-ttu-id="16987-130"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="16987-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16987-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="16987-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16987-132">**Clase CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="16987-132">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




