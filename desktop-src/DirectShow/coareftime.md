---
description: La clase COARefTime convierte los tiempos de referencia entre los segundos y las unidades 100-nanosegundos.
ms.assetid: 724420fc-9252-468f-9516-174be0a82999
title: Clase COARefTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 851495d69a1e34bd1723c20f88dc4bb86b7a8025
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678956"
---
# <a name="coareftime-class"></a><span data-ttu-id="93f12-103">Clase COARefTime</span><span class="sxs-lookup"><span data-stu-id="93f12-103">COARefTime class</span></span>

![jerarquía de clases coareftime](images/cutil05.png)

<span data-ttu-id="93f12-105">La `COARefTime` clase convierte los tiempos de referencia entre los segundos y las unidades 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="93f12-105">The `COARefTime` class converts reference times between seconds and 100-nanosecond units.</span></span>

<span data-ttu-id="93f12-106">Esta clase convierte entre los tiempos de referencia que son compatibles con la automatización y los tiempos de referencia que son compatibles con C/C++.</span><span class="sxs-lookup"><span data-stu-id="93f12-106">This class converts between reference times that are compatible with Automation and reference times that are compatible with C/C++.</span></span> <span data-ttu-id="93f12-107">Las interfaces compatibles con Automation usan valores **Double** para representar el tiempo en segundos.</span><span class="sxs-lookup"><span data-stu-id="93f12-107">Automation-compatible interfaces use **double** values to represent time in seconds.</span></span> <span data-ttu-id="93f12-108">Otras interfaces usan valores **LONGLONG** de 64 bits para representar el tiempo en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="93f12-108">Other interfaces use 64-bit **LONGLONG** values to represent time in 100-nanosecond units.</span></span> <span data-ttu-id="93f12-109">Para estos valores se definen los siguientes tipos:</span><span class="sxs-lookup"><span data-stu-id="93f12-109">The following types are defined for these values:</span></span>

``` syntax
typedef LONGLONG  REFERENCE_TIME;
typedef double    REFTIME;
```

<span data-ttu-id="93f12-110">Los filtros pueden utilizar la `COARefTime` clase para realizar la conversión entre los dos formatos.</span><span class="sxs-lookup"><span data-stu-id="93f12-110">Filters can use the `COARefTime` class to convert between the two formats.</span></span> <span data-ttu-id="93f12-111">Esta clase se deriva de la clase [**CRefTime**](creftime.md) .</span><span class="sxs-lookup"><span data-stu-id="93f12-111">This class is derived from the [**CRefTime**](creftime.md) class.</span></span>



| <span data-ttu-id="93f12-112">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="93f12-112">Public Methods</span></span>                                          | <span data-ttu-id="93f12-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="93f12-113">Description</span></span>                                                           |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="93f12-114">**COARefTime**</span><span class="sxs-lookup"><span data-stu-id="93f12-114">**COARefTime**</span></span>](coareftime-coareftime.md)             | <span data-ttu-id="93f12-115">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="93f12-115">Constructor method.</span></span>                                                   |
| <span data-ttu-id="93f12-116">Operadores</span><span class="sxs-lookup"><span data-stu-id="93f12-116">Operators</span></span>                                               | <span data-ttu-id="93f12-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="93f12-117">Description</span></span>                                                           |
| [<span data-ttu-id="93f12-118">**double**</span><span class="sxs-lookup"><span data-stu-id="93f12-118">**double**</span></span>](coareftime-double.md)                     | <span data-ttu-id="93f12-119">Convierte la hora de referencia en un valor **Double** .</span><span class="sxs-lookup"><span data-stu-id="93f12-119">Converts the reference time to a **double** value.</span></span>                    |
| [<span data-ttu-id="93f12-120">**tiempo de referencia \_**</span><span class="sxs-lookup"><span data-stu-id="93f12-120">**REFERENCE\_TIME**</span></span>](coareftime-reference-time.md)    | <span data-ttu-id="93f12-121">Convierte el objeto en un valor **de \_ hora de referencia** .</span><span class="sxs-lookup"><span data-stu-id="93f12-121">Casts the object to a **REFERENCE\_TIME** value.</span></span>                      |
| [<span data-ttu-id="93f12-122">**operador =**</span><span class="sxs-lookup"><span data-stu-id="93f12-122">**operator =**</span></span>](coareftime-operator-assign.md)        | <span data-ttu-id="93f12-123">Asigna una nueva hora de referencia.</span><span class="sxs-lookup"><span data-stu-id="93f12-123">Assigns a new reference time.</span></span>                                         |
| [<span data-ttu-id="93f12-124">**operador = =**</span><span class="sxs-lookup"><span data-stu-id="93f12-124">**operator ==**</span></span>](coareftime-operator-eq.md)           | <span data-ttu-id="93f12-125">Comprueba la igualdad entre dos tiempos de referencia.</span><span class="sxs-lookup"><span data-stu-id="93f12-125">Tests for equality between two reference times.</span></span>                       |
| [<span data-ttu-id="93f12-126">**operador! =**</span><span class="sxs-lookup"><span data-stu-id="93f12-126">**operator !=**</span></span>](cmediatype-operator-neq.md)          | <span data-ttu-id="93f12-127">Comprueba la desigualdad entre dos tiempos de referencia.</span><span class="sxs-lookup"><span data-stu-id="93f12-127">Tests for inequality between two reference times.</span></span>                     |
| [<span data-ttu-id="93f12-128">**operador <**</span><span class="sxs-lookup"><span data-stu-id="93f12-128">**operator <**</span></span>](coareftime-operator-lt.md)         | <span data-ttu-id="93f12-129">Comprueba si una hora de referencia es menor que otra.</span><span class="sxs-lookup"><span data-stu-id="93f12-129">Tests if one reference time is less than another.</span></span>                     |
| [<span data-ttu-id="93f12-130">**operador >**</span><span class="sxs-lookup"><span data-stu-id="93f12-130">**operator >**</span></span>](coareftime-operator-gt.md)         | <span data-ttu-id="93f12-131">Comprueba si una hora de referencia es mayor que otra.</span><span class="sxs-lookup"><span data-stu-id="93f12-131">Tests if one reference time is greater than another.</span></span>                  |
| [<span data-ttu-id="93f12-132">**operador <=**</span><span class="sxs-lookup"><span data-stu-id="93f12-132">**operator <=**</span></span>](coareftime-operator-lteq.md)      | <span data-ttu-id="93f12-133">Comprueba si una hora de referencia es menor o igual que otra.</span><span class="sxs-lookup"><span data-stu-id="93f12-133">Tests if one reference time is less than or equal to another.</span></span>         |
| [<span data-ttu-id="93f12-134">**operador >=**</span><span class="sxs-lookup"><span data-stu-id="93f12-134">**operator >=**</span></span>](coareftime-operator-gteq.md)      | <span data-ttu-id="93f12-135">Comprueba si una hora de referencia es mayor o igual que otra.</span><span class="sxs-lookup"><span data-stu-id="93f12-135">Tests if one reference time is greater than or equal to another.</span></span>      |
| [<span data-ttu-id="93f12-136">**operador +**</span><span class="sxs-lookup"><span data-stu-id="93f12-136">**operator +**</span></span>](coareftime-operator-plus.md)          | <span data-ttu-id="93f12-137">Agrega dos tiempos de referencia.</span><span class="sxs-lookup"><span data-stu-id="93f12-137">Adds two reference times.</span></span>                                             |
| [<span data-ttu-id="93f12-138">\* \* (operador) \* \*</span><span class="sxs-lookup"><span data-stu-id="93f12-138">\*\*operator  \*\*</span></span>](coareftime-operator-minus.md)         | <span data-ttu-id="93f12-139">Resta una hora de referencia de otra.</span><span class="sxs-lookup"><span data-stu-id="93f12-139">Subtracts one reference time from another.</span></span>                            |
| [<span data-ttu-id="93f12-140">**operador + =**</span><span class="sxs-lookup"><span data-stu-id="93f12-140">**operator +=**</span></span>](coareftime-operator-plus-assign.md)  | <span data-ttu-id="93f12-141">Agrega dos tiempos de referencia y asigna el resultado a este objeto.</span><span class="sxs-lookup"><span data-stu-id="93f12-141">Adds two reference times, and assigns the result to this object.</span></span>      |
| [<span data-ttu-id="93f12-142">**operador =**</span><span class="sxs-lookup"><span data-stu-id="93f12-142">**operator  =**</span></span>](coareftime-operator-minus-assign.md) | <span data-ttu-id="93f12-143">Resta dos tiempos de referencia y asigna el resultado a este objeto.</span><span class="sxs-lookup"><span data-stu-id="93f12-143">Subtracts two reference times, and assigns the result to this object.</span></span> |
| [<span data-ttu-id="93f12-144">**Operator \***</span><span class="sxs-lookup"><span data-stu-id="93f12-144">**operator \***</span></span>](coareftime-operator-mult.md)         | <span data-ttu-id="93f12-145">Multiplica una hora de referencia por un valor.</span><span class="sxs-lookup"><span data-stu-id="93f12-145">Multiplies a reference time by a value.</span></span>                               |
| [<span data-ttu-id="93f12-146">**Operator**</span><span class="sxs-lookup"><span data-stu-id="93f12-146">**operator /**</span></span>](coareftime-operator-div.md)           | <span data-ttu-id="93f12-147">Divide una hora de referencia por un valor.</span><span class="sxs-lookup"><span data-stu-id="93f12-147">Divides a reference time by a value.</span></span>                                  |



 

## <a name="requirements"></a><span data-ttu-id="93f12-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93f12-148">Requirements</span></span>



| <span data-ttu-id="93f12-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="93f12-149">Requirement</span></span> | <span data-ttu-id="93f12-150">Value</span><span class="sxs-lookup"><span data-stu-id="93f12-150">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93f12-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="93f12-151">Header</span></span><br/>  | <dl> <span data-ttu-id="93f12-152"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="93f12-152"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="93f12-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="93f12-153">Library</span></span><br/> | <dl> <span data-ttu-id="93f12-154"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="93f12-154"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




