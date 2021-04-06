---
description: La tabla de directorios especifica el diseño del directorio para el producto. Cada fila de la tabla indica un directorio tanto en el origen como en el destino.
ms.assetid: eaca30cb-fec1-49ca-8b23-5e54c583e3e2
title: Tabla de directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273445aef67e3f166255321d0ac0ccf1aee37515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002272"
---
# <a name="directory-table"></a><span data-ttu-id="4a6e1-104">Tabla de directorio</span><span class="sxs-lookup"><span data-stu-id="4a6e1-104">Directory Table</span></span>

<span data-ttu-id="4a6e1-105">La tabla de directorios especifica el diseño del directorio para el producto.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-105">The Directory table specifies the directory layout for the product.</span></span> <span data-ttu-id="4a6e1-106">Cada fila de la tabla indica un directorio tanto en el origen como en el destino.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-106">Each row of the table indicates a directory both at the source and the target.</span></span>

<span data-ttu-id="4a6e1-107">La tabla de directorio tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-107">The Directory table has the following columns.</span></span>



| <span data-ttu-id="4a6e1-108">Columna</span><span class="sxs-lookup"><span data-stu-id="4a6e1-108">Column</span></span>            | <span data-ttu-id="4a6e1-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="4a6e1-109">Type</span></span>                         | <span data-ttu-id="4a6e1-110">Clave</span><span class="sxs-lookup"><span data-stu-id="4a6e1-110">Key</span></span> | <span data-ttu-id="4a6e1-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="4a6e1-111">Nullable</span></span> |
|-------------------|------------------------------|-----|----------|
| <span data-ttu-id="4a6e1-112">Directorio</span><span class="sxs-lookup"><span data-stu-id="4a6e1-112">Directory</span></span>         | [<span data-ttu-id="4a6e1-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="4a6e1-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="4a6e1-114">Y</span><span class="sxs-lookup"><span data-stu-id="4a6e1-114">Y</span></span>   | <span data-ttu-id="4a6e1-115">N</span><span class="sxs-lookup"><span data-stu-id="4a6e1-115">N</span></span>        |
| <span data-ttu-id="4a6e1-116">Directorio \_ primario</span><span class="sxs-lookup"><span data-stu-id="4a6e1-116">Directory\_Parent</span></span> | [<span data-ttu-id="4a6e1-117">Identificador</span><span class="sxs-lookup"><span data-stu-id="4a6e1-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="4a6e1-118">N</span><span class="sxs-lookup"><span data-stu-id="4a6e1-118">N</span></span>   | <span data-ttu-id="4a6e1-119">Y</span><span class="sxs-lookup"><span data-stu-id="4a6e1-119">Y</span></span>        |
| <span data-ttu-id="4a6e1-120">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="4a6e1-120">DefaultDir</span></span>        | [<span data-ttu-id="4a6e1-121">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="4a6e1-121">DefaultDir</span></span>](defaultdir.md) | <span data-ttu-id="4a6e1-122">N</span><span class="sxs-lookup"><span data-stu-id="4a6e1-122">N</span></span>   | <span data-ttu-id="4a6e1-123">N</span><span class="sxs-lookup"><span data-stu-id="4a6e1-123">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="4a6e1-124">Columnas</span><span class="sxs-lookup"><span data-stu-id="4a6e1-124">Columns</span></span>

<dl> <dt>

<span data-ttu-id="4a6e1-125"><span id="Directory"></span><span id="directory"></span><span id="DIRECTORY"></span>Active</span><span class="sxs-lookup"><span data-stu-id="4a6e1-125"><span id="Directory"></span><span id="directory"></span><span id="DIRECTORY"></span>Directory</span></span>
</dt> <dd>

<span data-ttu-id="4a6e1-126">La columna de directorio contiene un identificador único para un directorio o ruta de acceso de directorio.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-126">The Directory column contains a unique identifier for a directory or directory path.</span></span> <span data-ttu-id="4a6e1-127">Esta columna puede contener el nombre de una propiedad que se establece en la ruta de acceso completa de un directorio de destino.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-127">This column can contain the name of a property that is set to the full path of a target directory.</span></span> <span data-ttu-id="4a6e1-128">Si esta columna contiene una propiedad, el directorio de destino toma el nombre especificado en la columna DefaultDir y toma el directorio primario especificado en la \_ columna principal del directorio.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-128">If this column contains a property, the target directory takes the name specified in the DefaultDir column and takes the parent directory specified in the Directory\_Parent column.</span></span>

<span data-ttu-id="4a6e1-129">El directorio de origen siempre toma el nombre especificado en la columna DefaultDir y toma el directorio primario especificado en la \_ columna principal del directorio.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-129">The source directory always takes the name specified in the DefaultDir column and takes the parent directory specified in the Directory\_Parent column.</span></span>

<span data-ttu-id="4a6e1-130">Si la \_ columna principal del directorio es null o igual al valor de la columna Directory, la columna Directory representa un directorio de destino raíz.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-130">If the Directory\_Parent column is either null or equal to the value of the Directory column, the Directory column represents a root target directory.</span></span> <span data-ttu-id="4a6e1-131">Solo se puede especificar un directorio raíz en la tabla de directorios.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-131">Only one root directory may be specified in the Directory table.</span></span>

</dd> <dt>

<span data-ttu-id="4a6e1-132"><span id="Directory_Parent"></span><span id="directory_parent"></span><span id="DIRECTORY_PARENT"></span>Directorio \_ primario</span><span class="sxs-lookup"><span data-stu-id="4a6e1-132"><span id="Directory_Parent"></span><span id="directory_parent"></span><span id="DIRECTORY_PARENT"></span>Directory\_Parent</span></span>
</dt> <dd>

<span data-ttu-id="4a6e1-133">Esta columna es una referencia al directorio principal del directorio.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-133">This column is a reference to the directory's parent directory.</span></span> <span data-ttu-id="4a6e1-134">Un registro que tiene una \_ columna principal de directorio igual a NULL o igual que la columna de directorio representa un directorio raíz.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-134">A record that has a Directory\_Parent column equal to null or equal to the Directory column represents a root directory.</span></span> <span data-ttu-id="4a6e1-135">La ruta de acceso completa del directorio principal se resuelve por referencia en la \_ columna principal del directorio es una clave externa en la columna directorio.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-135">The full path of the parent directory is resolved by reference in the Directory\_Parent column is an external key into the Directory column.</span></span> <span data-ttu-id="4a6e1-136">Por ejemplo, si una carpeta tiene un directorio principal denominado PDIR, el directorio principal de PDIR se proporciona en la \_ columna principal de directorio de la fila con PDIR en la columna directorio.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-136">For example, if a folder has a parent directory named PDIR, the parent directory of PDIR is given in the Directory\_Parent column of the row with PDIR in the Directory column.</span></span>

</dd> <dt>

<span data-ttu-id="4a6e1-137"><span id="DefaultDir"></span><span id="defaultdir"></span><span id="DEFAULTDIR"></span>DefaultDir</span><span class="sxs-lookup"><span data-stu-id="4a6e1-137"><span id="DefaultDir"></span><span id="defaultdir"></span><span id="DEFAULTDIR"></span>DefaultDir</span></span>
</dt> <dd>

<span data-ttu-id="4a6e1-138">La columna DefaultDir contiene el nombre del directorio (localizable) en el directorio principal.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-138">The DefaultDir column contains the directory's name (localizable)under the parent directory.</span></span> <span data-ttu-id="4a6e1-139">De forma predeterminada, es el nombre de los directorios de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-139">By default, this is the name of both the target and source directories.</span></span> <span data-ttu-id="4a6e1-140">Para especificar los nombres de directorio de origen y de destino diferentes, separe los nombres de origen y de destino con un signo de dos puntos de la manera siguiente: \[ targetName \] : \[ SourceName \] .</span><span class="sxs-lookup"><span data-stu-id="4a6e1-140">To specify different source and target directory names, separate the target and source names with a colon as follows: \[targetname\]:\[sourcename\].</span></span>

<span data-ttu-id="4a6e1-141">Si el valor de la \_ columna principal del directorio es null o es igual a la columna de directorio, la columna DefaultDir especifica el nombre de un directorio de origen raíz.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-141">If the value of the Directory\_Parent column is null or is equal to the Directory column, the DefaultDir column specifies the name of a root source directory.</span></span>

<span data-ttu-id="4a6e1-142">Para un directorio de origen no raíz, un punto (.) especificado en la columna DefaultDir para el nombre del directorio de origen o el nombre del directorio de destino indica que el directorio debe estar ubicado en el directorio primario sin un subdirectorio.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-142">For a non-root source directory, a period (.) entered in the DefaultDir column for the source directory name or the target directory name indicates the directory should be located in its parent directory without a subdirectory.</span></span>

<span data-ttu-id="4a6e1-143">Los nombres de directorio de esta columna se pueden formatear como pares de nombre de archivo corto de nombre de archivo \| .</span><span class="sxs-lookup"><span data-stu-id="4a6e1-143">The directory names in this column may be formatted as short filename \| long filename pairs.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a6e1-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4a6e1-144">Remarks</span></span>

<span data-ttu-id="4a6e1-145">Cada registro de la tabla representa un directorio en las imágenes de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-145">Each record in the table represents a directory in both the source and the destination images.</span></span> <span data-ttu-id="4a6e1-146">La tabla de directorio debe especificar un único directorio raíz con un valor de columna de directorio igual a la propiedad [**targetDir**](targetdir.md) .</span><span class="sxs-lookup"><span data-stu-id="4a6e1-146">The Directory table must specify a single root directory with a Directory column value equal to the [**TARGETDIR**](targetdir.md) property.</span></span>

<span data-ttu-id="4a6e1-147">Para una [instalación administrativa](administrative-installation.md), instale la imagen administrativa en el directorio raíz denominado targetdir y use los nombres de directorio de origen para resolver los directorios de destino.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-147">For an [administrative installation](administrative-installation.md), install the administrative image into the root directory named TARGETDIR and use the source directory names to resolve the target directories.</span></span>

<span data-ttu-id="4a6e1-148">Nota el instalador establece varias propiedades estándar en [las](properties.md) rutas de acceso a las carpetas del sistema.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-148">Note the installer sets a number of standard [properties](properties.md) to system folder paths.</span></span> <span data-ttu-id="4a6e1-149">Vea la [referencia](property-reference.md) de propiedades para obtener una lista de las propiedades que se establecen en carpetas del sistema.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-149">See the [Property Reference](property-reference.md) for a list of the properties that are set to system folders.</span></span>

<span data-ttu-id="4a6e1-150">La resolución de directorios se realiza durante la [acción CostFinalize](costfinalize-action.md) y se realiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="4a6e1-150">Directory resolution is performed during the [CostFinalize action](costfinalize-action.md) and is done as follows:</span></span>

### <a name="root-destination-directory"></a><span data-ttu-id="4a6e1-151">Directorio de destino raíz</span><span class="sxs-lookup"><span data-stu-id="4a6e1-151">Root Destination Directory</span></span>

<span data-ttu-id="4a6e1-152">Solo puede haber un único directorio de destino de raíz.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-152">There may only be a single root destination directory.</span></span> <span data-ttu-id="4a6e1-153">Para especificar el directorio raíz de destino, establezca la columna directorio en la propiedad [**targetDir**](targetdir.md) y la columna DefaultDir en la propiedad [**SourceDir**](sourcedir.md) .</span><span class="sxs-lookup"><span data-stu-id="4a6e1-153">To specify the root destination directory, set the Directory column to the [**TARGETDIR**](targetdir.md) property and the DefaultDir column to the [**SourceDir**](sourcedir.md) property.</span></span> <span data-ttu-id="4a6e1-154">Si se define la propiedad **targetDir** , el directorio de destino se resuelve en el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-154">If the **TARGETDIR** property is defined, the destination directory is resolved to the property's value.</span></span> <span data-ttu-id="4a6e1-155">Si la propiedad **targetDir** es undefined, la propiedad [**ROOTDRIVE**](rootdrive.md) se utiliza para resolver la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-155">If the **TARGETDIR** property is undefined, the [**ROOTDRIVE**](rootdrive.md) property is used to resolve the path.</span></span>

### <a name="root-source-directory"></a><span data-ttu-id="4a6e1-156">Directorio de origen raíz</span><span class="sxs-lookup"><span data-stu-id="4a6e1-156">Root Source Directory</span></span>

<span data-ttu-id="4a6e1-157">El valor de la columna DefaultDir para la entrada de directorio raíz debe establecerse en la propiedad [**SourceDir**](sourcedir.md) .</span><span class="sxs-lookup"><span data-stu-id="4a6e1-157">The value of the DefaultDir column for the root directory entry must be set to the [**SourceDir**](sourcedir.md) property.</span></span>

### <a name="non-root-destination-directories"></a><span data-ttu-id="4a6e1-158">Directorios de destino no raíz</span><span class="sxs-lookup"><span data-stu-id="4a6e1-158">Non-root Destination Directories</span></span>

<span data-ttu-id="4a6e1-159">El valor del directorio de un directorio no raíz también se interpreta como el nombre de una propiedad que define la ubicación del destino.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-159">The Directory value for a non-root directory is also interpreted as the name of a property defining the location of the destination.</span></span> <span data-ttu-id="4a6e1-160">Si se define la propiedad, el directorio de destino se resuelve en el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-160">If the property is defined, the destination directory is resolved to the property's value.</span></span> <span data-ttu-id="4a6e1-161">Si no se define la propiedad, el directorio de destino se resuelve en un subdirectorio bajo el directorio de destino resuelto para la \_ entrada principal del directorio.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-161">If the property is not defined, the destination directory is resolved to a subdirectory beneath the resolved destination directory for the Directory\_Parent entry.</span></span> <span data-ttu-id="4a6e1-162">El valor de DefaultDir define el nombre del subdirectorio.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-162">The DefaultDir value defines the name of the subdirectory.</span></span>

### <a name="non-root-source-directories"></a><span data-ttu-id="4a6e1-163">Directorios de origen no raíz</span><span class="sxs-lookup"><span data-stu-id="4a6e1-163">Non-root Source Directories</span></span>

<span data-ttu-id="4a6e1-164">El directorio de origen de un directorio no raíz se resuelve en un subdirectorio del directorio de origen resuelto para la \_ entrada principal del directorio.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-164">The source directory for a non-root directory is resolved to a subdirectory of the resolved source directory for the Directory\_Parent entry.</span></span> <span data-ttu-id="4a6e1-165">De nuevo, el valor de DefaultDir define el nombre del subdirectorio.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-165">Again, the DefaultDir value defines the name of the subdirectory.</span></span>

### <a name="short-or-long-file-names"></a><span data-ttu-id="4a6e1-166">Nombres de archivo cortos o largos</span><span class="sxs-lookup"><span data-stu-id="4a6e1-166">Short or Long File Names</span></span>

<span data-ttu-id="4a6e1-167">Al resolver directorios de destino, se usan los nombres cortos de archivo especificados en la columna DefaultDir si se establece la propiedad [**SHORTFILENAMES**](shortfilenames.md) o el volumen en el que se encuentra el directorio no admite nombres de archivo largos.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-167">When resolving destination directories, the short file names specified in the DefaultDir column are used if either the [**SHORTFILENAMES**](shortfilenames.md) property is set or the volume the directory is located on does not support long file names.</span></span> <span data-ttu-id="4a6e1-168">De lo contrario, se usa el nombre de archivo largo.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-168">Otherwise, the long file name is used.</span></span>

<span data-ttu-id="4a6e1-169">Tenga en cuenta que cuando se resuelven los directorios durante la acción CostFinalize, las claves de la tabla de directorio se convierten en [propiedades](properties.md) establecidas en rutas de acceso de directorio.</span><span class="sxs-lookup"><span data-stu-id="4a6e1-169">Note that when the directories are resolved during the CostFinalize action, the keys in the Directory table become [properties](properties.md) set to directory paths.</span></span>

[<span data-ttu-id="4a6e1-170">CreateFolder (tabla)</span><span class="sxs-lookup"><span data-stu-id="4a6e1-170">CreateFolder Table</span></span>](createfolder-table.md)

<span data-ttu-id="4a6e1-171">Para crear carpetas vacías durante una instalación, vea [CreateFolder Table](createfolder-table.md).</span><span class="sxs-lookup"><span data-stu-id="4a6e1-171">For creating empty folders during an installation, see [CreateFolder Table](createfolder-table.md).</span></span>

[<span data-ttu-id="4a6e1-172">Usar la tabla de directorio</span><span class="sxs-lookup"><span data-stu-id="4a6e1-172">Using the Directory Table</span></span>](using-the-directory-table.md)

<span data-ttu-id="4a6e1-173">Para obtener más información acerca de la tabla de directorios, incluidos ejemplos, consulte [uso de la tabla de directorios](using-the-directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="4a6e1-173">For more information about the Directory table, including samples, see [Using the Directory Table](using-the-directory-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="4a6e1-174">Validación</span><span class="sxs-lookup"><span data-stu-id="4a6e1-174">Validation</span></span>

<dl>

[<span data-ttu-id="4a6e1-175">ICE03</span><span class="sxs-lookup"><span data-stu-id="4a6e1-175">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="4a6e1-176">ICE06</span><span class="sxs-lookup"><span data-stu-id="4a6e1-176">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="4a6e1-177">ICE07</span><span class="sxs-lookup"><span data-stu-id="4a6e1-177">ICE07</span></span>](ice07.md)  
[<span data-ttu-id="4a6e1-178">ICE30</span><span class="sxs-lookup"><span data-stu-id="4a6e1-178">ICE30</span></span>](ice30.md)  
[<span data-ttu-id="4a6e1-179">ICE32</span><span class="sxs-lookup"><span data-stu-id="4a6e1-179">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="4a6e1-180">ICE38</span><span class="sxs-lookup"><span data-stu-id="4a6e1-180">ICE38</span></span>](ice38.md)  
[<span data-ttu-id="4a6e1-181">ICE46</span><span class="sxs-lookup"><span data-stu-id="4a6e1-181">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="4a6e1-182">ICE48</span><span class="sxs-lookup"><span data-stu-id="4a6e1-182">ICE48</span></span>](ice48.md)  
[<span data-ttu-id="4a6e1-183">ICE56</span><span class="sxs-lookup"><span data-stu-id="4a6e1-183">ICE56</span></span>](ice56.md)  
[<span data-ttu-id="4a6e1-184">ICE57</span><span class="sxs-lookup"><span data-stu-id="4a6e1-184">ICE57</span></span>](ice57.md)  
[<span data-ttu-id="4a6e1-185">ICE64</span><span class="sxs-lookup"><span data-stu-id="4a6e1-185">ICE64</span></span>](ice64.md)  
[<span data-ttu-id="4a6e1-186">ICE88</span><span class="sxs-lookup"><span data-stu-id="4a6e1-186">ICE88</span></span>](ice88.md)  
[<span data-ttu-id="4a6e1-187">ICE90</span><span class="sxs-lookup"><span data-stu-id="4a6e1-187">ICE90</span></span>](ice90.md)  
[<span data-ttu-id="4a6e1-188">ICE91</span><span class="sxs-lookup"><span data-stu-id="4a6e1-188">ICE91</span></span>](ice91.md)  
[<span data-ttu-id="4a6e1-189">ICE99</span><span class="sxs-lookup"><span data-stu-id="4a6e1-189">ICE99</span></span>](ice99.md)  
</dl>

 

 



