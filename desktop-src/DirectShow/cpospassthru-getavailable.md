---
description: 'El método GetAvailable recupera el intervalo de veces que la búsqueda es eficaz. Este método implementa el método IMediaSeeking:: GetAvailable.'
ms.assetid: 5f4af41a-eb7b-4caa-97e0-aaed78467723
title: Método CPosPassThru. GetAvailable (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32dbba173caf933185602523dadcf71ce7ca3ef7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679503"
---
# <a name="cpospassthrugetavailable-method"></a><span data-ttu-id="f70a5-104">CPosPassThru. GetAvailable, método</span><span class="sxs-lookup"><span data-stu-id="f70a5-104">CPosPassThru.GetAvailable method</span></span>

<span data-ttu-id="f70a5-105">El `GetAvailable` método recupera el intervalo de veces que la búsqueda es eficaz.</span><span class="sxs-lookup"><span data-stu-id="f70a5-105">The `GetAvailable` method retrieves the range of times in which seeking is efficient.</span></span> <span data-ttu-id="f70a5-106">Este método implementa el método [**IMediaSeeking:: GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) .</span><span class="sxs-lookup"><span data-stu-id="f70a5-106">This method implements the [**IMediaSeeking::GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f70a5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f70a5-107">Syntax</span></span>


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a><span data-ttu-id="f70a5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f70a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f70a5-109">*pEarliest*</span><span class="sxs-lookup"><span data-stu-id="f70a5-109">*pEarliest*</span></span> 
</dt> <dd>

<span data-ttu-id="f70a5-110">Puntero a una variable que recibe la hora más temprana para una búsqueda eficaz.</span><span class="sxs-lookup"><span data-stu-id="f70a5-110">Pointer to a variable that receives the earliest time for efficient seeking.</span></span>

</dd> <dt>

<span data-ttu-id="f70a5-111">*Planchas*</span><span class="sxs-lookup"><span data-stu-id="f70a5-111">*pLatest*</span></span> 
</dt> <dd>

<span data-ttu-id="f70a5-112">Puntero a una variable que recibe la hora más reciente para una búsqueda eficaz.</span><span class="sxs-lookup"><span data-stu-id="f70a5-112">Pointer to a variable that receives the latest time for efficient seeking.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f70a5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f70a5-113">Return value</span></span>

<span data-ttu-id="f70a5-114">Devuelve el valor **HRESULT** del PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="f70a5-114">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="f70a5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f70a5-115">Requirements</span></span>



| <span data-ttu-id="f70a5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f70a5-116">Requirement</span></span> | <span data-ttu-id="f70a5-117">Value</span><span class="sxs-lookup"><span data-stu-id="f70a5-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f70a5-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f70a5-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f70a5-119"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f70a5-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f70a5-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f70a5-120">Library</span></span><br/> | <dl> <span data-ttu-id="f70a5-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f70a5-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f70a5-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="f70a5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f70a5-123">**Clase CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="f70a5-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




