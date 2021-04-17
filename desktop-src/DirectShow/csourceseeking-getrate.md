---
description: 'El método GetRate recupera la velocidad de reproducción. Este método implementa el método IMediaSeeking:: GetRate.'
ms.assetid: e5c3ef27-6f57-4c74-b197-a3c4efb31239
title: Método CSourceSeeking. GetRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b14cad0b043193f7ee410455aaa399e3bcb26715
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660779"
---
# <a name="csourceseekinggetrate-method"></a><span data-ttu-id="d7371-104">CSourceSeeking. GetRate, método</span><span class="sxs-lookup"><span data-stu-id="d7371-104">CSourceSeeking.GetRate method</span></span>

<span data-ttu-id="d7371-105">El `GetRate` método recupera la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="d7371-105">The `GetRate` method retrieves the playback rate.</span></span> <span data-ttu-id="d7371-106">Este método implementa el método [**IMediaSeeking:: GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) .</span><span class="sxs-lookup"><span data-stu-id="d7371-106">This method implements the [**IMediaSeeking::GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7371-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7371-107">Syntax</span></span>


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a><span data-ttu-id="d7371-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7371-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7371-109">*pdRate*</span><span class="sxs-lookup"><span data-stu-id="d7371-109">*pdRate*</span></span> 
</dt> <dd>

<span data-ttu-id="d7371-110">Puntero a una variable que recibe la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="d7371-110">Pointer to a variable that receives the playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7371-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7371-111">Return value</span></span>

<span data-ttu-id="d7371-112">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="d7371-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="d7371-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d7371-113">Return code</span></span>                                                                               | <span data-ttu-id="d7371-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7371-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="d7371-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="d7371-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="d7371-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="d7371-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="d7371-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="d7371-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="d7371-118">Valor de puntero **nulo**</span><span class="sxs-lookup"><span data-stu-id="d7371-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d7371-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7371-119">Remarks</span></span>

<span data-ttu-id="d7371-120">La velocidad de reproducción se especifica mediante la variable miembro [**CSourceSeeking:: m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) .</span><span class="sxs-lookup"><span data-stu-id="d7371-120">The playback rate is specified by the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7371-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7371-121">Requirements</span></span>



| <span data-ttu-id="d7371-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7371-122">Requirement</span></span> | <span data-ttu-id="d7371-123">Value</span><span class="sxs-lookup"><span data-stu-id="d7371-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7371-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7371-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d7371-125"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d7371-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d7371-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d7371-126">Library</span></span><br/> | <dl> <span data-ttu-id="d7371-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d7371-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7371-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7371-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7371-129">**Clase CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="d7371-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




