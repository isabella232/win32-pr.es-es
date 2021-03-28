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
# <a name="locale-identifier-arguments-the-windows-shell"></a><span data-ttu-id="7bafa-103">Argumentos de identificador de configuración regional (Shell de Windows)</span><span class="sxs-lookup"><span data-stu-id="7bafa-103">Locale Identifier Arguments (The Windows Shell)</span></span>

<span data-ttu-id="7bafa-104">Los `inputlocale` `keywordlocale` identificadores y ayudan al motor de búsqueda a usar los separadores de palabras correctos identificando el idioma de las consultas escritas por el usuario y el idioma de las palabras clave de sintaxis de consulta avanzada.</span><span class="sxs-lookup"><span data-stu-id="7bafa-104">The `inputlocale` and `keywordlocale` identifiers help the search engine use the correct word breakers by identifying the language of user-entered queries and the language the of Advanced Query Syntax keywords.</span></span> <span data-ttu-id="7bafa-105">Estos no son siempre los mismos identificadores de código de idioma (LCID) porque Windows Search se ofrece en varias versiones internacionales y también incluye paquetes de interfaz de usuario multilingüe (MUI) para más idiomas.</span><span class="sxs-lookup"><span data-stu-id="7bafa-105">These are not always the same language code identifiers (LCIDs) because Windows Search is offered in a number of international versions and also includes Multilingual User Interface (MUI) packs for more languages.</span></span> <span data-ttu-id="7bafa-106">`inputlocale`Identifica el LCID para el idioma en el que los usuarios escriben su consulta de búsqueda en, mientras que `keywordlocale` identifica el LCID que el motor de búsqueda utiliza para las palabras clave.</span><span class="sxs-lookup"><span data-stu-id="7bafa-106">The `inputlocale` identifies the LCID for the language users input their search query in, while the `keywordlocale` identifies the LCID the search engine uses for keywords.</span></span>

## <a name="example"></a><span data-ttu-id="7bafa-107">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7bafa-107">Example</span></span>


```
search:query=matthew&inputlocale=2072&keywordlocale=1033
```



### <a name="argument-information"></a><span data-ttu-id="7bafa-108">Información de argumentos</span><span class="sxs-lookup"><span data-stu-id="7bafa-108">Argument Information</span></span>



|                          |                                         |
|--------------------------|-----------------------------------------|
| <span data-ttu-id="7bafa-109">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="7bafa-109">Minimum Operating System</span></span> | <span data-ttu-id="7bafa-110">Windows Vista con Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="7bafa-110">Windows Vista with Service Pack 1 (SP1)</span></span> |



 

 

 



