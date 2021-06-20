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
# <a name="locale-identifier-arguments-the-windows-shell"></a><span data-ttu-id="adb70-103">Argumentos del identificador de configuración regional (Shell de Windows)</span><span class="sxs-lookup"><span data-stu-id="adb70-103">Locale Identifier Arguments (The Windows Shell)</span></span>

<span data-ttu-id="adb70-104">Los identificadores y ayudan al motor de búsqueda a usar los separadores de palabras correctos mediante la identificación del idioma de las consultas especificadas por el usuario y el idioma de las palabras clave de sintaxis de `inputlocale` `keywordlocale` consulta avanzada.</span><span class="sxs-lookup"><span data-stu-id="adb70-104">The `inputlocale` and `keywordlocale` identifiers help the search engine use the correct word breakers by identifying the language of user-entered queries and the language the of Advanced Query Syntax keywords.</span></span> <span data-ttu-id="adb70-105">No siempre son los mismos identificadores de código de idioma (LCID) porque Windows Search se ofrece en varias versiones internacionales y también incluye paquetes Interfaz de usuario multilingüe (QR) para más idiomas.</span><span class="sxs-lookup"><span data-stu-id="adb70-105">These are not always the same language code identifiers (LCIDs) because Windows Search is offered in a number of international versions and also includes Multilingual User Interface (MUI) packs for more languages.</span></span> <span data-ttu-id="adb70-106">identifica el LCID para el idioma en el que los usuarios introducen su consulta de búsqueda, mientras que identifica el LCID que el motor de búsqueda `inputlocale` usa para las palabras `keywordlocale` clave.</span><span class="sxs-lookup"><span data-stu-id="adb70-106">The `inputlocale` identifies the LCID for the language users input their search query in, while the `keywordlocale` identifies the LCID the search engine uses for keywords.</span></span>

## <a name="example"></a><span data-ttu-id="adb70-107">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="adb70-107">Example</span></span>


```
search:query=matthew&inputlocale=2072&keywordlocale=1033
```



### <a name="argument-information"></a><span data-ttu-id="adb70-108">Información de argumentos</span><span class="sxs-lookup"><span data-stu-id="adb70-108">Argument Information</span></span>



|                              | <span data-ttu-id="adb70-109">Valor</span><span class="sxs-lookup"><span data-stu-id="adb70-109">Value</span></span>                                   |
|------------------------------|-----------------------------------------|
| <span data-ttu-id="adb70-110">**Sistema operativo mínimo**</span><span class="sxs-lookup"><span data-stu-id="adb70-110">**Minimum Operating System**</span></span> | <span data-ttu-id="adb70-111">Windows Vista con Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="adb70-111">Windows Vista with Service Pack 1 (SP1)</span></span> |



 

 

 



