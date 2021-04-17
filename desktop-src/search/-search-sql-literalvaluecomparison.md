---
description: La comparación de valores literales utiliza operadores de comparación estándar para hacer coincidir una columna de un solo valor con un valor literal.
ms.assetid: 941298b4-d703-4b3f-8bde-0e6e158560df
title: Comparación de valores literales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d8577e5a97dcc92131658c325f175efa1d0c3fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696282"
---
# <a name="literal-value-comparison"></a><span data-ttu-id="02ab4-103">Comparación de valores literales</span><span class="sxs-lookup"><span data-stu-id="02ab4-103">Literal Value Comparison</span></span>

<span data-ttu-id="02ab4-104">La comparación de valores literales utiliza operadores de comparación estándar para hacer coincidir una columna de un solo valor con un valor [literal](-search-sql-literals.md) .</span><span class="sxs-lookup"><span data-stu-id="02ab4-104">The literal value comparison uses standard comparison operators for matching a single-valued column to a [literal](-search-sql-literals.md) value.</span></span> <span data-ttu-id="02ab4-105">Para obtener información sobre la comparación de columnas con varios valores, consulte [comparaciones con múltiples valores (matriz)](-search-sql-multivaluedcomparisons.md).</span><span class="sxs-lookup"><span data-stu-id="02ab4-105">For information about comparing multivalued columns, see [Multi-Valued (ARRAY) Comparisons](-search-sql-multivaluedcomparisons.md).</span></span>

<span data-ttu-id="02ab4-106">El predicado de comparación de valores literales tiene la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="02ab4-106">The literal value comparison predicate has the following syntax:</span></span>


```
...WHERE <column> <comparison operator> <literal>
```



> [!Note]  
> <span data-ttu-id="02ab4-107">El lado derecho de la comparación debe ser un literal.</span><span class="sxs-lookup"><span data-stu-id="02ab4-107">The right side of the comparison must be a literal.</span></span> <span data-ttu-id="02ab4-108">No se puede comparar una columna con un valor calculado y no se puede comparar una columna con otra columna.</span><span class="sxs-lookup"><span data-stu-id="02ab4-108">You cannot compare a column against a computed value, and you cannot compare a column against another column.</span></span>

 

<span data-ttu-id="02ab4-109">La parte de la columna es cualquier columna de propiedad válida y se puede convertir a otro tipo si es necesario.</span><span class="sxs-lookup"><span data-stu-id="02ab4-109">The column part is any valid property column and can be cast to another type if necessary.</span></span> <span data-ttu-id="02ab4-110">Opcionalmente, puede escribir el nombre de la columna entre comillas dobles para facilitar la lectura sin que ello afecte a la funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="02ab4-110">Optionally, you can enclose the column name in double quotes for readability without affecting functionality.</span></span> <span data-ttu-id="02ab4-111">Para obtener más información, vea [convertir el tipo de datos de una columna](-search-sql-castingdatacolumntype.md).</span><span class="sxs-lookup"><span data-stu-id="02ab4-111">For more information, see [Casting the Data Type of a Column](-search-sql-castingdatacolumntype.md).</span></span>

<span data-ttu-id="02ab4-112">El literal puede ser cualquier cadena, numérica, hexadecimal, booleano o literal de fecha, entre comillas simples.</span><span class="sxs-lookup"><span data-stu-id="02ab4-112">The literal can be any string, numeric, hexadecimal, Boolean, or date literal, enclosed in single quotation marks.</span></span> <span data-ttu-id="02ab4-113">Solo se reconocen las coincidencias exactas y se omiten los caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="02ab4-113">Only exact matches are recognized, and wildcard characters are ignored.</span></span> <span data-ttu-id="02ab4-114">El literal también se puede convertir en otro tipo.</span><span class="sxs-lookup"><span data-stu-id="02ab4-114">The literal can also be cast to another type.</span></span>

## <a name="comparison-operators"></a><span data-ttu-id="02ab4-115">Operadores de comparación</span><span class="sxs-lookup"><span data-stu-id="02ab4-115">Comparison Operators</span></span>

<span data-ttu-id="02ab4-116">En la tabla siguiente se describen los operadores de comparación admitidos.</span><span class="sxs-lookup"><span data-stu-id="02ab4-116">The following table describes the supported comparison operators.</span></span>



| <span data-ttu-id="02ab4-117">Operadores de comparación</span><span class="sxs-lookup"><span data-stu-id="02ab4-117">Comparison operator</span></span> | <span data-ttu-id="02ab4-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="02ab4-118">Description</span></span>              |
|---------------------|--------------------------|
| =                   | <span data-ttu-id="02ab4-119">Igual a</span><span class="sxs-lookup"><span data-stu-id="02ab4-119">Equal to</span></span>                 |
| <span data-ttu-id="02ab4-120">! = o <></span><span class="sxs-lookup"><span data-stu-id="02ab4-120">!= or <></span></span>      | <span data-ttu-id="02ab4-121">No es igual a</span><span class="sxs-lookup"><span data-stu-id="02ab4-121">Not equal to</span></span>             |
| >                | <span data-ttu-id="02ab4-122">Mayor que</span><span class="sxs-lookup"><span data-stu-id="02ab4-122">Greater than</span></span>             |
| >=               | <span data-ttu-id="02ab4-123">Mayor o igual que</span><span class="sxs-lookup"><span data-stu-id="02ab4-123">Greater than or equal to</span></span> |
| <                | <span data-ttu-id="02ab4-124">Menor que</span><span class="sxs-lookup"><span data-stu-id="02ab4-124">Less than</span></span>                |
| <=               | <span data-ttu-id="02ab4-125">Menor o igual que</span><span class="sxs-lookup"><span data-stu-id="02ab4-125">Less than or equal to</span></span>    |



 

 

<span data-ttu-id="02ab4-126">Junto con el operador "=", Lenguaje de consulta estructurado de Windows Search (SQL) admite el uso de las palabras clave BEFORe y AFTER, que especifican si la consulta debe comparar los valores de columna antes o después de un valor especificado, en el orden de ordenación del diccionario.</span><span class="sxs-lookup"><span data-stu-id="02ab4-126">In conjunction with the "=" operator, Windows Search Structured Query Language (SQL) supports the use of BEFORE and AFTER keywords, which specify whether the query should compare column values before or after a specified value, in dictionary sort ordering.</span></span>


```
...WHERE <column> <comparison operator> [BEFORE | AFTER](<https://msdn.microsoft.com/library/Ff637626(v=MSDN.10).aspx>)
```



## <a name="examples"></a><span data-ttu-id="02ab4-127">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="02ab4-127">Examples</span></span>

<span data-ttu-id="02ab4-128">A continuación se muestran ejemplos del predicado de comparación de valores literales.</span><span class="sxs-lookup"><span data-stu-id="02ab4-128">The following are examples of the literal value comparison predicate.</span></span>


```
SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Title = 'Accounting'

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.IsFlagged != TRUE

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Size >= 10000

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Author = BEFORE('m')
```



## <a name="related-topics"></a><span data-ttu-id="02ab4-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="02ab4-129">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="02ab4-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="02ab4-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="02ab4-131">LIKE (predicado)</span><span class="sxs-lookup"><span data-stu-id="02ab4-131">LIKE Predicate</span></span>](-search-sql-like.md)
</dt> <dt>

[<span data-ttu-id="02ab4-132">DATEADD (función)</span><span class="sxs-lookup"><span data-stu-id="02ab4-132">DATEADD Function</span></span>](-search-sql-dateadd.md)
</dt> <dt>

[<span data-ttu-id="02ab4-133">Comparaciones de varios valores (matriz)</span><span class="sxs-lookup"><span data-stu-id="02ab4-133">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

[<span data-ttu-id="02ab4-134">Predicado NULL</span><span class="sxs-lookup"><span data-stu-id="02ab4-134">NULL Predicate</span></span>](-search-sql-null.md)
</dt> <dt>

<span data-ttu-id="02ab4-135">**Vista**</span><span class="sxs-lookup"><span data-stu-id="02ab4-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="02ab4-136">Predicados de texto completo</span><span class="sxs-lookup"><span data-stu-id="02ab4-136">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="02ab4-137">Predicados que no son de texto completo</span><span class="sxs-lookup"><span data-stu-id="02ab4-137">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



