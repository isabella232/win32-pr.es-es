---
description: La tabla Font contiene la información para registrar archivos de fuentes con el sistema.
ms.assetid: 5ddff430-a6f8-473b-8006-ac0124469a99
title: Tabla de fuentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10208c7b9a14ca7f311aff71653a53a3da9ed0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002269"
---
# <a name="font-table"></a><span data-ttu-id="56f44-103">Tabla de fuentes</span><span class="sxs-lookup"><span data-stu-id="56f44-103">Font Table</span></span>

<span data-ttu-id="56f44-104">La tabla Font contiene la información para registrar archivos de fuentes con el sistema.</span><span class="sxs-lookup"><span data-stu-id="56f44-104">The Font table contains the information for registering font files with the system.</span></span>

<span data-ttu-id="56f44-105">La tabla de fuentes tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="56f44-105">The Font table has the following columns.</span></span>



| <span data-ttu-id="56f44-106">Columna</span><span class="sxs-lookup"><span data-stu-id="56f44-106">Column</span></span>    | <span data-ttu-id="56f44-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="56f44-107">Type</span></span>                         | <span data-ttu-id="56f44-108">Clave</span><span class="sxs-lookup"><span data-stu-id="56f44-108">Key</span></span> | <span data-ttu-id="56f44-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="56f44-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="56f44-110">Archivo\_</span><span class="sxs-lookup"><span data-stu-id="56f44-110">File\_</span></span>    | [<span data-ttu-id="56f44-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="56f44-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="56f44-112">Y</span><span class="sxs-lookup"><span data-stu-id="56f44-112">Y</span></span>   | <span data-ttu-id="56f44-113">N</span><span class="sxs-lookup"><span data-stu-id="56f44-113">N</span></span>        |
| <span data-ttu-id="56f44-114">FontTitle</span><span class="sxs-lookup"><span data-stu-id="56f44-114">FontTitle</span></span> | [<span data-ttu-id="56f44-115">Texto</span><span class="sxs-lookup"><span data-stu-id="56f44-115">Text</span></span>](text.md)             | <span data-ttu-id="56f44-116">N</span><span class="sxs-lookup"><span data-stu-id="56f44-116">N</span></span>   | <span data-ttu-id="56f44-117">Y</span><span class="sxs-lookup"><span data-stu-id="56f44-117">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="56f44-118">Columnas</span><span class="sxs-lookup"><span data-stu-id="56f44-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="56f44-119"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Filesystem\_</span><span class="sxs-lookup"><span data-stu-id="56f44-119"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="56f44-120">Clave externa en la entrada de la [tabla de archivos](file-table.md) para el archivo de fuente.</span><span class="sxs-lookup"><span data-stu-id="56f44-120">External key into the [File table](file-table.md) entry for the font file.</span></span> <span data-ttu-id="56f44-121">Se recomienda que el componente que contiene el archivo de fuente tenga el valor de FontsFolder especificado en la \_ columna directorio de la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="56f44-121">It is recommended that the component containing the font file have the FontsFolder specified in the Directory\_ column of the [Component table](component-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="56f44-122"><span id="FontTitle"></span><span id="fonttitle"></span><span id="FONTTITLE"></span>FontTitle</span><span class="sxs-lookup"><span data-stu-id="56f44-122"><span id="FontTitle"></span><span id="fonttitle"></span><span id="FONTTITLE"></span>FontTitle</span></span>
</dt> <dd>

<span data-ttu-id="56f44-123">Nombre de la fuente.</span><span class="sxs-lookup"><span data-stu-id="56f44-123">Font name.</span></span> <span data-ttu-id="56f44-124">Se recomienda dejar esta columna null para las fuentes TrueType y las colecciones TrueType porque el instalador puede registrar la fuente después de leer el título de fuente correcto del archivo de fuente.</span><span class="sxs-lookup"><span data-stu-id="56f44-124">It is recommended that you leave this column null for TrueType Fonts and TrueType Collections because the installer can register the font after reading the correct font title from the font file.</span></span> <span data-ttu-id="56f44-125">Si se escribe el nombre de la fuente, debe ser idéntico al título de fuente del archivo de fuente.</span><span class="sxs-lookup"><span data-stu-id="56f44-125">If the font name is entered, it must be identical to font title from the font file.</span></span> <span data-ttu-id="56f44-126">Debe especificar un título para las fuentes que no tengan nombres incrustados, como los archivos. fon.</span><span class="sxs-lookup"><span data-stu-id="56f44-126">You must specify a title for fonts that do not have embedded names, such as .fon files.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56f44-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56f44-127">Remarks</span></span>

<span data-ttu-id="56f44-128">Se hace referencia a esta tabla cuando se ejecuta la acción [RegisterFonts](registerfonts-action.md) o la [acción UnregisterFonts](unregisterfonts-action.md) .</span><span class="sxs-lookup"><span data-stu-id="56f44-128">This table is referred to when the [RegisterFonts action](registerfonts-action.md) or the [UnregisterFonts action](unregisterfonts-action.md) is executed.</span></span>

<span data-ttu-id="56f44-129">Si el campo FontTitle es null, el nombre de la fuente se lee directamente desde el archivo de fuente especificado.</span><span class="sxs-lookup"><span data-stu-id="56f44-129">If the FontTitle field is left Null, the Font name is read directly from the font file specified.</span></span> <span data-ttu-id="56f44-130">Si el nombre de fuente grabado en el campo FontTitle difiere del nombre de fuente interno registrado en el archivo de fuente, la fuente se registra dos veces en la [acción RegisterFonts](registerfonts-action.md).</span><span class="sxs-lookup"><span data-stu-id="56f44-130">If the font name recorded into the FontTitle field differs from the internal font name recorded in the font file, the font is registered twice by the [RegisterFonts action](registerfonts-action.md).</span></span>

<span data-ttu-id="56f44-131">Los archivos de fuentes no deben crearse con un identificador de idioma, ya que las fuentes no tienen un recurso de identificador de idioma incrustado. Por lo tanto, la columna de idioma de la [tabla de archivos](file-table.md) debe dejarse como null para los archivos de fuentes.</span><span class="sxs-lookup"><span data-stu-id="56f44-131">Font files should not be authored with a language ID, as fonts do not have an embedded language ID resource.Thus the Language column of the [File table](file-table.md) should be left null for font files.</span></span>

<span data-ttu-id="56f44-132">Dado que el instalador no rerefcount los archivos de fuentes de forma predeterminada, los archivos de fuentes preexistentes se pueden quitar con su componente al desinstalar una aplicación.</span><span class="sxs-lookup"><span data-stu-id="56f44-132">Because the installer does not refcount font files by default, preexisting font files may be removed with their component when uninstalling an application.</span></span> <span data-ttu-id="56f44-133">Para asegurarse de que no se quita un archivo de fuente, los autores pueden establecer las marcas de bits **msidbComponentAttributesSharedDllRefCount** o **msidbComponentAttributesPermanent** en la columna Attributes de la tabla componente MSI del componente de tabla del componente \_ \_ \_ que contiene el archivo de fuente.</span><span class="sxs-lookup"><span data-stu-id="56f44-133">To ensure that a font file is not removed, authors may set the **msidbComponentAttributesSharedDllRefCount** or **msidbComponentAttributesPermanent** bit flags in the Attributes column of the Component Table\_msi\_Component\_Table for the component containing the font file.</span></span>

## <a name="validation"></a><span data-ttu-id="56f44-134">Validación</span><span class="sxs-lookup"><span data-stu-id="56f44-134">Validation</span></span>

<dl>

[<span data-ttu-id="56f44-135">ICE03</span><span class="sxs-lookup"><span data-stu-id="56f44-135">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="56f44-136">ICE06</span><span class="sxs-lookup"><span data-stu-id="56f44-136">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="56f44-137">ICE07</span><span class="sxs-lookup"><span data-stu-id="56f44-137">ICE07</span></span>](ice07.md)  
[<span data-ttu-id="56f44-138">ICE32</span><span class="sxs-lookup"><span data-stu-id="56f44-138">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="56f44-139">ICE51</span><span class="sxs-lookup"><span data-stu-id="56f44-139">ICE51</span></span>](ice51.md)  
[<span data-ttu-id="56f44-140">ICE60</span><span class="sxs-lookup"><span data-stu-id="56f44-140">ICE60</span></span>](ice60.md)  
</dl>

 

 



