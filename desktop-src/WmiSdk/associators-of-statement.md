---
description: Recupera todas las instancias de asociadas a una instancia de origen determinada.
ms.assetid: d6bd9643-523d-4d81-8bf1-da52ccc7524d
ms.tgt_platform: multiple
title: ASSOCIATORS OF (instrucción)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec595584efb5c32342e5bbdaa8bae309b21b29d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361126"
---
# <a name="associators-of-statement"></a><span data-ttu-id="ef983-103">ASSOCIATORS OF (instrucción)</span><span class="sxs-lookup"><span data-stu-id="ef983-103">ASSOCIATORS OF Statement</span></span>

<span data-ttu-id="ef983-104">La instrucción ASSOCIATORS OF recupera todas las instancias que están asociadas a una instancia de origen determinada.</span><span class="sxs-lookup"><span data-stu-id="ef983-104">The ASSOCIATORS OF statement retrieves all instances that are associated with a particular source instance.</span></span> <span data-ttu-id="ef983-105">Las instancias que se recuperan se conocen como puntos de conexión.</span><span class="sxs-lookup"><span data-stu-id="ef983-105">The instances that are retrieved are referred to as the endpoints.</span></span> <span data-ttu-id="ef983-106">Cada punto de conexión se devuelve tantas veces como hay asociaciones entre él y el objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="ef983-106">Each endpoint is returned as many times as there are associations between it and the source object.</span></span> <span data-ttu-id="ef983-107">Por ejemplo, suponga que hay instancias A, B, X e y. Existen dos instancias de asociación, una que vincula A y X y otra que vincula B e y. La consulta siguiente devuelve el punto de conexión único X:</span><span class="sxs-lookup"><span data-stu-id="ef983-107">For example, assume there are instances A, B, X, and Y. Two association instances exist, one that links A and X and another that links B and Y. The following query returns the single endpoint X:</span></span>


```sql
ASSOCIATORS OF {A}
```



<span data-ttu-id="ef983-108">Sin embargo, si hay otra asociación que vincula A y X, la consulta anterior devuelve dos puntos de conexión X.</span><span class="sxs-lookup"><span data-stu-id="ef983-108">However, if there is another association linking A and X, the above query returns two X endpoints.</span></span>

<span data-ttu-id="ef983-109">La sintaxis básica de la instrucción ASSOCIATORS OF es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="ef983-109">The basic syntax for the ASSOCIATORS OF statement is:</span></span>

``` syntax
ASSOCIATORS OF {ObjectPath}
```

<span data-ttu-id="ef983-110">Tenga en cuenta que las llaves forman parte de la sintaxis.</span><span class="sxs-lookup"><span data-stu-id="ef983-110">Note that the braces are part of the syntax.</span></span> <span data-ttu-id="ef983-111">Cualquier ruta de acceso de objeto válida puede utilizarse para ObjectPath.</span><span class="sxs-lookup"><span data-stu-id="ef983-111">Any valid object path can be used for ObjectPath.</span></span> <span data-ttu-id="ef983-112">Los tokens dentro de la ruta de acceso del objeto no pueden contener ningún espacio en blanco.</span><span class="sxs-lookup"><span data-stu-id="ef983-112">The tokens within the object path cannot contain any white space.</span></span> <span data-ttu-id="ef983-113">Por ejemplo, la consulta de la lista siguiente devuelve las instancias de que están asociadas con el disco lógico especificado:</span><span class="sxs-lookup"><span data-stu-id="ef983-113">For example, the query in the following list returns instances that are associated with the specified logical disk:</span></span>

<dl> <dt>

<span data-ttu-id="ef983-114"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Misma</span><span class="sxs-lookup"><span data-stu-id="ef983-114"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
```



</dd> <dt>

<span data-ttu-id="ef983-115"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Resultados</span><span class="sxs-lookup"><span data-stu-id="ef983-115"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

<span data-ttu-id="ef983-116">Al igual que con la [instrucción SELECT](select-statement-for-data-queries.md), una instrucción ASSOCIATORS of puede incluir una [cláusula WHERE](where-clause.md), pero la cláusula WHERE de una instrucción ASSOCIATORS of es muy diferente de la cláusula SELECT statementWHERE.</span><span class="sxs-lookup"><span data-stu-id="ef983-116">As with the [SELECT statement](select-statement-for-data-queries.md), an ASSOCIATORS OF statement can include a [WHERE clause](where-clause.md), but the WHERE clause for an ASSOCIATORS OF statement is very different from the SELECT statementWHERE clause.</span></span>

<span data-ttu-id="ef983-117">La [cláusula WHERE](where-clause.md) de la instrucción ASSOCIATORS of puede incluir una o varias de las siguientes palabras clave predefinidas y sus valores:</span><span class="sxs-lookup"><span data-stu-id="ef983-117">The [WHERE clause](where-clause.md) of the ASSOCIATORS OF statement can include one or more of the following predefined keywords and their values:</span></span>


```sql
ASSOCIATORS OF {ObjectPath} WHERE
    AssocClass = AssocClassName
    ClassDefsOnly
    RequiredAssocQualifier = QualifierName
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    ResultRole = PropertyName
    Role = PropertyName
```



<span data-ttu-id="ef983-118">Tenga en cuenta que las subcláusulas opcionales no se separan mediante comas.</span><span class="sxs-lookup"><span data-stu-id="ef983-118">Note that the optional subclauses are not separated by commas.</span></span>

<span data-ttu-id="ef983-119">La palabra clave **AssocClass** indica que los extremos devueltos deben estar asociados al origen a través de la clase especificada o de una de sus clases derivadas.</span><span class="sxs-lookup"><span data-stu-id="ef983-119">The **AssocClass** keyword indicates that the returned endpoints must be associated with the source through the specified class or one of its derived classes.</span></span> <span data-ttu-id="ef983-120">Por ejemplo, la consulta de la lista siguiente devuelve solo los extremos asociados al origen a través de la clase de asociación [**Win32 \_ SystemDevices**](/windows/desktop/CIMWin32Prov/win32-systemdevices) o cualquiera de sus clases derivadas:</span><span class="sxs-lookup"><span data-stu-id="ef983-120">For example, the query in the following list returns only endpoints that are associated with the source through the [**Win32\_SystemDevices**](/windows/desktop/CIMWin32Prov/win32-systemdevices) association class or any of its derived classes:</span></span>

<dl> <dt>

<span data-ttu-id="ef983-121"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Misma</span><span class="sxs-lookup"><span data-stu-id="ef983-121"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE AssocClass = Win32_SystemDevices
```



</dd> <dt>

<span data-ttu-id="ef983-122"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Resultados</span><span class="sxs-lookup"><span data-stu-id="ef983-122"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

<span data-ttu-id="ef983-123">La palabra clave **ClassDefsOnly** indica que la cláusula devuelve un conjunto de resultados de objetos de definición de clase en lugar de instancias reales de las clases.</span><span class="sxs-lookup"><span data-stu-id="ef983-123">The **ClassDefsOnly** keyword indicates that the clause returns a result set of class definition objects rather than actual instances of the classes.</span></span> <span data-ttu-id="ef983-124">Estos objetos son las definiciones de las clases a las que pertenecen las instancias de extremo.</span><span class="sxs-lookup"><span data-stu-id="ef983-124">These objects are the definitions of classes to which the endpoint instances belong.</span></span> <span data-ttu-id="ef983-125">Por ejemplo, la consulta de la lista siguiente devuelve definiciones para el [**\_ directorio Win32**](/windows/desktop/CIMWin32Prov/win32-directory) y las clases de [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) :</span><span class="sxs-lookup"><span data-stu-id="ef983-125">For example, the query in the following list returns definitions for the [**Win32\_Directory**](/windows/desktop/CIMWin32Prov/win32-directory) and [**Win32\_ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) classes:</span></span>

<dl> <dt>

<span data-ttu-id="ef983-126"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Misma</span><span class="sxs-lookup"><span data-stu-id="ef983-126"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ClassDefsOnly
```



</dd> <dt>

<span data-ttu-id="ef983-127"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Resultados</span><span class="sxs-lookup"><span data-stu-id="ef983-127"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory
```

``` syntax
Win32_ComputerSystem
Win32_DiskPartition
```

</dd> </dl>

<span data-ttu-id="ef983-128">Las palabras clave **ClassDefsOnly** y **ResultClass** se excluyen mutuamente.</span><span class="sxs-lookup"><span data-stu-id="ef983-128">The **ClassDefsOnly** and **ResultClass** keywords are mutually exclusive.</span></span> <span data-ttu-id="ef983-129">Si se usan conjuntamente, se producirá un error de consulta no válido.</span><span class="sxs-lookup"><span data-stu-id="ef983-129">Using them together causes an invalid query error.</span></span>

<span data-ttu-id="ef983-130">La palabra clave **RequiredAssocQualifier** indica que los extremos devueltos deben asociarse con el objeto de origen a través de una clase de asociación que incluye el calificador especificado.</span><span class="sxs-lookup"><span data-stu-id="ef983-130">The **RequiredAssocQualifier** keyword indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span> <span data-ttu-id="ef983-131">Este tipo de filtrado se usa para eliminar intervalos amplios de puntos de conexión a menos que los puntos de conexión estén asociados con el destino a través de un conjunto determinado de clases de asociación etiquetadas.</span><span class="sxs-lookup"><span data-stu-id="ef983-131">This type of filtering is used to eliminate broad ranges of endpoints unless the endpoints are associated with the target through a particular set of tagged association classes.</span></span> <span data-ttu-id="ef983-132">Por ejemplo, la consulta de la lista siguiente devuelve instancias de extremo si la clase de asociación incluye un calificador denominado **Association**.</span><span class="sxs-lookup"><span data-stu-id="ef983-132">For example, the query in the following list returns endpoint instances if the association class includes a qualifier called **Association**.</span></span>

<dl> <dt>

<span data-ttu-id="ef983-133"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Misma</span><span class="sxs-lookup"><span data-stu-id="ef983-133"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE RequiredAssocQualifier = Association
```



</dd> <dt>

<span data-ttu-id="ef983-134"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Resultados</span><span class="sxs-lookup"><span data-stu-id="ef983-134"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

<span data-ttu-id="ef983-135">La palabra clave **RequiredQualifier** indica que los extremos devueltos asociados al objeto de origen deben incluir el calificador especificado.</span><span class="sxs-lookup"><span data-stu-id="ef983-135">The **RequiredQualifier** keyword indicates that the returned endpoints associated with the source object must include the specified qualifier.</span></span> <span data-ttu-id="ef983-136">La palabra clave **RequiredQualifier** se puede usar para incluir determinados tipos de instancias en el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="ef983-136">The **RequiredQualifier** keyword can be used to include particular types of instances in the result set.</span></span> <span data-ttu-id="ef983-137">Por ejemplo, la consulta de la lista siguiente devuelve instancias de extremo que incluyen un calificador denominado [**configuración regional**](swbemobjectpath-locale.md).</span><span class="sxs-lookup"><span data-stu-id="ef983-137">For example, the query in the following list returns endpoint instances that include a qualifier called [**Locale**](swbemobjectpath-locale.md).</span></span>

<dl> <dt>

<span data-ttu-id="ef983-138"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Misma</span><span class="sxs-lookup"><span data-stu-id="ef983-138"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE RequiredQualifier = Locale
```



</dd> <dt>

<span data-ttu-id="ef983-139"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Resultados</span><span class="sxs-lookup"><span data-stu-id="ef983-139"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

<span data-ttu-id="ef983-140">La palabra clave **ResultClass** indica que los extremos devueltos asociados al objeto de origen deben pertenecer a la clase especificada o derivarse de ella.</span><span class="sxs-lookup"><span data-stu-id="ef983-140">The **ResultClass** keyword indicates that the returned endpoints associated with the source object must belong to or be derived from the specified class.</span></span> <span data-ttu-id="ef983-141">Por ejemplo, la consulta de la lista siguiente devuelve instancias de extremo que se derivan de la clase de [**\_ directorio CIM**](/windows/desktop/CIMWin32Prov/cim-directory) :</span><span class="sxs-lookup"><span data-stu-id="ef983-141">For example, the query in the following list returns endpoint instances that are derived from the [**CIM\_Directory**](/windows/desktop/CIMWin32Prov/cim-directory) class:</span></span>

<dl> <dt>

<span data-ttu-id="ef983-142"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Misma</span><span class="sxs-lookup"><span data-stu-id="ef983-142"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultClass = Cim_Directory
```



</dd> <dt>

<span data-ttu-id="ef983-143"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Resultados</span><span class="sxs-lookup"><span data-stu-id="ef983-143"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

<span data-ttu-id="ef983-144">Las palabras clave **ClassDefsOnly** y **ResultClass** se excluyen mutuamente.</span><span class="sxs-lookup"><span data-stu-id="ef983-144">The **ClassDefsOnly** and **ResultClass** keywords are mutually exclusive.</span></span> <span data-ttu-id="ef983-145">Si se usan conjuntamente, se producirá un error de consulta no válido.</span><span class="sxs-lookup"><span data-stu-id="ef983-145">Using them together causes an invalid query error.</span></span>

<span data-ttu-id="ef983-146">La palabra clave **ResultRole** indica que los extremos devueltos deben desempeñar un rol determinado en su asociación con el objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="ef983-146">The **ResultRole** keyword indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="ef983-147">El rol se define mediante la propiedad especificada, una propiedad de referencia de tipo [ref](references.md). Por ejemplo, la palabra clave **ResultRole** se puede utilizar para recuperar todos los extremos que tienen la propiedad **GroupComponent** en su asociación con un objeto de origen, como se muestra en la consulta siguiente.</span><span class="sxs-lookup"><span data-stu-id="ef983-147">The role is defined by the specified property, a reference property of type [ref](references.md). For example, the **ResultRole** keyword can be used to retrieve all endpoints that have the **GroupComponent** property in their association with a source object, as the following query illustrates.</span></span>

<dl> <dt>

<span data-ttu-id="ef983-148"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Misma</span><span class="sxs-lookup"><span data-stu-id="ef983-148"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultRole = GroupComponent
```



</dd> <dt>

<span data-ttu-id="ef983-149"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Resultados</span><span class="sxs-lookup"><span data-stu-id="ef983-149"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

<span data-ttu-id="ef983-150">La palabra clave **role** indica que los extremos devueltos participan en una asociación con el objeto de origen donde el objeto de origen desempeña un rol determinado.</span><span class="sxs-lookup"><span data-stu-id="ef983-150">The **Role** keyword indicates that the returned endpoints participate in an association with the source object where the source object plays a particular role.</span></span> <span data-ttu-id="ef983-151">El rol se define mediante la propiedad especificada, una propiedad de referencia de tipo **ref**. Por ejemplo, la palabra clave **role** se puede usar para recuperar todos los extremos asociados a un objeto de origen que tienen la propiedad **GroupComponent** , como se muestra en la consulta siguiente.</span><span class="sxs-lookup"><span data-stu-id="ef983-151">The role is defined by the specified property, a reference property of type **ref**. For example, the **Role** keyword can be used to retrieve all endpoints associated with a source object that have the **GroupComponent** property, as the following query illustrates.</span></span>

<dl> <dt>

<span data-ttu-id="ef983-152"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Misma</span><span class="sxs-lookup"><span data-stu-id="ef983-152"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE Role = GroupComponent
```



</dd> <dt>

<span data-ttu-id="ef983-153"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Resultados</span><span class="sxs-lookup"><span data-stu-id="ef983-153"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

> [!Note]  
> <span data-ttu-id="ef983-154">Las consultas complejas no pueden usar "and" o "or" para separar palabras clave para los ASOCIAdores de y [las referencias de](references-of-statement.md) instrucciones.</span><span class="sxs-lookup"><span data-stu-id="ef983-154">Complex queries cannot use "And" or "Or" to separate keywords for ASSOCIATORS OF and [REFERENCES OF](references-of-statement.md) statements.</span></span> <span data-ttu-id="ef983-155">Además, el signo igual es el único operador válido que se puede usar en dichas consultas.</span><span class="sxs-lookup"><span data-stu-id="ef983-155">Furthermore, the equal sign is the only valid operator that can be used in such queries.</span></span> <span data-ttu-id="ef983-156">Por ejemplo, la consulta siguiente es válida:</span><span class="sxs-lookup"><span data-stu-id="ef983-156">For example, the following query is valid:</span></span>

 


```sql
ASSOCIATORS OF {win32_LogicalDisk="C:"} WHERE resultClass = Win32_Directory requiredQualifier = Dynamic
```



> [!Note]  
> <span data-ttu-id="ef983-157">Los ejemplos siguientes no son válidos.</span><span class="sxs-lookup"><span data-stu-id="ef983-157">The next examples are not valid.</span></span> <span data-ttu-id="ef983-158">En el primer ejemplo no se usa el signo igual y el segundo ejemplo intenta usar erróneamente la palabra clave **y** .</span><span class="sxs-lookup"><span data-stu-id="ef983-158">The first example does not use the equal sign and the second example erroneously attempts to use the **AND** keyword.</span></span>

 

``` syntax
Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory requiredQualifier <> Dynamic

Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory AND requiredQualifier = Dynamic
```

 

 
