---
description: Los identificadores de inputlocale y keywordlocale ayudan al motor de búsqueda a usar los separadores de palabras correctos identificando el idioma de las consultas escritas por el usuario y el idioma de las palabras clave de sintaxis de consulta avanzada.
title: Argumentos de identificador de configuración regional (Shell de Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 881ce3a6-6cf6-45be-9a1e-148b9053d7c4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 403e0338b61a4dedba37a620000e3fd82c91f383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278867"
---
# <a name="locale-identifier-arguments-the-windows-shell"></a>Argumentos de identificador de configuración regional (Shell de Windows)

Los `inputlocale` `keywordlocale` identificadores y ayudan al motor de búsqueda a usar los separadores de palabras correctos identificando el idioma de las consultas escritas por el usuario y el idioma de las palabras clave de sintaxis de consulta avanzada. Estos no son siempre los mismos identificadores de código de idioma (LCID) porque Windows Search se ofrece en varias versiones internacionales y también incluye paquetes de interfaz de usuario multilingüe (MUI) para más idiomas. `inputlocale`Identifica el LCID para el idioma en el que los usuarios escriben su consulta de búsqueda en, mientras que `keywordlocale` identifica el LCID que el motor de búsqueda utiliza para las palabras clave.

## <a name="example"></a>Ejemplo


```
search:query=matthew&inputlocale=2072&keywordlocale=1033
```



### <a name="argument-information"></a>Información de argumentos



|                          |                                         |
|--------------------------|-----------------------------------------|
| Sistema operativo mínimo | Windows Vista con Service Pack 1 (SP1) |



 

 

 



