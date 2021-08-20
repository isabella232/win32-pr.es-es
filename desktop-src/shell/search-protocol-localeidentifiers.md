---
description: Comprenda los argumentos inputlocale y keywordlocale en la interfaz de usuario de Windows Shell, lo que ayuda al motor de búsqueda a usar los separadores de palabras correctos.
title: Argumentos del identificador de configuración regional (el Windows shell)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 881ce3a6-6cf6-45be-9a1e-148b9053d7c4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b9c97f40d380acdbb26486acb248a273cb9d220588300a559275b73e41596e2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117677342"
---
# <a name="locale-identifier-arguments-the-windows-shell"></a>Argumentos del identificador de configuración regional (el Windows shell)

Los identificadores y ayudan al motor de búsqueda a usar los separadores de palabras correctos mediante la identificación del idioma de las consultas especificadas por el usuario y el idioma de las palabras clave de sintaxis de `inputlocale` `keywordlocale` consulta avanzada. No siempre son los mismos identificadores de código de idioma (LCID) porque Windows Search se ofrece en varias versiones internacionales y también incluye paquetes Interfaz de usuario multilingüe (QR) para más idiomas. identifica el LCID del idioma en el que los usuarios introducen su consulta de búsqueda, mientras que identifica el LCID que el motor de búsqueda `inputlocale` usa para las palabras `keywordlocale` clave.

## <a name="example"></a>Ejemplo


```
search:query=matthew&inputlocale=2072&keywordlocale=1033
```



### <a name="argument-information"></a>Información de argumentos



|                              | Valor                                   |
|------------------------------|-----------------------------------------|
| **Sistema operativo mínimo** | Windows Vista con Service Pack 1 (SP1) |



 

 

 



