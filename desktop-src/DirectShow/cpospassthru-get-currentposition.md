---
description: 'El \_ método get CurrentPosition recupera la posición actual, en relación con la duración total de la secuencia. Este método implementa el método IMediaPosition:: get \_ CurrentPosition.'
ms.assetid: 6e68af98-440d-4ecc-b1aa-d5e241de4999
title: Método CPosPassThru.get_CurrentPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_CurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c146eb1ee3d0a48da90973ab181a4bd02182331
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660491"
---
# <a name="cpospassthruget_currentposition-method"></a><span data-ttu-id="af13b-104">CPosPassThru. Get \_ CurrentPosition (método)</span><span class="sxs-lookup"><span data-stu-id="af13b-104">CPosPassThru.get\_CurrentPosition method</span></span>

<span data-ttu-id="af13b-105">El `get_CurrentPosition` método recupera la posición actual, en relación con la duración total de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="af13b-105">The `get_CurrentPosition` method retrieves the current position, relative to the total duration of the stream.</span></span> <span data-ttu-id="af13b-106">Este método implementa el método [**IMediaPosition:: get \_ CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-get_currentposition) .</span><span class="sxs-lookup"><span data-stu-id="af13b-106">This method implements the [**IMediaPosition::get\_CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-get_currentposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="af13b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="af13b-107">Syntax</span></span>


```C++
HRESULT get_CurrentPosition(
   REFTIME *pllTime
);
```



## <a name="parameters"></a><span data-ttu-id="af13b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="af13b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af13b-109">*pllTime*</span><span class="sxs-lookup"><span data-stu-id="af13b-109">*pllTime*</span></span> 
</dt> <dd>

<span data-ttu-id="af13b-110">Puntero a una variable que recibe la posición actual, en segundos.</span><span class="sxs-lookup"><span data-stu-id="af13b-110">Pointer to a variable that receives the current position, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af13b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af13b-111">Return value</span></span>

<span data-ttu-id="af13b-112">Devuelve el valor **HRESULT** del PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="af13b-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="af13b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af13b-113">Requirements</span></span>



| <span data-ttu-id="af13b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="af13b-114">Requirement</span></span> | <span data-ttu-id="af13b-115">Value</span><span class="sxs-lookup"><span data-stu-id="af13b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af13b-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="af13b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="af13b-117"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="af13b-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="af13b-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="af13b-118">Library</span></span><br/> | <dl> <span data-ttu-id="af13b-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="af13b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af13b-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="af13b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af13b-121">**Clase CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="af13b-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




