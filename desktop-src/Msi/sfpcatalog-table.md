---
description: La tabla SFPCatalog contiene los catálogos que usa Windows me.
ms.assetid: e9dc65a9-4ec9-4310-b03a-a2c38720ca8c
title: Tabla SFPCatalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fe887644faf6cf0a5cda626bbf757e9f448ef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275664"
---
# <a name="sfpcatalog-table"></a><span data-ttu-id="4fc7f-103">Tabla SFPCatalog</span><span class="sxs-lookup"><span data-stu-id="4fc7f-103">SFPCatalog Table</span></span>

<span data-ttu-id="4fc7f-104">La tabla SFPCatalog contiene los catálogos que usa Windows me.</span><span class="sxs-lookup"><span data-stu-id="4fc7f-104">The SFPCatalog table contains the catalogs used by Windows Me.</span></span>

<span data-ttu-id="4fc7f-105">La tabla SFPCatalog tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="4fc7f-105">The SFPCatalog table has the following columns.</span></span>



| <span data-ttu-id="4fc7f-106">Columna</span><span class="sxs-lookup"><span data-stu-id="4fc7f-106">Column</span></span>     | <span data-ttu-id="4fc7f-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="4fc7f-107">Type</span></span>                       | <span data-ttu-id="4fc7f-108">Clave</span><span class="sxs-lookup"><span data-stu-id="4fc7f-108">Key</span></span> | <span data-ttu-id="4fc7f-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="4fc7f-109">Nullable</span></span> |
|------------|----------------------------|-----|----------|
| <span data-ttu-id="4fc7f-110">SFPCatalog</span><span class="sxs-lookup"><span data-stu-id="4fc7f-110">SFPCatalog</span></span> | [<span data-ttu-id="4fc7f-111">Nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="4fc7f-111">Filename</span></span>](filename.md)   | <span data-ttu-id="4fc7f-112">Y</span><span class="sxs-lookup"><span data-stu-id="4fc7f-112">Y</span></span>   | <span data-ttu-id="4fc7f-113">N</span><span class="sxs-lookup"><span data-stu-id="4fc7f-113">N</span></span>        |
| <span data-ttu-id="4fc7f-114">Catálogo</span><span class="sxs-lookup"><span data-stu-id="4fc7f-114">Catalog</span></span>    | [<span data-ttu-id="4fc7f-115">Binario</span><span class="sxs-lookup"><span data-stu-id="4fc7f-115">Binary</span></span>](binary.md)       | <span data-ttu-id="4fc7f-116">N</span><span class="sxs-lookup"><span data-stu-id="4fc7f-116">N</span></span>   | <span data-ttu-id="4fc7f-117">N</span><span class="sxs-lookup"><span data-stu-id="4fc7f-117">N</span></span>        |
| <span data-ttu-id="4fc7f-118">Dependencia</span><span class="sxs-lookup"><span data-stu-id="4fc7f-118">Dependency</span></span> | [<span data-ttu-id="4fc7f-119">Formatea</span><span class="sxs-lookup"><span data-stu-id="4fc7f-119">Formatted</span></span>](formatted.md) | <span data-ttu-id="4fc7f-120">N</span><span class="sxs-lookup"><span data-stu-id="4fc7f-120">N</span></span>   | <span data-ttu-id="4fc7f-121">Y</span><span class="sxs-lookup"><span data-stu-id="4fc7f-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="4fc7f-122">Columnas</span><span class="sxs-lookup"><span data-stu-id="4fc7f-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="4fc7f-123"><span id="SFPCatalog"></span><span id="sfpcatalog"></span><span id="SFPCATALOG"></span>SFPCatalog</span><span class="sxs-lookup"><span data-stu-id="4fc7f-123"><span id="SFPCatalog"></span><span id="sfpcatalog"></span><span id="SFPCATALOG"></span>SFPCatalog</span></span>
</dt> <dd>

<span data-ttu-id="4fc7f-124">Nombre corto de archivo para el catálogo.</span><span class="sxs-lookup"><span data-stu-id="4fc7f-124">The short file name for the catalog.</span></span> <span data-ttu-id="4fc7f-125">Dado que los catálogos no tienen ninguna versión, el catálogo especificado en esta columna puede sobrescribir un catálogo que tenga el mismo nombre y ya esté instalado en el sistema local.</span><span class="sxs-lookup"><span data-stu-id="4fc7f-125">Because catalogs have no version, the catalog specified in this column can overwrite a catalog that has the same name and is already installed on the local system.</span></span> <span data-ttu-id="4fc7f-126">Vea el tema sobre el control de versiones de archivos. el [archivo tiene una versión](neither-file-has-a-version.md).</span><span class="sxs-lookup"><span data-stu-id="4fc7f-126">See the file versioning topic [Neither File Has a Version](neither-file-has-a-version.md).</span></span>

</dd> <dt>

<span data-ttu-id="4fc7f-127"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catálogo</span><span class="sxs-lookup"><span data-stu-id="4fc7f-127"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span>
</dt> <dd>

<span data-ttu-id="4fc7f-128">Datos binarios para el catálogo.</span><span class="sxs-lookup"><span data-stu-id="4fc7f-128">Binary data for the catalog.</span></span>

</dd> <dt>

<span data-ttu-id="4fc7f-129"><span id="Dependency"></span><span id="dependency"></span><span id="DEPENDENCY"></span>Pendiente</span><span class="sxs-lookup"><span data-stu-id="4fc7f-129"><span id="Dependency"></span><span id="dependency"></span><span id="DEPENDENCY"></span>Dependency</span></span>
</dt> <dd>

<span data-ttu-id="4fc7f-130">El catálogo especificado en este campo es el elemento primario del catálogo dependiente especificado en el campo SFPCatalog.</span><span class="sxs-lookup"><span data-stu-id="4fc7f-130">The catalog specified in this field is the parent of the dependent catalog specified in the SFPCatalog field.</span></span> <span data-ttu-id="4fc7f-131">Escriba el nombre corto de archivo del catálogo primario en el campo dependencia.</span><span class="sxs-lookup"><span data-stu-id="4fc7f-131">Enter the short file name of the parent catalog into the Dependency field.</span></span> <span data-ttu-id="4fc7f-132">Este campo es una clave de vuelta a la columna SFPCatalog.</span><span class="sxs-lookup"><span data-stu-id="4fc7f-132">This field is a key back into the SFPCatalog column.</span></span> <span data-ttu-id="4fc7f-133">La coincidencia de dependencia distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4fc7f-133">The dependency match is case sensitive.</span></span>

<span data-ttu-id="4fc7f-134">Si el campo de dependencia hace referencia a otro registro de esta tabla SFPCatalog, el catálogo primario se instala antes que el catálogo dependiente.</span><span class="sxs-lookup"><span data-stu-id="4fc7f-134">If the Dependency field references another record in this SFPCatalog table, the parent catalog is installed before the dependent catalog.</span></span>

<span data-ttu-id="4fc7f-135">Si el campo de dependencia hace referencia a un catálogo primario que no está presente en el campo SFPCatalog de esta tabla y si el catálogo primario no está ya instalado, se produce un error en la instalación.</span><span class="sxs-lookup"><span data-stu-id="4fc7f-135">If the Dependency field references a parent catalog that is not present in the SFPCatalog field of this table, and if the parent catalog is not already installed, the installation fails.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4fc7f-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4fc7f-136">Remarks</span></span>

<span data-ttu-id="4fc7f-137">La [acción InstallSFPCatalogFile](installsfpcatalogfile-action.md) consulta la tabla de [componentes](component-table.md), la tabla de [archivos](file-table.md), la tabla [FileSFPCatalog](filesfpcatalog-table.md) y la tabla SFPCatalog.</span><span class="sxs-lookup"><span data-stu-id="4fc7f-137">The [InstallSFPCatalogFile action](installsfpcatalogfile-action.md) queries the [Component table](component-table.md), [File table](file-table.md), [FileSFPCatalog table](filesfpcatalog-table.md) and SFPCatalog table.</span></span>

## <a name="validation"></a><span data-ttu-id="4fc7f-138">Validación</span><span class="sxs-lookup"><span data-stu-id="4fc7f-138">Validation</span></span>

<dl>

[<span data-ttu-id="4fc7f-139">ICE03</span><span class="sxs-lookup"><span data-stu-id="4fc7f-139">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="4fc7f-140">ICE06</span><span class="sxs-lookup"><span data-stu-id="4fc7f-140">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="4fc7f-141">ICE29</span><span class="sxs-lookup"><span data-stu-id="4fc7f-141">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="4fc7f-142">ICE32</span><span class="sxs-lookup"><span data-stu-id="4fc7f-142">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="4fc7f-143">ICE46</span><span class="sxs-lookup"><span data-stu-id="4fc7f-143">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="4fc7f-144">ICE66</span><span class="sxs-lookup"><span data-stu-id="4fc7f-144">ICE66</span></span>](ice66.md)  
</dl>

 

 



