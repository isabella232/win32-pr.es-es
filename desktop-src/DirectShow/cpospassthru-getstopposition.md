---
description: 'El método GetStopPosition recupera la hora a la que se detendrá la reproducción, en relación con la duración de la secuencia. Este método implementa el método IMediaSeeking:: GetStopPosition.'
ms.assetid: 11486371-da0a-4b83-956b-ef6b92721e74
title: Método CPosPassThru. GetStopPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetStopPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ee704a47074db032badfa1f02ffbf2db8c7efa4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681151"
---
# <a name="cpospassthrugetstopposition-method"></a><span data-ttu-id="91e13-104">CPosPassThru. GetStopPosition, método</span><span class="sxs-lookup"><span data-stu-id="91e13-104">CPosPassThru.GetStopPosition method</span></span>

<span data-ttu-id="91e13-105">El `GetStopPosition` método recupera la hora a la que se detendrá la reproducción, en relación con la duración de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="91e13-105">The `GetStopPosition` method retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span> <span data-ttu-id="91e13-106">Este método implementa el método [**IMediaSeeking:: GetStopPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) .</span><span class="sxs-lookup"><span data-stu-id="91e13-106">This method implements the [**IMediaSeeking::GetStopPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="91e13-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="91e13-107">Syntax</span></span>


```C++
HRESULT GetStopPosition(
   LONGLONG *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="91e13-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91e13-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91e13-109">*pStop*</span><span class="sxs-lookup"><span data-stu-id="91e13-109">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="91e13-110">Puntero a una variable que recibe la hora de detención, en unidades del formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="91e13-110">Pointer to a variable that receives the stop time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91e13-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="91e13-111">Return value</span></span>

<span data-ttu-id="91e13-112">Devuelve el valor **HRESULT** del PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="91e13-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="91e13-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91e13-113">Requirements</span></span>



| <span data-ttu-id="91e13-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="91e13-114">Requirement</span></span> | <span data-ttu-id="91e13-115">Value</span><span class="sxs-lookup"><span data-stu-id="91e13-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91e13-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91e13-116">Header</span></span><br/>  | <dl> <span data-ttu-id="91e13-117"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="91e13-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="91e13-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="91e13-118">Library</span></span><br/> | <dl> <span data-ttu-id="91e13-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="91e13-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91e13-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="91e13-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91e13-121">**Clase CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="91e13-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




