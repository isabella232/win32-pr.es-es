---
description: Use la cláusula WHERE para restringir el ámbito de una consulta de datos, eventos o esquema.
ms.assetid: b275f8e0-773d-422c-be21-b427e7a1fb6b
ms.tgt_platform: multiple
title: Cláusula WHERE (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0587bffb1a10c4611773de8a61fdb7ac1576952
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063908"
---
# <a name="where-clause-wmi"></a>Cláusula WHERE (WMI)

Use la cláusula WHERE para restringir el ámbito de una consulta de datos, eventos o esquema. Para obtener más información, [vea Consulta con WQL.](querying-with-wql.md) La cláusula WHERE se forma de una propiedad o palabra clave, un operador y una constante. Todas las cláusulas WHERE deben especificar uno de los operadores predefinidos que se incluyen en Windows Management Instrumentation (WMI) Query Language (WQL). Puede anexar la cláusula WHERE a la instrucción SELECT mediante uno de los siguientes formularios:


```sql
SELECT * FROM class WHERE property operator constant
SELECT * FROM class WHERE constant operator property
```



donde es el elemento sobre el que se consulta, class es la clase en la que se consulta, y constant, operator y property son la constante, el operador y la propiedad o palabra clave que se van a \* usar. Para obtener más información sobre la instrucción SELECT, vea [Instrucción SELECT](select-statement-for-data-queries.md)para consultas de datos , Instrucción SELECT para consultas [de](select-statement-for-event-queries.md)eventos o Instrucción SELECT para consultas [de esquema.](select-statement-for-schema-queries.md)

El valor de la constante debe ser del tipo correcto para la propiedad . Además, el operador debe estar entre la lista de operadores [WQL válidos.](wql-operators.md) Un nombre de propiedad o una constante deben aparecer a ambos lados del operador en la cláusula WHERE.

Puede usar literales de cadena, como "NTFS", en una cláusula WHERE. Si desea incluir los siguientes caracteres especiales en la cadena, primero debe hacer un escape del carácter antefiriendo el carácter con una barra diagonal inversa ( \\ ):

-   barra diagonal inversa ( \\ \\ )
-   comillas dobles ( \\ ")
-   comillas simples ( \\ ')

No se pueden usar expresiones aritméticas arbitrarias. Por ejemplo, la consulta siguiente devuelve solo las instancias de la [**clase \_ LogicalDisk de Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) que representan unidades NTFS:


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem = "NTFS"
```



Los nombres de propiedad no pueden aparecer en ambos lados del operador . La consulta siguiente es un ejemplo de una consulta no válida:


```sql
SELECT * FROM PhysicalDisk WHERE Partitions < (4 + 7 - 2) 
    OR   (Partitions = SectorsPerTrack / 7)
```



Para la mayoría de los usos de descriptores de clase en una cláusula WHERE, WMI marca la consulta como no válida y devuelve un error. Sin embargo, use el operador punto (.) para las propiedades del objeto **de tipo** en WMI. Por ejemplo, la consulta siguiente es válida si Prop es una propiedad válida de MyClass y es el objeto de **tipo**:

``` syntax
SELECT * FROM MyClass WHERE Prop.embedprop = 5
```

Las pruebas de comparación siempre no tienen en cuenta mayúsculas de minúsculas. Es decir, las tres instrucciones siguientes se evalúan como **TRUE:**


```sql
SELECT * FROM MyClass WHERE Prop1 = "cat"
SELECT * FROM MyClass WHERE Prop1 = "CAT"
SELECT * FROM MyClass WHERE Prop1 = "cAt"
```



Puede construir una consulta que incluya tipos de datos booleanos, pero los únicos tipos de operando booleanos válidos son los tipos =, != y <> válidos. El valor **TRUE** es equivalente al número 1 y el valor **FALSE** es equivalente al número 0. Los ejemplos siguientes son de consultas que comparan un valor booleano con los valores **TRUE** o **FALSE.**


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



Los ejemplos siguientes son de consultas no válidas que intentan usar operandos no válidos.


```sql
SELECT * FROM MyClass WHERE BoolProp <= TRUE
SELECT * FROM MyClass WHERE BoolProp >= 0
SELECT * FROM MyClass WHERE BoolProp > FALSE
SELECT * FROM win32_computersystem WHERE infraredsupported >= null
```



Se pueden combinar varios grupos de propiedades, operadores y constantes en una cláusula WHERE mediante operadores lógicos y subexpresiones entre paréntesis. Cada grupo debe estar unido a los operadores AND, OR o [NOT,](wql-operators.md) como se muestra en las consultas siguientes. La primera consulta recupera todas las instancias de la clase [**\_ LogicalDisk de Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) con la **propiedad Name** establecida en C o D:


```sql
SELECT * FROM Win32_LogicalDisk WHERE Name = "C:" OR Name = "D:"
```



La segunda consulta recupera discos denominados "C:" o "D:" solo si tienen una cierta cantidad de espacio libre restante y tienen sistemas de archivos NTFS:


```sql
SELECT * FROM Win32_LogicalDisk WHERE (Name = "C:" OR Name = "D:") 
    AND  FreeSpace > 2000000  AND   FileSystem = "NTFS"
```



En este ejemplo se muestra una consulta de esquema mediante la cláusula WHERE.


```sql
SELECT * FROM meta_class WHERE __this ISA "myClassName"
```



La metaclase class identifica esto como una consulta de esquema, la propiedad denominada this identifica la clase de destino de la consulta y el operador ISA solicita definiciones para las \_ \_ \_ subclases [](isa-operator-for-schema-queries.md) de la clase de destino. Por lo tanto, la consulta anterior devuelve la definición de la clase myClassName y las definiciones de todas sus subclases.

El ejemplo siguiente es una consulta de datos que usa [la instrucción ASSOCIATORS OF](associators-of-statement.md) con WHERE:


```sql
ASSOCIATORS OF {myClass.keyVal="Value1"} WHERE ClassDefsOnly
```



En el ejemplo siguiente se muestra una consulta de esquema mediante ASSOCIATORS OF y WHERE:


```sql
ASSOCIATORS OF {myClass} WHERE SchemaOnly
```



El ejemplo siguiente es una consulta de datos que usa [la instrucción REFERENCES OF](references-of-statement.md) y WHERE:


```sql
REFERENCES OF {myClass.keyVal="Value1"} 
    WHERE RequiredQualifier = myQual
```



Este último ejemplo es una consulta de esquema que usa REFERENCES OF y WHERE:


```sql
REFERENCES OF {myClass} WHERE SchemaOnly
```



Además del formato [DATETIME de](date-and-time-format.md) WMI, la cláusula WHERE de WQL admite otros formatos de fecha y hora:

-   [Formatos de fecha admitidos por WQL](wql-supported-date-formats.md)
-   [Formatos de tiempo compatibles con WQL](wql-supported-time-formats.md)

 

 
