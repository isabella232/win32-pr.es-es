---
description: El término FORMSOF realiza coincidencias con otras formas lingüísticas de la palabra.
ms.assetid: b705b8bc-dc2c-4cee-8306-f494b0f96cbf
title: Término formsof
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1ffcbd832833a506db99236bf26921a4b0145ffe5bfccaed8fff59103370291
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863448"
---
# <a name="formsof-term"></a>Término formsof

El término FORMSOF realiza coincidencias con otras formas lingüísticas de la palabra. A continuación se muestra la sintaxis del término FORMSOF:


```
FORMSOF (<generation_type>,<match_words>)
```



El tipo de generación especifica cómo Microsoft Windows Search elige los formularios de palabras alternativos. El **valor INFLECTIONAL** elige formularios de inflexión alternativos para las palabras correspondientes. Si la palabra es un verbo, se usan tiempos alternativos. Si la palabra es un sustantivo, se usan las formas singular, plural y posesiva para detectar coincidencias.

El valor \_ de las palabras de coincidencia es una o varias palabras, separadas por comas.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se buscan coincidencias inflectionales para la palabra "run". Este ejemplo coincide con documentos que contienen "run", "running" o "ran".


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

 

 



