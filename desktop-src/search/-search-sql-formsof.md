---
description: El término FORMSOF realiza coincidencias con otras formas lingüísticas de la palabra.
ms.assetid: b705b8bc-dc2c-4cee-8306-f494b0f96cbf
title: Términos de FORMs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20504a7a36c7f0cb9c69b9513f33446501641bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705485"
---
# <a name="formsof-term"></a>Términos de FORMs

El término FORMSOF realiza coincidencias con otras formas lingüísticas de la palabra. A continuación se indican las sintaxis de los términos de FORMSOF:


```
FORMSOF (<generation_type>,<match_words>)
```



El tipo de generación especifica cómo Microsoft Windows Search elige los formularios de Word alternativos. El valor con **inflexión** elige formas de inflexión alternativas para las palabras de coincidencia. Si la palabra es un verbo, se usan decenas alternativos. Si la palabra es un nombre, los formularios singular, plural y Possessive se usan para detectar coincidencias.

El \_ valor buscar palabras es una o varias palabras, separadas por comas.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se buscan coincidencias con inflexión de la palabra "Run". Este ejemplo encuentra documentos que contienen "Run", "Running" o "Running".


```
...CONTAINS('FORMSOF(INFLECTIONAL,"run")')
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Predicado FREETEXT](-search-sql-freetext.md)
</dt> <dt>

[Cláusula WHERE](-search-sql-where.md)
</dt> </dl>

 

 



