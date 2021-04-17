---
description: 'Más información acerca de: JetCreateTable (función)'
title: Función JetCreateTable
TOCTitle: JetCreateTable Function
ms:assetid: 28455b8b-0000-4bd5-a3ca-e1ef0446ee07
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269210(v=EXCHG.10)
ms:contentKeyID: 32765513
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableW
- JetCreateTable
- JetCreateTableA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6f385cfd668af934bfde2669277db7ed048a1fa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717166"
---
# <a name="jetcreatetable-function"></a><span data-ttu-id="75b81-103">Función JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="75b81-103">JetCreateTable Function</span></span>


<span data-ttu-id="75b81-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="75b81-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatetable-function"></a><span data-ttu-id="75b81-105">Función JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="75b81-105">JetCreateTable Function</span></span>

<span data-ttu-id="75b81-106">La función **JetCreateTable** crea una tabla vacía en una base de datos ese.</span><span class="sxs-lookup"><span data-stu-id="75b81-106">The **JetCreateTable** function creates an empty table in an ESE database.</span></span>

```cpp
    JET_ERR JET_API JetCreateTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          unsigned long lPages,
      __in          unsigned long lDensity,
      __out         JET_TABLEID* ptableid
    );
```

### <a name="parameters"></a><span data-ttu-id="75b81-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75b81-107">Parameters</span></span>

<span data-ttu-id="75b81-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="75b81-108">*sesid*</span></span>

<span data-ttu-id="75b81-109">Contexto de sesión de base de datos que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="75b81-109">The database session context to use.</span></span>

<span data-ttu-id="75b81-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="75b81-110">*dbid*</span></span>

<span data-ttu-id="75b81-111">Identificador de base de datos que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="75b81-111">The database identifier to use.</span></span>

<span data-ttu-id="75b81-112">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="75b81-112">*szTableName*</span></span>

<span data-ttu-id="75b81-113">Nombre del índice que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="75b81-113">The name of the index to create.</span></span>

<span data-ttu-id="75b81-114">El nombre debe tener el formato de acuerdo con las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="75b81-114">The name must be formatted according to the following rules:</span></span>

  - <span data-ttu-id="75b81-115">Ser menor que JET_cbNameMost, sin incluir el carácter NULL de terminación.</span><span class="sxs-lookup"><span data-stu-id="75b81-115">Be less than JET_cbNameMost, not including the terminating NULL.</span></span>

  - <span data-ttu-id="75b81-116">Debe realizarse con el siguiente conjunto de caracteres: de 0 a 9, de la a a la Z, de la a a la z y de todos los demás signos de puntuación excepto " \! "</span><span class="sxs-lookup"><span data-stu-id="75b81-116">Be made of the following set of characters: 0 through 9, A through Z, a through z, and all other punctuation except for "\!"</span></span> <span data-ttu-id="75b81-117">(signo de exclamación), "," (coma), " \[ " (corchete de apertura) y " \] " (corchete de cierre), es decir, caracteres ASCII 0x20, 0x22 a 0x2d, 0x2f a 0x5a, 0x5c, 0x5d a 0x7F.</span><span class="sxs-lookup"><span data-stu-id="75b81-117">(exclamation point), "," (comma), "\[" (opening bracket), and "\]" (closing bracket) — that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="75b81-118">No comienza con un espacio.</span><span class="sxs-lookup"><span data-stu-id="75b81-118">Not begin with a space.</span></span>

  - <span data-ttu-id="75b81-119">Debe estar formado por al menos un carácter que no sea un espacio.</span><span class="sxs-lookup"><span data-stu-id="75b81-119">Be made of at least one non-space character.</span></span>

<span data-ttu-id="75b81-120">*lPages*</span><span class="sxs-lookup"><span data-stu-id="75b81-120">*lPages*</span></span>

<span data-ttu-id="75b81-121">Número inicial de páginas de base de datos que se van a asignar a la tabla.</span><span class="sxs-lookup"><span data-stu-id="75b81-121">The initial number of database pages to allocate for the table.</span></span> <span data-ttu-id="75b81-122">Si se especifica un número mayor que uno, se puede reducir la fragmentación si se insertan muchas filas en esta tabla.</span><span class="sxs-lookup"><span data-stu-id="75b81-122">Specifying a number larger than one can reduce fragmentation if many rows are inserted into this table.</span></span>

<span data-ttu-id="75b81-123">*lDensity*</span><span class="sxs-lookup"><span data-stu-id="75b81-123">*lDensity*</span></span>

<span data-ttu-id="75b81-124">Densidad de la tabla, en puntos porcentuales.</span><span class="sxs-lookup"><span data-stu-id="75b81-124">The table density, in percentage points.</span></span> <span data-ttu-id="75b81-125">El número debe ser 0 o estar comprendido entre 20 y 100.</span><span class="sxs-lookup"><span data-stu-id="75b81-125">The number must be either 0 or in the range of 20 through 100.</span></span> <span data-ttu-id="75b81-126">Pasar 0 significa que se debe usar el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="75b81-126">Passing 0 means that the default value should be used.</span></span> <span data-ttu-id="75b81-127">El valor predeterminado es 80.</span><span class="sxs-lookup"><span data-stu-id="75b81-127">The default is 80.</span></span>

<span data-ttu-id="75b81-128">*ptableid*</span><span class="sxs-lookup"><span data-stu-id="75b81-128">*ptableid*</span></span>

<span data-ttu-id="75b81-129">Si se ejecuta correctamente, se devuelve el identificador de tabla en este campo.</span><span class="sxs-lookup"><span data-stu-id="75b81-129">On success, the table identifier is returned in this field.</span></span> <span data-ttu-id="75b81-130">El valor es indefinido si la API no devuelve JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="75b81-130">The value is undefined if the API does not return JET_errSuccess.</span></span>

### <a name="return-value"></a><span data-ttu-id="75b81-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75b81-131">Return Value</span></span>

<span data-ttu-id="75b81-132">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="75b81-132">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="75b81-133">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="75b81-133">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="75b81-134">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="75b81-134">Return code</span></span></p></th>
<th><p><span data-ttu-id="75b81-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="75b81-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75b81-136">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="75b81-136">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="75b81-137">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="75b81-137">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b81-138">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="75b81-138">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="75b81-139">No se pudo resolver la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="75b81-139">The callback function could not be resolved.</span></span> <span data-ttu-id="75b81-140">Es posible que no se haya encontrado el archivo DLL o que no se haya encontrado la función del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="75b81-140">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="75b81-141">Con el registro suficiente habilitado, el registro de eventos proporcionará más detalles.</span><span class="sxs-lookup"><span data-stu-id="75b81-141">With sufficient logging enabled, the event log will provide more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b81-142">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="75b81-142">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="75b81-143">Se intentó indexar sobre una columna de actualización de custodia o de SLV (tenga en cuenta que las columnas de SLV están desusadas).</span><span class="sxs-lookup"><span data-stu-id="75b81-143">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b81-144">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="75b81-144">JET_errCannotNestDDL</span></span></p></td>
<td><p><span data-ttu-id="75b81-145">Si ptablecreate- &gt; grbit especifica JET_bitTableCreateTemplateTable, pero ptablecreate- &gt; szTemplateTableName se establece en NULL.</span><span class="sxs-lookup"><span data-stu-id="75b81-145">If ptablecreate-&gt;grbit specifies JET_bitTableCreateTemplateTable, but ptablecreate-&gt;szTemplateTableName is set to NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b81-146">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="75b81-146">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="75b81-147">Ya existe una columna.</span><span class="sxs-lookup"><span data-stu-id="75b81-147">A column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b81-148">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="75b81-148">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="75b81-149">Se intentó indizar una columna que no existe.</span><span class="sxs-lookup"><span data-stu-id="75b81-149">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="75b81-150">El intento de indizar condicionalmente en una columna que no existe también puede generar este error.</span><span class="sxs-lookup"><span data-stu-id="75b81-150">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b81-151">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="75b81-151">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="75b81-152">Se intentó agregar una columna redundante.</span><span class="sxs-lookup"><span data-stu-id="75b81-152">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="75b81-153">No debe haber más de una columna de incremento automático y no más de una columna de versión por tabla.</span><span class="sxs-lookup"><span data-stu-id="75b81-153">There should be no more than one autoincrement column, and no more than one version column per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b81-154">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="75b81-154">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="75b81-155">Se pasó una densidad no válida en el miembro <em>ulDensity</em> de la estructura <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="75b81-155">An invalid density was passed in the <em>ulDensity</em> member in the <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b81-156">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="75b81-156">JET_errDDLNotInheritable</span></span></p></td>
<td><p><span data-ttu-id="75b81-157">Significa que la tabla denominada en el miembro <strong>szTemplateTableName</strong> de la estructura <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> no era una marca marcada como tabla de plantilla (es decir, que la tabla no tenía JET_bitTableCreateTemplateTable establecido).</span><span class="sxs-lookup"><span data-stu-id="75b81-157">Signifies that the table named in the <strong>szTemplateTableName</strong> member of the <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> structure was not a marked as a template table (that is, that table did not have JET_bitTableCreateTemplateTable set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b81-158">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="75b81-158">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="75b81-159">Se intentó definir dos índices idénticos.</span><span class="sxs-lookup"><span data-stu-id="75b81-159">An attempt was made to define two identical indexes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b81-160">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="75b81-160">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="75b81-161">Se intentó especificar más de un índice principal para una tabla.</span><span class="sxs-lookup"><span data-stu-id="75b81-161">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="75b81-162">Una tabla debe tener exactamente un índice principal.</span><span class="sxs-lookup"><span data-stu-id="75b81-162">A table must have exactly one primary index.</span></span> <span data-ttu-id="75b81-163">Si no se especifica ningún índice principal, el motor de base de datos creará uno de forma transparente.</span><span class="sxs-lookup"><span data-stu-id="75b81-163">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b81-164">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="75b81-164">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="75b81-165">Se especificó una definición de índice no válida.</span><span class="sxs-lookup"><span data-stu-id="75b81-165">An invalid index definition was specified.</span></span> <span data-ttu-id="75b81-166">Algunas de las posibles razones para recibir este error son:</span><span class="sxs-lookup"><span data-stu-id="75b81-166">Some of the possible reasons for receiving this error are:</span></span></p>
<ul>
<li><p><span data-ttu-id="75b81-167">Un índice principal es condicional (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiene JET_bitIndexPrimary establecido y el miembro <strong>cConditionalColumn</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> es mayor que cero).</span><span class="sxs-lookup"><span data-stu-id="75b81-167">A primary index is conditional (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexPrimary set, and <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="75b81-168">Windows Server 2003 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="75b81-168">Windows Server 2003 and later.</span></span> <span data-ttu-id="75b81-169">Se ha intentado crear un índice de tupla con límites de tupla, pero sin pasar el miembro <strong>ptuplelimits</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiene JET_BITINDEXTUPLELIMITS establecido, pero el puntero <strong>ptuplelimits</strong> es null).</span><span class="sxs-lookup"><span data-stu-id="75b81-169">Attempting to create a tuple index with tuple limits, but without passing the <strong>ptuplelimits</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="75b81-170">Pasando una definición de clave no válida en el miembro <strong>szKey</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="75b81-170">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="75b81-171">Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener una descripción de las definiciones válidas.</span><span class="sxs-lookup"><span data-stu-id="75b81-171">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="75b81-172">Establecer el miembro <strong>cbVarSegMac</strong> de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para que sea mayor que JET_cbPrimaryKeyMost (para un índice principal) o mayor que JET_cbSecondaryKeyMost (para un índice secundario).</span><span class="sxs-lookup"><span data-stu-id="75b81-172">Setting the <strong>cbVarSegMac</strong> member in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="75b81-173">Pasar una combinación no válida para un índice Unicode definido por el usuario (uno que tiene el bit de JET_bitIndexUnicode establecido en el miembro <strong>grbit</strong> de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span><span class="sxs-lookup"><span data-stu-id="75b81-173">Passing an invalid combination for a user-defined Unicode index (one which has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span></span> <span data-ttu-id="75b81-174">Algunas causas comunes incluyen el miembro <strong>pidxunicode</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> es null o el LCID especificado en la estructura <strong>pidxunicode</strong> no es válido.</span><span class="sxs-lookup"><span data-stu-id="75b81-174">Some common causes include the <strong>pidxunicode</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is NULL, or the LCID specified in the <strong>pidxunicode</strong> structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="75b81-175">Especificar una columna de varios valores para un índice principal.</span><span class="sxs-lookup"><span data-stu-id="75b81-175">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="75b81-176">Intentando indexar demasiadas columnas condicionales.</span><span class="sxs-lookup"><span data-stu-id="75b81-176">Trying to index too many conditional columns.</span></span> <span data-ttu-id="75b81-177">El miembro <strong>cConditionalColumn</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> no debe ser mayor que JET_ccolKeyMost.</span><span class="sxs-lookup"><span data-stu-id="75b81-177">The <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b81-178">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="75b81-178">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="75b81-179">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="75b81-179">Windows XP and later.</span></span> <span data-ttu-id="75b81-180">Se especificó una estructura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> y no se admiten sus límites.</span><span class="sxs-lookup"><span data-stu-id="75b81-180">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="75b81-181">Vea la sección Comentarios de la estructura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="75b81-181">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b81-182">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="75b81-182">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="75b81-183">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="75b81-183">Windows XP and later.</span></span> <span data-ttu-id="75b81-184">Un índice de tupla no puede ser único (es decir, el miembro <em>grbit</em> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> no debe tener establecido JET_bitIndexPrimary y JET_bitIndexUnique).</span><span class="sxs-lookup"><span data-stu-id="75b81-184">A tuple index cannot be unique (that is, the <em>grbit</em> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b81-185">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="75b81-185">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="75b81-186">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="75b81-186">Windows XP and later.</span></span> <span data-ttu-id="75b81-187">Un índice de tupla solo puede estar en una sola columna (es decir, si el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiene JET_bitIndexTuples establecido y el miembro <strong>szKey</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> especifica más de una columna).</span><span class="sxs-lookup"><span data-stu-id="75b81-187">A tuple index can only be over a single column (that is, if the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b81-188">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="75b81-188">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="75b81-189">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="75b81-189">Windows XP and later.</span></span> <span data-ttu-id="75b81-190">Un índice de tupla no puede ser un índice principal (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> no debe tener establecido JET_bitIndexPrimary y JET_bitIndexTuples).</span><span class="sxs-lookup"><span data-stu-id="75b81-190">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b81-191">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="75b81-191">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="75b81-192">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="75b81-192">Windows XP and later.</span></span> <span data-ttu-id="75b81-193">Un índice de tupla no permite establecer el miembro <strong>cbVarSegMac</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="75b81-193">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b81-194">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="75b81-194">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="75b81-195">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="75b81-195">Windows XP and later.</span></span> <span data-ttu-id="75b81-196">Un índice de tupla solo puede estar en una columna de texto o Unicode.</span><span class="sxs-lookup"><span data-stu-id="75b81-196">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="75b81-197">Un intento de indizar otras columnas (como columnas binarias) dará como resultado JET_errIndexTuplesTextColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="75b81-197">An attempt to index other columns (such as binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b81-198">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="75b81-198">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="75b81-199">Se intentó crear un índice sin información de versión mientras estaba en una transacción.</span><span class="sxs-lookup"><span data-stu-id="75b81-199">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b81-200">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="75b81-200">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="75b81-201">El miembro <strong>CP</strong> de la estructura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> no se ha establecido en una página de códigos válida.</span><span class="sxs-lookup"><span data-stu-id="75b81-201">The <strong>cp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="75b81-202">Los únicos valores válidos para las columnas de texto son inglés (1252) y Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="75b81-202">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="75b81-203">Un valor de 0 significa que se usará el valor predeterminado (Inglés, 1252).</span><span class="sxs-lookup"><span data-stu-id="75b81-203">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b81-204">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="75b81-204">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="75b81-205">El miembro <strong>coltyp</strong> de la estructura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> no se ha establecido en un tipo de columna válido.</span><span class="sxs-lookup"><span data-stu-id="75b81-205">The <strong>coltyp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b81-206">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="75b81-206">JET_errInvalidCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="75b81-207">Algunas de las razones por las que puede producirse este error:</span><span class="sxs-lookup"><span data-stu-id="75b81-207">Some of the reasons this error may occur:</span></span></p>
<ul>
<li><p><span data-ttu-id="75b81-208">El miembro <strong>rgindexcreate</strong> de la estructura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> se estableció en NULL.</span><span class="sxs-lookup"><span data-stu-id="75b81-208">The <strong>rgindexcreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="75b81-209">El miembro <strong>rgcolumncreate</strong> de la estructura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> se estableció en NULL.</span><span class="sxs-lookup"><span data-stu-id="75b81-209">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="75b81-210">El miembro <strong>cbStruct</strong> de una estructura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> no se ha establecido en un valor válido.</span><span class="sxs-lookup"><span data-stu-id="75b81-210">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure was not set to a valid value.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b81-211">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="75b81-211">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="75b81-212">Se especificó una combinación no válida de miembros de <strong>grbit</strong> en <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>.</span><span class="sxs-lookup"><span data-stu-id="75b81-212">An invalid combination of <strong>grbit</strong> members was specified in <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>.</span></span></p>
<p><span data-ttu-id="75b81-213">La definición del índice no es válida porque el miembro <strong>grbit</strong> contiene valores incoherentes.</span><span class="sxs-lookup"><span data-stu-id="75b81-213">The index definition is invalid because the <strong>grbit</strong> member contains inconsistent values.</span></span> <span data-ttu-id="75b81-214">Algunas de las razones posibles son:</span><span class="sxs-lookup"><span data-stu-id="75b81-214">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="75b81-215">Un índice principal tenía un bit ignore especificado (es decir, JET_bitIndexPrimary se pasó con JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull o JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="75b81-215">A primary index had an ignore bit specified (that is, JET_bitIndexPrimary was passed with JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="75b81-216">Un índice vacío no omite ningún miembro nulo (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiene JET_bitIndexEmpty establecido, pero no tiene JET_bitIndexIgnoreAnyNull establecida).</span><span class="sxs-lookup"><span data-stu-id="75b81-216">An empty index does not ignore any NULL members (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="75b81-217">Pasando una estructura de <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> con un miembro <strong>grbit</strong> no válido.</span><span class="sxs-lookup"><span data-stu-id="75b81-217">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b81-218">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="75b81-218">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="75b81-219">Se pasó un ID. de configuración regional (LCID) no válido (ya sea a través del miembro <strong>LCID</strong> de la estructura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> a la que apunta el miembro <strong>pidxunicode</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> , o a través del campo <strong>LCID</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</span><span class="sxs-lookup"><span data-stu-id="75b81-219">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member of the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure which is pointed to by the <strong>pidxunicode</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure, or through the <strong>lcid</strong> field of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b81-220">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="75b81-220">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="75b81-221">Se proporcionó un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="75b81-221">An invalid parameter was given.</span></span> <span data-ttu-id="75b81-222">Algunas de las razones posibles son:</span><span class="sxs-lookup"><span data-stu-id="75b81-222">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="75b81-223">El miembro <strong>rgcolumncreate</strong> de la estructura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> es NULL.</span><span class="sxs-lookup"><span data-stu-id="75b81-223">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure is NULL.</span></span></p></li>
<li><p><span data-ttu-id="75b81-224">El miembro <strong>cbStruct</strong> de una de las estructuras <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> proporcionadas en el miembro <strong>rgcolumncreate</strong> de la estructura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> no se estableció en sizeof (JET_COLUMNCREATE).</span><span class="sxs-lookup"><span data-stu-id="75b81-224">The <strong>cbStruct</strong> member of one of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structures given in the <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was not set to sizeof( JET_COLUMNCREATE ).</span></span></p></li>
<li><p><span data-ttu-id="75b81-225">El miembro <strong>cbKey</strong> de una estructura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="75b81-225">The <strong>cbKey</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="75b81-226">El miembro <strong>cbStruct</strong> de una estructura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> no se establece en sizeof (JET_INDEXCREATE).</span><span class="sxs-lookup"><span data-stu-id="75b81-226">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is not set to sizeof( JET_INDEXCREATE ).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b81-227">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="75b81-227">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="75b81-228">El registro es demasiado grande.</span><span class="sxs-lookup"><span data-stu-id="75b81-228">The record is too big.</span></span> <span data-ttu-id="75b81-229">La suma del miembro <strong>cbMax</strong> de la estructura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> para todas las columnas fijas no debe superar un valor determinado.</span><span class="sxs-lookup"><span data-stu-id="75b81-229">The sum of the <strong>cbMax</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure for all fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b81-230">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="75b81-230">JET_errTableDuplicate</span></span></p></td>
<td><p><span data-ttu-id="75b81-231">La tabla ya existe.</span><span class="sxs-lookup"><span data-stu-id="75b81-231">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b81-232">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="75b81-232">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="75b81-233">Se intentó agregar demasiadas columnas a la tabla.</span><span class="sxs-lookup"><span data-stu-id="75b81-233">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="75b81-234">Una tabla no puede tener más de JET_ccolFixedMost columnas fijas, ni más de JET_ccolVarMost columnas de longitud variable, ni más de JET_ccolTaggedMost columnas etiquetadas.</span><span class="sxs-lookup"><span data-stu-id="75b81-234">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b81-235">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="75b81-235">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="75b81-236">Error al intentar normalizar una columna Unicode.</span><span class="sxs-lookup"><span data-stu-id="75b81-236">An error occurred attempting to normalize a Unicode column.</span></span> <span data-ttu-id="75b81-237">Esto puede deberse a la falta de recursos del sistema.</span><span class="sxs-lookup"><span data-stu-id="75b81-237">This can be caused by running out of system resources.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="75b81-238">Observaciones</span><span class="sxs-lookup"><span data-stu-id="75b81-238">Remarks</span></span>

<span data-ttu-id="75b81-239">**JetCreateTable** crea una tabla que no contiene ninguna columna.</span><span class="sxs-lookup"><span data-stu-id="75b81-239">**JetCreateTable** creates a table which does not contain any columns.</span></span> <span data-ttu-id="75b81-240">Para agregar columnas, vea [JetAddColumn](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="75b81-240">To add columns, see [JetAddColumn](./jetaddcolumn-function.md).</span></span>

<span data-ttu-id="75b81-241">Internamente, **JetCreateTable** llama a [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), rellenando una estructura de [JET_TABLECREATE2](./jet-tablecreate2-structure.md) con:</span><span class="sxs-lookup"><span data-stu-id="75b81-241">Internally, **JetCreateTable** calls [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), filling in a [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structure with:</span></span>

  - <span data-ttu-id="75b81-242">JET_TABLECREATE2. cbStruct = sizeof (JET_TABLECREATE2)</span><span class="sxs-lookup"><span data-stu-id="75b81-242">JET_TABLECREATE2.cbStruct = sizeof( JET_TABLECREATE2 )</span></span>

  - <span data-ttu-id="75b81-243">JET_TABLECREATE2. szTableName = szTableName</span><span class="sxs-lookup"><span data-stu-id="75b81-243">JET_TABLECREATE2.szTableName = szTableName</span></span>

  - <span data-ttu-id="75b81-244">JET_TABLECREATE2. ulPages = lPage</span><span class="sxs-lookup"><span data-stu-id="75b81-244">JET_TABLECREATE2.ulPages = lPage</span></span>

  - <span data-ttu-id="75b81-245">JET_TABLECREATE2. ulDensity = lDensity</span><span class="sxs-lookup"><span data-stu-id="75b81-245">JET_TABLECREATE2.ulDensity = lDensity</span></span>

  - <span data-ttu-id="75b81-246">JET_TABLECREATE2. TABLEID = JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="75b81-246">JET_TABLECREATE2.tableid = JET_tableidNil</span></span>

<span data-ttu-id="75b81-247">Todos los demás campos de la estructura de [JET_TABLECREATE2](./jet-tablecreate2-structure.md) interna se establecen en cero o null.</span><span class="sxs-lookup"><span data-stu-id="75b81-247">All the other fields of the internal [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structure are set to zero or NULL.</span></span> <span data-ttu-id="75b81-248">En la salida, *ptableid* se establecerá en JET_TABLECREATE2. TABLEID.</span><span class="sxs-lookup"><span data-stu-id="75b81-248">On output, *ptableid* will be set to JET_TABLECREATE2.tableid.</span></span>

<span data-ttu-id="75b81-249">Consulte [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="75b81-249">See [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) for more details.</span></span>

<span data-ttu-id="75b81-250">Al igual que [JetOpenTable](./jetopentable-function.md), cuando la aplicación se realiza utilizando el miembro **TABLEID** devuelto de la estructura [JET_TABLECREATE2](./jet-tablecreate2-structure.md) , normalmente se debe cerrar con [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="75b81-250">Like [JetOpenTable](./jetopentable-function.md), when the application is done using the returned **tableid** member from the [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structure, it should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="75b81-251">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75b81-251">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75b81-252"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="75b81-252"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="75b81-253">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="75b81-253">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b81-254"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="75b81-254"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="75b81-255">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="75b81-255">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b81-256"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="75b81-256"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="75b81-257">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="75b81-257">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b81-258"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="75b81-258"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="75b81-259">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="75b81-259">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b81-260"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="75b81-260"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="75b81-261">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="75b81-261">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b81-262"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="75b81-262"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="75b81-263">Se implementa como <strong>JetCreateTableW</strong> (Unicode) y <strong>JetCreateTableA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="75b81-263">Implemented as <strong>JetCreateTableW</strong> (Unicode) and <strong>JetCreateTableA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="75b81-264">Consulte también</span><span class="sxs-lookup"><span data-stu-id="75b81-264">See Also</span></span>

[<span data-ttu-id="75b81-265">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="75b81-265">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="75b81-266">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="75b81-266">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="75b81-267">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="75b81-267">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="75b81-268">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="75b81-268">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="75b81-269">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="75b81-269">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="75b81-270">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="75b81-270">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="75b81-271">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="75b81-271">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="75b81-272">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="75b81-272">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
