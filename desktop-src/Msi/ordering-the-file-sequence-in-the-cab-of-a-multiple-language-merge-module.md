---
description: Los módulos de combinación de varios idiomas, las transformaciones de idioma y los archivos. cab deben crearse de modo que el orden de los archivos coincida con el orden especificado en la tabla de archivos.
ms.assetid: c6ddf5fc-a7c5-49c1-899b-ff9fdff9c028
title: Ordenar la secuencia de archivos en el archivo. CAB de un módulo de combinación de varios idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01bdd00d8b09c0605b7ddcf656d87d41e3f53776
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279335"
---
# <a name="ordering-the-file-sequence-in-the-cab-of-a-multiple-language-merge-module"></a><span data-ttu-id="5d3fa-103">Ordenar la secuencia de archivos en el archivo. CAB de un módulo de combinación de varios idiomas</span><span class="sxs-lookup"><span data-stu-id="5d3fa-103">Ordering the File Sequence in the CAB of a Multiple Language Merge Module</span></span>

<span data-ttu-id="5d3fa-104">Los módulos de combinación de varios idiomas, las transformaciones de lenguaje y los archivos. cab deben crearse de modo que el orden de los archivos del archivo. cab coincida con el orden de instalación de los archivos especificados en la [tabla de archivos](file-table.md), incluso después de la aplicación de la transformación de lenguaje.</span><span class="sxs-lookup"><span data-stu-id="5d3fa-104">Multiple-language merge modules, language transforms, and cabinet files must be authored such that the order of the files in the .cab matches the installation order of files specified in the [File Table](file-table.md), even after the application of the language transform.</span></span> <span data-ttu-id="5d3fa-105">Si el orden en el módulo y en el archivo. cab no coinciden, no se puede usar el módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="5d3fa-105">If the order in the module and in the .cab do not match, the merge module cannot be used.</span></span>

<span data-ttu-id="5d3fa-106">Asigne a cada archivo del módulo un número de secuencia único que sea independiente del idioma y, a continuación, use siempre ese número de secuencia para el archivo.</span><span class="sxs-lookup"><span data-stu-id="5d3fa-106">Assign to each file in the module, a unique sequence number that is independent of its language, and then always use that sequence number for the file.</span></span> <span data-ttu-id="5d3fa-107">Use la misma secuencia al compilar el archivo. cab y crear una transformación de idioma.</span><span class="sxs-lookup"><span data-stu-id="5d3fa-107">Use the same sequence when building the cabinet file and authoring a language transform.</span></span>

<span data-ttu-id="5d3fa-108">Dado que el instalador solo instala los archivos enumerados en la [tabla de archivos](file-table.md), el uso de una secuencia de archivos global en el archivo. cab, la tabla de [archivos](file-table.md)y la transformación de idioma permite a la herramienta de combinación omitir los archivos adicionales almacenados en el archivo. cab que no aparecen en la tabla de [archivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="5d3fa-108">Because the Installer only installs the files listed in the [File Table](file-table.md), the use of a global file sequence in the cabinet, [File Table](file-table.md), and language transform enables the merge tool to skip any extra files stored in the cabinet that are not listed in the [File Table](file-table.md).</span></span> <span data-ttu-id="5d3fa-109">Pueden existir otros archivos en el archivo. cab, pero no deben aparecer en la [tabla de archivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="5d3fa-109">Other files may exist in the cabinet, but they must not be listed in the [File Table](file-table.md).</span></span> <span data-ttu-id="5d3fa-110">Por ejemplo, un módulo que instala Code.dll, English. dat, alemán. dat y francés. dat puede usar el siguiente orden de secuencia de archivos global.</span><span class="sxs-lookup"><span data-stu-id="5d3fa-110">For example, a module installing Code.dll, English.dat, German.dat, and French.dat can use the following global file sequence order.</span></span>



| <span data-ttu-id="5d3fa-111">Archivo</span><span class="sxs-lookup"><span data-stu-id="5d3fa-111">File</span></span>        | <span data-ttu-id="5d3fa-112">Secuencia</span><span class="sxs-lookup"><span data-stu-id="5d3fa-112">Sequence</span></span> |
|-------------|----------|
| <span data-ttu-id="5d3fa-113">Code.Dll</span><span class="sxs-lookup"><span data-stu-id="5d3fa-113">Code.Dll</span></span>    | <span data-ttu-id="5d3fa-114">1</span><span class="sxs-lookup"><span data-stu-id="5d3fa-114">1</span></span>        |
| <span data-ttu-id="5d3fa-115">Inglés. dat</span><span class="sxs-lookup"><span data-stu-id="5d3fa-115">English.Dat</span></span> | <span data-ttu-id="5d3fa-116">2</span><span class="sxs-lookup"><span data-stu-id="5d3fa-116">2</span></span>        |
| <span data-ttu-id="5d3fa-117">Alemán. dat</span><span class="sxs-lookup"><span data-stu-id="5d3fa-117">German.Dat</span></span>  | <span data-ttu-id="5d3fa-118">3</span><span class="sxs-lookup"><span data-stu-id="5d3fa-118">3</span></span>        |
| <span data-ttu-id="5d3fa-119">Francés. dat</span><span class="sxs-lookup"><span data-stu-id="5d3fa-119">French.Dat</span></span>  | <span data-ttu-id="5d3fa-120">4</span><span class="sxs-lookup"><span data-stu-id="5d3fa-120">4</span></span>        |



 

<span data-ttu-id="5d3fa-121">A continuación, se pueden crear transformaciones de lenguaje para modificar la [tabla de archivos](file-table.md) del módulo para inglés, alemán o francés.</span><span class="sxs-lookup"><span data-stu-id="5d3fa-121">Language transforms can then be authored to modify the [File Table](file-table.md) of the module for English, German, or French.</span></span>

<span data-ttu-id="5d3fa-122">[Tabla de archivos](file-table.md) (parcial para inglés)</span><span class="sxs-lookup"><span data-stu-id="5d3fa-122">[File Table](file-table.md) (partial for English)</span></span>



| <span data-ttu-id="5d3fa-123">Archivo</span><span class="sxs-lookup"><span data-stu-id="5d3fa-123">File</span></span>        | <span data-ttu-id="5d3fa-124">Secuencia</span><span class="sxs-lookup"><span data-stu-id="5d3fa-124">Sequence</span></span> |
|-------------|----------|
| <span data-ttu-id="5d3fa-125">Code.Dll</span><span class="sxs-lookup"><span data-stu-id="5d3fa-125">Code.Dll</span></span>    | <span data-ttu-id="5d3fa-126">1</span><span class="sxs-lookup"><span data-stu-id="5d3fa-126">1</span></span>        |
| <span data-ttu-id="5d3fa-127">Inglés. dat</span><span class="sxs-lookup"><span data-stu-id="5d3fa-127">English.Dat</span></span> | <span data-ttu-id="5d3fa-128">2</span><span class="sxs-lookup"><span data-stu-id="5d3fa-128">2</span></span>        |



 

<span data-ttu-id="5d3fa-129">[Tabla de archivos](file-table.md) (parcial para alemán)</span><span class="sxs-lookup"><span data-stu-id="5d3fa-129">[File Table](file-table.md) (partial for German)</span></span>



| <span data-ttu-id="5d3fa-130">Archivo</span><span class="sxs-lookup"><span data-stu-id="5d3fa-130">File</span></span>       | <span data-ttu-id="5d3fa-131">Secuencia</span><span class="sxs-lookup"><span data-stu-id="5d3fa-131">Sequence</span></span> |
|------------|----------|
| <span data-ttu-id="5d3fa-132">Code.Dll</span><span class="sxs-lookup"><span data-stu-id="5d3fa-132">Code.Dll</span></span>   | <span data-ttu-id="5d3fa-133">1</span><span class="sxs-lookup"><span data-stu-id="5d3fa-133">1</span></span>        |
| <span data-ttu-id="5d3fa-134">Alemán. dat</span><span class="sxs-lookup"><span data-stu-id="5d3fa-134">German.Dat</span></span> | <span data-ttu-id="5d3fa-135">3</span><span class="sxs-lookup"><span data-stu-id="5d3fa-135">3</span></span>        |



 

<span data-ttu-id="5d3fa-136">[Tabla de archivos](file-table.md) (parcial para francés)</span><span class="sxs-lookup"><span data-stu-id="5d3fa-136">[File Table](file-table.md) (partial for French)</span></span>



| <span data-ttu-id="5d3fa-137">Archivo</span><span class="sxs-lookup"><span data-stu-id="5d3fa-137">File</span></span>       | <span data-ttu-id="5d3fa-138">Secuencia</span><span class="sxs-lookup"><span data-stu-id="5d3fa-138">Sequence</span></span> |
|------------|----------|
| <span data-ttu-id="5d3fa-139">Code.Dll</span><span class="sxs-lookup"><span data-stu-id="5d3fa-139">Code.Dll</span></span>   | <span data-ttu-id="5d3fa-140">1</span><span class="sxs-lookup"><span data-stu-id="5d3fa-140">1</span></span>        |
| <span data-ttu-id="5d3fa-141">Francés. dat</span><span class="sxs-lookup"><span data-stu-id="5d3fa-141">French.Dat</span></span> | <span data-ttu-id="5d3fa-142">4</span><span class="sxs-lookup"><span data-stu-id="5d3fa-142">4</span></span>        |



 

<span data-ttu-id="5d3fa-143">Para obtener más información, vea [crear una transformación de lenguaje para un módulo de combinación de varios idiomas](authoring-a-language-transform-for-a-multiple-language-merge-module.md) y tablas de archivos de módulo de combinación de [creación](authoring-merge-module-file-tables.md).</span><span class="sxs-lookup"><span data-stu-id="5d3fa-143">For more information, see [Authoring a Language Transform for a Multiple Language Merge Module](authoring-a-language-transform-for-a-multiple-language-merge-module.md) and [Authoring Merge Module File Tables](authoring-merge-module-file-tables.md).</span></span>

 

 



