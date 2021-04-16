---
description: 'Más información acerca de: JetCreateTableColumnIndex (función)'
title: JetCreateTableColumnIndex función)
TOCTitle: JetCreateTableColumnIndex Function
ms:assetid: 9192614b-20a6-40fb-906a-51fc057e7483
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269343(v=EXCHG.10)
ms:contentKeyID: 32765632
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableColumnIndexA
- JetCreateTableColumnIndexW
- JetCreateTableColumnIndex
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aea9f79617c35c5a956f0cd5f621c7faadffe668
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720636"
---
# <a name="jetcreatetablecolumnindex-function"></a><span data-ttu-id="252fe-103">JetCreateTableColumnIndex función)</span><span class="sxs-lookup"><span data-stu-id="252fe-103">JetCreateTableColumnIndex Function</span></span>


<span data-ttu-id="252fe-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="252fe-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatetablecolumnindex-function"></a><span data-ttu-id="252fe-105">JetCreateTableColumnIndex función)</span><span class="sxs-lookup"><span data-stu-id="252fe-105">JetCreateTableColumnIndex Function</span></span>

<span data-ttu-id="252fe-106">La función **JetCreateTableColumnIndex** crea una tabla en una base de datos de ese con un conjunto inicial de índices y un conjunto inicial de columnas de una matriz de estructuras [JET_TABLECREATE](./jet-tablecreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="252fe-106">The **JetCreateTableColumnIndex** function creates a table in an ESE database with an initial set of indexes and an initial set of columns from an array of [JET_TABLECREATE](./jet-tablecreate-structure.md) structures.</span></span> <span data-ttu-id="252fe-107">El nombre **JetCreateTableColumnIndex** proviene del orden de creación de los objetos.</span><span class="sxs-lookup"><span data-stu-id="252fe-107">The name **JetCreateTableColumnIndex** comes from the order of creation of the objects.</span></span> <span data-ttu-id="252fe-108">En primer lugar, crea una tabla, columnas y, finalmente, índices.</span><span class="sxs-lookup"><span data-stu-id="252fe-108">It first creates a table, columns, and then finally indexes.</span></span>

```cpp
    JET_ERR JET_API JetCreateTableColumnIndex(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in_out      JET_TABLECREATE* ptablecreate
    );
```

### <a name="parameters"></a><span data-ttu-id="252fe-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="252fe-109">Parameters</span></span>

<span data-ttu-id="252fe-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="252fe-110">*sesid*</span></span>

<span data-ttu-id="252fe-111">Contexto de sesión de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="252fe-111">The database session context to use for the API call.</span></span>

<span data-ttu-id="252fe-112">*DBID*</span><span class="sxs-lookup"><span data-stu-id="252fe-112">*dbid*</span></span>

<span data-ttu-id="252fe-113">Identificador de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="252fe-113">The database identifier to use for the API call.</span></span>

<span data-ttu-id="252fe-114">*ptablecreate*</span><span class="sxs-lookup"><span data-stu-id="252fe-114">*ptablecreate*</span></span>

<span data-ttu-id="252fe-115">Puntero a una estructura de [JET_TABLECREATE](./jet-tablecreate-structure.md) que define la tabla que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="252fe-115">A pointer to a [JET_TABLECREATE](./jet-tablecreate-structure.md) structure which defines the table to be created.</span></span> <span data-ttu-id="252fe-116">Consulte [JET_TABLECREATE](./jet-tablecreate-structure.md) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="252fe-116">See [JET_TABLECREATE](./jet-tablecreate-structure.md) for more details.</span></span>

### <a name="return-value"></a><span data-ttu-id="252fe-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="252fe-117">Return Value</span></span>

<span data-ttu-id="252fe-118">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="252fe-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="252fe-119">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="252fe-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="252fe-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="252fe-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="252fe-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="252fe-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="252fe-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="252fe-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="252fe-123">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="252fe-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="252fe-124">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="252fe-124">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="252fe-125">No se pudo resolver la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="252fe-125">The callback function could not be resolved.</span></span> <span data-ttu-id="252fe-126">Es posible que no se haya encontrado el archivo DLL o que no se haya encontrado la función del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="252fe-126">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="252fe-127">Con el registro suficiente habilitado, el registro de eventos proporcionará más detalles.</span><span class="sxs-lookup"><span data-stu-id="252fe-127">With sufficient logging enabled, the event log will provide more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="252fe-128">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="252fe-128">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="252fe-129">Se intentó indexar sobre una columna de actualización de custodia o de SLV (tenga en cuenta que las columnas de SLV están desusadas).</span><span class="sxs-lookup"><span data-stu-id="252fe-129">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="252fe-130">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="252fe-130">JET_errCannotNestDDL</span></span></p></td>
<td><p><span data-ttu-id="252fe-131">Si ptablecreate- &gt; grbit especifica JET_bitTableCreateTemplateTable, pero ptablecreate- &gt; szTemplateTableName se establece en NULL.</span><span class="sxs-lookup"><span data-stu-id="252fe-131">If ptablecreate-&gt;grbit specifies JET_bitTableCreateTemplateTable, but ptablecreate-&gt;szTemplateTableName is set to NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="252fe-132">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="252fe-132">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="252fe-133">Ya existe una columna.</span><span class="sxs-lookup"><span data-stu-id="252fe-133">A column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="252fe-134">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="252fe-134">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="252fe-135">Se intentó indizar una columna que no existe.</span><span class="sxs-lookup"><span data-stu-id="252fe-135">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="252fe-136">El intento de indizar condicionalmente en una columna que no existe también puede generar este error.</span><span class="sxs-lookup"><span data-stu-id="252fe-136">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="252fe-137">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="252fe-137">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="252fe-138">Se intentó agregar una columna redundante.</span><span class="sxs-lookup"><span data-stu-id="252fe-138">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="252fe-139">No debe haber más de una columna de incremento automático y no más de una columna de versión por tabla.</span><span class="sxs-lookup"><span data-stu-id="252fe-139">There should be no more than one autoincrement column, and no more than one version column per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="252fe-140">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="252fe-140">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="252fe-141">Este error se devolverá si el miembro <strong>ulDensity</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> está establecido en un número inferior a 20 o superior a 100.</span><span class="sxs-lookup"><span data-stu-id="252fe-141">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to a number less than 20 or more than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="252fe-142">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="252fe-142">JET_errDDLNotInheritable</span></span></p></td>
<td><p><span data-ttu-id="252fe-143">Significa que la tabla con el nombre del miembro <strong>szTemplateTableName</strong> de la estructura <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> no se marcó como tabla de plantilla (es decir, que la tabla no tenía JET_bitTableCreateTemplateTable Set).</span><span class="sxs-lookup"><span data-stu-id="252fe-143">Signifies that the table named in the <strong>szTemplateTableName</strong> member of the <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> structure was not marked as a template table (that is, that table did not have JET_bitTableCreateTemplateTable set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="252fe-144">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="252fe-144">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="252fe-145">Se ha intentado definir dos índices idénticos.</span><span class="sxs-lookup"><span data-stu-id="252fe-145">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="252fe-146">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="252fe-146">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="252fe-147">Se intentó especificar más de un índice principal para una tabla.</span><span class="sxs-lookup"><span data-stu-id="252fe-147">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="252fe-148">Una tabla debe tener exactamente un índice principal.</span><span class="sxs-lookup"><span data-stu-id="252fe-148">A table must have exactly one primary index.</span></span> <span data-ttu-id="252fe-149">Si no se especifica ningún índice principal, el motor de base de datos creará uno de forma transparente.</span><span class="sxs-lookup"><span data-stu-id="252fe-149">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="252fe-150">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="252fe-150">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="252fe-151">Se especificó una definición de índice no válida.</span><span class="sxs-lookup"><span data-stu-id="252fe-151">An invalid index definition was specified.</span></span> <span data-ttu-id="252fe-152">Algunas de las posibles razones para recibir este error son:</span><span class="sxs-lookup"><span data-stu-id="252fe-152">Some of the possible reasons for receiving this error are:</span></span></p>
<ul>
<li><p><span data-ttu-id="252fe-153">Un índice principal es condicional (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiene JET_bitIndexPrimary establecido y el miembro <strong>cConditionalColumn</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> es mayor que cero).</span><span class="sxs-lookup"><span data-stu-id="252fe-153">A primary index is conditional (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexPrimary set, and <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="252fe-154">Windows Server 2003 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="252fe-154">Windows Server 2003 and later.</span></span> <span data-ttu-id="252fe-155">Se ha intentado crear un índice de tupla con límites de tupla, pero sin pasar el miembro <strong>ptuplelimits</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiene JET_BITINDEXTUPLELIMITS establecido, pero el puntero <strong>ptuplelimits</strong> es null).</span><span class="sxs-lookup"><span data-stu-id="252fe-155">Attempting to create a tuple index with tuple limits, but without passing the <strong>ptuplelimits</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="252fe-156">Pasando una definición de clave no válida en el miembro <strong>szKey</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="252fe-156">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="252fe-157">Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener una descripción de las definiciones válidas.</span><span class="sxs-lookup"><span data-stu-id="252fe-157">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="252fe-158">Establecer el miembro <strong>cbVarSegMac</strong> de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para que sea mayor que JET_cbPrimaryKeyMost (para un índice principal) o mayor que JET_cbSecondaryKeyMost (para un índice secundario).</span><span class="sxs-lookup"><span data-stu-id="252fe-158">Setting the <strong>cbVarSegMac</strong> member in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="252fe-159">Pasar una combinación no válida para un índice Unicode definido por el usuario (uno que tiene el bit de JET_bitIndexUnicode establecido en el miembro <strong>grbit</strong> de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span><span class="sxs-lookup"><span data-stu-id="252fe-159">Passing an invalid combination for a user-defined Unicode index (one which has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span></span> <span data-ttu-id="252fe-160">Algunas causas comunes incluyen el miembro <strong>pidxunicode</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> es null o el LCID especificado en la estructura <strong>pidxunicode</strong> no es válido.</span><span class="sxs-lookup"><span data-stu-id="252fe-160">Some common causes include the <strong>pidxunicode</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is NULL, or the LCID specified in the <strong>pidxunicode</strong> structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="252fe-161">Especificar una columna de varios valores para un índice principal.</span><span class="sxs-lookup"><span data-stu-id="252fe-161">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="252fe-162">Intentando indexar demasiadas columnas condicionales.</span><span class="sxs-lookup"><span data-stu-id="252fe-162">Trying to index too many conditional columns.</span></span> <span data-ttu-id="252fe-163">El miembro <strong>cConditionalColumn</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> no debe ser mayor que JET_ccolKeyMost.</span><span class="sxs-lookup"><span data-stu-id="252fe-163">The <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="252fe-164">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="252fe-164">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="252fe-165">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="252fe-165">Windows XP and later.</span></span> <span data-ttu-id="252fe-166">Se especificó una estructura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> y no se admiten sus límites.</span><span class="sxs-lookup"><span data-stu-id="252fe-166">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="252fe-167">Vea la sección Comentarios de la estructura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="252fe-167">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="252fe-168">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="252fe-168">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="252fe-169">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="252fe-169">Windows XP and later.</span></span> <span data-ttu-id="252fe-170">Un índice de tupla no puede ser único (es decir, el miembro <em>grbit</em> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> no debe tener establecido JET_bitIndexPrimary y JET_bitIndexUnique).</span><span class="sxs-lookup"><span data-stu-id="252fe-170">A tuple index cannot be unique (that is, the <em>grbit</em> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="252fe-171">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="252fe-171">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="252fe-172">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="252fe-172">Windows XP and later.</span></span> <span data-ttu-id="252fe-173">Un índice de tupla solo puede estar en una sola columna (es decir, si el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiene JET_bitIndexTuples establecido y el miembro <strong>szKey</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> especifica más de una columna).</span><span class="sxs-lookup"><span data-stu-id="252fe-173">A tuple index can only be over a single column (that is, if the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="252fe-174">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="252fe-174">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="252fe-175">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="252fe-175">Windows XP and later.</span></span> <span data-ttu-id="252fe-176">Un índice de tupla no puede ser un índice principal (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> no debe tener establecido JET_bitIndexPrimary y JET_bitIndexTuples).</span><span class="sxs-lookup"><span data-stu-id="252fe-176">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="252fe-177">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="252fe-177">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="252fe-178">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="252fe-178">Windows XP and later.</span></span> <span data-ttu-id="252fe-179">Un índice de tupla solo puede estar en una columna de texto o Unicode.</span><span class="sxs-lookup"><span data-stu-id="252fe-179">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="252fe-180">Un intento de indizar otras columnas (como columnas binarias) dará como resultado JET_errIndexTuplesTextColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="252fe-180">An attempt to index other columns (such as binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="252fe-181">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="252fe-181">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="252fe-182">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="252fe-182">Windows XP and later.</span></span> <span data-ttu-id="252fe-183">Un índice de tupla no permite establecer el miembro <strong>cbVarSegMac</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="252fe-183">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure to be set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="252fe-184">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="252fe-184">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="252fe-185">Se intentó crear un índice sin información de versión mientras estaba en una transacción.</span><span class="sxs-lookup"><span data-stu-id="252fe-185">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="252fe-186">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="252fe-186">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="252fe-187">El miembro <strong>CP</strong> de la estructura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> no se ha establecido en una página de códigos válida.</span><span class="sxs-lookup"><span data-stu-id="252fe-187">The <strong>cp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="252fe-188">Los únicos valores válidos para las columnas de texto son inglés (1252) y Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="252fe-188">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="252fe-189">Un valor de 0 significa que se usará el valor predeterminado (Inglés, 1252).</span><span class="sxs-lookup"><span data-stu-id="252fe-189">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="252fe-190">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="252fe-190">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="252fe-191">El miembro <strong>coltyp</strong> de la estructura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> no se ha establecido en un tipo de columna válido.</span><span class="sxs-lookup"><span data-stu-id="252fe-191">The <strong>coltyp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="252fe-192">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="252fe-192">JET_errInvalidCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="252fe-193">Algunas de las razones por las que puede producirse este error:</span><span class="sxs-lookup"><span data-stu-id="252fe-193">Some of the reasons this error may occur:</span></span></p>
<ul>
<li><p><span data-ttu-id="252fe-194">El miembro <strong>rgindexcreate</strong> de la estructura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> se estableció en NULL.</span><span class="sxs-lookup"><span data-stu-id="252fe-194">The <strong>rgindexcreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="252fe-195">El miembro <strong>rgcolumncreate</strong> de la estructura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> se estableció en NULL.</span><span class="sxs-lookup"><span data-stu-id="252fe-195">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="252fe-196">El miembro <strong>cbStruct</strong> de una estructura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> no se ha establecido en un valor válido.</span><span class="sxs-lookup"><span data-stu-id="252fe-196">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure was not set to a valid value.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="252fe-197">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="252fe-197">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="252fe-198">Se especificó una combinación no válida de miembros de <strong>grbit</strong> en <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>.</span><span class="sxs-lookup"><span data-stu-id="252fe-198">An invalid combination of <strong>grbit</strong> members was specified in <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>.</span></span></p>
<p><span data-ttu-id="252fe-199">La definición del índice no es válida porque el miembro <strong>grbit</strong> contiene valores incoherentes.</span><span class="sxs-lookup"><span data-stu-id="252fe-199">The index definition is invalid because the <strong>grbit</strong> member contains inconsistent values.</span></span> <span data-ttu-id="252fe-200">Algunas de las razones posibles son:</span><span class="sxs-lookup"><span data-stu-id="252fe-200">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="252fe-201">Un índice principal tenía un bit ignore especificado (es decir, JET_bitIndexPrimary se pasó con JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull o JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="252fe-201">A primary index had an ignore bit specified (that is, JET_bitIndexPrimary was passed with JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="252fe-202">Un índice vacío no omite ningún miembro nulo (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiene JET_bitIndexEmpty establecido, pero no tiene JET_bitIndexIgnoreAnyNull establecida).</span><span class="sxs-lookup"><span data-stu-id="252fe-202">An empty index does not ignore any NULL members (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="252fe-203">Pasando una estructura de <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> con un miembro <strong>grbit</strong> no válido.</span><span class="sxs-lookup"><span data-stu-id="252fe-203">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="252fe-204">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="252fe-204">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="252fe-205">Se pasó un ID. de configuración regional (LCID) no válido (ya sea a través del miembro <strong>LCID</strong> de la estructura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> a la que apunta el miembro <strong>pidxunicode</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> , o a través del campo <strong>LCID</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</span><span class="sxs-lookup"><span data-stu-id="252fe-205">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member of the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure which is pointed to by the <strong>pidxunicode</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure, or through the <strong>lcid</strong> field of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="252fe-206">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="252fe-206">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="252fe-207">Se proporcionó un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="252fe-207">An invalid parameter was given.</span></span> <span data-ttu-id="252fe-208">Algunas de las razones posibles son:</span><span class="sxs-lookup"><span data-stu-id="252fe-208">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="252fe-209">El miembro <strong>rgcolumncreate</strong> de la estructura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> es NULL.</span><span class="sxs-lookup"><span data-stu-id="252fe-209">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure is NULL.</span></span></p></li>
<li><p><span data-ttu-id="252fe-210">El miembro <strong>cbStruct</strong> de una de las estructuras <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> proporcionadas en el miembro <strong>rgcolumncreate</strong> de la estructura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> no se estableció en sizeof (JET_COLUMNCREATE).</span><span class="sxs-lookup"><span data-stu-id="252fe-210">The <strong>cbStruct</strong> member of one of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structures given in the <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was not set to sizeof( JET_COLUMNCREATE).</span></span></p></li>
<li><p><span data-ttu-id="252fe-211">El miembro <strong>cbKey</strong> de una estructura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="252fe-211">The <strong>cbKey</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="252fe-212">El miembro <strong>cbStruct</strong> de una estructura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> no se establece en sizeof (JET_INDEXCREATE).</span><span class="sxs-lookup"><span data-stu-id="252fe-212">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is not set to sizeof( JET_INDEXCREATE).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="252fe-213">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="252fe-213">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="252fe-214">El registro es demasiado grande.</span><span class="sxs-lookup"><span data-stu-id="252fe-214">The record is too big.</span></span> <span data-ttu-id="252fe-215">La suma del miembro <strong>cbMax</strong> de la estructura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> para todas las columnas fijas no debe superar un valor determinado.</span><span class="sxs-lookup"><span data-stu-id="252fe-215">The sum of the <strong>cbMax</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure for all fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="252fe-216">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="252fe-216">JET_errTableDuplicate</span></span></p></td>
<td><p><span data-ttu-id="252fe-217">La tabla ya existe.</span><span class="sxs-lookup"><span data-stu-id="252fe-217">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="252fe-218">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="252fe-218">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="252fe-219">Se intentó agregar demasiadas columnas a la tabla.</span><span class="sxs-lookup"><span data-stu-id="252fe-219">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="252fe-220">Una tabla no puede tener más de JET_ccolFixedMost columnas fijas, ni más de JET_ccolVarMost columnas de longitud variable, ni más de JET_ccolTaggedMost columnas etiquetadas.</span><span class="sxs-lookup"><span data-stu-id="252fe-220">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="252fe-221">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="252fe-221">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="252fe-222">Error al intentar normalizar una columna Unicode.</span><span class="sxs-lookup"><span data-stu-id="252fe-222">An error occurred attempting to normalize a Unicode column.</span></span> <span data-ttu-id="252fe-223">Esto puede deberse a la falta de recursos del sistema.</span><span class="sxs-lookup"><span data-stu-id="252fe-223">This can be caused by running out of system resources.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="252fe-224">Observaciones</span><span class="sxs-lookup"><span data-stu-id="252fe-224">Remarks</span></span>

<span data-ttu-id="252fe-225">Llamar a **JetCreateTableColumnIndex** es idéntico a llamar a [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), con cada campo de la estructura [JET_TABLECREATE2](./jet-tablecreate2-structure.md) que contiene el valor del campo correspondiente de [JET_TABLECREATE](./jet-tablecreate-structure.md), con las siguientes excepciones:</span><span class="sxs-lookup"><span data-stu-id="252fe-225">Calling **JetCreateTableColumnIndex** is identical to calling [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), with each field in the [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structure containing the value of the corresponding field of [JET_TABLECREATE](./jet-tablecreate-structure.md), with the following exceptions:</span></span>

  - <span data-ttu-id="252fe-226">JET_TABLECREATE2. cbStruct establecido en sizeof (JET_TABLECREATE2)</span><span class="sxs-lookup"><span data-stu-id="252fe-226">JET_TABLECREATE2.cbStruct set to sizeof( JET_TABLECREATE2)</span></span>

  - <span data-ttu-id="252fe-227">JET_TABLECREATE2. szCallback establecido en NULL</span><span class="sxs-lookup"><span data-stu-id="252fe-227">JET_TABLECREATE2.szCallback set to NULL</span></span>

  - <span data-ttu-id="252fe-228">JET_TABLECREATE2. cbtyp establecido en 0</span><span class="sxs-lookup"><span data-stu-id="252fe-228">JET_TABLECREATE2.cbtyp set to 0</span></span>

<span data-ttu-id="252fe-229">Consulte [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="252fe-229">See [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) for more details.</span></span>

<span data-ttu-id="252fe-230">Al igual que [JetOpenTable](./jetopentable-function.md), cuando la aplicación se realiza utilizando el ID *. de tipo devuelto,* normalmente se debe cerrar con [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="252fe-230">Like [JetOpenTable](./jetopentable-function.md), when the application is done using the returned *tableid*, it should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="252fe-231">Requisitos</span><span class="sxs-lookup"><span data-stu-id="252fe-231">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="252fe-232"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="252fe-232"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="252fe-233">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="252fe-233">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="252fe-234"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="252fe-234"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="252fe-235">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="252fe-235">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="252fe-236"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="252fe-236"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="252fe-237">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="252fe-237">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="252fe-238"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="252fe-238"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="252fe-239">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="252fe-239">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="252fe-240"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="252fe-240"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="252fe-241">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="252fe-241">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="252fe-242"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="252fe-242"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="252fe-243">Se implementa como <strong>JetCreateTableColumnIndexW</strong> (Unicode) y <strong>JetCreateTableColumnIndexA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="252fe-243">Implemented as <strong>JetCreateTableColumnIndexW</strong> (Unicode) and <strong>JetCreateTableColumnIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="252fe-244">Consulte también</span><span class="sxs-lookup"><span data-stu-id="252fe-244">See Also</span></span>

[<span data-ttu-id="252fe-245">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="252fe-245">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="252fe-246">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="252fe-246">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="252fe-247">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="252fe-247">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="252fe-248">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="252fe-248">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="252fe-249">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="252fe-249">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="252fe-250">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="252fe-250">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="252fe-251">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="252fe-251">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="252fe-252">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="252fe-252">JetCreateTableColumnIndex</span></span>]()  
[<span data-ttu-id="252fe-253">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="252fe-253">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
