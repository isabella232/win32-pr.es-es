---
description: Los alias de grupo de columnas proporcionan una manera de usar nombres más cortos en lugar del nombre de una columna o un grupo de columnas. El predicado de alias de grupo opcional forma parte de la cláusula WHERE.
ms.assetid: 7782ac24-ea6c-4a97-b1b6-982f276fcefc
title: 'WITH : predicado de alias de grupo de AS'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ed77072c83d1c28dcc3ec63396b46a21a57c4a97d9c6dcd70259bd861d19762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226738"
---
# <a name="with----as-group-alias-predicate"></a>WITH : predicado de alias de grupo de AS

Los alias de grupo de columnas proporcionan una manera de usar nombres más cortos en lugar del nombre de una columna o un grupo de columnas. El predicado de alias de grupo opcional forma parte de la cláusula WHERE. Su sintaxis es la siguiente:


```
...WHERE[ WITH(<columns>) AS #<alias_name>]
[,WITH(<columns>) AS #<alias_name>]
```



Puede especificar más de un alias de grupo, separando with... Los predicados AS se basan en comas.

Cuando se hace referencia a un alias de grupo en un predicado de cláusula WHERE, la condición se aplica a cada columna del grupo. Los valores lógicos resultantes de la coincidencia de cada columna se combinan mediante el operador **lógico OR.**

Un alias debe definirse antes de que se pueda usar y solo se puede usar dentro de la cláusula WHERE. El nombre de alias debe ser un identificador normal precedido de un signo de kilo requerido ( \# ).

El especificador de columna puede contener uno o varios especificadores de columna, separados por comas. La lista de columnas debe incluirse entre paréntesis y el peso se puede asignar a cada una de ellas. Cada columna tiene la sintaxis siguiente:


```
<column_identifier> [<weight_assignment>]
```



Para obtener información sobre cómo especificar los pesos de columna, [vea FREETEXT Predicate](-search-sql-freetext.md) y [CONTAINS Predicate](-search-sql-contains.md).

El identificador de columna puede ser normal o delimitado.

## <a name="examples"></a>Ejemplos

Los siguientes ejemplos de cláusula WHERE muestran cuándo y cómo se puede usar el predicado de alias de grupo. En el primer ejemplo se muestra una cláusula WHERE más repetitiva que no usa alias de grupo.


```
...WHERE
    FREETEXT("System.ItemNameDisplay",'"computer software"')
    OR
    FREETEXT("System.Title",'"computer software"')
    OR 
    FREETEXT("System.Keywords",'"computer software"')
```



El ejemplo anterior se puede simplificar mediante un alias de grupo, como se muestra en el ejemplo siguiente.


```
...WHERE
    WITH("System.ItemNameDisplay","System.Title","System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



A continuación se muestra un ejemplo de ponderación positiva en el que la **propiedad Title** tiene más peso al determinar el rango relativo.


```
...WHERE
    WITH("System.Title":0.8,*:0.5,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



A continuación se muestra un ejemplo de ponderación negativa en el que no se tiene en cuenta la propiedad **Title** con un peso de 0.


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

**Conceptual**
</dt> <dt>

[Predicados de texto completo](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicados que no son de texto completo](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



