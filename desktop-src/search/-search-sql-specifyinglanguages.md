---
description: Puede especificar el idioma que se usa en las consultas de búsqueda.
ms.assetid: 3a7ecf8f-38ae-41d1-be70-e9ab23977a01
title: Especificar idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50b3f65a41670989d41e235831ec8c008a6d8cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540662"
---
# <a name="specifying-languages"></a><span data-ttu-id="5f346-103">Especificar idiomas</span><span class="sxs-lookup"><span data-stu-id="5f346-103">Specifying Languages</span></span>

<span data-ttu-id="5f346-104">Puede especificar el idioma que se usa en las consultas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="5f346-104">You can specify the language used in search queries.</span></span> <span data-ttu-id="5f346-105">Los predicados FREETEXT y Contains de la cláusula WHERE admiten la especificación de un idioma.</span><span class="sxs-lookup"><span data-stu-id="5f346-105">Both the FREETEXT and CONTAINS predicates in the WHERE clause support specifying a language.</span></span> <span data-ttu-id="5f346-106">Puede indicar el lenguaje de consulta proporcionando un identificador de código de idioma (LCID) numérico en el predicado CONTAINS o FREETEXT.</span><span class="sxs-lookup"><span data-stu-id="5f346-106">You can indicate the query language by providing a numeric language code identifier (LCID) in the CONTAINS or FREETEXT predicate.</span></span> <span data-ttu-id="5f346-107">Este LCID especifica el separador de palabras que se va a utilizar para analizar la cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="5f346-107">This LCID specifies which word breaker to use to parse the query string.</span></span> <span data-ttu-id="5f346-108">Utiliza la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="5f346-108">It uses the following syntax:</span></span>


```
CONTAINS | FREETEXT
([<column_identifier>,]'<content_search_condition>' [,LCID]) 
```



<span data-ttu-id="5f346-109">Para obtener más información, vea la sintaxis de los predicados [Contains](-search-sql-contains.md) y [FREETEXT](-search-sql-freetext.md) .</span><span class="sxs-lookup"><span data-stu-id="5f346-109">For more information, see the syntax for the [CONTAINS](-search-sql-contains.md) and [FREETEXT](-search-sql-freetext.md) predicates.</span></span>

 

 



