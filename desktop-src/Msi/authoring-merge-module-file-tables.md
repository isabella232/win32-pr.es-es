---
description: En cada módulo de combinación se requiere una tabla de archivos y debe haber un registro para cada archivo que el módulo de combinación está entregando al paquete de instalación de destino.
ms.assetid: 436933c7-6e5d-4b4e-9147-c60a26871dbe
title: Crear tablas de archivos de módulo de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2687ed69c1a0362f96db896a5fdf4237ac4681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082544"
---
# <a name="authoring-merge-module-file-tables"></a><span data-ttu-id="79489-103">Crear tablas de archivos de módulo de combinación</span><span class="sxs-lookup"><span data-stu-id="79489-103">Authoring Merge Module File Tables</span></span>

<span data-ttu-id="79489-104">En cada módulo de combinación se requiere una [tabla de archivos](file-table.md) y debe haber un registro para cada archivo que el módulo de combinación está entregando al paquete de instalación de destino.</span><span class="sxs-lookup"><span data-stu-id="79489-104">A [File Table](file-table.md) is required in every merge module, and should have a record for each file that is being delivered to the target installation package by the merge module.</span></span> <span data-ttu-id="79489-105">Cuando el módulo de fusión mediante combinación se combina en un archivo. msi, cada archivo de la tabla de archivos de módulo de combinación se almacena en un [*archivo. cab*](c-gly.md) en el archivo. msm.</span><span class="sxs-lookup"><span data-stu-id="79489-105">When the merge module is merged into a .msi file, every file in the merge module File Table is stored inside a [*cabinet file*](c-gly.md) in the .msm file.</span></span> <span data-ttu-id="79489-106">El nombre del archivo. cab en un módulo de combinación es siempre el siguiente: MergeModule.CABinet.</span><span class="sxs-lookup"><span data-stu-id="79489-106">The name of the cabinet in a merge module is always the following: MergeModule.CABinet.</span></span>

<span data-ttu-id="79489-107">Para obtener más información, consulte [generación de archivos. cab de MergeModule.CABinet](generating-mergemodule-cabinet-cabinet-files.md).</span><span class="sxs-lookup"><span data-stu-id="79489-107">For more information, see [Generating MergeModule.CABinet Cabinet Files](generating-mergemodule-cabinet-cabinet-files.md).</span></span>

-   <span data-ttu-id="79489-108">Dado que los archivos de un módulo de combinación siempre se almacenan dentro de un archivo. cab, no es necesario establecer las marcas de bits **msidbFileAttributesNoncompressed** o **msidbFileAttributesCompressed** en la columna Attributes de la [tabla File](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="79489-108">Because the files of a merge module are always stored inside a cabinet file, it is not necessary to set the **msidbFileAttributesNoncompressed** or **msidbFileAttributesCompressed** bit flags in the Attributes column of the [File Table](file-table.md).</span></span>
-   <span data-ttu-id="79489-109">Los nombres de los archivos de MergeModule.CABinet deben coincidir con la clave principal de la [tabla de archivos](file-table.md)del módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="79489-109">The names of files in MergeModule.CABinet must match the primary key in the merge module's [File Table](file-table.md).</span></span>

    <span data-ttu-id="79489-110">La columna de archivo es la clave principal de la [tabla de archivos](file-table.md) y las entradas de este campo deben seguir la Convención que se describe en [asignar nombres a las claves principales en las bases de datos de módulos de combinación](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="79489-110">The File column is the primary key of the [File Table](file-table.md) and the entries in this field must follow the convention that is described in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span>

-   <span data-ttu-id="79489-111">Los números de secuencia de archivo se especifican en la columna Sequence de la [tabla File](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="79489-111">File sequence numbers are specified in the Sequence column of the [File Table](file-table.md).</span></span>

    <span data-ttu-id="79489-112">Los archivos deben aparecer en la [tabla de archivos](file-table.md) del módulo de combinación en la misma secuencia en la que se almacenan en MergeModule.CABinet.</span><span class="sxs-lookup"><span data-stu-id="79489-112">Files must be listed in the merge module's [File Table](file-table.md) in the same sequence that they are stored in MergeModule.CABinet.</span></span> <span data-ttu-id="79489-113">No es necesario que los números de secuencia de los archivos sean consecutivos, pero deben seguir la misma secuencia que los archivos que se almacenan en el archivo.</span><span class="sxs-lookup"><span data-stu-id="79489-113">The sequence numbers of files do not need to be consecutive, but they must follow the same sequence as the files that are stored inside the cabinet.</span></span> <span data-ttu-id="79489-114">Por ejemplo, el primer, segundo y tercer archivo almacenados en el archivo. cab pueden tener los números de secuencia 100, 200 y 300.</span><span class="sxs-lookup"><span data-stu-id="79489-114">For example, the first, second, and third files stored in the cabinet can have the sequence numbers 100, 200, and 300.</span></span>

-   <span data-ttu-id="79489-115">El instalador omite los archivos adicionales incluidos en MergeModule.CABinet que no aparecen en la [tabla de archivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="79489-115">The Installer skips extra files included in MergeModule.CABinet that are not listed in the [File Table](file-table.md).</span></span>

    <span data-ttu-id="79489-116">Un archivo contenedor puede contener todos los archivos necesarios para un módulo de combinación que admita varios idiomas mediante transformaciones.</span><span class="sxs-lookup"><span data-stu-id="79489-116">One cabinet file can contain all the files necessary for a merge module that supports multiple languages using transforms.</span></span> <span data-ttu-id="79489-117">A todos los archivos de idioma se les puede asignar un número de secuencia único en el archivo. cab y, a continuación, una transformación puede Agregar o quitar archivos de la [tabla de archivos](file-table.md) cuando sea necesario para un idioma específico.</span><span class="sxs-lookup"><span data-stu-id="79489-117">All the language files can be given a unique sequence number in the cabinet, and then a transform can add or remove files from the [File Table](file-table.md) when needed for a specific language.</span></span> <span data-ttu-id="79489-118">Para obtener más información, vea [crear módulos de combinación en varios lenguajes](authoring-multiple-language-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="79489-118">For more information, see [Authoring Multiple Language Merge Modules](authoring-multiple-language-merge-modules.md).</span></span>

<span data-ttu-id="79489-119">Para obtener más información, vea [File Table](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="79489-119">For more information, see [File Table](file-table.md).</span></span>

 

 



