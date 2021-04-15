---
description: La instrucción REFERENCEs de recupera todas las instancias de asociación que hacen referencia a una instancia de origen determinada.
ms.assetid: 674be546-e7fd-4150-9d7c-2888d24bf1b3
ms.tgt_platform: multiple
title: REFERENCIAS de la instrucción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c7cc624a1e91220fc6bfc89ef0a75878a9cfb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648281"
---
# <a name="references-of-statement"></a>REFERENCIAS de la instrucción

La instrucción REFERENCEs de recupera todas las instancias de asociación que hacen referencia a una instancia de origen determinada. La instrucción REFERENCEs de es similar a la instrucción ASSOCIATORS OF en su sintaxis. Sin embargo, en lugar de recuperar instancias de extremo, recupera las instancias de asociación intermedias.

Las referencias de la cláusula WHERE pueden incluir una o varias de las siguientes palabras clave predefinidas y sus valores:


```sql
REFERENCES OF {SourceObject} WHERE 
    ClassDefsOnly
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    Role = PropertyName
```



Para especificar un objeto de origen, use una ruta de acceso de objeto válida para SourceObject. Al igual que con la instrucción SELECT, la cláusula WHERE es opcional y se usa para definir aún más la consulta. Es decir, la siguiente instrucción es perfectamente válida:


```sql
REFERENCES OF {Adapter="AHA-294X"}
```



La palabra clave **ClassDefsOnly** indica que la instrucción devuelve un conjunto de resultados de objetos de definición de clase en lugar de instancias reales de las clases de asociación. Estos objetos contienen definiciones de las clases a las que pertenecen las instancias que hacen referencia al objeto de origen. Por ejemplo, la siguiente instrucción devuelve definiciones para las clases **AdapterDriver** y **AdapterProtocol** :


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE ClassDefsOnly
```



La palabra clave **RequiredQualifier** indica que los objetos de asociación devueltos deben incluir el calificador especificado. La palabra clave **RequiredQualifier** se puede usar para incluir instancias particulares de asociaciones en el conjunto de resultados. Por ejemplo, la siguiente instrucción devuelve instancias de asociación que incluyen un calificador denominado **AdapterTag**:


```sql
REFERENCES OF {Adapter="AHA-294X"}  WHERE RequiredQualifier = AdapterTag
```



La palabra clave **ResultClass** indica que los objetos de asociación devueltos deben pertenecer a la clase especificada o derivarse de ella. Por ejemplo, la siguiente instrucción devuelve las asociaciones de la clase **AdapterDriver** o las subclases de **AdapterDriver**:


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE ResultClass = AdapterDriver
```



Las palabras clave **ClassDefsOnly** y **ResultClass** se excluyen mutuamente. Si se usan conjuntamente, se producirá un error de consulta no válido.

La palabra clave **role** indica que las asociaciones devueltas son solo aquellas en las que el objeto de origen desempeña un rol determinado. El rol se define mediante la propiedad especificada, una propiedad de referencia de tipo [ref](references.md). La palabra clave **role** es útil en las asociaciones en las que un determinado objeto puede desempeñar un rol en algunos casos y otro rol en otros, como en las asociaciones jerárquicas. La palabra clave **role** se puede usar para recuperar todas las asociaciones en las que el objeto de origen desempeña el rol del elemento primario, por ejemplo. La siguiente instrucción ilustra la sintaxis para recuperar asociaciones que tienen una propiedad **primaria** que hace referencia al objeto de origen como elemento primario:


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE Role = parent
```



> [!Note]  
> Las consultas complejas no pueden usar "and" o "or" para separar palabras clave para los ASOCIAdores de y las referencias de instrucciones. Además, el signo igual es el único operador válido que se puede usar con las palabras clave en estas consultas. Por ejemplo, la consulta siguiente es válida:

 


```sql
"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
    "WHERE resultclass = Win32_NetworkAdapterSetting " +
    "requiredQualifier = Dynamic"
```



> [!Note]  
> Los ejemplos siguientes no son válidos. En el primer ejemplo no se usa el signo igual y el segundo ejemplo intenta usar erróneamente la palabra clave **y** :

 


```sql
"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
    "WHERE resultclass = Win32_NetworkAdapterSetting " +
    "requiredQualifier <> Dynamic"

"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
"WHERE resultclass = Win32_NetworkAdapterSetting " +
"AND requiredQualifier = Dynamic"
```



 

 



