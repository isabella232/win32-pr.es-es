---
description: Comprenda los argumentos inputlocale y keywordlocale en la interfaz de usuario de Windows Shell, lo que ayuda al motor de búsqueda a usar los separadores de palabras correctos.
title: Argumentos del identificador de configuración regional (Shell de Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 881ce3a6-6cf6-45be-9a1e-148b9053d7c4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 34eab39e7ed956bf68048d9ce5861c12eedbbe7a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403598"
---
# <a name="locale-identifier-arguments-the-windows-shell"></a>Argumentos del identificador de configuración regional (Shell de Windows)

Los identificadores y ayudan al motor de búsqueda a usar los separadores de palabras correctos mediante la identificación del idioma de las consultas especificadas por el usuario y el idioma de las palabras clave de sintaxis de `inputlocale` `keywordlocale` consulta avanzada. No siempre son los mismos identificadores de código de idioma (LCID) porque Windows Search se ofrece en varias versiones internacionales y también incluye paquetes Interfaz de usuario multilingüe (QR) para más idiomas. identifica el LCID para el idioma en el que los usuarios introducen su consulta de búsqueda, mientras que identifica el LCID que el motor de búsqueda `inputlocale` usa para las palabras `keywordlocale` clave.

## <a name="example"></a>Ejemplo


```
search:query=matthew&inputlocale=2072&keywordlocale=1033
```



### <a name="argument-information"></a>Información de argumentos



|                              | Valor                                   |
|------------------------------|-----------------------------------------|
| **Sistema operativo mínimo** | Windows Vista con Service Pack 1 (SP1) |



 

 

 



