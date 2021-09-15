---
description: Recupera todas las instancias asociadas a una instancia de origen determinada.
ms.assetid: d6bd9643-523d-4d81-8bf1-da52ccc7524d
ms.tgt_platform: multiple
title: ASSOCIATORS OF (Instrucción)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec595584efb5c32342e5bbdaa8bae309b21b29d2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568080"
---
# <a name="associators-of-statement"></a>ASSOCIATORS OF (Instrucción)

La instrucción ASSOCIATORS OF recupera todas las instancias asociadas a una instancia de origen determinada. Las instancias que se recuperan se conocen como los puntos de conexión. Cada punto de conexión se devuelve tantas veces como haya asociaciones entre él y el objeto de origen. Por ejemplo, suponga que hay instancias A, B, X e Y. Existen dos instancias de asociación, una que vincula A y X y otra que vincula B e Y. La consulta siguiente devuelve el único punto de conexión X:


```sql
ASSOCIATORS OF {A}
```



Sin embargo, si hay otra asociación que vincula A y X, la consulta anterior devuelve dos puntos de conexión X.

La sintaxis básica de la instrucción ASSOCIATORS OF es:

``` syntax
ASSOCIATORS OF {ObjectPath}
```

Tenga en cuenta que las llaves forman parte de la sintaxis. Se puede usar cualquier ruta de acceso de objeto válida para ObjectPath. Los tokens de la ruta de acceso del objeto no pueden contener ningún espacio en blanco. Por ejemplo, la consulta de la lista siguiente devuelve instancias asociadas al disco lógico especificado:

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Consulta:
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Resultados:
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

Al igual que con la instrucción [SELECT](select-statement-for-data-queries.md), una instrucción ASSOCIATORS OF puede incluir una cláusula [WHERE](where-clause.md), pero la cláusula WHERE para una instrucción ASSOCIATORS OF es muy diferente de la cláusula SELECT statementWHERE.

La [cláusula WHERE](where-clause.md) de la instrucción ASSOCIATORS OF puede incluir una o varias de las siguientes palabras clave predefinidas y sus valores:


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



Tenga en cuenta que las subclauses opcionales no están separadas por comas.

La **palabra clave AssocClass** indica que los puntos de conexión devueltos deben asociarse al origen a través de la clase especificada o de una de sus clases derivadas. Por ejemplo, la consulta de la lista siguiente devuelve solo los puntos de conexión asociados al origen a través de la clase de asociación [**\_ SystemDevices de Win32**](/windows/desktop/CIMWin32Prov/win32-systemdevices) o cualquiera de sus clases derivadas:

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Consulta:
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE AssocClass = Win32_SystemDevices
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Resultados:
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

La **palabra clave ClassDefsOnly** indica que la cláusula devuelve un conjunto de resultados de objetos de definición de clase en lugar de instancias reales de las clases. Estos objetos son las definiciones de clases a las que pertenecen las instancias de punto de conexión. Por ejemplo, la consulta de la lista siguiente devuelve definiciones para las clases [**Directorio Win32 \_**](/windows/desktop/CIMWin32Prov/win32-directory) y [**Equipo Win32Sistema: \_**](/windows/desktop/CIMWin32Prov/win32-computersystem)

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Consulta:
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ClassDefsOnly
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Resultados:
</dt> <dd>

``` syntax
Win32_Directory
```

``` syntax
Win32_ComputerSystem
Win32_DiskPartition
```

</dd> </dl>

Las **palabras clave ClassDefsOnly** **y ResultClass** son mutuamente excluyentes. Si se usan juntos, se produce un error de consulta no válido.

La **palabra clave RequiredAssocQualifier** indica que los puntos de conexión devueltos deben asociarse al objeto de origen a través de una clase de asociación que incluya el calificador especificado. Este tipo de filtrado se usa para eliminar amplios intervalos de puntos de conexión a menos que los puntos de conexión estén asociados al destino a través de un conjunto determinado de clases de asociación etiquetadas. Por ejemplo, la consulta de la lista siguiente devuelve instancias de punto de conexión si la clase de asociación incluye un calificador llamado **Association**.

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Consulta:
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE RequiredAssocQualifier = Association
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Resultados:
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

La **palabra clave RequiredQualifier** indica que los puntos de conexión devueltos asociados al objeto de origen deben incluir el calificador especificado. La **palabra clave RequiredQualifier** se puede usar para incluir determinados tipos de instancias en el conjunto de resultados. Por ejemplo, la consulta de la lista siguiente devuelve instancias de punto de conexión que incluyen un calificador denominado [**Configuración regional.**](swbemobjectpath-locale.md)

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Consulta:
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE RequiredQualifier = Locale
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Resultados:
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

La **palabra clave ResultClass** indica que los puntos de conexión devueltos asociados al objeto de origen deben pertenecer o derivarse de la clase especificada. Por ejemplo, la consulta de la lista siguiente devuelve instancias de punto de conexión que se derivan de la [**clase \_ de directorio CIM:**](/windows/desktop/CIMWin32Prov/cim-directory)

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Consulta:
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultClass = Cim_Directory
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Resultados:
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

Las **palabras clave ClassDefsOnly** **y ResultClass** son mutuamente excluyentes. Si se usan juntos, se produce un error de consulta no válido.

La **palabra clave ResultRole** indica que los puntos de conexión devueltos deben desempeñar un rol determinado en su asociación con el objeto de origen. El rol se define mediante la propiedad especificada, una propiedad de referencia de tipo [ref](references.md). Por ejemplo, la palabra clave **ResultRole** se puede usar para recuperar todos los puntos de conexión que tienen la propiedad **GroupComponent** en su asociación con un objeto de origen, como se muestra en la consulta siguiente.

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Consulta:
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultRole = GroupComponent
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Resultados:
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

La **palabra clave Role** indica que los puntos de conexión devueltos participan en una asociación con el objeto de origen donde el objeto de origen desempeña un rol determinado. El rol se define mediante la propiedad especificada, una propiedad de referencia de tipo **ref**. Por ejemplo, la palabra clave **Role** se puede usar para recuperar todos los puntos de conexión asociados a un objeto de origen que tienen la **propiedad GroupComponent,** como se muestra en la consulta siguiente.

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Consulta:
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE Role = GroupComponent
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Resultados:
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

> [!Note]  
> Las consultas complejas no pueden usar "And" u "Or" para separar palabras clave para las instrucciones ASSOCIATORS OF y [REFERENCES OF.](references-of-statement.md) Además, el signo igual es el único operador válido que se puede usar en estas consultas. Por ejemplo, la consulta siguiente es válida:

 


```sql
ASSOCIATORS OF {win32_LogicalDisk="C:"} WHERE resultClass = Win32_Directory requiredQualifier = Dynamic
```



> [!Note]  
> Los ejemplos siguientes no son válidos. El primer ejemplo no usa el signo igual y el segundo ejemplo intenta erróneamente usar la **palabra clave AND.**

 

``` syntax
Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory requiredQualifier <> Dynamic

Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory AND requiredQualifier = Dynamic
```

 

 
