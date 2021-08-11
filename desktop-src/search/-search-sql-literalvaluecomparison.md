---
description: La comparación de valores literales usa operadores de comparación estándar para hacer coincidir una columna de un solo valor con un valor literal.
ms.assetid: 941298b4-d703-4b3f-8bde-0e6e158560df
title: Comparación de valores literales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c1e311c6f98c1114b63a1bf650d6e7be004e1e8e4cf5848b962a7cbf8049bfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118227183"
---
# <a name="literal-value-comparison"></a>Comparación de valores literales

La comparación de valores literales usa operadores de comparación estándar para hacer coincidir una columna de un solo valor con un [valor literal.](-search-sql-literals.md) Para obtener información sobre cómo comparar columnas de varios valores, vea [Comparaciones multivalor (ARRAY).](-search-sql-multivaluedcomparisons.md)

El predicado de comparación de valores literales tiene la sintaxis siguiente:


```
...WHERE <column> <comparison operator> <literal>
```



> [!Note]  
> El lado derecho de la comparación debe ser un literal. No se puede comparar una columna con un valor calculado y no se puede comparar una columna con otra columna.

 

La parte de columna es cualquier columna de propiedad válida y se puede convertir a otro tipo si es necesario. Opcionalmente, puede incluir el nombre de columna entre comillas dobles para mejorar la legibilidad sin que ello afecte a la funcionalidad. Para obtener más información, [vea Convertir el tipo de datos de una columna](-search-sql-castingdatacolumntype.md).

El literal puede ser cualquier literal de cadena, numérico, hexadecimal, booleano o de fecha, entre comillas simples. Solo se reconocen coincidencias exactas y se omiten los caracteres comodín. El literal también se puede convertir a otro tipo.

## <a name="comparison-operators"></a>Operadores de comparación

En la tabla siguiente se describen los operadores de comparación admitidos.



| Operadores de comparación | Descripción              |
|---------------------|--------------------------|
| =                   | Igual a                 |
| != o <>      | No es igual a             |
| >                | Mayor que             |
| >=               | Mayor o igual que |
| <                | Menor que                |
| <=               | Menor o igual que    |



 

 

Junto con el operador "=", Windows Search Lenguaje de consulta estructurado (SQL) admite el uso de palabras clave BEFORE y AFTER, que especifican si la consulta debe comparar los valores de columna antes o después de un valor especificado, en la ordenación del diccionario.


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

[Predicado LIKE](-search-sql-like.md)
</dt> <dt>

[Función DATEADD](-search-sql-dateadd.md)
</dt> <dt>

[Comparaciones multivalor (ARRAY)](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

[Predicado NULL](-search-sql-null.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Predicados de texto completo](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicados que no son de texto completo](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



