---
description: La clase CRefTime es una clase auxiliar para administrar los tiempos de referencia.
ms.assetid: 4be0fc23-77fb-4c45-a899-c1dfc6ee89b9
title: Clase CRefTime (Reftime. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 01e83520943abafd814425b6ff3fb53f48775627
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660563"
---
# <a name="creftime-class"></a><span data-ttu-id="e76b3-103">Clase CRefTime</span><span class="sxs-lookup"><span data-stu-id="e76b3-103">CRefTime class</span></span>

![jerarquía de clases creftime](images/cutil05.png)

<span data-ttu-id="e76b3-105">La `CRefTime` clase es una clase auxiliar para administrar los tiempos de referencia.</span><span class="sxs-lookup"><span data-stu-id="e76b3-105">The `CRefTime` class is a helper class for managing reference times.</span></span>

<span data-ttu-id="e76b3-106">Una *hora de referencia* es una unidad de tiempo representada en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="e76b3-106">A *reference time* is a unit of time represented in 100-nanosecond units.</span></span> <span data-ttu-id="e76b3-107">Esta clase comparte el mismo diseño de datos que el tipo de datos de [**\_ hora de referencia**](reference-time.md) , pero agrega algunos métodos y operadores que proporcionan funciones aritméticas, de conversión y de comparación.</span><span class="sxs-lookup"><span data-stu-id="e76b3-107">This class shares the same data layout as the [**REFERENCE\_TIME**](reference-time.md) data type, but adds some methods and operators that provide comparison, conversion, and arithmetic functions.</span></span> <span data-ttu-id="e76b3-108">Para obtener más información acerca de los tiempos de referencia, consulte [hora y relojes en DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="e76b3-108">For more information about reference times, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>



| <span data-ttu-id="e76b3-109">Variables de miembro público</span><span class="sxs-lookup"><span data-stu-id="e76b3-109">Public Member Variables</span></span>                                                 | <span data-ttu-id="e76b3-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e76b3-110">Description</span></span>                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="e76b3-111">**m \_ hora**</span><span class="sxs-lookup"><span data-stu-id="e76b3-111">**m\_time**</span></span>](creftime-m-time.md)                                      | <span data-ttu-id="e76b3-112">Especifica el valor de la **\_ hora de referencia** .</span><span class="sxs-lookup"><span data-stu-id="e76b3-112">Specifies the **REFERENCE\_TIME** value.</span></span>              |
| <span data-ttu-id="e76b3-113">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="e76b3-113">Public Methods</span></span>                                                          | <span data-ttu-id="e76b3-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="e76b3-114">Description</span></span>                                           |
| [<span data-ttu-id="e76b3-115">**CRefTime**</span><span class="sxs-lookup"><span data-stu-id="e76b3-115">**CRefTime**</span></span>](creftime-creftime.md)                                   | <span data-ttu-id="e76b3-116">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="e76b3-116">Constructor method.</span></span>                                   |
| [<span data-ttu-id="e76b3-117">**GetUnits**</span><span class="sxs-lookup"><span data-stu-id="e76b3-117">**GetUnits**</span></span>](creftime-getunits.md)                                   | <span data-ttu-id="e76b3-118">Recupera el tiempo de referencia en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="e76b3-118">Retrieves the reference time in 100-nanosecond units.</span></span> |
| [<span data-ttu-id="e76b3-119">**Milisegundos**</span><span class="sxs-lookup"><span data-stu-id="e76b3-119">**Millisecs**</span></span>](creftime-millisecs.md)                                 | <span data-ttu-id="e76b3-120">Convierte el tiempo de referencia en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="e76b3-120">Converts the reference time to milliseconds.</span></span>          |
| <span data-ttu-id="e76b3-121">Operadores</span><span class="sxs-lookup"><span data-stu-id="e76b3-121">Operators</span></span>                                                               | <span data-ttu-id="e76b3-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="e76b3-122">Description</span></span>                                           |
| [<span data-ttu-id="e76b3-123">**tiempo de referencia \_ del operador ()**</span><span class="sxs-lookup"><span data-stu-id="e76b3-123">**operator REFERENCE\_TIME()**</span></span>](creftime-operator-reference-time-.md) | <span data-ttu-id="e76b3-124">Convierte el objeto en un tipo de datos de **\_ hora de referencia** .</span><span class="sxs-lookup"><span data-stu-id="e76b3-124">Casts the object to a **REFERENCE\_TIME** data type.</span></span>  |
| [<span data-ttu-id="e76b3-125">**operador =**</span><span class="sxs-lookup"><span data-stu-id="e76b3-125">**operator=**</span></span>](creftime-operator-assign.md)                           | <span data-ttu-id="e76b3-126">Asigna una nueva hora de referencia.</span><span class="sxs-lookup"><span data-stu-id="e76b3-126">Assigns a new reference time.</span></span>                         |
| [<span data-ttu-id="e76b3-127">**operador + =**</span><span class="sxs-lookup"><span data-stu-id="e76b3-127">**operator+=**</span></span>](creftime-operator-plus-assign.md)                     | <span data-ttu-id="e76b3-128">Agrega dos tiempos de referencia.</span><span class="sxs-lookup"><span data-stu-id="e76b3-128">Adds two reference times.</span></span>                             |
| [<span data-ttu-id="e76b3-129">**operador =**</span><span class="sxs-lookup"><span data-stu-id="e76b3-129">**operator =**</span></span>](creftime-operator-minus-assign.md)                    | <span data-ttu-id="e76b3-130">Resta una hora de referencia de otra.</span><span class="sxs-lookup"><span data-stu-id="e76b3-130">Subtracts one reference time from another.</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="e76b3-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e76b3-131">Remarks</span></span>

<span data-ttu-id="e76b3-132">Existe un riesgo potencial con el uso de esta clase.</span><span class="sxs-lookup"><span data-stu-id="e76b3-132">There is a potential pitfall with using this class.</span></span> <span data-ttu-id="e76b3-133">Si aplica el operador + = con un objeto **CRefTime** como operando izquierdo y una variable de tipo **Long** como operando derecho, el compilador convertirá implícitamente el operando derecho en un objeto **CRefTime** .</span><span class="sxs-lookup"><span data-stu-id="e76b3-133">If you apply the += operator with a **CRefTime** object as the left operand and a variable of type **LONG** as the right operand, the compiler will implicitly coerce the right operand into a **CRefTime** object.</span></span> <span data-ttu-id="e76b3-134">Esta coerción usa el constructor **CRefTime** que convierte los milisegundos en unidades de \_ tiempo de referencia; como resultado, el operando derecho se multiplica por 10.000:</span><span class="sxs-lookup"><span data-stu-id="e76b3-134">This coercion uses the **CRefTime** constructor that converts milliseconds into REFERENCE\_TIME units; as a result, the right operand is multiplied by 10,000:</span></span>


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt += val;    // Coerce val to CRefTime, rt.m_time is now 200,000.
```



<span data-ttu-id="e76b3-135">Sin embargo, no ocurre lo mismo con el operador +:</span><span class="sxs-lookup"><span data-stu-id="e76b3-135">However, the same thing does not happen using the + operator:</span></span>


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt = rt + val; // CRefTime, rt.m_time is 20.
```



## <a name="requirements"></a><span data-ttu-id="e76b3-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e76b3-136">Requirements</span></span>



| <span data-ttu-id="e76b3-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="e76b3-137">Requirement</span></span> | <span data-ttu-id="e76b3-138">Value</span><span class="sxs-lookup"><span data-stu-id="e76b3-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e76b3-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e76b3-139">Header</span></span><br/>  | <dl> <span data-ttu-id="e76b3-140"><dt>Reftime. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e76b3-140"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e76b3-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e76b3-141">Library</span></span><br/> | <dl> <span data-ttu-id="e76b3-142"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e76b3-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




