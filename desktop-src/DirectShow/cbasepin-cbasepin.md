---
description: Método de constructor.
ms.assetid: e8cb5f1d-171f-4bf8-8ab6-6e547c4678d2
title: Constructor CBasePin. CBasePin (Amfilter. h)
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
ms.openlocfilehash: dd4883d3d8e906e1da2f377344b735037c5e5cd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671636"
---
# <a name="cbasepincbasepin-constructor"></a><span data-ttu-id="c86c3-103">Constructor CBasePin. CBasePin</span><span class="sxs-lookup"><span data-stu-id="c86c3-103">CBasePin.CBasePin constructor</span></span>

<span data-ttu-id="c86c3-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="c86c3-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c86c3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c86c3-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="c86c3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c86c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c86c3-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="c86c3-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="c86c3-108">Cadena que contiene el nombre de depuración para el objeto.</span><span class="sxs-lookup"><span data-stu-id="c86c3-108">String containing the debug name for the object.</span></span> <span data-ttu-id="c86c3-109">Para obtener más información, vea [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="c86c3-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="c86c3-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="c86c3-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="c86c3-111">Puntero al filtro que creó este pin.</span><span class="sxs-lookup"><span data-stu-id="c86c3-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="c86c3-112">*pLock*</span><span class="sxs-lookup"><span data-stu-id="c86c3-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="c86c3-113">Puntero a un bloqueo de [**CCritSec**](ccritsec.md) , que se usa para serializar los cambios de estado.</span><span class="sxs-lookup"><span data-stu-id="c86c3-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="c86c3-114">Puede ser la misma sección crítica que el bloqueo de filtro, [**CBaseFilter:: m \_ Plock**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="c86c3-114">Can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="c86c3-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="c86c3-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="c86c3-116">Puntero a una variable que recibe un valor **HRESULT** que indica si el método se ha ejecutado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="c86c3-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="c86c3-117">Inicialice el valor a S \_ OK antes de crear el objeto.</span><span class="sxs-lookup"><span data-stu-id="c86c3-117">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="c86c3-118">Solo se cambia el valor si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="c86c3-118">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="c86c3-119">*pName*</span><span class="sxs-lookup"><span data-stu-id="c86c3-119">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="c86c3-120">Cadena de caracteres anchos que contiene el nombre del PIN.</span><span class="sxs-lookup"><span data-stu-id="c86c3-120">Wide-character string containing the name of the pin.</span></span> <span data-ttu-id="c86c3-121">Para obtener más información, vea [**CBasePin:: QueryPinInfo**](cbasepin-querypininfo.md).</span><span class="sxs-lookup"><span data-stu-id="c86c3-121">For more information, see [**CBasePin::QueryPinInfo**](cbasepin-querypininfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="c86c3-122">*dir*</span><span class="sxs-lookup"><span data-stu-id="c86c3-122">*dir*</span></span> 
</dt> <dd>

<span data-ttu-id="c86c3-123">Miembro de la enumeración de [**\_ dirección del PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) que especifica la dirección del PIN.</span><span class="sxs-lookup"><span data-stu-id="c86c3-123">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumeration specifying the direction of the pin.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c86c3-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c86c3-124">Remarks</span></span>

<span data-ttu-id="c86c3-125">La sección crítica especificada por *Plock* serializa el estado del PIN, incluido el estado de la conexión, la elección del asignador, el tipo de medio y el estado de las operaciones de vaciado.</span><span class="sxs-lookup"><span data-stu-id="c86c3-125">The critical section specified by *pLock* serializes the pin's state, including its connection status, choice of allocator, media type, and the status of flush operations.</span></span> <span data-ttu-id="c86c3-126">No utilice esta sección crítica para serializar las operaciones de streaming.</span><span class="sxs-lookup"><span data-stu-id="c86c3-126">Do not use this critical section to serialize streaming operations.</span></span> <span data-ttu-id="c86c3-127">Para obtener más información, vea [flujo de datos en el gráfico de filtros](data-flow-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="c86c3-127">For more information, see [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md).</span></span>

<span data-ttu-id="c86c3-128">Un filtro podría crear PIN en su método de constructor, por lo que en este punto el puntero *pFilter* podría no hacer referencia a un objeto válido.</span><span class="sxs-lookup"><span data-stu-id="c86c3-128">A filter might create pins in its constructor method, so at this point the *pFilter* pointer might not refer to a valid object.</span></span> <span data-ttu-id="c86c3-129">Almacene el puntero, pero no desreferenciarlo mientras esté dentro del constructor del PIN.</span><span class="sxs-lookup"><span data-stu-id="c86c3-129">Store the pointer, but do not dereference it while inside the pin's constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="c86c3-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c86c3-130">Requirements</span></span>



| <span data-ttu-id="c86c3-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c86c3-131">Requirement</span></span> | <span data-ttu-id="c86c3-132">Value</span><span class="sxs-lookup"><span data-stu-id="c86c3-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c86c3-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c86c3-133">Header</span></span><br/>  | <dl> <span data-ttu-id="c86c3-134"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c86c3-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c86c3-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c86c3-135">Library</span></span><br/> | <dl> <span data-ttu-id="c86c3-136"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c86c3-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c86c3-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="c86c3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c86c3-138">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="c86c3-138">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




