---
description: El protocolo Search-MS? Application es una Convención para consultar el índice de Windows Search.
ms.assetid: e8b18018-c712-4007-bb0a-af90a75780d6
title: Introducción con argumentos de Parameter-Value
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bd6e3df2ddb1d0c3f62293d3d3dc2615e855f93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275261"
---
# <a name="getting-started-with-parameter-value-arguments"></a>Introducción con argumentos de Parameter-Value

La **búsqueda-MS** ? el [Protocolo de aplicación](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) es una Convención para consultar el índice de Windows Search. El protocolo permite que las aplicaciones, como el explorador de Windows, consulten el índice con argumentos de valor de parámetro, incluidos los argumentos de propiedad, las búsquedas guardadas anteriormente, la sintaxis de consulta avanzada (AQS), la sintaxis de consulta natural (NQS) y los identificadores de código de idioma (LCID) del indexador y la propia consulta.

Este tema se organiza de la siguiente manera:

- [Acerca de los argumentos de Parameter-Value](#about-parameter-value-arguments)
- [Ejemplos](#examples)
- [Temas relacionados](#related-topics)

## <a name="about-parameter-value-arguments"></a>Acerca de los argumentos de Parameter-Value

El protocolo Search-MS usa la siguiente sintaxis codificada como dirección URL estándar:

```
search-ms:parameter=value[&parameter=value]&
```

La sintaxis comienza mediante la identificación del protocolo en sí (Search-MS:). Los pares de parámetro/valor son argumentos pasados al motor de búsqueda, como se describe en la tabla siguiente.

| Parámetro                                                    | Value                                                         | Descripción                                                                                                                                                                                                                                                                | Versión                  |
|--------------------------------------------------------------|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| Query                                                        | Texto con codificación URL                                              | Texto de la consulta escrito por el usuario.                                                                                                                                                                                                                                        | Windows XP y versiones posteriores    |
| [inputlocale](-search-3x-wds-qryidx-localeidentifiers.md)   | Cualquier LCID válido                                                | LCID que identifica el idioma de entrada de la consulta.                                                                                                                                                                                                                 | Windows XP y versiones posteriores    |
| [keywordlocale](-search-3x-wds-qryidx-localeidentifiers.md) | Cualquier LCID válido                                                | LCID que identifica el idioma de la versión internacional del indexador. El valor predeterminado es 1033 (en-US).                                                                                                                                                            | Windows XP y versiones posteriores    |
| [rutas](-search-3x-wds-qryidx-crumb.md)                     | AQS (instrucción)                                                 | Este argumento restringe el ámbito en el que se busca. En Windows Vista y versiones posteriores, Search-MS admite AQS completo, así como una implementación especial para un `location` argumento. En Windows XP, Search-MS también admite AQS completo, salvo una implementación especial de `kind` y `store` . | Windows XP y versiones posteriores    |
| [sintáctica](-search-3x-wds-qryidx-syntaxargument.md)           | NQS, AQS (no distingue mayúsculas de minúsculas)                                 | Sintaxis de consulta que se va a usar para buscar en el índice: sintaxis de consulta natural o sintaxis de consulta avanzada (AQS). AQS es el valor predeterminado y siempre se asume que se analiza y se admite.                                                                                                    | Windows Vista y versiones posteriores |
| [stackedby](-search-3x-wds-qryidx-stackedby.md)             | Cualquier propiedad válida del sistema de propiedades                   | Propiedad que especifica la columna por la que se van a apilar los resultados.                                                                                                                                                                                                                  | Windows Vista y versiones posteriores |
| [subquery](-search-3x-wds-qryidx-subquery.md)               | Una ruta de acceso completa para un archivo de búsqueda guardado ( \* . Search-MS) | Los resultados de la subconsulta se utilizan como el origen de la consulta. Es decir, se busca en los términos de la consulta con los resultados de la subconsulta.                                                                                                                           | Windows Vista y versiones posteriores |
| displayname                                                  | Cadena con codificación URL                                            | Nombre de la búsqueda actual.                                                                                                                                                                                                                                            | Windows Vista y versiones posteriores |


Para obtener información relacionada, consulte [registrar una aplicación en un protocolo de dirección URL](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85)).

## <a name="examples"></a>Ejemplos

```
search-ms:query=microsoft&
search-ms:query=vacation&subquery=mydepartment.search-ms&
search-ms:query=seattle&crumb=kind:pics&
search-ms:query=seattle&crumb=folder:C:\MyFolder&
```

## <a name="related-topics"></a>Temas relacionados

[Argumentos de identificador de configuración regional](-search-3x-wds-qryidx-localeidentifiers.md)

[Argumento de MIGAs de](-search-3x-wds-qryidx-crumb.md)

[Argumento de sintaxis](-search-3x-wds-qryidx-syntaxargument.md)

[Argumento STACKEDBY](-search-3x-wds-qryidx-stackedby.md)

[Argumento de subconsulta](-search-3x-wds-qryidx-subquery.md)
