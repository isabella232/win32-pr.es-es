---
description: Use la cláusula WHERE para restringir el ámbito de una consulta de datos, eventos o esquema.
ms.assetid: b275f8e0-773d-422c-be21-b427e7a1fb6b
ms.tgt_platform: multiple
title: Cláusula WHERE (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0587bffb1a10c4611773de8a61fdb7ac1576952
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386733"
---
# <a name="where-clause-wmi"></a><span data-ttu-id="ed73b-103">Cláusula WHERE (WMI)</span><span class="sxs-lookup"><span data-stu-id="ed73b-103">WHERE Clause (WMI)</span></span>

<span data-ttu-id="ed73b-104">Use la cláusula WHERE para restringir el ámbito de una consulta de datos, eventos o esquema.</span><span class="sxs-lookup"><span data-stu-id="ed73b-104">Use the WHERE clause to narrow the scope of a data, event, or schema query.</span></span> <span data-ttu-id="ed73b-105">Para obtener más información, [vea Consulta con WQL.](querying-with-wql.md)</span><span class="sxs-lookup"><span data-stu-id="ed73b-105">For more information, see [Querying with WQL](querying-with-wql.md).</span></span> <span data-ttu-id="ed73b-106">La cláusula WHERE se forma de una propiedad o palabra clave, un operador y una constante.</span><span class="sxs-lookup"><span data-stu-id="ed73b-106">The WHERE clause is made up of a property or keyword, an operator, and a constant.</span></span> <span data-ttu-id="ed73b-107">Todas las cláusulas WHERE deben especificar uno de los operadores predefinidos que se incluyen en el lenguaje de consulta (WQL) Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ed73b-107">All WHERE clauses must specify one of the predefined operators that are included in the Windows Management Instrumentation (WMI) Query Language (WQL).</span></span> <span data-ttu-id="ed73b-108">Puede anexar la cláusula WHERE a la instrucción SELECT mediante uno de los siguientes formularios:</span><span class="sxs-lookup"><span data-stu-id="ed73b-108">You can append the WHERE clause to the SELECT statement using one of the following forms:</span></span>


```sql
SELECT * FROM class WHERE property operator constant
SELECT * FROM class WHERE constant operator property
```



<span data-ttu-id="ed73b-109">donde es el elemento sobre el que se consulta, class es la clase en la que se consulta, y constant, operator y property son la constante, el operador y la propiedad o palabra clave que se van a \* usar.</span><span class="sxs-lookup"><span data-stu-id="ed73b-109">where \* is the item queried about, class is the class in which to query, and constant, operator, and property are the constant, operator, and property or keyword to use.</span></span> <span data-ttu-id="ed73b-110">Para obtener más información sobre la instrucción SELECT, vea [Instrucción SELECT](select-statement-for-data-queries.md)para consultas de datos , Instrucción SELECT para consultas [de](select-statement-for-event-queries.md)eventos o Instrucción SELECT para consultas [de esquema.](select-statement-for-schema-queries.md)</span><span class="sxs-lookup"><span data-stu-id="ed73b-110">For more information about the SELECT statement, see [SELECT Statement for Data Queries](select-statement-for-data-queries.md), [SELECT Statement for Event Queries](select-statement-for-event-queries.md), or [SELECT Statement for Schema Queries](select-statement-for-schema-queries.md).</span></span>

<span data-ttu-id="ed73b-111">El valor de la constante debe ser del tipo correcto para la propiedad .</span><span class="sxs-lookup"><span data-stu-id="ed73b-111">The value of the constant must be of the correct type for the property.</span></span> <span data-ttu-id="ed73b-112">Además, el operador debe estar entre la lista de operadores [WQL válidos.](wql-operators.md)</span><span class="sxs-lookup"><span data-stu-id="ed73b-112">Moreover, the operator must be among the list of valid [WQL operators](wql-operators.md).</span></span> <span data-ttu-id="ed73b-113">Un nombre de propiedad o una constante deben aparecer a ambos lados del operador en la cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="ed73b-113">Either a property name or a constant must appear on either side of the operator in the WHERE clause.</span></span>

<span data-ttu-id="ed73b-114">Puede usar literales de cadena, como "NTFS", en una cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="ed73b-114">You may use string literals, such as "NTFS", in a WHERE clause.</span></span> <span data-ttu-id="ed73b-115">Si desea incluir los siguientes caracteres especiales en la cadena, primero debe usar como prefijo el carácter con una barra diagonal inversa ( \\ ):</span><span class="sxs-lookup"><span data-stu-id="ed73b-115">If you wish to include the following special characters in your string, you must first escape the character by prefixing the character with a backslash (\\):</span></span>

-   <span data-ttu-id="ed73b-116">barra diagonal inversa ( \\ \\ )</span><span class="sxs-lookup"><span data-stu-id="ed73b-116">backslash (\\\\)</span></span>
-   <span data-ttu-id="ed73b-117">comillas dobles ( \\ ")</span><span class="sxs-lookup"><span data-stu-id="ed73b-117">double quotes (\\")</span></span>
-   <span data-ttu-id="ed73b-118">comillas simples ( \\ ')</span><span class="sxs-lookup"><span data-stu-id="ed73b-118">single quotes (\\')</span></span>

<span data-ttu-id="ed73b-119">No se pueden usar expresiones aritméticas arbitrarias.</span><span class="sxs-lookup"><span data-stu-id="ed73b-119">Arbitrary arithmetic expressions cannot be used.</span></span> <span data-ttu-id="ed73b-120">Por ejemplo, la consulta siguiente devuelve solo las instancias de la clase [**\_ LogicalDisk de Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) que representan unidades NTFS:</span><span class="sxs-lookup"><span data-stu-id="ed73b-120">For example, the following query returns only the instances of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class that represent NTFS drives:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem = "NTFS"
```



<span data-ttu-id="ed73b-121">Los nombres de propiedad no pueden aparecer en ambos lados del operador .</span><span class="sxs-lookup"><span data-stu-id="ed73b-121">Property names cannot appear on both sides of the operator.</span></span> <span data-ttu-id="ed73b-122">La consulta siguiente es un ejemplo de una consulta no válida:</span><span class="sxs-lookup"><span data-stu-id="ed73b-122">The following query is an example of an invalid query:</span></span>


```sql
SELECT * FROM PhysicalDisk WHERE Partitions < (4 + 7 - 2) 
    OR   (Partitions = SectorsPerTrack / 7)
```



<span data-ttu-id="ed73b-123">Para la mayoría de los usos de descriptores de clase en una cláusula WHERE, WMI marca la consulta como no válida y devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="ed73b-123">For most uses of class descriptors in a WHERE clause, WMI flags the query as invalid and returns an error.</span></span> <span data-ttu-id="ed73b-124">Sin embargo, use el operador punto (.) para las propiedades del objeto **de tipo** en WMI.</span><span class="sxs-lookup"><span data-stu-id="ed73b-124">However, use the dot (.) operator for properties of type **object** in WMI.</span></span> <span data-ttu-id="ed73b-125">Por ejemplo, la consulta siguiente es válida si Prop es una propiedad válida de MyClass y es el objeto de **tipo**:</span><span class="sxs-lookup"><span data-stu-id="ed73b-125">For example, the following query is valid if Prop is a valid property of MyClass and is type **object**:</span></span>

``` syntax
SELECT * FROM MyClass WHERE Prop.embedprop = 5
```

<span data-ttu-id="ed73b-126">Las pruebas de comparación siempre no tienen en cuenta mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="ed73b-126">Comparison tests are always case-insensitive.</span></span> <span data-ttu-id="ed73b-127">Es decir, las tres instrucciones siguientes se evalúan como **TRUE:**</span><span class="sxs-lookup"><span data-stu-id="ed73b-127">That is, the following three statements all evaluate to **TRUE**:</span></span>


```sql
SELECT * FROM MyClass WHERE Prop1 = "cat"
SELECT * FROM MyClass WHERE Prop1 = "CAT"
SELECT * FROM MyClass WHERE Prop1 = "cAt"
```



<span data-ttu-id="ed73b-128">Puede construir una consulta que incluya tipos de datos booleanos, pero los únicos tipos de operando booleanos válidos son los tipos =, != y <> válidos.</span><span class="sxs-lookup"><span data-stu-id="ed73b-128">You can construct a query that includes Boolean data types, but the only valid Boolean operand types are the =, != and <> types.</span></span> <span data-ttu-id="ed73b-129">El valor **TRUE** es equivalente al número 1 y el valor **FALSE** es equivalente al número 0.</span><span class="sxs-lookup"><span data-stu-id="ed73b-129">The value **TRUE** is equivalent to the number 1, and the value **FALSE** is equivalent to the number 0.</span></span> <span data-ttu-id="ed73b-130">Los ejemplos siguientes son de consultas que comparan un valor booleano con los valores **TRUE** o **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="ed73b-130">The following examples are of queries that compare a Boolean value against the values **TRUE** or **FALSE**.</span></span>


```sql
SELECT * FROM MyClass WHERE BoolProp = 1
SELECT * FROM MyClass WHERE BoolProp = TRUE
SELECT * FROM MyClass WHERE BoolProp <> FALSE
SELECT * FROM MyClass WHERE BoolProp = 0
SELECT * FROM MyClass WHERE BoolProp = FALSE
SELECT * FROM MyClass WHERE BoolProp != 1
SELECT * FROM MyClass WHERE BoolProp != FALSE
SELECT * FROM MyClass WHERE BoolProp <> FALSE
```



<span data-ttu-id="ed73b-131">Los ejemplos siguientes son de consultas no válidas que intentan usar operandos no válidos.</span><span class="sxs-lookup"><span data-stu-id="ed73b-131">The following examples are of invalid queries that attempt to use invalid operands.</span></span>


```sql
SELECT * FROM MyClass WHERE BoolProp <= TRUE
SELECT * FROM MyClass WHERE BoolProp >= 0
SELECT * FROM MyClass WHERE BoolProp > FALSE
SELECT * FROM win32_computersystem WHERE infraredsupported >= null
```



<span data-ttu-id="ed73b-132">Se pueden combinar varios grupos de propiedades, operadores y constantes en una cláusula WHERE mediante operadores lógicos y subexpresiones entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="ed73b-132">Multiple groups of properties, operators, and constants can be combined in a WHERE clause using logical operators and parenthetical subexpressions.</span></span> <span data-ttu-id="ed73b-133">Cada grupo debe estar unido a los operadores AND, OR o [NOT,](wql-operators.md) como se muestra en las consultas siguientes.</span><span class="sxs-lookup"><span data-stu-id="ed73b-133">Each group must be joined with the AND, OR, or NOT [operators](wql-operators.md) as is shown in the following queries.</span></span> <span data-ttu-id="ed73b-134">La primera consulta recupera todas las instancias de la clase [**\_ LogicalDisk de Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) con la **propiedad Name** establecida en C o D:</span><span class="sxs-lookup"><span data-stu-id="ed73b-134">The first query retrieves all instances of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class with the **Name** property set to either C or D:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE Name = "C:" OR Name = "D:"
```



<span data-ttu-id="ed73b-135">La segunda consulta recupera discos denominados "C:" o "D:" solo si tienen una cierta cantidad de espacio libre restante y tienen sistemas de archivos NTFS:</span><span class="sxs-lookup"><span data-stu-id="ed73b-135">The second query retrieves disks named "C:" or "D:" only if they have a certain amount of free space remaining and have NTFS file systems:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE (Name = "C:" OR Name = "D:") 
    AND  FreeSpace > 2000000  AND   FileSystem = "NTFS"
```



<span data-ttu-id="ed73b-136">En este ejemplo se muestra una consulta de esquema mediante la cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="ed73b-136">This example shows a schema query using the WHERE clause.</span></span>


```sql
SELECT * FROM meta_class WHERE __this ISA "myClassName"
```



<span data-ttu-id="ed73b-137">La metaclase class identifica esto como una consulta de esquema, la propiedad denominada this identifica la clase de destino de la consulta y el operador ISA solicita definiciones para las \_ \_ \_ subclases [](isa-operator-for-schema-queries.md) de la clase de destino.</span><span class="sxs-lookup"><span data-stu-id="ed73b-137">The class meta\_class identifies this as a schema query, the property called \_\_this identifies the target class of the query and the [ISA operator](isa-operator-for-schema-queries.md) requests definitions for the subclasses of the target class.</span></span> <span data-ttu-id="ed73b-138">Por lo tanto, la consulta anterior devuelve la definición de la clase myClassName y las definiciones de todas sus subclases.</span><span class="sxs-lookup"><span data-stu-id="ed73b-138">Therefore, the preceding query returns the definition for the myClassName class and definitions for all of its subclasses.</span></span>

<span data-ttu-id="ed73b-139">El ejemplo siguiente es una consulta de datos que usa [la instrucción ASSOCIATORS OF](associators-of-statement.md) con WHERE:</span><span class="sxs-lookup"><span data-stu-id="ed73b-139">The following example is a data query using the [ASSOCIATORS OF statement](associators-of-statement.md) with WHERE:</span></span>


```sql
ASSOCIATORS OF {myClass.keyVal="Value1"} WHERE ClassDefsOnly
```



<span data-ttu-id="ed73b-140">En el ejemplo siguiente se muestra una consulta de esquema mediante ASSOCIATORS OF y WHERE:</span><span class="sxs-lookup"><span data-stu-id="ed73b-140">The next example shows a schema query using ASSOCIATORS OF and WHERE:</span></span>


```sql
ASSOCIATORS OF {myClass} WHERE SchemaOnly
```



<span data-ttu-id="ed73b-141">El ejemplo siguiente es una consulta de datos que usa [la instrucción REFERENCES OF](references-of-statement.md) y WHERE:</span><span class="sxs-lookup"><span data-stu-id="ed73b-141">The following example is a data query using the [REFERENCES OF statement](references-of-statement.md) and WHERE:</span></span>


```sql
REFERENCES OF {myClass.keyVal="Value1"} 
    WHERE RequiredQualifier = myQual
```



<span data-ttu-id="ed73b-142">Este último ejemplo es una consulta de esquema que usa REFERENCES OF y WHERE:</span><span class="sxs-lookup"><span data-stu-id="ed73b-142">This last example is a schema query using REFERENCES OF and WHERE:</span></span>


```sql
REFERENCES OF {myClass} WHERE SchemaOnly
```



<span data-ttu-id="ed73b-143">Además del formato [DATETIME de](date-and-time-format.md) WMI, la cláusula WHERE de WQL admite otros formatos de fecha y hora:</span><span class="sxs-lookup"><span data-stu-id="ed73b-143">In addition to the WMI [DATETIME](date-and-time-format.md) format, the WQL WHERE clause supports several other date and time formats:</span></span>

-   [<span data-ttu-id="ed73b-144">Formatos de fecha admitidos por WQL</span><span class="sxs-lookup"><span data-stu-id="ed73b-144">WQL-Supported Date Formats</span></span>](wql-supported-date-formats.md)
-   [<span data-ttu-id="ed73b-145">Formatos de tiempo compatibles con WQL</span><span class="sxs-lookup"><span data-stu-id="ed73b-145">WQL-Supported Time Formats</span></span>](wql-supported-time-formats.md)

 

 
