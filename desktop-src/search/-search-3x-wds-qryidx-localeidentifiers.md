---
description: Los identificadores de inputlocale y keywordlocale ayudan al motor de búsqueda a usar los separadores de palabras correctos identificando el idioma de las consultas escritas por el usuario y el idioma de las palabras clave de sintaxis de consulta avanzada.
ms.assetid: dc610f49-5106-47f9-b29b-84949dd2c42b
title: Argumentos de identificador de configuración regional (búsqueda de Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea1549a550e4bf6b8099241a6f3d2275860a983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907756"
---
# <a name="locale-identifier-arguments-windows-search"></a>Argumentos de identificador de configuración regional (búsqueda de Windows)

Los `inputlocale` `keywordlocale` identificadores y ayudan al motor de búsqueda a usar los separadores de palabras correctos identificando el idioma de las consultas escritas por el usuario y el idioma de las palabras clave de sintaxis de consulta avanzada. Estos no son siempre los mismos identificadores de código de idioma (LCID) porque Windows Search se ofrece en varias versiones internacionales y también incluye paquetes MUI para más idiomas. Inputlocale identifica el LCID para el idioma en el que los usuarios escriben su consulta de búsqueda en, mientras que keywordlocale identifica el LCID que el motor de búsqueda utiliza para las palabras clave.

Este tema se organiza de la siguiente manera:

-   [Ejemplo](#example)
-   [Temas relacionados](#related-topics)

## <a name="example"></a>Ejemplo


```
 search-ms:query=matthew&inputlocale=2072&keywordlocale=1033
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción con argumentos de Parameter-Value](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[Argumento de MIGAs de](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[Argumento de sintaxis](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[Argumento STACKEDBY](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[Argumento de subconsulta](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 



