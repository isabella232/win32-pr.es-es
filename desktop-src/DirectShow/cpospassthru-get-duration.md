---
description: 'El \_ método get Duration recupera la duración de la secuencia. Este método implementa el método IMediaPosition:: get \_ Duration.'
ms.assetid: 326a8cd3-d05f-49d0-941d-08f9778e9a06
title: Método CPosPassThru.get_Duration (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_Duration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df518a0691a4fe1a6c0443ba93a83e65577efe21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681029"
---
# <a name="cpospassthruget_duration-method"></a><span data-ttu-id="e1b0e-104">CPosPassThru. Get \_ Duration (método)</span><span class="sxs-lookup"><span data-stu-id="e1b0e-104">CPosPassThru.get\_Duration method</span></span>

<span data-ttu-id="e1b0e-105">El `get_Duration` método recupera la duración de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="e1b0e-105">The `get_Duration` method retrieves the duration of the stream.</span></span> <span data-ttu-id="e1b0e-106">Este método implementa el método [**IMediaPosition:: get \_ Duration**](/windows/desktop/api/Control/nf-control-imediaposition-get_duration) .</span><span class="sxs-lookup"><span data-stu-id="e1b0e-106">This method implements the [**IMediaPosition::get\_Duration**](/windows/desktop/api/Control/nf-control-imediaposition-get_duration) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1b0e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e1b0e-107">Syntax</span></span>


```C++
HRESULT get_Duration(
   REFTIME *plength
);
```



## <a name="parameters"></a><span data-ttu-id="e1b0e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e1b0e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1b0e-109">*plength*</span><span class="sxs-lookup"><span data-stu-id="e1b0e-109">*plength*</span></span> 
</dt> <dd>

<span data-ttu-id="e1b0e-110">Puntero a una variable que recibe la longitud total de la secuencia, en segundos.</span><span class="sxs-lookup"><span data-stu-id="e1b0e-110">Pointer to a variable that receives the total stream length, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1b0e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1b0e-111">Return value</span></span>

<span data-ttu-id="e1b0e-112">Devuelve el valor **HRESULT** del PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="e1b0e-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1b0e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1b0e-113">Requirements</span></span>



| <span data-ttu-id="e1b0e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1b0e-114">Requirement</span></span> | <span data-ttu-id="e1b0e-115">Value</span><span class="sxs-lookup"><span data-stu-id="e1b0e-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1b0e-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e1b0e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e1b0e-117"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e1b0e-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e1b0e-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e1b0e-118">Library</span></span><br/> | <dl> <span data-ttu-id="e1b0e-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e1b0e-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1b0e-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1b0e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1b0e-121">**Clase CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="e1b0e-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




