---
description: 'Método CPosPassThru.GetMediaTime: el método GetMediaTime recupera las marcas de tiempo en el ejemplo actual.'
ms.assetid: 36f3b6d3-b884-4168-94f3-f334a5056c7d
title: Método CPosPassThru.GetMediaTime (Ctlutil.h)
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
ms.openlocfilehash: 328a0ae09c80a687863cfedb994f5a80cebebf14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095263"
---
# <a name="cpospassthrugetmediatime-method"></a><span data-ttu-id="7be54-103">Método CPosPassThru.GetMediaTime</span><span class="sxs-lookup"><span data-stu-id="7be54-103">CPosPassThru.GetMediaTime method</span></span>

<span data-ttu-id="7be54-104">El `GetMediaTime` método recupera las marcas de tiempo en el ejemplo actual.</span><span class="sxs-lookup"><span data-stu-id="7be54-104">The `GetMediaTime` method retrieves the time stamps on the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="7be54-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7be54-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="7be54-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7be54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7be54-107">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="7be54-107">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="7be54-108">Puntero a una variable que recibe la hora de inicio, en unidades del formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="7be54-108">Pointer to a variable that receives the start time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="7be54-109">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="7be54-109">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="7be54-110">Puntero a una variable que recibe la hora de finalización, en unidades del formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="7be54-110">Pointer to a variable that receives the end time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7be54-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7be54-111">Return value</span></span>

<span data-ttu-id="7be54-112">Devuelve E \_ FAIL.</span><span class="sxs-lookup"><span data-stu-id="7be54-112">Returns E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="7be54-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7be54-113">Remarks</span></span>

<span data-ttu-id="7be54-114">Invalide este método si el filtro almacena en caché las marcas de tiempo en los ejemplos que recibe.</span><span class="sxs-lookup"><span data-stu-id="7be54-114">Override this method if your filter caches the time stamps on the samples it receives.</span></span>

## <a name="requirements"></a><span data-ttu-id="7be54-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7be54-115">Requirements</span></span>



| <span data-ttu-id="7be54-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7be54-116">Requirement</span></span> | <span data-ttu-id="7be54-117">Value</span><span class="sxs-lookup"><span data-stu-id="7be54-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7be54-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7be54-118">Header</span></span><br/>  | <dl> <span data-ttu-id="7be54-119"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="7be54-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7be54-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7be54-120">Library</span></span><br/> | <dl> <span data-ttu-id="7be54-121"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="7be54-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7be54-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7be54-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7be54-123">**CPosPassThru (clase)**</span><span class="sxs-lookup"><span data-stu-id="7be54-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




