---
description: Utilice la cláusula WHERE para restringir el ámbito de una consulta de datos, eventos o esquemas.
ms.assetid: b275f8e0-773d-422c-be21-b427e7a1fb6b
ms.tgt_platform: multiple
title: WHERE (cláusula, WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a72e68d8266b72f6e41e17c0b85766b7a58bb197
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707343"
---
# <a name="where-clause-wmi"></a>WHERE (cláusula, WMI)

Utilice la cláusula WHERE para restringir el ámbito de una consulta de datos, eventos o esquemas. Para obtener más información, vea [consultas con WQL](querying-with-wql.md). La cláusula WHERE se compone de una propiedad o una palabra clave, un operador y una constante. Todas las cláusulas WHERE deben especificar uno de los operadores predefinidos que se incluyen en el lenguaje de consulta de Instrumental de administración de Windows (WMI). Puede anexar la cláusula WHERE a la instrucción SELECT mediante una de las siguientes formas:


```sql
SELECT * FROM class WHERE property operator constant
SELECT * FROM class WHERE constant operator property
```



donde \* es el elemento que se consulta, la clase es la clase en la que se realiza la consulta, y la constante, el operador y la propiedad son la constante, el operador y la propiedad o la palabra clave que se va a usar. Para obtener más información acerca de la instrucción SELECT, vea [instrucción SELECT para consultas de datos](select-statement-for-data-queries.md), [instrucción SELECT para consultas de eventos](select-statement-for-event-queries.md)o [instrucción SELECT para consultas de esquema](select-statement-for-schema-queries.md).

El valor de la constante debe ser del tipo correcto para la propiedad. Además, el operador debe estar entre la lista de [operadores WQL](wql-operators.md)válidos. Un nombre de propiedad o una constante deben aparecer a cada lado del operador en la cláusula WHERE.

Puede usar literales de cadena, como "NTFS", en una cláusula WHERE. Si desea incluir los siguientes caracteres especiales en la cadena, primero debe escapar el carácter prefijando el carácter con una barra diagonal inversa ( \) :

-   barra diagonal inversa\\\)
-   comillas dobles ( \\ ")
-   comillas simples ( \\ ')

No se pueden usar expresiones aritméticas arbitrarias. Por ejemplo, la siguiente consulta solo devuelve las instancias de la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) que representan las unidades NTFS:


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem = "NTFS"
```



Los nombres de propiedad no pueden aparecer en ambos lados del operador. La consulta siguiente es un ejemplo de una consulta no válida:


```sql
SELECT * FROM PhysicalDisk WHERE Partitions < (4 + 7 - 2) 
    OR   (Partitions = SectorsPerTrack / 7)
```



Para la mayoría de los usos de los descriptores de clase en una cláusula WHERE, WMI marca la consulta como no válida y devuelve un error. Sin embargo, utilice el operador de punto (.) para las propiedades de tipo **Object** en WMI. Por ejemplo, la consulta siguiente es válida si prop es una propiedad válida de MyClass y es de tipo **Object**:

``` syntax
SELECT * FROM MyClass WHERE Prop.embedprop = 5
```

Las pruebas de comparación siempre distinguen entre mayúsculas y minúsculas. Es decir, las tres instrucciones siguientes se evalúan como **true**:


```sql
SELECT * FROM MyClass WHERE Prop1 = "cat"
SELECT * FROM MyClass WHERE Prop1 = "CAT"
SELECT * FROM MyClass WHERE Prop1 = "cAt"
```



Puede crear una consulta que incluya tipos de datos booleanos, pero los únicos tipos de operando booleanos válidos son los tipos =,! = y <> . El valor **true** es equivalente al número 1 y el valor **false** es equivalente al número 0. Los ejemplos siguientes son de consultas que comparan un valor booleano con los valores **true** o **false**.


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



Se pueden combinar varios grupos de propiedades, operadores y constantes en una cláusula WHERE mediante operadores lógicos y subexpresiones entre paréntesis. Cada grupo se debe combinar con los [operadores](wql-operators.md) and, or o not tal y como se muestra en las siguientes consultas. La primera consulta recupera todas las instancias de la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) con la propiedad **Name** establecida en C o D:


```sql
SELECT * FROM Win32_LogicalDisk WHERE Name = "C:" OR Name = "D:"
```



La segunda consulta recupera los discos denominados "C:" o "D:" solo si tienen una determinada cantidad de espacio libre restante y tienen sistemas de archivos NTFS:


```sql
SELECT * FROM Win32_LogicalDisk WHERE (Name = "C:" OR Name = "D:") 
    AND  FreeSpace > 2000000  AND   FileSystem = "NTFS"
```



EN este ejemplo se muestra una consulta de esquema mediante la cláusula WHERE.


```sql
SELECT * FROM meta_class WHERE __this ISA "myClassName"
```



La clase meta lo \_ identifica como una consulta de esquema, la propiedad a la que \_ \_ se identifica la clase de destino de la consulta y el [operador ISA](isa-operator-for-schema-queries.md) solicita las definiciones de las subclases de la clase de destino. Por lo tanto, la consulta anterior devuelve la definición de la clase myClassName y las definiciones de todas sus subclases.

El ejemplo siguiente es una consulta de datos que utiliza la [instrucción ASSOCIATORS of](associators-of-statement.md) con Where:


```sql
ASSOCIATORS OF {myClass.keyVal="Value1"} WHERE ClassDefsOnly
```



EN el ejemplo siguiente se muestra una consulta de esquema mediante ASSOCIATORS OF y donde:


```sql
ASSOCIATORS OF {myClass} WHERE SchemaOnly
```



El ejemplo siguiente es una consulta de datos que usa las [referencias de la instrucción](references-of-statement.md) y dónde:


```sql
REFERENCES OF {myClass.keyVal="Value1"} 
    WHERE RequiredQualifier = myQual
```



Este último ejemplo es una consulta de esquema que usa referencias de y donde:


```sql
REFERENCES OF {myClass} WHERE SchemaOnly
```



Además del formato [DateTime](date-and-time-format.md) de WMI, la cláusula WHERE de WQL admite varios formatos de fecha y hora:

-   [WQL: formatos de fecha admitidos](wql-supported-date-formats.md)
-   [WQL: formatos de hora compatibles](wql-supported-time-formats.md)

 

 
