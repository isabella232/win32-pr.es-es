---
description: 'Más información acerca de: JetCreateTableColumnIndex2 (función)'
title: JetCreateTableColumnIndex2 función)
TOCTitle: JetCreateTableColumnIndex2 Function
ms:assetid: ad9caaf3-8cd2-453f-894d-8ac438c50b73
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294057(v=EXCHG.10)
ms:contentKeyID: 32765672
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableColumnIndex2W
- JetCreateTableColumnIndex2
- JetCreateTableColumnIndex2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 51a1789fe050ddd62990f6561ddeb01363d69f6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083455"
---
# <a name="jetcreatetablecolumnindex2-function"></a><span data-ttu-id="1c08f-103">JetCreateTableColumnIndex2 función)</span><span class="sxs-lookup"><span data-stu-id="1c08f-103">JetCreateTableColumnIndex2 Function</span></span>


<span data-ttu-id="1c08f-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1c08f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatetablecolumnindex2-function"></a><span data-ttu-id="1c08f-105">JetCreateTableColumnIndex2 función)</span><span class="sxs-lookup"><span data-stu-id="1c08f-105">JetCreateTableColumnIndex2 Function</span></span>

<span data-ttu-id="1c08f-106">La función **JetCreateTableColumnIndex2** crea una tabla en una base de datos de ese con un conjunto inicial de índices y un conjunto inicial de columnas de una matriz de estructuras [JET_TABLECREATE2](./jet-tablecreate2-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="1c08f-106">The **JetCreateTableColumnIndex2** function creates a table in an ESE database with an initial set of indexes and an initial set of columns from an array of [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structures.</span></span> <span data-ttu-id="1c08f-107">La estructura de [JET_TABLECREATE2](./jet-tablecreate2-structure.md) permite especificar una función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="1c08f-107">The [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structure allows a callback function to be specified.</span></span>

<span data-ttu-id="1c08f-108">**Windows XP: JetCreateTableColumnIndex2** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1c08f-108">**Windows XP:  JetCreateTableColumnIndex2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetCreateTableColumnIndex2(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in_out      JET_TABLECREATE2* ptablecreate
    );
```

### <a name="parameters"></a><span data-ttu-id="1c08f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1c08f-109">Parameters</span></span>

<span data-ttu-id="1c08f-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="1c08f-110">*sesid*</span></span>

<span data-ttu-id="1c08f-111">Contexto de sesión de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="1c08f-111">The database session context to use for the API call.</span></span>

<span data-ttu-id="1c08f-112">*DBID*</span><span class="sxs-lookup"><span data-stu-id="1c08f-112">*dbid*</span></span>

<span data-ttu-id="1c08f-113">Identificador de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="1c08f-113">The database identifier to use for the API call.</span></span>

<span data-ttu-id="1c08f-114">*ptablecreate*</span><span class="sxs-lookup"><span data-stu-id="1c08f-114">*ptablecreate*</span></span>

<span data-ttu-id="1c08f-115">Puntero a una estructura de [JET_TABLECREATE2](./jet-tablecreate2-structure.md) que define la tabla que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="1c08f-115">A pointer to a [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structure which defines the table to be created.</span></span> <span data-ttu-id="1c08f-116">Consulte [JET_TABLECREATE2](./jet-tablecreate2-structure.md) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="1c08f-116">See [JET_TABLECREATE2](./jet-tablecreate2-structure.md) for more details.</span></span>

### <a name="return-value"></a><span data-ttu-id="1c08f-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1c08f-117">Return Value</span></span>

<span data-ttu-id="1c08f-118">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="1c08f-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="1c08f-119">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1c08f-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1c08f-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1c08f-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="1c08f-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c08f-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c08f-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="1c08f-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="1c08f-123">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="1c08f-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c08f-124">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="1c08f-124">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="1c08f-125">No se pudo resolver la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="1c08f-125">The callback function could not be resolved.</span></span> <span data-ttu-id="1c08f-126">Es posible que no se haya encontrado el archivo DLL o que no se haya encontrado la función del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="1c08f-126">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="1c08f-127">Con el registro suficiente habilitado, el registro de eventos proporcionará más detalles.</span><span class="sxs-lookup"><span data-stu-id="1c08f-127">With sufficient logging enabled, the event log will provide more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c08f-128">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="1c08f-128">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="1c08f-129">Se intentó indexar sobre una columna de actualización de custodia o de SLV (tenga en cuenta que las columnas de SLV están desusadas).</span><span class="sxs-lookup"><span data-stu-id="1c08f-129">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c08f-130">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="1c08f-130">JET_errCannotNestDDL</span></span></p></td>
<td><p><span data-ttu-id="1c08f-131">Si ptablecreate- &gt; grbit especifica JET_bitTableCreateTemplateTable, pero ptablecreate- &gt; szTemplateTableName se establece en NULL.</span><span class="sxs-lookup"><span data-stu-id="1c08f-131">If ptablecreate-&gt;grbit specifies JET_bitTableCreateTemplateTable, but ptablecreate-&gt;szTemplateTableName is set to NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c08f-132">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="1c08f-132">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="1c08f-133">Ya existe una columna.</span><span class="sxs-lookup"><span data-stu-id="1c08f-133">A column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c08f-134">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="1c08f-134">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="1c08f-135">Se intentó indizar una columna que no existe.</span><span class="sxs-lookup"><span data-stu-id="1c08f-135">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="1c08f-136">El intento de indizar condicionalmente en una columna que no existe también puede generar este error.</span><span class="sxs-lookup"><span data-stu-id="1c08f-136">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c08f-137">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="1c08f-137">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="1c08f-138">Se intentó agregar una columna redundante.</span><span class="sxs-lookup"><span data-stu-id="1c08f-138">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="1c08f-139">No debe haber más de una columna de incremento automático y no más de una columna de versión por tabla.</span><span class="sxs-lookup"><span data-stu-id="1c08f-139">There should be no more than one autoincrement column, and no more than one version column per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c08f-140">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="1c08f-140">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="1c08f-141">Este error se devolverá si el miembro <strong>ulDensity</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> está establecido en un número inferior a 20 o superior a 100.</span><span class="sxs-lookup"><span data-stu-id="1c08f-141">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to a number less than 20 or more than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c08f-142">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="1c08f-142">JET_errDDLNotInheritable</span></span></p></td>
<td><p><span data-ttu-id="1c08f-143">Significa que la tabla denominada en el miembro <strong>szTemplateTableName</strong> de la estructura <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> no era una marca marcada como tabla de plantilla (es decir, que la tabla no tenía JET_bitTableCreateTemplateTable establecido).</span><span class="sxs-lookup"><span data-stu-id="1c08f-143">Signifies that the table named in the <strong>szTemplateTableName</strong> member of the <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> structure was not a marked as a template table (that is, that table did not have JET_bitTableCreateTemplateTable set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c08f-144">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="1c08f-144">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="1c08f-145">Se ha intentado definir dos índices idénticos.</span><span class="sxs-lookup"><span data-stu-id="1c08f-145">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c08f-146">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="1c08f-146">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="1c08f-147">Se intentó especificar más de un índice principal para una tabla.</span><span class="sxs-lookup"><span data-stu-id="1c08f-147">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="1c08f-148">Una tabla debe tener exactamente un índice principal.</span><span class="sxs-lookup"><span data-stu-id="1c08f-148">A table must have exactly one primary index.</span></span> <span data-ttu-id="1c08f-149">Si no se especifica ningún índice principal, el motor de base de datos creará uno de forma transparente.</span><span class="sxs-lookup"><span data-stu-id="1c08f-149">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c08f-150">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="1c08f-150">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="1c08f-151">Se especificó una definición de índice no válida.</span><span class="sxs-lookup"><span data-stu-id="1c08f-151">An invalid index definition was specified.</span></span> <span data-ttu-id="1c08f-152">Algunas de las posibles razones para recibir este error son:</span><span class="sxs-lookup"><span data-stu-id="1c08f-152">Some of the possible reasons for receiving this error are:</span></span></p>
<ul>
<li><p><span data-ttu-id="1c08f-153">Un índice principal es condicional (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiene JET_bitIndexPrimary establecido y el miembro <strong>cConditionalColumn</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> es mayor que cero).</span><span class="sxs-lookup"><span data-stu-id="1c08f-153">A primary index is conditional (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexPrimary set, and <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="1c08f-154">Windows Server 2003 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="1c08f-154">Windows Server 2003 and later.</span></span> <span data-ttu-id="1c08f-155">Se ha intentado crear un índice de tupla con límites de tupla, pero sin pasar el miembro <strong>ptuplelimits</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiene JET_BITINDEXTUPLELIMITS establecido, pero el puntero <strong>ptuplelimits</strong> es null).</span><span class="sxs-lookup"><span data-stu-id="1c08f-155">Attempting to create a tuple index with tuple limits, but without passing the <strong>ptuplelimits</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="1c08f-156">Pasando una definición de clave no válida en el miembro <strong>szKey</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="1c08f-156">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="1c08f-157">Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener una descripción de las definiciones válidas.</span><span class="sxs-lookup"><span data-stu-id="1c08f-157">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="1c08f-158">Establecer el miembro <strong>cbVarSegMac</strong> de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para que sea mayor que JET_cbPrimaryKeyMost (para un índice principal) o mayor que JET_cbSecondaryKeyMost (para un índice secundario).</span><span class="sxs-lookup"><span data-stu-id="1c08f-158">Setting the <strong>cbVarSegMac</strong> member in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="1c08f-159">Pasar una combinación no válida para un índice Unicode definido por el usuario (uno que tiene el bit de JET_bitIndexUnicode establecido en el miembro <strong>grbit</strong> de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span><span class="sxs-lookup"><span data-stu-id="1c08f-159">Passing an invalid combination for a user-defined Unicode index (one which has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span></span> <span data-ttu-id="1c08f-160">Algunas causas comunes incluyen el miembro <strong>pidxunicode</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> es null o el LCID especificado en la estructura <strong>pidxunicode</strong> no es válido.</span><span class="sxs-lookup"><span data-stu-id="1c08f-160">Some common causes include the <strong>pidxunicode</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is NULL, or the LCID specified in the <strong>pidxunicode</strong> structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="1c08f-161">Especificar una columna de varios valores para un índice principal.</span><span class="sxs-lookup"><span data-stu-id="1c08f-161">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="1c08f-162">Intentando indexar demasiadas columnas condicionales.</span><span class="sxs-lookup"><span data-stu-id="1c08f-162">Trying to index too many conditional columns.</span></span> <span data-ttu-id="1c08f-163">El miembro <strong>cConditionalColumn</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> no debe ser mayor que JET_ccolKeyMost.</span><span class="sxs-lookup"><span data-stu-id="1c08f-163">The <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c08f-164">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="1c08f-164">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="1c08f-165">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="1c08f-165">Windows XP and later.</span></span> <span data-ttu-id="1c08f-166">Se especificó una estructura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> y no se admiten sus límites.</span><span class="sxs-lookup"><span data-stu-id="1c08f-166">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="1c08f-167">Vea la sección Comentarios de la estructura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="1c08f-167">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c08f-168">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="1c08f-168">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="1c08f-169">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="1c08f-169">Windows XP and later.</span></span> <span data-ttu-id="1c08f-170">Un índice de tupla no puede ser único (es decir, el miembro <em>grbit</em> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> no debe tener establecido JET_bitIndexPrimary y JET_bitIndexUnique).</span><span class="sxs-lookup"><span data-stu-id="1c08f-170">A tuple index cannot be unique (that is, the <em>grbit</em> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c08f-171">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="1c08f-171">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="1c08f-172">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="1c08f-172">Windows XP and later.</span></span> <span data-ttu-id="1c08f-173">Un índice de tupla solo puede estar en una sola columna (es decir, si el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiene JET_bitIndexTuples establecido y el miembro <strong>szKey</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> especifica más de una columna).</span><span class="sxs-lookup"><span data-stu-id="1c08f-173">A tuple index can only be over a single column (that is, if the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c08f-174">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="1c08f-174">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="1c08f-175">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="1c08f-175">Windows XP and later.</span></span> <span data-ttu-id="1c08f-176">Un índice de tupla no puede ser un índice principal (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> no debe tener establecido JET_bitIndexPrimary y JET_bitIndexTuples).</span><span class="sxs-lookup"><span data-stu-id="1c08f-176">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c08f-177">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="1c08f-177">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="1c08f-178">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="1c08f-178">Windows XP and later.</span></span> <span data-ttu-id="1c08f-179">Un índice de tupla solo puede estar en una columna de texto o Unicode.</span><span class="sxs-lookup"><span data-stu-id="1c08f-179">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="1c08f-180">Un intento de indizar otras columnas (como columnas binarias) dará como resultado JET_errIndexTuplesTextColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="1c08f-180">An attempt to index other columns (such as binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c08f-181">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="1c08f-181">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="1c08f-182">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="1c08f-182">Windows XP and later.</span></span> <span data-ttu-id="1c08f-183">Un índice de tupla no permite establecer el miembro <strong>cbVarSegMac</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="1c08f-183">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure to be set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c08f-184">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="1c08f-184">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="1c08f-185">Se intentó crear un índice sin información de versión mientras estaba en una transacción.</span><span class="sxs-lookup"><span data-stu-id="1c08f-185">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c08f-186">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="1c08f-186">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="1c08f-187">El miembro <strong>CP</strong> de la estructura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> no se ha establecido en una página de códigos válida.</span><span class="sxs-lookup"><span data-stu-id="1c08f-187">The <strong>cp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="1c08f-188">Los únicos valores válidos para las columnas de texto son inglés (1252) y Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="1c08f-188">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="1c08f-189">Un valor de 0 significa que se usará el valor predeterminado (Inglés, 1252).</span><span class="sxs-lookup"><span data-stu-id="1c08f-189">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c08f-190">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="1c08f-190">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="1c08f-191">El miembro <strong>coltyp</strong> de la estructura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> no se ha establecido en un tipo de columna válido.</span><span class="sxs-lookup"><span data-stu-id="1c08f-191">The <strong>coltyp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c08f-192">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="1c08f-192">JET_errInvalidCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="1c08f-193">Algunas de las razones por las que puede producirse este error:</span><span class="sxs-lookup"><span data-stu-id="1c08f-193">Some of the reasons this error may occur:</span></span></p>
<ul>
<li><p><span data-ttu-id="1c08f-194">El miembro <strong>rgindexcreate</strong> de la estructura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> se estableció en NULL.</span><span class="sxs-lookup"><span data-stu-id="1c08f-194">The <strong>rgindexcreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="1c08f-195">El miembro <strong>rgcolumncreate</strong> de la estructura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> se estableció en NULL.</span><span class="sxs-lookup"><span data-stu-id="1c08f-195">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="1c08f-196">El miembro <strong>cbStruct</strong> de una estructura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> no se ha establecido en un valor válido.</span><span class="sxs-lookup"><span data-stu-id="1c08f-196">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure was not set to a valid value.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c08f-197">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="1c08f-197">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="1c08f-198">Se especificó una combinación no válida de miembros de <strong>grbit</strong> en <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>.</span><span class="sxs-lookup"><span data-stu-id="1c08f-198">An invalid combination of <strong>grbit</strong> members was specified in <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>.</span></span></p>
<p><span data-ttu-id="1c08f-199">La definición del índice no es válida porque el miembro <strong>grbit</strong> contiene valores incoherentes.</span><span class="sxs-lookup"><span data-stu-id="1c08f-199">The index definition is invalid because the <strong>grbit</strong> member contains inconsistent values.</span></span> <span data-ttu-id="1c08f-200">Algunas de las razones posibles son:</span><span class="sxs-lookup"><span data-stu-id="1c08f-200">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="1c08f-201">Un índice principal tenía un bit ignore especificado (es decir, JET_bitIndexPrimary se pasó con JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull o JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="1c08f-201">A primary index had an ignore bit specified (that is, JET_bitIndexPrimary was passed with JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="1c08f-202">Un índice vacío no omite ningún miembro nulo (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiene JET_bitIndexEmpty establecido, pero no tiene JET_bitIndexIgnoreAnyNull establecida).</span><span class="sxs-lookup"><span data-stu-id="1c08f-202">An empty index does not ignore any NULL members (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="1c08f-203">Pasando una estructura de <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> con un miembro <strong>grbit</strong> no válido.</span><span class="sxs-lookup"><span data-stu-id="1c08f-203">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c08f-204">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="1c08f-204">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="1c08f-205">Se pasó un ID. de configuración regional (LCID) no válido (ya sea a través del miembro <strong>LCID</strong> de la estructura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> a la que apunta el miembro <strong>pidxunicode</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> , o a través del campo <strong>LCID</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</span><span class="sxs-lookup"><span data-stu-id="1c08f-205">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member of the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure which is pointed to by the <strong>pidxunicode</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure, or through the <strong>lcid</strong> field of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c08f-206">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="1c08f-206">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="1c08f-207">Se proporcionó un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="1c08f-207">An invalid parameter was given.</span></span> <span data-ttu-id="1c08f-208">Algunas de las razones posibles son:</span><span class="sxs-lookup"><span data-stu-id="1c08f-208">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="1c08f-209">El miembro <strong>rgcolumncreate</strong> de la estructura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> es NULL.</span><span class="sxs-lookup"><span data-stu-id="1c08f-209">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure is NULL.</span></span></p></li>
<li><p><span data-ttu-id="1c08f-210">El miembro <strong>cbStruct</strong> de una de las estructuras <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> proporcionadas en el miembro <strong>rgcolumncreate</strong> de la estructura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> no se estableció en sizeof (JET_COLUMNCREATE).</span><span class="sxs-lookup"><span data-stu-id="1c08f-210">The <strong>cbStruct</strong> member of one of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structures given in the <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was not set to sizeof( JET_COLUMNCREATE ).</span></span></p></li>
<li><p><span data-ttu-id="1c08f-211">El miembro <strong>cbKey</strong> de una estructura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="1c08f-211">The <strong>cbKey</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="1c08f-212">El miembro <strong>cbStruct</strong> de una estructura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> no se establece en sizeof (JET_INDEXCREATE).</span><span class="sxs-lookup"><span data-stu-id="1c08f-212">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is not set to sizeof( JET_INDEXCREATE ).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c08f-213">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="1c08f-213">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="1c08f-214">El registro es demasiado grande.</span><span class="sxs-lookup"><span data-stu-id="1c08f-214">The record is too big.</span></span> <span data-ttu-id="1c08f-215">La suma del miembro <strong>cbMax</strong> de la estructura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> para todas las columnas fijas no debe superar un valor determinado.</span><span class="sxs-lookup"><span data-stu-id="1c08f-215">The sum of the <strong>cbMax</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure for all fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c08f-216">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="1c08f-216">JET_errTableDuplicate</span></span></p></td>
<td><p><span data-ttu-id="1c08f-217">La tabla ya existe.</span><span class="sxs-lookup"><span data-stu-id="1c08f-217">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c08f-218">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="1c08f-218">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="1c08f-219">Se intentó agregar demasiadas columnas a la tabla.</span><span class="sxs-lookup"><span data-stu-id="1c08f-219">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="1c08f-220">Una tabla no puede tener más de JET_ccolFixedMost columnas fijas, ni más de JET_ccolVarMost columnas de longitud variable, ni más de JET_ccolTaggedMost columnas etiquetadas.</span><span class="sxs-lookup"><span data-stu-id="1c08f-220">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c08f-221">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="1c08f-221">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="1c08f-222">Error al intentar normalizar una columna Unicode.</span><span class="sxs-lookup"><span data-stu-id="1c08f-222">An error occurred attempting to normalize a Unicode column.</span></span> <span data-ttu-id="1c08f-223">Esto puede deberse a la falta de recursos del sistema.</span><span class="sxs-lookup"><span data-stu-id="1c08f-223">This can be caused by running out of system resources.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="1c08f-224">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1c08f-224">Remarks</span></span>

<span data-ttu-id="1c08f-225">El nombre **JetCreateTableColumnIndex2** procede del orden de creación de los objetos: primero crea una tabla, columnas y, finalmente, índices.</span><span class="sxs-lookup"><span data-stu-id="1c08f-225">The name **JetCreateTableColumnIndex2** comes from the order of creation of the objects: It first creates a table, columns, and then finally indexes.</span></span> <span data-ttu-id="1c08f-226">**JetCreateTableColumnIndex2** crea una tabla con un conjunto inicial de columnas e índices.</span><span class="sxs-lookup"><span data-stu-id="1c08f-226">**JetCreateTableColumnIndex2** creates a table with an initial set of columns and indexes.</span></span> <span data-ttu-id="1c08f-227">Las columnas e índices adicionales se pueden agregar y quitar dinámicamente con [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md)y [JetDeleteIndex](./jetdeleteindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="1c08f-227">Additional columns and indexes can be added and removed dynamically with [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), and [JetDeleteIndex](./jetdeleteindex-function.md).</span></span>

<span data-ttu-id="1c08f-228">Al igual que [JetOpenTable](./jetopentable-function.md), cuando la aplicación se realiza utilizando el ID *. de tipo devuelto,* normalmente se debe cerrar con [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="1c08f-228">Like [JetOpenTable](./jetopentable-function.md), when the application is done using the returned *tableid*, it should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="1c08f-229">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c08f-229">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c08f-230"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="1c08f-230"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1c08f-231">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1c08f-231">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c08f-232"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="1c08f-232"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1c08f-233">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1c08f-233">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c08f-234"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="1c08f-234"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1c08f-235">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="1c08f-235">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c08f-236"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="1c08f-236"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1c08f-237">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="1c08f-237">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c08f-238"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="1c08f-238"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1c08f-239">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="1c08f-239">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c08f-240"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="1c08f-240"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="1c08f-241">Se implementa como <strong>JetCreateTableColumnIndex2W</strong> (Unicode) y <strong>JetCreateTableColumnIndex2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="1c08f-241">Implemented as <strong>JetCreateTableColumnIndex2W</strong> (Unicode) and <strong>JetCreateTableColumnIndex2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="1c08f-242">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1c08f-242">See Also</span></span>

[<span data-ttu-id="1c08f-243">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="1c08f-243">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="1c08f-244">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="1c08f-244">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="1c08f-245">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1c08f-245">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1c08f-246">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="1c08f-246">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="1c08f-247">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="1c08f-247">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="1c08f-248">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="1c08f-248">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="1c08f-249">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="1c08f-249">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="1c08f-250">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="1c08f-250">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="1c08f-251">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="1c08f-251">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="1c08f-252">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="1c08f-252">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="1c08f-253">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="1c08f-253">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="1c08f-254">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="1c08f-254">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="1c08f-255">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="1c08f-255">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="1c08f-256">JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="1c08f-256">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="1c08f-257">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="1c08f-257">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="1c08f-258">JetDeleteColumn</span><span class="sxs-lookup"><span data-stu-id="1c08f-258">JetDeleteColumn</span></span>](./jetdeletecolumn-function.md)  
[<span data-ttu-id="1c08f-259">JetDeleteColumn2</span><span class="sxs-lookup"><span data-stu-id="1c08f-259">JetDeleteColumn2</span></span>](./jetdeletecolumn2-function.md)
