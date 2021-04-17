---
description: 'Más información acerca de: JetCreateTableColumnIndex4W (función)'
title: JetCreateTableColumnIndex4W función)
TOCTitle: JetCreateTableColumnIndex4W Function
ms:assetid: 5a74b397-dfb4-4a1d-807b-284329239bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835042(v=EXCHG.10)
ms:contentKeyID: 49894664
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCreateTableColumnIndex4W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 26ebdb8cf62123febe2d44b5a638c285c180062c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717165"
---
# <a name="jetcreatetablecolumnindex4w-function"></a><span data-ttu-id="9fc0d-103">JetCreateTableColumnIndex4W función)</span><span class="sxs-lookup"><span data-stu-id="9fc0d-103">JetCreateTableColumnIndex4W Function</span></span>


<span data-ttu-id="9fc0d-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9fc0d-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="9fc0d-105">La función **JetCreateTableColumnIndex4W** crea una tabla en un motor de almacenamiento extensible (ese (base de datos con un conjunto inicial de índices y un conjunto inicial de columnas de una matriz de estructuras [JET_TABLECREATE3](./jet-tablecreate3-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="9fc0d-105">The **JetCreateTableColumnIndex4W** function creates a table in an Extensible Storage Engine (ESE( database with an initial set of indexes and an initial set of columns from an array of [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structures.</span></span> <span data-ttu-id="9fc0d-106">La estructura de [JET_TABLECREATE3](./jet-tablecreate3-structure.md) permite especificar una función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-106">The [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structure allows a callback function to be specified.</span></span>

<span data-ttu-id="9fc0d-107">La función **JetCreateTableColumnIndex4W** se presentó en el sistema operativo Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-107">The **JetCreateTableColumnIndex4W** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetCreateTableColumnIndex4W(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in_out      JET_TABLECREATE3* ptablecreate
);
```

### <a name="parameters"></a><span data-ttu-id="9fc0d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9fc0d-108">Parameters</span></span>

<span data-ttu-id="9fc0d-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="9fc0d-109">*sesid*</span></span>

<span data-ttu-id="9fc0d-110">Contexto de sesión de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="9fc0d-111">*DBID*</span><span class="sxs-lookup"><span data-stu-id="9fc0d-111">*dbid*</span></span>

<span data-ttu-id="9fc0d-112">Identificador de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-112">The database identifier to use for the API call.</span></span>

<span data-ttu-id="9fc0d-113">*ptablecreate*</span><span class="sxs-lookup"><span data-stu-id="9fc0d-113">*ptablecreate*</span></span>

<span data-ttu-id="9fc0d-114">Puntero a una estructura de [JET_TABLECREATE3](./jet-tablecreate3-structure.md) que define la tabla que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-114">A pointer to a [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structure that defines the table to be created.</span></span> <span data-ttu-id="9fc0d-115">Consulte [JET_TABLECREATE3](./jet-tablecreate3-structure.md) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-115">See [JET_TABLECREATE3](./jet-tablecreate3-structure.md) for more details.</span></span>

### <a name="return-value"></a><span data-ttu-id="9fc0d-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9fc0d-116">Return value</span></span>

<span data-ttu-id="9fc0d-117">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los códigos de retorno que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the return codes listed in the following table.</span></span> <span data-ttu-id="9fc0d-118">Para obtener más información sobre los posibles errores de Enginge de almacenamiento extensible (ESE), vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9fc0d-118">For more information about the possible Extensible Storage Enginge (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9fc0d-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9fc0d-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="9fc0d-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="9fc0d-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9fc0d-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="9fc0d-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="9fc0d-122">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fc0d-123">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="9fc0d-123">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="9fc0d-124">No se pudo resolver la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-124">The callback function could not be resolved.</span></span> <span data-ttu-id="9fc0d-125">Es posible que no se haya encontrado el archivo DLL o que no se haya encontrado la función del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-125">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="9fc0d-126">Con el registro suficiente habilitado, el registro de eventos proporcionará más detalles.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-126">With sufficient logging enabled, the event log will provide more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fc0d-127">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="9fc0d-127">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="9fc0d-128">Se intentó indexar sobre una columna de actualización de custodia o de SLV (tenga en cuenta que las columnas de SLV están desusadas).</span><span class="sxs-lookup"><span data-stu-id="9fc0d-128">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fc0d-129">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="9fc0d-129">JET_errCannotNestDDL</span></span></p></td>
<td><p><span data-ttu-id="9fc0d-130">Se devuelve si el parámetro <em>ptablecreate- &gt; grbit</em> especifica el valor JET_bitTableCreateTemplateTable, pero el parámetro <em>ptablecreate- &gt; szTemplateTableName</em> se establece en NULL.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-130">Returned if the <em>ptablecreate-&gt;grbit</em> parameter specifies the JET_bitTableCreateTemplateTable value, but the <em>ptablecreate-&gt;szTemplateTableName</em> parameter is set to null.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fc0d-131">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="9fc0d-131">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="9fc0d-132">Ya existe una columna.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-132">A column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fc0d-133">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="9fc0d-133">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="9fc0d-134">Se intentó indizar una columna que no existe.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-134">An attempt was made to index over a nonexistent column.</span></span> <span data-ttu-id="9fc0d-135">Un intento de indexación condicional de una columna no existente también puede generar este error.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-135">An attempt to conditionally index over a nonexistent column can also produce this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fc0d-136">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="9fc0d-136">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="9fc0d-137">Se intentó agregar una columna redundante.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-137">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="9fc0d-138">No debe existir más de una columna de incremento automático y no debe existir más de una columna de versión por tabla.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-138">No more than one autoincrement column should exist, and no more than one version column should exist per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fc0d-139">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="9fc0d-139">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="9fc0d-140">Este error se devolverá si el miembro <strong>ulDensity</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> está establecido en un número inferior a 20 o superior a 100.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-140">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to a number less than 20 or more than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fc0d-141">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="9fc0d-141">JET_errDDLNotInheritable</span></span></p></td>
<td><p><span data-ttu-id="9fc0d-142">Significa que la tabla denominada en el miembro <strong>szTemplateTableName</strong> de la estructura <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> no se marcó como tabla de plantilla (es decir, que la tabla no tenía el valor de parámetro JET_bitTableCreateTemplateTable establecido).</span><span class="sxs-lookup"><span data-stu-id="9fc0d-142">Signifies that the table named in the <strong>szTemplateTableName</strong> member of the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure was not marked as a template table (that is, that table did not have the JET_bitTableCreateTemplateTable parameter value set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fc0d-143">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="9fc0d-143">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="9fc0d-144">Se ha intentado definir dos índices idénticos.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-144">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fc0d-145">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="9fc0d-145">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="9fc0d-146">Se intentó especificar más de un índice principal para una tabla.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-146">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="9fc0d-147">Una tabla debe tener exactamente un índice principal.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-147">A table must have exactly one primary index.</span></span> <span data-ttu-id="9fc0d-148">Si no se especifica ningún índice principal, el motor de base de datos creará uno de forma transparente.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-148">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fc0d-149">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="9fc0d-149">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="9fc0d-150">Se especificó una definición de índice no válida.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-150">An invalid index definition was specified.</span></span> <span data-ttu-id="9fc0d-151">A continuación se indican algunas de las razones posibles de este error:</span><span class="sxs-lookup"><span data-stu-id="9fc0d-151">The following are some of the possible reasons for this error:</span></span></p>
<ul>
<li><p><span data-ttu-id="9fc0d-152">Un índice principal es condicional (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tiene el valor JET_bitIndexPrimary establecido y el miembro <strong>cConditionalColumn</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> es mayor que cero).</span><span class="sxs-lookup"><span data-stu-id="9fc0d-152">A primary index is conditional (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has the JET_bitIndexPrimary value set, and the <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="9fc0d-153">Se aplica a las versiones del sistema operativo Windows Server a partir de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-153">Applies to versions of the Windows Server operating system starting with Windows Server 2003.</span></span> <span data-ttu-id="9fc0d-154">Un intento de crear un índice de tupla con límites de tupla, pero sin pasar el miembro <strong>ptuplelimits</strong> en la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (es decir, el miembro <strong>grbit</strong> de la estructura <strong>JET_INDEXCREATE2</strong> tiene JET_bitIndexTupleLimits valor establecido, pero el puntero <strong>ptuplelimits</strong> es null).</span><span class="sxs-lookup"><span data-stu-id="9fc0d-154">An attempt to create a tuple index with tuple limits, but without passing the <strong>ptuplelimits</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure (that is, the <strong>grbit</strong> member of the <strong>JET_INDEXCREATE2</strong> structure has JET_bitIndexTupleLimits value set, but the <strong>ptuplelimits</strong> pointer is null).</span></span></p></li>
<li><p><span data-ttu-id="9fc0d-155">Pasando una definición de clave no válida en el miembro <strong>szKey</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="9fc0d-155">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="9fc0d-156">Para obtener información sobre las definiciones válidas, vea <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-156">For information about valid definitions, see <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</span></span></p></li>
<li><p><span data-ttu-id="9fc0d-157">Establecer el miembro <strong>cbVarSegMac</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> para que sea mayor que el valor JET_cbPrimaryKeyMost (para un índice principal) o mayor que el valor JET_cbSecondaryKeyMost (para un índice secundario).</span><span class="sxs-lookup"><span data-stu-id="9fc0d-157">Setting the <strong>cbVarSegMac</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> to be greater than the JET_cbPrimaryKeyMost value (for a primary index) or greater than the JET_cbSecondaryKeyMost value (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="9fc0d-158">Pasar una combinación no válida para un índice Unicode definido por el usuario (uno que tiene el bit de valor JET_bitIndexUnicode establecido en el miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span><span class="sxs-lookup"><span data-stu-id="9fc0d-158">Passing an invalid combination for a user-defined Unicode index (one that has the JET_bitIndexUnicode value bit set in the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span> <span data-ttu-id="9fc0d-159">Algunas causas comunes incluyen el miembro <strong>pidxunicode</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> es null o el LCID especificado en la estructura <strong>pidxunicode</strong> no es válido.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-159">Some common causes include the <strong>pidxunicode</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is null, or the LCID specified in the <strong>pidxunicode</strong> structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="9fc0d-160">Especificar una columna multivalor para un índice principal.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-160">Specifying a multivalued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="9fc0d-161">Intentando indexar demasiadas columnas condicionales.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-161">Trying to index too many conditional columns.</span></span> <span data-ttu-id="9fc0d-162">El miembro <strong>cConditionalColumn</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> no debe ser mayor que <strong>JET_ccolKeyMost</strong>.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-162">The <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not be greater than <strong>JET_ccolKeyMost</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fc0d-163">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="9fc0d-163">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="9fc0d-164">Se aplica a las versiones de Windows a partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-164">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="9fc0d-165">Se especificó una estructura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> y no se admiten sus límites.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-165">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="9fc0d-166">Para obtener más información, vea la sección Comentarios de la estructura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="9fc0d-166">For more information, see the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fc0d-167">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="9fc0d-167">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="9fc0d-168">Se aplica a las versiones de Windows a partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-168">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="9fc0d-169">Un índice de tupla no puede ser único (es decir, el miembro <em>grbit</em> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> no debe tener establecidos los valores JET_bitIndexPrimary y JET_bitIndexUnique).</span><span class="sxs-lookup"><span data-stu-id="9fc0d-169">A tuple index cannot be unique (that is, the <em>grbit</em> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexUnique values set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fc0d-170">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="9fc0d-170">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="9fc0d-171">Se aplica a las versiones de Windows a partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-171">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="9fc0d-172">Un índice de tupla solo puede estar en una sola columna (es decir, si el miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tiene JET_bitIndexTuples valor establecido y el miembro <strong>szKey</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> especifica más de una columna).</span><span class="sxs-lookup"><span data-stu-id="9fc0d-172">A tuple index can only be over a single column (that is, if the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexTuples value set, and the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fc0d-173">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="9fc0d-173">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="9fc0d-174">Se aplica a las versiones de Windows a partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-174">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="9fc0d-175">Un índice de tupla no puede ser un índice principal (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> no debe tener establecido JET_bitIndexPrimary y JET_bitIndexTuples).</span><span class="sxs-lookup"><span data-stu-id="9fc0d-175">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fc0d-176">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="9fc0d-176">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="9fc0d-177">Se aplica a las versiones de Windows a partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-177">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="9fc0d-178">Un índice de tupla solo puede estar en una columna de texto o Unicode.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-178">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="9fc0d-179">Un intento de indizar otras columnas (como columnas binarias) producirá un código de respuesta JET_errIndexTuplesTextColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-179">An attempt to index other columns (such as binary columns) will result in a JET_errIndexTuplesTextColumnsOnly response code.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fc0d-180">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="9fc0d-180">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="9fc0d-181">Se aplica a las versiones de Windows a partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-181">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="9fc0d-182">Un índice de tupla no permite establecer el miembro <strong>cbVarSegMac</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="9fc0d-182">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure to be set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fc0d-183">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="9fc0d-183">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="9fc0d-184">Se intentó crear un índice sin información de versión mientras estaba en una transacción.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-184">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fc0d-185">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="9fc0d-185">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="9fc0d-186">El miembro <strong>CP</strong> de la estructura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> no se ha establecido en una página de códigos válida.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-186">The <strong>cp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="9fc0d-187">Los únicos valores válidos para las columnas de texto son inglés (1252) y Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="9fc0d-187">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="9fc0d-188">Un valor de 0 significa que se usará el valor predeterminado (Inglés, 1252).</span><span class="sxs-lookup"><span data-stu-id="9fc0d-188">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fc0d-189">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="9fc0d-189">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="9fc0d-190">El miembro <strong>coltyp</strong> de la estructura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> no se ha establecido en un tipo de columna válido.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-190">The <strong>coltyp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fc0d-191">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="9fc0d-191">JET_errInvalidCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="9fc0d-192">A continuación se indican algunos de los motivos por los que puede producirse este error:</span><span class="sxs-lookup"><span data-stu-id="9fc0d-192">The following are some reasons why this error may occur:</span></span></p>
<ul>
<li><p><span data-ttu-id="9fc0d-193">El miembro <strong>rgindexcreate</strong> de la estructura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> se estableció en NULL.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-193">The <strong>rgindexcreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to null.</span></span></p></li>
<li><p><span data-ttu-id="9fc0d-194">El miembro <strong>rgcolumncreate</strong> de la estructura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> se estableció en NULL.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-194">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to null.</span></span></p></li>
<li><p><span data-ttu-id="9fc0d-195">El miembro <strong>cbStruct</strong> de una estructura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> no se ha establecido en un valor válido.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-195">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure was not set to a valid value.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fc0d-196">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="9fc0d-196">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="9fc0d-197">Se especificó una combinación no válida de miembros <strong>grbit</strong> en la estructura <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> .</span><span class="sxs-lookup"><span data-stu-id="9fc0d-197">An invalid combination of <strong>grbit</strong> members was specified in the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure.</span></span></p>
<p><span data-ttu-id="9fc0d-198">La definición del índice no es válida porque el miembro <strong>grbit</strong> contiene valores incoherentes.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-198">The index definition is invalid because the <strong>grbit</strong> member contains inconsistent values.</span></span> <span data-ttu-id="9fc0d-199">A continuación se indican algunas razones posibles:</span><span class="sxs-lookup"><span data-stu-id="9fc0d-199">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="9fc0d-200">Un índice principal tenía un bit ignore especificado (es decir, JET_bitIndexPrimary valor se pasó con los valores JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull o JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="9fc0d-200">A primary index had an ignore bit specified (that is, JET_bitIndexPrimary value was passed with the JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull values).</span></span></p></li>
<li><p><span data-ttu-id="9fc0d-201">Un índice vacío no omite ningún miembro nulo (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tiene el valor JET_bitIndexEmpty establecido, pero no tiene JET_bitIndexIgnoreAnyNull valor establecido).</span><span class="sxs-lookup"><span data-stu-id="9fc0d-201">An empty index does not ignore any null members (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has the JET_bitIndexEmpty value set, but does not have JET_bitIndexIgnoreAnyNull value set).</span></span></p></li>
<li><p><span data-ttu-id="9fc0d-202">Pasando una estructura de <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> con un miembro <strong>grbit</strong> no válido.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-202">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fc0d-203">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="9fc0d-203">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="9fc0d-204">Se pasó un ID. de configuración regional (LCID) no válido (ya sea a través del miembro <strong>LCID</strong> de la estructura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> a la que apunta el miembro <strong>pidxunicode</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> , o a través del campo <strong>LCID</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span><span class="sxs-lookup"><span data-stu-id="9fc0d-204">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member of the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure that the <strong>pidxunicode</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure points to, or through the <strong>lcid</strong> field of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fc0d-205">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="9fc0d-205">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="9fc0d-206">Se proporcionó un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-206">An invalid parameter was given.</span></span> <span data-ttu-id="9fc0d-207">A continuación se indican algunas razones posibles:</span><span class="sxs-lookup"><span data-stu-id="9fc0d-207">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="9fc0d-208">El miembro <strong>rgcolumncreate</strong> de la estructura <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> es NULL.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-208">The <strong>rgcolumncreate</strong> member of the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure is null.</span></span></p></li>
<li><p><span data-ttu-id="9fc0d-209">El miembro <strong>cbStruct</strong> de una de las estructuras <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> proporcionadas en el miembro <strong>rgcolumncreate</strong> de la estructura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> no se estableció en sizeof (JET_COLUMNCREATE).</span><span class="sxs-lookup"><span data-stu-id="9fc0d-209">The <strong>cbStruct</strong> member of one of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structures given in the <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was not set to sizeof( JET_COLUMNCREATE ).</span></span></p></li>
<li><p><span data-ttu-id="9fc0d-210">El miembro <strong>cbKey</strong> de una estructura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-210">The <strong>cbKey</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="9fc0d-211">El miembro <strong>cbStruct</strong> de una estructura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> no se establece en sizeof (JET_INDEXCREATE2).</span><span class="sxs-lookup"><span data-stu-id="9fc0d-211">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is not set to sizeof( JET_INDEXCREATE2 ).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fc0d-212">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="9fc0d-212">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="9fc0d-213">El registro es demasiado grande.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-213">The record is too big.</span></span> <span data-ttu-id="9fc0d-214">La suma del miembro <strong>cbMax</strong> de la estructura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> para todas las columnas fijas no debe superar un valor determinado.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-214">The sum of the <strong>cbMax</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure for all fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fc0d-215">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="9fc0d-215">JET_errTableDuplicate</span></span></p></td>
<td><p><span data-ttu-id="9fc0d-216">La tabla ya existe.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-216">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fc0d-217">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="9fc0d-217">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="9fc0d-218">Se intentó agregar demasiadas columnas a la tabla.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-218">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="9fc0d-219">Una tabla no puede tener más de <strong>JET_ccolFixedMost</strong> columnas fijas, ni más de <strong>JET_ccolVarMost</strong> columnas de longitud variable, ni más de <strong>JET_ccolTaggedMost</strong> columnas etiquetadas.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-219">A table can have no more than <strong>JET_ccolFixedMost</strong> fixed columns, no more than <strong>JET_ccolVarMost</strong> variable-length columns, and no more than <strong>JET_ccolTaggedMost</strong> tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fc0d-220">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="9fc0d-220">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="9fc0d-221">Se produjo un error cuando se intentó normalizar una columna Unicode.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-221">An error occurred when an attempt was made to normalize a Unicode column.</span></span> <span data-ttu-id="9fc0d-222">Esto puede deberse a la falta de recursos del sistema.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-222">This can be caused by running out of system resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fc0d-223">JET_errSpaceHintsInvalid</span><span class="sxs-lookup"><span data-stu-id="9fc0d-223">JET_errSpaceHintsInvalid</span></span></p></td>
<td><p><span data-ttu-id="9fc0d-224">Un elemento de la estructura de sugerencias de espacio JET no era correcto o accionable.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-224">An element of the JET space hints structure was not correct or actionable.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="9fc0d-225">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9fc0d-225">Remarks</span></span>

<span data-ttu-id="9fc0d-226">La función **JetCreateTableColumnIndex4W** crea una tabla con un conjunto inicial de columnas e índices.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-226">The **JetCreateTableColumnIndex4W** function creates a table with an initial set of columns and indexes.</span></span> <span data-ttu-id="9fc0d-227">Las columnas e índices adicionales se pueden agregar y quitar dinámicamente por medio de las funciones [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md), [JetCreateIndex4W](./jetcreateindex4w-function.md)y [JetDeleteIndex](./jetdeleteindex-function.md) .</span><span class="sxs-lookup"><span data-stu-id="9fc0d-227">Additional columns and indexes can be added and removed dynamically by means of the [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md), [JetCreateIndex4W](./jetcreateindex4w-function.md), and [JetDeleteIndex](./jetdeleteindex-function.md) functions.</span></span>

<span data-ttu-id="9fc0d-228">Al igual que con la función [JetOpenTable](./jetopentable-function.md) , cuando la aplicación se realiza utilizando el ID *. de la devolución,* la función [JetCloseTable](./jetclosetable-function.md) debe cerrar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-228">As with the [JetOpenTable](./jetopentable-function.md) function, when the application is done using the returned *tableid*, the [JetCloseTable](./jetclosetable-function.md) function should close the application.</span></span>

#### <a name="requirements"></a><span data-ttu-id="9fc0d-229">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fc0d-229">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9fc0d-230"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="9fc0d-230"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9fc0d-231">Requiere Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-231">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fc0d-232"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9fc0d-232"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9fc0d-233">Requiere Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-233">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fc0d-234"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="9fc0d-234"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9fc0d-235">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-235">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fc0d-236"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="9fc0d-236"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9fc0d-237">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-237">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fc0d-238"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="9fc0d-238"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9fc0d-239">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-239">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9fc0d-240">Vea también</span><span class="sxs-lookup"><span data-stu-id="9fc0d-240">See also</span></span>

[<span data-ttu-id="9fc0d-241">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="9fc0d-241">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="9fc0d-242">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="9fc0d-242">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="9fc0d-243">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9fc0d-243">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9fc0d-244">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="9fc0d-244">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="9fc0d-245">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="9fc0d-245">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="9fc0d-246">JET_INDEXCREATE2</span><span class="sxs-lookup"><span data-stu-id="9fc0d-246">JET_INDEXCREATE2</span></span>](./jet-indexcreate2-structure.md)  
[<span data-ttu-id="9fc0d-247">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9fc0d-247">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="9fc0d-248">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="9fc0d-248">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="9fc0d-249">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="9fc0d-249">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="9fc0d-250">JET_TABLECREATE3</span><span class="sxs-lookup"><span data-stu-id="9fc0d-250">JET_TABLECREATE3</span></span>](./jet-tablecreate3-structure.md)  
[<span data-ttu-id="9fc0d-251">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="9fc0d-251">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="9fc0d-252">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="9fc0d-252">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="9fc0d-253">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="9fc0d-253">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="9fc0d-254">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="9fc0d-254">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="9fc0d-255">JetCreateIndex3</span><span class="sxs-lookup"><span data-stu-id="9fc0d-255">JetCreateIndex3</span></span>](./jetcreateindex3-function.md)  
[<span data-ttu-id="9fc0d-256">JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="9fc0d-256">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="9fc0d-257">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="9fc0d-257">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="9fc0d-258">JetDeleteColumn</span><span class="sxs-lookup"><span data-stu-id="9fc0d-258">JetDeleteColumn</span></span>](./jetdeletecolumn-function.md)  
[<span data-ttu-id="9fc0d-259">JetDeleteColumn2</span><span class="sxs-lookup"><span data-stu-id="9fc0d-259">JetDeleteColumn2</span></span>](./jetdeletecolumn2-function.md)
