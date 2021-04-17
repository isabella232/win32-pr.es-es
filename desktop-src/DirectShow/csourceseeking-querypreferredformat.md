---
description: 'El método QueryPreferredFormat recupera el formato de hora preferido del objeto. Este método implementa el método IMediaSeeking:: QueryPreferredFormat.'
ms.assetid: 3b73b7cf-1ba7-47c5-8442-5f138b74f335
title: Método CSourceSeeking. QueryPreferredFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.QueryPreferredFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8916e23756279dd30eaf177ef839944a4c68d61a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690467"
---
# <a name="csourceseekingquerypreferredformat-method"></a><span data-ttu-id="14362-104">CSourceSeeking. QueryPreferredFormat, método</span><span class="sxs-lookup"><span data-stu-id="14362-104">CSourceSeeking.QueryPreferredFormat method</span></span>

<span data-ttu-id="14362-105">El `QueryPreferredFormat` método recupera el formato de hora preferido del objeto.</span><span class="sxs-lookup"><span data-stu-id="14362-105">The `QueryPreferredFormat` method retrieves the object's preferred time format.</span></span> <span data-ttu-id="14362-106">Este método implementa el método [**IMediaSeeking:: QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) .</span><span class="sxs-lookup"><span data-stu-id="14362-106">This method implements the [**IMediaSeeking::QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="14362-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14362-107">Syntax</span></span>


```C++
HRESULT QueryPreferredFormat(
   GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="14362-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14362-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14362-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="14362-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="14362-110">Puntero a una variable que recibe un GUID con formato de hora.</span><span class="sxs-lookup"><span data-stu-id="14362-110">Pointer to a variable that receives a time format GUID.</span></span> <span data-ttu-id="14362-111">Consulte [**GUID de formato de hora**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="14362-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14362-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14362-112">Return value</span></span>

<span data-ttu-id="14362-113">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="14362-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="14362-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="14362-114">Return code</span></span>                                                                               | <span data-ttu-id="14362-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="14362-115">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="14362-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="14362-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="14362-117">Correcto</span><span class="sxs-lookup"><span data-stu-id="14362-117">Success</span></span><br/>                |
| <dl> <span data-ttu-id="14362-118"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="14362-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="14362-119">Valor de puntero **nulo**</span><span class="sxs-lookup"><span data-stu-id="14362-119">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="14362-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="14362-120">Remarks</span></span>

<span data-ttu-id="14362-121">El único formato de hora admitido por la clase base es el \_ formato \_ de hora \_ tiempo medio (100-nanosegundos).</span><span class="sxs-lookup"><span data-stu-id="14362-121">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="14362-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14362-122">Requirements</span></span>



| <span data-ttu-id="14362-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="14362-123">Requirement</span></span> | <span data-ttu-id="14362-124">Value</span><span class="sxs-lookup"><span data-stu-id="14362-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14362-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="14362-125">Header</span></span><br/>  | <dl> <span data-ttu-id="14362-126"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14362-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="14362-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="14362-127">Library</span></span><br/> | <dl> <span data-ttu-id="14362-128"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="14362-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14362-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="14362-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14362-130">**Clase CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="14362-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




