---
description: 'El método GetCurrentPosition recupera la posición actual, en relación con la duración total de la secuencia. Este método implementa el método IMediaSeeking:: GetCurrentPosition.'
ms.assetid: 07020182-2199-4153-9bab-f30d112bc09f
title: Método CPosPassThru. GetCurrentPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetCurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5cdbd93edf7630499f6585fbbf6e34a70bed68c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680456"
---
# <a name="cpospassthrugetcurrentposition-method"></a><span data-ttu-id="6db2f-104">CPosPassThru. GetCurrentPosition, método</span><span class="sxs-lookup"><span data-stu-id="6db2f-104">CPosPassThru.GetCurrentPosition method</span></span>

<span data-ttu-id="6db2f-105">El `GetCurrentPosition` método recupera la posición actual, en relación con la duración total de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="6db2f-105">The `GetCurrentPosition` method retrieves the current position, relative to the total duration of the stream.</span></span> <span data-ttu-id="6db2f-106">Este método implementa el método [**IMediaSeeking:: GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) .</span><span class="sxs-lookup"><span data-stu-id="6db2f-106">This method implements the [**IMediaSeeking::GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6db2f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6db2f-107">Syntax</span></span>


```C++
HRESULT GetCurrentPosition(
   LONGLONG *pCurrent
);
```



## <a name="parameters"></a><span data-ttu-id="6db2f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6db2f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6db2f-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="6db2f-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="6db2f-110">Puntero a una variable que recibe la posición actual, en unidades del formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="6db2f-110">Pointer to a variable that receives the current position, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6db2f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6db2f-111">Return value</span></span>

<span data-ttu-id="6db2f-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6db2f-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6db2f-113">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="6db2f-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="6db2f-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6db2f-114">Return code</span></span>                                                                               | <span data-ttu-id="6db2f-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="6db2f-115">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="6db2f-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="6db2f-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="6db2f-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="6db2f-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="6db2f-118"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="6db2f-118"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="6db2f-119">No se admite el método.</span><span class="sxs-lookup"><span data-stu-id="6db2f-119">Method is not supported.</span></span><br/>   |
| <dl> <span data-ttu-id="6db2f-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="6db2f-120"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="6db2f-121">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="6db2f-121">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6db2f-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6db2f-122">Remarks</span></span>

<span data-ttu-id="6db2f-123">Este método llama al método [**CPosPassThru:: GetMediaTime**](cpospassthru-getmediatime.md) para recuperar la posición más reciente.</span><span class="sxs-lookup"><span data-stu-id="6db2f-123">This method calls the [**CPosPassThru::GetMediaTime**](cpospassthru-getmediatime.md) method to retrieve the most recent position.</span></span> <span data-ttu-id="6db2f-124">Si se produce un error en **GetMediaTime** , el método llama a **IMediaSeeking:: GetCurrentPosition** en el PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="6db2f-124">If **GetMediaTime** fails, the method calls **IMediaSeeking::GetCurrentPosition** on the connected pin.</span></span>

<span data-ttu-id="6db2f-125">De forma predeterminada, se produce un error en el método **GetMediaTime** en la clase base.</span><span class="sxs-lookup"><span data-stu-id="6db2f-125">The **GetMediaTime** method fails by default in the base class.</span></span> <span data-ttu-id="6db2f-126">Si el filtro almacena en caché la posición actual, invalide **GetMediaTime** para devolver el valor almacenado en caché.</span><span class="sxs-lookup"><span data-stu-id="6db2f-126">If your filter caches the current position, override **GetMediaTime** to return the cached value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6db2f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6db2f-127">Requirements</span></span>



| <span data-ttu-id="6db2f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6db2f-128">Requirement</span></span> | <span data-ttu-id="6db2f-129">Value</span><span class="sxs-lookup"><span data-stu-id="6db2f-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6db2f-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6db2f-130">Header</span></span><br/>  | <dl> <span data-ttu-id="6db2f-131"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6db2f-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6db2f-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6db2f-132">Library</span></span><br/> | <dl> <span data-ttu-id="6db2f-133"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="6db2f-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6db2f-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="6db2f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6db2f-135">**Clase CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="6db2f-135">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




