---
title: Cómo funciona la indexación de tuplas
description: Los índices de tupla se usan para optimizar las búsquedas que tienen 0 o más cadenas de búsqueda medial y 0 o 1 cadenas de búsqueda final. También se pueden utilizar para optimizar las búsquedas de una cadena de búsqueda inicial si no hay ningún índice ordinario disponible sobre ese atributo.
ms.assetid: 0f7b3f64-70cd-4581-a9ab-bb882eabef8c
ms.tgt_platform: multiple
keywords:
- indexación de tuplas
- Buscar Active Directory de Active Directory, optimización
- Active Directory, optimización de búsqueda Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607b9a50ef0ec367bea95f82afd89aa39fbf5b1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789514"
---
# <a name="how-tuple-indexing-works"></a><span data-ttu-id="2e2ee-107">Cómo funciona la indexación de tuplas</span><span class="sxs-lookup"><span data-stu-id="2e2ee-107">How Tuple Indexing Works</span></span>

<span data-ttu-id="2e2ee-108">Los índices de tupla se usan para optimizar las búsquedas que tienen 0 o más [cadenas de búsqueda medial](search-string-types.md) y 0 o 1 cadenas de búsqueda final.</span><span class="sxs-lookup"><span data-stu-id="2e2ee-108">Tuple indices are used to optimize searches that have 0 or more [medial-search strings](search-string-types.md) and 0 or 1 final-search strings.</span></span> <span data-ttu-id="2e2ee-109">También se pueden utilizar para optimizar las búsquedas de una cadena de búsqueda inicial si no hay ningún índice ordinario disponible sobre ese atributo.</span><span class="sxs-lookup"><span data-stu-id="2e2ee-109">They can also be used to optimize searches for an initial search string if no ordinary index is available over that attribute.</span></span>

<span data-ttu-id="2e2ee-110">Puede activar la indexación de tupla para un atributo estableciendo el bit 5, que corresponde al valor 32, en el atributo [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) .</span><span class="sxs-lookup"><span data-stu-id="2e2ee-110">You can turn on tuple indexing for an attribute by setting bit 5, which corresponds to the value 32, in the [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) attribute.</span></span> <span data-ttu-id="2e2ee-111">Este atributo se establece en el objeto de esquema que representa el atributo que necesita el índice de tupla.</span><span class="sxs-lookup"><span data-stu-id="2e2ee-111">This attribute is set in the schema object that represents the attribute that needs the tuple index.</span></span> <span data-ttu-id="2e2ee-112">El impacto en el rendimiento de la activación de la indización de tupla es que cualquier valor de cadena establecido para ese atributo se expandirá en un gran número de fragmentos en el índice de la tupla.</span><span class="sxs-lookup"><span data-stu-id="2e2ee-112">The performance impact of turning on tuple indexing is that any string value that is set for that attribute will be expanded into a large number of fragments in the tuple index.</span></span> <span data-ttu-id="2e2ee-113">Cuando se expande un atributo, consume una cantidad mayor de espacio en disco en el archivo de árbol de información del directorio y también se actualiza más lentamente.</span><span class="sxs-lookup"><span data-stu-id="2e2ee-113">When an attribute expands, it consumes a larger amount of disk space in the Directory Information Tree file, and also gets updated more slowly.</span></span>

<span data-ttu-id="2e2ee-114">Los índices de tupla están diseñados para acelerar las búsquedas del formulario `*string*` .</span><span class="sxs-lookup"><span data-stu-id="2e2ee-114">Tuple indices are designed to accelerate searches of the form `*string*`.</span></span> <span data-ttu-id="2e2ee-115">La aceleración puede ser considerable porque esta forma de búsqueda no se puede optimizar de otra manera, y en su forma no optimizada, obliga al servidor Active Directory a recorrer todos los objetos del ámbito de la búsqueda para realizar la consulta.</span><span class="sxs-lookup"><span data-stu-id="2e2ee-115">The acceleration can be considerable because this form of search cannot be optimized in any other way, and in its un-optimized form, it forces the Active Directory server to walk every object in the scope of the search to perform the query.</span></span> <span data-ttu-id="2e2ee-116">Por lo tanto, una búsqueda base simplemente buscaría un objeto, que utilizaría menos recursos, una búsqueda secundaria inmediata buscaría solo los elementos secundarios de un objeto (que podría usar menos recursos o más recursos en función del tamaño del contenedor) y una búsqueda de subárbol recorrerá todo el subárbol bajo el objeto base, que normalmente requeriría una gran cantidad de recursos y ser muy lento debido al tamaño del subárbol.</span><span class="sxs-lookup"><span data-stu-id="2e2ee-116">Thus, a base search would just search one object, which would use fewer resources, an immediate children search would search just the children of an object (which could use fewer resources or more resources depending on the container size), and a subtree search will walk the entire subtree under the base object, which would usually require a lot of resources and be very slow because of the subtree size.</span></span>

<span data-ttu-id="2e2ee-117">Los índices de tupla funcionan dividiendo una cadena en *tuplas*.</span><span class="sxs-lookup"><span data-stu-id="2e2ee-117">Tuple indices work by breaking a string into *tuples*.</span></span> <span data-ttu-id="2e2ee-118">Por ejemplo, la cadena "Active Directory" se dividiría en las siguientes tuplas:</span><span class="sxs-lookup"><span data-stu-id="2e2ee-118">For example, the string "Active Directory" would be broken into the following tuples:</span></span>

-   ` "Active Dir"`
-   ` "ctive Dire"`
-   ` "tive Direc"`
-   ` "ive Direct"`
-   ` "ve Directo"`
-   ` "e Director"`
-   ` " Directory"`
-   ` "Directory"`
-   ` "irectory"`
-   ` "rectory"`
-   ` "ectory"`
-   ` "ctory"`
-   ` "tory"`
-   ` "ory"`

> [!Note]  
> <span data-ttu-id="2e2ee-119">El directorio se detendrá en 32767 caracteres al expandir una cadena para la indexación de tupla.</span><span class="sxs-lookup"><span data-stu-id="2e2ee-119">The directory will stop at 32767 characters when expanding a string for tuple indexing.</span></span>

 

<span data-ttu-id="2e2ee-120">Un índice de tupla contiene una entrada para cada una de estas tuplas.</span><span class="sxs-lookup"><span data-stu-id="2e2ee-120">A tuple index would contain an entry for each one of these tuples.</span></span> <span data-ttu-id="2e2ee-121">Por lo tanto, si un usuario busca `*cto*` , el servidor de Active Directory buscará todas las coincidencias de "CTO" en el índice y, en este caso, buscará un puntero de nuevo al registro que tenía un atributo (índice de tupla) con un valor de "Directory".</span><span class="sxs-lookup"><span data-stu-id="2e2ee-121">So, if a user searches for `*cto*`, then the Active Directory server will look up all the matches for "cto" in the index and, in this case, find a pointer back to the record that had a (tuple indexed) attribute with a value of "Directory".</span></span>

<span data-ttu-id="2e2ee-122">Si la cadena de búsqueda medial ( `*cto*` en el ejemplo anterior) es lo suficientemente específica, la búsqueda será bastante eficaz porque reduce en gran medida el número de objetos que el servidor de Active Directory debe inspeccionar para realizar la consulta.</span><span class="sxs-lookup"><span data-stu-id="2e2ee-122">If the medial search string (`*cto*` in the previous example) is specific enough, then the search will be quite efficient because it greatly reduces the number of objects that the Active Directory server must inspect to perform the query.</span></span>

 

 