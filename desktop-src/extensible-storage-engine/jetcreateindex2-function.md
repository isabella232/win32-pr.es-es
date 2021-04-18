---
description: 'Más información acerca de: JetCreateIndex2 (función)'
title: Función JetCreateIndex2
TOCTitle: JetCreateIndex2 Function
ms:assetid: 8810eaed-40cb-4561-aafc-9a9bbdb0d05b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269324(v=EXCHG.10)
ms:contentKeyID: 32765614
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndex2W
- JetCreateIndex2A
- JetCreateIndex2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 42c1eb8fa1bb7fa880cf7286a1ec472ddc7ba7fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716606"
---
# <a name="jetcreateindex2-function"></a><span data-ttu-id="11ad1-103">Función JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="11ad1-103">JetCreateIndex2 Function</span></span>


<span data-ttu-id="11ad1-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="11ad1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateindex2-function"></a><span data-ttu-id="11ad1-105">Función JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="11ad1-105">JetCreateIndex2 Function</span></span>

<span data-ttu-id="11ad1-106">La función **JetCreateIndex2** crea índices sobre los datos en una base de datos de ese, que se puede usar para buscar datos específicos rápidamente.</span><span class="sxs-lookup"><span data-stu-id="11ad1-106">The **JetCreateIndex2** function creates indexes over data in an ESE database, which can be used to locate specific data quickly.</span></span>

```cpp
    JET_ERR JET_API JetCreateIndex2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_INDEXCREATE* pindexcreate,
      __in          unsigned long cIndexCreate
    );
```

### <a name="parameters"></a><span data-ttu-id="11ad1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11ad1-107">Parameters</span></span>

<span data-ttu-id="11ad1-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="11ad1-108">*sesid*</span></span>

<span data-ttu-id="11ad1-109">Contexto de sesión de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="11ad1-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="11ad1-110">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="11ad1-110">*tableid*</span></span>

<span data-ttu-id="11ad1-111">Tabla en la que se creará el índice.</span><span class="sxs-lookup"><span data-stu-id="11ad1-111">The table on which the index will be created.</span></span>

<span data-ttu-id="11ad1-112">*pindexcreate*</span><span class="sxs-lookup"><span data-stu-id="11ad1-112">*pindexcreate*</span></span>

<span data-ttu-id="11ad1-113">Matriz de estructuras de [JET_INDEXCREATE](./jet-indexcreate-structure.md) , cada una de las cuales define un índice que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="11ad1-113">An array of [JET_INDEXCREATE](./jet-indexcreate-structure.md) structures, each of which defines an index to be created.</span></span>

<span data-ttu-id="11ad1-114">*cIndexCreate*</span><span class="sxs-lookup"><span data-stu-id="11ad1-114">*cIndexCreate*</span></span>

<span data-ttu-id="11ad1-115">Número de elementos de la matriz *pindexcreate* .</span><span class="sxs-lookup"><span data-stu-id="11ad1-115">The number of elements in the *pindexcreate* array.</span></span>

### <a name="return-value"></a><span data-ttu-id="11ad1-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11ad1-116">Return Value</span></span>

<span data-ttu-id="11ad1-117">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="11ad1-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="11ad1-118">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="11ad1-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="11ad1-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="11ad1-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="11ad1-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="11ad1-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="11ad1-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="11ad1-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="11ad1-122">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="11ad1-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11ad1-123">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="11ad1-123">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="11ad1-124">Se intentó indexar sobre una columna de actualización de custodia o de SLV (tenga en cuenta que las columnas de SLV están desusadas).</span><span class="sxs-lookup"><span data-stu-id="11ad1-124">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11ad1-125">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="11ad1-125">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="11ad1-126">Se intentó indizar una columna que no existe.</span><span class="sxs-lookup"><span data-stu-id="11ad1-126">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="11ad1-127">El intento de indizar condicionalmente en una columna que no existe también puede generar este error.</span><span class="sxs-lookup"><span data-stu-id="11ad1-127">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11ad1-128">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="11ad1-128">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="11ad1-129">Este error se devolverá si el miembro <strong>ulDensity</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> está establecido en un número inferior a 20 o superior a 100.</span><span class="sxs-lookup"><span data-stu-id="11ad1-129">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to a number less than 20 or more than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11ad1-130">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="11ad1-130">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="11ad1-131">Se ha intentado definir dos índices idénticos.</span><span class="sxs-lookup"><span data-stu-id="11ad1-131">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11ad1-132">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="11ad1-132">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="11ad1-133">Se intentó especificar más de un índice principal para una tabla.</span><span class="sxs-lookup"><span data-stu-id="11ad1-133">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="11ad1-134">Una tabla debe tener exactamente un índice principal.</span><span class="sxs-lookup"><span data-stu-id="11ad1-134">A table must have exactly one primary index.</span></span> <span data-ttu-id="11ad1-135">Si no se especifica ningún índice principal, el motor de base de datos creará uno de forma transparente.</span><span class="sxs-lookup"><span data-stu-id="11ad1-135">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11ad1-136">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="11ad1-136">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="11ad1-137">Se especificó una definición de índice no válida.</span><span class="sxs-lookup"><span data-stu-id="11ad1-137">An invalid index definition was specified.</span></span> <span data-ttu-id="11ad1-138">Algunas de las posibles razones para recibir este error son:</span><span class="sxs-lookup"><span data-stu-id="11ad1-138">Some of the possible reasons for receiving this error are:</span></span></p>
<ul>
<li><p><span data-ttu-id="11ad1-139">Un índice principal es condicional (el miembro<strong>grbit</strong> de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiene JET_bitIndexPrimary establecido y el miembro <strong>cConditionalColumn</strong> de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> es mayor que cero).</span><span class="sxs-lookup"><span data-stu-id="11ad1-139">A primary index is conditional (<strong>grbit</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> has JET_bitIndexPrimary set, and the <strong>cConditionalColumn</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="11ad1-140">Windows Server 2003 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="11ad1-140">Windows Server 2003 and later.</span></span> <span data-ttu-id="11ad1-141">Se ha intentado crear un índice de tupla con límites de tupla, pero sin pasar información en el miembro <strong>ptuplelimits</strong> en <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (es decir, <em>grbit</em> JET_bitIndexTupleLimits se ha establecido, pero el puntero <strong>ptuplelimits</strong> es null).</span><span class="sxs-lookup"><span data-stu-id="11ad1-141">Attempting to create a tuple index with tuple limits, but without passing information in the <strong>ptuplelimits</strong> member in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (that is, <em>grbit</em> has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="11ad1-142">Pasando una definición de clave no válida en el miembro <strong>szKey</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="11ad1-142">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="11ad1-143">Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener una descripción de las definiciones válidas.</span><span class="sxs-lookup"><span data-stu-id="11ad1-143">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="11ad1-144">Establecer el miembro <strong>cbVarSegMac</strong> de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para que sea mayor que JET_cbPrimaryKeyMost (para un índice principal) o mayor que JET_cbSecondaryKeyMost (para un índice secundario).</span><span class="sxs-lookup"><span data-stu-id="11ad1-144">Setting the <strong>cbVarSegMac</strong> member in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="11ad1-145">Pasar una combinación no válida para un índice Unicode definido por el usuario (uno que tiene el bit de JET_bitIndexUnicode establecido en el miembro <strong>grbit</strong> de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span><span class="sxs-lookup"><span data-stu-id="11ad1-145">Passing an invalid combination for a user-defined Unicode index (one which has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span></span> <span data-ttu-id="11ad1-146">Algunas causas comunes pueden ser que el campo pidxunicode de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> sea NULL o que el LCID especificado en la estructura pidxunicode no sea válido.</span><span class="sxs-lookup"><span data-stu-id="11ad1-146">Some common causes may be that the pidxunicode field of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is NULL, or the LCID specified in the pidxunicode structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="11ad1-147">Especificar una columna de varios valores para un índice principal.</span><span class="sxs-lookup"><span data-stu-id="11ad1-147">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="11ad1-148">Intentando indexar demasiadas columnas condicionales.</span><span class="sxs-lookup"><span data-stu-id="11ad1-148">Trying to index too many conditional columns.</span></span> <span data-ttu-id="11ad1-149">El miembro <strong>cConditionalColumn</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> no debe ser mayor que JET_ccolKeyMost.</span><span class="sxs-lookup"><span data-stu-id="11ad1-149">The <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11ad1-150">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="11ad1-150">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="11ad1-151">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="11ad1-151">Windows XP and later.</span></span> <span data-ttu-id="11ad1-152">Se especificó una estructura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> y no se admiten sus límites.</span><span class="sxs-lookup"><span data-stu-id="11ad1-152">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="11ad1-153">Vea la sección Comentarios de la estructura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="11ad1-153">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11ad1-154">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="11ad1-154">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="11ad1-155">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="11ad1-155">Windows XP and later.</span></span> <span data-ttu-id="11ad1-156">Un índice de tupla no puede ser único (<em>grbit</em> no debe tener JET_bitIndexTuples y JET_bitIndexUnique establecer).</span><span class="sxs-lookup"><span data-stu-id="11ad1-156">A tuple index cannot be unique (<em>grbit</em> must not have both JET_bitIndexTuples and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11ad1-157">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="11ad1-157">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="11ad1-158">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="11ad1-158">Windows XP and later.</span></span> <span data-ttu-id="11ad1-159">Un índice de tupla solo puede estar en una sola columna (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiene JET_bitIndexTuples establecido y el miembro <strong>szKey</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> especifica más de una columna).</span><span class="sxs-lookup"><span data-stu-id="11ad1-159">A tuple index can only be over a single column (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11ad1-160">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="11ad1-160">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="11ad1-161">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="11ad1-161">Windows XP and later.</span></span> <span data-ttu-id="11ad1-162">Un índice de tupla no puede ser un índice principal (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> no debe tener establecido JET_bitIndexPrimary y JET_bitIndexTuples).</span><span class="sxs-lookup"><span data-stu-id="11ad1-162">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11ad1-163">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="11ad1-163">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="11ad1-164">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="11ad1-164">Windows XP and later.</span></span> <span data-ttu-id="11ad1-165">Un índice de tupla solo puede estar en una columna de texto o Unicode.</span><span class="sxs-lookup"><span data-stu-id="11ad1-165">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="11ad1-166">Un intento de indizar otras columnas (por ejemplo, columnas binarias) dará como resultado JET_errIndexTuplesTextColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="11ad1-166">An attempt to index other columns (for example, binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11ad1-167">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="11ad1-167">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="11ad1-168">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="11ad1-168">Windows XP and later.</span></span> <span data-ttu-id="11ad1-169">Un índice de tupla no permite establecer el miembro <strong>cbVarSegMac</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="11ad1-169">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11ad1-170">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="11ad1-170">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="11ad1-171">Se intentó crear un índice sin información de versión mientras estaba en una transacción.</span><span class="sxs-lookup"><span data-stu-id="11ad1-171">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11ad1-172">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="11ad1-172">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="11ad1-173">La definición del índice no es válida porque el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> contiene valores incoherentes.</span><span class="sxs-lookup"><span data-stu-id="11ad1-173">The index definition is invalid because the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure contains inconsistent values.</span></span> <span data-ttu-id="11ad1-174">Algunas de las razones posibles son:</span><span class="sxs-lookup"><span data-stu-id="11ad1-174">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="11ad1-175">Un índice principal tenía un bit omitido especificado (JET_bitIndexPrimary se pasó con uno de JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull o JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="11ad1-175">A primary index had an ignore bit specified (JET_bitIndexPrimary was passed with one of JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="11ad1-176">Un índice vacío no omite los campos NULOs (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiene JET_bitIndexEmpty establecido, pero no tiene JET_bitIndexIgnoreAnyNull establecida).</span><span class="sxs-lookup"><span data-stu-id="11ad1-176">An empty index does not ignore any NULL fields (that is, <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="11ad1-177">Pasando una estructura de <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> con un miembro <strong>grbit</strong> no válido.</span><span class="sxs-lookup"><span data-stu-id="11ad1-177">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span> <span data-ttu-id="11ad1-178">Vea <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span><span class="sxs-lookup"><span data-stu-id="11ad1-178">See <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span></span></p></li>
</ul>
<p><span data-ttu-id="11ad1-179">Al crear varios índices a la vez (es decir, si el parámetro <em>cIndexCreate</em> es mayor que uno), ninguno de los índices puede contener ninguno de los bits siguientes:</span><span class="sxs-lookup"><span data-stu-id="11ad1-179">When creating several indexes at once (that is, if the <em>cIndexCreate</em> parameter is greater than one), none of the indexes may contain any of the following bits:</span></span></p>
<ul>
<li><p><span data-ttu-id="11ad1-180">JET_bitIndexPrimary</span><span class="sxs-lookup"><span data-stu-id="11ad1-180">JET_bitIndexPrimary</span></span></p></li>
<li><p><span data-ttu-id="11ad1-181">JET_bitIndexUnversioned</span><span class="sxs-lookup"><span data-stu-id="11ad1-181">JET_bitIndexUnversioned</span></span></p></li>
<li><p><span data-ttu-id="11ad1-182">JET_bitIndexEmpty</span><span class="sxs-lookup"><span data-stu-id="11ad1-182">JET_bitIndexEmpty</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11ad1-183">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="11ad1-183">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="11ad1-184">Se pasó un ID. de configuración regional (LCID) no válido (ya sea a través del miembro <strong>LCID</strong> en la estructura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , que el miembro <strong>pidxunicode</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> contiene un puntero a o a través del miembro <strong>LCID</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</span><span class="sxs-lookup"><span data-stu-id="11ad1-184">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member in the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure, which the <strong>pidxunicode</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure contains a pointer to, or through the <strong>lcid</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11ad1-185">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="11ad1-185">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="11ad1-186">Se especificó un nombre de índice no válido.</span><span class="sxs-lookup"><span data-stu-id="11ad1-186">An invalid index name was specified.</span></span> <span data-ttu-id="11ad1-187">Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="11ad1-187">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11ad1-188">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="11ad1-188">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="11ad1-189">Se pasó un parámetro no válido a la API.</span><span class="sxs-lookup"><span data-stu-id="11ad1-189">An invalid parameter was passed into the API.</span></span> <span data-ttu-id="11ad1-190">Algunas de las razones por las que se puede devolver este error son:</span><span class="sxs-lookup"><span data-stu-id="11ad1-190">Some of the reasons this error may be returned are:</span></span></p>
<ul>
<li><p><span data-ttu-id="11ad1-191">El campo <strong>cbKey</strong> de una estructura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="11ad1-191">The <strong>cbKey</strong> field of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="11ad1-192">El miembro <strong>cbStruct</strong> de una estructura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> no se establece en sizeof (<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</span><span class="sxs-lookup"><span data-stu-id="11ad1-192">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is not set to sizeof(<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11ad1-193">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="11ad1-193">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="11ad1-194">Error al intentar normalizar una columna Unicode.</span><span class="sxs-lookup"><span data-stu-id="11ad1-194">An error occurred attempting to normalize a Unicode column.</span></span> <span data-ttu-id="11ad1-195">Esto puede deberse a la falta de recursos del sistema.</span><span class="sxs-lookup"><span data-stu-id="11ad1-195">This can be caused by running out of system resources.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="11ad1-196">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11ad1-196">Remarks</span></span>

<span data-ttu-id="11ad1-197">El valor devuelto es JET_errSuccess si se completan correctamente todos los índices especificados.</span><span class="sxs-lookup"><span data-stu-id="11ad1-197">The return value is JET_errSuccess on successful completion of all indexes specified.</span></span>

<span data-ttu-id="11ad1-198">**JetCreateIndex2** recorre en iteración los índices proporcionados en **pindexcreate** y a veces se anulará en el primer error.</span><span class="sxs-lookup"><span data-stu-id="11ad1-198">**JetCreateIndex2** iterates through the indexes given in **pindexcreate**, and will sometimes abort on the first failure.</span></span> <span data-ttu-id="11ad1-199">Es posible que no se haya intentado ningún índice después del primer índice con un error, aunque el miembro **Err** de la estructura [JET_INDEXCREATE](./jet-indexcreate-structure.md) contiene JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="11ad1-199">Any indexes after the first index with an error may not have been attempted, even though the **err** member of the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure contains JET_errSuccess.</span></span>

#### <a name="requirements"></a><span data-ttu-id="11ad1-200">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11ad1-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="11ad1-201"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="11ad1-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="11ad1-202">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="11ad1-202">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11ad1-203"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="11ad1-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="11ad1-204">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="11ad1-204">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11ad1-205"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="11ad1-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="11ad1-206">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="11ad1-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11ad1-207"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="11ad1-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="11ad1-208">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="11ad1-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11ad1-209"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="11ad1-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="11ad1-210">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="11ad1-210">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11ad1-211"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="11ad1-211"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="11ad1-212">Se implementa como <strong>JetCreateIndex2W</strong> (Unicode) y <strong>JetCreateIndex2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="11ad1-212">Implemented as <strong>JetCreateIndex2W</strong> (Unicode) and <strong>JetCreateIndex2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="11ad1-213">Consulte también</span><span class="sxs-lookup"><span data-stu-id="11ad1-213">See Also</span></span>

[<span data-ttu-id="11ad1-214">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="11ad1-214">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="11ad1-215">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="11ad1-215">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="11ad1-216">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="11ad1-216">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="11ad1-217">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="11ad1-217">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="11ad1-218">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="11ad1-218">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="11ad1-219">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="11ad1-219">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="11ad1-220">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="11ad1-220">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="11ad1-221">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="11ad1-221">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="11ad1-222">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="11ad1-222">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
