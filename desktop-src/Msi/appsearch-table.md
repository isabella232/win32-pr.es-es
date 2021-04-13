---
description: La tabla AppSearch contiene las propiedades necesarias para buscar un archivo que tenga una firma de archivo determinada. La tabla AppSearch también se puede usar para establecer una propiedad en el valor existente de una entrada del archivo Registry o. ini.
ms.assetid: d560096f-6baa-4fea-8786-f4e3d5ee6bf4
title: Tabla AppSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9419a768a51364b4f22444288e6728a87289aa0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276523"
---
# <a name="appsearch-table"></a><span data-ttu-id="97dc7-104">Tabla AppSearch</span><span class="sxs-lookup"><span data-stu-id="97dc7-104">AppSearch Table</span></span>

<span data-ttu-id="97dc7-105">La tabla AppSearch contiene las propiedades necesarias para buscar un archivo que tenga una firma de archivo determinada.</span><span class="sxs-lookup"><span data-stu-id="97dc7-105">The AppSearch table contains properties needed to search for a file having a particular file signature.</span></span> <span data-ttu-id="97dc7-106">La tabla AppSearch también se puede usar para establecer una propiedad en el valor existente de una entrada del archivo Registry o. ini.</span><span class="sxs-lookup"><span data-stu-id="97dc7-106">The AppSearch table can also be used to set a property to the existing value of a registry or .ini file entry.</span></span>

<span data-ttu-id="97dc7-107">La tabla AppSearch tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="97dc7-107">The AppSearch table has the following columns.</span></span>



| <span data-ttu-id="97dc7-108">Columna</span><span class="sxs-lookup"><span data-stu-id="97dc7-108">Column</span></span>      | <span data-ttu-id="97dc7-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="97dc7-109">Type</span></span>                         | <span data-ttu-id="97dc7-110">Clave</span><span class="sxs-lookup"><span data-stu-id="97dc7-110">Key</span></span> | <span data-ttu-id="97dc7-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="97dc7-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="97dc7-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="97dc7-112">Property</span></span>    | [<span data-ttu-id="97dc7-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="97dc7-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="97dc7-114">Y</span><span class="sxs-lookup"><span data-stu-id="97dc7-114">Y</span></span>   | <span data-ttu-id="97dc7-115">N</span><span class="sxs-lookup"><span data-stu-id="97dc7-115">N</span></span>        |
| <span data-ttu-id="97dc7-116">Signatura\_</span><span class="sxs-lookup"><span data-stu-id="97dc7-116">Signature\_</span></span> | [<span data-ttu-id="97dc7-117">Identificador</span><span class="sxs-lookup"><span data-stu-id="97dc7-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="97dc7-118">Y</span><span class="sxs-lookup"><span data-stu-id="97dc7-118">Y</span></span>   | <span data-ttu-id="97dc7-119">N</span><span class="sxs-lookup"><span data-stu-id="97dc7-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="97dc7-120">Columnas</span><span class="sxs-lookup"><span data-stu-id="97dc7-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="97dc7-121"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propiedad</span><span class="sxs-lookup"><span data-stu-id="97dc7-121"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="97dc7-122">Al ejecutar la acción [AppSearch](appsearch-action.md) se establece esta propiedad en la ubicación del archivo indicado por la \_ columna Signature.</span><span class="sxs-lookup"><span data-stu-id="97dc7-122">Running the [AppSearch](appsearch-action.md) action sets this property to the location of the file indicated by the Signature\_ column.</span></span> <span data-ttu-id="97dc7-123">Esta propiedad se establece si la firma de archivo existe en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="97dc7-123">This property is set if the file signature exists on the user's computer.</span></span> <span data-ttu-id="97dc7-124">Las propiedades utilizadas en esta columna deben ser propiedades [públicas](public-properties.md) y tener un identificador que no contenga ninguna letra minúscula.</span><span class="sxs-lookup"><span data-stu-id="97dc7-124">The properties used in this column must be [public](public-properties.md) properties and have an identifier that contains no lowercase letters.</span></span>

<span data-ttu-id="97dc7-125">La propiedad enumerada en el campo de propiedad se puede inicializar en la tabla de [propiedades](property-table.md) o desde una línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="97dc7-125">The property listed in the Property field may be initialized in the [Property](property-table.md) table or from a command line.</span></span> <span data-ttu-id="97dc7-126">Si la acción [AppSearch](appsearch-action.md) localiza la firma, el instalador invalida el valor de la propiedad inicializado con el valor encontrado.</span><span class="sxs-lookup"><span data-stu-id="97dc7-126">If the [AppSearch](appsearch-action.md) action locates the signature, the installer overrides the initialized property value with the found value.</span></span> <span data-ttu-id="97dc7-127">Si no se encuentra la firma, se utiliza el valor de la propiedad inicial.</span><span class="sxs-lookup"><span data-stu-id="97dc7-127">If the signature is not found, then the initial property value is used.</span></span> <span data-ttu-id="97dc7-128">Si nunca se inicializó la propiedad, la propiedad solo se establecerá si se encuentra la firma.</span><span class="sxs-lookup"><span data-stu-id="97dc7-128">If the property was never initialized, then the property will only be set if the signature is found.</span></span> <span data-ttu-id="97dc7-129">De lo contrario, la propiedad no está definida.</span><span class="sxs-lookup"><span data-stu-id="97dc7-129">Otherwise, the property is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="97dc7-130"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signatura\_</span><span class="sxs-lookup"><span data-stu-id="97dc7-130"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="97dc7-131">La \_ columna Signature contiene un identificador único denominado Signature y también es una clave externa en las tablas [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md)y [DrLocator](drlocator-table.md) .</span><span class="sxs-lookup"><span data-stu-id="97dc7-131">The Signature\_ column contains a unique identifier called a signature and is also an external key into the [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md), and [DrLocator](drlocator-table.md) tables.</span></span> <span data-ttu-id="97dc7-132">Al buscar un archivo, el valor de esta columna también debe ser una clave externa en la tabla de [signatura](signature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="97dc7-132">When searching for a file, the value in this column must also be a foreign key into the [Signature](signature-table.md) table.</span></span> <span data-ttu-id="97dc7-133">Si el valor de esta columna no aparece en la tabla de firmas, el instalador determina que la búsqueda es para un directorio.</span><span class="sxs-lookup"><span data-stu-id="97dc7-133">If the value in this column is not listed in the Signature table, the installer determines that the search is for a directory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97dc7-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="97dc7-134">Remarks</span></span>

<span data-ttu-id="97dc7-135">La acción [AppSearch](appsearch-action.md) de [*las tablas de secuencia*](s-gly.md) procesa la información de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="97dc7-135">The [AppSearch](appsearch-action.md) action in [*sequence tables*](s-gly.md) processes the information in this table.</span></span> <span data-ttu-id="97dc7-136">Para obtener información sobre el uso de *tablas de secuencia*, vea [usar una tabla de secuencia](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="97dc7-136">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="97dc7-137">La acción [AppSearch](appsearch-action.md) busca firmas mediante la tabla [CompLocator](complocator-table.md) en primer lugar, la tabla [RegLocator](reglocator-table.md) Second, la tabla [IniLocator](inilocator-table.md) Third y, por último, la tabla [DrLocator](drlocator-table.md) .</span><span class="sxs-lookup"><span data-stu-id="97dc7-137">The [AppSearch](appsearch-action.md) action searches for signatures using the [CompLocator](complocator-table.md) table first, the [RegLocator](reglocator-table.md) table second, the [IniLocator](inilocator-table.md) table third, and finally the [DrLocator](drlocator-table.md) table.</span></span> <span data-ttu-id="97dc7-138">Las firmas de archivo se muestran en la tabla de [firmas](signature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="97dc7-138">File signatures are listed in the [Signature](signature-table.md) table.</span></span> <span data-ttu-id="97dc7-139">Una firma que no está en la tabla de signatura denota un directorio y la acción establece la propiedad en la ruta de acceso del directorio para esa firma.</span><span class="sxs-lookup"><span data-stu-id="97dc7-139">A signature that is not in the Signature table denotes a directory and the action sets the property to the directory path for that signature.</span></span>

<span data-ttu-id="97dc7-140">Vea [Buscar aplicaciones, archivos, entradas del registro o entradas del archivo. ini existentes](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span><span class="sxs-lookup"><span data-stu-id="97dc7-140">See [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="97dc7-141">Validación</span><span class="sxs-lookup"><span data-stu-id="97dc7-141">Validation</span></span>

<dl>

[<span data-ttu-id="97dc7-142">ICE03</span><span class="sxs-lookup"><span data-stu-id="97dc7-142">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="97dc7-143">ICE06</span><span class="sxs-lookup"><span data-stu-id="97dc7-143">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="97dc7-144">ICE32</span><span class="sxs-lookup"><span data-stu-id="97dc7-144">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="97dc7-145">ICE52</span><span class="sxs-lookup"><span data-stu-id="97dc7-145">ICE52</span></span>](ice52.md)  
[<span data-ttu-id="97dc7-146">ICE88</span><span class="sxs-lookup"><span data-stu-id="97dc7-146">ICE88</span></span>](ice88.md)  
</dl>

 

 



