---
description: Una herramienta de combinación evalúa la tabla ModuleInstallExecuteSequence y, a continuación, inserta las acciones calculadas en la tabla InstallExecuteSequence con un número de secuencia correcto.
ms.assetid: 6cd04d9a-5489-4fde-951e-aa962e9bd755
title: Tabla ModuleInstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d294ddfdf06028bf18d518e1086d37a0719f8c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669805"
---
# <a name="moduleinstallexecutesequence-table"></a><span data-ttu-id="72095-103">Tabla ModuleInstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="72095-103">ModuleInstallExecuteSequence Table</span></span>

<span data-ttu-id="72095-104">Una herramienta de combinación evalúa la tabla ModuleInstallExecuteSequence y, a continuación, inserta las acciones calculadas en la [tabla InstallExecuteSequence](installexecutesequence-table.md) con un número de secuencia correcto.</span><span class="sxs-lookup"><span data-stu-id="72095-104">A merge tool evaluates the ModuleInstallExecuteSequence table and then inserts the calculated actions into the [InstallExecuteSequence table](installexecutesequence-table.md) with a correct sequence number.</span></span>

<span data-ttu-id="72095-105">La tabla ModuleInstallExecuteSequence contiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="72095-105">The ModuleInstallExecuteSequence table contains the following columns.</span></span>



| <span data-ttu-id="72095-106">Columna</span><span class="sxs-lookup"><span data-stu-id="72095-106">Column</span></span>     | <span data-ttu-id="72095-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="72095-107">Type</span></span>                         | <span data-ttu-id="72095-108">Clave</span><span class="sxs-lookup"><span data-stu-id="72095-108">Key</span></span> | <span data-ttu-id="72095-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="72095-109">Nullable</span></span> |
|------------|------------------------------|-----|----------|
| <span data-ttu-id="72095-110">Acción</span><span class="sxs-lookup"><span data-stu-id="72095-110">Action</span></span>     | [<span data-ttu-id="72095-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="72095-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="72095-112">Y</span><span class="sxs-lookup"><span data-stu-id="72095-112">Y</span></span>   | <span data-ttu-id="72095-113">N</span><span class="sxs-lookup"><span data-stu-id="72095-113">N</span></span>        |
| <span data-ttu-id="72095-114">Secuencia</span><span class="sxs-lookup"><span data-stu-id="72095-114">Sequence</span></span>   | [<span data-ttu-id="72095-115">Entero</span><span class="sxs-lookup"><span data-stu-id="72095-115">Integer</span></span>](integer.md)       |     | <span data-ttu-id="72095-116">Y</span><span class="sxs-lookup"><span data-stu-id="72095-116">Y</span></span>        |
| <span data-ttu-id="72095-117">BaseAction</span><span class="sxs-lookup"><span data-stu-id="72095-117">BaseAction</span></span> | [<span data-ttu-id="72095-118">Identificador</span><span class="sxs-lookup"><span data-stu-id="72095-118">Identifier</span></span>](identifier.md) |     | <span data-ttu-id="72095-119">Y</span><span class="sxs-lookup"><span data-stu-id="72095-119">Y</span></span>        |
| <span data-ttu-id="72095-120">Después</span><span class="sxs-lookup"><span data-stu-id="72095-120">After</span></span>      | [<span data-ttu-id="72095-121">Entero</span><span class="sxs-lookup"><span data-stu-id="72095-121">Integer</span></span>](integer.md)       |     | <span data-ttu-id="72095-122">Y</span><span class="sxs-lookup"><span data-stu-id="72095-122">Y</span></span>        |
| <span data-ttu-id="72095-123">Condición</span><span class="sxs-lookup"><span data-stu-id="72095-123">Condition</span></span>  | [<span data-ttu-id="72095-124">Condition</span><span class="sxs-lookup"><span data-stu-id="72095-124">Condition</span></span>](condition.md)   |     | <span data-ttu-id="72095-125">Y</span><span class="sxs-lookup"><span data-stu-id="72095-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="72095-126">Columnas</span><span class="sxs-lookup"><span data-stu-id="72095-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="72095-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Actuar</span><span class="sxs-lookup"><span data-stu-id="72095-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="72095-128">Acción que se va a insertar en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="72095-128">Action to insert into sequence.</span></span> <span data-ttu-id="72095-129">Hace referencia a una de las [acciones estándar](standard-actions.md)del instalador o a una entrada en la [tabla CustomAction](customaction-table.md)o la tabla de [cuadro de diálogo](dialog-table.md)del módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="72095-129">Refers to one of the installer [standard actions](standard-actions.md), or an entry in the merge module's [CustomAction table](customaction-table.md), or [Dialog table](dialog-table.md).</span></span>

<span data-ttu-id="72095-130">Si se usa una [acción estándar](standard-actions.md) en la columna de acción de una tabla de secuencia de módulo de combinación, las columnas BaseAction y After de ese registro deben ser null.</span><span class="sxs-lookup"><span data-stu-id="72095-130">If a [standard action](standard-actions.md) is used in the Action column of a merge module sequence table, the BaseAction and After columns of that record must be null.</span></span>

</dd> <dt>

<span data-ttu-id="72095-131"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>SPRJ</span><span class="sxs-lookup"><span data-stu-id="72095-131"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="72095-132">El número de secuencia de una acción estándar.</span><span class="sxs-lookup"><span data-stu-id="72095-132">The sequence number of a standard action.</span></span> <span data-ttu-id="72095-133">Si se especifica una acción o un cuadro de diálogo personalizado en la columna Acción de esta fila, este campo debe establecerse en NULL.</span><span class="sxs-lookup"><span data-stu-id="72095-133">If a custom action or dialog is entered into the Action column of this row, this field must be set to null.</span></span>

<span data-ttu-id="72095-134">Al usar [acciones estándar](standard-actions.md) en las tablas de secuencia de módulo de combinación, el valor de la columna de secuencia debe ser el número de secuencia de acción recomendado.</span><span class="sxs-lookup"><span data-stu-id="72095-134">When using [standard actions](standard-actions.md) in merge module sequence tables, the value in the Sequence column should be the recommended action sequence number.</span></span> <span data-ttu-id="72095-135">Si el número de secuencia del módulo de combinación difiere del de la misma acción en la tabla de secuencia de archivos. msi, la herramienta de combinación utiliza el número de secuencia del archivo. msi.</span><span class="sxs-lookup"><span data-stu-id="72095-135">If the sequence number in the merge module differs from that for the same action in the .msi file sequence table, the merge tool uses the sequence number from the .msi file.</span></span> <span data-ttu-id="72095-136">Vea las secuencias sugeridas en [usar una tabla de secuencia](using-a-sequence-table.md) para ver los números de secuencia recomendados de las acciones estándar.</span><span class="sxs-lookup"><span data-stu-id="72095-136">See the suggested sequences in [Using a Sequence Table](using-a-sequence-table.md) for the recommended sequence numbers of standard actions.</span></span>

</dd> <dt>

<span data-ttu-id="72095-137"><span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>BaseAction</span><span class="sxs-lookup"><span data-stu-id="72095-137"><span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>BaseAction</span></span>
</dt> <dd>

<span data-ttu-id="72095-138">La columna BaseAction puede contener una acción estándar, una acción personalizada especificada en la tabla de acciones personalizadas del módulo de combinación o un cuadro de diálogo especificado en la tabla de diálogo del módulo.</span><span class="sxs-lookup"><span data-stu-id="72095-138">The BaseAction column may contain a standard action, a custom action specified in the merge module's custom action table, or a dialog specified in the module's dialog table.</span></span> <span data-ttu-id="72095-139">La columna BaseAction es una clave en la columna Action de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="72095-139">The BaseAction column is a key into the Action column of this table.</span></span> <span data-ttu-id="72095-140">No puede ser una clave externa en otra tabla o tabla de mezcla del archivo de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="72095-140">It cannot be a foreign key into another merge table or table in the Windows Installer file.</span></span> <span data-ttu-id="72095-141">Esto significa que todas las acciones, acciones personalizadas o cuadros de diálogo estándar que se enumeran en la columna BaseAction también deben aparecer en la columna Acción de otro registro de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="72095-141">This means that every standard action, custom action, or dialog listed in the BaseAction column must also be listed in the Action column of another record in this table.</span></span>

</dd> <dt>

<span data-ttu-id="72095-142"><span id="After"></span><span id="after"></span><span id="AFTER"></span>Continuación</span><span class="sxs-lookup"><span data-stu-id="72095-142"><span id="After"></span><span id="after"></span><span id="AFTER"></span>After</span></span>
</dt> <dd>

<span data-ttu-id="72095-143">Valor booleano que indica si la acción viene antes o después de BaseAction.</span><span class="sxs-lookup"><span data-stu-id="72095-143">Boolean for whether Action comes before or after BaseAction.</span></span>



| <span data-ttu-id="72095-144">Value</span><span class="sxs-lookup"><span data-stu-id="72095-144">Value</span></span> | <span data-ttu-id="72095-145">Significado</span><span class="sxs-lookup"><span data-stu-id="72095-145">Meaning</span></span>                          |
|-------|----------------------------------|
| <span data-ttu-id="72095-146">0</span><span class="sxs-lookup"><span data-stu-id="72095-146">0</span></span>     | <span data-ttu-id="72095-147">Acción que debe transcurrir antes de BaseAction</span><span class="sxs-lookup"><span data-stu-id="72095-147">Action to come before BaseAction</span></span> |
| <span data-ttu-id="72095-148">1</span><span class="sxs-lookup"><span data-stu-id="72095-148">1</span></span>     | <span data-ttu-id="72095-149">Acción que debe aparecer después de BaseAction</span><span class="sxs-lookup"><span data-stu-id="72095-149">Action to come after BaseAction</span></span>  |



 

</dd> <dt>

<span data-ttu-id="72095-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Cumple</span><span class="sxs-lookup"><span data-stu-id="72095-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="72095-151">Instrucción condicional que indica si la acción se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="72095-151">A conditional statement that indicates if the action is to be executed.</span></span> <span data-ttu-id="72095-152">Un valor NULL se evalúa como true.</span><span class="sxs-lookup"><span data-stu-id="72095-152">A null value evaluates to true.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72095-153">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72095-153">Remarks</span></span>

<span data-ttu-id="72095-154">Si la [tabla ModuleInstallExecuteSequence](installexecutesequence-table.md) está presente, la [tabla InstallExecuteSequence](installexecutesequence-table.md) también debe estar presente en el módulo Merge.</span><span class="sxs-lookup"><span data-stu-id="72095-154">If the [ModuleInstallExecuteSequence table](installexecutesequence-table.md) is present, the [InstallExecuteSequence table](installexecutesequence-table.md) must also be present in the merge module.</span></span>

 

 



