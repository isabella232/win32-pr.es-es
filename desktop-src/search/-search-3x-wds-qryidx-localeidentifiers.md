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
# <a name="locale-identifier-arguments-windows-search"></a><span data-ttu-id="23f57-103">Argumentos de identificador de configuración regional (búsqueda de Windows)</span><span class="sxs-lookup"><span data-stu-id="23f57-103">Locale Identifier Arguments (Windows Search)</span></span>

<span data-ttu-id="23f57-104">Los `inputlocale` `keywordlocale` identificadores y ayudan al motor de búsqueda a usar los separadores de palabras correctos identificando el idioma de las consultas escritas por el usuario y el idioma de las palabras clave de sintaxis de consulta avanzada.</span><span class="sxs-lookup"><span data-stu-id="23f57-104">The `inputlocale` and `keywordlocale` identifiers help the search engine use the correct word breakers by identifying the language of user-entered queries and the language the of Advanced Query Syntax keywords.</span></span> <span data-ttu-id="23f57-105">Estos no son siempre los mismos identificadores de código de idioma (LCID) porque Windows Search se ofrece en varias versiones internacionales y también incluye paquetes MUI para más idiomas.</span><span class="sxs-lookup"><span data-stu-id="23f57-105">These are not always the same language code identifiers (LCIDs) because Windows Search is offered in a number of international versions and also includes MUI packs for more languages.</span></span> <span data-ttu-id="23f57-106">Inputlocale identifica el LCID para el idioma en el que los usuarios escriben su consulta de búsqueda en, mientras que keywordlocale identifica el LCID que el motor de búsqueda utiliza para las palabras clave.</span><span class="sxs-lookup"><span data-stu-id="23f57-106">The inputlocale identifies the LCID for the language users input their search query in, while the keywordlocale identifies the LCID the search engine uses for keywords.</span></span>

<span data-ttu-id="23f57-107">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="23f57-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="23f57-108">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="23f57-108">Example</span></span>](#example)
-   [<span data-ttu-id="23f57-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="23f57-109">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="23f57-110">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="23f57-110">Example</span></span>


```
 search-ms:query=matthew&inputlocale=2072&keywordlocale=1033
```



## <a name="related-topics"></a><span data-ttu-id="23f57-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="23f57-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23f57-112">Introducción con argumentos de Parameter-Value</span><span class="sxs-lookup"><span data-stu-id="23f57-112">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="23f57-113">Argumento de MIGAs de</span><span class="sxs-lookup"><span data-stu-id="23f57-113">CRUMB Argument</span></span>](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[<span data-ttu-id="23f57-114">Argumento de sintaxis</span><span class="sxs-lookup"><span data-stu-id="23f57-114">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="23f57-115">Argumento STACKEDBY</span><span class="sxs-lookup"><span data-stu-id="23f57-115">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[<span data-ttu-id="23f57-116">Argumento de subconsulta</span><span class="sxs-lookup"><span data-stu-id="23f57-116">SUBQUERY Argument</span></span>](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 



