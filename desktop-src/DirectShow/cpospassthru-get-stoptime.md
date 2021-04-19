---
description: 'El \_ método get StopTime recupera la hora a la que se detendrá la reproducción, en relación con la duración de la secuencia. Este método implementa el método IMediaPosition:: get \_ StopTime.'
ms.assetid: 0ca3f047-ac43-419e-a1ed-b406f89f7af7
title: Método CPosPassThru.get_StopTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_StopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 227b054a9737c06e56f7311acc7e0093766608b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660508"
---
# <a name="cpospassthruget_stoptime-method"></a><span data-ttu-id="62613-104">CPosPassThru. Get \_ StopTime (método)</span><span class="sxs-lookup"><span data-stu-id="62613-104">CPosPassThru.get\_StopTime method</span></span>

<span data-ttu-id="62613-105">El `get_StopTime` método recupera la hora a la que se detendrá la reproducción, en relación con la duración de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="62613-105">The `get_StopTime` method retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span> <span data-ttu-id="62613-106">Este método implementa el método [**IMediaPosition:: get \_ StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_stoptime) .</span><span class="sxs-lookup"><span data-stu-id="62613-106">This method implements the [**IMediaPosition::get\_StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_stoptime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="62613-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62613-107">Syntax</span></span>


```C++
HRESULT get_StopTime(
   REFTIME *pllTime
);
```



## <a name="parameters"></a><span data-ttu-id="62613-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62613-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62613-109">*pllTime*</span><span class="sxs-lookup"><span data-stu-id="62613-109">*pllTime*</span></span> 
</dt> <dd>

<span data-ttu-id="62613-110">Puntero a una variable que recibe la hora de detención, en segundos.</span><span class="sxs-lookup"><span data-stu-id="62613-110">Pointer to a variable that receives the stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62613-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62613-111">Return value</span></span>

<span data-ttu-id="62613-112">Devuelve el valor **HRESULT** del PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="62613-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="62613-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62613-113">Requirements</span></span>



| <span data-ttu-id="62613-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="62613-114">Requirement</span></span> | <span data-ttu-id="62613-115">Value</span><span class="sxs-lookup"><span data-stu-id="62613-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62613-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62613-116">Header</span></span><br/>  | <dl> <span data-ttu-id="62613-117"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="62613-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="62613-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="62613-118">Library</span></span><br/> | <dl> <span data-ttu-id="62613-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="62613-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62613-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="62613-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62613-121">**Clase CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="62613-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




