---
description: Durante una instalación Windows Installer, el instalador puede buscar un archivo y crear una propiedad que contenga la ruta de acceso del archivo.
ms.assetid: 6587b349-852d-4d4e-a8d4-76dfb0ef0f0b
title: Buscar un archivo y crear una propiedad que contiene la ruta de acceso del archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed742ee874c2e4b76137e9f17e90fbf54e9729f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910682"
---
# <a name="searching-for-a-file-and-creating-a-property-holding-the-files-path"></a><span data-ttu-id="23d69-103">Buscar un archivo y crear una propiedad que contiene la ruta de acceso del archivo</span><span class="sxs-lookup"><span data-stu-id="23d69-103">Searching for a File and Creating a Property Holding the File's Path</span></span>

<span data-ttu-id="23d69-104">**Para buscar un archivo y crear una propiedad que contenga la ruta de acceso de ese archivo**</span><span class="sxs-lookup"><span data-stu-id="23d69-104">**To search for a file and create a property holding the path of that file**</span></span>

1.  <span data-ttu-id="23d69-105">En primer lugar, realice una búsqueda del archivo enumerando la firma y el nombre del archivo en la [tabla de firma](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="23d69-105">First do a search for the file by listing the file signature and name in the [Signature Table](signature-table.md).</span></span>

    <span data-ttu-id="23d69-106">Los campos restantes de este registro pueden dejarse vacíos para especificar una búsqueda de cualquier versión de MyApp.exe.</span><span class="sxs-lookup"><span data-stu-id="23d69-106">The remaining fields of this record can be left empty to specify a search for any version of MyApp.exe.</span></span>

    <span data-ttu-id="23d69-107">[Tabla de firmas](signature-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="23d69-107">[Signature Table](signature-table.md) (partial)</span></span>

    

    | <span data-ttu-id="23d69-108">Firma</span><span class="sxs-lookup"><span data-stu-id="23d69-108">Signature</span></span>          | <span data-ttu-id="23d69-109">Nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="23d69-109">File name</span></span>            |
    |--------------------|----------------------|
    | <span data-ttu-id="23d69-110">AppFile</span><span class="sxs-lookup"><span data-stu-id="23d69-110">AppFile</span></span><br/> | <span data-ttu-id="23d69-111">MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="23d69-111">MyApp.exe</span></span><br/> |

    

     

2.  <span data-ttu-id="23d69-112">A continuación, especifique la ruta de acceso del archivo que se va a buscar en la [tabla DrLocator](drlocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="23d69-112">Next, specify the path of the file that is being searched for in the [DrLocator Table](drlocator-table.md).</span></span>

    <span data-ttu-id="23d69-113">Dado que AppFolder no aparece en la [tabla de firmas](signature-table.md), el instalador determina que AppFolder es una carpeta en lugar de un archivo.</span><span class="sxs-lookup"><span data-stu-id="23d69-113">Because AppFolder is not listed in the [Signature Table](signature-table.md), the Installer determines that AppFolder is a folder rather than a file.</span></span>

    [<span data-ttu-id="23d69-114">Tabla DrLocator</span><span class="sxs-lookup"><span data-stu-id="23d69-114">DrLocator Table</span></span>](drlocator-table.md)

    

    | <span data-ttu-id="23d69-115">Firma</span><span class="sxs-lookup"><span data-stu-id="23d69-115">Signature</span></span>            | <span data-ttu-id="23d69-116">Parent</span><span class="sxs-lookup"><span data-stu-id="23d69-116">Parent</span></span>             | <span data-ttu-id="23d69-117">Ruta</span><span class="sxs-lookup"><span data-stu-id="23d69-117">Path</span></span> | <span data-ttu-id="23d69-118">Profundidad</span><span class="sxs-lookup"><span data-stu-id="23d69-118">Depth</span></span> |
    |----------------------|--------------------|------|-------|
    | <span data-ttu-id="23d69-119">AppFile</span><span class="sxs-lookup"><span data-stu-id="23d69-119">AppFile</span></span><br/>   |                    |      |       |
    | <span data-ttu-id="23d69-120">AppFolder</span><span class="sxs-lookup"><span data-stu-id="23d69-120">AppFolder</span></span><br/> | <span data-ttu-id="23d69-121">AppFile</span><span class="sxs-lookup"><span data-stu-id="23d69-121">AppFile</span></span><br/> |      |       |

    

     

3.  <span data-ttu-id="23d69-122">Por último, rellene la [tabla AppSearch](appsearch-table.md) para que la [acción AppSearch](appsearch-action.md) devuelva la ruta de acceso de AppFolder.</span><span class="sxs-lookup"><span data-stu-id="23d69-122">Finally, populate the [AppSearch Table](appsearch-table.md) so that the [AppSearch Action](appsearch-action.md) returns the path of AppFolder.</span></span>

    <span data-ttu-id="23d69-123">Después de que el instalador ejecute la acción AppSearch, el valor de mi carpeta es la ruta de acceso completa de AppFolder.</span><span class="sxs-lookup"><span data-stu-id="23d69-123">After the Installer executes the AppSearch action, the value of MYFOLDER is the full path of AppFolder.</span></span>

    <span data-ttu-id="23d69-124">[Tabla AppSearch](appsearch-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="23d69-124">[AppSearch Table](appsearch-table.md) (partial)</span></span>

    

    | <span data-ttu-id="23d69-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="23d69-125">Property</span></span>            | <span data-ttu-id="23d69-126">Firma</span><span class="sxs-lookup"><span data-stu-id="23d69-126">Signature</span></span>            |
    |---------------------|----------------------|
    | <span data-ttu-id="23d69-127">MYFOLDER</span><span class="sxs-lookup"><span data-stu-id="23d69-127">MYFOLDER</span></span><br/> | <span data-ttu-id="23d69-128">AppFolder</span><span class="sxs-lookup"><span data-stu-id="23d69-128">AppFolder</span></span><br/> |

    

     

 

 




