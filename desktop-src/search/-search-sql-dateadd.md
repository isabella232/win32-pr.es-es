---
description: La función DATEADD realiza los cálculos de fecha y hora de las propiedades coincidentes que tienen tipos de fecha. Utilice la función DATEADD para obtener fechas y horas en un período de tiempo especificado antes de la presente.
ms.assetid: 83ef098d-85ef-4883-a1e1-9229e050247f
title: Función DATEADD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0b193e75ec644eb3312a61c723edeac43ee264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153962"
---
# <a name="dateadd-function"></a><span data-ttu-id="68b03-104">Función DATEADD</span><span class="sxs-lookup"><span data-stu-id="68b03-104">DATEADD Function</span></span>

<span data-ttu-id="68b03-105">La función DATEADD realiza los cálculos de fecha y hora de las propiedades coincidentes que tienen tipos de fecha.</span><span class="sxs-lookup"><span data-stu-id="68b03-105">The DATEADD function performs time and date calculations for matching properties having date types.</span></span> <span data-ttu-id="68b03-106">Utilice la función DATEADD para obtener fechas y horas en un período de tiempo especificado antes de la presente.</span><span class="sxs-lookup"><span data-stu-id="68b03-106">Use the DATEADD function to obtain dates and times in a specified amount of time before the present.</span></span>

## <a name="syntax"></a><span data-ttu-id="68b03-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68b03-107">Syntax</span></span>


```
DATEADD (DateTimeUnits, OffsetValue, DateTime)
```



## <a name="arguments"></a><span data-ttu-id="68b03-108">Argumentos</span><span class="sxs-lookup"><span data-stu-id="68b03-108">Arguments</span></span>

<span data-ttu-id="68b03-109">*DateTimeUnits*</span><span class="sxs-lookup"><span data-stu-id="68b03-109">*DateTimeUnits*</span></span>

<span data-ttu-id="68b03-110">Especifica las unidades del parámetro de *fecha* y hora: año, trimestre, mes, semana, día, hora, minuto o segundo.</span><span class="sxs-lookup"><span data-stu-id="68b03-110">Specifies the units of the *DateTime* parameter: YEAR, QUARTER, MONTH, WEEK, DAY, HOUR, MINUTE, or SECOND.</span></span> <span data-ttu-id="68b03-111">Este valor distingue entre mayúsculas y minúsculas y no se necesitan comillas alrededor del parámetro.</span><span class="sxs-lookup"><span data-stu-id="68b03-111">This value is case-sensitive, and quotation marks are not required around the parameter.</span></span>

<span data-ttu-id="68b03-112">*OffsetValue*</span><span class="sxs-lookup"><span data-stu-id="68b03-112">*OffsetValue*</span></span>

<span data-ttu-id="68b03-113">Especifica el desplazamiento de tiempo, en las unidades especificadas por el parámetro *DateTimeUnits* .</span><span class="sxs-lookup"><span data-stu-id="68b03-113">Specifies the time offset, in the units specified by the *DateTimeUnits* parameter.</span></span> <span data-ttu-id="68b03-114">**OffsetValue** debe ser un entero negativo.</span><span class="sxs-lookup"><span data-stu-id="68b03-114">**OffsetValue** must be a negative integer.</span></span> <span data-ttu-id="68b03-115">No se admiten valores positivos.</span><span class="sxs-lookup"><span data-stu-id="68b03-115">Positive values are not supported.</span></span>

<span data-ttu-id="68b03-116">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="68b03-116">*DateTime*</span></span>

<span data-ttu-id="68b03-117">Especifica una marca de tiempo de la que se va a calcular el desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="68b03-117">Specifies a time stamp from which to calculate the offset.</span></span> <span data-ttu-id="68b03-118">No puede ser un literal de fecha.</span><span class="sxs-lookup"><span data-stu-id="68b03-118">This cannot be a date literal.</span></span> <span data-ttu-id="68b03-119">Debe ser GETGMTDATE o el resultado de otra función DATEADD.</span><span class="sxs-lookup"><span data-stu-id="68b03-119">It must be either GETGMTDATE or the result of another DATEADD function.</span></span>

## <a name="remarks"></a><span data-ttu-id="68b03-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68b03-120">Remarks</span></span>

<span data-ttu-id="68b03-121">La función DATEADD solo se puede usar en comparaciones de valores literales y solo en el lado derecho del operador de comparación.</span><span class="sxs-lookup"><span data-stu-id="68b03-121">The DATEADD function can be used only in literal value comparisons and only on the right side of the comparison operator.</span></span>

<span data-ttu-id="68b03-122">La función GETGMTDATE devuelve la fecha y hora actuales en la hora del meridiano de Greenwich (GMT).</span><span class="sxs-lookup"><span data-stu-id="68b03-122">The GETGMTDATE function returns the current date and time in Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="68b03-123">Recuerde que este valor puede no ser el mismo que el de la hora local del equipo.</span><span class="sxs-lookup"><span data-stu-id="68b03-123">Remember that this value may not be the same as the local time of your computer.</span></span>

<span data-ttu-id="68b03-124">No use el operador de comparación es igual a (=) porque la representación de tiempo interna puede producir errores de redondeo que producen resultados de coincidencia inesperados.</span><span class="sxs-lookup"><span data-stu-id="68b03-124">Do not use the equals (=) comparison operator because the internal time representation can produce rounding errors that result in unexpected matching results.</span></span>

<span data-ttu-id="68b03-125">Puede usar varias funciones DATEADD para combinar unidades de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="68b03-125">You can use multiple DATEADD functions to combine offset units.</span></span>

### <a name="examples"></a><span data-ttu-id="68b03-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="68b03-126">Examples</span></span>

<span data-ttu-id="68b03-127">La cláusula WHERE de ejemplo siguiente coincide con los documentos que se modificaron en los últimos cinco días:</span><span class="sxs-lookup"><span data-stu-id="68b03-127">The following example WHERE clause matches documents that were modified within the last five days:</span></span>


```
...WHERE System.DateModified <=DATEADD (DAY, -5, GETGMTDATE())
```



<span data-ttu-id="68b03-128">En el ejemplo siguiente, la cláusula WHERE coincide con los documentos que se modificaron en los últimos dos días y cuatro horas:</span><span class="sxs-lookup"><span data-stu-id="68b03-128">The following example WHERE clause matches documents that were modified within the last two days and four hours:</span></span>


```
...WHERE System.DateModified <=DATEADD (DAY, -2, DATEADD (HOUR, -4, GETGMTDATE()))
```



## <a name="related-topics"></a><span data-ttu-id="68b03-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="68b03-129">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="68b03-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="68b03-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="68b03-131">Comparación de valores literales</span><span class="sxs-lookup"><span data-stu-id="68b03-131">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[<span data-ttu-id="68b03-132">Comparaciones de varios valores (matriz)</span><span class="sxs-lookup"><span data-stu-id="68b03-132">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

<span data-ttu-id="68b03-133">**Vista**</span><span class="sxs-lookup"><span data-stu-id="68b03-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="68b03-134">Predicados de texto completo</span><span class="sxs-lookup"><span data-stu-id="68b03-134">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="68b03-135">Predicados que no son de texto completo</span><span class="sxs-lookup"><span data-stu-id="68b03-135">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



