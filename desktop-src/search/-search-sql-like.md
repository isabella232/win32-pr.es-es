---
description: El predicado LIKE realiza una comparación de coincidencia de patrones en la columna especificada.
ms.assetid: d4bcf406-1253-4e56-b770-79edd4a98205
title: LIKE (predicado)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba042fb2fe3005e062e7961a048a81a64c0c144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720329"
---
# <a name="like-predicate"></a>LIKE (predicado)

El predicado LIKE realiza una comparación de coincidencia de patrones en la columna especificada. Utiliza la siguiente sintaxis:


```
...WHERE <column> LIKE '<wildcard_literal>'
```



<column>Puede ser un [identificador](-search-sql-identifiers.md)normal o delimitado. La columna está limitada a las propiedades del almacén de propiedades.

El <literal de carácter comodín \_> es un literal de cadena. Está entre comillas y, opcionalmente, puede contener caracteres comodín. La cadena de coincidencia puede contener varios caracteres comodín si es necesario. En la tabla siguiente se describen los caracteres comodín que reconoce el predicado LIKE.



| Wildcard (Carácter comodín)                | Descripción                                                                                                                                                                                     | Ejemplo                                                                                                                                                                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| % (porcentaje)             | Coincide con cero o más caracteres.                                                                                                                                                         | ' COMP% r ' coincide con ' Comp ' seguido de cero o más caracteres, terminando en r.                                                                                                                                  |
| \_ (subrayado)         | Coincidencia con cualquier carácter individual.                                                                                                                                                                   | ' COMP \_ ter ' coincide con ' Comp ' seguido de exactamente un carácter, seguido de ' ter '.                                                                                                                              |
| \[\](corchetes) | Coincide con cualquier carácter individual del intervalo o conjunto especificado. Por ejemplo, \[ a-z \] especifica un intervalo; \[ AEIOU \] especifica el conjunto de vocales.                                                  | ' COMP \[ a-z \] re ' coincide con ' Comp ' seguido de un solo carácter en el intervalo de la a a la z, seguido de ' is '. ' COMP \[ AO \] ' coincide con ' Comp ' seguido de un carácter único que debe ser un o un o.<br/> |
| \[^ \] intercalación          | Coincide con cualquier carácter individual que no esté dentro del intervalo o conjunto especificado. Por ejemplo, \[ ^ a-z \] especifica un intervalo que excluye de la a a la z; \[ ^ AEIOU \] especifica un conjunto que excluye las vocales. | ' COMP \[ ^ u \] ' coincide con ' Comp ' seguido de cualquier carácter individual que no sea un u.                                                                                                                                        |



 

Si crea predicados con varios intervalos, los intervalos deben estar en orden.

> [!Note]  
> Para buscar coincidencias con los caracteres comodín como caracteres literales para buscar coincidencias y no como caracteres comodín, coloque el carácter entre corchetes. Por ejemplo, para que coincida con el signo de porcentaje, use ' \[ % \] '.

 

## <a name="examples"></a>Ejemplos


```
...WHERE System.ItemNameDisplay LIKE 'financ%'
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Comparación de valores literales](-search-sql-literalvaluecomparison.md)
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

 

 




