---
description: En la tabla de medios se describe el conjunto de discos que componen el medio de origen para la instalación.
ms.assetid: f9789f1d-35bf-40d6-9724-d5a160a0d06d
title: Tabla de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a59cd8bf864aa890891873ed92a39225c6eebdf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361850"
---
# <a name="media-table"></a><span data-ttu-id="fd520-103">Tabla de medios</span><span class="sxs-lookup"><span data-stu-id="fd520-103">Media Table</span></span>

<span data-ttu-id="fd520-104">En la tabla de medios se describe el conjunto de discos que componen el medio de origen para la instalación.</span><span class="sxs-lookup"><span data-stu-id="fd520-104">The Media table describes the set of disks that make up the source media for the installation.</span></span>

<span data-ttu-id="fd520-105">La tabla de medios contiene las columnas que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="fd520-105">The Media table contains the columns shown in the following table.</span></span>



| <span data-ttu-id="fd520-106">Columna</span><span class="sxs-lookup"><span data-stu-id="fd520-106">Column</span></span>       | <span data-ttu-id="fd520-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="fd520-107">Type</span></span>                     | <span data-ttu-id="fd520-108">Clave</span><span class="sxs-lookup"><span data-stu-id="fd520-108">Key</span></span> | <span data-ttu-id="fd520-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="fd520-109">Nullable</span></span> |
|--------------|--------------------------|-----|----------|
| <span data-ttu-id="fd520-110">Detectaron</span><span class="sxs-lookup"><span data-stu-id="fd520-110">DiskId</span></span>       | [<span data-ttu-id="fd520-111">Entero</span><span class="sxs-lookup"><span data-stu-id="fd520-111">Integer</span></span>](integer.md)   | <span data-ttu-id="fd520-112">Y</span><span class="sxs-lookup"><span data-stu-id="fd520-112">Y</span></span>   | <span data-ttu-id="fd520-113">N</span><span class="sxs-lookup"><span data-stu-id="fd520-113">N</span></span>        |
| <span data-ttu-id="fd520-114">LastSequence</span><span class="sxs-lookup"><span data-stu-id="fd520-114">LastSequence</span></span> | [<span data-ttu-id="fd520-115">Entero</span><span class="sxs-lookup"><span data-stu-id="fd520-115">Integer</span></span>](integer.md)   | <span data-ttu-id="fd520-116">N</span><span class="sxs-lookup"><span data-stu-id="fd520-116">N</span></span>   | <span data-ttu-id="fd520-117">N</span><span class="sxs-lookup"><span data-stu-id="fd520-117">N</span></span>        |
| <span data-ttu-id="fd520-118">DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="fd520-118">DiskPrompt</span></span>   | [<span data-ttu-id="fd520-119">Texto</span><span class="sxs-lookup"><span data-stu-id="fd520-119">Text</span></span>](text.md)         | <span data-ttu-id="fd520-120">N</span><span class="sxs-lookup"><span data-stu-id="fd520-120">N</span></span>   | <span data-ttu-id="fd520-121">Y</span><span class="sxs-lookup"><span data-stu-id="fd520-121">Y</span></span>        |
| <span data-ttu-id="fd520-122">Archiva</span><span class="sxs-lookup"><span data-stu-id="fd520-122">Cabinet</span></span>      | [<span data-ttu-id="fd520-123">Archiva</span><span class="sxs-lookup"><span data-stu-id="fd520-123">Cabinet</span></span>](cabinet.md)   | <span data-ttu-id="fd520-124">N</span><span class="sxs-lookup"><span data-stu-id="fd520-124">N</span></span>   | <span data-ttu-id="fd520-125">Y</span><span class="sxs-lookup"><span data-stu-id="fd520-125">Y</span></span>        |
| <span data-ttu-id="fd520-126">VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="fd520-126">VolumeLabel</span></span>  | [<span data-ttu-id="fd520-127">Texto</span><span class="sxs-lookup"><span data-stu-id="fd520-127">Text</span></span>](text.md)         | <span data-ttu-id="fd520-128">N</span><span class="sxs-lookup"><span data-stu-id="fd520-128">N</span></span>   | <span data-ttu-id="fd520-129">Y</span><span class="sxs-lookup"><span data-stu-id="fd520-129">Y</span></span>        |
| <span data-ttu-id="fd520-130">Source</span><span class="sxs-lookup"><span data-stu-id="fd520-130">Source</span></span>       | [<span data-ttu-id="fd520-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fd520-131">Property</span></span>](property.md) | <span data-ttu-id="fd520-132">N</span><span class="sxs-lookup"><span data-stu-id="fd520-132">N</span></span>   | <span data-ttu-id="fd520-133">Y</span><span class="sxs-lookup"><span data-stu-id="fd520-133">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="fd520-134">Columnas</span><span class="sxs-lookup"><span data-stu-id="fd520-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="fd520-135"><span id="DiskId"></span><span id="diskid"></span><span id="DISKID"></span>Detectaron</span><span class="sxs-lookup"><span data-stu-id="fd520-135"><span id="DiskId"></span><span id="diskid"></span><span id="DISKID"></span>DiskId</span></span>
</dt> <dd>

<span data-ttu-id="fd520-136">Determina el criterio de ordenación de la tabla.</span><span class="sxs-lookup"><span data-stu-id="fd520-136">Determines the sort order for the table.</span></span> <span data-ttu-id="fd520-137">Este número debe ser igual o mayor que 1.</span><span class="sxs-lookup"><span data-stu-id="fd520-137">This number must be equal to or greater than 1.</span></span>

</dd> <dt>

<span data-ttu-id="fd520-138"><span id="LastSequence"></span><span id="lastsequence"></span><span id="LASTSEQUENCE"></span>LastSequence</span><span class="sxs-lookup"><span data-stu-id="fd520-138"><span id="LastSequence"></span><span id="lastsequence"></span><span id="LASTSEQUENCE"></span>LastSequence</span></span>
</dt> <dd>

<span data-ttu-id="fd520-139">Número de secuencia de archivo para el último archivo de este medio.</span><span class="sxs-lookup"><span data-stu-id="fd520-139">File sequence number for the last file for this media.</span></span> <span data-ttu-id="fd520-140">Los números de la columna LastSequence especifican qué archivos de la tabla de [archivos](file-table.md) se encuentran en un disco de origen determinado.</span><span class="sxs-lookup"><span data-stu-id="fd520-140">The numbers in the LastSequence column specify which of the files in the [File](file-table.md) table are found on a particular source disk.</span></span> <span data-ttu-id="fd520-141">Cada disco de origen contiene todos los archivos con números de secuencia (como se muestra en la columna secuencia de la tabla de archivos) menores o iguales que el valor de la columna LastSequence, y mayor que el valor LastSequence del disco anterior (o mayor que 0, para la primera entrada de la tabla de medios).</span><span class="sxs-lookup"><span data-stu-id="fd520-141">Each source disk contains all files with sequence numbers (as shown in the Sequence column of the File table) less than or equal to the value in the LastSequence column, and greater than the LastSequence value of the previous disk (or greater than 0, for the first entry in the Media table).</span></span> <span data-ttu-id="fd520-142">Este número no debe ser negativo; el límite máximo es de 32767 archivos.</span><span class="sxs-lookup"><span data-stu-id="fd520-142">This number must be non-negative; the maximum limit is 32767 files.</span></span> <span data-ttu-id="fd520-143">Para obtener más información sobre cómo crear un paquete de Windows Installer con más archivos, vea [crear un paquete de gran tamaño](authoring-a-large-package.md).</span><span class="sxs-lookup"><span data-stu-id="fd520-143">For more information about creating a Windows Installer package with more files, see [Authoring a Large Package](authoring-a-large-package.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd520-144"><span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="fd520-144"><span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>DiskPrompt</span></span>
</dt> <dd>

<span data-ttu-id="fd520-145">El nombre del disco, que suele ser el texto visible impreso en el disco.</span><span class="sxs-lookup"><span data-stu-id="fd520-145">The disk name, which is usually the visible text printed on the disk.</span></span> <span data-ttu-id="fd520-146">Este texto traducible se usa para preguntar al usuario cuando es necesario insertar este disco.</span><span class="sxs-lookup"><span data-stu-id="fd520-146">This localizable text is used to prompt the user when this disk needs to be inserted.</span></span>

</dd> <dt>

<span data-ttu-id="fd520-147"><span id="Cabinet"></span><span id="cabinet"></span><span id="CABINET"></span>Archiva</span><span class="sxs-lookup"><span data-stu-id="fd520-147"><span id="Cabinet"></span><span id="cabinet"></span><span id="CABINET"></span>Cabinet</span></span>
</dt> <dd>

<span data-ttu-id="fd520-148">El nombre del archivo. cab si algunos o todos los archivos almacenados en el medio se comprimen en un archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="fd520-148">The name of the cabinet if some or all of the files stored on the media are compressed into a cabinet file.</span></span> <span data-ttu-id="fd520-149">Si no se usan contenedores, esta columna debe estar en blanco.</span><span class="sxs-lookup"><span data-stu-id="fd520-149">If no cabinets are used, this column must be blank.</span></span> <span data-ttu-id="fd520-150">El nombre del archivo. cab debe utilizar la sintaxis del tipo de datos del [archivo. cab](cabinet.md) .</span><span class="sxs-lookup"><span data-stu-id="fd520-150">The name of the cabinet must use the syntax of the [Cabinet](cabinet.md) data type.</span></span> <span data-ttu-id="fd520-151">Windows Installer requiere siempre un origen válido para reparar los archivos incluidos en los archivos. cab insertados.</span><span class="sxs-lookup"><span data-stu-id="fd520-151">Windows Installer always requires a valid source to repair files included in embedded cabinet files.</span></span> <span data-ttu-id="fd520-152">Cuando Windows Installer instala un paquete que contiene un archivo. cab incrustado, el sistema puede guardar una copia del archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="fd520-152">When Windows Installer installs a package containing an embedded cabinet file, a copy of the cabinet file can be saved by the system.</span></span> <span data-ttu-id="fd520-153">Esta copia no se puede usar para reparar el archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="fd520-153">This copy cannot be used to repair the cabinet file.</span></span> <span data-ttu-id="fd520-154">Para conservar espacio en disco, use archivos. cab externos en lugar de archivos. cab incrustados.</span><span class="sxs-lookup"><span data-stu-id="fd520-154">To conserve disk space, use external cabinet files instead of embedded cabinet files.</span></span>

</dd> <dt>

<span data-ttu-id="fd520-155"><span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="fd520-155"><span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel</span></span>
</dt> <dd>

<span data-ttu-id="fd520-156">Etiqueta atribuida al volumen.</span><span class="sxs-lookup"><span data-stu-id="fd520-156">The label attributed to the volume.</span></span> <span data-ttu-id="fd520-157">Esta es la etiqueta de volumen devuelta por la función [**GetVolumeInformation**](/windows/win32/api/fileapi/nf-fileapi-getvolumeinformationa) .</span><span class="sxs-lookup"><span data-stu-id="fd520-157">This is the volume label returned by the [**GetVolumeInformation**](/windows/win32/api/fileapi/nf-fileapi-getvolumeinformationa) function.</span></span> <span data-ttu-id="fd520-158">Si la propiedad [**SourceDir**](sourcedir.md) hace referencia a un volumen extraíble (disquete o CD-ROM), esta etiqueta de volumen se usa para comprobar que el disco adecuado se encuentra en la unidad antes de intentar instalar archivos.</span><span class="sxs-lookup"><span data-stu-id="fd520-158">If the [**SourceDir**](sourcedir.md) property refers to a removable (floppy or CD-ROM) volume, then this volume label is used to verify that the proper disk is in the drive before attempting to install files.</span></span> <span data-ttu-id="fd520-159">La entrada de esta columna debe coincidir con la etiqueta de volumen del medio físico.</span><span class="sxs-lookup"><span data-stu-id="fd520-159">The entry in this column must match the volume label of the physical media.</span></span>

</dd> <dt>

<span data-ttu-id="fd520-160"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Fuentes</span><span class="sxs-lookup"><span data-stu-id="fd520-160"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Source</span></span>
</dt> <dd>

<span data-ttu-id="fd520-161">Este campo solo se usa en la revisión y, de lo contrario, se deja en blanco.</span><span class="sxs-lookup"><span data-stu-id="fd520-161">This field is only used by patching and is otherwise left blank.</span></span> <span data-ttu-id="fd520-162">Una transformación de revisión puede escribir aquí una propiedad que es la ubicación del archivo. cab que contiene los archivos de revisión o los nuevos archivos agregados por la revisión.</span><span class="sxs-lookup"><span data-stu-id="fd520-162">A patch transform can enter a property here that is the location of the cabinet file containing the patch files or any new files added by the patch.</span></span> <span data-ttu-id="fd520-163">Se debe especificar un origen diferente para estos archivos porque el origen del paquete de revisión se puede almacenar por separado del origen del producto.</span><span class="sxs-lookup"><span data-stu-id="fd520-163">A different source needs to be specified for these files because the source of the patch package can be stored separately from the product's source.</span></span> <span data-ttu-id="fd520-164">Si el campo del archivo. cab está vacío, el instalador omite el valor de esta columna.</span><span class="sxs-lookup"><span data-stu-id="fd520-164">If the Cabinet field is empty, the installer ignores the value in this column.</span></span> <span data-ttu-id="fd520-165">Si este campo está vacío, el instalador usa el valor de la propiedad [**SourceDir**](sourcedir.md) como origen del archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="fd520-165">If this field is empty, the installer uses the value of the [**SourceDir**](sourcedir.md) property as the source of the cabinet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd520-166">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd520-166">Remarks</span></span>

<span data-ttu-id="fd520-167">Si el nombre del archivo. cab está precedido por un signo de número ( \# ), los archivos que hacen referencia a este registro de tabla multimedia se empaquetan en un archivo. cab que se almacena en la base de datos como una secuencia independiente.</span><span class="sxs-lookup"><span data-stu-id="fd520-167">If the cabinet name is preceded by a number sign (\#), then the files referencing this Media table record are packed in a cabinet file that is stored within the database as a separate stream.</span></span>

<span data-ttu-id="fd520-168">Para obtener más información sobre cómo agregar archivadores a las tablas de archivos y las tablas de medios, consulte [uso de archivadores y orígenes comprimidos](using-cabinets-and-compressed-sources.md).</span><span class="sxs-lookup"><span data-stu-id="fd520-168">For more information about how to add cabinets to the File tables and Media tables, see [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).</span></span>

<span data-ttu-id="fd520-169">Windows Installer requiere que el archivo. msi esté en el primer disco de medios extraíbles (CD, DVD o disquete) usado para la instalación del producto.</span><span class="sxs-lookup"><span data-stu-id="fd520-169">Windows Installer requires that the .msi file be on the first disk of removable media (CD, DVD or floppy) used for the product's installation.</span></span>

<span data-ttu-id="fd520-170">**Determinar el SourceMode**</span><span class="sxs-lookup"><span data-stu-id="fd520-170">**Determining the SourceMode**</span></span>

<span data-ttu-id="fd520-171">La propiedad de [**Resumen de recuento de palabras**](word-count-summary.md) determina el modo de origen de la instalación actual.</span><span class="sxs-lookup"><span data-stu-id="fd520-171">The [**Word Count Summary**](word-count-summary.md) property determines the source mode for the current install.</span></span> <span data-ttu-id="fd520-172">Si esta propiedad se establece en 2 o 3, se supone la instalación de un archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="fd520-172">If this property is set to 2 or 3, a cabinet install is assumed.</span></span> <span data-ttu-id="fd520-173">En este modo, se supone que los archivos. cab existen en el directorio indicado por la propiedad [**SourceDir**](sourcedir.md) .</span><span class="sxs-lookup"><span data-stu-id="fd520-173">In this mode, the cabinet files are assumed to exist in the directory indicated by the [**SourceDir**](sourcedir.md) property.</span></span> <span data-ttu-id="fd520-174">Si el valor de tipo de origen es 0 o 1, se supone que todos los archivos de código fuente existen en el árbol cuya raíz se indica mediante la propiedad **SourceDir** .</span><span class="sxs-lookup"><span data-stu-id="fd520-174">If the Source Type value is 0 or 1, all source files are assumed to exist in the tree whose root is indicated by the **SourceDir** property.</span></span>

<span data-ttu-id="fd520-175">Tenga en cuenta que esto solo se aplica a los archivos de la tabla de archivos que no tienen los bits comprimidos o sin comprimir establecidos en la columna atributos.</span><span class="sxs-lookup"><span data-stu-id="fd520-175">Note that this only applies to files in the File table that do not have either the Compressed or Uncompressed bits set in the attributes column.</span></span> <span data-ttu-id="fd520-176">Estos bits invalidan el valor de la propiedad de [**Resumen de recuento de palabras**](word-count-summary.md) al determinar si un archivo determinado está comprimido o descomprimido.</span><span class="sxs-lookup"><span data-stu-id="fd520-176">These bits override the value of the [**Word Count Summary**](word-count-summary.md) property when determining if a particular file is compressed or uncompressed.</span></span>

## <a name="validation"></a><span data-ttu-id="fd520-177">Validación</span><span class="sxs-lookup"><span data-stu-id="fd520-177">Validation</span></span>

<dl>

[<span data-ttu-id="fd520-178">ICE03</span><span class="sxs-lookup"><span data-stu-id="fd520-178">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="fd520-179">ICE04</span><span class="sxs-lookup"><span data-stu-id="fd520-179">ICE04</span></span>](ice04.md)  
[<span data-ttu-id="fd520-180">ICE06</span><span class="sxs-lookup"><span data-stu-id="fd520-180">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="fd520-181">ICE35</span><span class="sxs-lookup"><span data-stu-id="fd520-181">ICE35</span></span>](ice35.md)  
[<span data-ttu-id="fd520-182">ICE58</span><span class="sxs-lookup"><span data-stu-id="fd520-182">ICE58</span></span>](ice58.md)  
[<span data-ttu-id="fd520-183">ICE71</span><span class="sxs-lookup"><span data-stu-id="fd520-183">ICE71</span></span>](ice71.md)  
[<span data-ttu-id="fd520-184">ICE81</span><span class="sxs-lookup"><span data-stu-id="fd520-184">ICE81</span></span>](ice81.md)  
</dl>

 

 
