---
description: Esta tabla temporal habilita la opción de desinstalación de revisión de acción personalizada para las acciones personalizadas agregadas o actualizadas por una revisión.
ms.assetid: 2d4a934f-e245-4d0a-b8bf-52457107ac08
title: MsiTransformView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb50c397c10ede3a21b40600952d50e55a5ba1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678247"
---
# <a name="msitransformview"></a><span data-ttu-id="3733c-103">MsiTransformView</span><span class="sxs-lookup"><span data-stu-id="3733c-103">MsiTransformView</span></span>

<span data-ttu-id="3733c-104">Esta tabla temporal habilita la [opción de desinstalación de revisión de acción personalizada](custom-action-patch-uninstall-option.md) para las acciones personalizadas agregadas o actualizadas por una revisión.</span><span class="sxs-lookup"><span data-stu-id="3733c-104">This temporary table enables the [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md) for custom actions added or updated by a patch.</span></span>

<span data-ttu-id="3733c-105">Si una revisión agrega o actualiza una acción personalizada con el atributo **msidbCustomActionTypePatchUninstall** , Windows Installer ejecutará la acción personalizada nueva o actualizada cuando se desinstale la revisión.</span><span class="sxs-lookup"><span data-stu-id="3733c-105">If a patch adds or updates a custom action having the **msidbCustomActionTypePatchUninstall** attribute, Windows Installer runs the new or updated custom action when the patch is uninstalled.</span></span> <span data-ttu-id="3733c-106">Windows Installer hace que las actualizaciones de la revisión se desinstalen disponibles para la acción personalizada desinstalar revisión.</span><span class="sxs-lookup"><span data-stu-id="3733c-106">Windows Installer makes the updates within the patch being uninstalled available to the patch uninstall custom action.</span></span> <span data-ttu-id="3733c-107">La revisión debe incluir una *<PatchGUID>* tabla MsiTransformView para proporcionar esta información a Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="3733c-107">The patch must include a MsiTransformView *<PatchGUID>* table to provide this information to Windows Installer.</span></span> <span data-ttu-id="3733c-108">La información de esta tabla está disponible para cualquier acción personalizada inmediata y no está disponible para las acciones personalizadas diferidas.</span><span class="sxs-lookup"><span data-stu-id="3733c-108">The information in this table is available to any immediate custom action, and is unavailable to deferred custom actions.</span></span>

<span data-ttu-id="3733c-109">**[Windows Installer 4,0 y versiones anteriores](not-supported-in-windows-installer-4-0.md):** No compatible.</span><span class="sxs-lookup"><span data-stu-id="3733c-109">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="3733c-110">La [opción de desinstalación de revisión de acción personalizada](custom-action-patch-uninstall-option.md) está disponible a partir de Windows Installer 4,5.</span><span class="sxs-lookup"><span data-stu-id="3733c-110">The [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md) is available beginning with Windows Installer 4.5.</span></span>

<span data-ttu-id="3733c-111">Esta tabla se debe denominar MsiTransformView *<PatchGUID>* TABLE, donde *<PatchGUID>* es el GUID que identifica la revisión de forma única.</span><span class="sxs-lookup"><span data-stu-id="3733c-111">This table should be named MsiTransformView *<PatchGUID>* Table, where *<PatchGUID>* is the GUID that uniquely identifies the patch.</span></span> <span data-ttu-id="3733c-112">La *<PatchGUID>* tabla MsiTransformView tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="3733c-112">The MsiTransformView *<PatchGUID>* Table has the following columns.</span></span>



| <span data-ttu-id="3733c-113">Columna</span><span class="sxs-lookup"><span data-stu-id="3733c-113">Column</span></span>  | <span data-ttu-id="3733c-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="3733c-114">Type</span></span>                         | <span data-ttu-id="3733c-115">Clave</span><span class="sxs-lookup"><span data-stu-id="3733c-115">Key</span></span> | <span data-ttu-id="3733c-116">Nullable</span><span class="sxs-lookup"><span data-stu-id="3733c-116">Nullable</span></span> |
|---------|------------------------------|-----|----------|
| <span data-ttu-id="3733c-117">Tabla</span><span class="sxs-lookup"><span data-stu-id="3733c-117">Table</span></span>   | [<span data-ttu-id="3733c-118">Identificador</span><span class="sxs-lookup"><span data-stu-id="3733c-118">Identifier</span></span>](identifier.md) | <span data-ttu-id="3733c-119">Y</span><span class="sxs-lookup"><span data-stu-id="3733c-119">Y</span></span>   | <span data-ttu-id="3733c-120">N</span><span class="sxs-lookup"><span data-stu-id="3733c-120">N</span></span>        |
| <span data-ttu-id="3733c-121">Columna</span><span class="sxs-lookup"><span data-stu-id="3733c-121">Column</span></span>  | [<span data-ttu-id="3733c-122">Texto</span><span class="sxs-lookup"><span data-stu-id="3733c-122">Text</span></span>](text.md)             | <span data-ttu-id="3733c-123">Y</span><span class="sxs-lookup"><span data-stu-id="3733c-123">Y</span></span>   | <span data-ttu-id="3733c-124">N</span><span class="sxs-lookup"><span data-stu-id="3733c-124">N</span></span>        |
| <span data-ttu-id="3733c-125">Row</span><span class="sxs-lookup"><span data-stu-id="3733c-125">Row</span></span>     | [<span data-ttu-id="3733c-126">Texto</span><span class="sxs-lookup"><span data-stu-id="3733c-126">Text</span></span>](text.md)             | <span data-ttu-id="3733c-127">Y</span><span class="sxs-lookup"><span data-stu-id="3733c-127">Y</span></span>   | <span data-ttu-id="3733c-128">Y</span><span class="sxs-lookup"><span data-stu-id="3733c-128">Y</span></span>        |
| <span data-ttu-id="3733c-129">Datos</span><span class="sxs-lookup"><span data-stu-id="3733c-129">Data</span></span>    | [<span data-ttu-id="3733c-130">Texto</span><span class="sxs-lookup"><span data-stu-id="3733c-130">Text</span></span>](text.md)             | <span data-ttu-id="3733c-131">N</span><span class="sxs-lookup"><span data-stu-id="3733c-131">N</span></span>   | <span data-ttu-id="3733c-132">Y</span><span class="sxs-lookup"><span data-stu-id="3733c-132">Y</span></span>        |
| <span data-ttu-id="3733c-133">Current</span><span class="sxs-lookup"><span data-stu-id="3733c-133">Current</span></span> | [<span data-ttu-id="3733c-134">Texto</span><span class="sxs-lookup"><span data-stu-id="3733c-134">Text</span></span>](text.md)             | <span data-ttu-id="3733c-135">N</span><span class="sxs-lookup"><span data-stu-id="3733c-135">N</span></span>   | <span data-ttu-id="3733c-136">Y</span><span class="sxs-lookup"><span data-stu-id="3733c-136">Y</span></span>        |



 

## <a name="column"></a><span data-ttu-id="3733c-137">Columna</span><span class="sxs-lookup"><span data-stu-id="3733c-137">Column</span></span>

<dl> <dt>

<span data-ttu-id="3733c-138"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Cuadro</span><span class="sxs-lookup"><span data-stu-id="3733c-138"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="3733c-139">Nombre de una tabla de base de datos modificada.</span><span class="sxs-lookup"><span data-stu-id="3733c-139">Name of an altered database table.</span></span>

</dd> <dt>

<span data-ttu-id="3733c-140"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Artículo</span><span class="sxs-lookup"><span data-stu-id="3733c-140"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Column</span></span>
</dt> <dd>

<span data-ttu-id="3733c-141">Nombre de una columna de tabla alterada o inserción, eliminación, creación o eliminación.</span><span class="sxs-lookup"><span data-stu-id="3733c-141">Name of an altered table column or INSERT, DELETE, CREATE, or DROP.</span></span>

</dd> <dt>

<span data-ttu-id="3733c-142"><span id="Row"></span><span id="row"></span><span id="ROW"></span>Columna</span><span class="sxs-lookup"><span data-stu-id="3733c-142"><span id="Row"></span><span id="row"></span><span id="ROW"></span>Row</span></span>
</dt> <dd>

<span data-ttu-id="3733c-143">Una lista de los valores de clave principal separados por tabulaciones.</span><span class="sxs-lookup"><span data-stu-id="3733c-143">A list of the primary key values separated by tabs.</span></span> <span data-ttu-id="3733c-144">Los valores de clave principal NULL se representan mediante un solo carácter de espacio.</span><span class="sxs-lookup"><span data-stu-id="3733c-144">Null primary key values are represented by a single space character.</span></span> <span data-ttu-id="3733c-145">Un valor null en esta columna indica un cambio de esquema.</span><span class="sxs-lookup"><span data-stu-id="3733c-145">A Null value in this column indicates a schema change.</span></span>

</dd> <dt>

<span data-ttu-id="3733c-146"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span><span class="sxs-lookup"><span data-stu-id="3733c-146"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="3733c-147">Los datos, el nombre de un flujo de datos o una definición de columna.</span><span class="sxs-lookup"><span data-stu-id="3733c-147">Data, name of a data stream, or a column definition.</span></span>

</dd> <dt>

<span data-ttu-id="3733c-148"><span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Corrientes</span><span class="sxs-lookup"><span data-stu-id="3733c-148"><span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Current</span></span>
</dt> <dd>

<span data-ttu-id="3733c-149">Valor actual de la base de datos de referencia o de una columna a un número.</span><span class="sxs-lookup"><span data-stu-id="3733c-149">Current value from reference database, or column a number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3733c-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3733c-150">Remarks</span></span>

<span data-ttu-id="3733c-151">Revisión desinstalar las acciones personalizadas se ejecutan cuando se desinstala la revisión.</span><span class="sxs-lookup"><span data-stu-id="3733c-151">Patch uninstall custom actions run when the patch is uninstalled.</span></span> <span data-ttu-id="3733c-152">No se ejecutan cuando se desinstala el producto.</span><span class="sxs-lookup"><span data-stu-id="3733c-152">They do not run when the product is uninstalled.</span></span> <span data-ttu-id="3733c-153">Use la [opción de desinstalación de revisión de acción personalizada](custom-action-patch-uninstall-option.md) y esta tabla para ejecutar una personalizada solo cuando se desinstale la revisión.</span><span class="sxs-lookup"><span data-stu-id="3733c-153">Use the [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md) and this table to run a custom only when the patch is being uninstalled.</span></span>

<span data-ttu-id="3733c-154">Una revisión puede actualizar una acción personalizada proporcionada en el paquete original (archivo. msi). Para ejecutar la versión actualizada de la acción personalizada cuando se desinstale la revisión, marque la acción personalizada con el atributo **msidbCustomActionTypePatchUninstall** en el paquete original.</span><span class="sxs-lookup"><span data-stu-id="3733c-154">A patch can update a custom action provided in the original package (.msi file.) To run the updated version of the custom action when the patch is uninstalled, mark the custom action with the **msidbCustomActionTypePatchUninstall** attribute in the original package.</span></span>

 

 



