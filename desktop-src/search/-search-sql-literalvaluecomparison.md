---
description: La comparación de valores literales utiliza operadores de comparación estándar para hacer coincidir una columna de un solo valor con un valor literal.
ms.assetid: 941298b4-d703-4b3f-8bde-0e6e158560df
title: Comparación de valores literales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d8577e5a97dcc92131658c325f175efa1d0c3fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696282"
---
# <a name="literal-value-comparison"></a>Comparación de valores literales

La comparación de valores literales utiliza operadores de comparación estándar para hacer coincidir una columna de un solo valor con un valor [literal](-search-sql-literals.md) . Para obtener información sobre la comparación de columnas con varios valores, consulte [comparaciones con múltiples valores (matriz)](-search-sql-multivaluedcomparisons.md).

El predicado de comparación de valores literales tiene la siguiente sintaxis:


```
...WHERE <column> <comparison operator> <literal>
```



> [!Note]  
> El lado derecho de la comparación debe ser un literal. No se puede comparar una columna con un valor calculado y no se puede comparar una columna con otra columna.

 

La parte de la columna es cualquier columna de propiedad válida y se puede convertir a otro tipo si es necesario. Opcionalmente, puede escribir el nombre de la columna entre comillas dobles para facilitar la lectura sin que ello afecte a la funcionalidad. Para obtener más información, vea [convertir el tipo de datos de una columna](-search-sql-castingdatacolumntype.md).

El literal puede ser cualquier cadena, numérica, hexadecimal, booleano o literal de fecha, entre comillas simples. Solo se reconocen las coincidencias exactas y se omiten los caracteres comodín. El literal también se puede convertir en otro tipo.

## <a name="comparison-operators"></a>Operadores de comparación

En la tabla siguiente se describen los operadores de comparación admitidos.



| Operadores de comparación | Descripción              |
|---------------------|--------------------------|
| =                   | Igual a                 |
| ! = o <>      | No es igual a             |
| >                | Mayor que             |
| >=               | Mayor o igual que |
| <                | Menor que                |
| <=               | Menor o igual que    |



 

 

Junto con el operador "=", Lenguaje de consulta estructurado de Windows Search (SQL) admite el uso de las palabras clave BEFORe y AFTER, que especifican si la consulta debe comparar los valores de columna antes o después de un valor especificado, en el orden de ordenación del diccionario.


```
...WHERE <column> <comparison operator> [BEFORE | AFTER](<https://msdn.microsoft.com/library/Ff637626(v=MSDN.10).aspx>)
```



## <a name="examples"></a>Ejemplos

A continuación se muestran ejemplos del predicado de comparación de valores literales.


```
SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Title = 'Accounting'

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.IsFlagged != TRUE

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Size >= 10000

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Author = BEFORE('m')
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[LIKE (predicado)](-search-sql-like.md)
</dt> <dt>

[DATEADD (función)](-search-sql-dateadd.md)
</dt> <dt>

[Comparaciones de varios valores (matriz)](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

[Predicado NULL](-search-sql-null.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Predicados de texto completo](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicados que no son de texto completo](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



