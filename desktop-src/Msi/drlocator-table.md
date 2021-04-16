---
description: La tabla DrLocator contiene la información necesaria para buscar un archivo o un directorio mediante la búsqueda en el árbol de directorios.
ms.assetid: 2b779ff7-f410-4af0-899d-4432b015d526
title: Tabla DrLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78df5a5af83a18a14027b88033e977b2c63d2027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652467"
---
# <a name="drlocator-table"></a><span data-ttu-id="6a6fa-103">Tabla DrLocator</span><span class="sxs-lookup"><span data-stu-id="6a6fa-103">DrLocator Table</span></span>

<span data-ttu-id="6a6fa-104">La tabla DrLocator contiene la información necesaria para buscar un archivo o un directorio mediante la búsqueda en el árbol de directorios.</span><span class="sxs-lookup"><span data-stu-id="6a6fa-104">The DrLocator table holds the information needed to find a file or directory by searching the directory tree.</span></span>

<span data-ttu-id="6a6fa-105">La tabla DrLocator tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="6a6fa-105">The DrLocator table has the following columns.</span></span>



| <span data-ttu-id="6a6fa-106">Columna</span><span class="sxs-lookup"><span data-stu-id="6a6fa-106">Column</span></span>      | <span data-ttu-id="6a6fa-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="6a6fa-107">Type</span></span>                         | <span data-ttu-id="6a6fa-108">Clave</span><span class="sxs-lookup"><span data-stu-id="6a6fa-108">Key</span></span> | <span data-ttu-id="6a6fa-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="6a6fa-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="6a6fa-110">Signatura\_</span><span class="sxs-lookup"><span data-stu-id="6a6fa-110">Signature\_</span></span> | [<span data-ttu-id="6a6fa-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="6a6fa-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="6a6fa-112">Y</span><span class="sxs-lookup"><span data-stu-id="6a6fa-112">Y</span></span>   | <span data-ttu-id="6a6fa-113">N</span><span class="sxs-lookup"><span data-stu-id="6a6fa-113">N</span></span>        |
| <span data-ttu-id="6a6fa-114">Parent</span><span class="sxs-lookup"><span data-stu-id="6a6fa-114">Parent</span></span>      | [<span data-ttu-id="6a6fa-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="6a6fa-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="6a6fa-116">Y</span><span class="sxs-lookup"><span data-stu-id="6a6fa-116">Y</span></span>   | <span data-ttu-id="6a6fa-117">Y</span><span class="sxs-lookup"><span data-stu-id="6a6fa-117">Y</span></span>        |
| <span data-ttu-id="6a6fa-118">Ruta</span><span class="sxs-lookup"><span data-stu-id="6a6fa-118">Path</span></span>        | [<span data-ttu-id="6a6fa-119">AnyPath</span><span class="sxs-lookup"><span data-stu-id="6a6fa-119">AnyPath</span></span>](anypath.md)       | <span data-ttu-id="6a6fa-120">Y</span><span class="sxs-lookup"><span data-stu-id="6a6fa-120">Y</span></span>   | <span data-ttu-id="6a6fa-121">Y</span><span class="sxs-lookup"><span data-stu-id="6a6fa-121">Y</span></span>        |
| <span data-ttu-id="6a6fa-122">Profundidad</span><span class="sxs-lookup"><span data-stu-id="6a6fa-122">Depth</span></span>       | [<span data-ttu-id="6a6fa-123">Entero</span><span class="sxs-lookup"><span data-stu-id="6a6fa-123">Integer</span></span>](integer.md)       | <span data-ttu-id="6a6fa-124">N</span><span class="sxs-lookup"><span data-stu-id="6a6fa-124">N</span></span>   | <span data-ttu-id="6a6fa-125">Y</span><span class="sxs-lookup"><span data-stu-id="6a6fa-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="6a6fa-126">Columnas</span><span class="sxs-lookup"><span data-stu-id="6a6fa-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="6a6fa-127"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signatura\_</span><span class="sxs-lookup"><span data-stu-id="6a6fa-127"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="6a6fa-128">La \_ columna Signature es una clave externa de la primera columna de la [tabla Signature](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="6a6fa-128">The Signature\_ column is an external key to the first column of the [Signature table](signature-table.md).</span></span> <span data-ttu-id="6a6fa-129">Este campo puede representar una firma de archivo única que aparece en la tabla de signatura.</span><span class="sxs-lookup"><span data-stu-id="6a6fa-129">This field may represent a unique file signature listed in the Signature table.</span></span> <span data-ttu-id="6a6fa-130">Si el valor de esta columna no se encuentra en la tabla de firmas, se supone que la búsqueda es para un directorio al que apunta la tabla DrLocator.</span><span class="sxs-lookup"><span data-stu-id="6a6fa-130">If the value in this column is absent from the Signature table, then the search is assumed to be for a directory pointed to by the DrLocator table.</span></span>

</dd> <dt>

<span data-ttu-id="6a6fa-131"><span id="Parent"></span><span id="parent"></span><span id="PARENT"></span>Aérea</span><span class="sxs-lookup"><span data-stu-id="6a6fa-131"><span id="Parent"></span><span id="parent"></span><span id="PARENT"></span>Parent</span></span>
</dt> <dd>

<span data-ttu-id="6a6fa-132">Esta columna es la firma del directorio principal del archivo o directorio en la \_ columna firma.</span><span class="sxs-lookup"><span data-stu-id="6a6fa-132">This column is the signature of the parent directory of the file or directory in the Signature\_ column.</span></span> <span data-ttu-id="6a6fa-133">Si este campo es NULL y la columna Path no se expande a una ruta de acceso completa, se busca en todas las unidades fijas del sistema del usuario mediante la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="6a6fa-133">If this field is null, and the Path column does not expand to a full path, then all the fixed drives of the user's system are searched by using the Path.</span></span>

<span data-ttu-id="6a6fa-134">Este campo es una clave en una de las tablas siguientes: [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md)o DrLocator.</span><span class="sxs-lookup"><span data-stu-id="6a6fa-134">This field is a key into one of the following tables: the [RegLocator](reglocator-table.md), the [IniLocator](inilocator-table.md), the [CompLocator](complocator-table.md), or the DrLocator tables.</span></span>

</dd> <dt>

<span data-ttu-id="6a6fa-135"><span id="Path"></span><span id="path"></span><span id="PATH"></span>Camino</span><span class="sxs-lookup"><span data-stu-id="6a6fa-135"><span id="Path"></span><span id="path"></span><span id="PATH"></span>Path</span></span>
</dt> <dd>

<span data-ttu-id="6a6fa-136">La columna Path contiene la ruta de acceso en el sistema del usuario.</span><span class="sxs-lookup"><span data-stu-id="6a6fa-136">The Path column contains the path on the user's system.</span></span> <span data-ttu-id="6a6fa-137">Se trata de una ruta de acceso completa o un subtrazado relativo situado debajo del directorio especificado en la columna primaria.</span><span class="sxs-lookup"><span data-stu-id="6a6fa-137">This is a either a full path or a relative subpath below the directory specified in the Parent column.</span></span> <span data-ttu-id="6a6fa-138">Vea las restricciones en el tipo de datos [AnyPath](anypath.md) .</span><span class="sxs-lookup"><span data-stu-id="6a6fa-138">See the restrictions on the [AnyPath](anypath.md) data type.</span></span>

</dd> <dt>

<span data-ttu-id="6a6fa-139"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>Amplia</span><span class="sxs-lookup"><span data-stu-id="6a6fa-139"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>Depth</span></span>
</dt> <dd>

<span data-ttu-id="6a6fa-140">La profundidad por debajo de la ruta de acceso en la que el instalador busca el archivo o directorio especificado en la columna de firma \_ .</span><span class="sxs-lookup"><span data-stu-id="6a6fa-140">The depth below the path that the installer searches for the file or directory specified in the Signature\_ column.</span></span> <span data-ttu-id="6a6fa-141">El valor usado en el campo de profundidad se basa en cero.</span><span class="sxs-lookup"><span data-stu-id="6a6fa-141">The value used in the Depth field is based on zero.</span></span> <span data-ttu-id="6a6fa-142">Por ejemplo, si el campo de ruta de acceso es c:/archivos de programa/bin, la columna de profundidad debe establecerse en 0 o más para detectar un archivo ubicado dentro de la ubicación de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="6a6fa-142">For example, if the Path field is c:/Program Files/bin, the Depth column must be set to 0 or greater, to detect a file located inside the folder bin.</span></span> <span data-ttu-id="6a6fa-143">Si el campo de profundidad está vacío, se supone que la profundidad es cero.</span><span class="sxs-lookup"><span data-stu-id="6a6fa-143">If the Depth field is empty, the depth is assumed to be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a6fa-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a6fa-144">Remarks</span></span>

<span data-ttu-id="6a6fa-145">Esta tabla se usa con la [tabla AppSearch](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="6a6fa-145">This table is used with the [AppSearch Table](appsearch-table.md).</span></span>

<span data-ttu-id="6a6fa-146">Por lo general, las columnas de esta tabla no están localizadas.</span><span class="sxs-lookup"><span data-stu-id="6a6fa-146">This table's columns are generally not localized.</span></span> <span data-ttu-id="6a6fa-147">Si un autor decide buscar productos en varios idiomas, debe haber una entrada independiente incluida en la tabla para cada idioma.</span><span class="sxs-lookup"><span data-stu-id="6a6fa-147">If an author decides to search for products in multiple languages, then there must be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="6a6fa-148">Vea [Buscar aplicaciones, archivos, entradas del registro o entradas del archivo. ini existentes](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span><span class="sxs-lookup"><span data-stu-id="6a6fa-148">See [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="6a6fa-149">Validación</span><span class="sxs-lookup"><span data-stu-id="6a6fa-149">Validation</span></span>

<dl>

[<span data-ttu-id="6a6fa-150">ICE03</span><span class="sxs-lookup"><span data-stu-id="6a6fa-150">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="6a6fa-151">ICE06</span><span class="sxs-lookup"><span data-stu-id="6a6fa-151">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="6a6fa-152">ICE46</span><span class="sxs-lookup"><span data-stu-id="6a6fa-152">ICE46</span></span>](ice46.md)  
</dl>

 

 



