---
title: Solo atributos de búsqueda
description: A veces, realiza una búsqueda para determinar qué tipo de datos están disponibles para un objeto.
ms.assetid: 97eccea6-6a2b-4785-afd8-4af3dc7bd657
ms.tgt_platform: multiple
keywords:
- Atributos de búsqueda solo ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c2a97873dfb52f56b123919c3eedd277a63a74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993843"
---
# <a name="search-attributes-only"></a><span data-ttu-id="912b1-104">Solo atributos de búsqueda</span><span class="sxs-lookup"><span data-stu-id="912b1-104">Search Attributes Only</span></span>

<span data-ttu-id="912b1-105">A veces, realiza una búsqueda para determinar qué tipo de datos están disponibles para un objeto.</span><span class="sxs-lookup"><span data-stu-id="912b1-105">Sometimes you perform a search to determine what type of data is available for an object.</span></span> <span data-ttu-id="912b1-106">En este caso, solo le interesan los atributos y no los valores del objeto.</span><span class="sxs-lookup"><span data-stu-id="912b1-106">In this case, you are interested only in the attributes, and not the values, of the object.</span></span> <span data-ttu-id="912b1-107">Para ello, establezca la opción "solo atributos de búsqueda".</span><span class="sxs-lookup"><span data-stu-id="912b1-107">To accomplish this, you set the "search attributes only" option.</span></span> <span data-ttu-id="912b1-108">Al especificar esta opción, se devuelven los nombres de atributo sin sus valores.</span><span class="sxs-lookup"><span data-stu-id="912b1-108">Specifying this option returns the attribute names without their values.</span></span> <span data-ttu-id="912b1-109">Sin embargo, el conjunto de resultados incluye solo los atributos que tienen valores asignados.</span><span class="sxs-lookup"><span data-stu-id="912b1-109">However, the result set includes only those attributes that have values assigned.</span></span> <span data-ttu-id="912b1-110">Por ejemplo, considere un objeto con los siguientes atributos:</span><span class="sxs-lookup"><span data-stu-id="912b1-110">For example, consider an object with the following attributes:</span></span>

``` syntax
First Name = Jeff
Last Name = Smith
Department = <Empty>
Phone Number = (425) 432-3442
```

<span data-ttu-id="912b1-111">Cuando se establece la opción solo atributos de búsqueda, el conjunto de resultados incluye:</span><span class="sxs-lookup"><span data-stu-id="912b1-111">When the search attributes only option is set, the result set includes:</span></span>

``` syntax
First Name
Last Name
Phone Number
```

<span data-ttu-id="912b1-112">Para obtener más información sobre cómo usar la opción solo atributos de búsqueda con una interfaz de búsqueda específica, vea:</span><span class="sxs-lookup"><span data-stu-id="912b1-112">For more information about using the search attributes only option with a specific search interface, see:</span></span>

-   [<span data-ttu-id="912b1-113">Devolver solo nombres de atributo con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="912b1-113">Returning Only Attribute Names with IDirectorySearch</span></span>](returning-only-attribute-names-with-idirectorysearch.md)
-   [<span data-ttu-id="912b1-114">Buscar con Objetos de datos ActiveX</span><span class="sxs-lookup"><span data-stu-id="912b1-114">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="912b1-115">Buscar con OLE DB</span><span class="sxs-lookup"><span data-stu-id="912b1-115">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




