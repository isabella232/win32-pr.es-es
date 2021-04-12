---
description: 'Más información acerca de: JetEnumerateColumns (función)'
title: Función JetEnumerateColumns
TOCTitle: JetEnumerateColumns Function
ms:assetid: 8413d056-cdb1-420e-9dd3-7280ad510165
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269321(v=EXCHG.10)
ms:contentKeyID: 32765611
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEnumerateColumns
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b913fb970232ca6f0fc21eb846df85e1db684f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277859"
---
# <a name="jetenumeratecolumns-function"></a><span data-ttu-id="dc381-103">Función JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="dc381-103">JetEnumerateColumns Function</span></span>


<span data-ttu-id="dc381-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="dc381-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetenumeratecolumns-function"></a><span data-ttu-id="dc381-105">Función JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="dc381-105">JetEnumerateColumns Function</span></span>

<span data-ttu-id="dc381-106">La función **JetEnumerateColumns** recupera eficazmente un conjunto de columnas y sus valores del registro actual de un cursor o del búfer de copia de ese cursor.</span><span class="sxs-lookup"><span data-stu-id="dc381-106">The **JetEnumerateColumns** function efficiently retrieves a set of columns and their values from the current record of a cursor or the copy buffer of that cursor.</span></span> <span data-ttu-id="dc381-107">Las columnas y los valores recuperados se pueden restringir por una lista de identificadores de columna, números de *itagSequence* y otras características.</span><span class="sxs-lookup"><span data-stu-id="dc381-107">The columns and values retrieved can be restricted by a list of column IDs, *itagSequence* numbers, and other characteristics.</span></span> <span data-ttu-id="dc381-108">Esta API de recuperación de columnas es única, ya que devuelve información en memoria asignada dinámicamente que se obtiene mediante una devolución de llamada compatible con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) proporcionada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="dc381-108">This column retrieval API is unique in that it returns information in dynamically allocated memory that is obtained using a user-provided [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback.</span></span> <span data-ttu-id="dc381-109">Esta nueva flexibilidad permite la recuperación eficaz de datos de columna con características específicas (como el tamaño y la multiplicidad) que son desconocidas para el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="dc381-109">This new flexibility permits the efficient retrieval of column data with specific characteristics (such as size and multiplicity) that are unknown to the caller.</span></span> <span data-ttu-id="dc381-110">Esto elimina la necesidad de usar los modos de detección de [JetRetrieveColumn](./jetretrievecolumn-function.md) para determinar esas características a fin de configurar una llamada final a [JetRetrieveColumn](./jetretrievecolumn-function.md) que recupere correctamente los datos deseados.</span><span class="sxs-lookup"><span data-stu-id="dc381-110">This eliminates the need for the use of the discovery modes of [JetRetrieveColumn](./jetretrievecolumn-function.md) to determine those characteristics in order to setup a final call to [JetRetrieveColumn](./jetretrievecolumn-function.md) that will successfully retrieve the desired data.</span></span>

<span data-ttu-id="dc381-111">**Windows XP: JetEnumerateColumns** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="dc381-111">**Windows XP:  JetEnumerateColumns** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetEnumerateColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          unsigned long cEnumColumnId,
      __in_opt      JET_ENUMCOLUMNID* rgEnumColumnId,
      __out         unsigned long* pcEnumColumn,
      __out         JET_ENUMCOLUMN** prgEnumColumn,
      __in          JET_PFNREALLOC pfnRealloc,
      __in          void* pvReallocContext,
      __in          unsigned long cbDataMost,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="dc381-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc381-112">Parameters</span></span>

<span data-ttu-id="dc381-113">*sesid*</span><span class="sxs-lookup"><span data-stu-id="dc381-113">*sesid*</span></span>

<span data-ttu-id="dc381-114">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="dc381-114">The session to use for this call.</span></span>

<span data-ttu-id="dc381-115">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="dc381-115">*tableid*</span></span>

<span data-ttu-id="dc381-116">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="dc381-116">The cursor to use for this call.</span></span>

<span data-ttu-id="dc381-117">*cEnumColumnId*</span><span class="sxs-lookup"><span data-stu-id="dc381-117">*cEnumColumnId*</span></span>

<span data-ttu-id="dc381-118">Una matriz de identificadores de columna, cada uno con una matriz opcional de números *itagSequence* para enumerar.</span><span class="sxs-lookup"><span data-stu-id="dc381-118">An array of column IDs, each with an optional array of *itagSequence* numbers to enumerate.</span></span>

<span data-ttu-id="dc381-119">Si *cEnumColumnId* es 0 (cero), *rgEnumColumnId* se omite y todos los valores de columna se enumeran y se devuelven al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="dc381-119">If *cEnumColumnId* is 0 (zero) then *rgEnumColumnId* is ignored and all column values are enumerated and returned to the caller.</span></span> <span data-ttu-id="dc381-120">Si un elemento de la matriz de ID. de columna hace referencia a un ID. de columna de 0 (cero), se omitirá la enumeración de esa columna y se generará una ranura correspondiente en la salida con un estado de columna de JET_wrnColumnSkipped.</span><span class="sxs-lookup"><span data-stu-id="dc381-120">If an element of the column ID array refers to a column ID of 0 (zero) then enumeration of that column is skipped and a corresponding slot in the output will be generated with a column status of JET_wrnColumnSkipped.</span></span>

<span data-ttu-id="dc381-121">Si *ctagSequence* es 0 (cero) para un elemento determinado de la matriz de ID. de columna, se omite *rgtagSequence* y se enumeran todos los valores de columna para ese ID. de columna y se devuelven al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="dc381-121">If *ctagSequence* is 0 (zero) for a given element of the column ID array then *rgtagSequence* is ignored and all column values for that column ID are enumerated and returned to the caller.</span></span> <span data-ttu-id="dc381-122">Si un elemento de una matriz de números de *itagSequence* hace referencia a un número de *itagSequence* de 0 (cero), se omite la enumeración de ese número *itagSequence* y se generará una ranura correspondiente en la salida con un estado de valor de columna de JET_wrnColumnSkipped.</span><span class="sxs-lookup"><span data-stu-id="dc381-122">If an element of an *itagSequence* number array refers to a *itagSequence* number of 0 (zero) then the enumeration of that *itagSequence* number is skipped and a corresponding slot in the output will be generated with a column value status of JET_wrnColumnSkipped.</span></span>

<span data-ttu-id="dc381-123">*rgEnumColumnId*</span><span class="sxs-lookup"><span data-stu-id="dc381-123">*rgEnumColumnId*</span></span>

<span data-ttu-id="dc381-124">Vea *cEnumColumnId*.</span><span class="sxs-lookup"><span data-stu-id="dc381-124">See *cEnumColumnId*.</span></span>

<span data-ttu-id="dc381-125">*pcEnumColumn*</span><span class="sxs-lookup"><span data-stu-id="dc381-125">*pcEnumColumn*</span></span>

<span data-ttu-id="dc381-126">Devuelve la matriz enumerada de columnas y sus valores en la memoria asignada a través de la devolución de llamada compatible con *itagSequence* proporcionada.</span><span class="sxs-lookup"><span data-stu-id="dc381-126">Returns the enumerated array of columns and their values in memory allocated through the provided *itagSequence* compatible callback.</span></span>

<span data-ttu-id="dc381-127">Si se solicita una matriz de identificadores de columna en la entrada, el orden y el tamaño de la matriz de salida reflejarán el orden y el tamaño de la matriz de entrada.</span><span class="sxs-lookup"><span data-stu-id="dc381-127">If an array of column IDs is requested on input then the order and size of the output array will reflect the order and size of the input array.</span></span> <span data-ttu-id="dc381-128">Del mismo modo, si se solicita una matriz de números *itagSequence* para un identificador de columna determinado en la entrada, el orden y el tamaño de la matriz de salida de los valores de columna de esa columna reflejará el orden y el tamaño de la matriz de entrada.</span><span class="sxs-lookup"><span data-stu-id="dc381-128">Similarly, if an array of *itagSequence* numbers is requested for a particular column ID on input then the order and size of the output array of column values for that column will reflect the order and size of the input array.</span></span>

<span data-ttu-id="dc381-129">Los parámetros de salida se establecen en 0 (cero) y **null** en cualquier error, excepto en JET_errBadColumnId y JET_errColumnNotFound.</span><span class="sxs-lookup"><span data-stu-id="dc381-129">The output parameters are set to 0 (zero) and **NULL** on any error except for JET_errBadColumnId and JET_errColumnNotFound.</span></span> <span data-ttu-id="dc381-130">Cuando se devuelven estos errores, los datos de salida son válidos y completos para todos los identificadores de columna afectados.</span><span class="sxs-lookup"><span data-stu-id="dc381-130">When these errors are returned, the output data is valid and complete for all but the affected column IDs.</span></span> <span data-ttu-id="dc381-131">El código de estado de cada uno de los identificadores de columna afectados se establece en uno de estos errores para que el autor de la llamada pueda determinar qué ID. de columna fueron incorrectos y, potencialmente, tomar medidas correctivas.</span><span class="sxs-lookup"><span data-stu-id="dc381-131">The status code for each of the affected column IDs is set to one of these errors so that the caller may determine which column IDs were bad and potentially take corrective action.</span></span>

<span data-ttu-id="dc381-132">*prgEnumColumn*</span><span class="sxs-lookup"><span data-stu-id="dc381-132">*prgEnumColumn*</span></span>

<span data-ttu-id="dc381-133">Vea *pcEnumColumn*.</span><span class="sxs-lookup"><span data-stu-id="dc381-133">See *pcEnumColumn*.</span></span>

<span data-ttu-id="dc381-134">*pfnRealloc*</span><span class="sxs-lookup"><span data-stu-id="dc381-134">*pfnRealloc*</span></span>

<span data-ttu-id="dc381-135">Identifica una devolución de llamada compatible con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) y un puntero de contexto opcional que se usa para asignar memoria para la matriz de salida de columnas y sus valores.</span><span class="sxs-lookup"><span data-stu-id="dc381-135">Identifies a [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback and an optional context pointer used to allocate memory for the output array of columns and their values.</span></span>

<span data-ttu-id="dc381-136">*pvReallocContext*</span><span class="sxs-lookup"><span data-stu-id="dc381-136">*pvReallocContext*</span></span>

<span data-ttu-id="dc381-137">Vea *pfnRealloc*.</span><span class="sxs-lookup"><span data-stu-id="dc381-137">See *pfnRealloc*.</span></span>

<span data-ttu-id="dc381-138">*cbDataMost*</span><span class="sxs-lookup"><span data-stu-id="dc381-138">*cbDataMost*</span></span>

<span data-ttu-id="dc381-139">Establece un límite en la cantidad de datos que se van a devolver de una columna de texto largo o binario largo.</span><span class="sxs-lookup"><span data-stu-id="dc381-139">Sets a cap on the amount of data to return from a long text or long binary column.</span></span>

<span data-ttu-id="dc381-140">Este parámetro se puede utilizar para evitar la enumeración de un valor de columna extremadamente grande.</span><span class="sxs-lookup"><span data-stu-id="dc381-140">This parameter can be used to prevent the enumeration of an extremely large column value.</span></span> <span data-ttu-id="dc381-141">Normalmente, este tipo de enumeración podría producir un error en la llamada de API con JET_errOutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="dc381-141">Ordinarily, such an enumeration might fail the API call with JET_errOutOfMemory.</span></span> <span data-ttu-id="dc381-142">Si un valor de columna grande se trunca de este modo, el estado del valor de la columna será JET_wrnColumnTruncated.</span><span class="sxs-lookup"><span data-stu-id="dc381-142">If a large column value is truncated in such a manner then the column value's status will be JET_wrnColumnTruncated.</span></span>

<span data-ttu-id="dc381-143">*grbit*</span><span class="sxs-lookup"><span data-stu-id="dc381-143">*grbit*</span></span>

<span data-ttu-id="dc381-144">Grupo de bits que especifica cero o más de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="dc381-144">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dc381-145">Value</span><span class="sxs-lookup"><span data-stu-id="dc381-145">Value</span></span></p></th>
<th><p><span data-ttu-id="dc381-146">Significado</span><span class="sxs-lookup"><span data-stu-id="dc381-146">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc381-147">JET_bitEnumerateCompressOutput</span><span class="sxs-lookup"><span data-stu-id="dc381-147">JET_bitEnumerateCompressOutput</span></span></p></td>
<td><p><span data-ttu-id="dc381-148">Al enumerar los valores de columna, todas las columnas para las que se recuperan todos los valores y que solo tienen un valor de columna que no es NULL pueden devolverse en un formato comprimido.</span><span class="sxs-lookup"><span data-stu-id="dc381-148">When enumerating column values, all columns for which we are retrieving all values and that have only one non-NULL column value may be returned in a compressed format.</span></span> <span data-ttu-id="dc381-149">El estado de estas columnas se establecerá en JET_wrnColumnSingleValue y el tamaño del valor de columna y la memoria que contiene el valor de columna se devolverán directamente en la estructura de <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> .</span><span class="sxs-lookup"><span data-stu-id="dc381-149">The status for such columns will be set to JET_wrnColumnSingleValue and the size of the column value and the memory containing the column value will be returned directly in the <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> structure.</span></span> <span data-ttu-id="dc381-150">No se garantiza que todas las columnas coincidentes se compriman de esta manera.</span><span class="sxs-lookup"><span data-stu-id="dc381-150">It is not guaranteed that all eligible columns are compressed in this manner.</span></span> <span data-ttu-id="dc381-151">Consulte <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="dc381-151">See <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc381-152">JET_bitEnumerateCopy</span><span class="sxs-lookup"><span data-stu-id="dc381-152">JET_bitEnumerateCopy</span></span></p></td>
<td><p><span data-ttu-id="dc381-153">Esta opción indica que los valores de columna modificados del registro se deben enumerar en lugar de los valores de columna originales.</span><span class="sxs-lookup"><span data-stu-id="dc381-153">This option indicates that the modified column values of the record should be enumerated rather than the original column values.</span></span> <span data-ttu-id="dc381-154">Si un valor de columna no se ha modificado, se enumera el valor de la columna original.</span><span class="sxs-lookup"><span data-stu-id="dc381-154">If a column value has not been modified, the original column value is enumerated.</span></span> <span data-ttu-id="dc381-155">De esta manera, se puede enumerar un valor de columna que todavía no se ha insertado o actualizado al insertar o actualizar un registro.</span><span class="sxs-lookup"><span data-stu-id="dc381-155">In this way, a column value that has not yet been inserted or updated may be enumerated when inserting or updating a record.</span></span></p>
<p><span data-ttu-id="dc381-156">Esta opción es idéntica a JET_bitRetrieveCopy cuando se usa con <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> o <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a>.</span><span class="sxs-lookup"><span data-stu-id="dc381-156">This option is identical to JET_bitRetrieveCopy when used with <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> or <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc381-157">JET_bitEnumerateIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="dc381-157">JET_bitEnumerateIgnoreDefault</span></span></p></td>
<td><p><span data-ttu-id="dc381-158">Si una columna determinada no está presente en el registro, no se devolverá ningún valor de columna.</span><span class="sxs-lookup"><span data-stu-id="dc381-158">If a given column is not present in the record then no column value will be returned.</span></span> <span data-ttu-id="dc381-159">Normalmente, el valor predeterminado de la columna, si existe, se devolvería en este caso.</span><span class="sxs-lookup"><span data-stu-id="dc381-159">Ordinarily, the default value for the column, if any, would be returned in this case.</span></span> <span data-ttu-id="dc381-160">Se garantiza que, si la columna se establece en un valor distinto del valor predeterminado, se devolverá un valor diferente (es decir, si una columna con un valor predeterminado se establece explícitamente en <strong>null</strong> , se devolverá un valor <strong>null</strong> como valor para esa columna).</span><span class="sxs-lookup"><span data-stu-id="dc381-160">It is guaranteed that if the column is set to a value different than the default value then that different value will be returned (that is, if a column with a default value is explicitly set to <strong>NULL</strong> then a <strong>NULL</strong> will be returned as the value for that column).</span></span> <span data-ttu-id="dc381-161">Tenga en cuenta que, aunque se solicite esta opción, sigue siendo posible ver un valor de columna que sea igual al valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="dc381-161">Note that, even if this option is requested, it is still possible to see a column value that happens to be equal to the default value.</span></span> <span data-ttu-id="dc381-162">No se realiza ningún esfuerzo para quitar los valores de columna que coincidan con sus valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="dc381-162">No effort is made to remove column values that match their default values.</span></span></p>
<p><span data-ttu-id="dc381-163">Es importante tener en cuenta que esta opción afecta a la salida de <strong>JetEnumerateColumns</strong> cuando se usa con JET_bitEnumeratePresenceOnly o JET_bitEnumerateTaggedOnly.</span><span class="sxs-lookup"><span data-stu-id="dc381-163">It is important to note that this option affects the output of <strong>JetEnumerateColumns</strong> when used with JET_bitEnumeratePresenceOnly or JET_bitEnumerateTaggedOnly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc381-164">JET_bitEnumerateIgnoreUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="dc381-164">JET_bitEnumerateIgnoreUserDefinedDefault</span></span></p></td>
<td><p><span data-ttu-id="dc381-165">Si una columna determinada no está presente en el registro y tiene un valor predeterminado definido por el usuario, no se devolverá ningún valor de columna.</span><span class="sxs-lookup"><span data-stu-id="dc381-165">If a given column is not present in the record and it has a user defined default value then no column value will be returned.</span></span> <span data-ttu-id="dc381-166">Esta opción impedirá que se llame a la devolución de llamada que calcula el valor predeterminado definido por el usuario para la columna al enumerar los valores de esa columna.</span><span class="sxs-lookup"><span data-stu-id="dc381-166">This option will prevent the callback that computes the user defined default value for the column from being called when enumerating the values for that column.</span></span></p>
<p><span data-ttu-id="dc381-167"><strong>Windows Server 2003 y versiones anteriores:  </strong> En Windows Server 2003 y versiones anteriores, se producirá un error en la operación con JET_errCallbackFailed.</span><span class="sxs-lookup"><span data-stu-id="dc381-167"><strong>Windows Server 2003 and earlier:  </strong>For Windows Server 2003 and earlier releases, the operation will fail with JET_errCallbackFailed.</span></span></p>
<p><span data-ttu-id="dc381-168"><strong>Windows Server 2003 SP1:  </strong> Este valor posible solo está disponible para Windows Server 2003 SP1 y los sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="dc381-168"><strong>Windows Server 2003 SP1:  </strong>This possible value is only available for Windows Server 2003 SP1 and later operating systems.</span></span> <span data-ttu-id="dc381-169">Si se especifica este valor posible y la tabla contiene una columna que tiene un valor predeterminado definido por el usuario, se producirá un error en la operación con JET_errCallbackFailed.</span><span class="sxs-lookup"><span data-stu-id="dc381-169">If this possible value is specified and the table contains a column that has a user defined default value, then the operation will fail with JET_errCallbackFailed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc381-170">JET_bitEnumeratePresenceOnly</span><span class="sxs-lookup"><span data-stu-id="dc381-170">JET_bitEnumeratePresenceOnly</span></span></p></td>
<td><p><span data-ttu-id="dc381-171">Si existe un valor no NULL para el valor de columna o columna solicitado, no se devuelven los datos asociados.</span><span class="sxs-lookup"><span data-stu-id="dc381-171">If a non-NULL value exists for the requested column or column value then the associated data is not returned.</span></span> <span data-ttu-id="dc381-172">En su lugar, el estado asociado para ese valor de columna o columna se establecerá en JET_wrnColumnPresent.</span><span class="sxs-lookup"><span data-stu-id="dc381-172">Instead, the associated status for that column or column value will be set to JET_wrnColumnPresent.</span></span> <span data-ttu-id="dc381-173">Si el valor de la columna o columna es <strong>null</strong> , JET_wrnColumnNull se devolverá como de costumbre.</span><span class="sxs-lookup"><span data-stu-id="dc381-173">If the column or column value is <strong>NULL</strong> then JET_wrnColumnNull will be returned as usual.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc381-174">JET_bitEnumerateTaggedOnly</span><span class="sxs-lookup"><span data-stu-id="dc381-174">JET_bitEnumerateTaggedOnly</span></span></p></td>
<td><p><span data-ttu-id="dc381-175">Al enumerar todos los valores de columna del registro (por ejemplo, es cuando <em>cEnumColumnId</em> es cero), solo se devolverán los valores de columna etiquetada.</span><span class="sxs-lookup"><span data-stu-id="dc381-175">When enumerating all column values in the record (for example,that is when <em>cEnumColumnId</em> is zero), only tagged column values will be returned.</span></span> <span data-ttu-id="dc381-176">Esta opción no está permitida cuando se enumera una matriz de identificadores de columna específica.</span><span class="sxs-lookup"><span data-stu-id="dc381-176">This option is not allowed when enumerating a specific array of column IDs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc381-177">JET_bitEnumerateInRecordOnly</span><span class="sxs-lookup"><span data-stu-id="dc381-177">JET_bitEnumerateInRecordOnly</span></span></p></td>
<td><p><span data-ttu-id="dc381-178"><strong>Windows 7:  </strong> JET_bitEnumerateInRecordOnly se presenta en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dc381-178"><strong>Windows 7:  </strong>JET_bitEnumerateInRecordOnly is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="dc381-179">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc381-179">Return Value</span></span>

<span data-ttu-id="dc381-180">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="dc381-180">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="dc381-181">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="dc381-181">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dc381-182">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="dc381-182">Return code</span></span></p></th>
<th><p><span data-ttu-id="dc381-183">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc381-183">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc381-184">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="dc381-184">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="dc381-185">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="dc381-185">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc381-186">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="dc381-186">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="dc381-187">El ID. de columna especificado está fuera de los límites legales de un identificador de columna.</span><span class="sxs-lookup"><span data-stu-id="dc381-187">The column ID given is outside the legal limits of a column ID.</span></span> <span data-ttu-id="dc381-188"><strong>JetEnumerateColumns</strong> devolverá este error si se solicitaron ID. de columna específicos, uno de esos identificadores de columna no era válido y el primer ID. de columna no válido dio error en el código de estado de la columna.</span><span class="sxs-lookup"><span data-stu-id="dc381-188">This error will be returned by <strong>JetEnumerateColumns</strong> if specific column ids were requested, one of those column ids was invalid, and the first invalid column ID failed with this error for its column status code.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc381-189">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="dc381-189">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="dc381-190">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="dc381-190">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc381-191">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="dc381-191">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="dc381-192">La columna descrita por el ID. de columna especificado no existe en la tabla.</span><span class="sxs-lookup"><span data-stu-id="dc381-192">The column described by the given column ID does not exist in the table.</span></span> <span data-ttu-id="dc381-193"><strong>JetEnumerateColumns</strong> devolverá este error si se solicitaron ID. de columna específicos, uno de esos identificadores de columna no era válido y el primer ID. de columna no válido dio error en el código de estado de la columna.</span><span class="sxs-lookup"><span data-stu-id="dc381-193">This error will be returned by <strong>JetEnumerateColumns</strong> if specific column IDs were requested, one of those column IDs was invalid, and the first invalid column ID failed with this error for its column status code.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc381-194">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="dc381-194">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="dc381-195">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="dc381-195">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="dc381-196"><strong>Windows XP:  </strong> Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="dc381-196"><strong>Windows XP:  </strong>This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc381-197">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="dc381-197">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="dc381-198">Una de las opciones solicitadas no era válida o no se implementó.</span><span class="sxs-lookup"><span data-stu-id="dc381-198">One of the options requested was invalid or not implemented.</span></span> <span data-ttu-id="dc381-199">Este error lo devolverá <strong>JetEnumerateColumns</strong> cuando:</span><span class="sxs-lookup"><span data-stu-id="dc381-199">This error will be returned by <strong>JetEnumerateColumns</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="dc381-200">Se especifica JET_bitEnumerateLocal.</span><span class="sxs-lookup"><span data-stu-id="dc381-200">JET_bitEnumerateLocal is specified.</span></span></p></li>
<li><p><span data-ttu-id="dc381-201">Se ha especificado un <em>grbit</em> no válido.</span><span class="sxs-lookup"><span data-stu-id="dc381-201">An illegal <em>grbit</em> is specified.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc381-202">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="dc381-202">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="dc381-203">Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="dc381-203">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="dc381-204">Este error lo devolverá <strong>JetEnumerateColumns</strong> cuando:</span><span class="sxs-lookup"><span data-stu-id="dc381-204">This error will be returned by <strong>JetEnumerateColumns</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="dc381-205"><em>pcEnumColumn</em> es <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="dc381-205"><em>pcEnumColumn</em> is <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="dc381-206"><em>prgEnumColumn</em> es <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="dc381-206"><em>prgEnumColumn</em> is <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="dc381-207"><em>pfnRealloc</em> es <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="dc381-207"><em>pfnRealloc</em> is <strong>NULL</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc381-208">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="dc381-208">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="dc381-209">El cursor no está situado en un registro.</span><span class="sxs-lookup"><span data-stu-id="dc381-209">The cursor is not positioned on a record.</span></span> <span data-ttu-id="dc381-210">Esto puede ocurrir por diversos motivos.</span><span class="sxs-lookup"><span data-stu-id="dc381-210">This can happen for many different reasons.</span></span> <span data-ttu-id="dc381-211">Por ejemplo, esto ocurrirá si el cursor está situado actualmente después del último registro en el índice actual.</span><span class="sxs-lookup"><span data-stu-id="dc381-211">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc381-212">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="dc381-212">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="dc381-213">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="dc381-213">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc381-214">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="dc381-214">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="dc381-215">El cursor se coloca en un registro que se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="dc381-215">The cursor is positioned on a record that has been deleted.</span></span> <span data-ttu-id="dc381-216">Esto puede ocurrir por diversos motivos.</span><span class="sxs-lookup"><span data-stu-id="dc381-216">This can happen for many different reasons.</span></span> <span data-ttu-id="dc381-217">La razón más común es que la sesión no está en una transacción, el cursor se colocó en un registro, se eliminó el registro y, a continuación, el cursor intentó hacer referencia a ese registro.</span><span class="sxs-lookup"><span data-stu-id="dc381-217">The most common reason is that the session is not in a transaction, the cursor was positioned on a record, that record was deleted, and then the cursor attempted to reference that record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc381-218">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="dc381-218">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="dc381-219">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="dc381-219">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc381-220">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="dc381-220">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="dc381-221">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="dc381-221">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="dc381-222"><strong>Windows XP:  </strong> Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="dc381-222"><strong>Windows XP:  </strong>This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc381-223">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="dc381-223">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="dc381-224">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="dc381-224">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dc381-225">Si se ejecuta correctamente, los datos solicitados se devolverán en los búferes de salida.</span><span class="sxs-lookup"><span data-stu-id="dc381-225">On success, the requested data will be returned in the output buffers.</span></span> <span data-ttu-id="dc381-226">Es responsabilidad del llamador liberar cualquier memoria asignada por esta devolución de llamada y devolverla en los búferes de salida.</span><span class="sxs-lookup"><span data-stu-id="dc381-226">It is the caller's responsibility to free any memory allocated by this callback and returned in the output buffers.</span></span> <span data-ttu-id="dc381-227">Esa memoria se debe liberar mediante la devolución de llamada compatible con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) proporcionada.</span><span class="sxs-lookup"><span data-stu-id="dc381-227">That memory should be freed through the provided [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback.</span></span> <span data-ttu-id="dc381-228">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="dc381-228">No change to the database state will occur.</span></span>

<span data-ttu-id="dc381-229">En caso de error, no se devolverá ninguno de los datos solicitados.</span><span class="sxs-lookup"><span data-stu-id="dc381-229">On failure, none of the requested data will be returned.</span></span> <span data-ttu-id="dc381-230">Cualquier memoria asignada durante la llamada se liberará automáticamente mediante la devolución de llamada compatible con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) proporcionada.</span><span class="sxs-lookup"><span data-stu-id="dc381-230">Any memory that was allocated during the call will be freed automatically using the provided [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback.</span></span> <span data-ttu-id="dc381-231">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="dc381-231">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="dc381-232">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dc381-232">Remarks</span></span>

<span data-ttu-id="dc381-233">Si está enumerando todos los valores de columna del registro y no especificó JET_bitEnumerateIgnoreDefaults, no puede suponer que nunca verá un valor de columna o columna con un código de estado de JET_wrnColumnNull.</span><span class="sxs-lookup"><span data-stu-id="dc381-233">If you are enumerating all column values in the record and you did not specify JET_bitEnumerateIgnoreDefaults then you cannot assume that you will never see a column or column value with a status code of JET_wrnColumnNull.</span></span> <span data-ttu-id="dc381-234">Puede ver este código de estado si una columna tiene un valor predeterminado y se estableció explícitamente en **null** o si la columna es una columna no dispersa (por ejemplo, una columna fija o variable).</span><span class="sxs-lookup"><span data-stu-id="dc381-234">You can see this status code if a column has a default value and was explicitly set to **NULL** or if the column is a non-sparse column (for example, a fixed or variable column).</span></span>

<span data-ttu-id="dc381-235">El parámetro *cbDataMost* no se aplica a todos los valores de columna.</span><span class="sxs-lookup"><span data-stu-id="dc381-235">The *cbDataMost* parameter does not apply to all column values.</span></span> <span data-ttu-id="dc381-236">Este parámetro solo truncará los valores de texto largo y de columna binaria larga que son tan grandes que se han almacenado por separado del registro.</span><span class="sxs-lookup"><span data-stu-id="dc381-236">This parameter will only truncate long text and long binary column values that are so large that they have been stored separately from the record.</span></span>

<span data-ttu-id="dc381-237">Si **JetEnumerateColumns** devuelve datos en sus parámetros de salida, el llamador es responsable de liberar la memoria de la matriz, así como cualquier memoria a la que hacen referencia los punteros incrustados en esa matriz.</span><span class="sxs-lookup"><span data-stu-id="dc381-237">If **JetEnumerateColumns** returns data in its output parameters then the caller is responsible for freeing the memory in the array as well as any memory referred to by pointers embedded in that array.</span></span>

#### <a name="requirements"></a><span data-ttu-id="dc381-238">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc381-238">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc381-239"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="dc381-239"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="dc381-240">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="dc381-240">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc381-241"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="dc381-241"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="dc381-242">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="dc381-242">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc381-243"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="dc381-243"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="dc381-244">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="dc381-244">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc381-245"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="dc381-245"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="dc381-246">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="dc381-246">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc381-247"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="dc381-247"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="dc381-248">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="dc381-248">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="dc381-249">Consulte también</span><span class="sxs-lookup"><span data-stu-id="dc381-249">See Also</span></span>

[<span data-ttu-id="dc381-250">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="dc381-250">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="dc381-251">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="dc381-251">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="dc381-252">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="dc381-252">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="dc381-253">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="dc381-253">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="dc381-254">JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="dc381-254">JET_ENUMCOLUMNID</span></span>](./jet-enumcolumnid-structure.md)  
[<span data-ttu-id="dc381-255">JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="dc381-255">JET_ENUMCOLUMN</span></span>](./jet-enumcolumn-structure.md)  
[<span data-ttu-id="dc381-256">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="dc381-256">JET_ENUMCOLUMNVALUE</span></span>](./jet-enumcolumnvalue-structure.md)  
[<span data-ttu-id="dc381-257">JET_PFNREALLOC</span><span class="sxs-lookup"><span data-stu-id="dc381-257">JET_PFNREALLOC</span></span>](./jet-pfnrealloc-callback-function.md)  
[<span data-ttu-id="dc381-258">realloc</span><span class="sxs-lookup"><span data-stu-id="dc381-258">realloc</span></span>](/cpp/c-runtime-library/reference/realloc?view=vs-2019)  
[<span data-ttu-id="dc381-259">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="dc381-259">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="dc381-260">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="dc381-260">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)
