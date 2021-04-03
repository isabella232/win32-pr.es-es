---
description: Durante una instalación Windows Installer, el instalador puede buscar una entrada del registro y crear una propiedad que contenga el valor del registro.
ms.assetid: 3a663fc7-cdcf-4ac3-8251-836ba0d3cc11
title: Buscar una entrada del registro y crear una propiedad que contiene el valor del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82bd7572c0176f4870eed199800715190d9bbbf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907685"
---
# <a name="searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry"></a><span data-ttu-id="bd90a-103">Buscar una entrada del registro y crear una propiedad que contiene el valor del registro</span><span class="sxs-lookup"><span data-stu-id="bd90a-103">Searching for a Registry Entry and Creating a Property Holding the Value of the Registry</span></span>

<span data-ttu-id="bd90a-104">**Para buscar una entrada del registro y crear una propiedad que contenga el valor de ese archivo**</span><span class="sxs-lookup"><span data-stu-id="bd90a-104">**To search for a registry entry and create a property holding the value of that file**</span></span>

1.  <span data-ttu-id="bd90a-105">No agregue la firma a la [tabla de firma](signature-table.md) o a la [tabla CompLocator](complocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="bd90a-105">Do not add the signature to the [Signature Table](signature-table.md) or the [CompLocator Table](complocator-table.md).</span></span> <span data-ttu-id="bd90a-106">Si una firma de archivo se muestra en la [tabla AppSearch](appsearch-table.md) y no aparece en las tablas Signature o CompLocator, el instalador busca en la [tabla RegLocator](reglocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="bd90a-106">If a file signature is listed in the [AppSearch Table](appsearch-table.md) and is not listed in the Signature or CompLocator tables, the Installer looks in the [RegLocator Table](reglocator-table.md).</span></span>

2.  <span data-ttu-id="bd90a-107">Especifique la entrada del registro que se va a buscar en la [tabla RegLocator](reglocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="bd90a-107">Specify the registry entry to be searched for in the [RegLocator Table](reglocator-table.md).</span></span> <span data-ttu-id="bd90a-108">Si la firma no está presente en la [tabla de signatura](signature-table.md) y el valor de la columna Type es **msidbLocatorTypeRawValue**, se supone que la búsqueda es para el nombre de clave del registro específico al que apunta la tabla RegLocator.</span><span class="sxs-lookup"><span data-stu-id="bd90a-108">If the signature is absent from the [Signature Table](signature-table.md) and the value of the Type column is **msidbLocatorTypeRawValue**, then the search is assumed to be for the specific registry key name pointed to by the RegLocator Table.</span></span>

    <span data-ttu-id="bd90a-109">[Tabla RegLocator](reglocator-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="bd90a-109">[RegLocator Table](reglocator-table.md) (partial)</span></span>

    

    | <span data-ttu-id="bd90a-110">Signatura\_</span><span class="sxs-lookup"><span data-stu-id="bd90a-110">Signature\_</span></span>         | <span data-ttu-id="bd90a-111">Root</span><span class="sxs-lookup"><span data-stu-id="bd90a-111">Root</span></span>         | <span data-ttu-id="bd90a-112">Clave</span><span class="sxs-lookup"><span data-stu-id="bd90a-112">Key</span></span>                                                           | <span data-ttu-id="bd90a-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="bd90a-113">Name</span></span>                  | <span data-ttu-id="bd90a-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="bd90a-114">Type</span></span>                                    |
    |---------------------|--------------|---------------------------------------------------------------|-----------------------|-----------------------------------------|
    | <span data-ttu-id="bd90a-115">AppValue</span><span class="sxs-lookup"><span data-stu-id="bd90a-115">AppValue</span></span><br/> | <span data-ttu-id="bd90a-116">2</span><span class="sxs-lookup"><span data-stu-id="bd90a-116">2</span></span><br/> | <span data-ttu-id="bd90a-117">**Software** \\ de **Microsoft** \\ **MyApp**</span><span class="sxs-lookup"><span data-stu-id="bd90a-117">**SOFTWARE**\\**Microsoft**\\**MyApp**</span></span><br/> <br/> | <span data-ttu-id="bd90a-118">**Myname**</span><span class="sxs-lookup"><span data-stu-id="bd90a-118">**Myname**</span></span><br/> | <span data-ttu-id="bd90a-119">**msidbLocatorTypeRawValue**</span><span class="sxs-lookup"><span data-stu-id="bd90a-119">**msidbLocatorTypeRawValue**</span></span><br/> |

    

     

3.  <span data-ttu-id="bd90a-120">Por último, rellene la [tabla AppSearch](appsearch-table.md) para que la [acción AppSearch](appsearch-action.md) devuelva el valor de AppValue.</span><span class="sxs-lookup"><span data-stu-id="bd90a-120">Finally, populate the [AppSearch Table](appsearch-table.md) so that the [AppSearch Action](appsearch-action.md) returns the value of AppValue.</span></span> <span data-ttu-id="bd90a-121">Después de que el instalador ejecute la acción AppSearch, el valor de MYREGVAL es el valor de AppValue.</span><span class="sxs-lookup"><span data-stu-id="bd90a-121">After the Installer executes the AppSearch Action, the value of MYREGVAL is the value of AppValue.</span></span>

    <span data-ttu-id="bd90a-122">[Tabla AppSearch](appsearch-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="bd90a-122">[AppSearch Table](appsearch-table.md) (partial)</span></span>

    

    | <span data-ttu-id="bd90a-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bd90a-123">Property</span></span>            | <span data-ttu-id="bd90a-124">Firma</span><span class="sxs-lookup"><span data-stu-id="bd90a-124">Signature</span></span>           |
    |---------------------|---------------------|
    | <span data-ttu-id="bd90a-125">MYREGVAL</span><span class="sxs-lookup"><span data-stu-id="bd90a-125">MYREGVAL</span></span><br/> | <span data-ttu-id="bd90a-126">AppValue</span><span class="sxs-lookup"><span data-stu-id="bd90a-126">AppValue</span></span><br/> |

    

     

 

 




