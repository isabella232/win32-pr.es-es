---
description: Los módulos de combinación proporcionan un método estándar para proporcionar componentes compartidos de Windows Installer y la lógica de configuración para las aplicaciones.
ms.assetid: 63ced106-12e3-4483-8bfe-22c54fe7a204
title: Usar la automatización para combinar un módulo de combinación en una base de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e28b8cfc1716cdbb296fd0a1410787ae55bb62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677523"
---
# <a name="using-automation-to-merge-a-merge-module-into-a-database"></a><span data-ttu-id="90b6b-103">Usar la automatización para combinar un módulo de combinación en una base de datos</span><span class="sxs-lookup"><span data-stu-id="90b6b-103">Using Automation to Merge a Merge Module into a Database</span></span>

<span data-ttu-id="90b6b-104">Los [módulos de combinación](merge-modules.md) proporcionan un método estándar para proporcionar [*componentes*](c-gly.md)compartidos de Windows Installer y la lógica de configuración para las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="90b6b-104">[Merge Modules](merge-modules.md) provide a standard method for you to deliver shared Windows Installer [*components*](c-gly.md), and setup logic to applications.</span></span>

<span data-ttu-id="90b6b-105">Los módulos de combinación se deben combinar en un paquete de instalación mediante una herramienta de combinación.</span><span class="sxs-lookup"><span data-stu-id="90b6b-105">Merge modules must be merged into an installation package by using a merge tool.</span></span> <span data-ttu-id="90b6b-106">El procedimiento recomendado es obtener una herramienta de combinación distribuida de forma gratuita o comprar una de las herramientas de combinación que están disponibles en proveedores de software independientes, por ejemplo, puede usar [Mergemod.dll](merge-module-automation.md).</span><span class="sxs-lookup"><span data-stu-id="90b6b-106">The best practice is to obtain a freely distributed merge tool, or purchase one of the merge tools that are available from independent software vendors, for example, you can use [Mergemod.dll](merge-module-automation.md).</span></span>

<span data-ttu-id="90b6b-107">En el procedimiento siguiente se muestra cómo combinar un módulo de combinación en una base de datos de Windows Installer mediante la [automatización del módulo de combinación](merge-module-automation.md).</span><span class="sxs-lookup"><span data-stu-id="90b6b-107">The following procedure shows you how to merge a merge module into a Windows Installer database by using [Merge Module Automation](merge-module-automation.md).</span></span>

<span data-ttu-id="90b6b-108">**Para combinar un módulo en una base de datos**</span><span class="sxs-lookup"><span data-stu-id="90b6b-108">**To merge a module into a database**</span></span>

1.  <span data-ttu-id="90b6b-109">Abra un archivo de registro mediante el método [**openlog**](merge-openlog.md) .</span><span class="sxs-lookup"><span data-stu-id="90b6b-109">Open a log file by using the [**OpenLog**](merge-openlog.md) method.</span></span>

    <span data-ttu-id="90b6b-110">Este paso solo es necesario si necesita crear un archivo de registro o anexar un archivo de registro existente para el proceso de mezcla.</span><span class="sxs-lookup"><span data-stu-id="90b6b-110">This step is required only if you need to create a log file, or append an existing log file for the merge process.</span></span>

2.  <span data-ttu-id="90b6b-111">Abra la base de datos de instalación [. msi](windows-installer-file-extensions.md) mediante el método [**OpenDatabase**](merge-opendatabase.md) del [**objeto Merge**](merge-object.md).</span><span class="sxs-lookup"><span data-stu-id="90b6b-111">Open the [.msi](windows-installer-file-extensions.md) installation database by using the [**OpenDatabase**](merge-opendatabase.md) method of the [**Merge Object**](merge-object.md).</span></span>

    <span data-ttu-id="90b6b-112">Este paso es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="90b6b-112">This step is required.</span></span>

    <span data-ttu-id="90b6b-113">La base de datos que abre es aquella en la que desea recibir el módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="90b6b-113">The database that you open is the one that you want to receive the merge module.</span></span>

3.  <span data-ttu-id="90b6b-114">Abra el módulo de combinación [. MSM](windows-installer-file-extensions.md) con el método [**OpenModule**](merge-openmodule.md) .</span><span class="sxs-lookup"><span data-stu-id="90b6b-114">Open the [.msm](windows-installer-file-extensions.md) merge module by using the [**OpenModule**](merge-openmodule.md) method.</span></span>

    <span data-ttu-id="90b6b-115">Este paso es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="90b6b-115">This step is required.</span></span>

    <span data-ttu-id="90b6b-116">Éste es el módulo de combinación que se combina en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="90b6b-116">This is the merge module that is being merged into the database.</span></span> <span data-ttu-id="90b6b-117">Un módulo debe estar abierto antes de que se pueda combinar con una base de datos de instalación.</span><span class="sxs-lookup"><span data-stu-id="90b6b-117">A module must be opened before it can be merged with an installation database.</span></span>

4.  <span data-ttu-id="90b6b-118">Combine el módulo en la base de datos de instalación mediante una llamada al método [**Merge**](merge-object.md) o al método [**MergeEx**](merge-mergeex.md) .</span><span class="sxs-lookup"><span data-stu-id="90b6b-118">Merge the module into the installation database by calling the [**Merge**](merge-object.md) method or [**MergeEx**](merge-mergeex.md) method.</span></span>

    <span data-ttu-id="90b6b-119">Este paso es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="90b6b-119">This step is required.</span></span>

    <span data-ttu-id="90b6b-120">Solo se puede llamar una vez al método [**Merge**](merge-object.md) o al método [**MergeEx**](merge-mergeex.md) para combinar una combinación específica de archivos [. msi](windows-installer-file-extensions.md) y. msm.</span><span class="sxs-lookup"><span data-stu-id="90b6b-120">The [**Merge**](merge-object.md) method or [**MergeEx**](merge-mergeex.md) method can only be called one time to merge a specific combination of [.msi](windows-installer-file-extensions.md) and .msm files.</span></span>

    > [!Note]  
    > <span data-ttu-id="90b6b-121">El método [**MergeEx**](merge-mergeex.md) solo está disponible en [Mergemod.dll versión 2,0](merge-module-automation.md) o posterior, y solo cuando se usa la interfaz [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) .</span><span class="sxs-lookup"><span data-stu-id="90b6b-121">The [**MergeEx**](merge-mergeex.md) method is only available in [Mergemod.dll version 2.0](merge-module-automation.md) or later, and only when using the [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) interface.</span></span>

     

5.  <span data-ttu-id="90b6b-122">Recupere la propiedad [**Errors**](merge-errors.md) y examine la colección de objetos de [**error**](error-object.md) que devuelve para conflictos de combinación u otros errores.</span><span class="sxs-lookup"><span data-stu-id="90b6b-122">Retrieve the [**Errors**](merge-errors.md) property and examine the collection of [**Error**](error-object.md) objects it returns for merge conflicts or other errors.</span></span>

    <span data-ttu-id="90b6b-123">Debe resolver los errores.</span><span class="sxs-lookup"><span data-stu-id="90b6b-123">You must resolve any errors.</span></span>

    <span data-ttu-id="90b6b-124">La recuperación no es destructiva y se pueden recuperar varias instancias de la colección de errores mediante la lectura repetida de la propiedad [**errores**](merge-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="90b6b-124">The retrieval is nondestructive, and multiple instances of the error collection can be retrieved by repeatedly reading the [**Errors**](merge-errors.md) property.</span></span>

6.  <span data-ttu-id="90b6b-125">Asocie los componentes del módulo de combinación con las características de mediante el método [**Connect**](merge-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="90b6b-125">Associate the components of the merge module with the features by using the [**Connect**](merge-connect.md) method.</span></span>

    <span data-ttu-id="90b6b-126">Este paso solo es necesario si tiene características existentes y desea agregar características para combinarlas en la base de datos de instalación.</span><span class="sxs-lookup"><span data-stu-id="90b6b-126">This step is only required if you have existing features and you want to add features to merge into the installation database.</span></span>

    <span data-ttu-id="90b6b-127">Una característica debe existir antes de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="90b6b-127">A feature must exist before you call this method.</span></span> <span data-ttu-id="90b6b-128">Para obtener más información, vea [conectar un módulo de combinación a varias características](connecting-a-merge-module-to-multiple-features.md).</span><span class="sxs-lookup"><span data-stu-id="90b6b-128">For more information, see [Connecting a Merge Module to Multiple Features](connecting-a-merge-module-to-multiple-features.md).</span></span>

7.  <span data-ttu-id="90b6b-129">Si es necesario, extraiga los archivos de origen del módulo mediante uno o varios de los siguientes procedimientos:</span><span class="sxs-lookup"><span data-stu-id="90b6b-129">If necessary, extract source files from the module by doing one or more of the following:</span></span>
    -   <span data-ttu-id="90b6b-130">Use [**ExtractFiles**](merge-extractfiles.md) o [**ExtractFilesEx**](merge-extractfilesex.md) para extraer archivos de un archivo. cab incrustado y, a continuación, cópielo en un directorio especificado.</span><span class="sxs-lookup"><span data-stu-id="90b6b-130">Use [**ExtractFiles**](merge-extractfiles.md) or [**ExtractFilesEx**](merge-extractfilesex.md) to extract files from an embedded .cab file and then copy into a specified directory.</span></span>
        > [!Note]  
        > <span data-ttu-id="90b6b-131">[**ExtractFilesEx**](merge-extractfilesex.md) requiere [Mergemod.dll versión 2,0](merge-module-automation.md) o posterior.</span><span class="sxs-lookup"><span data-stu-id="90b6b-131">[**ExtractFilesEx**](merge-extractfilesex.md) requires [Mergemod.dll version 2.0](merge-module-automation.md) or later.</span></span>

         

    -   <span data-ttu-id="90b6b-132">Use [**ExtractCAB**](merge-extractcab.md) para extraer archivos de un archivo. cab incrustado y, a continuación, guárdelos en un archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="90b6b-132">Use [**ExtractCAB**](merge-extractcab.md) to extract files from an embedded .cab file, and then save in a specified file.</span></span>
    -   <span data-ttu-id="90b6b-133">Use [**CreateSourceImage**](merge-createsourceimage.md) para extraer archivos de un módulo y, después de la fusión mediante combinación, cópielo en una imagen de origen en el disco.</span><span class="sxs-lookup"><span data-stu-id="90b6b-133">Use [**CreateSourceImage**](merge-createsourceimage.md) to extract files from a module, and then after the merge, copy to a source image on disk.</span></span>
        > [!Note]  
        > <span data-ttu-id="90b6b-134">[**CreateSourceImage**](merge-createsourceimage.md) solo está disponible en [Mergemod.dll versión 2,0](merge-module-automation.md) o posterior.</span><span class="sxs-lookup"><span data-stu-id="90b6b-134">[**CreateSourceImage**](merge-createsourceimage.md) is only available in [Mergemod.dll version 2.0](merge-module-automation.md) or later.</span></span>

         
8.  <span data-ttu-id="90b6b-135">Cierre el módulo de combinación abierto actual mediante el método [**CloseModule**](merge-closemodule.md) .</span><span class="sxs-lookup"><span data-stu-id="90b6b-135">Close the current open merge module by using the [**CloseModule**](merge-closemodule.md) method.</span></span>

    <span data-ttu-id="90b6b-136">Este paso es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="90b6b-136">This step is required.</span></span>

9.  <span data-ttu-id="90b6b-137">Cierre la base de datos de instalación abierta con el método [**CerrarBaseDeDatos**](merge-closedatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="90b6b-137">Close the open installation database by using the [**CloseDatabase**](merge-closedatabase.md) method.</span></span>

    <span data-ttu-id="90b6b-138">Este paso es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="90b6b-138">This step is required.</span></span>

    <span data-ttu-id="90b6b-139">Al cerrar una base de datos, se borra toda la información de dependencias, pero no se producen errores que no se recuperen.</span><span class="sxs-lookup"><span data-stu-id="90b6b-139">Closing a database clears all dependency information, but does not affect any errors that are not retrieved.</span></span>

10. <span data-ttu-id="90b6b-140">Cierre el archivo de registro actual mediante el método [**closelog**](merge-closelog.md) .</span><span class="sxs-lookup"><span data-stu-id="90b6b-140">Close the current log file by using the [**CloseLog**](merge-closelog.md) method.</span></span>

    <span data-ttu-id="90b6b-141">Este paso es necesario si tiene un archivo de registro abierto.</span><span class="sxs-lookup"><span data-stu-id="90b6b-141">This step is required if you have an open log file.</span></span>

<span data-ttu-id="90b6b-142">Una vez que el módulo se ha combinado en la base de datos mediante [Mergemod.dll](merge-module-automation.md), la [tabla de medios](media-table.md) debe actualizarse para describir el diseño de la imagen de origen deseada.</span><span class="sxs-lookup"><span data-stu-id="90b6b-142">After the module has been merged into the database using [Mergemod.dll](merge-module-automation.md), the [Media Table](media-table.md) must be updated to describe the desired source image layout.</span></span> <span data-ttu-id="90b6b-143">El proceso de mezcla proporcionado por Mergemod.dll no actualiza la tabla de medios porque el consumidor del módulo de combinación puede seleccionar varias maneras de diseñar la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="90b6b-143">The merge process provided by Mergemod.dll does not update the Media Table because the consumer of the merge module can select various ways to layout the source image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90b6b-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="90b6b-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90b6b-145">Versiones publicadas, herramientas y redistribuibles</span><span class="sxs-lookup"><span data-stu-id="90b6b-145">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



