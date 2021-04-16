---
description: El método WaitEvent espera hasta que se señale el evento especificado.
ms.assetid: 64880f46-7b8f-4823-9d50-052e30ecf04b
title: Método CDynamicOutputPin. WaitEvent (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.WaitEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b27f3c387c82eaeebc119f967deaca8e7314ccd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671266"
---
# <a name="cdynamicoutputpinwaitevent-method"></a><span data-ttu-id="dffe9-103">CDynamicOutputPin. WaitEvent, método</span><span class="sxs-lookup"><span data-stu-id="dffe9-103">CDynamicOutputPin.WaitEvent method</span></span>

<span data-ttu-id="dffe9-104">El `WaitEvent` método espera hasta que se señale el evento especificado.</span><span class="sxs-lookup"><span data-stu-id="dffe9-104">The `WaitEvent` method waits until the specified event is signaled.</span></span>

## <a name="syntax"></a><span data-ttu-id="dffe9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dffe9-105">Syntax</span></span>


```C++
static HRESULT WaitEvent(
   HANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="dffe9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dffe9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dffe9-107">*hEvent*</span><span class="sxs-lookup"><span data-stu-id="dffe9-107">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="dffe9-108">Identificador para un evento.</span><span class="sxs-lookup"><span data-stu-id="dffe9-108">Handle to an event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dffe9-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dffe9-109">Return value</span></span>

<span data-ttu-id="dffe9-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dffe9-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="dffe9-111">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="dffe9-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="dffe9-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="dffe9-112">Return code</span></span>                                                                                  | <span data-ttu-id="dffe9-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="dffe9-113">Description</span></span>                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="dffe9-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="dffe9-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="dffe9-115">Correcto.</span><span class="sxs-lookup"><span data-stu-id="dffe9-115">Success.</span></span><br/>          |
| <dl> <span data-ttu-id="dffe9-116"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="dffe9-116"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="dffe9-117">error inesperado.</span><span class="sxs-lookup"><span data-stu-id="dffe9-117">Unexpected error.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dffe9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dffe9-118">Requirements</span></span>



| <span data-ttu-id="dffe9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="dffe9-119">Requirement</span></span> | <span data-ttu-id="dffe9-120">Value</span><span class="sxs-lookup"><span data-stu-id="dffe9-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dffe9-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dffe9-121">Header</span></span><br/>  | <dl> <span data-ttu-id="dffe9-122"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dffe9-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="dffe9-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dffe9-123">Library</span></span><br/> | <dl> <span data-ttu-id="dffe9-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="dffe9-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dffe9-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="dffe9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dffe9-126">**Clase CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="dffe9-126">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




