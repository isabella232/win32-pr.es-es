---
description: 'Las consultas de asociación de esquema usan las mismas instrucciones que se usan en las consultas de asociación de datos: ASSOCIATORS OF y REFERENCES OF.'
ms.assetid: b5fc2d86-702a-42cd-82e6-f15c905ba6aa
ms.tgt_platform: multiple
title: Asociaciones de esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461dc7c64267376baf1515ed7784da59bc789f6f1cc1171587823adb27799830
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995695"
---
# <a name="schema-associations"></a>Asociaciones de esquema

Las consultas de asociación de esquema usan las mismas instrucciones que se usan en las consultas de asociación de datos: ASSOCIATORS OF y REFERENCES OF. Sin embargo, con las consultas de asociación de datos, se devuelven instancias de clase y, con las consultas de asociación de esquema, se devuelven nombres de clases que pueden participar en relaciones de asociación. Por ejemplo, use una consulta de esquema para buscar todas las clases de asociación definidas en el esquema que hacen referencia a una clase de origen.

La sintaxis de las instrucciones ASSOCIATORS OF y REFERENCES OF es la misma para las consultas de asociación de esquema que para las consultas de asociación de datos con las siguientes excepciones:

-   El objeto de origen es una clase en lugar de una instancia de .
-   Hay una palabra clave adicional, **SchemaOnly**, que identifica la consulta como que se aplica a un esquema en lugar de a los datos.
-   La **palabra clave ClassDefsOnly** no es válida.

En el ejemplo siguiente se muestra la sintaxis completa de la instrucción ASSOCIATORS OF para una consulta de esquema. Para obtener una sintaxis detallada, [vea ASSOCIATORS OF (Instrucción](associators-of-statement.md)).


```sql
ASSOCIATORS OF {SourceClass} WHERE 
    AssocClass = AssocClassName
    RequiredAssocQualifier = QualifierName
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    ResultRole = PropertyName
    Role = PropertyName
    SchemaOnly
```



En el ejemplo siguiente se muestra una consulta que devuelve las clases **Protocol** y **Driver,** las dos clases que hacen referencia a la clase de origen.


```sql
ASSOCIATORS OF {Adapter} WHERE SchemaOnly
```



La consulta siguiente devuelve solo la **clase Driver** debido a la restricción que coloca la palabra **clave AssocClass.**


```sql
ASSOCIATORS OF {Adapter} WHERE AssocClass = AdapterDriver SchemaOnly
```



La sintaxis completa de la instrucción REFERENCES OF para una consulta de esquema es la siguiente. Para obtener una sintaxis detallada, [vea REFERENCES OF (Instrucción](references-of-statement.md)).


```sql
REFERENCES OF {SourceClass} WHERE
    ResultClass = ClassName
    Role = PropertyName
    RequiredQualifier = QualifierName
    SchemaOnly
```



> [!Note]  
> Las consultas de asociación de esquema pueden devolver objetos duplicados.

 

Por ejemplo, la consulta siguiente devolverá la clase [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) varias veces al enumerar clases en el espacio de **nombres raíz \\ cimv2.**


```sql
ASSOCIATORS OF {Win32_ComputerSystem} WHERE SchemaOnly
```



 

 
