---
title: Crear un filtro de consulta
description: Un filtro de consulta indica a Active Directory Domain Services que busque los datos en una sintaxis de consulta LDAP. Todas las tecnologías de acceso a datos especificadas que se enumeran en el tema elección de la tecnología de búsqueda admiten la sintaxis de consultas LDAP.
ms.assetid: 0bd652f0-41a6-4a0d-8742-9d6a2a7f168a
ms.tgt_platform: multiple
keywords:
- Active Directory ejemplos Active Directory, crear un filtro de consulta
- filtros de consulta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2e0a4e4a02312fcc9affb681407044ba0d8e18
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903003"
---
# <a name="creating-a-query-filter"></a><span data-ttu-id="0259e-106">Crear un filtro de consulta</span><span class="sxs-lookup"><span data-stu-id="0259e-106">Creating a Query Filter</span></span>

<span data-ttu-id="0259e-107">Un filtro de consulta indica a Active Directory Domain Services que busque los datos en una sintaxis de consulta LDAP.</span><span class="sxs-lookup"><span data-stu-id="0259e-107">A query filter instructs Active Directory Domain Services to find data in an LDAP query syntax.</span></span> <span data-ttu-id="0259e-108">Todas las tecnologías de acceso a datos especificadas que se enumeran en el tema [elección de la tecnología de búsqueda](choosing-the-search-technology.md) admiten la sintaxis de consultas LDAP.</span><span class="sxs-lookup"><span data-stu-id="0259e-108">All the specified data access technologies listed in the [Choosing the Search Technology](choosing-the-search-technology.md) topic support LDAP query syntax.</span></span>

<span data-ttu-id="0259e-109">La sintaxis de consulta LDAP es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="0259e-109">The LDAP query syntax is as follows:</span></span>


```C++
<expression><expression>...
```



<span data-ttu-id="0259e-110">Un filtro puede contener una o varias expresiones.</span><span class="sxs-lookup"><span data-stu-id="0259e-110">A filter can contain one, or more, expressions.</span></span> <span data-ttu-id="0259e-111">Una expresión tiene el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="0259e-111">An expression has the following form:</span></span>


```C++
(<logicaloperator><comparison><comparison...>)
```



<span data-ttu-id="0259e-112">donde " &lt; operadorlógico &gt; " es uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="0259e-112">where "&lt;logicaloperator&gt;" is one of the following.</span></span>



| <span data-ttu-id="0259e-113">Operator</span><span class="sxs-lookup"><span data-stu-id="0259e-113">Operator</span></span>        | <span data-ttu-id="0259e-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="0259e-114">Description</span></span>                |
|-----------------|----------------------------|
| <span data-ttu-id="0259e-115">"\|"</span><span class="sxs-lookup"><span data-stu-id="0259e-115">"\|"</span></span><br/> | <span data-ttu-id="0259e-116">**Or** lógico</span><span class="sxs-lookup"><span data-stu-id="0259e-116">Logical **OR**</span></span><br/>  |
| <span data-ttu-id="0259e-117">"&"</span><span class="sxs-lookup"><span data-stu-id="0259e-117">"&"</span></span><br/>  | <span data-ttu-id="0259e-118">**And** lógico</span><span class="sxs-lookup"><span data-stu-id="0259e-118">Logical **AND**</span></span><br/> |
| <span data-ttu-id="0259e-119">"!"</span><span class="sxs-lookup"><span data-stu-id="0259e-119">"!"</span></span><br/>  | <span data-ttu-id="0259e-120">**Not** lógico</span><span class="sxs-lookup"><span data-stu-id="0259e-120">Logical **NOT**</span></span><br/> |



 

<span data-ttu-id="0259e-121">y " &lt; Comparison &gt; " es lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0259e-121">and "&lt;comparison&gt;" is the following:</span></span>


```C++
(<attribute><operator><value>)
```



<span data-ttu-id="0259e-122">donde " &lt; Attribute &gt; " es el **lDAPDisplayName** del atributo que se va a evaluar, " &lt; Value &gt; " es el valor con el que se va a comparar y " &lt; Operator &gt; " es uno de los siguientes operadores de comparación.</span><span class="sxs-lookup"><span data-stu-id="0259e-122">where "&lt;attribute&gt;" is the **lDAPDisplayName** of the attribute to evaluate, "&lt;value&gt;" is the value to compare against, and "&lt;operator&gt;" is one of the following comparison operators.</span></span>



| <span data-ttu-id="0259e-123">Operator</span><span class="sxs-lookup"><span data-stu-id="0259e-123">Operator</span></span>           | <span data-ttu-id="0259e-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="0259e-124">Description</span></span>                         |
|--------------------|-------------------------------------|
| <span data-ttu-id="0259e-125">"="</span><span class="sxs-lookup"><span data-stu-id="0259e-125">"="</span></span><br/>     | <span data-ttu-id="0259e-126">Equals</span><span class="sxs-lookup"><span data-stu-id="0259e-126">Equals</span></span><br/>                   |
| <span data-ttu-id="0259e-127">"~="</span><span class="sxs-lookup"><span data-stu-id="0259e-127">"~="</span></span><br/>    | <span data-ttu-id="0259e-128">Aproximadamente es igual a</span><span class="sxs-lookup"><span data-stu-id="0259e-128">Approximately equals</span></span><br/>     |
| <span data-ttu-id="0259e-129">"<="</span><span class="sxs-lookup"><span data-stu-id="0259e-129">"<="</span></span><br/> | <span data-ttu-id="0259e-130">Menor o igual que</span><span class="sxs-lookup"><span data-stu-id="0259e-130">Less than or equal to</span></span><br/>    |
| <span data-ttu-id="0259e-131">">="</span><span class="sxs-lookup"><span data-stu-id="0259e-131">">="</span></span><br/> | <span data-ttu-id="0259e-132">Mayor o igual que</span><span class="sxs-lookup"><span data-stu-id="0259e-132">Greater than or equal to</span></span><br/> |



 

<span data-ttu-id="0259e-133">Además, dependiendo de la sintaxis de atributo, el " &lt; valor &gt; " puede contener el símbolo comodín (" \* ").</span><span class="sxs-lookup"><span data-stu-id="0259e-133">In addition, depending on the attribute syntax, the "&lt;value&gt;" may contain the wildcard symbol ("\*").</span></span> <span data-ttu-id="0259e-134">Un " &lt; valor &gt; " que solo contenga un carácter comodín comprobará la existencia de cualquier valor en " &lt; Attribute &gt; ".</span><span class="sxs-lookup"><span data-stu-id="0259e-134">A "&lt;value&gt;" that contains only a wildcard will check for the existence of any value in "&lt;attribute&gt;".</span></span> <span data-ttu-id="0259e-135">Si no se establece ningún valor para " &lt; Attribute &gt; ", se producirá un error en la prueba.</span><span class="sxs-lookup"><span data-stu-id="0259e-135">If no value is set for "&lt;attribute&gt;", the test will fail.</span></span>

<span data-ttu-id="0259e-136">Si alguno de los siguientes caracteres especiales debe aparecer en el filtro de consulta como literales, deben reemplazarse por la secuencia de escape indicada.</span><span class="sxs-lookup"><span data-stu-id="0259e-136">If any of the following special characters must appear in the query filter as literals, they must be replaced by the listed escape sequence.</span></span>



| <span data-ttu-id="0259e-137">Carácter ASCII</span><span class="sxs-lookup"><span data-stu-id="0259e-137">ASCII character</span></span>    | <span data-ttu-id="0259e-138">Sustitución de secuencias de escape</span><span class="sxs-lookup"><span data-stu-id="0259e-138">Escape sequence substitute</span></span> |
|--------------------|----------------------------|
| \*<br/>      | <span data-ttu-id="0259e-139">" \\ 2A"</span><span class="sxs-lookup"><span data-stu-id="0259e-139">"\\2a"</span></span><br/>          |
| <span data-ttu-id="0259e-140">(</span><span class="sxs-lookup"><span data-stu-id="0259e-140">(</span></span><br/>       | <span data-ttu-id="0259e-141">" \\ 28"</span><span class="sxs-lookup"><span data-stu-id="0259e-141">"\\28"</span></span><br/>          |
| <span data-ttu-id="0259e-142">)</span><span class="sxs-lookup"><span data-stu-id="0259e-142">)</span></span><br/>       | <span data-ttu-id="0259e-143">" \\ 29"</span><span class="sxs-lookup"><span data-stu-id="0259e-143">"\\29"</span></span><br/>          |
| \\<br/>      | <span data-ttu-id="0259e-144">" \\ 5C"</span><span class="sxs-lookup"><span data-stu-id="0259e-144">"\\5c"</span></span><br/>          |
| <span data-ttu-id="0259e-145">**NUL**</span><span class="sxs-lookup"><span data-stu-id="0259e-145">**NUL**</span></span><br/> | <span data-ttu-id="0259e-146">" \\ 00"</span><span class="sxs-lookup"><span data-stu-id="0259e-146">"\\00"</span></span><br/>          |



 

<span data-ttu-id="0259e-147">Además, los datos binarios arbitrarios se pueden representar mediante la sintaxis de la secuencia de escape codificando cada byte de datos binarios con la barra diagonal inversa seguida de dos dígitos hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="0259e-147">In addition, arbitrary binary data may be represented using the escape sequence syntax by encoding each byte of binary data with the backslash followed by two hexadecimal digits.</span></span> <span data-ttu-id="0259e-148">Por ejemplo, el valor de cuatro bytes 0x00000004 se codifica como " \\ 00 \\ 00 \\ 00 \\ 04" en una cadena de filtro.</span><span class="sxs-lookup"><span data-stu-id="0259e-148">For example, the four-byte value 0x00000004 is encoded as "\\00\\00\\00\\04" in a filter string.</span></span>

## <a name="examples"></a><span data-ttu-id="0259e-149">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0259e-149">Examples</span></span>

<span data-ttu-id="0259e-150">La cadena de consulta siguiente buscará todos los objetos de tipo "Computer".</span><span class="sxs-lookup"><span data-stu-id="0259e-150">The following query string will search for all objects of type "computer".</span></span>


```C++
(objectCategory=computer)
```



<span data-ttu-id="0259e-151">La siguiente cadena de consulta buscará todos los objetos de tipo "equipo" con un nombre que comience por "escritorio".</span><span class="sxs-lookup"><span data-stu-id="0259e-151">The following query string will search for all objects of type "computer" with a name that begins with "desktop".</span></span>


```C++
(&(objectCategory=computer)(name=desktop*))
```



<span data-ttu-id="0259e-152">La siguiente cadena de consulta buscará todos los objetos de tipo "Computer" con un nombre que comience por "Desktop" o un nombre que comience por "Notebook".</span><span class="sxs-lookup"><span data-stu-id="0259e-152">The following query string will search for all objects of type "computer" with a name that begins with "desktop" or a name that begins with "notebook".</span></span>


```C++
(&(objectCategory=computer)(|(name=desktop*)(name=notebook*)))
```



<span data-ttu-id="0259e-153">La cadena de consulta siguiente buscará todos los objetos de tipo "usuario" que tengan un número de teléfono particular.</span><span class="sxs-lookup"><span data-stu-id="0259e-153">The following query string will search for all objects of type "user" that have a home phone number.</span></span>


```C++
(&(objectCategory=user)(homePhone=*))
```



<span data-ttu-id="0259e-154">Para obtener más información acerca de las cadenas de filtro de consulta y ejemplos de uso, vea:</span><span class="sxs-lookup"><span data-stu-id="0259e-154">For more information about query filter strings, and usage examples, see:</span></span>

-   [<span data-ttu-id="0259e-155">Buscar objetos por clase</span><span class="sxs-lookup"><span data-stu-id="0259e-155">Finding Objects by Class</span></span>](finding-objects-by-class.md)
-   [<span data-ttu-id="0259e-156">Buscar objetos por nombre</span><span class="sxs-lookup"><span data-stu-id="0259e-156">Finding Objects by Name</span></span>](finding-objects-by-name.md)
-   [<span data-ttu-id="0259e-157">Buscar una lista de atributos para consultar</span><span class="sxs-lookup"><span data-stu-id="0259e-157">Finding a List of Attributes To Query</span></span>](finding-a-list-of-attributes-to-query.md)
-   [<span data-ttu-id="0259e-158">Comprobar la sintaxis del filtro de consulta</span><span class="sxs-lookup"><span data-stu-id="0259e-158">Checking the Query Filter Syntax</span></span>](checking-the-query-filter-syntax.md)
-   [<span data-ttu-id="0259e-159">Cómo especificar valores de comparación</span><span class="sxs-lookup"><span data-stu-id="0259e-159">How to Specify Comparison Values</span></span>](how-to-specify-comparison-values.md)

 

 





