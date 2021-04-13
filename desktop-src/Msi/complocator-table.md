---
description: La tabla CompLocator contiene la información necesaria para buscar un archivo o un directorio que use los datos de configuración del instalador.
ms.assetid: 8b527307-51bf-47b3-a0b2-3421cc5278b7
title: Tabla CompLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9fcb4a3c4f2e2c6f3ca3c92f6dc7466326bd11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547011"
---
# <a name="complocator-table"></a><span data-ttu-id="e994a-103">Tabla CompLocator</span><span class="sxs-lookup"><span data-stu-id="e994a-103">CompLocator Table</span></span>

<span data-ttu-id="e994a-104">La tabla CompLocator contiene la información necesaria para buscar un archivo o un directorio que use los datos de configuración del instalador.</span><span class="sxs-lookup"><span data-stu-id="e994a-104">The CompLocator Table contains the information needed to find a file or directory that is using the installer configuration data.</span></span>

<span data-ttu-id="e994a-105">La tabla CompLocator contiene la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="e994a-105">The CompLocator table contains the following information.</span></span>



| <span data-ttu-id="e994a-106">Columna</span><span class="sxs-lookup"><span data-stu-id="e994a-106">Column</span></span>      | <span data-ttu-id="e994a-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="e994a-107">Type</span></span>                         | <span data-ttu-id="e994a-108">Clave</span><span class="sxs-lookup"><span data-stu-id="e994a-108">Key</span></span> | <span data-ttu-id="e994a-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="e994a-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="e994a-110">Signatura\_</span><span class="sxs-lookup"><span data-stu-id="e994a-110">Signature\_</span></span> | [<span data-ttu-id="e994a-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="e994a-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="e994a-112">Y</span><span class="sxs-lookup"><span data-stu-id="e994a-112">Y</span></span>   | <span data-ttu-id="e994a-113">N</span><span class="sxs-lookup"><span data-stu-id="e994a-113">N</span></span>        |
| <span data-ttu-id="e994a-114">ComponentId</span><span class="sxs-lookup"><span data-stu-id="e994a-114">ComponentId</span></span> | [<span data-ttu-id="e994a-115">GUID</span><span class="sxs-lookup"><span data-stu-id="e994a-115">GUID</span></span>](guid.md)             | <span data-ttu-id="e994a-116">N</span><span class="sxs-lookup"><span data-stu-id="e994a-116">N</span></span>   | <span data-ttu-id="e994a-117">N</span><span class="sxs-lookup"><span data-stu-id="e994a-117">N</span></span>        |
| <span data-ttu-id="e994a-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="e994a-118">Type</span></span>        | [<span data-ttu-id="e994a-119">Entero</span><span class="sxs-lookup"><span data-stu-id="e994a-119">Integer</span></span>](integer.md)       | <span data-ttu-id="e994a-120">N</span><span class="sxs-lookup"><span data-stu-id="e994a-120">N</span></span>   | <span data-ttu-id="e994a-121">Y</span><span class="sxs-lookup"><span data-stu-id="e994a-121">Y</span></span>        |



 

## <a name="column-information"></a><span data-ttu-id="e994a-122">Información de columna</span><span class="sxs-lookup"><span data-stu-id="e994a-122">Column Information</span></span>

<dl> <dt>

<span data-ttu-id="e994a-123"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signatura\_</span><span class="sxs-lookup"><span data-stu-id="e994a-123"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="e994a-124">Esta columna representa una firma de archivo única y también es la clave externa en la [tabla de firmas](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="e994a-124">This column represents a unique file signature and is also the external key into the [Signature Table](signature-table.md).</span></span> <span data-ttu-id="e994a-125">Si la clave no está presente en la tabla de firmas, se supone que se trata de la presencia de un directorio señalado por la tabla CompLocator.</span><span class="sxs-lookup"><span data-stu-id="e994a-125">If the key is absent from the Signature Table, the search is assumed to be for the presence of a directory pointed to by the CompLocator Table.</span></span>

</dd> <dt>

<span data-ttu-id="e994a-126"><span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId</span><span class="sxs-lookup"><span data-stu-id="e994a-126"><span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId</span></span>
</dt> <dd>

<span data-ttu-id="e994a-127">IDENTIFICADOR de componente del componente cuya ruta de acceso de clave se va a usar para la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="e994a-127">The component ID of the component whose key path is to be used for the search.</span></span> <span data-ttu-id="e994a-128">Debe ser el GUID de un componente que aparece en el campo ComponentId de la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="e994a-128">This should be the GUID of a component that appears in the ComponentId field of the [Component Table](component-table.md).</span></span> <span data-ttu-id="e994a-129">Puede ser el identificador de componente de un componente que pertenece a otro producto instalado en el equipo.</span><span class="sxs-lookup"><span data-stu-id="e994a-129">It may be the component ID of a component belonging to another product installed on the computer.</span></span> <span data-ttu-id="e994a-130">No debe ser el GUID de un componente publicado que aparece en el campo ComponentId de la [tabla PublishComponent](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="e994a-130">It should not be the GUID of a published component appearing in the ComponentId field of the [PublishComponent Table](publishcomponent-table.md).</span></span>

<span data-ttu-id="e994a-131">Para buscar el valor GUID del identificador de componente para un archivo instalado por otro producto, vaya al paquete de instalación del producto.</span><span class="sxs-lookup"><span data-stu-id="e994a-131">To find the component ID GUID value for a file installed by another product, go to the installation package of the product.</span></span> <span data-ttu-id="e994a-132">Vaya a la [tabla de archivos](file-table.md) y busque la fila que contiene el identificador de archivo del archivo.</span><span class="sxs-lookup"><span data-stu-id="e994a-132">Go to the [File Table](file-table.md) and find the row that contains the file identifier for the file.</span></span> <span data-ttu-id="e994a-133">La \_ columna componente de esta fila contiene el identificador de componente del componente que controla el archivo.</span><span class="sxs-lookup"><span data-stu-id="e994a-133">The Component\_ column of this row contains the component identifier for the component that controls the file.</span></span> <span data-ttu-id="e994a-134">Vaya a la [tabla de componentes](component-table.md) y busque la fila que contiene este identificador de componente en la columna componente.</span><span class="sxs-lookup"><span data-stu-id="e994a-134">Go to the [Component table](component-table.md) and find the row that contains this component identifier in the Component column.</span></span> <span data-ttu-id="e994a-135">La columna ComponentId de esta fila contiene el GUID del identificador del componente.</span><span class="sxs-lookup"><span data-stu-id="e994a-135">The ComponentId column of this row contains the component ID GUID.</span></span>

</dd> <dt>

<span data-ttu-id="e994a-136"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Automáticamente</span><span class="sxs-lookup"><span data-stu-id="e994a-136"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="e994a-137">Valor booleano que determina si la ruta de acceso de la clave del componente es un nombre de archivo o una ubicación de directorio.</span><span class="sxs-lookup"><span data-stu-id="e994a-137">A Boolean value that determines if the key path of the component is a file name or a directory location.</span></span>

<span data-ttu-id="e994a-138">En la tabla siguiente se enumeran los valores válidos.</span><span class="sxs-lookup"><span data-stu-id="e994a-138">The following table lists valid values.</span></span> <span data-ttu-id="e994a-139">Si no está presente, el tipo se establece en 1 (uno).</span><span class="sxs-lookup"><span data-stu-id="e994a-139">If absent, Type is set to be 1 (one).</span></span>



| <span data-ttu-id="e994a-140">Constante</span><span class="sxs-lookup"><span data-stu-id="e994a-140">Constant</span></span>                      | <span data-ttu-id="e994a-141">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="e994a-141">Hexadecimal</span></span> | <span data-ttu-id="e994a-142">Decimal</span><span class="sxs-lookup"><span data-stu-id="e994a-142">Decimal</span></span> | <span data-ttu-id="e994a-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="e994a-143">Description</span></span>              |
|-------------------------------|-------------|---------|--------------------------|
| <span data-ttu-id="e994a-144">**msidbLocatorTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="e994a-144">**msidbLocatorTypeDirectory**</span></span> | <span data-ttu-id="e994a-145">0x000</span><span class="sxs-lookup"><span data-stu-id="e994a-145">0x000</span></span>       | <span data-ttu-id="e994a-146">0</span><span class="sxs-lookup"><span data-stu-id="e994a-146">0</span></span>       | <span data-ttu-id="e994a-147">La ruta de acceso de la clave es un directorio.</span><span class="sxs-lookup"><span data-stu-id="e994a-147">Key path is a directory.</span></span> |
| <span data-ttu-id="e994a-148">**msidbLocatorTypeFileName**</span><span class="sxs-lookup"><span data-stu-id="e994a-148">**msidbLocatorTypeFileName**</span></span>  | <span data-ttu-id="e994a-149">0x001</span><span class="sxs-lookup"><span data-stu-id="e994a-149">0x001</span></span>       | <span data-ttu-id="e994a-150">1</span><span class="sxs-lookup"><span data-stu-id="e994a-150">1</span></span>       | <span data-ttu-id="e994a-151">La ruta de acceso de la clave es un nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="e994a-151">Key path is a file name.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e994a-152">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e994a-152">Remarks</span></span>

<span data-ttu-id="e994a-153">Esta tabla se usa con la [tabla AppSearch](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="e994a-153">This table is used with the [AppSearch Table](appsearch-table.md).</span></span>

<span data-ttu-id="e994a-154">Normalmente, las columnas de esta tabla no están localizadas.</span><span class="sxs-lookup"><span data-stu-id="e994a-154">Typically, the columns in this table are not localized.</span></span> <span data-ttu-id="e994a-155">Si un autor decide buscar productos en varios idiomas, puede haber una entrada independiente incluida en la tabla para cada idioma.</span><span class="sxs-lookup"><span data-stu-id="e994a-155">If an author decides to search for products in multiple languages, then there can be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="e994a-156">Para obtener más información, vea [Buscar aplicaciones, archivos, entradas del registro o entradas del archivo. ini existentes](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span><span class="sxs-lookup"><span data-stu-id="e994a-156">For more information, see [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="e994a-157">Validación</span><span class="sxs-lookup"><span data-stu-id="e994a-157">Validation</span></span>

<dl>

[<span data-ttu-id="e994a-158">ICE03</span><span class="sxs-lookup"><span data-stu-id="e994a-158">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="e994a-159">ICE06</span><span class="sxs-lookup"><span data-stu-id="e994a-159">ICE06</span></span>](ice06.md)  
</dl>

 

 



