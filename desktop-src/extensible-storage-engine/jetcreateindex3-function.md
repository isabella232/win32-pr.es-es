---
description: 'Más información acerca de: JetCreateIndex3 (función)'
title: Función JetCreateIndex3
TOCTitle: JetCreateIndex3 Function
ms:assetid: bc9b940e-65c6-49d6-ad32-74434527d29f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294075(v=EXCHG.10)
ms:contentKeyID: 32765690
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndex3A
- JetCreateIndex3
- JetCreateIndex3W
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c4f3331a903d4885499ff6c2cd2cad0d8b8534a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360992"
---
# <a name="jetcreateindex3-function"></a><span data-ttu-id="2a44d-103">Función JetCreateIndex3</span><span class="sxs-lookup"><span data-stu-id="2a44d-103">JetCreateIndex3 Function</span></span>


<span data-ttu-id="2a44d-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2a44d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateindex3-function"></a><span data-ttu-id="2a44d-105">Función JetCreateIndex3</span><span class="sxs-lookup"><span data-stu-id="2a44d-105">JetCreateIndex3 Function</span></span>

<span data-ttu-id="2a44d-106">La función **JetCreateIndex3** crea índices sobre los datos en una base de datos de ese, que se puede usar para buscar datos específicos rápidamente.</span><span class="sxs-lookup"><span data-stu-id="2a44d-106">The **JetCreateIndex3** function creates indexes over data in an ESE database, which can be used to locate specific data quickly.</span></span>

<span data-ttu-id="2a44d-107">**Windows 7: JetCreateIndex3** se incluye en el sistema operativo Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2a44d-107">**Windows 7:  JetCreateIndex3** is introduced in the Windows 7 operating system.</span></span>

```cpp
    JET_ERR JET_API JetCreateIndex3(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_INDEXCREATE2* pindexcreate,
      __in          unsigned long cIndexCreate
    );
```

### <a name="parameters"></a><span data-ttu-id="2a44d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2a44d-108">Parameters</span></span>

<span data-ttu-id="2a44d-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="2a44d-109">*sesid*</span></span>

<span data-ttu-id="2a44d-110">Contexto de sesión de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="2a44d-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="2a44d-111">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="2a44d-111">*tableid*</span></span>

<span data-ttu-id="2a44d-112">Tabla en la que se creará el índice.</span><span class="sxs-lookup"><span data-stu-id="2a44d-112">The table on which the index will be created.</span></span>

<span data-ttu-id="2a44d-113">*pindexcreate*</span><span class="sxs-lookup"><span data-stu-id="2a44d-113">*pindexcreate*</span></span>

<span data-ttu-id="2a44d-114">Matriz de estructuras de [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) , cada una de las cuales define un índice que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="2a44d-114">An array of [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structures, each of which defines an index to be created.</span></span>

<span data-ttu-id="2a44d-115">*cIndexCreate*</span><span class="sxs-lookup"><span data-stu-id="2a44d-115">*cIndexCreate*</span></span>

<span data-ttu-id="2a44d-116">Número de elementos de la matriz *pindexcreate* .</span><span class="sxs-lookup"><span data-stu-id="2a44d-116">The number of elements in the *pindexcreate* array.</span></span>

### <a name="return-value"></a><span data-ttu-id="2a44d-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2a44d-117">Return Value</span></span>

<span data-ttu-id="2a44d-118">Esta función devuelve el tipo de datos [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="2a44d-118">This function returns the [JET_ERR](./jet-err.md) data type with one of the following return codes.</span></span> <span data-ttu-id="2a44d-119">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="2a44d-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2a44d-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2a44d-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="2a44d-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a44d-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2a44d-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="2a44d-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="2a44d-123">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="2a44d-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a44d-124">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="2a44d-124">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="2a44d-125">Se intentó indexar sobre una columna de actualización de custodia o de SLV (tenga en cuenta que las columnas de SLV están desusadas).</span><span class="sxs-lookup"><span data-stu-id="2a44d-125">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a44d-126">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="2a44d-126">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="2a44d-127">Se intentó indizar una columna que no existe.</span><span class="sxs-lookup"><span data-stu-id="2a44d-127">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="2a44d-128">El intento de indizar condicionalmente en una columna que no existe también puede generar este error.</span><span class="sxs-lookup"><span data-stu-id="2a44d-128">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a44d-129">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="2a44d-129">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="2a44d-130">Este error se devolverá si el miembro <strong>ulDensity</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> está establecido en un número menor que 20 o mayor que 100.</span><span class="sxs-lookup"><span data-stu-id="2a44d-130">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to a number less than 20 or greater than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a44d-131">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="2a44d-131">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="2a44d-132">Se ha intentado definir dos índices idénticos.</span><span class="sxs-lookup"><span data-stu-id="2a44d-132">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a44d-133">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="2a44d-133">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="2a44d-134">Se intentó especificar más de un índice principal para una tabla.</span><span class="sxs-lookup"><span data-stu-id="2a44d-134">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="2a44d-135">Una tabla debe tener exactamente un índice principal.</span><span class="sxs-lookup"><span data-stu-id="2a44d-135">A table must have exactly one primary index.</span></span> <span data-ttu-id="2a44d-136">Si no se especifica ningún índice principal, el motor de base de datos creará uno de forma transparente.</span><span class="sxs-lookup"><span data-stu-id="2a44d-136">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a44d-137">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="2a44d-137">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="2a44d-138">Se especificó una definición de índice no válida.</span><span class="sxs-lookup"><span data-stu-id="2a44d-138">An invalid index definition was specified.</span></span> <span data-ttu-id="2a44d-139">A continuación se indican algunas posibles razones para recibir este error:</span><span class="sxs-lookup"><span data-stu-id="2a44d-139">The following are some possible reasons for receiving this error:</span></span></p>
<ul>
<li><p><span data-ttu-id="2a44d-140">Un índice principal es condicional (el miembro<strong>grbit</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tiene JET_bitIndexPrimary establecido y el miembro <strong>cConditionalColumn</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> es mayor que cero).</span><span class="sxs-lookup"><span data-stu-id="2a44d-140">A primary index is conditional (<strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> has JET_bitIndexPrimary set, and the <strong>cConditionalColumn</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="2a44d-141">Windows Server 2003 y versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="2a44d-141">Windows Server 2003 and later versions of Windows.</span></span> <span data-ttu-id="2a44d-142">Se ha intentado crear un índice de tupla con límites de tupla, pero sin pasar información en el miembro <strong>ptuplelimits</strong> en <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (es decir, <em>grbit</em> JET_bitIndexTupleLimits se ha establecido, pero el puntero <strong>ptuplelimits</strong> es null).</span><span class="sxs-lookup"><span data-stu-id="2a44d-142">Attempting to create a tuple index with tuple limits, but without passing information in the <strong>ptuplelimits</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (that is, <em>grbit</em> has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="2a44d-143">Pasando una definición de clave no válida en el miembro <strong>szKey</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="2a44d-143">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="2a44d-144">Consulte <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> para obtener una descripción de las definiciones válidas.</span><span class="sxs-lookup"><span data-stu-id="2a44d-144">See <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="2a44d-145">Establecer el miembro <strong>cbVarSegMac</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> para que sea mayor que JET_cbPrimaryKeyMost (para un índice principal) o mayor que JET_cbSecondaryKeyMost (para un índice secundario).</span><span class="sxs-lookup"><span data-stu-id="2a44d-145">Setting the <strong>cbVarSegMac</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="2a44d-146">Pasar una combinación no válida para un índice Unicode definido por el usuario (uno que tiene el bit de JET_bitIndexUnicode establecido en el miembro <strong>grbit</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span><span class="sxs-lookup"><span data-stu-id="2a44d-146">Passing an invalid combination for a user-defined Unicode index (one which has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span></span> <span data-ttu-id="2a44d-147">Algunas causas comunes pueden ser que el campo pidxunicode de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> sea NULL o que el LCID especificado en la estructura pidxunicode no sea válido.</span><span class="sxs-lookup"><span data-stu-id="2a44d-147">Some common causes may be that the pidxunicode field of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is NULL, or the LCID specified in the pidxunicode structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="2a44d-148">Especificar una columna de varios valores para un índice principal.</span><span class="sxs-lookup"><span data-stu-id="2a44d-148">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="2a44d-149">Intentando indexar demasiadas columnas condicionales.</span><span class="sxs-lookup"><span data-stu-id="2a44d-149">Trying to index too many conditional columns.</span></span> <span data-ttu-id="2a44d-150">El miembro <strong>cConditionalColumn</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> no debe ser mayor que JET_ccolKeyMost.</span><span class="sxs-lookup"><span data-stu-id="2a44d-150">The <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a44d-151">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="2a44d-151">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="2a44d-152">Windows XP y versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="2a44d-152">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="2a44d-153">Se especificó una estructura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> y no se admiten sus límites.</span><span class="sxs-lookup"><span data-stu-id="2a44d-153">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="2a44d-154">Vea la sección Comentarios de la estructura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="2a44d-154">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a44d-155">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="2a44d-155">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="2a44d-156">Windows XP y versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="2a44d-156">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="2a44d-157">Un índice de tupla no puede ser único (<em>grbit</em> no debe tener JET_bitIndexTuples y JET_bitIndexUnique establecer).</span><span class="sxs-lookup"><span data-stu-id="2a44d-157">A tuple index cannot be unique (<em>grbit</em> must not have both JET_bitIndexTuples and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a44d-158">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="2a44d-158">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="2a44d-159">Windows XP y versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="2a44d-159">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="2a44d-160">Un índice de tupla solo puede estar en una sola columna (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tiene JET_bitIndexTuples establecido y el miembro <strong>szKey</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> especifica más de una columna).</span><span class="sxs-lookup"><span data-stu-id="2a44d-160">A tuple index can only be over a single column (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a44d-161">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="2a44d-161">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="2a44d-162">Windows XP y versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="2a44d-162">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="2a44d-163">Un índice de tupla no puede ser un índice principal (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> no debe tener establecido JET_bitIndexPrimary y JET_bitIndexTuples).</span><span class="sxs-lookup"><span data-stu-id="2a44d-163">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a44d-164">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="2a44d-164">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="2a44d-165">Windows XP y versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="2a44d-165">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="2a44d-166">Un índice de tupla solo puede estar en una columna de texto o Unicode.</span><span class="sxs-lookup"><span data-stu-id="2a44d-166">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="2a44d-167">Un intento de indizar otras columnas (por ejemplo, columnas binarias) dará como resultado JET_errIndexTuplesTextColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="2a44d-167">An attempt to index other columns (for example, binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a44d-168">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="2a44d-168">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="2a44d-169">Windows XP y versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="2a44d-169">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="2a44d-170">Un índice de tupla no permite establecer el miembro <strong>cbVarSegMac</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="2a44d-170">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a44d-171">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="2a44d-171">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="2a44d-172">Se intentó crear un índice sin información de versión mientras estaba en una transacción.</span><span class="sxs-lookup"><span data-stu-id="2a44d-172">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a44d-173">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="2a44d-173">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="2a44d-174">La definición del índice no es válida porque el miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> contiene valores incoherentes.</span><span class="sxs-lookup"><span data-stu-id="2a44d-174">The index definition is invalid because the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure contains inconsistent values.</span></span> <span data-ttu-id="2a44d-175">A continuación se indican algunas razones posibles:</span><span class="sxs-lookup"><span data-stu-id="2a44d-175">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="2a44d-176">Un índice principal tenía un bit omitido especificado (JET_bitIndexPrimary se pasó con uno de JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull o JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="2a44d-176">A primary index had an ignore bit specified (JET_bitIndexPrimary was passed with one of JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="2a44d-177">Un índice vacío no omite los campos NULOs (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tiene JET_bitIndexEmpty establecido, pero no tiene JET_bitIndexIgnoreAnyNull establecida).</span><span class="sxs-lookup"><span data-stu-id="2a44d-177">An empty index does not ignore any NULL fields (that is, <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="2a44d-178">Pasando una estructura de <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> con un miembro <strong>grbit</strong> no válido.</span><span class="sxs-lookup"><span data-stu-id="2a44d-178">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span> <span data-ttu-id="2a44d-179">Vea <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span><span class="sxs-lookup"><span data-stu-id="2a44d-179">See <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span></span></p></li>
</ul>
<p><span data-ttu-id="2a44d-180">Al crear varios índices a la vez (es decir, si el parámetro <em>cIndexCreate</em> es mayor que uno), ninguno de los índices puede contener ninguno de los bits siguientes:</span><span class="sxs-lookup"><span data-stu-id="2a44d-180">When creating several indexes at once (that is, if the <em>cIndexCreate</em> parameter is greater than one), none of the indexes may contain any of the following bits:</span></span></p>
<ul>
<li><p><span data-ttu-id="2a44d-181">JET_bitIndexPrimary</span><span class="sxs-lookup"><span data-stu-id="2a44d-181">JET_bitIndexPrimary</span></span></p></li>
<li><p><span data-ttu-id="2a44d-182">JET_bitIndexUnversioned</span><span class="sxs-lookup"><span data-stu-id="2a44d-182">JET_bitIndexUnversioned</span></span></p></li>
<li><p><span data-ttu-id="2a44d-183">JET_bitIndexEmpty</span><span class="sxs-lookup"><span data-stu-id="2a44d-183">JET_bitIndexEmpty</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a44d-184">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="2a44d-184">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="2a44d-185">Se pasó un ID. de configuración regional (LCID) no válido (ya sea a través del miembro <strong>LCID</strong> en la estructura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , que el miembro <strong>pidxunicode</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> contiene un puntero a o a través del miembro <strong>LCID</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span><span class="sxs-lookup"><span data-stu-id="2a44d-185">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member in the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure, which the <strong>pidxunicode</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure contains a pointer to, or through the <strong>lcid</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a44d-186">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="2a44d-186">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="2a44d-187">Se especificó un nombre de índice no válido.</span><span class="sxs-lookup"><span data-stu-id="2a44d-187">An invalid index name was specified.</span></span> <span data-ttu-id="2a44d-188">Consulte <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="2a44d-188">See <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a44d-189">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="2a44d-189">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="2a44d-190">Se pasó un parámetro no válido a la API.</span><span class="sxs-lookup"><span data-stu-id="2a44d-190">An invalid parameter was passed into the API.</span></span> <span data-ttu-id="2a44d-191">A continuación se indican algunos de los motivos por los que se puede devolver este error:</span><span class="sxs-lookup"><span data-stu-id="2a44d-191">The following are some reasons why this error may be returned:</span></span></p>
<ul>
<li><p><span data-ttu-id="2a44d-192">El campo <strong>cbKey</strong> de una estructura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="2a44d-192">The <strong>cbKey</strong> field of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="2a44d-193">El miembro <strong>cbStruct</strong> de una estructura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> no se establece en sizeof ( <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span><span class="sxs-lookup"><span data-stu-id="2a44d-193">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is not set to sizeof( <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a44d-194">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="2a44d-194">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="2a44d-195">Error al intentar normalizar una columna Unicode.</span><span class="sxs-lookup"><span data-stu-id="2a44d-195">An error occurred while trying to normalize a Unicode column.</span></span> <span data-ttu-id="2a44d-196">Esto puede deberse a la falta de recursos del sistema.</span><span class="sxs-lookup"><span data-stu-id="2a44d-196">This can be caused by running out of system resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a44d-197">JET_errSpaceHintsInvalid</span><span class="sxs-lookup"><span data-stu-id="2a44d-197">JET_errSpaceHintsInvalid</span></span></p></td>
<td><p><span data-ttu-id="2a44d-198">Un elemento de la estructura de sugerencias de espacio JET no era correcto o accionable.</span><span class="sxs-lookup"><span data-stu-id="2a44d-198">An element of the JET space hints structure was not correct or actionable.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="2a44d-199">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a44d-199">Remarks</span></span>

<span data-ttu-id="2a44d-200">El valor devuelto es JET_errSuccess si se completan correctamente todos los índices especificados.</span><span class="sxs-lookup"><span data-stu-id="2a44d-200">The return value is JET_errSuccess on successful completion of all indexes specified.</span></span>

<span data-ttu-id="2a44d-201">**JetCreateIndex3** recorre en iteración los índices proporcionados en **pindexcreate** y a veces se anulará en el primer error.</span><span class="sxs-lookup"><span data-stu-id="2a44d-201">**JetCreateIndex3** iterates through the indexes given in **pindexcreate**, and will sometimes abort on the first failure.</span></span> <span data-ttu-id="2a44d-202">Es posible que no se haya intentado ningún índice después del primer índice con un error, aunque el miembro **Err** de la estructura [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) contiene JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="2a44d-202">Any indexes after the first index with an error may not have been attempted, even though the **err** member of the [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structure contains JET_errSuccess.</span></span>

#### <a name="requirements"></a><span data-ttu-id="2a44d-203">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a44d-203">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2a44d-204"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="2a44d-204"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2a44d-205">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="2a44d-205">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a44d-206"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="2a44d-206"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2a44d-207">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="2a44d-207">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a44d-208"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="2a44d-208"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2a44d-209">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="2a44d-209">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a44d-210"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="2a44d-210"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="2a44d-211">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="2a44d-211">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a44d-212"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="2a44d-212"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="2a44d-213">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="2a44d-213">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a44d-214"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="2a44d-214"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="2a44d-215">Se implementa como <strong>JetCreateIndex3W</strong> (Unicode) y <strong>JetCreateIndex3A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="2a44d-215">Implemented as <strong>JetCreateIndex3W</strong> (Unicode) and <strong>JetCreateIndex3A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="2a44d-216">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2a44d-216">See Also</span></span>

[<span data-ttu-id="2a44d-217">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="2a44d-217">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="2a44d-218">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="2a44d-218">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="2a44d-219">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="2a44d-219">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="2a44d-220">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="2a44d-220">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="2a44d-221">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="2a44d-221">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="2a44d-222">JET_INDEXCREATE2</span><span class="sxs-lookup"><span data-stu-id="2a44d-222">JET_INDEXCREATE2</span></span>](./jet-indexcreate2-structure.md)  
[<span data-ttu-id="2a44d-223">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="2a44d-223">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="2a44d-224">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="2a44d-224">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="2a44d-225">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="2a44d-225">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="2a44d-226">JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="2a44d-226">JET_SPACEHINTS</span></span>](./jet-spacehints-structure.md)
