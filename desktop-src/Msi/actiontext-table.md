---
description: La tabla ActionText contiene el texto que se va a mostrar en un cuadro de diálogo de progreso y se escribe en el registro para las acciones que tardan mucho tiempo en ejecutarse. El texto mostrado consta de la descripción de la acción y, opcionalmente, los datos con formato de la acción.
ms.assetid: 88d18422-77d0-4929-9341-d078843cb2a9
title: Tabla de ActionText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8071a8542571a3364e151522a7fc4c0b11362045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667059"
---
# <a name="actiontext-table"></a><span data-ttu-id="7b302-104">Tabla de ActionText</span><span class="sxs-lookup"><span data-stu-id="7b302-104">ActionText Table</span></span>

<span data-ttu-id="7b302-105">La tabla ActionText contiene el texto que se va a mostrar en un cuadro de diálogo de progreso y se escribe en el registro para las acciones que tardan mucho tiempo en ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="7b302-105">The ActionText Table contains text to be displayed in a progress dialog box, and written to the log for actions that take a long time to execute.</span></span> <span data-ttu-id="7b302-106">El texto mostrado consta de la descripción de la acción y, opcionalmente, los datos con formato de la acción.</span><span class="sxs-lookup"><span data-stu-id="7b302-106">The displayed text consists of the action description and optionally formatted data from the action.</span></span>

<span data-ttu-id="7b302-107">La tabla ActionText tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="7b302-107">The ActionText Table has the following columns.</span></span>



| <span data-ttu-id="7b302-108">Columna</span><span class="sxs-lookup"><span data-stu-id="7b302-108">Column</span></span>      | <span data-ttu-id="7b302-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="7b302-109">Type</span></span>                         | <span data-ttu-id="7b302-110">Clave</span><span class="sxs-lookup"><span data-stu-id="7b302-110">Key</span></span> | <span data-ttu-id="7b302-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="7b302-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="7b302-112">Acción</span><span class="sxs-lookup"><span data-stu-id="7b302-112">Action</span></span>      | [<span data-ttu-id="7b302-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="7b302-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="7b302-114">Y</span><span class="sxs-lookup"><span data-stu-id="7b302-114">Y</span></span>   | <span data-ttu-id="7b302-115">N</span><span class="sxs-lookup"><span data-stu-id="7b302-115">N</span></span>        |
| <span data-ttu-id="7b302-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b302-116">Description</span></span> | [<span data-ttu-id="7b302-117">Texto</span><span class="sxs-lookup"><span data-stu-id="7b302-117">Text</span></span>](text.md)             | <span data-ttu-id="7b302-118">N</span><span class="sxs-lookup"><span data-stu-id="7b302-118">N</span></span>   | <span data-ttu-id="7b302-119">Y</span><span class="sxs-lookup"><span data-stu-id="7b302-119">Y</span></span>        |
| <span data-ttu-id="7b302-120">Plantilla</span><span class="sxs-lookup"><span data-stu-id="7b302-120">Template</span></span>    | [<span data-ttu-id="7b302-121">Plantilla</span><span class="sxs-lookup"><span data-stu-id="7b302-121">Template</span></span>](template.md)     | <span data-ttu-id="7b302-122">N</span><span class="sxs-lookup"><span data-stu-id="7b302-122">N</span></span>   | <span data-ttu-id="7b302-123">Y</span><span class="sxs-lookup"><span data-stu-id="7b302-123">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="7b302-124">Columnas</span><span class="sxs-lookup"><span data-stu-id="7b302-124">Columns</span></span>

<dl> <dt>

<span data-ttu-id="7b302-125"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Actuar</span><span class="sxs-lookup"><span data-stu-id="7b302-125"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="7b302-126">Nombre de la acción.</span><span class="sxs-lookup"><span data-stu-id="7b302-126">Name of the action.</span></span>

<span data-ttu-id="7b302-127">Clave de la tabla principal.</span><span class="sxs-lookup"><span data-stu-id="7b302-127">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="7b302-128"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación</span><span class="sxs-lookup"><span data-stu-id="7b302-128"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="7b302-129">Descripción localizada que se muestra en el cuadro de diálogo de progreso o que se escribe en el registro cuando se ejecuta la acción.</span><span class="sxs-lookup"><span data-stu-id="7b302-129">Localized description that is displayed in the progress dialog box, or written to the log when the action is executing.</span></span>

</dd> <dt>

<span data-ttu-id="7b302-130"><span id="Template"></span><span id="template"></span><span id="TEMPLATE"></span>Plantillas</span><span class="sxs-lookup"><span data-stu-id="7b302-130"><span id="Template"></span><span id="template"></span><span id="TEMPLATE"></span>Template</span></span>
</dt> <dd>

<span data-ttu-id="7b302-131">Una plantilla de formato localizada que se utiliza para dar formato a los registros de datos de acción que se van a mostrar durante la ejecución de la acción.</span><span class="sxs-lookup"><span data-stu-id="7b302-131">A localized format template that is used to format action data records to display during action execution.</span></span> <span data-ttu-id="7b302-132">Si no se proporciona una plantilla, los datos de la acción no se muestran.</span><span class="sxs-lookup"><span data-stu-id="7b302-132">If a template is not supplied, then the action data is not displayed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7b302-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7b302-133">Remarks</span></span>

<span data-ttu-id="7b302-134">Normalmente, las entradas de la tabla ActionText hacen referencia a las acciones de las tablas de secuencia.</span><span class="sxs-lookup"><span data-stu-id="7b302-134">Typically, the entries in the ActionText table refer to actions in sequence tables.</span></span> <span data-ttu-id="7b302-135">Hay otras acciones que realiza el instalador y que no aparecen en la tabla de secuencia, pero que deben especificarse en la tabla.</span><span class="sxs-lookup"><span data-stu-id="7b302-135">There are other actions the installer performs that are not listed in the sequence table, but still need to be specified in the table.</span></span> <span data-ttu-id="7b302-136">En la tabla siguiente se identifican las entradas de tabla necesarias en las que el nombre de acción y la plantilla deben crearse exactamente como se muestra, pero la descripción se puede personalizar.</span><span class="sxs-lookup"><span data-stu-id="7b302-136">The following table identifies the required table entries where the action name and template must be authored exactly as shown, but the description can be customized.</span></span>



| <span data-ttu-id="7b302-137">Acción</span><span class="sxs-lookup"><span data-stu-id="7b302-137">Action</span></span>          | <span data-ttu-id="7b302-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b302-138">Description</span></span>                             | <span data-ttu-id="7b302-139">Plantilla</span><span class="sxs-lookup"><span data-stu-id="7b302-139">Template</span></span> |
|-----------------|-----------------------------------------|----------|
| <span data-ttu-id="7b302-140">Reversión</span><span class="sxs-lookup"><span data-stu-id="7b302-140">Rollback</span></span>        | <span data-ttu-id="7b302-141">Deshace las acciones.</span><span class="sxs-lookup"><span data-stu-id="7b302-141">Undoes actions.</span></span>                         | <span data-ttu-id="7b302-142">\[1\]</span><span class="sxs-lookup"><span data-stu-id="7b302-142">\[1\]</span></span>    |
| <span data-ttu-id="7b302-143">RollbackCleanup</span><span class="sxs-lookup"><span data-stu-id="7b302-143">RollbackCleanup</span></span> | <span data-ttu-id="7b302-144">Quita los archivos antiguos.</span><span class="sxs-lookup"><span data-stu-id="7b302-144">Removes old files.</span></span>                      | <span data-ttu-id="7b302-145">\[1\]</span><span class="sxs-lookup"><span data-stu-id="7b302-145">\[1\]</span></span>    |
| <span data-ttu-id="7b302-146">GenerateScript</span><span class="sxs-lookup"><span data-stu-id="7b302-146">GenerateScript</span></span>  | <span data-ttu-id="7b302-147">Genera operaciones del sistema para la acción.</span><span class="sxs-lookup"><span data-stu-id="7b302-147">Generates system operations for action.</span></span> | <span data-ttu-id="7b302-148">\[1\]</span><span class="sxs-lookup"><span data-stu-id="7b302-148">\[1\]</span></span>    |



 

> [!Note]  
> <span data-ttu-id="7b302-149">El texto de la acción solo se muestra para las acciones que se ejecutan dentro del script de instalación.</span><span class="sxs-lookup"><span data-stu-id="7b302-149">Action text is only displayed for actions that run within the installation script.</span></span> <span data-ttu-id="7b302-150">Por lo tanto, el texto de la acción solo se muestra para las acciones que se secuencian entre las acciones [InstallInitialize](installinitialize-action.md) y [InstallFinalize](installfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="7b302-150">Therefore, action text is only displayed for actions that are sequenced between the [InstallInitialize](installinitialize-action.md) and [InstallFinalize](installfinalize-action.md) actions.</span></span>

 

<span data-ttu-id="7b302-151">Puede importar una tabla de ActionText localizada en la base de datos mediante Msidb.exe o [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span><span class="sxs-lookup"><span data-stu-id="7b302-151">You can import a localized ActionText table into your database by using Msidb.exe or [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="7b302-152">El SDK incluye una tabla de ActionText localizada para cada uno de los idiomas que aparecen en la sección [localizar las tablas de error y ActionText](localizing-the-error-and-actiontext-tables.md) .</span><span class="sxs-lookup"><span data-stu-id="7b302-152">The SDK includes a localized ActionText Table for each of the languages listed in the [Localizing the Error and ActionText Tables](localizing-the-error-and-actiontext-tables.md) section.</span></span> <span data-ttu-id="7b302-153">Si no se rellena la tabla de ActionText, el instalador carga las cadenas localizadas para el idioma especificado por la propiedad [**ProductLanguage**](productlanguage.md) .</span><span class="sxs-lookup"><span data-stu-id="7b302-153">If the ActionText table is not populated, the installer loads localized strings for the language specified by the [**ProductLanguage**](productlanguage.md) property.</span></span>

## <a name="validation"></a><span data-ttu-id="7b302-154">Validación</span><span class="sxs-lookup"><span data-stu-id="7b302-154">Validation</span></span>

<dl>

[<span data-ttu-id="7b302-155">ICE03</span><span class="sxs-lookup"><span data-stu-id="7b302-155">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="7b302-156">ICE06</span><span class="sxs-lookup"><span data-stu-id="7b302-156">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="7b302-157">ICE46</span><span class="sxs-lookup"><span data-stu-id="7b302-157">ICE46</span></span>](ice46.md)  
</dl>

 

 



