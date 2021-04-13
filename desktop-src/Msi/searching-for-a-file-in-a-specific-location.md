---
description: Durante una instalación Windows Installer, el instalador puede buscar un archivo en una ubicación específica en el sistema del usuario.
ms.assetid: 127d83a2-b651-42ef-ac7c-a7fa1b15cf27
title: Buscar un archivo en una ubicación específica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ad4e456d331119b698d8e6e696e86b953006eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546022"
---
# <a name="searching-for-a-file-in-a-specific-location"></a><span data-ttu-id="260dc-103">Buscar un archivo en una ubicación específica</span><span class="sxs-lookup"><span data-stu-id="260dc-103">Searching for a File in a Specific Location</span></span>

<span data-ttu-id="260dc-104">**Para buscar un archivo en una ubicación específica en un sistema de usuarios**</span><span class="sxs-lookup"><span data-stu-id="260dc-104">**To search for a file in a specific location on a user system**</span></span>

1.  <span data-ttu-id="260dc-105">Enumere la firma y el nombre del archivo en la [tabla de firmas](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="260dc-105">List the file signature and name in the [Signature Table](signature-table.md).</span></span> <span data-ttu-id="260dc-106">Los campos restantes de este registro pueden ser null para buscar cualquier versión de MyApp.exe.</span><span class="sxs-lookup"><span data-stu-id="260dc-106">The remaining fields in this record can be null to search for any version of MyApp.exe.</span></span>

    [<span data-ttu-id="260dc-107">Tabla de firmas</span><span class="sxs-lookup"><span data-stu-id="260dc-107">Signature Table</span></span>](signature-table.md)

    

    | <span data-ttu-id="260dc-108">Firma</span><span class="sxs-lookup"><span data-stu-id="260dc-108">Signature</span></span>          | <span data-ttu-id="260dc-109">Nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="260dc-109">File name</span></span>            |
    |--------------------|----------------------|
    | <span data-ttu-id="260dc-110">AppFile</span><span class="sxs-lookup"><span data-stu-id="260dc-110">AppFile</span></span><br/> | <span data-ttu-id="260dc-111">MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="260dc-111">MyApp.exe</span></span><br/> |

    

     

2.  <span data-ttu-id="260dc-112">Escriba la propiedad que el instalador va a establecer si MyApp.exe está instalado.</span><span class="sxs-lookup"><span data-stu-id="260dc-112">Enter the property that the Installer is to set if MyApp.exe is installed.</span></span>

    <span data-ttu-id="260dc-113">[Tabla AppSearch](appsearch-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="260dc-113">[AppSearch Table](appsearch-table.md) (partial)</span></span>

    

    | <span data-ttu-id="260dc-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="260dc-114">Property</span></span>         | <span data-ttu-id="260dc-115">Firma</span><span class="sxs-lookup"><span data-stu-id="260dc-115">Signature</span></span>          |
    |------------------|--------------------|
    | <span data-ttu-id="260dc-116">MYAPP</span><span class="sxs-lookup"><span data-stu-id="260dc-116">MYAPP</span></span><br/> | <span data-ttu-id="260dc-117">AppFile</span><span class="sxs-lookup"><span data-stu-id="260dc-117">AppFile</span></span><br/> |

    

     

3.  <span data-ttu-id="260dc-118">Use la [tabla DrLocator](drlocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="260dc-118">Use the [DrLocator Table](drlocator-table.md).</span></span> <span data-ttu-id="260dc-119">Escriba la ruta de acceso completa al archivo en el sistema de usuario en el campo ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="260dc-119">Enter the full path to the file on the user system in the Path field.</span></span> <span data-ttu-id="260dc-120">Escriba un valor de 0 en la columna de profundidad para buscar en la carpeta bin.</span><span class="sxs-lookup"><span data-stu-id="260dc-120">Enter a value of 0 into the Depth column to search the bin folder.</span></span>

    [<span data-ttu-id="260dc-121">Tabla DrLocator</span><span class="sxs-lookup"><span data-stu-id="260dc-121">DrLocator Table</span></span>](drlocator-table.md)

    

    | <span data-ttu-id="260dc-122">Firma</span><span class="sxs-lookup"><span data-stu-id="260dc-122">Signature</span></span>          | <span data-ttu-id="260dc-123">Parent</span><span class="sxs-lookup"><span data-stu-id="260dc-123">Parent</span></span> | <span data-ttu-id="260dc-124">Ruta</span><span class="sxs-lookup"><span data-stu-id="260dc-124">Path</span></span>                                                    | <span data-ttu-id="260dc-125">Profundidad</span><span class="sxs-lookup"><span data-stu-id="260dc-125">Depth</span></span>        |
    |--------------------|--------|---------------------------------------------------------|--------------|
    | <span data-ttu-id="260dc-126">AppFile</span><span class="sxs-lookup"><span data-stu-id="260dc-126">AppFile</span></span><br/> |        | <span data-ttu-id="260dc-127">C: \\ archivos de programa \\ suproducts \\ bin de proyectos \\</span><span class="sxs-lookup"><span data-stu-id="260dc-127">C:\\Program Files\\MyProducts\\Projects\\bin</span></span><br/> | <span data-ttu-id="260dc-128">0</span><span class="sxs-lookup"><span data-stu-id="260dc-128">0</span></span><br/> |

    

     

4.  <span data-ttu-id="260dc-129">Incluya la acción AppSearch en la secuencia de acciones.</span><span class="sxs-lookup"><span data-stu-id="260dc-129">Include the AppSearch action in the action sequence.</span></span> <span data-ttu-id="260dc-130">Si MyApp.exe está instalado en C: \\ archivos de programa \\ suproducts \\ \\ bin, el instalador establece la propiedad MyApp en la ubicación del archivo.</span><span class="sxs-lookup"><span data-stu-id="260dc-130">If MyApp.exe is installed in C:\\Program Files\\MyProducts\\Projects\\bin, the Installer sets the property MYAPP to the location of file.</span></span>

 

 




