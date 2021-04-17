---
description: Cada archivo que se entrega al paquete de instalación de destino mediante el módulo de combinación debe almacenarse en un archivo. cab incrustado como una secuencia dentro del archivo. msm. El nombre de este archivo. cab siempre es MergeModule.CABinet.
ms.assetid: 884df249-977e-4e8e-8978-15331a7c1d8a
title: Generación de archivos. cab de MergeModule.CABinet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a26eb9bb3daf92d81e21267b2f56706b74d9179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667786"
---
# <a name="generating-mergemodulecabinet-cabinet-files"></a><span data-ttu-id="647a2-104">Generación de archivos. cab de MergeModule.CABinet</span><span class="sxs-lookup"><span data-stu-id="647a2-104">Generating MergeModule.CABinet Cabinet Files</span></span>

<span data-ttu-id="647a2-105">Cada archivo que se entrega al paquete de instalación de destino mediante el módulo de combinación debe almacenarse en un archivo. cab incrustado como una secuencia dentro del archivo. msm.</span><span class="sxs-lookup"><span data-stu-id="647a2-105">Every file that is delivered to the target installation package by the merge module must be stored inside of a cabinet file embedded as a stream inside the .msm file.</span></span> <span data-ttu-id="647a2-106">El nombre de este archivo. cab siempre es MergeModule.CABinet.</span><span class="sxs-lookup"><span data-stu-id="647a2-106">The name of this cabinet is always MergeModule.CABinet.</span></span>

<span data-ttu-id="647a2-107">Los nombres de los archivos de MergeModule.CABinet deben coincidir con las claves principales que se usan en la [tabla de archivos](file-table.md) del módulo de combinación y deben cumplir la Convención descrita en [naming Keys Primary in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="647a2-107">The names of files in MergeModule.CABinet must match the primary keys used in the merge module's [File table](file-table.md) and must adhere to the convention described in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span>

<span data-ttu-id="647a2-108">El instalador omite los archivos adicionales incluidos en MergeModule.CABinet que no aparecen en la [tabla de archivos](file-table.md)del módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="647a2-108">The installer skips extra files included in MergeModule.CABinet that are not listed in the merge module's [File table](file-table.md).</span></span> <span data-ttu-id="647a2-109">No es necesario que los números de secuencia de los archivos especificados en la tabla de archivos sean consecutivos, pero deben seguir la misma secuencia que los archivos almacenados en MergeModule.CABinet.</span><span class="sxs-lookup"><span data-stu-id="647a2-109">The sequence numbers of files specified in the File table do not need to be consecutive, but they must follow the same sequence as the files stored inside MergeModule.CABinet.</span></span> <span data-ttu-id="647a2-110">Para obtener más información, vea [crear tablas de archivos de módulo de combinación](authoring-merge-module-file-tables.md).</span><span class="sxs-lookup"><span data-stu-id="647a2-110">For more information, see [Authoring Merge Module File Tables](authoring-merge-module-file-tables.md).</span></span>

<span data-ttu-id="647a2-111">Esto significa que un único archivo contenedor puede contener todos los archivos necesarios para que un módulo de combinación admita varios idiomas.</span><span class="sxs-lookup"><span data-stu-id="647a2-111">This means that a single cabinet file can contain all the files needed for a merge module to support multiple languages.</span></span> <span data-ttu-id="647a2-112">Todos los archivos de idioma pueden tener números de secuencia únicos en el archivo. cab y, a continuación, se puede usar una transformación de idioma para agregar o quitar archivos de la tabla de archivos con el fin de obtener un módulo de combinación para un idioma determinado.</span><span class="sxs-lookup"><span data-stu-id="647a2-112">All the language files can be given unique sequence numbers in the cabinet and then a language transform can be used to add or remove files from the File table to obtain a merge module for a particular language.</span></span> <span data-ttu-id="647a2-113">Para obtener más información, vea [crear módulos de combinación en varios lenguajes](authoring-multiple-language-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="647a2-113">For details, see [Authoring Multiple Language Merge Modules](authoring-multiple-language-merge-modules.md).</span></span>

<span data-ttu-id="647a2-114">MergeModule.CABinet se puede Agregar al módulo de fusión mediante combinación abriendo una [ \_ tabla de secuencias](-streams-table.md)temporales.</span><span class="sxs-lookup"><span data-stu-id="647a2-114">MergeModule.CABinet can be added to the merge module by opening a temporary [\_Streams Table](-streams-table.md).</span></span> <span data-ttu-id="647a2-115">Por ejemplo, la herramienta Msidb.exe proporcionado con el SDK de Windows Installer se puede usar para agregar el MergeModule.CABinet al módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="647a2-115">For example, the tool Msidb.exe provided with the Windows Installer SDK can be used to add the MergeModule.CABinet to the merge module.</span></span> <span data-ttu-id="647a2-116">Para obtener más información, vea [incluir un archivo. cab en una instalación de](including-a-cabinet-file-in-an-installation.md).</span><span class="sxs-lookup"><span data-stu-id="647a2-116">For more information, see [Including a Cabinet File in an Installation](including-a-cabinet-file-in-an-installation.md).</span></span>

 

 



