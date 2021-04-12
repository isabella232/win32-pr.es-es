---
description: 'Las consultas de Asociación de esquema usan las mismas instrucciones que se utilizan en las consultas de Asociación de datos: ASOCIAdores de y referencias de.'
ms.assetid: b5fc2d86-702a-42cd-82e6-f15c905ba6aa
ms.tgt_platform: multiple
title: Asociaciones de esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2f0c3b753bf4657c66a635319bab7dbe435a3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278761"
---
# <a name="schema-associations"></a>Asociaciones de esquema

Las consultas de Asociación de esquema usan las mismas instrucciones que se utilizan en las consultas de Asociación de datos: ASOCIAdores de y referencias de. Sin embargo, con las consultas de Asociación de datos, se devuelven instancias de clase y con consultas de Asociación de esquema, se devuelven los nombres de las clases que pueden participar en las relaciones de asociación. Por ejemplo, utilice una consulta de esquema para buscar todas las clases de asociación definidas en el esquema que hacen referencia a una clase de origen.

La sintaxis de los ASOCIAdores de y las referencias de las instrucciones de es la misma para las consultas de Asociación de esquema que para las consultas de Asociación de datos con las excepciones siguientes:

-   El objeto de origen es una clase en lugar de una instancia de.
-   Hay una palabra clave adicional, **SchemaOnly**, que identifica la consulta como aplicable a un esquema en lugar de a los datos.
-   La palabra clave **ClassDefsOnly** no es válida.

En el ejemplo siguiente se muestra la sintaxis completa de la instrucción ASSOCIATORS OF para una consulta de esquema. Para obtener información detallada sobre la sintaxis, vea [ASSOCIATORS OF Statement](associators-of-statement.md).


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



En el ejemplo siguiente se muestra una consulta que devuelve las clases de **controlador** y de **Protocolo** , las dos clases que hacen referencia a la clase de origen.


```sql
ASSOCIATORS OF {Adapter} WHERE SchemaOnly
```



La consulta siguiente devuelve solo la clase de **controlador** debido a la restricción colocada por la palabra clave **AssocClass** .


```sql
ASSOCIATORS OF {Adapter} WHERE AssocClass = AdapterDriver SchemaOnly
```



La sintaxis completa de las referencias de la instrucción para una consulta de esquema es la siguiente. Para obtener información detallada sobre la sintaxis, vea [References of Statement](references-of-statement.md).


```sql
REFERENCES OF {SourceClass} WHERE
    ResultClass = ClassName
    Role = PropertyName
    RequiredQualifier = QualifierName
    SchemaOnly
```



> [!Note]  
> Las consultas de Asociación de esquema pueden devolver objetos duplicados.

 

Por ejemplo, la siguiente consulta devolverá la clase [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) varias veces al enumerar las clases en el espacio de nombres **root \\ cimv2** .


```sql
ASSOCIATORS OF {Win32_ComputerSystem} WHERE SchemaOnly
```



 

 
