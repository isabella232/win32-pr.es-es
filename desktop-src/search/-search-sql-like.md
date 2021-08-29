---
description: El predicado LIKE realiza una comparación de coincidencia de patrones en la columna especificada.
ms.assetid: d4bcf406-1253-4e56-b770-79edd4a98205
title: Predicado LIKE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b2faa337ab96eb8cd32c262eb49c792f545de45
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886811"
---
# <a name="like-predicate"></a>Predicado LIKE

El predicado LIKE realiza una comparación de coincidencia de patrones en la columna especificada. Utiliza la siguiente sintaxis:


```
...WHERE <column> LIKE '<wildcard_literal>'
```



La &lt; columna puede ser un identificador normal o &gt; [delimitado.](-search-sql-identifiers.md) La columna se limita a las propiedades del almacén de propiedades.

El <literal \_ comodín> es un literal de cadena. Se incluye entre comillas y, opcionalmente, puede contener caracteres comodín. La cadena de coincidencia puede contener varios caracteres comodín si es necesario. En la tabla siguiente se describen los caracteres comodín que reconoce el predicado LIKE.



| Wildcard (Carácter comodín)                | Descripción                                                                                                                                                                                     | Ejemplo                                                                                                                                                                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| % (porcentaje)             | Coincide con cero o más caracteres.                                                                                                                                                         | 'comp%r' coincide con 'comp' seguido de cero o más caracteres, finalizando en una r.                                                                                                                                  |
| \_ (subrayado)         | Coincidencia con cualquier carácter individual.                                                                                                                                                                   | 'comp \_ ter' coincide con 'comp' seguido exactamente de uno de los caracteres, seguido de 'ter'.                                                                                                                              |
| \[\](corchetes) | Coincide con cualquier carácter individual dentro del intervalo o conjunto especificado. Por ejemplo, \[ a-z \] especifica un intervalo; \[ aeiou \] especifica el conjunto de votos.                                                  | 'comp a-z re' coincide con 'comp' seguido de un solo carácter en el intervalo de \[ \] a a z, seguido de 're'. 'comp \[ ao' coincide con 'comp' seguido de un carácter único que \] debe ser una o.<br/> |
| \[^ \] (caret)          | Coincide con cualquier carácter individual que no esté dentro del intervalo o conjunto especificado. Por ejemplo, \[ ^a-z \] especifica un intervalo que excluye de a a z; \[ ^aeiou \] especifica un conjunto que excluye las votos. | 'comp \[ \] ^u' coincide con 'comp' seguido de cualquier carácter único que no sea una u.                                                                                                                                        |



 

Si crea predicados con varios intervalos, los intervalos deben estar en orden.

> [!Note]  
> Para que los caracteres comodín coincidan como caracteres literales y no como caracteres comodín, coloque el carácter entre corchetes. Por ejemplo, para que coincida con el signo de porcentaje, use \[ ' % \]

 

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

 

 




