---
description: Comprenda los argumentos inputlocale y keywordlocale Windows Search, lo que ayuda al motor de búsqueda a usar los separadores de palabras correctos.
ms.assetid: dc610f49-5106-47f9-b29b-84949dd2c42b
title: Argumentos del identificador de configuración regional (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe4c56e9c3fb5a84938d4779c7a3ebeb849b0787
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403758"
---
# <a name="locale-identifier-arguments-windows-search"></a><span data-ttu-id="7b267-103">Argumentos del identificador de configuración regional (Windows Search)</span><span class="sxs-lookup"><span data-stu-id="7b267-103">Locale Identifier Arguments (Windows Search)</span></span>

<span data-ttu-id="7b267-104">Los identificadores y ayudan al motor de búsqueda a usar los separadores de palabras correctos mediante la identificación del idioma de las consultas especificadas por el usuario y el idioma de las palabras clave de sintaxis de `inputlocale` `keywordlocale` consulta avanzada.</span><span class="sxs-lookup"><span data-stu-id="7b267-104">The `inputlocale` and `keywordlocale` identifiers help the search engine use the correct word breakers by identifying the language of user-entered queries and the language the of Advanced Query Syntax keywords.</span></span> <span data-ttu-id="7b267-105">No siempre son los mismos identificadores de código de idioma (LCID), ya que Windows Search se ofrece en varias versiones internacionales y también incluye paquetes de QR para más idiomas.</span><span class="sxs-lookup"><span data-stu-id="7b267-105">These are not always the same language code identifiers (LCIDs) because Windows Search is offered in a number of international versions and also includes MUI packs for more languages.</span></span> <span data-ttu-id="7b267-106">Inputlocale identifica el LCID para el idioma en el que los usuarios introducen su consulta de búsqueda, mientras que la palabra clavelocale identifica el LCID que el motor de búsqueda usa para las palabras clave.</span><span class="sxs-lookup"><span data-stu-id="7b267-106">The inputlocale identifies the LCID for the language users input their search query in, while the keywordlocale identifies the LCID the search engine uses for keywords.</span></span>

<span data-ttu-id="7b267-107">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="7b267-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="7b267-108">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7b267-108">Example</span></span>](#example)
-   [<span data-ttu-id="7b267-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7b267-109">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="7b267-110">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7b267-110">Example</span></span>


```
 search-ms:query=matthew&inputlocale=2072&keywordlocale=1033
```



## <a name="related-topics"></a><span data-ttu-id="7b267-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7b267-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b267-112">Tareas iniciales con Parameter-Value argumentos</span><span class="sxs-lookup"><span data-stu-id="7b267-112">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="7b267-113">Argumento CRUMB</span><span class="sxs-lookup"><span data-stu-id="7b267-113">CRUMB Argument</span></span>](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[<span data-ttu-id="7b267-114">Argumento SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7b267-114">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="7b267-115">Argumento STACKEDBY</span><span class="sxs-lookup"><span data-stu-id="7b267-115">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[<span data-ttu-id="7b267-116">Argumento SUBQUERY</span><span class="sxs-lookup"><span data-stu-id="7b267-116">SUBQUERY Argument</span></span>](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 



