---
description: La instrucción REFERENCES OF recupera todas las instancias de asociación que hacen referencia a una instancia de origen determinada.
ms.assetid: 674be546-e7fd-4150-9d7c-2888d24bf1b3
ms.tgt_platform: multiple
title: REFERENCES OF (Instrucción)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c7cc624a1e91220fc6bfc89ef0a75878a9cfb1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063940"
---
# <a name="references-of-statement"></a>REFERENCES OF (Instrucción)

La instrucción REFERENCES OF recupera todas las instancias de asociación que hacen referencia a una instancia de origen determinada. La instrucción REFERENCES OF es similar a la instrucción ASSOCIATORS OF en su sintaxis. Sin embargo, en lugar de recuperar instancias de punto de conexión, recupera las instancias de asociación que intervienen.

La cláusula REFERENCES OF WHERE puede incluir una o varias de las siguientes palabras clave predefinidas y sus valores:


```sql
REFERENCES OF {SourceObject} WHERE 
    ClassDefsOnly
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    Role = PropertyName
```



Para especificar un objeto de origen, use cualquier ruta de acceso de objeto válida para SourceObject. Al igual que con la instrucción SELECT, la cláusula WHERE es opcional y se usa para definir aún más la consulta. Es decir, la siguiente instrucción es perfectamente válida:


```sql
REFERENCES OF {Adapter="AHA-294X"}
```



La **palabra clave ClassDefsOnly** indica que la instrucción devuelve un conjunto de resultados de objetos de definición de clase en lugar de instancias reales de las clases de asociación. Estos objetos contienen definiciones de clases a las que pertenecen las instancias que hacen referencia al objeto de origen. Por ejemplo, la siguiente instrucción devuelve definiciones para las clases **AdapterDriver** y **AdapterProtocol:**


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE ClassDefsOnly
```



La **palabra clave RequiredQualifier** indica que los objetos de asociación devueltos deben incluir el calificador especificado. La **palabra clave RequiredQualifier** se puede usar para incluir instancias concretas de asociaciones en el conjunto de resultados. Por ejemplo, la siguiente instrucción devuelve instancias de asociación que incluyen un calificador denominado **AdapterTag**:


```sql
REFERENCES OF {Adapter="AHA-294X"}  WHERE RequiredQualifier = AdapterTag
```



La **palabra clave ResultClass** indica que los objetos de asociación devueltos deben pertenecer o derivarse de la clase especificada. Por ejemplo, la siguiente instrucción devuelve asociaciones de la **clase AdapterDriver** o subclases de **AdapterDriver**:


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE ResultClass = AdapterDriver
```



Las **palabras clave ClassDefsOnly** **y ResultClass** son mutuamente excluyentes. Si se usan juntos, se produce un error de consulta no válido.

La **palabra clave Role** indica que las asociaciones devueltas son solo aquellas en las que el objeto de origen desempeña un rol determinado. El rol se define mediante la propiedad especificada, una propiedad de referencia de tipo [ref](references.md). La **palabra clave Role** es útil en asociaciones en las que un determinado objeto puede desempeñar un rol en algunos casos y otro rol en otros, como en asociaciones jerárquicas. La **palabra clave Role** se puede usar para recuperar todas las asociaciones en las que el objeto de origen desempeña el rol de elemento primario, por ejemplo. La siguiente instrucción muestra la sintaxis para recuperar asociaciones que tienen una **propiedad** primaria que hace referencia al objeto de origen como elemento primario:


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE Role = parent
```



> [!Note]  
> Las consultas complejas no pueden usar "And" o "Or" para separar palabras clave para las instrucciones ASSOCIATORS OF y REFERENCES OF. Además, el signo igual es el único operador válido que se puede usar con las palabras clave de estas consultas. Por ejemplo, la consulta siguiente es válida:

 


```sql
"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
    "WHERE resultclass = Win32_NetworkAdapterSetting " +
    "requiredQualifier = Dynamic"
```



> [!Note]  
> Los ejemplos siguientes no son válidos. El primer ejemplo no usa el signo igual y el segundo ejemplo intenta usar erróneamente la **palabra clave AND:**

 


```sql
"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
    "WHERE resultclass = Win32_NetworkAdapterSetting " +
    "requiredQualifier <> Dynamic"

"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
"WHERE resultclass = Win32_NetworkAdapterSetting " +
"AND requiredQualifier = Dynamic"
```



 

 



