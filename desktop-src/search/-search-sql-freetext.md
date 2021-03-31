---
description: El predicado FREETEXT forma parte de la cláusula WHERE y permite buscar palabras y frases en columnas de texto.
ms.assetid: 8afc95d1-25cd-4448-8bee-d132c2da22b3
title: Predicado FREETEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc78be4d5ac75f892c82c6dad390e4583876856f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808941"
---
# <a name="freetext-predicate"></a><span data-ttu-id="22022-103">Predicado FREETEXT</span><span class="sxs-lookup"><span data-stu-id="22022-103">FREETEXT Predicate</span></span>

<span data-ttu-id="22022-104">El predicado FREETEXT forma parte de la cláusula [Where](-search-sql-where.md) y permite buscar palabras y frases en columnas de texto.</span><span class="sxs-lookup"><span data-stu-id="22022-104">The FREETEXT predicate is part of the [WHERE](-search-sql-where.md) clause and supports searching for words and phrases in text columns.</span></span> <span data-ttu-id="22022-105">Use el predicado FREETEXT para buscar documentos que contengan combinaciones de las palabras de búsqueda que se distribuyen a lo largo del contenido o de las columnas especificadas.</span><span class="sxs-lookup"><span data-stu-id="22022-105">Use the FREETEXT predicate to find documents containing combinations of the search words spread throughout the content or columns specified.</span></span> <span data-ttu-id="22022-106">Para obtener el valor de rango, incluya System. Search. Rank, que es una clasificación de relevancia, como una columna en la instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="22022-106">To get the rank value, include System.Search.Rank, which is a ranking of relevence, as a column in the SELECT statment.</span></span>

<span data-ttu-id="22022-107">El predicado FREETEXT tiene la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="22022-107">The FREETEXT predicate has the following syntax:</span></span>


```
FREETEXT
(["<fulltext_column>",]'<freetext_condition>'[,<LCID>])...
```



<span data-ttu-id="22022-108">La referencia de columna fulltext es opcional.</span><span class="sxs-lookup"><span data-stu-id="22022-108">The fulltext column reference is optional.</span></span> <span data-ttu-id="22022-109">Con él, puede especificar una sola columna o un alias de [agrupación de columnas](-search-sql-with-as.md) en el que se prueba el predicado FREETEXT.</span><span class="sxs-lookup"><span data-stu-id="22022-109">With it, you can specify a single column, or a [column grouping alias](-search-sql-with-as.md) against which the FREETEXT predicate is tested.</span></span> <span data-ttu-id="22022-110">Cuando la columna fulltext se especifica como "ALL" o " \* ", se busca en todas las propiedades de texto indizadas.</span><span class="sxs-lookup"><span data-stu-id="22022-110">When the fulltext column is specified as "ALL" or "\*", all indexed text properties are searched.</span></span> <span data-ttu-id="22022-111">Aunque no es necesario que la columna sea una propiedad de texto, los resultados podrían no tener sentido si la columna es algún otro tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="22022-111">Although the column is not required to be a text property, the results might be meaningless if the column is some other data type.</span></span> <span data-ttu-id="22022-112">El nombre de la columna puede ser un [identificador](-search-sql-identifiers.md)normal o delimitado, y debe separarlo de la condición mediante una coma.</span><span class="sxs-lookup"><span data-stu-id="22022-112">The column name can be either a regular or delimited [identifier](-search-sql-identifiers.md), and you must separate it from the condition by a comma.</span></span> <span data-ttu-id="22022-113">Si no se proporciona ninguna condición de texto completo, se usa la columna de contenido, que es el cuerpo del documento.</span><span class="sxs-lookup"><span data-stu-id="22022-113">If no fulltext condition is supplied, the Contents column, which is the body of the document, is used.</span></span>

<span data-ttu-id="22022-114">Puede especificar una configuración regional de búsqueda para identificar el separador de palabras y las formas con inflexión adecuadas para la consulta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="22022-114">You can specify a search locale to identify the appropriate word breaker and inflectional forms for the search query.</span></span> <span data-ttu-id="22022-115">Los valores de configuración regional válidos son un identificador de código de idioma (LCID) estándar de Windows.</span><span class="sxs-lookup"><span data-stu-id="22022-115">Valid locale values are a Windows standard language code identifier (LCID).</span></span> <span data-ttu-id="22022-116">Por ejemplo, 1033 es el LCID para Estados Unidos-English.</span><span class="sxs-lookup"><span data-stu-id="22022-116">For example, 1033 is the LCID for United States-English.</span></span> <span data-ttu-id="22022-117">Coloque el LCID como el último elemento dentro de los paréntesis de la cláusula FREETEXT.</span><span class="sxs-lookup"><span data-stu-id="22022-117">Place the LCID as the last item inside the parentheses of the FREETEXT clause.</span></span> <span data-ttu-id="22022-118">Para obtener información importante acerca de la búsqueda y los lenguajes, consulte [uso de búsquedas localizadas](-search-sql-usinglocsearches.md).</span><span class="sxs-lookup"><span data-stu-id="22022-118">For important information about searching and languages, see [Using Localized Searches](-search-sql-usinglocsearches.md).</span></span>

> [!Note]  
> <span data-ttu-id="22022-119">La configuración regional de búsqueda predeterminada es la configuración regional predeterminada del sistema.</span><span class="sxs-lookup"><span data-stu-id="22022-119">The default search locale is the system default locale.</span></span>

 

<span data-ttu-id="22022-120">Debe incluir la parte de la condición FREETEXT entre comillas simples y debe estar formada por uno o varios términos de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="22022-120">You must enclose the freetext condition portion in single quotation marks, and it must consist of one or more search terms.</span></span> <span data-ttu-id="22022-121">El predicado FREETEXT no admite operaciones lógicas.</span><span class="sxs-lookup"><span data-stu-id="22022-121">The FREETEXT predicate does not support logical operations.</span></span> <span data-ttu-id="22022-122">Para buscar una frase como si fuera una sola palabra, incluya la frase entre comillas dobles.</span><span class="sxs-lookup"><span data-stu-id="22022-122">To search for a phrase as if it were a single word, enclose the phrase in double quotation marks.</span></span>

<span data-ttu-id="22022-123">Cuando se usa el predicado FREETEXT, los resultados de la consulta de búsqueda devuelven documentos que contienen todos los términos de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="22022-123">When you use the FREETEXT predicate, the search query results return documents containing all of the search terms.</span></span> <span data-ttu-id="22022-124">No es necesario que los términos aparezcan en ningún orden concreto.</span><span class="sxs-lookup"><span data-stu-id="22022-124">The terms do not need to appear in any particular order.</span></span> <span data-ttu-id="22022-125">Los documentos que contienen más de los términos de búsqueda tienen valores de columna de rango más altos.</span><span class="sxs-lookup"><span data-stu-id="22022-125">Documents that contain more of the search terms have higher rank column values.</span></span>

## <a name="examples"></a><span data-ttu-id="22022-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="22022-126">Examples</span></span>

<span data-ttu-id="22022-127">En el siguiente ejemplo se buscan documentos que contengan "equipo", "software", "hardware" o combinaciones de esas palabras:</span><span class="sxs-lookup"><span data-stu-id="22022-127">The following example searches for documents containing "computer", "software", "hardware", or combinations of those words:</span></span>


```
WHERE FREETEXT('computer software hardware')
```



> [!Note]  
> <span data-ttu-id="22022-128">No se puede usar la coincidencia de palabra única y la coincidencia de frases en el mismo predicado FREETEXT.</span><span class="sxs-lookup"><span data-stu-id="22022-128">You cannot use both single-word matching and phrase matching in the same FREETEXT predicate.</span></span>

 

<span data-ttu-id="22022-129">Al realizar consultas con contrataciones, debe usar el carácter de escape de la comilla en la contracción cuando use FREETEXT, pero no cuando use Contains.</span><span class="sxs-lookup"><span data-stu-id="22022-129">When performing queries with contractions, you must escape the quotation mark in the contraction when using FREETEXT, but not when using CONTAINS.</span></span>

<span data-ttu-id="22022-130">Por ejemplo, se produce un error en la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="22022-130">For example, the following syntax fails:</span></span>


```
WHERE FREETEXT(*,'"We'll meet next week"')
```



<span data-ttu-id="22022-131">La sintaxis correcta incluye dos comillas simples, no una comilla doble.</span><span class="sxs-lookup"><span data-stu-id="22022-131">The correct syntax includes two single quotation marks, not a double quotation mark.</span></span>

<span data-ttu-id="22022-132">La siguiente sintaxis se realiza correctamente:</span><span class="sxs-lookup"><span data-stu-id="22022-132">The following syntax succeeds:</span></span>


```
WHERE FREETEXT(*,'"We''ll meet next week"')
```



## <a name="related-topics"></a><span data-ttu-id="22022-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="22022-133">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="22022-134">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="22022-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="22022-135">Predicado CONTAINS</span><span class="sxs-lookup"><span data-stu-id="22022-135">CONTAINS Predicate</span></span>](-search-sql-contains.md)
</dt> <dt>

[<span data-ttu-id="22022-136">Cláusula WHERE</span><span class="sxs-lookup"><span data-stu-id="22022-136">WHERE Clause</span></span>](-search-sql-where.md)
</dt> <dt>

<span data-ttu-id="22022-137">**Vista**</span><span class="sxs-lookup"><span data-stu-id="22022-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="22022-138">Predicados que no son de texto completo</span><span class="sxs-lookup"><span data-stu-id="22022-138">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



