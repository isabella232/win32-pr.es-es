---
description: El lenguaje de consulta de WMI (WQL) es un subconjunto del Lenguaje de consulta estructurado de American National Standards Institute (ANSI SQL) &\# 8212; con cambios semánticos menores. En la tabla siguiente se enumeran las palabras clave de WQL.
ms.assetid: 72a7ec04-9af3-41ae-9189-6e1d46803fa9
ms.tgt_platform: multiple
title: WQL (SQL para WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87498b6e8e37ab900e21eedf2c15d5cdba9f9bd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276244"
---
# <a name="wql-sql-for-wmi"></a><span data-ttu-id="9d028-104">WQL (SQL para WMI)</span><span class="sxs-lookup"><span data-stu-id="9d028-104">WQL (SQL for WMI)</span></span>

<span data-ttu-id="9d028-105">El lenguaje de consulta de WMI (WQL) es un subconjunto del Lenguaje de consulta estructurado de American National Standards Institute (ANSI SQL) con cambios semánticos menores.</span><span class="sxs-lookup"><span data-stu-id="9d028-105">The WMI Query Language (WQL) is a subset of the American National Standards Institute Structured Query Language (ANSI SQL) with minor semantic changes.</span></span> <span data-ttu-id="9d028-106">En la tabla siguiente se enumeran las palabras clave de WQL.</span><span class="sxs-lookup"><span data-stu-id="9d028-106">The following table lists the WQL keywords.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9d028-107">Palabra clave WQL</span><span class="sxs-lookup"><span data-stu-id="9d028-107">WQL keyword</span></span></th>
<th><span data-ttu-id="9d028-108">Significado</span><span class="sxs-lookup"><span data-stu-id="9d028-108">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d028-109">y</span><span class="sxs-lookup"><span data-stu-id="9d028-109">AND</span></span><br/></td>
<td><span data-ttu-id="9d028-110">Combina dos expresiones booleanas y devuelve <strong>true</strong> cuando ambas expresiones son <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d028-110">Combines two Boolean expressions, and returns <strong>TRUE</strong> when both expressions are <strong>TRUE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d028-111"><a href="associators-of-statement.md">ASSOCIATORS OF</a></span><span class="sxs-lookup"><span data-stu-id="9d028-111"><a href="associators-of-statement.md">ASSOCIATORS OF</a></span></span></td>
<td><span data-ttu-id="9d028-112">Recupera todas las instancias de asociadas a una instancia de de origen.</span><span class="sxs-lookup"><span data-stu-id="9d028-112">Retrieves all instances that are associated with a source instance.</span></span><br/> <span data-ttu-id="9d028-113">Use esta instrucción con consultas de esquema y consultas de datos.</span><span class="sxs-lookup"><span data-stu-id="9d028-113">Use this statement with schema queries and data queries.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d028-114"><a href="--class-identifier.md">__CLASS</a></span><span class="sxs-lookup"><span data-stu-id="9d028-114"><a href="--class-identifier.md">__CLASS</a></span></span></td>
<td><span data-ttu-id="9d028-115">Hace referencia a la clase del objeto en una consulta.</span><span class="sxs-lookup"><span data-stu-id="9d028-115">References the class of the object in a query.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d028-116">FROM</span><span class="sxs-lookup"><span data-stu-id="9d028-116">FROM</span></span><br/></td>
<td><span data-ttu-id="9d028-117">Especifica la clase que contiene las propiedades enumeradas en una instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="9d028-117">Specifies the class that contains the properties listed in a SELECT statement.</span></span> <span data-ttu-id="9d028-118">Instrumental de administración de Windows (WMI) admite consultas de datos de una sola clase a la vez.</span><span class="sxs-lookup"><span data-stu-id="9d028-118">Windows Management Instrumentation (WMI) supports data queries from only one class at a time.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d028-119"><a href="group-clause.md">GROUP (cláusula)</a></span><span class="sxs-lookup"><span data-stu-id="9d028-119"><a href="group-clause.md">GROUP Clause</a></span></span></td>
<td><span data-ttu-id="9d028-120">Hace que WMI genere una notificación para representar un grupo de eventos.</span><span class="sxs-lookup"><span data-stu-id="9d028-120">Causes WMI to generate one notification to represent a group of events.</span></span><br/> <span data-ttu-id="9d028-121">Use esta cláusula con consultas de eventos.</span><span class="sxs-lookup"><span data-stu-id="9d028-121">Use this clause with event queries.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d028-122"><a href="having-clause.md">HAVING</a></span><span class="sxs-lookup"><span data-stu-id="9d028-122"><a href="having-clause.md">HAVING</a></span></span></td>
<td><span data-ttu-id="9d028-123">Filtra los eventos que se reciben durante el intervalo de agrupación especificado en la <a href="within-clause.md">cláusula Within</a>.</span><span class="sxs-lookup"><span data-stu-id="9d028-123">Filters the events that are received during the grouping interval that is specified in the <a href="within-clause.md">WITHIN clause</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d028-124"><a href="wql-operators.md">IS</a></span><span class="sxs-lookup"><span data-stu-id="9d028-124"><a href="wql-operators.md">IS</a></span></span></td>
<td><span data-ttu-id="9d028-125">Operador de comparación utilizado con NOT y <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d028-125">Comparison operator used with NOT and <strong>NULL</strong>.</span></span> <span data-ttu-id="9d028-126">La sintaxis de esta instrucción es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="9d028-126">The syntax for this statement is the following:</span></span><br/> <span data-ttu-id="9d028-127">IS [NOT] <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="9d028-127">IS [NOT] <strong>NULL</strong></span></span><br/> <span data-ttu-id="9d028-128">(donde no es opcional)</span><span class="sxs-lookup"><span data-stu-id="9d028-128">(where NOT is optional)</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d028-129"><a href="wql-operators.md">ISA</a></span><span class="sxs-lookup"><span data-stu-id="9d028-129"><a href="wql-operators.md">ISA</a></span></span></td>
<td><span data-ttu-id="9d028-130">Operador que aplica una consulta a las subclases de una clase especificada.</span><span class="sxs-lookup"><span data-stu-id="9d028-130">Operator that applies a query to the subclasses of a specified class.</span></span> <span data-ttu-id="9d028-131">Para obtener más información, vea <a href="isa-operator-for-event-queries.md">operador ISA para consultas de eventos</a>, <a href="isa-operator-for-data-queries.md">operador ISA para consultas de datos</a>y <a href="isa-operator-for-schema-queries.md">operador ISA para consultas de esquema</a>.</span><span class="sxs-lookup"><span data-stu-id="9d028-131">For more information, see <a href="isa-operator-for-event-queries.md">ISA Operator for Event Queries</a>, <a href="isa-operator-for-data-queries.md">ISA Operator for Data Queries</a>, and <a href="isa-operator-for-schema-queries.md">ISA Operator for Schema Queries</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d028-132">KEYSONLY</span><span class="sxs-lookup"><span data-stu-id="9d028-132">KEYSONLY</span></span><br/></td>
<td><span data-ttu-id="9d028-133">Se utiliza en <a href="references-of-statement.md">referencias de</a> y <a href="associators-of-statement.md">asociadores de</a> consultas para asegurarse de que las instancias resultantes solo se rellenan con las claves de las instancias, lo que reduce la sobrecarga de la llamada.</span><span class="sxs-lookup"><span data-stu-id="9d028-133">Used in <a href="references-of-statement.md">REFERENCES OF</a> and <a href="associators-of-statement.md">ASSOCIATORS OF</a> queries to ensure that the resulting instances are only populated with the keys of the instances, which reduces the overhead of the call.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d028-134"><a href="wql-operators.md">LIKE</a></span><span class="sxs-lookup"><span data-stu-id="9d028-134"><a href="wql-operators.md">LIKE</a></span></span></td>
<td><span data-ttu-id="9d028-135">Operador que determina si una cadena de caracteres determinada coincide con un patrón especificado.</span><span class="sxs-lookup"><span data-stu-id="9d028-135">Operator that determines whether or not a given character string matches a specified pattern.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d028-136">NOT</span><span class="sxs-lookup"><span data-stu-id="9d028-136">NOT</span></span><br/></td>
<td><span data-ttu-id="9d028-137">Operador de comparación que utiliza en una consulta WQL SELECT, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="9d028-137">Comparison operator that use in a WQL SELECT query, for example:</span></span><br/>
<pre data-space="preserve"><code>SELECT * FROM meta_class WHERE NOT __class < &quot;Win32&quot; AND NOT __this ISA &quot;Win32_Account&quot;</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d028-138"><strong>NULL</strong></span><span class="sxs-lookup"><span data-stu-id="9d028-138"><strong>NULL</strong></span></span></td>
<td><span data-ttu-id="9d028-139">Indica que un objeto no tiene un valor asignado explícitamente.</span><span class="sxs-lookup"><span data-stu-id="9d028-139">Indicates an object does not have an explicitly assigned value.</span></span> <span data-ttu-id="9d028-140"><strong>Null</strong> no es equivalente a cero (0) o en blanco.</span><span class="sxs-lookup"><span data-stu-id="9d028-140"><strong>NULL</strong> is not equivalent to zero (0) or blank.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d028-141">O BIEN</span><span class="sxs-lookup"><span data-stu-id="9d028-141">OR</span></span><br/></td>
<td><span data-ttu-id="9d028-142">Combina dos condiciones.</span><span class="sxs-lookup"><span data-stu-id="9d028-142">Combines two conditions.</span></span><br/> <span data-ttu-id="9d028-143">Cuando se utiliza más de un operador lógico en una instrucción, los operadores OR se evalúan después de los operadores y.</span><span class="sxs-lookup"><span data-stu-id="9d028-143">When more than one logical operator is used in a statement, the OR operators are evaluated after the AND operators.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d028-144"><a href="references-of-statement.md">REFERENCIAS DE</a></span><span class="sxs-lookup"><span data-stu-id="9d028-144"><a href="references-of-statement.md">REFERENCES OF</a></span></span></td>
<td><span data-ttu-id="9d028-145">Recupera todas las instancias de asociación que hacen referencia a una instancia de origen concreta.</span><span class="sxs-lookup"><span data-stu-id="9d028-145">Retrieves all association instances that refer to a specific source instance.</span></span> <span data-ttu-id="9d028-146">Use esta instrucción con consultas de esquema y de datos.</span><span class="sxs-lookup"><span data-stu-id="9d028-146">Use this statement with schema and data queries.</span></span> <span data-ttu-id="9d028-147">La instrucción <a href="references-of-statement.md">References de</a> es similar a la instrucción <a href="associators-of-statement.md">ASSOCIATORS of</a> .</span><span class="sxs-lookup"><span data-stu-id="9d028-147">The <a href="references-of-statement.md">REFERENCES OF</a> statement is similar to the <a href="associators-of-statement.md">ASSOCIATORS OF</a> statement.</span></span> <span data-ttu-id="9d028-148">Sin embargo, no recupera las instancias de extremo; Recupera las instancias de asociación.</span><span class="sxs-lookup"><span data-stu-id="9d028-148">However, it does not retrieve endpoint instances; it retrieves the association instances.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d028-149">SELECT</span><span class="sxs-lookup"><span data-stu-id="9d028-149">SELECT</span></span><br/></td>
<td><span data-ttu-id="9d028-150">Especifica las propiedades que se utilizan en una consulta.</span><span class="sxs-lookup"><span data-stu-id="9d028-150">Specifies the properties that are used in a query.</span></span><br/> <span data-ttu-id="9d028-151">Para obtener más información, vea <a href="select-statement-for-data-queries.md">instrucción SELECT para consultas de datos</a>, <a href="select-statement-for-event-queries.md">instrucción SELECT para consultas de eventos</a>o <a href="select-statement-for-schema-queries.md">instrucción SELECT para consultas de esquema</a>.</span><span class="sxs-lookup"><span data-stu-id="9d028-151">For more information, see <a href="select-statement-for-data-queries.md">SELECT Statement for Data Queries</a>, <a href="select-statement-for-event-queries.md">SELECT Statement for Event Queries</a>, or <a href="select-statement-for-schema-queries.md">SELECT Statement for Schema Queries</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d028-152"><strong>TRUE</strong></span><span class="sxs-lookup"><span data-stu-id="9d028-152"><strong>TRUE</strong></span></span></td>
<td><span data-ttu-id="9d028-153">Operador booleano que se evalúa como-1 (menos uno).</span><span class="sxs-lookup"><span data-stu-id="9d028-153">Boolean operator that evaluates to -1 (minus one).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d028-154"><a href="where-clause.md">WHERE</a></span><span class="sxs-lookup"><span data-stu-id="9d028-154"><a href="where-clause.md">WHERE</a></span></span></td>
<td><span data-ttu-id="9d028-155">Limita el ámbito de una consulta de datos, eventos o esquemas.</span><span class="sxs-lookup"><span data-stu-id="9d028-155">Narrows the scope of a data, event, or schema query.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d028-156"><a href="within-clause.md">WITHIN</a></span><span class="sxs-lookup"><span data-stu-id="9d028-156"><a href="within-clause.md">WITHIN</a></span></span></td>
<td><span data-ttu-id="9d028-157">Especifica un intervalo de sondeo o agrupación.</span><span class="sxs-lookup"><span data-stu-id="9d028-157">Specifies a polling or grouping interval.</span></span><br/> <span data-ttu-id="9d028-158">Use esta cláusula con consultas de eventos.</span><span class="sxs-lookup"><span data-stu-id="9d028-158">Use this clause with event queries.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d028-159">false</span><span class="sxs-lookup"><span data-stu-id="9d028-159">FALSE</span></span><br/></td>
<td><span data-ttu-id="9d028-160">Operador booleano que se evalúa como 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="9d028-160">Boolean operator that evaluates to 0 (zero).</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="9d028-161">El uso de una palabra clave WQL como nombre de objeto puede dar lugar a una consulta que no se puede analizar incluso cuando la consulta se compila sin errores.</span><span class="sxs-lookup"><span data-stu-id="9d028-161">Using a WQL key word as an object name can result in a query that cannot be parsed even when the query compiles without error.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9d028-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9d028-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d028-163">Operadores WQL</span><span class="sxs-lookup"><span data-stu-id="9d028-163">WQL Operators</span></span>](wql-operators.md)
</dt> <dt>

[<span data-ttu-id="9d028-164">WQL: formatos de fecha admitidos</span><span class="sxs-lookup"><span data-stu-id="9d028-164">WQL-Supported Date Formats</span></span>](wql-supported-date-formats.md)
</dt> <dt>

[<span data-ttu-id="9d028-165">WQL: formatos de hora compatibles</span><span class="sxs-lookup"><span data-stu-id="9d028-165">WQL-Supported Time Formats</span></span>](wql-supported-time-formats.md)
</dt> </dl>

 

 




