---
description: Orca.exe es un editor de tablas de base de datos para crear y editar Windows Installer paquetes y módulos de combinación.
ms.assetid: 4dddc262-1271-4e00-a986-53380b957b17
title: Orca.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4647b137650bfba521dba3976ea7a1ae66451ce
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102164"
---
# <a name="orcaexe"></a><span data-ttu-id="50445-103">Orca.exe</span><span class="sxs-lookup"><span data-stu-id="50445-103">Orca.exe</span></span>

<span data-ttu-id="50445-104">Orca.exe es un editor de tablas de base de datos para crear y editar Windows Installer paquetes y módulos de combinación.</span><span class="sxs-lookup"><span data-stu-id="50445-104">Orca.exe is a database table editor for creating and editing Windows Installer packages and merge modules.</span></span> <span data-ttu-id="50445-105">La herramienta proporciona una interfaz gráfica para la validación, resaltando las entradas concretas donde se producen errores o advertencias de validación.</span><span class="sxs-lookup"><span data-stu-id="50445-105">The tool provides a graphical interface for validation, highlighting the particular entries where validation errors or warnings occur.</span></span>

<span data-ttu-id="50445-106">Esta herramienta solo está disponible en el Windows SDK [Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="50445-106">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="50445-107">Se proporciona como un archivo Orca.msi datos.</span><span class="sxs-lookup"><span data-stu-id="50445-107">It is provided as an Orca.msi file.</span></span> <span data-ttu-id="50445-108">Después de instalar Windows SDK Components for Windows Installer Developers, haga doble clic en Orca.msi para instalar el archivo Orca.exe.</span><span class="sxs-lookup"><span data-stu-id="50445-108">After installing the Windows SDK Components for Windows Installer Developers, double click Orca.msi to install the Orca.exe file.</span></span>

## <a name="syntax"></a><span data-ttu-id="50445-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="50445-109">Syntax</span></span>

<span data-ttu-id="50445-110">\**orca\*\*\*\[\<options>\]\[\<source file>\]*</span><span class="sxs-lookup"><span data-stu-id="50445-110">**orca** *\[\<options>\]\[\<source file>\]*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="50445-111">Opciones de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="50445-111">Command Line Options</span></span>

<span data-ttu-id="50445-112">Orca.exe usa las siguientes opciones de línea de comandos que no tienen en cuenta las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="50445-112">Orca.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="50445-113">También se puede usar un delimitador de barra diagonal en lugar de un guión.</span><span class="sxs-lookup"><span data-stu-id="50445-113">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="50445-114">Opción</span><span class="sxs-lookup"><span data-stu-id="50445-114">Option</span></span> | <span data-ttu-id="50445-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="50445-115">Description</span></span>                                                 |
|--------|-------------------------------------------------------------|
| <span data-ttu-id="50445-116">-q</span><span class="sxs-lookup"><span data-stu-id="50445-116">-q</span></span>     | <span data-ttu-id="50445-117">Modo silencioso</span><span class="sxs-lookup"><span data-stu-id="50445-117">Quiet mode</span></span>                                                  |
| <span data-ttu-id="50445-118">-S</span><span class="sxs-lookup"><span data-stu-id="50445-118">-s</span></span>     | <span data-ttu-id="50445-119"><*base*> de datos \[ de esquema "orca.dat": valor predeterminado\]</span><span class="sxs-lookup"><span data-stu-id="50445-119"><*database*> Schema database \["orca.dat" - default\]</span></span> |
| <span data-ttu-id="50445-120">-?</span><span class="sxs-lookup"><span data-stu-id="50445-120">-?</span></span>     | <span data-ttu-id="50445-121">Cuadro de diálogo de ayuda</span><span class="sxs-lookup"><span data-stu-id="50445-121">Help dialog</span></span>                                                 |



 

<span data-ttu-id="50445-122">Orca.exe usa las siguientes opciones de línea de comandos que no tienen en cuenta las mayúsculas y minúsculas con los módulos de combinación.</span><span class="sxs-lookup"><span data-stu-id="50445-122">Orca.exe uses the following case-insensitive command line options with merge modules.</span></span> <span data-ttu-id="50445-123">También se puede usar un delimitador de barra diagonal en lugar de un guión.</span><span class="sxs-lookup"><span data-stu-id="50445-123">A slash delimiter may also be used in place of a dash.</span></span> <span data-ttu-id="50445-124">Al realizar una combinación, se requieren las propiedades -f, -m y <*sourcefile*>.</span><span class="sxs-lookup"><span data-stu-id="50445-124">When performing a merge the -f, -m and <*sourcefile*> are all required.</span></span>



| <span data-ttu-id="50445-125">Opción</span><span class="sxs-lookup"><span data-stu-id="50445-125">Option</span></span>     | <span data-ttu-id="50445-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="50445-126">Description</span></span>                                                                |
|------------|----------------------------------------------------------------------------|
| <span data-ttu-id="50445-127">-c</span><span class="sxs-lookup"><span data-stu-id="50445-127">-c</span></span>         | <span data-ttu-id="50445-128">Confirme la combinación en la base de datos si no hay errores.</span><span class="sxs-lookup"><span data-stu-id="50445-128">Commit merge to database if no errors.</span></span>                                     |
| <span data-ttu-id="50445-129">-!</span><span class="sxs-lookup"><span data-stu-id="50445-129">-!</span></span>         | <span data-ttu-id="50445-130">Confirmar la combinación en una base de datos incluso si hay errores.</span><span class="sxs-lookup"><span data-stu-id="50445-130">Commit merge to a database even if there are errors.</span></span>                       |
| <span data-ttu-id="50445-131">-M</span><span class="sxs-lookup"><span data-stu-id="50445-131">-m</span></span>         | <span data-ttu-id="50445-132"><*módulo>* Módulo de mezcla para combinar en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="50445-132"><*module*> Merge Module to merge into database.</span></span>                      |
| <span data-ttu-id="50445-133">-f</span><span class="sxs-lookup"><span data-stu-id="50445-133">-f</span></span>         | <span data-ttu-id="50445-134">\[Característica:Características 2 para conectarse al módulo de \] mezcla.</span><span class="sxs-lookup"><span data-stu-id="50445-134">Feature\[:Feature2\] Feature(s) to connect to Merge Module.</span></span>                |
| <span data-ttu-id="50445-135">-r</span><span class="sxs-lookup"><span data-stu-id="50445-135">-r</span></span>         | <span data-ttu-id="50445-136"><*Id. de* directorio> directory para el redireccionamiento raíz del módulo.</span><span class="sxs-lookup"><span data-stu-id="50445-136"><*directory id*> Directory entry for the module root redirection.</span></span>    |
| <span data-ttu-id="50445-137">-X</span><span class="sxs-lookup"><span data-stu-id="50445-137">-x</span></span>         | <span data-ttu-id="50445-138"><*directorio*> extraer archivos a una imagen en el directorio .</span><span class="sxs-lookup"><span data-stu-id="50445-138"><*directory*> Extract files to an image under the directory.</span></span>         |
| <span data-ttu-id="50445-139">-g</span><span class="sxs-lookup"><span data-stu-id="50445-139">-g</span></span>         | <span data-ttu-id="50445-140"><*language*> Language usado para abrir un módulo.</span><span class="sxs-lookup"><span data-stu-id="50445-140"><*language*> Language used to open a module.</span></span>                         |
| <span data-ttu-id="50445-141">-l</span><span class="sxs-lookup"><span data-stu-id="50445-141">-l</span></span>         | <span data-ttu-id="50445-142"><*archivo de*> archivo que se va a usar como registro, anexe si ya existe.</span><span class="sxs-lookup"><span data-stu-id="50445-142"><*log file*> File to use as a log, append if it already exists.</span></span>      |
| <span data-ttu-id="50445-143">-i</span><span class="sxs-lookup"><span data-stu-id="50445-143">-i</span></span>         | <span data-ttu-id="50445-144"><*directorio*> extraer archivos en la imagen de origen en el directorio .</span><span class="sxs-lookup"><span data-stu-id="50445-144"><*directory*> Extract files to the source image under the directory.</span></span> |
| <span data-ttu-id="50445-145">-cab</span><span class="sxs-lookup"><span data-stu-id="50445-145">-cab</span></span>       | <span data-ttu-id="50445-146"><*filename*> extraer el archivo del archivo del archivo.</span><span class="sxs-lookup"><span data-stu-id="50445-146"><*filename*> Extract the MSM cabinet to file.</span></span>                        |
| <span data-ttu-id="50445-147">-lfn</span><span class="sxs-lookup"><span data-stu-id="50445-147">-lfn</span></span>       | <span data-ttu-id="50445-148">Use nombres de archivo largos durante la extracción.</span><span class="sxs-lookup"><span data-stu-id="50445-148">Use Long File Names during the extraction.</span></span>                                 |
| <span data-ttu-id="50445-149">-configure</span><span class="sxs-lookup"><span data-stu-id="50445-149">-configure</span></span> | <span data-ttu-id="50445-150"><*nombre*> configurar el módulo mediante datos de un archivo.</span><span class="sxs-lookup"><span data-stu-id="50445-150"><*filename*> Configure the module using data from a file.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="50445-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="50445-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50445-152">Windows Installer Development Tools</span><span class="sxs-lookup"><span data-stu-id="50445-152">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="50445-153">Versiones, herramientas y redistribuibles publicados</span><span class="sxs-lookup"><span data-stu-id="50445-153">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



