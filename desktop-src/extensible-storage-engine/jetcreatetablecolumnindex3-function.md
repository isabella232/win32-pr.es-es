---
description: 'Más información acerca de: JetCreateTableColumnIndex3 (función)'
title: JetCreateTableColumnIndex3 función)
TOCTitle: JetCreateTableColumnIndex3 Function
ms:assetid: c1a1b091-b4a6-4cdc-a0ea-af21c1462449
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294079(v=EXCHG.10)
ms:contentKeyID: 32765694
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableColumnIndex3
- JetCreateTableColumnIndex3W
- JetCreateTableColumnIndex3A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bf1d6aed3178f5593826097f8c5d6b01bd8c72d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720754"
---
# <a name="jetcreatetablecolumnindex3-function"></a><span data-ttu-id="59bc6-103">JetCreateTableColumnIndex3 función)</span><span class="sxs-lookup"><span data-stu-id="59bc6-103">JetCreateTableColumnIndex3 Function</span></span>


<span data-ttu-id="59bc6-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="59bc6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatetablecolumnindex3-function"></a><span data-ttu-id="59bc6-105">JetCreateTableColumnIndex3 función)</span><span class="sxs-lookup"><span data-stu-id="59bc6-105">JetCreateTableColumnIndex3 Function</span></span>

<span data-ttu-id="59bc6-106">La función **JetCreateTableColumnIndex3** crea una tabla en una base de datos de ese con un conjunto inicial de índices y un conjunto inicial de columnas de una matriz de estructuras [JET_TABLECREATE3](./jet-tablecreate3-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="59bc6-106">The **JetCreateTableColumnIndex3** function creates a table in an ESE database with an initial set of indexes and an initial set of columns from an array of [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structures.</span></span> <span data-ttu-id="59bc6-107">La estructura de [JET_TABLECREATE3](./jet-tablecreate3-structure.md) permite especificar una función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="59bc6-107">The [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structure allows a callback function to be specified.</span></span>

<span data-ttu-id="59bc6-108">**Windows 7:** **JetCreateTableColumnIndex3** se incluye en el sistema operativo Windows 7.</span><span class="sxs-lookup"><span data-stu-id="59bc6-108">**Windows 7:** **JetCreateTableColumnIndex3** is introduced in the Windows 7 operating system.</span></span>

```cpp
    JET_ERR JET_API JetCreateTableColumnIndex3(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in_out      JET_TABLECREATE3* ptablecreate
    );
```

### <a name="parameters"></a><span data-ttu-id="59bc6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="59bc6-109">Parameters</span></span>

<span data-ttu-id="59bc6-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="59bc6-110">*sesid*</span></span>

<span data-ttu-id="59bc6-111">Contexto de sesión de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="59bc6-111">The database session context to use for the API call.</span></span>

<span data-ttu-id="59bc6-112">*DBID*</span><span class="sxs-lookup"><span data-stu-id="59bc6-112">*dbid*</span></span>

<span data-ttu-id="59bc6-113">Identificador de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="59bc6-113">The database identifier to use for the API call.</span></span>

<span data-ttu-id="59bc6-114">*ptablecreate*</span><span class="sxs-lookup"><span data-stu-id="59bc6-114">*ptablecreate*</span></span>

<span data-ttu-id="59bc6-115">Puntero a una estructura de [JET_TABLECREATE3](./jet-tablecreate3-structure.md) que define la tabla que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="59bc6-115">A pointer to a [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structure that defines the table to be created.</span></span> <span data-ttu-id="59bc6-116">Consulte [JET_TABLECREATE3](./jet-tablecreate3-structure.md) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="59bc6-116">See [JET_TABLECREATE3](./jet-tablecreate3-structure.md) for more details.</span></span>

### <a name="return-value"></a><span data-ttu-id="59bc6-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="59bc6-117">Return Value</span></span>

<span data-ttu-id="59bc6-118">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="59bc6-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="59bc6-119">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="59bc6-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="59bc6-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="59bc6-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="59bc6-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="59bc6-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="59bc6-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="59bc6-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="59bc6-123">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="59bc6-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59bc6-124">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="59bc6-124">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="59bc6-125">No se pudo resolver la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="59bc6-125">The callback function could not be resolved.</span></span> <span data-ttu-id="59bc6-126">Es posible que no se haya encontrado el archivo DLL o que no se haya encontrado la función del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="59bc6-126">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="59bc6-127">Con el registro suficiente habilitado, el registro de eventos proporcionará más detalles.</span><span class="sxs-lookup"><span data-stu-id="59bc6-127">With sufficient logging enabled, the event log will provide more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59bc6-128">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="59bc6-128">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="59bc6-129">Se intentó indexar sobre una columna de actualización de custodia o de SLV (tenga en cuenta que las columnas de SLV están desusadas).</span><span class="sxs-lookup"><span data-stu-id="59bc6-129">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59bc6-130">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="59bc6-130">JET_errCannotNestDDL</span></span></p></td>
<td><p><span data-ttu-id="59bc6-131">Si ptablecreate- &gt; grbit especifica JET_bitTableCreateTemplateTable, pero ptablecreate- &gt; szTemplateTableName se establece en NULL.</span><span class="sxs-lookup"><span data-stu-id="59bc6-131">If ptablecreate-&gt;grbit specifies JET_bitTableCreateTemplateTable, but ptablecreate-&gt;szTemplateTableName is set to NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59bc6-132">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="59bc6-132">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="59bc6-133">Ya existe una columna.</span><span class="sxs-lookup"><span data-stu-id="59bc6-133">A column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59bc6-134">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="59bc6-134">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="59bc6-135">Se intentó indizar una columna que no existe.</span><span class="sxs-lookup"><span data-stu-id="59bc6-135">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="59bc6-136">El intento de indizar condicionalmente en una columna que no existe también puede generar este error.</span><span class="sxs-lookup"><span data-stu-id="59bc6-136">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59bc6-137">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="59bc6-137">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="59bc6-138">Se intentó agregar una columna redundante.</span><span class="sxs-lookup"><span data-stu-id="59bc6-138">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="59bc6-139">No debe haber más de una columna de incremento automático y no más de una columna de versión por tabla.</span><span class="sxs-lookup"><span data-stu-id="59bc6-139">There should be no more than one autoincrement column, and no more than one version column per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59bc6-140">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="59bc6-140">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="59bc6-141">Este error se devolverá si el miembro <strong>ulDensity</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> está establecido en un número inferior a 20 o superior a 100.</span><span class="sxs-lookup"><span data-stu-id="59bc6-141">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to a number less than 20 or more than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59bc6-142">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="59bc6-142">JET_errDDLNotInheritable</span></span></p></td>
<td><p><span data-ttu-id="59bc6-143">Significa que la tabla con el nombre del miembro <strong>szTemplateTableName</strong> de la estructura <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> no se marcó como tabla de plantilla (es decir, que la tabla no tenía JET_bitTableCreateTemplateTable Set).</span><span class="sxs-lookup"><span data-stu-id="59bc6-143">Signifies that the table named in the <strong>szTemplateTableName</strong> member of the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure was not marked as a template table (that is, that table did not have JET_bitTableCreateTemplateTable set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59bc6-144">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="59bc6-144">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="59bc6-145">Se ha intentado definir dos índices idénticos.</span><span class="sxs-lookup"><span data-stu-id="59bc6-145">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59bc6-146">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="59bc6-146">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="59bc6-147">Se intentó especificar más de un índice principal para una tabla.</span><span class="sxs-lookup"><span data-stu-id="59bc6-147">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="59bc6-148">Una tabla debe tener exactamente un índice principal.</span><span class="sxs-lookup"><span data-stu-id="59bc6-148">A table must have exactly one primary index.</span></span> <span data-ttu-id="59bc6-149">Si no se especifica ningún índice principal, el motor de base de datos creará uno de forma transparente.</span><span class="sxs-lookup"><span data-stu-id="59bc6-149">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59bc6-150">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="59bc6-150">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="59bc6-151">Se especificó una definición de índice no válida.</span><span class="sxs-lookup"><span data-stu-id="59bc6-151">An invalid index definition was specified.</span></span> <span data-ttu-id="59bc6-152">A continuación se indican algunas de las razones posibles para recibir este error:</span><span class="sxs-lookup"><span data-stu-id="59bc6-152">The following are some of the possible reasons for receiving this error:</span></span></p>
<ul>
<li><p><span data-ttu-id="59bc6-153">Un índice principal es condicional (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tiene JET_bitIndexPrimary establecido y el miembro <strong>cConditionalColumn</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> es mayor que cero).</span><span class="sxs-lookup"><span data-stu-id="59bc6-153">A primary index is conditional (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexPrimary set, and <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="59bc6-154">Windows Server 2003 y versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="59bc6-154">Windows Server 2003 and later versions of Windows.</span></span> <span data-ttu-id="59bc6-155">Se ha intentado crear un índice de tupla con límites de tupla, pero sin pasar el miembro <strong>ptuplelimits</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (es decir, el miembro <strong>grbit</strong> de la estructura JET_INDEXCREATE2 tiene JET_bitIndexTupleLimits establecido, pero el puntero <strong>ptuplelimits</strong> es null).</span><span class="sxs-lookup"><span data-stu-id="59bc6-155">Attempting to create a tuple index with tuple limits, but without passing the <strong>ptuplelimits</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure (that is, the <strong>grbit</strong> member of the JET_INDEXCREATE2 structure has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="59bc6-156">Pasando una definición de clave no válida en el miembro <strong>szKey</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="59bc6-156">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="59bc6-157">Consulte <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> para obtener una descripción de las definiciones válidas.</span><span class="sxs-lookup"><span data-stu-id="59bc6-157">See <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="59bc6-158">Establecer el miembro <strong>cbVarSegMac</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> para que sea mayor que JET_cbPrimaryKeyMost (para un índice principal) o mayor que JET_cbSecondaryKeyMost (para un índice secundario).</span><span class="sxs-lookup"><span data-stu-id="59bc6-158">Setting the <strong>cbVarSegMac</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="59bc6-159">Pasar una combinación no válida para un índice Unicode definido por el usuario (una que tiene el bit de JET_bitIndexUnicode establecido en el miembro <strong>grbit</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span><span class="sxs-lookup"><span data-stu-id="59bc6-159">Passing an invalid combination for a user-defined Unicode index (one that has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span></span> <span data-ttu-id="59bc6-160">Algunas causas comunes incluyen el miembro <strong>pidxunicode</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> es null o el LCID especificado en la estructura <strong>pidxunicode</strong> no es válido.</span><span class="sxs-lookup"><span data-stu-id="59bc6-160">Some common causes include the <strong>pidxunicode</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is NULL, or the LCID specified in the <strong>pidxunicode</strong> structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="59bc6-161">Especificar una columna de varios valores para un índice principal.</span><span class="sxs-lookup"><span data-stu-id="59bc6-161">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="59bc6-162">Intentando indexar demasiadas columnas condicionales.</span><span class="sxs-lookup"><span data-stu-id="59bc6-162">Trying to index too many conditional columns.</span></span> <span data-ttu-id="59bc6-163">El miembro <strong>cConditionalColumn</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> no debe ser mayor que JET_ccolKeyMost.</span><span class="sxs-lookup"><span data-stu-id="59bc6-163">The <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59bc6-164">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="59bc6-164">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="59bc6-165">Windows XP y versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="59bc6-165">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="59bc6-166">Se especificó una estructura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> y no se admiten sus límites.</span><span class="sxs-lookup"><span data-stu-id="59bc6-166">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="59bc6-167">Vea la sección Comentarios de la estructura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="59bc6-167">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59bc6-168">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="59bc6-168">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="59bc6-169">Windows XP y versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="59bc6-169">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="59bc6-170">Un índice de tupla no puede ser único (es decir, el miembro <em>grbit</em> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> no debe tener establecido JET_bitIndexPrimary y JET_bitIndexUnique).</span><span class="sxs-lookup"><span data-stu-id="59bc6-170">A tuple index cannot be unique (that is, the <em>grbit</em> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59bc6-171">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="59bc6-171">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="59bc6-172">Windows XP y versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="59bc6-172">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="59bc6-173">Un índice de tupla solo puede estar en una sola columna (es decir, si el miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tiene JET_bitIndexTuples establecido y el miembro <strong>szKey</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> especifica más de una columna).</span><span class="sxs-lookup"><span data-stu-id="59bc6-173">A tuple index can only be over a single column (that is, if the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59bc6-174">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="59bc6-174">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="59bc6-175">Windows XP y versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="59bc6-175">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="59bc6-176">Un índice de tupla no puede ser un índice principal (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> no debe tener establecido JET_bitIndexPrimary y JET_bitIndexTuples).</span><span class="sxs-lookup"><span data-stu-id="59bc6-176">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59bc6-177">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="59bc6-177">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="59bc6-178">Windows XP y versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="59bc6-178">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="59bc6-179">Un índice de tupla solo puede estar en una columna de texto o Unicode.</span><span class="sxs-lookup"><span data-stu-id="59bc6-179">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="59bc6-180">Un intento de indizar otras columnas (como columnas binarias) dará como resultado JET_errIndexTuplesTextColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="59bc6-180">An attempt to index other columns (such as binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59bc6-181">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="59bc6-181">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="59bc6-182">Windows XP y versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="59bc6-182">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="59bc6-183">Un índice de tupla no permite establecer el miembro <strong>cbVarSegMac</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="59bc6-183">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure to be set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59bc6-184">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="59bc6-184">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="59bc6-185">Se intentó crear un índice sin información de versión mientras estaba en una transacción.</span><span class="sxs-lookup"><span data-stu-id="59bc6-185">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59bc6-186">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="59bc6-186">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="59bc6-187">El miembro <strong>CP</strong> de la estructura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> no se ha establecido en una página de códigos válida.</span><span class="sxs-lookup"><span data-stu-id="59bc6-187">The <strong>cp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="59bc6-188">Los únicos valores válidos para las columnas de texto son inglés (1252) y Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="59bc6-188">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="59bc6-189">Un valor de 0 significa que se usará el valor predeterminado (Inglés, 1252).</span><span class="sxs-lookup"><span data-stu-id="59bc6-189">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59bc6-190">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="59bc6-190">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="59bc6-191">El miembro <strong>coltyp</strong> de la estructura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> no se ha establecido en un tipo de columna válido.</span><span class="sxs-lookup"><span data-stu-id="59bc6-191">The <strong>coltyp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59bc6-192">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="59bc6-192">JET_errInvalidCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="59bc6-193">A continuación se indican algunos de los motivos por los que puede producirse este error:</span><span class="sxs-lookup"><span data-stu-id="59bc6-193">The following are some reasons why this error may occur:</span></span></p>
<ul>
<li><p><span data-ttu-id="59bc6-194">El miembro <strong>rgindexcreate</strong> de la estructura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> se estableció en NULL.</span><span class="sxs-lookup"><span data-stu-id="59bc6-194">The <strong>rgindexcreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="59bc6-195">El miembro <strong>rgcolumncreate</strong> de la estructura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> se estableció en NULL.</span><span class="sxs-lookup"><span data-stu-id="59bc6-195">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="59bc6-196">El miembro <strong>cbStruct</strong> de una estructura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> no se ha establecido en un valor válido.</span><span class="sxs-lookup"><span data-stu-id="59bc6-196">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure was not set to a valid value.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59bc6-197">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="59bc6-197">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="59bc6-198">Se especificó una combinación no válida de miembros de <strong>grbit</strong> en <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a>.</span><span class="sxs-lookup"><span data-stu-id="59bc6-198">An invalid combination of <strong>grbit</strong> members was specified in <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a>.</span></span></p>
<p><span data-ttu-id="59bc6-199">La definición del índice no es válida porque el miembro <strong>grbit</strong> contiene valores incoherentes.</span><span class="sxs-lookup"><span data-stu-id="59bc6-199">The index definition is invalid because the <strong>grbit</strong> member contains inconsistent values.</span></span> <span data-ttu-id="59bc6-200">A continuación se indican algunas razones posibles:</span><span class="sxs-lookup"><span data-stu-id="59bc6-200">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="59bc6-201">Un índice principal tenía un bit ignore especificado (es decir, JET_bitIndexPrimary se pasó con JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull o JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="59bc6-201">A primary index had an ignore bit specified (that is, JET_bitIndexPrimary was passed with JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="59bc6-202">Un índice vacío no omite ningún miembro nulo (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tiene JET_bitIndexEmpty establecido, pero no tiene JET_bitIndexIgnoreAnyNull establecida).</span><span class="sxs-lookup"><span data-stu-id="59bc6-202">An empty index does not ignore any NULL members (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="59bc6-203">Pasando una estructura de <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> con un miembro <strong>grbit</strong> no válido.</span><span class="sxs-lookup"><span data-stu-id="59bc6-203">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59bc6-204">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="59bc6-204">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="59bc6-205">Se pasó un ID. de configuración regional (LCID) no válido (ya sea a través del miembro <strong>LCID</strong> de la estructura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> a la que apunta el miembro <strong>pidxunicode</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> , o a través del campo <strong>LCID</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span><span class="sxs-lookup"><span data-stu-id="59bc6-205">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member of the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure which is pointed to by the <strong>pidxunicode</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure, or through the <strong>lcid</strong> field of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59bc6-206">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="59bc6-206">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="59bc6-207">Se proporcionó un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="59bc6-207">An invalid parameter was given.</span></span> <span data-ttu-id="59bc6-208">A continuación se indican algunas razones posibles:</span><span class="sxs-lookup"><span data-stu-id="59bc6-208">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="59bc6-209">El miembro <strong>rgcolumncreate</strong> de la estructura <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> es NULL.</span><span class="sxs-lookup"><span data-stu-id="59bc6-209">The <strong>rgcolumncreate</strong> member of the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure is NULL.</span></span></p></li>
<li><p><span data-ttu-id="59bc6-210">El miembro <strong>cbStruct</strong> de una de las estructuras <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> proporcionadas en el miembro <strong>rgcolumncreate</strong> de la estructura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> no se estableció en sizeof (JET_COLUMNCREATE).</span><span class="sxs-lookup"><span data-stu-id="59bc6-210">The <strong>cbStruct</strong> member of one of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structures given in the <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was not set to sizeof( JET_COLUMNCREATE ).</span></span></p></li>
<li><p><span data-ttu-id="59bc6-211">El miembro <strong>cbKey</strong> de una estructura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="59bc6-211">The <strong>cbKey</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="59bc6-212">El miembro <strong>cbStruct</strong> de una estructura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> no se establece en sizeof (JET_INDEXCREATE2).</span><span class="sxs-lookup"><span data-stu-id="59bc6-212">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is not set to sizeof( JET_INDEXCREATE2 ).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59bc6-213">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="59bc6-213">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="59bc6-214">El registro es demasiado grande.</span><span class="sxs-lookup"><span data-stu-id="59bc6-214">The record is too big.</span></span> <span data-ttu-id="59bc6-215">La suma del miembro <strong>cbMax</strong> de la estructura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> para todas las columnas fijas no debe superar un valor determinado.</span><span class="sxs-lookup"><span data-stu-id="59bc6-215">The sum of the <strong>cbMax</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure for all fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59bc6-216">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="59bc6-216">JET_errTableDuplicate</span></span></p></td>
<td><p><span data-ttu-id="59bc6-217">La tabla ya existe.</span><span class="sxs-lookup"><span data-stu-id="59bc6-217">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59bc6-218">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="59bc6-218">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="59bc6-219">Se intentó agregar demasiadas columnas a la tabla.</span><span class="sxs-lookup"><span data-stu-id="59bc6-219">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="59bc6-220">Una tabla no puede tener más de JET_ccolFixedMost columnas fijas, ni más de JET_ccolVarMost columnas de longitud variable, ni más de JET_ccolTaggedMost columnas etiquetadas.</span><span class="sxs-lookup"><span data-stu-id="59bc6-220">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59bc6-221">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="59bc6-221">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="59bc6-222">Error al intentar normalizar una columna Unicode.</span><span class="sxs-lookup"><span data-stu-id="59bc6-222">An error occurred attempting to normalize a Unicode column.</span></span> <span data-ttu-id="59bc6-223">Esto puede deberse a la falta de recursos del sistema.</span><span class="sxs-lookup"><span data-stu-id="59bc6-223">This can be caused by running out of system resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59bc6-224">JET_errSpaceHintsInvalid</span><span class="sxs-lookup"><span data-stu-id="59bc6-224">JET_errSpaceHintsInvalid</span></span></p></td>
<td><p><span data-ttu-id="59bc6-225">Un elemento de la estructura de sugerencias de espacio JET no era correcto o accionable.</span><span class="sxs-lookup"><span data-stu-id="59bc6-225">An element of the JET space hints structure was not correct or actionable.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="59bc6-226">Observaciones</span><span class="sxs-lookup"><span data-stu-id="59bc6-226">Remarks</span></span>

<span data-ttu-id="59bc6-227">El nombre **JetCreateTableColumnIndex3** procede del orden de creación de los objetos: primero crea una tabla, columnas y, finalmente, índices.</span><span class="sxs-lookup"><span data-stu-id="59bc6-227">The name **JetCreateTableColumnIndex3** comes from the order of creation of the objects: It first creates a table, columns, and then finally indexes.</span></span> <span data-ttu-id="59bc6-228">**JetCreateTableColumnIndex3** crea una tabla con un conjunto inicial de columnas e índices.</span><span class="sxs-lookup"><span data-stu-id="59bc6-228">**JetCreateTableColumnIndex3** creates a table with an initial set of columns and indexes.</span></span> <span data-ttu-id="59bc6-229">Las columnas e índices adicionales se pueden agregar y quitar dinámicamente con [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md)y [JetDeleteIndex](./jetdeleteindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="59bc6-229">Additional columns and indexes can be added and removed dynamically with [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md), and [JetDeleteIndex](./jetdeleteindex-function.md).</span></span>

<span data-ttu-id="59bc6-230">Al igual que [JetOpenTable](./jetopentable-function.md), cuando la aplicación se realiza utilizando el ID *. de tipo devuelto,* normalmente se debe cerrar con [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="59bc6-230">Like [JetOpenTable](./jetopentable-function.md), when the application is done using the returned *tableid*, it should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="59bc6-231">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59bc6-231">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="59bc6-232"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="59bc6-232"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="59bc6-233">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="59bc6-233">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59bc6-234"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="59bc6-234"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="59bc6-235">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="59bc6-235">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59bc6-236"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="59bc6-236"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="59bc6-237">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="59bc6-237">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59bc6-238"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="59bc6-238"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="59bc6-239">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="59bc6-239">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59bc6-240"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="59bc6-240"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="59bc6-241">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="59bc6-241">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59bc6-242"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="59bc6-242"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="59bc6-243">Se implementa como <strong>JetCreateTableColumnIndex3W</strong> (Unicode) y <strong>JetCreateTableColumnIndex3A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="59bc6-243">Implemented as <strong>JetCreateTableColumnIndex3W</strong> (Unicode) and <strong>JetCreateTableColumnIndex3A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="59bc6-244">Consulte también</span><span class="sxs-lookup"><span data-stu-id="59bc6-244">See Also</span></span>

[<span data-ttu-id="59bc6-245">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="59bc6-245">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="59bc6-246">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="59bc6-246">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="59bc6-247">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="59bc6-247">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="59bc6-248">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="59bc6-248">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="59bc6-249">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="59bc6-249">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="59bc6-250">JET_INDEXCREATE2</span><span class="sxs-lookup"><span data-stu-id="59bc6-250">JET_INDEXCREATE2</span></span>](./jet-indexcreate2-structure.md)  
[<span data-ttu-id="59bc6-251">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="59bc6-251">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="59bc6-252">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="59bc6-252">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="59bc6-253">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="59bc6-253">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="59bc6-254">JET_TABLECREATE3</span><span class="sxs-lookup"><span data-stu-id="59bc6-254">JET_TABLECREATE3</span></span>](./jet-tablecreate3-structure.md)  
[<span data-ttu-id="59bc6-255">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="59bc6-255">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="59bc6-256">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="59bc6-256">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="59bc6-257">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="59bc6-257">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="59bc6-258">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="59bc6-258">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="59bc6-259">JetCreateIndex3</span><span class="sxs-lookup"><span data-stu-id="59bc6-259">JetCreateIndex3</span></span>](./jetcreateindex3-function.md)  
[<span data-ttu-id="59bc6-260">JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="59bc6-260">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="59bc6-261">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="59bc6-261">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="59bc6-262">JetDeleteColumn</span><span class="sxs-lookup"><span data-stu-id="59bc6-262">JetDeleteColumn</span></span>](./jetdeletecolumn-function.md)  
[<span data-ttu-id="59bc6-263">JetDeleteColumn2</span><span class="sxs-lookup"><span data-stu-id="59bc6-263">JetDeleteColumn2</span></span>](./jetdeletecolumn2-function.md)
