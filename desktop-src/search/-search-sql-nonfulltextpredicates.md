---
description: El lenguaje de consulta de Microsoft Windows Search admite seis predicados de búsqueda que no son de texto completo. Los predicados descritos en esta sección se enumeran en la tabla siguiente.
ms.assetid: 74aa6dbc-5c0d-433e-96d9-a8db63907342
title: Predicados que no son de texto completo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d41076ebc61aa56ed547f13f717ac40bed35959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705482"
---
# <a name="non-full-text-predicates"></a><span data-ttu-id="5897a-104">Predicados que no son de texto completo</span><span class="sxs-lookup"><span data-stu-id="5897a-104">Non-Full-Text Predicates</span></span>

<span data-ttu-id="5897a-105">El lenguaje de consulta de Microsoft Windows Search admite seis predicados de búsqueda que no son de texto completo.</span><span class="sxs-lookup"><span data-stu-id="5897a-105">The Microsoft Windows Search query language supports six non-full-text search predicates.</span></span> <span data-ttu-id="5897a-106">Los predicados descritos en esta sección se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="5897a-106">The predicates described in this section are listed in the following table.</span></span>



| <span data-ttu-id="5897a-107">Predicado de texto no completo</span><span class="sxs-lookup"><span data-stu-id="5897a-107">Non-full-text predicate</span></span>                                                    | <span data-ttu-id="5897a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="5897a-108">Description</span></span>                                                                                                                                                                             |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5897a-109">ALL bit a bit y SOME</span><span class="sxs-lookup"><span data-stu-id="5897a-109">ALL BITWISE and SOME BITWISE</span></span>](all-bitwise.md)                            | <span data-ttu-id="5897a-110">Es un conjunto de palabras clave que se van a probar los bits de un tipo entero.</span><span class="sxs-lookup"><span data-stu-id="5897a-110">Is a set of keywords that are about testing the bits in an integral type.</span></span>                                                                                                               |
| [<span data-ttu-id="5897a-111">DATEADD (función)</span><span class="sxs-lookup"><span data-stu-id="5897a-111">DATEADD Function</span></span>](-search-sql-dateadd.md)                                | <span data-ttu-id="5897a-112">Realiza cálculos de fecha y hora para las propiedades coincidentes que tienen tipos de fecha.</span><span class="sxs-lookup"><span data-stu-id="5897a-112">Performs time and date calculations for matching properties having date types.</span></span> <span data-ttu-id="5897a-113">Utilice la función DATEADD para obtener fechas y horas en un período de tiempo especificado antes de la presente.</span><span class="sxs-lookup"><span data-stu-id="5897a-113">Use the DATEADD function to obtain dates and times in a specified amount of time before the present.</span></span>     |
| [<span data-ttu-id="5897a-114">LIKE (predicado)</span><span class="sxs-lookup"><span data-stu-id="5897a-114">LIKE Predicate</span></span>](-search-sql-like.md)                                     | <span data-ttu-id="5897a-115">Compara los valores de columna utilizando la coincidencia de patrones simple con caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="5897a-115">Compares column values using simple pattern matching with wildcard characters.</span></span>                                                                                                          |
| [<span data-ttu-id="5897a-116">Comparación de valores literales</span><span class="sxs-lookup"><span data-stu-id="5897a-116">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)         | <span data-ttu-id="5897a-117">Compara los valores de columna con cadena, fecha, marca de tiempo, numérico y otros valores literales.</span><span class="sxs-lookup"><span data-stu-id="5897a-117">Compares column values against string, date, time stamp, numeric, and other literal values.</span></span> <span data-ttu-id="5897a-118">Este predicado admite desigualdades como mayor que (' > ') y menor que (' < ').</span><span class="sxs-lookup"><span data-stu-id="5897a-118">This predicate supports inequalities such as greater than ('>'), and less than ('<').</span></span> |
| [<span data-ttu-id="5897a-119">Comparaciones de varios valores (matriz)</span><span class="sxs-lookup"><span data-stu-id="5897a-119">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md) | <span data-ttu-id="5897a-120">Compara las columnas de varios valores con una matriz de literales de varios valores.</span><span class="sxs-lookup"><span data-stu-id="5897a-120">Compares multivalued columns against a multivalued array of literals.</span></span>                                                                                                                   |
| [<span data-ttu-id="5897a-121">Predicado NULL</span><span class="sxs-lookup"><span data-stu-id="5897a-121">NULL Predicate</span></span>](-search-sql-null.md)                                     | <span data-ttu-id="5897a-122">Detecta los valores de columna que no están definidos para el documento.</span><span class="sxs-lookup"><span data-stu-id="5897a-122">Detects column values that are undefined for the document.</span></span>                                                                                                                              |



 

> [!IMPORTANT]
> <span data-ttu-id="5897a-123">Las consultas de búsqueda que usan el predicado **null** pueden requerir que búsqueda de Windows Examine todo el catálogo, lo que puede ralentizar el rendimiento de la consulta.</span><span class="sxs-lookup"><span data-stu-id="5897a-123">Search queries using the **NULL** predicate can require that Windows Search scan the entire catalog, which might slow down the query's performance.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5897a-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5897a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5897a-125">Predicados de texto completo</span><span class="sxs-lookup"><span data-stu-id="5897a-125">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> </dl>

 

 



