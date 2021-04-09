---
description: Los alias de grupo de columnas proporcionan una manera de usar nombres más cortos en lugar del nombre de una columna o un grupo de columnas. El predicado de alias de grupo opcional forma parte de la cláusula WHERE.
ms.assetid: 7782ac24-ea6c-4a97-b1b6-982f276fcefc
title: CON el predicado de alias de grupo AS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29218e11fbffe5f47128eeefba3a7fe847a5b21d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808924"
---
# <a name="with----as-group-alias-predicate"></a>CON el predicado de alias de grupo AS

Los alias de grupo de columnas proporcionan una manera de usar nombres más cortos en lugar del nombre de una columna o un grupo de columnas. El predicado de alias de grupo opcional forma parte de la cláusula WHERE. Su sintaxis es la siguiente:


```
...WHERE[ WITH(<columns>) AS #<alias_name>]
[,WITH(<columns>) AS #<alias_name>]
```



Puede especificar más de un alias de grupo, separando la... COMO predicados por comas.

Cuando se hace referencia a un alias de grupo en un predicado de la cláusula WHERE, la condición se aplica a cada columna del grupo. Los valores lógicos resultantes de la coincidencia de cada columna se combinan mediante el operador lógico **or** .

Se debe definir un alias antes de poder usarlo y solo se puede usar dentro de la cláusula WHERE. El nombre del alias debe ser un identificador normal precedido por un signo de almohadilla ( \# ) necesario.

El especificador de columna puede contener uno o más especificadores de columna, separados por comas. La lista de columnas debe ir entre paréntesis y la ponderación se puede asignar a cada una. Cada columna tiene la siguiente sintaxis:


```
<column_identifier> [<weight_assignment>]
```



Para obtener información sobre cómo especificar los pesos de las columnas, vea [predicado FREETEXT](-search-sql-freetext.md) and [Contains Predicate](-search-sql-contains.md).

El identificador de columna puede ser normal o delimitado.

## <a name="examples"></a>Ejemplos

Los siguientes ejemplos de la cláusula WHERE muestran Cuándo y cómo se puede usar el predicado de alias de grupo. EN el primer ejemplo se muestra una cláusula WHERE más repetitiva que no usa el alias de grupo.


```
...WHERE
    FREETEXT("System.ItemNameDisplay",'"computer software"')
    OR
    FREETEXT("System.Title",'"computer software"')
    OR 
    FREETEXT("System.Keywords",'"computer software"')
```



El ejemplo anterior se puede simplificar mediante el uso de un alias de grupo, tal como se muestra en el ejemplo siguiente.


```
...WHERE
    WITH("System.ItemNameDisplay","System.Title","System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



A continuación se ofrece un ejemplo de ponderación positiva en la que la propiedad **title** tiene más peso para determinar el rango relativo.


```
...WHERE
    WITH("System.Title":0.8,*:0.5,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



A continuación se proporciona un ejemplo de ponderación negativa donde no se tiene en cuenta la propiedad **title** con el peso de 0.


```
...WHERE
    WITH("System.Title":0,*:1.0,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Predicado FREETEXT](-search-sql-freetext.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Predicados de texto completo](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicados que no son de texto completo](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



