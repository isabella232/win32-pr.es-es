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
# <a name="associators-of-statement"></a>ASSOCIATORS OF (instrucción)

La instrucción ASSOCIATORS OF recupera todas las instancias que están asociadas a una instancia de origen determinada. Las instancias que se recuperan se conocen como puntos de conexión. Cada punto de conexión se devuelve tantas veces como hay asociaciones entre él y el objeto de origen. Por ejemplo, suponga que hay instancias A, B, X e y. Existen dos instancias de asociación, una que vincula A y X y otra que vincula B e y. La consulta siguiente devuelve el punto de conexión único X:


```sql
ASSOCIATORS OF {A}
```



Sin embargo, si hay otra asociación que vincula A y X, la consulta anterior devuelve dos puntos de conexión X.

La sintaxis básica de la instrucción ASSOCIATORS OF es la siguiente:

``` syntax
ASSOCIATORS OF {ObjectPath}
```

Tenga en cuenta que las llaves forman parte de la sintaxis. Cualquier ruta de acceso de objeto válida puede utilizarse para ObjectPath. Los tokens dentro de la ruta de acceso del objeto no pueden contener ningún espacio en blanco. Por ejemplo, la consulta de la lista siguiente devuelve las instancias de que están asociadas con el disco lógico especificado:

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Misma
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Resultados
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

Al igual que con la [instrucción SELECT](select-statement-for-data-queries.md), una instrucción ASSOCIATORS of puede incluir una [cláusula WHERE](where-clause.md), pero la cláusula WHERE de una instrucción ASSOCIATORS of es muy diferente de la cláusula SELECT statementWHERE.

La [cláusula WHERE](where-clause.md) de la instrucción ASSOCIATORS of puede incluir una o varias de las siguientes palabras clave predefinidas y sus valores:


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



Tenga en cuenta que las subcláusulas opcionales no se separan mediante comas.

La palabra clave **AssocClass** indica que los extremos devueltos deben estar asociados al origen a través de la clase especificada o de una de sus clases derivadas. Por ejemplo, la consulta de la lista siguiente devuelve solo los extremos asociados al origen a través de la clase de asociación [**Win32 \_ SystemDevices**](/windows/desktop/CIMWin32Prov/win32-systemdevices) o cualquiera de sus clases derivadas:

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Misma
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE AssocClass = Win32_SystemDevices
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Resultados
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

La palabra clave **ClassDefsOnly** indica que la cláusula devuelve un conjunto de resultados de objetos de definición de clase en lugar de instancias reales de las clases. Estos objetos son las definiciones de las clases a las que pertenecen las instancias de extremo. Por ejemplo, la consulta de la lista siguiente devuelve definiciones para el [**\_ directorio Win32**](/windows/desktop/CIMWin32Prov/win32-directory) y las clases de [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) :

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Misma
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ClassDefsOnly
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Resultados
</dt> <dd>

``` syntax
Win32_Directory
```

``` syntax
Win32_ComputerSystem
Win32_DiskPartition
```

</dd> </dl>

Las palabras clave **ClassDefsOnly** y **ResultClass** se excluyen mutuamente. Si se usan conjuntamente, se producirá un error de consulta no válido.

La palabra clave **RequiredAssocQualifier** indica que los extremos devueltos deben asociarse con el objeto de origen a través de una clase de asociación que incluye el calificador especificado. Este tipo de filtrado se usa para eliminar intervalos amplios de puntos de conexión a menos que los puntos de conexión estén asociados con el destino a través de un conjunto determinado de clases de asociación etiquetadas. Por ejemplo, la consulta de la lista siguiente devuelve instancias de extremo si la clase de asociación incluye un calificador denominado **Association**.

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Misma
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE RequiredAssocQualifier = Association
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Resultados
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

La palabra clave **RequiredQualifier** indica que los extremos devueltos asociados al objeto de origen deben incluir el calificador especificado. La palabra clave **RequiredQualifier** se puede usar para incluir determinados tipos de instancias en el conjunto de resultados. Por ejemplo, la consulta de la lista siguiente devuelve instancias de extremo que incluyen un calificador denominado [**configuración regional**](swbemobjectpath-locale.md).

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Misma
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE RequiredQualifier = Locale
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Resultados
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

La palabra clave **ResultClass** indica que los extremos devueltos asociados al objeto de origen deben pertenecer a la clase especificada o derivarse de ella. Por ejemplo, la consulta de la lista siguiente devuelve instancias de extremo que se derivan de la clase de [**\_ directorio CIM**](/windows/desktop/CIMWin32Prov/cim-directory) :

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Misma
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultClass = Cim_Directory
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Resultados
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

Las palabras clave **ClassDefsOnly** y **ResultClass** se excluyen mutuamente. Si se usan conjuntamente, se producirá un error de consulta no válido.

La palabra clave **ResultRole** indica que los extremos devueltos deben desempeñar un rol determinado en su asociación con el objeto de origen. El rol se define mediante la propiedad especificada, una propiedad de referencia de tipo [ref](references.md). Por ejemplo, la palabra clave **ResultRole** se puede utilizar para recuperar todos los extremos que tienen la propiedad **GroupComponent** en su asociación con un objeto de origen, como se muestra en la consulta siguiente.

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Misma
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultRole = GroupComponent
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Resultados
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

La palabra clave **role** indica que los extremos devueltos participan en una asociación con el objeto de origen donde el objeto de origen desempeña un rol determinado. El rol se define mediante la propiedad especificada, una propiedad de referencia de tipo **ref**. Por ejemplo, la palabra clave **role** se puede usar para recuperar todos los extremos asociados a un objeto de origen que tienen la propiedad **GroupComponent** , como se muestra en la consulta siguiente.

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Misma
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE Role = GroupComponent
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Resultados
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

> [!Note]  
> Las consultas complejas no pueden usar "and" o "or" para separar palabras clave para los ASOCIAdores de y [las referencias de](references-of-statement.md) instrucciones. Además, el signo igual es el único operador válido que se puede usar en dichas consultas. Por ejemplo, la consulta siguiente es válida:

 


```sql
ASSOCIATORS OF {win32_LogicalDisk="C:"} WHERE resultClass = Win32_Directory requiredQualifier = Dynamic
```



> [!Note]  
> Los ejemplos siguientes no son válidos. En el primer ejemplo no se usa el signo igual y el segundo ejemplo intenta usar erróneamente la palabra clave **y** .

 

``` syntax
Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory requiredQualifier <> Dynamic

Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory AND requiredQualifier = Dynamic
```

 

 
