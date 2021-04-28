---
description: 'Constructor CBasePin.CBasePin: método constructor.'
ms.assetid: e8cb5f1d-171f-4bf8-8ab6-6e547c4678d2
title: Constructor CBasePin.CBasePin (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CBasePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f11dea6bd5bc3f766e5f93a04022dab5ba6e51a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099433"
---
# <a name="cbasepincbasepin-constructor"></a><span data-ttu-id="3adec-103">Constructor CBasePin.CBasePin</span><span class="sxs-lookup"><span data-stu-id="3adec-103">CBasePin.CBasePin constructor</span></span>

<span data-ttu-id="3adec-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="3adec-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3adec-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3adec-105">Syntax</span></span>


```C++
CBasePin(
   TCHAR         *pObjectName,
   CBaseFilter   *pFilter,
   CCritSec      *pLock,
   HRESULT       *phr,
   LPCWSTR       pName,
   PIN_DIRECTION dir
);
```



## <a name="parameters"></a><span data-ttu-id="3adec-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3adec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3adec-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="3adec-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="3adec-108">Cadena que contiene el nombre de depuración del objeto.</span><span class="sxs-lookup"><span data-stu-id="3adec-108">String containing the debug name for the object.</span></span> <span data-ttu-id="3adec-109">Para obtener más información, vea [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="3adec-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="3adec-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="3adec-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="3adec-111">Puntero al filtro que creó este pin.</span><span class="sxs-lookup"><span data-stu-id="3adec-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="3adec-112">*Plock*</span><span class="sxs-lookup"><span data-stu-id="3adec-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="3adec-113">Puntero a un [**bloqueo CCritSec,**](ccritsec.md) que se usa para serializar los cambios de estado.</span><span class="sxs-lookup"><span data-stu-id="3adec-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="3adec-114">Puede ser la misma sección crítica que el bloqueo de filtro, [**CBaseFilter::m \_ pLock**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="3adec-114">Can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="3adec-115">*Phr*</span><span class="sxs-lookup"><span data-stu-id="3adec-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="3adec-116">Puntero a una variable que recibe un **valor HRESULT** que indica el éxito o error del método.</span><span class="sxs-lookup"><span data-stu-id="3adec-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="3adec-117">Inicialice el valor en S \_ OK antes de crear el objeto .</span><span class="sxs-lookup"><span data-stu-id="3adec-117">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="3adec-118">El valor solo se cambia si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="3adec-118">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="3adec-119">*pName*</span><span class="sxs-lookup"><span data-stu-id="3adec-119">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="3adec-120">Cadena de caracteres anchos que contiene el nombre del pin.</span><span class="sxs-lookup"><span data-stu-id="3adec-120">Wide-character string containing the name of the pin.</span></span> <span data-ttu-id="3adec-121">Para obtener más información, [**vea CBasePin::QueryPinInfo**](cbasepin-querypininfo.md).</span><span class="sxs-lookup"><span data-stu-id="3adec-121">For more information, see [**CBasePin::QueryPinInfo**](cbasepin-querypininfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="3adec-122">*dir*</span><span class="sxs-lookup"><span data-stu-id="3adec-122">*dir*</span></span> 
</dt> <dd>

<span data-ttu-id="3adec-123">Miembro de la [**enumeración \_ PIN DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) que especifica la dirección del pin.</span><span class="sxs-lookup"><span data-stu-id="3adec-123">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumeration specifying the direction of the pin.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3adec-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3adec-124">Remarks</span></span>

<span data-ttu-id="3adec-125">La sección crítica especificada por *pLock* serializa el estado del pin, incluido su estado de conexión, la elección del asignador, el tipo de medio y el estado de las operaciones de vaciado.</span><span class="sxs-lookup"><span data-stu-id="3adec-125">The critical section specified by *pLock* serializes the pin's state, including its connection status, choice of allocator, media type, and the status of flush operations.</span></span> <span data-ttu-id="3adec-126">No use esta sección crítica para serializar las operaciones de streaming.</span><span class="sxs-lookup"><span data-stu-id="3adec-126">Do not use this critical section to serialize streaming operations.</span></span> <span data-ttu-id="3adec-127">Para obtener más información, [vea Data Flow en el gráfico de filtros](data-flow-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="3adec-127">For more information, see [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md).</span></span>

<span data-ttu-id="3adec-128">Un filtro podría crear pines en su método de constructor, por lo que en este momento el *puntero pFilter* podría no hacer referencia a un objeto válido.</span><span class="sxs-lookup"><span data-stu-id="3adec-128">A filter might create pins in its constructor method, so at this point the *pFilter* pointer might not refer to a valid object.</span></span> <span data-ttu-id="3adec-129">Almacene el puntero, pero no lo desreferencia mientras esté dentro del constructor del pin.</span><span class="sxs-lookup"><span data-stu-id="3adec-129">Store the pointer, but do not dereference it while inside the pin's constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="3adec-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3adec-130">Requirements</span></span>



| <span data-ttu-id="3adec-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="3adec-131">Requirement</span></span> | <span data-ttu-id="3adec-132">Value</span><span class="sxs-lookup"><span data-stu-id="3adec-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3adec-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3adec-133">Header</span></span><br/>  | <dl> <span data-ttu-id="3adec-134"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="3adec-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3adec-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3adec-135">Library</span></span><br/> | <dl> <span data-ttu-id="3adec-136"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3adec-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3adec-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3adec-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3adec-138">**CBasePin (clase)**</span><span class="sxs-lookup"><span data-stu-id="3adec-138">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




