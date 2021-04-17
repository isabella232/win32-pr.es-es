---
description: 'El \_ método get PrerollTime recupera la cantidad de datos que se pondrán en cola antes de la posición de inicio. Este método implementa el método IMediaPosition:: get \_ PrerollTime.'
ms.assetid: 37c12798-eb0d-4859-8b2e-52d6ae147863
title: Método CPosPassThru.get_PrerollTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_PrerollTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55cb2cc37a18c9ea00b4eb7115590f472b8d467e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660551"
---
# <a name="cpospassthruget_prerolltime-method"></a><span data-ttu-id="96ce5-104">CPosPassThru. Get \_ PrerollTime (método)</span><span class="sxs-lookup"><span data-stu-id="96ce5-104">CPosPassThru.get\_PrerollTime method</span></span>

<span data-ttu-id="96ce5-105">El `get_PrerollTime` método recupera la cantidad de datos que se pondrán en cola antes de la posición de inicio.</span><span class="sxs-lookup"><span data-stu-id="96ce5-105">The `get_PrerollTime` method retrieves the amount of data that will be queued before the start position.</span></span> <span data-ttu-id="96ce5-106">Este método implementa el método [**IMediaPosition:: get \_ PrerollTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_prerolltime) .</span><span class="sxs-lookup"><span data-stu-id="96ce5-106">This method implements the [**IMediaPosition::get\_PrerollTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_prerolltime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="96ce5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96ce5-107">Syntax</span></span>


```C++
HRESULT get_PrerollTime(
   REFTIME *pllTime
);
```



## <a name="parameters"></a><span data-ttu-id="96ce5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="96ce5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96ce5-109">*pllTime*</span><span class="sxs-lookup"><span data-stu-id="96ce5-109">*pllTime*</span></span> 
</dt> <dd>

<span data-ttu-id="96ce5-110">Puntero a una variable que recibe el tiempo de prelanzamiento, en segundos.</span><span class="sxs-lookup"><span data-stu-id="96ce5-110">Pointer to a variable that receives the preroll time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96ce5-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="96ce5-111">Return value</span></span>

<span data-ttu-id="96ce5-112">Devuelve el valor **HRESULT** del PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="96ce5-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="96ce5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96ce5-113">Requirements</span></span>



| <span data-ttu-id="96ce5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="96ce5-114">Requirement</span></span> | <span data-ttu-id="96ce5-115">Value</span><span class="sxs-lookup"><span data-stu-id="96ce5-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96ce5-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="96ce5-116">Header</span></span><br/>  | <dl> <span data-ttu-id="96ce5-117"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="96ce5-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="96ce5-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="96ce5-118">Library</span></span><br/> | <dl> <span data-ttu-id="96ce5-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="96ce5-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96ce5-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="96ce5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96ce5-121">**Clase CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="96ce5-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




