---
description: ICE35 valida que los componentes que contienen archivos comprimidos almacenados en un archivo. cab no estén configurados para ejecutarse desde el origen. Con Windows Installer 2,0 o posterior, esta restricción se ha quitado.
ms.assetid: b4df27e2-9790-4b18-a173-25fa8b0ecd4d
title: ICE35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea6a98079d3c57e0c796332cf0cd5f11045a07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002252"
---
# <a name="ice35"></a><span data-ttu-id="8417e-104">ICE35</span><span class="sxs-lookup"><span data-stu-id="8417e-104">ICE35</span></span>

<span data-ttu-id="8417e-105">ICE35 valida que los componentes que contienen archivos comprimidos almacenados en un [archivo. cab](cabinet-files.md) no estén configurados para ejecutarse desde el origen.</span><span class="sxs-lookup"><span data-stu-id="8417e-105">ICE35 validates that components containing compressed files stored in a [cabinet file](cabinet-files.md) are not set to run from source.</span></span> <span data-ttu-id="8417e-106">Con Windows Installer 2,0 o posterior, esta restricción se ha quitado.</span><span class="sxs-lookup"><span data-stu-id="8417e-106">With Windows Installer 2.0 or later, this restriction has been removed.</span></span>

<span data-ttu-id="8417e-107">ICE35 consulta la columna Cabinet de la [tabla de medios](media-table.md) para determinar qué archivos se comprimen y almacenan en un archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="8417e-107">ICE35 queries the Cabinet column of the [Media table](media-table.md) to determine which files are compressed and stored in a cabinet file.</span></span> <span data-ttu-id="8417e-108">Consulta la [tabla de archivos](file-table.md) para determinar qué componentes contienen estos archivos.</span><span class="sxs-lookup"><span data-stu-id="8417e-108">It queries the [File table](file-table.md) to determine which components contain these files.</span></span> <span data-ttu-id="8417e-109">Finalmente, comprueba la [tabla de componentes](component-table.md) para determinar si los bits de origen de ejecución se establecen en la columna de atributos.</span><span class="sxs-lookup"><span data-stu-id="8417e-109">Finally, it checks the [Component table](component-table.md) to determine whether the run-from-source bits are set in the Attributes column.</span></span>

## <a name="result"></a><span data-ttu-id="8417e-110">Resultado</span><span class="sxs-lookup"><span data-stu-id="8417e-110">Result</span></span>

<span data-ttu-id="8417e-111">ICE35 envía un mensaje de error si hay un archivo comprimido almacenado en un archivo. cab que pertenece a un componente con el bit msidbComponentAttributesSourceOnly establecido en la columna Attributes de la [tabla Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="8417e-111">ICE35 posts an error message if there is a compressed file stored in a cabinet file belonging to a component with the msidbComponentAttributesSourceOnly bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="8417e-112">Con Windows Installer 2,0 o posterior, se cambia de un error a un mensaje de advertencia.</span><span class="sxs-lookup"><span data-stu-id="8417e-112">With Windows Installer 2.0 or later, this is changed from an error to a warning message.</span></span> <span data-ttu-id="8417e-113">Un paquete que solo admite Windows Installer 2,0 y versiones posteriores tiene la \_ propiedad de PID PAGECOUNT de la secuencia de información de Resumen establecida en un valor de al menos 200.</span><span class="sxs-lookup"><span data-stu-id="8417e-113">A package that supports only Windows Installer 2.0 and later has the PID\_PAGECOUNT property of the Summary Information Stream set to a value of at least 200.</span></span>

<span data-ttu-id="8417e-114">ICE35 envía un mensaje de advertencia si hay un archivo comprimido almacenado en un archivo. cab que pertenece a un componente con el bit msidbComponentAttributesOptional establecido en la columna atributos de la [tabla componente](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="8417e-114">ICE35 posts warning message if there is a compressed file stored in a cabinet file belonging to a component with the msidbComponentAttributesOptional bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="8417e-115">Este mensaje de advertencia se ha quitado con Windows Installer 2,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="8417e-115">This warning message has been removed with Windows Installer 2.0 and later.</span></span>

<span data-ttu-id="8417e-116">Si hay varios archivos en un componente en un archivo. cab, ICE35 informa de los errores de cada archivo que tiene el conjunto de bits de origen ejecutado.</span><span class="sxs-lookup"><span data-stu-id="8417e-116">If multiple files in a component are in a cabinet file, ICE35 reports errors for each file that has the run from source bit set.</span></span>

## <a name="example"></a><span data-ttu-id="8417e-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8417e-117">Example</span></span>

<span data-ttu-id="8417e-118">ICE35 notifica los siguientes errores y advertencias para el ejemplo que se muestra con una versión anterior a Windows Installer versión 2,0.</span><span class="sxs-lookup"><span data-stu-id="8417e-118">ICE35 reports the following errors and warnings for the example shown using a version earlier than Windows Installer version 2.0.</span></span>



| <span data-ttu-id="8417e-119">Error ICE35</span><span class="sxs-lookup"><span data-stu-id="8417e-119">ICE35 Error</span></span>                                                                                                | <span data-ttu-id="8417e-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="8417e-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8417e-121">ERROR: el componente Component3 no se puede ejecutar solo desde el origen, porque su archivo de miembro ' Archivo3 ' está comprimido.</span><span class="sxs-lookup"><span data-stu-id="8417e-121">ERROR: Component Component3 cannot be Run From Source only, because its member file 'File3' is compressed.</span></span> | <span data-ttu-id="8417e-122">Hay un archivo comprimido almacenado en un archivo. cab y este archivo pertenece a un componente con el bit SourceOnly establecido en la columna Attributes de la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="8417e-122">There is a compressed file stored in a cabinet file and this file belongs to a component with the SourceOnly bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="8417e-123">Para corregir este error, cambie los 2 bits inferiores del valor de los atributos Component2's a "00", lo que significa solo local o quite File4 del archivo. CAB.</span><span class="sxs-lookup"><span data-stu-id="8417e-123">To fix this error change the lower 2 bits of Component2's Attributes value to "00", meaning Local only, or remove File4 from the CAB file.</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="8417e-124">ERROR: el componente Component3 no se puede ejecutar solo desde el origen, porque su archivo de miembro ' Archivo3 ' está comprimido.</span><span class="sxs-lookup"><span data-stu-id="8417e-124">ERROR: Component Component3 cannot be Run From Source only, because its member file 'File3' is compressed.</span></span> | <span data-ttu-id="8417e-125">Hay un archivo comprimido almacenado en un archivo. cab y este archivo pertenece a un componente con el bit SourceOnly establecido en la columna Attributes de la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="8417e-125">There is a compressed file stored in a cabinet file and this file belongs to a component with the SourceOnly bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="8417e-126">Dado que no todos los archivos de un componente tienen que proceder de los mismos medios, ICE35 informa de los errores de cada archivo del componente que se encuentra en un archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="8417e-126">Because the files in a component do not all have to originate from the same media, ICE35 reports errors for each file in the component that is in a cabinet.</span></span><br/> <span data-ttu-id="8417e-127">Para corregir este error, cambie los 2 bits inferiores del valor de los atributos Component2's a "00", lo que significa solo local o quite File4 del archivo. CAB.</span><span class="sxs-lookup"><span data-stu-id="8417e-127">To fix this error change the lower 2 bits of Component2's Attributes value to "00", meaning Local only, or remove File4 from the CAB file.</span></span><br/> |



 

<span data-ttu-id="8417e-128">[Tabla de medios](media-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="8417e-128">[Media Table](media-table.md) (partial)</span></span>



| <span data-ttu-id="8417e-129">DiskID</span><span class="sxs-lookup"><span data-stu-id="8417e-129">DiskID</span></span> | <span data-ttu-id="8417e-130">LastSequence</span><span class="sxs-lookup"><span data-stu-id="8417e-130">LastSequence</span></span> | <span data-ttu-id="8417e-131">Archiva</span><span class="sxs-lookup"><span data-stu-id="8417e-131">Cabinet</span></span>   |
|--------|--------------|-----------|
| <span data-ttu-id="8417e-132">1</span><span class="sxs-lookup"><span data-stu-id="8417e-132">1</span></span>      | <span data-ttu-id="8417e-133">2</span><span class="sxs-lookup"><span data-stu-id="8417e-133">2</span></span>            |           |
| <span data-ttu-id="8417e-134">2</span><span class="sxs-lookup"><span data-stu-id="8417e-134">2</span></span>      | <span data-ttu-id="8417e-135">4</span><span class="sxs-lookup"><span data-stu-id="8417e-135">4</span></span>            | <span data-ttu-id="8417e-136">One.cab</span><span class="sxs-lookup"><span data-stu-id="8417e-136">One.cab</span></span>   |
| <span data-ttu-id="8417e-137">3</span><span class="sxs-lookup"><span data-stu-id="8417e-137">3</span></span>      | <span data-ttu-id="8417e-138">5</span><span class="sxs-lookup"><span data-stu-id="8417e-138">5</span></span>            | <span data-ttu-id="8417e-139">\#Two.cab</span><span class="sxs-lookup"><span data-stu-id="8417e-139">\#Two.cab</span></span> |



 

<span data-ttu-id="8417e-140">[Tabla de archivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="8417e-140">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="8417e-141">Archivo</span><span class="sxs-lookup"><span data-stu-id="8417e-141">File</span></span>  | <span data-ttu-id="8417e-142">Componente\_</span><span class="sxs-lookup"><span data-stu-id="8417e-142">Component\_</span></span> | <span data-ttu-id="8417e-143">Secuencia</span><span class="sxs-lookup"><span data-stu-id="8417e-143">Sequence</span></span> |
|-------|-------------|----------|
| <span data-ttu-id="8417e-144">Archivo1</span><span class="sxs-lookup"><span data-stu-id="8417e-144">File1</span></span> | <span data-ttu-id="8417e-145">Component1</span><span class="sxs-lookup"><span data-stu-id="8417e-145">Component1</span></span>  | <span data-ttu-id="8417e-146">1</span><span class="sxs-lookup"><span data-stu-id="8417e-146">1</span></span>        |
| <span data-ttu-id="8417e-147">Archivo2</span><span class="sxs-lookup"><span data-stu-id="8417e-147">File2</span></span> | <span data-ttu-id="8417e-148">Component2</span><span class="sxs-lookup"><span data-stu-id="8417e-148">Component2</span></span>  | <span data-ttu-id="8417e-149">2</span><span class="sxs-lookup"><span data-stu-id="8417e-149">2</span></span>        |
| <span data-ttu-id="8417e-150">File3</span><span class="sxs-lookup"><span data-stu-id="8417e-150">File3</span></span> | <span data-ttu-id="8417e-151">Component2</span><span class="sxs-lookup"><span data-stu-id="8417e-151">Component2</span></span>  | <span data-ttu-id="8417e-152">3</span><span class="sxs-lookup"><span data-stu-id="8417e-152">3</span></span>        |
| <span data-ttu-id="8417e-153">File4</span><span class="sxs-lookup"><span data-stu-id="8417e-153">File4</span></span> | <span data-ttu-id="8417e-154">Component3</span><span class="sxs-lookup"><span data-stu-id="8417e-154">Component3</span></span>  | <span data-ttu-id="8417e-155">4</span><span class="sxs-lookup"><span data-stu-id="8417e-155">4</span></span>        |
| <span data-ttu-id="8417e-156">File5</span><span class="sxs-lookup"><span data-stu-id="8417e-156">File5</span></span> | <span data-ttu-id="8417e-157">Component3</span><span class="sxs-lookup"><span data-stu-id="8417e-157">Component3</span></span>  | <span data-ttu-id="8417e-158">5</span><span class="sxs-lookup"><span data-stu-id="8417e-158">5</span></span>        |



 

<span data-ttu-id="8417e-159">[Tabla de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="8417e-159">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="8417e-160">Componente</span><span class="sxs-lookup"><span data-stu-id="8417e-160">Component</span></span>  | <span data-ttu-id="8417e-161">Atributos</span><span class="sxs-lookup"><span data-stu-id="8417e-161">Attributes</span></span> |
|------------|------------|
| <span data-ttu-id="8417e-162">Component1</span><span class="sxs-lookup"><span data-stu-id="8417e-162">Component1</span></span> | <span data-ttu-id="8417e-163">0</span><span class="sxs-lookup"><span data-stu-id="8417e-163">0</span></span>          |
| <span data-ttu-id="8417e-164">Component2</span><span class="sxs-lookup"><span data-stu-id="8417e-164">Component2</span></span> | <span data-ttu-id="8417e-165">2</span><span class="sxs-lookup"><span data-stu-id="8417e-165">2</span></span>          |
| <span data-ttu-id="8417e-166">Component3</span><span class="sxs-lookup"><span data-stu-id="8417e-166">Component3</span></span> | <span data-ttu-id="8417e-167">1</span><span class="sxs-lookup"><span data-stu-id="8417e-167">1</span></span>          |



 

<span data-ttu-id="8417e-168">[Tabla de acceso directo](shortcut-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="8417e-168">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="8417e-169">Acceso directo</span><span class="sxs-lookup"><span data-stu-id="8417e-169">Shortcut</span></span>  | <span data-ttu-id="8417e-170">Icono\_</span><span class="sxs-lookup"><span data-stu-id="8417e-170">Icon\_</span></span> |
|-----------|--------|
| <span data-ttu-id="8417e-171">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="8417e-171">Shortcut1</span></span> | <span data-ttu-id="8417e-172">Icon2</span><span class="sxs-lookup"><span data-stu-id="8417e-172">Icon2</span></span>  |



 

<span data-ttu-id="8417e-173">Tenga en cuenta que los archivos también se pueden marcar como comprimidos mediante la propiedad [**recuento de palabras**](word-count-summary.md) de la [secuencia de información de Resumen](summary-information-stream.md).</span><span class="sxs-lookup"><span data-stu-id="8417e-173">Note that files can also be marked as compressed using the [**Word Count Summary**](word-count-summary.md) Property of the [Summary Information stream](summary-information-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8417e-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8417e-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8417e-175">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="8417e-175">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




