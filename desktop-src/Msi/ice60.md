---
description: ICE60 valida la tabla de archivos de una base de datos Windows Installer.
ms.assetid: 95d9b8b4-0b65-451a-8629-f0b276d6e35d
title: ICE60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26c6f296fd514f582a699a5f839a7e145169e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667942"
---
# <a name="ice60"></a><span data-ttu-id="da579-103">ICE60</span><span class="sxs-lookup"><span data-stu-id="da579-103">ICE60</span></span>

<span data-ttu-id="da579-104">ICE60 comprueba que los archivos de la [tabla de archivos](file-table.md) cumplen la siguiente condición:</span><span class="sxs-lookup"><span data-stu-id="da579-104">ICE60 checks that files in the [File table](file-table.md) meet the following condition:</span></span>

-   <span data-ttu-id="da579-105">Si el archivo no es una fuente y tiene una versión, debe tener un idioma.</span><span class="sxs-lookup"><span data-stu-id="da579-105">If the file is not a font and has a version, then it must have a language.</span></span>
-   <span data-ttu-id="da579-106">ICE60 comprueba que no hay ningún archivo con versión en la [tabla MsiFileHash](msifilehash-table.md).</span><span class="sxs-lookup"><span data-stu-id="da579-106">ICE60 checks that no versioned files are listed in the [MsiFileHash table](msifilehash-table.md).</span></span>

<span data-ttu-id="da579-107">Un error al corregir una advertencia de ICE60 suele conducir a que un archivo se reinstale innecesariamente cuando se realiza una reparación del producto.</span><span class="sxs-lookup"><span data-stu-id="da579-107">Failure to fix a warning reported by ICE60 generally leads to a file being needlessly reinstalled when a product repair is done.</span></span> <span data-ttu-id="da579-108">Esto sucede porque el archivo que se va a instalar en la reparación y el archivo existente en el disco tienen la misma versión (son el mismo archivo) pero distintos idiomas.</span><span class="sxs-lookup"><span data-stu-id="da579-108">This happens because the file to be installed in the repair and the existing file on disk have the same version (they are the same file) but different languages.</span></span> <span data-ttu-id="da579-109">La tabla de archivos muestra el idioma como null, pero el propio archivo tiene un valor de idioma en el recurso.</span><span class="sxs-lookup"><span data-stu-id="da579-109">The file table lists the language as null, but the file itself has a language value in the resource.</span></span> <span data-ttu-id="da579-110">En función de las [reglas de control de versiones de archivo](file-versioning-rules.md), el instalador favorece el archivo que se va a instalar, por lo que se Recopia innecesariamente.</span><span class="sxs-lookup"><span data-stu-id="da579-110">Based on the [file versioning rules](file-versioning-rules.md), the installer favors the file to be installed, so it is recopied needlessly.</span></span>

## <a name="result"></a><span data-ttu-id="da579-111">Resultado</span><span class="sxs-lookup"><span data-stu-id="da579-111">Result</span></span>

<span data-ttu-id="da579-112">ICE60 envía una advertencia o un error si un archivo de la [tabla de archivos](file-table.md) que no es una fuente y tiene una versión, no tiene un idioma.</span><span class="sxs-lookup"><span data-stu-id="da579-112">ICE60 posts a warning or an error if a file in the [File table](file-table.md) that is not a font and has a version, does not have a language.</span></span>

<span data-ttu-id="da579-113">ICE60 envía el siguiente error si un archivo que aparece en la tabla MsiFileHash tiene versiones.</span><span class="sxs-lookup"><span data-stu-id="da579-113">ICE60 posts the following error if a file listed in the MsiFileHash table is versioned.</span></span>

``` syntax
ERROR: "The file [1] is Versioned. It cannot be hashed"
```

## <a name="example"></a><span data-ttu-id="da579-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="da579-114">Example</span></span>

<span data-ttu-id="da579-115">ICE60 notifica el siguiente error y advertencia para el ejemplo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="da579-115">ICE60 reports the following error and warning for the example shown.</span></span> <span data-ttu-id="da579-116">(El archivo B es una fuente; los demás archivos no lo son).</span><span class="sxs-lookup"><span data-stu-id="da579-116">(File B is a font; the other files are not.)</span></span>

``` syntax
WARNING: The file FileE is not a Font, and its version is not a companion file reference. It should have a language specified in the Language column.
```

<span data-ttu-id="da579-117">Filea tiene una versión y un idioma; por lo tanto, no se genera ninguna advertencia o error.</span><span class="sxs-lookup"><span data-stu-id="da579-117">FileA has both a version and a language; therefore no warning or error is generated.</span></span>

<span data-ttu-id="da579-118">FileB tiene una versión pero no un idioma.</span><span class="sxs-lookup"><span data-stu-id="da579-118">FileB has a version but no language.</span></span> <span data-ttu-id="da579-119">Sin embargo, no se genera ninguna advertencia ni error, porque es una fuente.</span><span class="sxs-lookup"><span data-stu-id="da579-119">No warning or error is generated, however, because it is a font.</span></span>

<span data-ttu-id="da579-120">FileC es una referencia complementaria, por lo que no tiene que tener un idioma.</span><span class="sxs-lookup"><span data-stu-id="da579-120">FileC is a companion reference, so it does not have to have a language.</span></span> <span data-ttu-id="da579-121">No se genera ninguna advertencia o error.</span><span class="sxs-lookup"><span data-stu-id="da579-121">No warning or error is generated.</span></span>

<span data-ttu-id="da579-122">Archivó no tiene ninguna versión, por lo que no necesita tener un idioma.</span><span class="sxs-lookup"><span data-stu-id="da579-122">FileD has no version, so it does not need to have a language.</span></span> <span data-ttu-id="da579-123">No se genera ninguna advertencia o error.</span><span class="sxs-lookup"><span data-stu-id="da579-123">No warning or error is generated.</span></span>

<span data-ttu-id="da579-124">El archivo tiene una versión pero no un idioma.</span><span class="sxs-lookup"><span data-stu-id="da579-124">FileE has a version but no language.</span></span> <span data-ttu-id="da579-125">Por lo tanto, se genera una advertencia.</span><span class="sxs-lookup"><span data-stu-id="da579-125">Therefore a warning is generated.</span></span>

<span data-ttu-id="da579-126">Para corregir esta advertencia, agregue un idioma al archivo.</span><span class="sxs-lookup"><span data-stu-id="da579-126">To fix this warning, add a language to FileE.</span></span>

<span data-ttu-id="da579-127">Los archivos deben tener valores de idioma almacenados en el recurso de versión siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="da579-127">Files should have language values stored in the version resource whenever possible.</span></span> <span data-ttu-id="da579-128">Si un archivo es independiente del idioma, use el [LANGID](column-data-types.md) 0.</span><span class="sxs-lookup"><span data-stu-id="da579-128">If a file is language neutral, use the [LANGID](column-data-types.md) 0.</span></span>

<span data-ttu-id="da579-129">[Tabla de archivos](file-table.md) (FileB es una fuente; los demás archivos no lo son).</span><span class="sxs-lookup"><span data-stu-id="da579-129">[File Table](file-table.md) (FileB is a font; the other files are not.)</span></span>



| <span data-ttu-id="da579-130">Archivo</span><span class="sxs-lookup"><span data-stu-id="da579-130">File</span></span>  | <span data-ttu-id="da579-131">Versión</span><span class="sxs-lookup"><span data-stu-id="da579-131">Version</span></span> | <span data-ttu-id="da579-132">Idioma</span><span class="sxs-lookup"><span data-stu-id="da579-132">Language</span></span> |
|-------|---------|----------|
| <span data-ttu-id="da579-133">Archivoa</span><span class="sxs-lookup"><span data-stu-id="da579-133">FileA</span></span> | <span data-ttu-id="da579-134">1,0</span><span class="sxs-lookup"><span data-stu-id="da579-134">1.0</span></span>     | <span data-ttu-id="da579-135">3082</span><span class="sxs-lookup"><span data-stu-id="da579-135">1033</span></span>     |
| <span data-ttu-id="da579-136">FileB</span><span class="sxs-lookup"><span data-stu-id="da579-136">FileB</span></span> | <span data-ttu-id="da579-137">1,0</span><span class="sxs-lookup"><span data-stu-id="da579-137">1.0</span></span>     |          |
| <span data-ttu-id="da579-138">FileC</span><span class="sxs-lookup"><span data-stu-id="da579-138">FileC</span></span> | <span data-ttu-id="da579-139">Archivoa</span><span class="sxs-lookup"><span data-stu-id="da579-139">FileA</span></span>   |          |
| <span data-ttu-id="da579-140">Registrado</span><span class="sxs-lookup"><span data-stu-id="da579-140">FileD</span></span> |         |          |
| <span data-ttu-id="da579-141">Archivo</span><span class="sxs-lookup"><span data-stu-id="da579-141">FileE</span></span> | <span data-ttu-id="da579-142">1,0</span><span class="sxs-lookup"><span data-stu-id="da579-142">1.0</span></span>     |          |



 

[<span data-ttu-id="da579-143">Tabla de fuentes</span><span class="sxs-lookup"><span data-stu-id="da579-143">Font Table</span></span>](font-table.md)



| <span data-ttu-id="da579-144">Archivo</span><span class="sxs-lookup"><span data-stu-id="da579-144">File</span></span>  | <span data-ttu-id="da579-145">FontTitle</span><span class="sxs-lookup"><span data-stu-id="da579-145">FontTitle</span></span>  |
|-------|------------|
| <span data-ttu-id="da579-146">FileB</span><span class="sxs-lookup"><span data-stu-id="da579-146">FileB</span></span> | <span data-ttu-id="da579-147">Título de fuente</span><span class="sxs-lookup"><span data-stu-id="da579-147">Font Title</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="da579-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="da579-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da579-149">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="da579-149">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



