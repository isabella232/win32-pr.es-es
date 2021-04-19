---
description: El método RegisterMediaTime almacena en caché las marcas de tiempo del ejemplo actual.
ms.assetid: 9ff8e4ec-3401-4272-894d-643f0fc029de
title: Método CRendererPosPassThru. RegisterMediaTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.RegisterMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3c829690572d55ea700d51124b99370f23e755a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660452"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh"></a><span data-ttu-id="b523f-103">Método CRendererPosPassThru. RegisterMediaTime (Ctlutil. h)</span><span class="sxs-lookup"><span data-stu-id="b523f-103">CRendererPosPassThru.RegisterMediaTime method (Ctlutil.h)</span></span>

<span data-ttu-id="b523f-104">El método **RegisterMediaTime** almacena en caché las marcas de tiempo del ejemplo actual.</span><span class="sxs-lookup"><span data-stu-id="b523f-104">The **RegisterMediaTime** method caches the time stamps from the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="b523f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b523f-105">Syntax</span></span>


```C++
HRESULT RegisterMediaTime(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="b523f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b523f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b523f-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="b523f-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="b523f-108">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b523f-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b523f-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b523f-109">Return value</span></span>

<span data-ttu-id="b523f-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b523f-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b523f-111">Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="b523f-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="b523f-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b523f-112">Return code</span></span>                                                                                                  | <span data-ttu-id="b523f-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="b523f-113">Description</span></span>                                |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="b523f-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b523f-114"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="b523f-115">Correcto.</span><span class="sxs-lookup"><span data-stu-id="b523f-115">Success.</span></span><br/>                        |
| <dl> <span data-ttu-id="b523f-116"><dt>**\_tiempo medio de VFW E \_ \_ \_ no \_ establecido**</dt></span><span class="sxs-lookup"><span data-stu-id="b523f-116"><dt>**VFW\_E\_MEDIA\_TIME\_NOT\_SET**</dt></span></span> </dl> | <span data-ttu-id="b523f-117">El ejemplo no tiene una marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="b523f-117">The sample is not time-stamped.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b523f-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b523f-118">Remarks</span></span>

<span data-ttu-id="b523f-119">Este método almacena las marcas de tiempo del ejemplo actual.</span><span class="sxs-lookup"><span data-stu-id="b523f-119">This method stores the time stamps from the current sample.</span></span> <span data-ttu-id="b523f-120">El método [**CRendererPosPassThru:: GetMediaTime**](crendererpospassthru-getmediatime.md) recupera los mismos valores.</span><span class="sxs-lookup"><span data-stu-id="b523f-120">The [**CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) method retrieves the same values.</span></span>

<span data-ttu-id="b523f-121">El filtro debe llamar a este método para cada ejemplo que recibe.</span><span class="sxs-lookup"><span data-stu-id="b523f-121">The filter should call this method for each sample that it receives.</span></span> <span data-ttu-id="b523f-122">El método se sobrecarga para aceptar un puntero al ejemplo o los propios valores de la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="b523f-122">The method is overloaded to accept either a pointer to the sample, or the time stamp values themselves.</span></span>

## <a name="requirements"></a><span data-ttu-id="b523f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b523f-123">Requirements</span></span>



| <span data-ttu-id="b523f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b523f-124">Requirement</span></span> | <span data-ttu-id="b523f-125">Value</span><span class="sxs-lookup"><span data-stu-id="b523f-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b523f-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b523f-126">Header</span></span><br/>  | <dl> <span data-ttu-id="b523f-127"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b523f-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b523f-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b523f-128">Library</span></span><br/> | <dl> <span data-ttu-id="b523f-129"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b523f-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




