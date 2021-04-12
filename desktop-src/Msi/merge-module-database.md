---
description: La base de datos de un módulo de combinación contiene todas las propiedades de instalación y la lógica de instalación del módulo.
ms.assetid: 72e42392-54e6-4be8-9a43-04158552be3d
title: Base de datos de módulo de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74158e38d10b302c28520f6c1736e9cc6d823641
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361030"
---
# <a name="merge-module-database"></a><span data-ttu-id="11808-103">Base de datos de módulo de combinación</span><span class="sxs-lookup"><span data-stu-id="11808-103">Merge Module Database</span></span>

<span data-ttu-id="11808-104">La base de datos de un módulo de combinación contiene todas las propiedades de instalación y la lógica de instalación del módulo.</span><span class="sxs-lookup"><span data-stu-id="11808-104">The database of a merge module contains all the installation properties and setup logic for the module.</span></span> <span data-ttu-id="11808-105">Básicamente es una base de [datos de instalador](installer-database.md) o un archivo. msi simplificado.</span><span class="sxs-lookup"><span data-stu-id="11808-105">It is essentially a simplified [installer database](installer-database.md) or .msi file.</span></span> <span data-ttu-id="11808-106">Los archivos de base de datos del módulo de combinación estándar se indican mediante una extensión. msm.</span><span class="sxs-lookup"><span data-stu-id="11808-106">Standard merge module database files are indicated by an .msm extension.</span></span> <span data-ttu-id="11808-107">Para obtener una lista de todas las tablas de base de datos que pueden existir en los módulos de combinación, vea [Merge Module Database tables](merge-module-database-tables.md).</span><span class="sxs-lookup"><span data-stu-id="11808-107">For a list of all database tables that can exist in merge modules, see [Merge Module Database Tables](merge-module-database-tables.md).</span></span> <span data-ttu-id="11808-108">Las tablas siguientes son necesarias en la base de datos de cada archivo. MSM:</span><span class="sxs-lookup"><span data-stu-id="11808-108">The following tables are required in the database of every .msm file:</span></span>

[<span data-ttu-id="11808-109">Componente</span><span class="sxs-lookup"><span data-stu-id="11808-109">Component</span></span>](component-table.md)

[<span data-ttu-id="11808-110">Directorio</span><span class="sxs-lookup"><span data-stu-id="11808-110">Directory</span></span>](directory-table.md)

[<span data-ttu-id="11808-111">FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="11808-111">FeatureComponents</span></span>](featurecomponents-table.md)

[<span data-ttu-id="11808-112">Archivo</span><span class="sxs-lookup"><span data-stu-id="11808-112">File</span></span>](file-table.md)

[<span data-ttu-id="11808-113">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="11808-113">ModuleSignature</span></span>](modulesignature-table.md)

[<span data-ttu-id="11808-114">ModuleComponents</span><span class="sxs-lookup"><span data-stu-id="11808-114">ModuleComponents</span></span>](modulecomponents-table.md)

<span data-ttu-id="11808-115">Tenga en cuenta que las tablas Component, Directory, FeatureComponents y File también están presentes en todos los archivos. msi.</span><span class="sxs-lookup"><span data-stu-id="11808-115">Note that the Component, Directory, FeatureComponents, and File tables are also present in all .msi files.</span></span> <span data-ttu-id="11808-116">Una base de datos de módulo de combinación no contiene una [tabla de características](feature-table.md) , por lo que el archivo. MSM no se puede instalar por sí solo.</span><span class="sxs-lookup"><span data-stu-id="11808-116">A merge module database does not contain a [Feature table](feature-table.md) and so the .msm file cannot be installed alone.</span></span> <span data-ttu-id="11808-117">Para instalar un módulo de combinación, primero debe combinarse mediante una herramienta de combinación en un archivo. msi.</span><span class="sxs-lookup"><span data-stu-id="11808-117">To install a merge module, it must first be merged by using a merge tool into an .msi file.</span></span>

<span data-ttu-id="11808-118">La [tabla ModuleSignature](modulesignature-table.md) solo está presente en archivos. msi que se han combinado con al menos un archivo. msm.</span><span class="sxs-lookup"><span data-stu-id="11808-118">The [ModuleSignature Table](modulesignature-table.md) is only present in .msi files that has been merged with at least one .msm file.</span></span> <span data-ttu-id="11808-119">Si esta tabla está presente en un archivo. msi, contiene un registro para cada módulo de combinación que se ha combinado previamente en la base de datos de instalación.</span><span class="sxs-lookup"><span data-stu-id="11808-119">If this table is present in an .msi file, it contains one record for each merge module that has been previously merged into the installation database.</span></span>

<span data-ttu-id="11808-120">Los módulos de combinación pueden contener tablas de secuencia módulo CRT opcionales.</span><span class="sxs-lookup"><span data-stu-id="11808-120">Merge modules may contain optional MergeModule Sequence tables.</span></span> <span data-ttu-id="11808-121">Estas tablas solo se producen en archivos. msm.</span><span class="sxs-lookup"><span data-stu-id="11808-121">These tables occur only in .msm files.</span></span> <span data-ttu-id="11808-122">Cuando los archivos. MSM se combinan en un archivo. msi, estas tablas modifican las [*tablas de secuencia*](s-gly.md) de acciones del archivo. msi.</span><span class="sxs-lookup"><span data-stu-id="11808-122">When the .msm files are merged into an .msi file, these tables modify the action [*sequence tables*](s-gly.md) of the .msi file.</span></span>

<span data-ttu-id="11808-123">Los módulos de combinación pueden contener tablas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="11808-123">Merge modules may contain custom tables.</span></span> <span data-ttu-id="11808-124">Estas tablas las utilizan las [acciones personalizadas](custom-actions.md) definidas en el módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="11808-124">These tables are used by [custom actions](custom-actions.md) defined in the merge module.</span></span>

<span data-ttu-id="11808-125">Los módulos de combinación raramente requieren tablas de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="11808-125">Merge modules rarely require user interface tables.</span></span> <span data-ttu-id="11808-126">Estas tablas solo deben estar presentes en casos raros en los que el módulo de combinación requiere la intervención del usuario durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="11808-126">These tables need to be present only in rare cases where the merge module requires input from the user during installation.</span></span> <span data-ttu-id="11808-127">Para obtener más información, vea [creación de interfaces de usuario en módulos de combinación](authoring-user-interfaces-in-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="11808-127">For more information, see [Authoring User Interfaces in Merge Modules](authoring-user-interfaces-in-merge-modules.md).</span></span>

 

 



