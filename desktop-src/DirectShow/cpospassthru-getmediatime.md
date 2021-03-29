---
description: El método GetMediaTime recupera las marcas de tiempo en el ejemplo actual.
ms.assetid: 36f3b6d3-b884-4168-94f3-f334a5056c7d
title: Método CPosPassThru. GetMediaTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b2748d986f121a38041155dcd43f13a647916486
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679136"
---
# <a name="cpospassthrugetmediatime-method"></a><span data-ttu-id="f386b-103">CPosPassThru. GetMediaTime, método</span><span class="sxs-lookup"><span data-stu-id="f386b-103">CPosPassThru.GetMediaTime method</span></span>

<span data-ttu-id="f386b-104">El `GetMediaTime` método recupera las marcas de tiempo en el ejemplo actual.</span><span class="sxs-lookup"><span data-stu-id="f386b-104">The `GetMediaTime` method retrieves the time stamps on the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="f386b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f386b-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="f386b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f386b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f386b-107">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="f386b-107">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="f386b-108">Puntero a una variable que recibe la hora de inicio, en unidades del formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="f386b-108">Pointer to a variable that receives the start time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="f386b-109">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="f386b-109">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="f386b-110">Puntero a una variable que recibe la hora de finalización, en unidades del formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="f386b-110">Pointer to a variable that receives the end time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f386b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f386b-111">Return value</span></span>

<span data-ttu-id="f386b-112">Devuelve E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="f386b-112">Returns E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f386b-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f386b-113">Remarks</span></span>

<span data-ttu-id="f386b-114">Invalide este método si el filtro almacena en caché las marcas de tiempo de los ejemplos que recibe.</span><span class="sxs-lookup"><span data-stu-id="f386b-114">Override this method if your filter caches the time stamps on the samples it receives.</span></span>

## <a name="requirements"></a><span data-ttu-id="f386b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f386b-115">Requirements</span></span>



| <span data-ttu-id="f386b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f386b-116">Requirement</span></span> | <span data-ttu-id="f386b-117">Value</span><span class="sxs-lookup"><span data-stu-id="f386b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f386b-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f386b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f386b-119"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f386b-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f386b-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f386b-120">Library</span></span><br/> | <dl> <span data-ttu-id="f386b-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f386b-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f386b-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="f386b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f386b-123">**Clase CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="f386b-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




