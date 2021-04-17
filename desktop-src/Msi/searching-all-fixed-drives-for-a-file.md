---
description: Durante una instalación Windows Installer, el instalador puede buscar un archivo en todas las unidades fijas.
ms.assetid: c8aa84a8-5525-4a12-898f-63dc30113b13
title: Buscar un archivo en todas las unidades fijas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b79c7f2999d4ee7937790dc68470210f1d4b2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678031"
---
# <a name="searching-all-fixed-drives-for-a-file"></a><span data-ttu-id="447be-103">Buscar un archivo en todas las unidades fijas</span><span class="sxs-lookup"><span data-stu-id="447be-103">Searching All Fixed Drives for a File</span></span>

<span data-ttu-id="447be-104">**Para buscar un archivo en todas las unidades fijas**</span><span class="sxs-lookup"><span data-stu-id="447be-104">**To search all fixed drives for a file**</span></span>

1.  <span data-ttu-id="447be-105">Escriba la firma y el nombre del archivo en la [tabla de firmas](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="447be-105">Enter the file signature and name in the [Signature Table](signature-table.md).</span></span> <span data-ttu-id="447be-106">Los campos restantes de este registro pueden ser null para buscar cualquier versión de MyApp.exe.</span><span class="sxs-lookup"><span data-stu-id="447be-106">The remaining fields in this record can be null to search for any version of MyApp.exe.</span></span>

    <span data-ttu-id="447be-107">[Tabla de firmas](signature-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="447be-107">[Signature Table](signature-table.md) (partial)</span></span>

    

    | <span data-ttu-id="447be-108">Firma</span><span class="sxs-lookup"><span data-stu-id="447be-108">Signature</span></span>          | <span data-ttu-id="447be-109">Nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="447be-109">File Name</span></span>            |
    |--------------------|----------------------|
    | <span data-ttu-id="447be-110">AppFile</span><span class="sxs-lookup"><span data-stu-id="447be-110">AppFile</span></span><br/> | <span data-ttu-id="447be-111">MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="447be-111">MyApp.exe</span></span><br/> |

    

     

2.  <span data-ttu-id="447be-112">Escriba la propiedad que el instalador va a establecer si MyApp.exe está instalado.</span><span class="sxs-lookup"><span data-stu-id="447be-112">Enter the property that the Installer is to set if MyApp.exe is installed.</span></span>

    [<span data-ttu-id="447be-113">Tabla AppSearch</span><span class="sxs-lookup"><span data-stu-id="447be-113">AppSearch Table</span></span>](appsearch-table.md)

    

    | <span data-ttu-id="447be-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="447be-114">Property</span></span>         | <span data-ttu-id="447be-115">Firma</span><span class="sxs-lookup"><span data-stu-id="447be-115">Signature</span></span>          |
    |------------------|--------------------|
    | <span data-ttu-id="447be-116">MYAPP</span><span class="sxs-lookup"><span data-stu-id="447be-116">MYAPP</span></span><br/> | <span data-ttu-id="447be-117">AppFile</span><span class="sxs-lookup"><span data-stu-id="447be-117">AppFile</span></span><br/> |

    

     

3.  <span data-ttu-id="447be-118">Use la [tabla DrLocator](drlocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="447be-118">Use the [DrLocator Table](drlocator-table.md).</span></span> <span data-ttu-id="447be-119">Deje vacíos los campos primario y de ruta de acceso para buscar en todas las unidades fijas del sistema de usuario.</span><span class="sxs-lookup"><span data-stu-id="447be-119">Leave the Parent and Path fields empty to search all fixed drives of the user system.</span></span> <span data-ttu-id="447be-120">Especifique en la columna profundidad el número de niveles de subdirectorio que se van a buscar.</span><span class="sxs-lookup"><span data-stu-id="447be-120">Specify in the Depth column the number of subdirectory levels to search.</span></span> <span data-ttu-id="447be-121">Por ejemplo, establecer Depth en 0 detecta c: \\MyApp.exe, pero no detecta el archivo a una profundidad de 2, por ejemplo: c: archivos de \\ programa \\ mis aplicaciones \\MyApp.exe.</span><span class="sxs-lookup"><span data-stu-id="447be-121">For example, setting Depth to 0 detects c:\\MyApp.exe, but does not detect the file at a depth of 2, for example: c:\\Program Files\\MyApps\\MyApp.exe.</span></span>

    [<span data-ttu-id="447be-122">Tabla DrLocator</span><span class="sxs-lookup"><span data-stu-id="447be-122">DrLocator Table</span></span>](drlocator-table.md)

    

    | <span data-ttu-id="447be-123">Firma</span><span class="sxs-lookup"><span data-stu-id="447be-123">Signature</span></span>          | <span data-ttu-id="447be-124">Parent</span><span class="sxs-lookup"><span data-stu-id="447be-124">Parent</span></span> | <span data-ttu-id="447be-125">Ruta</span><span class="sxs-lookup"><span data-stu-id="447be-125">Path</span></span> | <span data-ttu-id="447be-126">Profundidad</span><span class="sxs-lookup"><span data-stu-id="447be-126">Depth</span></span>        |
    |--------------------|--------|------|--------------|
    | <span data-ttu-id="447be-127">AppFile</span><span class="sxs-lookup"><span data-stu-id="447be-127">AppFile</span></span><br/> |        |      | <span data-ttu-id="447be-128">3</span><span class="sxs-lookup"><span data-stu-id="447be-128">3</span></span><br/> |

    

     

4.  <span data-ttu-id="447be-129">Incluya la acción AppSearch en la secuencia de acciones.</span><span class="sxs-lookup"><span data-stu-id="447be-129">Include the AppSearch action in the action sequence.</span></span> <span data-ttu-id="447be-130">Si MyApp.exe está instalado, el instalador establece la propiedad MYAPP en la ubicación del archivo.</span><span class="sxs-lookup"><span data-stu-id="447be-130">If MyApp.exe is installed, the Installer sets the property MYAPP to the location of the file.</span></span> <span data-ttu-id="447be-131">Si el archivo está instalado, MYAPP se evalúa como true en una expresión condicional.</span><span class="sxs-lookup"><span data-stu-id="447be-131">If the file is installed, MYAPP evaluates as True in a conditional expression.</span></span>

 

 




