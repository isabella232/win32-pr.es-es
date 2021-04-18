---
description: 'Más información acerca de: JetCreateIndex4W (función)'
title: Función JetCreateIndex4W
TOCTitle: JetCreateIndex4W Function
ms:assetid: 968745a2-66ce-4c7f-ab5b-43282adc5313
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835044(v=EXCHG.10)
ms:contentKeyID: 49894666
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCreateIndex4W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a4c7671cbe361b6214552f4c611cd1706c0e48d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716605"
---
# <a name="jetcreateindex4w-function"></a><span data-ttu-id="2f1ba-103">Función JetCreateIndex4W</span><span class="sxs-lookup"><span data-stu-id="2f1ba-103">JetCreateIndex4W Function</span></span>


<span data-ttu-id="2f1ba-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2f1ba-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="2f1ba-105">La función **JetCreateIndex4W** crea índices sobre los datos en una base de datos del motor de almacenamiento extensible (ese), que se puede usar para buscar datos específicos rápidamente.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-105">The **JetCreateIndex4W** function creates indexes over data in an Extensible Storage Engine (ESE) database, which can be used to locate specific data quickly.</span></span>

<span data-ttu-id="2f1ba-106">La función **JetCreateIndex4W** se presentó en el sistema operativo Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-106">The **JetCreateIndex4W** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetCreateIndex4W(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_INDEXCREATE2* pindexcreate,
  __in          unsigned long cIndexCreate
);
```

### <a name="parameters"></a><span data-ttu-id="2f1ba-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f1ba-107">Parameters</span></span>

<span data-ttu-id="2f1ba-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="2f1ba-108">*sesid*</span></span>

<span data-ttu-id="2f1ba-109">Contexto de sesión de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="2f1ba-110">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="2f1ba-110">*tableid*</span></span>

<span data-ttu-id="2f1ba-111">Tabla en la que se creará el índice.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-111">The table on which the index will be created.</span></span>

<span data-ttu-id="2f1ba-112">*pindexcreate*</span><span class="sxs-lookup"><span data-stu-id="2f1ba-112">*pindexcreate*</span></span>

<span data-ttu-id="2f1ba-113">Matriz de estructuras de [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) , cada una de las cuales define un índice que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-113">An array of [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structures, each of which defines an index to be created.</span></span>

<span data-ttu-id="2f1ba-114">*cIndexCreate*</span><span class="sxs-lookup"><span data-stu-id="2f1ba-114">*cIndexCreate*</span></span>

<span data-ttu-id="2f1ba-115">Número de elementos de la matriz *pindexcreate* .</span><span class="sxs-lookup"><span data-stu-id="2f1ba-115">The number of elements in the *pindexcreate* array.</span></span>

### <a name="return-value"></a><span data-ttu-id="2f1ba-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f1ba-116">Return value</span></span>

<span data-ttu-id="2f1ba-117">Esta función devuelve el tipo de datos [JET_ERR](./jet-err.md) con uno de los códigos de retorno que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-117">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="2f1ba-118">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="2f1ba-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2f1ba-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2f1ba-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="2f1ba-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f1ba-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f1ba-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="2f1ba-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="2f1ba-122">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f1ba-123">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="2f1ba-123">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="2f1ba-124">Se intentó indexar sobre una columna de actualización de custodia o de SLV (tenga en cuenta que las columnas de SLV están desusadas).</span><span class="sxs-lookup"><span data-stu-id="2f1ba-124">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f1ba-125">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="2f1ba-125">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="2f1ba-126">Se intentó indizar una columna que no existe.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-126">An attempt was made to index over a nonexistent column.</span></span> <span data-ttu-id="2f1ba-127">Un intento de indexación condicional de una columna no existente también puede generar este error.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-127">An attempt to conditionally index over a nonexistent column can also produce this error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f1ba-128">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="2f1ba-128">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="2f1ba-129">Este error se devolverá si el miembro <strong>ulDensity</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> está establecido en un número menor que 20 o mayor que 100.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-129">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to a number less than 20 or greater than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f1ba-130">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="2f1ba-130">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="2f1ba-131">Se ha intentado definir dos índices idénticos.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-131">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f1ba-132">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="2f1ba-132">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="2f1ba-133">Se intentó especificar más de un índice principal para una tabla.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-133">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="2f1ba-134">Una tabla debe tener exactamente un índice principal.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-134">A table must have exactly one primary index.</span></span> <span data-ttu-id="2f1ba-135">Si no se especifica ningún índice principal, el motor de base de datos creará uno de forma transparente.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-135">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f1ba-136">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="2f1ba-136">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="2f1ba-137">Se especificó una definición de índice no válida.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-137">An invalid index definition was specified.</span></span> <span data-ttu-id="2f1ba-138">A continuación se indican algunas de las razones posibles de este error:</span><span class="sxs-lookup"><span data-stu-id="2f1ba-138">The following are some possible reasons for this error:</span></span></p>
<ul>
<li><p><span data-ttu-id="2f1ba-139">Un índice principal es condicional (el miembro<strong>grbit</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tiene <strong>JET_bitIndexPrimary</strong> establecido y el miembro <strong>cConditionalColumn</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> es mayor que cero).</span><span class="sxs-lookup"><span data-stu-id="2f1ba-139">A primary index is conditional (<strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> has <strong>JET_bitIndexPrimary</strong> set, and the <strong>cConditionalColumn</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="2f1ba-140">Se aplica a las versiones de Windows a partir de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-140">Applies to versions of Windows starting with Windows Server 2003.</span></span> <span data-ttu-id="2f1ba-141">Se intentó crear un índice de tupla con límites de tupla, pero sin pasar información en el miembro <strong>ptuplelimits</strong> en <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (es decir, <em>grbit</em> se ha establecido <strong>JET_bitIndexTupleLimits</strong> , pero el puntero <strong>ptuplelimits</strong> es null).</span><span class="sxs-lookup"><span data-stu-id="2f1ba-141">An attempt was made to create a tuple index with tuple limits, but without passing information in the <strong>ptuplelimits</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (that is, <em>grbit</em> has <strong>JET_bitIndexTupleLimits</strong> set, but the <strong>ptuplelimits</strong> pointer is null).</span></span></p></li>
<li><p><span data-ttu-id="2f1ba-142">Pasando una definición de clave no válida en el miembro <strong>szKey</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="2f1ba-142">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="2f1ba-143">Para obtener información sobre las definiciones válidas, vea <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-143">For information about valid definitions, see <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</span></span></p></li>
<li><p><span data-ttu-id="2f1ba-144">Establecer el miembro <strong>cbVarSegMac</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> para que sea mayor que <strong>JET_cbPrimaryKeyMost</strong> (para un índice principal) o mayor que <strong>JET_cbSecondaryKeyMost</strong> (para un índice secundario).</span><span class="sxs-lookup"><span data-stu-id="2f1ba-144">Setting the <strong>cbVarSegMac</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> to be greater than <strong>JET_cbPrimaryKeyMost</strong> (for a primary index) or greater than <strong>JET_cbSecondaryKeyMost</strong> (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="2f1ba-145">Pasar una combinación no válida para un índice Unicode definido por el usuario (uno que tiene el bit de <strong>JET_bitIndexUnicode</strong> establecido en el miembro <strong>grbit</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span><span class="sxs-lookup"><span data-stu-id="2f1ba-145">Passing an invalid combination for a user-defined Unicode index (one which has the <strong>JET_bitIndexUnicode</strong> bit set in the <strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span></span> <span data-ttu-id="2f1ba-146">Algunas causas comunes pueden ser que el campo pidxunicode de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> sea NULL o que el LCID especificado en la estructura pidxunicode no sea válido.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-146">Some common causes may be that the pidxunicode field of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is null, or the LCID specified in the pidxunicode structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="2f1ba-147">Especificar una columna multivalor para un índice principal.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-147">Specifying a multivalued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="2f1ba-148">Intentando indexar demasiadas columnas condicionales.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-148">Trying to index too many conditional columns.</span></span> <span data-ttu-id="2f1ba-149">El miembro <strong>cConditionalColumn</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> no debe ser mayor que <strong>JET_ccolKeyMost</strong>.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-149">The <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not be greater than <strong>JET_ccolKeyMost</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f1ba-150">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="2f1ba-150">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="2f1ba-151">Se aplica a las versiones de Windows a partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-151">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="2f1ba-152">Se especificó una estructura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> y no se admiten sus límites.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-152">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="2f1ba-153">Para obtener más información, vea la sección Comentarios de la estructura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="2f1ba-153">For more information, see the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f1ba-154">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="2f1ba-154">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="2f1ba-155">Se aplica a las versiones de Windows a partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-155">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="2f1ba-156">Un índice de tupla no puede ser único (<em>grbit</em> no debe tener <strong>JET_bitIndexTuples</strong> y <strong>JET_bitIndexUnique</strong> establecer).</span><span class="sxs-lookup"><span data-stu-id="2f1ba-156">A tuple index cannot be unique (<em>grbit</em> must not have both <strong>JET_bitIndexTuples</strong> and <strong>JET_bitIndexUnique</strong> set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f1ba-157">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="2f1ba-157">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="2f1ba-158">Se aplica a las versiones de Windows a partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-158">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="2f1ba-159">Un índice de tupla solo puede estar en una sola columna (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tiene <strong>JET_bitIndexTuples</strong> establecido y el miembro <strong>szKey</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> especifica más de una columna).</span><span class="sxs-lookup"><span data-stu-id="2f1ba-159">A tuple index can only be over a single column (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has <strong>JET_bitIndexTuples</strong> set, and the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f1ba-160">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="2f1ba-160">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="2f1ba-161">Se aplica a las versiones de Windows a partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-161">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="2f1ba-162">Un índice de tupla no puede ser un índice principal (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> no debe tener establecido <strong>JET_bitIndexPrimary</strong> y <strong>JET_bitIndexTuples</strong> ).</span><span class="sxs-lookup"><span data-stu-id="2f1ba-162">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both <strong>JET_bitIndexPrimary</strong> and <strong>JET_bitIndexTuples</strong> set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f1ba-163">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="2f1ba-163">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="2f1ba-164">Se aplica a las versiones de Windows a partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-164">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="2f1ba-165">Un índice de tupla solo puede estar en una columna de texto o Unicode.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-165">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="2f1ba-166">Un intento de indizar otras columnas (por ejemplo, columnas binarias) dará como resultado <strong>JET_errIndexTuplesTextColumnsOnly</strong>.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-166">An attempt to index other columns (for example, binary columns) will result in <strong>JET_errIndexTuplesTextColumnsOnly</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f1ba-167">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="2f1ba-167">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="2f1ba-168">Se aplica a las versiones de Windows a partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-168">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="2f1ba-169">Un índice de tupla no permite establecer el miembro <strong>cbVarSegMac</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="2f1ba-169">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f1ba-170">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="2f1ba-170">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="2f1ba-171">Se intentó crear un índice sin información de versión mientras estaba en una transacción.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-171">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f1ba-172">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="2f1ba-172">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="2f1ba-173">La definición del índice no es válida porque el miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> contiene valores incoherentes.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-173">The index definition is invalid because the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure contains inconsistent values.</span></span> <span data-ttu-id="2f1ba-174">A continuación se indican algunas razones posibles:</span><span class="sxs-lookup"><span data-stu-id="2f1ba-174">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="2f1ba-175">Un índice principal tenía un bit omitido especificado (JET_bitIndexPrimary se pasó con uno de <strong>JET_bitIndexIgnoreNull</strong>, <strong>JET_bitIndexIgnoreAnyNull</strong>o <strong>JET_bitIndexIgnoreFirstNull</strong>).</span><span class="sxs-lookup"><span data-stu-id="2f1ba-175">A primary index had an ignore bit specified (JET_bitIndexPrimary was passed with one of <strong>JET_bitIndexIgnoreNull</strong>, <strong>JET_bitIndexIgnoreAnyNull</strong>, or <strong>JET_bitIndexIgnoreFirstNull</strong>).</span></span></p></li>
<li><p><span data-ttu-id="2f1ba-176">Un índice vacío no omite los campos nulos (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tiene <strong>JET_bitIndexEmpty</strong> establecido, pero no tiene <strong>JET_bitIndexIgnoreAnyNull</strong> establecida).</span><span class="sxs-lookup"><span data-stu-id="2f1ba-176">An empty index does not ignore any null fields (that is, <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has <strong>JET_bitIndexEmpty</strong> set, but does not have <strong>JET_bitIndexIgnoreAnyNull</strong> set).</span></span></p></li>
<li><p><span data-ttu-id="2f1ba-177">Pasando una estructura de <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> con un miembro <strong>grbit</strong> no válido.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-177">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span> <span data-ttu-id="2f1ba-178">Vea <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-178">See <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span></span></p></li>
</ul>
<p><span data-ttu-id="2f1ba-179">Al crear varios índices a la vez (es decir, si el parámetro <em>cIndexCreate</em> es mayor que uno), ninguno de los índices puede contener ninguno de los bits siguientes:</span><span class="sxs-lookup"><span data-stu-id="2f1ba-179">When creating several indexes at once (that is, if the <em>cIndexCreate</em> parameter is greater than one), none of the indexes may contain any of the following bits:</span></span></p>
<ul>
<li><p><span data-ttu-id="2f1ba-180"><strong>JET_bitIndexPrimary</strong></span><span class="sxs-lookup"><span data-stu-id="2f1ba-180"><strong>JET_bitIndexPrimary</strong></span></span></p></li>
<li><p><span data-ttu-id="2f1ba-181"><strong>JET_bitIndexUnversioned</strong></span><span class="sxs-lookup"><span data-stu-id="2f1ba-181"><strong>JET_bitIndexUnversioned</strong></span></span></p></li>
<li><p><span data-ttu-id="2f1ba-182"><strong>JET_bitIndexEmpty</strong></span><span class="sxs-lookup"><span data-stu-id="2f1ba-182"><strong>JET_bitIndexEmpty</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f1ba-183">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="2f1ba-183">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="2f1ba-184">Se pasó un ID. de configuración regional (LCID) no válido (ya sea a través del miembro <strong>LCID</strong> en la estructura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , que el miembro <strong>pidxunicode</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> contiene un puntero a o a través del miembro <strong>LCID</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span><span class="sxs-lookup"><span data-stu-id="2f1ba-184">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member in the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure, which the <strong>pidxunicode</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure contains a pointer to, or through the <strong>lcid</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f1ba-185">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="2f1ba-185">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="2f1ba-186">Se especificó un nombre de índice no válido.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-186">An invalid index name was specified.</span></span> <span data-ttu-id="2f1ba-187">Consulte <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-187">See <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f1ba-188">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="2f1ba-188">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="2f1ba-189">Se pasó un parámetro no válido a la API.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-189">An invalid parameter was passed into the API.</span></span> <span data-ttu-id="2f1ba-190">A continuación se indican algunos de los motivos por los que se puede devolver este error:</span><span class="sxs-lookup"><span data-stu-id="2f1ba-190">The following are some reasons why this error may be returned:</span></span></p>
<ul>
<li><p><span data-ttu-id="2f1ba-191">El campo <strong>cbKey</strong> de una estructura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-191">The <strong>cbKey</strong> field of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="2f1ba-192">El miembro <strong>cbStruct</strong> de una estructura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> no se establece en sizeof (JET_INDEXCREATE2).</span><span class="sxs-lookup"><span data-stu-id="2f1ba-192">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is not set to sizeof(JET_INDEXCREATE2).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f1ba-193">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="2f1ba-193">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="2f1ba-194">Error al intentar normalizar una columna Unicode.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-194">An error occurred while trying to normalize a Unicode column.</span></span> <span data-ttu-id="2f1ba-195">Esto puede deberse a la falta de recursos del sistema.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-195">This can be caused by running out of system resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f1ba-196">JET_errSpaceHintsInvalid</span><span class="sxs-lookup"><span data-stu-id="2f1ba-196">JET_errSpaceHintsInvalid</span></span></p></td>
<td><p><span data-ttu-id="2f1ba-197">Un elemento de la estructura de sugerencias de espacio JET no era correcto o accionable.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-197">An element of the JET space hints structure was not correct or actionable.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="2f1ba-198">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f1ba-198">Remarks</span></span>

<span data-ttu-id="2f1ba-199">La función **JetCreateIndex4W** recorre en iteración los índices especificados en el parámetro *pindexcreate* y a veces se anulará en el primer error.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-199">The **JetCreateIndex4W** function iterates through the indexes given in the *pindexcreate* parameter, and will sometimes abort on the first failure.</span></span> <span data-ttu-id="2f1ba-200">Es posible que no se haya intentado ningún índice después del primer índice con un error, aunque el miembro **Err** de la estructura [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) contiene JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-200">Any indexes after the first index with an error may not have been attempted, even though the **err** member of the [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structure contains JET_errSuccess.</span></span>

#### <a name="requirements"></a><span data-ttu-id="2f1ba-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f1ba-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f1ba-202"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="2f1ba-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2f1ba-203">Requiere Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-203">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f1ba-204"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="2f1ba-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2f1ba-205">Requiere Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-205">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f1ba-206"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="2f1ba-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2f1ba-207">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-207">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f1ba-208"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="2f1ba-208"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="2f1ba-209">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-209">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f1ba-210"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="2f1ba-210"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="2f1ba-211">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-211">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="2f1ba-212">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f1ba-212">See also</span></span>

[<span data-ttu-id="2f1ba-213">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="2f1ba-213">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="2f1ba-214">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="2f1ba-214">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="2f1ba-215">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="2f1ba-215">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="2f1ba-216">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="2f1ba-216">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="2f1ba-217">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="2f1ba-217">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="2f1ba-218">JET_INDEXCREATE2</span><span class="sxs-lookup"><span data-stu-id="2f1ba-218">JET_INDEXCREATE2</span></span>](./jet-indexcreate2-structure.md)  
[<span data-ttu-id="2f1ba-219">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="2f1ba-219">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="2f1ba-220">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="2f1ba-220">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="2f1ba-221">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="2f1ba-221">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="2f1ba-222">JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="2f1ba-222">JET_SPACEHINTS</span></span>](./jet-spacehints-structure.md)
