---
description: 'El método GetPositions recupera la posición actual y la posición de detención, en relación con la duración total de la secuencia. Este método implementa el método IMediaSeeking:: GetPositions.'
ms.assetid: 51e45bc3-ae30-4b05-b9d9-684c1b028f51
title: Método CPosPassThru. GetPositions (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0852199e8e143ce5b0348c3b79afd495a5a47627
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660816"
---
# <a name="cpospassthrugetpositions-method"></a><span data-ttu-id="cac16-104">CPosPassThru. GetPositions, método</span><span class="sxs-lookup"><span data-stu-id="cac16-104">CPosPassThru.GetPositions method</span></span>

<span data-ttu-id="cac16-105">El `GetPositions` método recupera la posición actual y la posición de detención, en relación con la duración total de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="cac16-105">The `GetPositions` method retrieves the current position and the stop position, relative to the total duration of the stream.</span></span> <span data-ttu-id="cac16-106">Este método implementa el método [**IMediaSeeking:: GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) .</span><span class="sxs-lookup"><span data-stu-id="cac16-106">This method implements the [**IMediaSeeking::GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cac16-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cac16-107">Syntax</span></span>


```C++
HRESULT GetPositions(
   LONGLONG *pCurrent,
   LONGLONG *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="cac16-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cac16-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cac16-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="cac16-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="cac16-110">Puntero a una variable que recibe la posición actual, en unidades del formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="cac16-110">Pointer to a variable that receives the current position, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="cac16-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="cac16-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="cac16-112">Puntero a una variable que recibe la posición de detención, en unidades del formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="cac16-112">Pointer to a variable that receives the stop position, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cac16-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cac16-113">Return value</span></span>

<span data-ttu-id="cac16-114">Devuelve el valor **HRESULT** del PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="cac16-114">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="cac16-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cac16-115">Requirements</span></span>



| <span data-ttu-id="cac16-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cac16-116">Requirement</span></span> | <span data-ttu-id="cac16-117">Value</span><span class="sxs-lookup"><span data-stu-id="cac16-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cac16-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cac16-118">Header</span></span><br/>  | <dl> <span data-ttu-id="cac16-119"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cac16-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cac16-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cac16-120">Library</span></span><br/> | <dl> <span data-ttu-id="cac16-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="cac16-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cac16-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="cac16-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cac16-123">**Clase CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="cac16-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




