---
description: Orca.exe es un editor de tablas de base de datos para crear y editar Windows Installer paquetes y módulos de combinación.
ms.assetid: 4dddc262-1271-4e00-a986-53380b957b17
title: Orca.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3f17874e08fcdbfdbab38c480219579897b9896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082064"
---
# <a name="orcaexe"></a><span data-ttu-id="0caea-103">Orca.exe</span><span class="sxs-lookup"><span data-stu-id="0caea-103">Orca.exe</span></span>

<span data-ttu-id="0caea-104">Orca.exe es un editor de tablas de base de datos para crear y editar Windows Installer paquetes y módulos de combinación.</span><span class="sxs-lookup"><span data-stu-id="0caea-104">Orca.exe is a database table editor for creating and editing Windows Installer packages and merge modules.</span></span> <span data-ttu-id="0caea-105">La herramienta proporciona una interfaz gráfica para la validación, resaltando las entradas concretas en las que se producen errores o advertencias de validación.</span><span class="sxs-lookup"><span data-stu-id="0caea-105">The tool provides a graphical interface for validation, highlighting the particular entries where validation errors or warnings occur.</span></span>

<span data-ttu-id="0caea-106">Esta herramienta solo está disponible en los [componentes de Windows SDK para los desarrolladores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="0caea-106">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="0caea-107">Se proporciona como un archivo de Orca.msi.</span><span class="sxs-lookup"><span data-stu-id="0caea-107">It is provided as an Orca.msi file.</span></span> <span data-ttu-id="0caea-108">Después de instalar los componentes de Windows SDK para Windows Installer desarrolladores, haga doble clic en Orca.msi para instalar el archivo de Orca.exe.</span><span class="sxs-lookup"><span data-stu-id="0caea-108">After installing the Windows SDK Components for Windows Installer Developers, double click Orca.msi to install the Orca.exe file.</span></span>

## <a name="syntax"></a><span data-ttu-id="0caea-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0caea-109">Syntax</span></span>

<span data-ttu-id="0caea-110">\**Orca\*\*\*\[<options>\]\[<source file>\]*</span><span class="sxs-lookup"><span data-stu-id="0caea-110">**orca** *\[<options>\]\[<source file>\]*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="0caea-111">Opciones de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="0caea-111">Command Line Options</span></span>

<span data-ttu-id="0caea-112">Orca.exe usa las siguientes opciones de la línea de comandos que no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0caea-112">Orca.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="0caea-113">También se puede usar un delimitador de barra diagonal en lugar de un guión.</span><span class="sxs-lookup"><span data-stu-id="0caea-113">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="0caea-114">Opción</span><span class="sxs-lookup"><span data-stu-id="0caea-114">Option</span></span> | <span data-ttu-id="0caea-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="0caea-115">Description</span></span>                                                 |
|--------|-------------------------------------------------------------|
| <span data-ttu-id="0caea-116">-q</span><span class="sxs-lookup"><span data-stu-id="0caea-116">-q</span></span>     | <span data-ttu-id="0caea-117">Modo silencioso</span><span class="sxs-lookup"><span data-stu-id="0caea-117">Quiet mode</span></span>                                                  |
| <span data-ttu-id="0caea-118">-S</span><span class="sxs-lookup"><span data-stu-id="0caea-118">-s</span></span>     | <span data-ttu-id="0caea-119">< base \[ de datos de esquema de> de bases de datos "orca. dat": predeterminado\]</span><span class="sxs-lookup"><span data-stu-id="0caea-119"><*database*> Schema database \["orca.dat" - default\]</span></span> |
| <span data-ttu-id="0caea-120">-?</span><span class="sxs-lookup"><span data-stu-id="0caea-120">-?</span></span>     | <span data-ttu-id="0caea-121">Cuadro de diálogo de ayuda</span><span class="sxs-lookup"><span data-stu-id="0caea-121">Help dialog</span></span>                                                 |



 

<span data-ttu-id="0caea-122">Orca.exe usa las siguientes opciones de la línea de comandos que no distinguen mayúsculas de minúsculas con los módulos de combinación.</span><span class="sxs-lookup"><span data-stu-id="0caea-122">Orca.exe uses the following case-insensitive command line options with merge modules.</span></span> <span data-ttu-id="0caea-123">También se puede usar un delimitador de barra diagonal en lugar de un guión.</span><span class="sxs-lookup"><span data-stu-id="0caea-123">A slash delimiter may also be used in place of a dash.</span></span> <span data-ttu-id="0caea-124">Al realizar una combinación, se necesitan los>-f,-m y <*SourceFile* .</span><span class="sxs-lookup"><span data-stu-id="0caea-124">When performing a merge the -f, -m and <*sourcefile*> are all required.</span></span>



| <span data-ttu-id="0caea-125">Opción</span><span class="sxs-lookup"><span data-stu-id="0caea-125">Option</span></span>     | <span data-ttu-id="0caea-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="0caea-126">Description</span></span>                                                                |
|------------|----------------------------------------------------------------------------|
| <span data-ttu-id="0caea-127">-c</span><span class="sxs-lookup"><span data-stu-id="0caea-127">-c</span></span>         | <span data-ttu-id="0caea-128">Confirme la combinación en la base de datos si no hay errores.</span><span class="sxs-lookup"><span data-stu-id="0caea-128">Commit merge to database if no errors.</span></span>                                     |
| <span data-ttu-id="0caea-129">-!</span><span class="sxs-lookup"><span data-stu-id="0caea-129">-!</span></span>         | <span data-ttu-id="0caea-130">Confirme la fusión mediante combinación en una base de datos, incluso si hay errores.</span><span class="sxs-lookup"><span data-stu-id="0caea-130">Commit merge to a database even if there are errors.</span></span>                       |
| <span data-ttu-id="0caea-131">-M</span><span class="sxs-lookup"><span data-stu-id="0caea-131">-m</span></span>         | <span data-ttu-id="0caea-132"><*módulo*> módulo de combinación que se va a combinar en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="0caea-132"><*module*> Merge Module to merge into database.</span></span>                      |
| <span data-ttu-id="0caea-133">-f</span><span class="sxs-lookup"><span data-stu-id="0caea-133">-f</span></span>         | <span data-ttu-id="0caea-134">Característica \[ : característica2 \] características para conectarse al módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="0caea-134">Feature\[:Feature2\] Feature(s) to connect to Merge Module.</span></span>                |
| <span data-ttu-id="0caea-135">-r</span><span class="sxs-lookup"><span data-stu-id="0caea-135">-r</span></span>         | <span data-ttu-id="0caea-136"><*identificador de directorio*> entrada de directorio para la redirección raíz del módulo.</span><span class="sxs-lookup"><span data-stu-id="0caea-136"><*directory id*> Directory entry for the module root redirection.</span></span>    |
| <span data-ttu-id="0caea-137">-X</span><span class="sxs-lookup"><span data-stu-id="0caea-137">-x</span></span>         | <span data-ttu-id="0caea-138"><*directorio*> extraer archivos en una imagen en el directorio.</span><span class="sxs-lookup"><span data-stu-id="0caea-138"><*directory*> Extract files to an image under the directory.</span></span>         |
| <span data-ttu-id="0caea-139">-g</span><span class="sxs-lookup"><span data-stu-id="0caea-139">-g</span></span>         | <span data-ttu-id="0caea-140"><*lenguaje> lenguaje* usado para abrir un módulo.</span><span class="sxs-lookup"><span data-stu-id="0caea-140"><*language*> Language used to open a module.</span></span>                         |
| <span data-ttu-id="0caea-141">-l</span><span class="sxs-lookup"><span data-stu-id="0caea-141">-l</span></span>         | <span data-ttu-id="0caea-142"><archivo de *registro*> archivo que se va a usar como registro; Anexe si ya existe.</span><span class="sxs-lookup"><span data-stu-id="0caea-142"><*log file*> File to use as a log, append if it already exists.</span></span>      |
| <span data-ttu-id="0caea-143">-i</span><span class="sxs-lookup"><span data-stu-id="0caea-143">-i</span></span>         | <span data-ttu-id="0caea-144"><*directorio*> Extraiga los archivos a la imagen de origen en el directorio.</span><span class="sxs-lookup"><span data-stu-id="0caea-144"><*directory*> Extract files to the source image under the directory.</span></span> |
| <span data-ttu-id="0caea-145">-CAB</span><span class="sxs-lookup"><span data-stu-id="0caea-145">-cab</span></span>       | <span data-ttu-id="0caea-146"><*nombre* de archivo> Extraiga el archivo. cab de MSM en el archivo.</span><span class="sxs-lookup"><span data-stu-id="0caea-146"><*filename*> Extract the MSM cabinet to file.</span></span>                        |
| <span data-ttu-id="0caea-147">-lfn</span><span class="sxs-lookup"><span data-stu-id="0caea-147">-lfn</span></span>       | <span data-ttu-id="0caea-148">Use nombres de archivo largos durante la extracción.</span><span class="sxs-lookup"><span data-stu-id="0caea-148">Use Long File Names during the extraction.</span></span>                                 |
| <span data-ttu-id="0caea-149">-configurar</span><span class="sxs-lookup"><span data-stu-id="0caea-149">-configure</span></span> | <span data-ttu-id="0caea-150"><*nombre* de archivo> configurar el módulo mediante datos de un archivo.</span><span class="sxs-lookup"><span data-stu-id="0caea-150"><*filename*> Configure the module using data from a file.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="0caea-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0caea-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0caea-152">Herramientas de desarrollo de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="0caea-152">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="0caea-153">Versiones publicadas, herramientas y redistribuibles</span><span class="sxs-lookup"><span data-stu-id="0caea-153">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



