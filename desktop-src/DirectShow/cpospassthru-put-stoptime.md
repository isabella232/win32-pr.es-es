---
description: El \_ método put StopTime establece la hora a la que se detendrá la reproducción, en relación con la duración de la secuencia. Este método implementa el método IMediaPosition::p UT \_ StopTime.
ms.assetid: 0a344cad-df93-47f1-8c7f-5d5ef775b850
title: Método CPosPassThru.put_StopTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_StopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f5763700947596a0fb437ba3840df058d4d3239
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661291"
---
# <a name="cpospassthruput_stoptime-method"></a><span data-ttu-id="28e94-104">CPosPassThru. put \_ StopTime (método)</span><span class="sxs-lookup"><span data-stu-id="28e94-104">CPosPassThru.put\_StopTime method</span></span>

<span data-ttu-id="28e94-105">El `put_StopTime` método establece la hora a la que se detendrá la reproducción, en relación con la duración de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="28e94-105">The `put_StopTime` method sets the time at which the playback will stop, relative to the duration of the stream.</span></span> <span data-ttu-id="28e94-106">Este método implementa el método [**IMediaPosition::p UT \_ StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_stoptime) .</span><span class="sxs-lookup"><span data-stu-id="28e94-106">This method implements the [**IMediaPosition::put\_StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_stoptime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="28e94-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28e94-107">Syntax</span></span>


```C++
HRESULT put_StopTime(
   REFTIME llTime
);
```



## <a name="parameters"></a><span data-ttu-id="28e94-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28e94-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28e94-109">*llTime*</span><span class="sxs-lookup"><span data-stu-id="28e94-109">*llTime*</span></span> 
</dt> <dd>

<span data-ttu-id="28e94-110">Detiene la hora como un valor **doble** , en segundos.</span><span class="sxs-lookup"><span data-stu-id="28e94-110">Stop time as a **double** value, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28e94-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28e94-111">Return value</span></span>

<span data-ttu-id="28e94-112">Devuelve el valor **HRESULT** del PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="28e94-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="28e94-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28e94-113">Requirements</span></span>



| <span data-ttu-id="28e94-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="28e94-114">Requirement</span></span> | <span data-ttu-id="28e94-115">Value</span><span class="sxs-lookup"><span data-stu-id="28e94-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28e94-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28e94-116">Header</span></span><br/>  | <dl> <span data-ttu-id="28e94-117"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="28e94-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="28e94-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="28e94-118">Library</span></span><br/> | <dl> <span data-ttu-id="28e94-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="28e94-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28e94-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="28e94-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28e94-121">**Clase CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="28e94-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




