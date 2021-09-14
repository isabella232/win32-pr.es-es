---
description: Comprenda los argumentos inputlocale y keywordlocale en Windows Search, lo que ayuda al motor de búsqueda a usar los separadores de palabras correctos.
ms.assetid: dc610f49-5106-47f9-b29b-84949dd2c42b
title: Argumentos del identificador de configuración regional (Windows búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe4c56e9c3fb5a84938d4779c7a3ebeb849b0787
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127262591"
---
# <a name="locale-identifier-arguments-windows-search"></a>Argumentos del identificador de configuración regional (Windows búsqueda)

Los identificadores y ayudan al motor de búsqueda a usar los separadores de palabras correctos mediante la identificación del idioma de las consultas especificadas por el usuario y el idioma de las palabras clave advanced `inputlocale` `keywordlocale` query syntax. No siempre son los mismos identificadores de código de idioma (LCID), ya que Windows Search se ofrece en varias versiones internacionales y también incluye paquetes de QR para más idiomas. Inputlocale identifica el LCID para el idioma en el que los usuarios introducen su consulta de búsqueda, mientras que la palabra clavelocale identifica el LCID que el motor de búsqueda usa para las palabras clave.

Este tema se organiza de la siguiente manera:

-   [Ejemplo](#example)
-   [Temas relacionados](#related-topics)

## <a name="example"></a>Ejemplo


```
 search-ms:query=matthew&inputlocale=2072&keywordlocale=1033
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas iniciales con Parameter-Value argumentos](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[Argumento CRUMB](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[Argumento SYNTAX](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[Argumento STACKEDBY](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[Argumento SUBQUERY](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 



