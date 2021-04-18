---
description: 'Más información acerca de: JetRetrieveColumn (función)'
title: Función JetRetrieveColumn
TOCTitle: JetRetrieveColumn Function
ms:assetid: 1e55063f-6033-4416-a9a6-894032fed069
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269198(v=EXCHG.10)
ms:contentKeyID: 32765501
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 074fb2471733afac40f76dcae1a4ce3ff38edc0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707179"
---
# <a name="jetretrievecolumn-function"></a><span data-ttu-id="5d951-103">Función JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="5d951-103">JetRetrieveColumn Function</span></span>


<span data-ttu-id="5d951-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5d951-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetretrievecolumn-function"></a><span data-ttu-id="5d951-105">Función JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="5d951-105">JetRetrieveColumn Function</span></span>

<span data-ttu-id="5d951-106">La función **JetRetrieveColumn** recupera un valor de columna único del registro actual.</span><span class="sxs-lookup"><span data-stu-id="5d951-106">The **JetRetrieveColumn** function retrieves a single column value from the current record.</span></span> <span data-ttu-id="5d951-107">El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</span><span class="sxs-lookup"><span data-stu-id="5d951-107">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="5d951-108">Como alternativa, esta función puede recuperar una columna de un registro que se crea en el búfer de copia del cursor.</span><span class="sxs-lookup"><span data-stu-id="5d951-108">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="5d951-109">Esta función también puede recuperar los datos de columna de una entrada de índice que hace referencia al registro actual.</span><span class="sxs-lookup"><span data-stu-id="5d951-109">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="5d951-110">Además de recuperar el valor de la columna real, **JetRetrieveColumn** también se puede usar para recuperar el tamaño de una columna, antes de recuperar los propios datos de la columna para que se pueda ajustar el tamaño adecuado de los búferes de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5d951-110">In addition to retrieving the actual column value, **JetRetrieveColumn** can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span>

```cpp
    JET_ERR JET_API JetRetrieveColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __out_opt     void* pvData,
      __in          unsigned long cbData,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit,
      __in_out_opt  JET_RETINFO* pretinfo
    );
```

### <a name="parameters"></a><span data-ttu-id="5d951-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d951-111">Parameters</span></span>

<span data-ttu-id="5d951-112">*sesid*</span><span class="sxs-lookup"><span data-stu-id="5d951-112">*sesid*</span></span>

<span data-ttu-id="5d951-113">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="5d951-113">The session to use for this call.</span></span>

<span data-ttu-id="5d951-114">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="5d951-114">*tableid*</span></span>

<span data-ttu-id="5d951-115">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="5d951-115">The cursor to use for this call.</span></span>

<span data-ttu-id="5d951-116">*columnid*</span><span class="sxs-lookup"><span data-stu-id="5d951-116">*columnid*</span></span>

<span data-ttu-id="5d951-117">[JET_COLUMNID](./jet-columnid.md) de la columna que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="5d951-117">The [JET_COLUMNID](./jet-columnid.md) of the column to retrieve.</span></span>

<span data-ttu-id="5d951-118">Se puede proporcionar un valor de *columnid* de 0 (cero) que no hace referencia a ninguna columna individual.</span><span class="sxs-lookup"><span data-stu-id="5d951-118">A *columnid* value of 0 (zero) can be given which does not itself refer to any individual column.</span></span> <span data-ttu-id="5d951-119">Cuando se proporciona *columnid* 0 (cero), todas las columnas etiquetadas, dispersas y columnas con varios valores se tratan como una sola columna.</span><span class="sxs-lookup"><span data-stu-id="5d951-119">When *columnid* 0 (zero) is given, all tagged columns, sparse, and multi-valued columns are treated as a single column.</span></span> <span data-ttu-id="5d951-120">Esto facilita la recuperación de todas las columnas dispersas que se encuentran en un registro.</span><span class="sxs-lookup"><span data-stu-id="5d951-120">This facilitates retrieving all sparse columns that are present in a record.</span></span>

<span data-ttu-id="5d951-121">*pvData*</span><span class="sxs-lookup"><span data-stu-id="5d951-121">*pvData*</span></span>

<span data-ttu-id="5d951-122">Búfer de salida que recibe el valor de la columna.</span><span class="sxs-lookup"><span data-stu-id="5d951-122">The output buffer that receives the column value.</span></span>

<span data-ttu-id="5d951-123">*cbData*</span><span class="sxs-lookup"><span data-stu-id="5d951-123">*cbData*</span></span>

<span data-ttu-id="5d951-124">Tamaño máximo, en bytes, del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="5d951-124">The maximum size, in bytes, of the output buffer.</span></span>

<span data-ttu-id="5d951-125">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="5d951-125">*pcbActual*</span></span>

<span data-ttu-id="5d951-126">Recibe el tamaño real, en bytes, del valor de la columna.</span><span class="sxs-lookup"><span data-stu-id="5d951-126">Receives the actual size, in bytes, of the column value.</span></span>

<span data-ttu-id="5d951-127">Si este parámetro es **null**, no se devolverá el tamaño real del valor de la columna.</span><span class="sxs-lookup"><span data-stu-id="5d951-127">If this parameter is **NULL**, then the actual size of the column value will not be returned.</span></span>

<span data-ttu-id="5d951-128">*grbit*</span><span class="sxs-lookup"><span data-stu-id="5d951-128">*grbit*</span></span>

<span data-ttu-id="5d951-129">Grupo de bits que contiene las opciones que se van a usar para esta llamada, que incluyen cero o más de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="5d951-129">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5d951-130">Value</span><span class="sxs-lookup"><span data-stu-id="5d951-130">Value</span></span></p></th>
<th><p><span data-ttu-id="5d951-131">Significado</span><span class="sxs-lookup"><span data-stu-id="5d951-131">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d951-132">JET_bitRetrieveCopy</span><span class="sxs-lookup"><span data-stu-id="5d951-132">JET_bitRetrieveCopy</span></span></p></td>
<td><p><span data-ttu-id="5d951-133">Esta marca hace que la columna de recuperación recupere el valor modificado en lugar del valor original.</span><span class="sxs-lookup"><span data-stu-id="5d951-133">This flag causes retrieve column to retrieve the modified value instead of the original value.</span></span> <span data-ttu-id="5d951-134">Si el valor no se ha modificado, se recupera el valor original.</span><span class="sxs-lookup"><span data-stu-id="5d951-134">If the value has not been modified, then the original value is retrieved.</span></span> <span data-ttu-id="5d951-135">De esta manera, se puede recuperar un valor que todavía no se ha insertado o actualizado durante la operación de inserción o actualización de un registro.</span><span class="sxs-lookup"><span data-stu-id="5d951-135">In this way, a value that has not yet been inserted or updated may be retrieved during the operation of inserting or updating a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d951-136">JET_bitRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="5d951-136">JET_bitRetrieveFromIndex</span></span></p></td>
<td><p><span data-ttu-id="5d951-137">Esta opción se utiliza para recuperar los valores de columna del índice, si es posible, sin tener acceso al registro.</span><span class="sxs-lookup"><span data-stu-id="5d951-137">This option is used to retrieve column values from the index, if possible, without accessing the record.</span></span> <span data-ttu-id="5d951-138">De esta manera, se puede evitar la carga innecesaria de registros cuando los datos necesarios están disponibles en las propias entradas de índice.</span><span class="sxs-lookup"><span data-stu-id="5d951-138">In this way, unnecessary loading of records can be avoided when needed data is available from index entries themselves.</span></span> <span data-ttu-id="5d951-139">En los casos en los que no se puede recuperar el valor de la columna original del índice debido a las transformaciones irreversibles o al truncamiento de los datos, se obtendrá acceso al registro y se recuperarán los datos de la forma habitual.</span><span class="sxs-lookup"><span data-stu-id="5d951-139">In cases where the original column value cannot be retrieved from the index, because of irreversible transformations or data truncation, the record will be accessed and the data retrieved as normal.</span></span> <span data-ttu-id="5d951-140">Se trata de una opción de rendimiento y solo se debe especificar cuando es probable que se pueda recuperar el valor de la columna del índice.</span><span class="sxs-lookup"><span data-stu-id="5d951-140">This is a performance option and should only be specified when it is likely that the column value can be retrieved from the index.</span></span> <span data-ttu-id="5d951-141">Esta opción no se debe especificar si el índice actual es el índice clúster, ya que las entradas de índice para el índice agrupado, o principal, son los propios registros.</span><span class="sxs-lookup"><span data-stu-id="5d951-141">This option should not be specified if the current index is the clustered index, since the index entries for the clustered, or primary, index are the records themselves.</span></span> <span data-ttu-id="5d951-142">No se puede establecer este bit si también se establece JET_bitRetrieveFromPrimaryBookmark.</span><span class="sxs-lookup"><span data-stu-id="5d951-142">This bit cannot be set if JET_bitRetrieveFromPrimaryBookmark is also set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d951-143">JET_bitRetrieveFromPrimaryBookmark</span><span class="sxs-lookup"><span data-stu-id="5d951-143">JET_bitRetrieveFromPrimaryBookmark</span></span></p></td>
<td><p><span data-ttu-id="5d951-144">Esta opción se usa para recuperar valores de columna del marcador de índice y puede diferir del valor de índice cuando una columna aparece en el índice principal y en el índice actual.</span><span class="sxs-lookup"><span data-stu-id="5d951-144">This option is used to retrieve column values from the index bookmark, and may differ from the index value when a column appears both in the primary index and the current index.</span></span> <span data-ttu-id="5d951-145">Esta opción no se debe especificar si el índice actual es el índice clúster o principal.</span><span class="sxs-lookup"><span data-stu-id="5d951-145">This option should not be specified if the current index is the clustered, or primary, index.</span></span> <span data-ttu-id="5d951-146">No se puede establecer este bit si también se establece JET_bitRetrieveFromIndex.</span><span class="sxs-lookup"><span data-stu-id="5d951-146">This bit cannot be set if JET_bitRetrieveFromIndex is also set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d951-147">JET_bitRetrieveTag</span><span class="sxs-lookup"><span data-stu-id="5d951-147">JET_bitRetrieveTag</span></span></p></td>
<td><p><span data-ttu-id="5d951-148">Esta opción se usa para recuperar el número de secuencia de un valor de columna de varios valores en pretinfo- &gt; itagSequence.</span><span class="sxs-lookup"><span data-stu-id="5d951-148">This option is used to retrieve the sequence number of a multi-valued column value in pretinfo-&gt;itagSequence.</span></span> <span data-ttu-id="5d951-149">El campo itagSequence suele ser una entrada para recuperar valores de columna con varios valores de un registro.</span><span class="sxs-lookup"><span data-stu-id="5d951-149">The itagSequence field is commonly an input for retrieving multi-valued column values from a record.</span></span> <span data-ttu-id="5d951-150">Sin embargo, cuando se recuperan valores de un índice, también es posible asociar la entrada de índice con un número de secuencia determinado y recuperar también este número de secuencia.</span><span class="sxs-lookup"><span data-stu-id="5d951-150">However, when retrieving values from an index, it is also possible to associate the index entry with a particular sequence number and retrieve this sequence number as well.</span></span> <span data-ttu-id="5d951-151">Recuperar el número de secuencia puede ser una operación costosa y solo debe realizarse si es necesario.</span><span class="sxs-lookup"><span data-stu-id="5d951-151">Retrieving the sequence number can be a costly operation and should only be done if necessary.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d951-152">JET_bitRetrieveNull</span><span class="sxs-lookup"><span data-stu-id="5d951-152">JET_bitRetrieveNull</span></span></p></td>
<td><p><span data-ttu-id="5d951-153">Esta opción se usa para recuperar los valores <strong>null</strong> de las columnas con varios valores.</span><span class="sxs-lookup"><span data-stu-id="5d951-153">This option is used to retrieve multi-valued column <strong>NULL</strong> values.</span></span> <span data-ttu-id="5d951-154">Si no se especifica esta opción, se omitirán automáticamente los valores <strong>null</strong> de las columnas con varios valores.</span><span class="sxs-lookup"><span data-stu-id="5d951-154">If this option is not specified, multi-valued column <strong>NULL</strong> values will automatically be skipped.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d951-155">JET_bitRetrieveIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="5d951-155">JET_bitRetrieveIgnoreDefault</span></span></p></td>
<td><p><span data-ttu-id="5d951-156">Esta opción solo afecta a las columnas con varios valores y hace que se devuelva un valor <strong>null</strong> cuando el número de secuencia solicitado es 1 y no hay valores establecidos para la columna en el registro.</span><span class="sxs-lookup"><span data-stu-id="5d951-156">This option affects only multi-valued columns and causes a <strong>NULL</strong> value to be returned when the requested sequence number is 1 and there are no set values for the column in the record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d951-157">JET_bitRetrieveLongId</span><span class="sxs-lookup"><span data-stu-id="5d951-157">JET_bitRetrieveLongId</span></span></p></td>
<td><p><span data-ttu-id="5d951-158">Esta marca solo es para uso interno y no está pensada para usarse en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5d951-158">This flag is for internal use only and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d951-159">JET_bitRetrieveLongValueRefCount</span><span class="sxs-lookup"><span data-stu-id="5d951-159">JET_bitRetrieveLongValueRefCount</span></span></p></td>
<td><p><span data-ttu-id="5d951-160">Esta marca solo es para uso interno y no está pensada para usarse en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5d951-160">This flag is for internal use only and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d951-161">JET_bitRetrieveTuple</span><span class="sxs-lookup"><span data-stu-id="5d951-161">JET_bitRetrieveTuple</span></span></p></td>
<td><p><span data-ttu-id="5d951-162">Esta marca permitirá la recuperación de un segmento de tupla del índice.</span><span class="sxs-lookup"><span data-stu-id="5d951-162">This flag will allow the retrieval of a tuple segment of the index.</span></span> <span data-ttu-id="5d951-163">Este bit debe especificarse con JET_bitRetrieveFromIndex.</span><span class="sxs-lookup"><span data-stu-id="5d951-163">This bit must be specified with JET_bitRetrieveFromIndex.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5d951-164">*pretinfo*</span><span class="sxs-lookup"><span data-stu-id="5d951-164">*pretinfo*</span></span>

<span data-ttu-id="5d951-165">Si *pretinfo* se da como **null** , la función se comporta como si se hubiera proporcionado un valor de *ItagSequence* de 1 y una *ibLongValue* de 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="5d951-165">If *pretinfo* is give as **NULL** then the function behaves as though an *itagSequence* of 1 and an *ibLongValue* of 0 (zero) were given.</span></span> <span data-ttu-id="5d951-166">Esto hace que la recuperación de columnas recupere el primer valor de una columna con varios valores y que recupere datos largos en el desplazamiento 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="5d951-166">This causes column retrieval to retrieve the first value of a multi-valued column, and to retrieve long data at offset 0 (zero).</span></span>

<span data-ttu-id="5d951-167">Este parámetro se usa para proporcionar uno o varios de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="5d951-167">This parameter is used to provide one or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5d951-168">Value</span><span class="sxs-lookup"><span data-stu-id="5d951-168">Value</span></span></p></th>
<th><p><span data-ttu-id="5d951-169">Significado</span><span class="sxs-lookup"><span data-stu-id="5d951-169">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d951-170">ibLongValue</span><span class="sxs-lookup"><span data-stu-id="5d951-170">ibLongValue</span></span></p></td>
<td><p><span data-ttu-id="5d951-171">Proporciona un desplazamiento binario en un valor de columna largo cuando se recupera una parte del valor de una columna.</span><span class="sxs-lookup"><span data-stu-id="5d951-171">Gives a binary offset into a long column value when retrieving a portion of a column value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d951-172">itagSequence</span><span class="sxs-lookup"><span data-stu-id="5d951-172">itagSequence</span></span></p></td>
<td><p><span data-ttu-id="5d951-173">Proporciona el número de secuencia del valor de columna de varios valores deseado.</span><span class="sxs-lookup"><span data-stu-id="5d951-173">Gives the sequence number of the desired multi-valued column value.</span></span> <span data-ttu-id="5d951-174">Tenga en cuenta que este campo solo se establece si se especifica el JET_bitRetrieveTag.</span><span class="sxs-lookup"><span data-stu-id="5d951-174">Note that this field is only set if the JET_bitRetrieveTag is specified.</span></span> <span data-ttu-id="5d951-175">De lo contrario, no se modifica.</span><span class="sxs-lookup"><span data-stu-id="5d951-175">Otherwise, it is unmodified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d951-176">columnidNextTagged</span><span class="sxs-lookup"><span data-stu-id="5d951-176">columnidNextTagged</span></span></p></td>
<td><p><span data-ttu-id="5d951-177">Devuelve el ID. de columna del valor de la columna devuelta cuando se recuperan todas las columnas etiquetadas, dispersas y con varios valores, mediante el paso de <em>columnid</em> de 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="5d951-177">Returns the column ID of the returned column value when retrieving all tagged, sparse and multi-valued, columns using passing <em>columnid</em> of 0 (zero).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="5d951-178">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d951-178">Return Value</span></span>

<span data-ttu-id="5d951-179">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="5d951-179">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="5d951-180">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="5d951-180">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5d951-181">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="5d951-181">Return code</span></span></p></th>
<th><p><span data-ttu-id="5d951-182">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d951-182">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d951-183">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="5d951-183">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="5d951-184">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="5d951-184">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d951-185">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="5d951-185">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="5d951-186">El ID. de columna especificado está fuera de los límites legales de un identificador de columna.</span><span class="sxs-lookup"><span data-stu-id="5d951-186">The column ID given is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d951-187">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="5d951-187">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="5d951-188">Se pasó un valor de número de secuencia de columna con varios valores no válido en pretinfo- &gt; itagSequence.</span><span class="sxs-lookup"><span data-stu-id="5d951-188">An invalid multi-valued column sequence number value has been passed in pretinfo-&gt;itagSequence.</span></span> <span data-ttu-id="5d951-189">Los valores válidos para los números de secuencia de valores de columna con varios valores son 1 o superior.</span><span class="sxs-lookup"><span data-stu-id="5d951-189">Valid values for the multi-valued column value sequence numbers are 1 or greater.</span></span> <span data-ttu-id="5d951-190">Un valor de 0 (cero) no es válido para esta función.</span><span class="sxs-lookup"><span data-stu-id="5d951-190">A value of 0 (zero) is invalid for this function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d951-191">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="5d951-191">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="5d951-192">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="5d951-192">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d951-193">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="5d951-193">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="5d951-194">La columna descrita por el <em>columnid</em> determinado no existe en la tabla.</span><span class="sxs-lookup"><span data-stu-id="5d951-194">The column described by the given <em>columnid</em> does not exist in the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d951-195">JET_errIndexTuplesCannotRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="5d951-195">JET_errIndexTuplesCannotRetrieveFromIndex</span></span></p></td>
<td><p><span data-ttu-id="5d951-196">Las columnas indizadas como subcadenas no se pueden recuperar del índice, puesto que solo una pequeña parte de la columna está presente normalmente en cada entrada de índice.</span><span class="sxs-lookup"><span data-stu-id="5d951-196">Columns indexed as substrings cannot be retrieved from the index, since only a small portion of the column is typically present in each index entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d951-197">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="5d951-197">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="5d951-198">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="5d951-198">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="5d951-199">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="5d951-199">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d951-200">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="5d951-200">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="5d951-201">En algunos casos, el búfer proporcionado para la columna de recuperación debe tener el tamaño suficiente para poder devolver cualquier cantidad de valor de columna.</span><span class="sxs-lookup"><span data-stu-id="5d951-201">In some cases, the buffer given for the retrieve column must be sufficiently sized in order to return any amount of the column value.</span></span> <span data-ttu-id="5d951-202">Por ejemplo, las columnas actualizables de custodia se ajustan para ser coherentes con el contexto transaccional de la sesión de llamada y este ajuste requiere el búfer proporcionado por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="5d951-202">For example, escrow updatable columns are adjusted to be consistent for the transactional context of the calling session and this adjustment requires the buffer provided by the caller.</span></span> <span data-ttu-id="5d951-203">Si se proporciona espacio en búfer insuficiente, se devuelve JET_errInvalidBufferSize y no se devuelve ningún dato de columna.</span><span class="sxs-lookup"><span data-stu-id="5d951-203">If insufficient buffer space is supplied, then JET_errInvalidBufferSize is returned and no column data whatsoever is returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d951-204">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="5d951-204">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="5d951-205">Uno o varios de los parámetros especificados no son correctos.</span><span class="sxs-lookup"><span data-stu-id="5d951-205">One or more of the parameters given is incorrect.</span></span> <span data-ttu-id="5d951-206">Esto puede ocurrir si retinfo. cbStruct es más pequeño que el tamaño de <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</span><span class="sxs-lookup"><span data-stu-id="5d951-206">This can happen if the retinfo.cbStruct is smaller that the size of <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d951-207">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="5d951-207">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="5d951-208">Las opciones proporcionadas son desconocidas o una combinación no válida de valores de bits conocidos.</span><span class="sxs-lookup"><span data-stu-id="5d951-208">The options supplied are unknown or an illegal combination of known bit settings.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d951-209">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="5d951-209">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="5d951-210">El cursor no está situado en un registro.</span><span class="sxs-lookup"><span data-stu-id="5d951-210">The cursor is not positioned on a record.</span></span> <span data-ttu-id="5d951-211">Esto puede ocurrir por diversos motivos.</span><span class="sxs-lookup"><span data-stu-id="5d951-211">This can happen for many different reasons.</span></span> <span data-ttu-id="5d951-212">Por ejemplo, esto ocurrirá si el cursor está situado actualmente después del último registro en el índice actual.</span><span class="sxs-lookup"><span data-stu-id="5d951-212">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d951-213">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="5d951-213">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="5d951-214">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="5d951-214">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d951-215">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="5d951-215">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="5d951-216">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="5d951-216">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d951-217">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="5d951-217">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="5d951-218">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="5d951-218">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="5d951-219"><strong>Windows XP:</strong>  Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="5d951-219"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d951-220">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="5d951-220">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="5d951-221">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="5d951-221">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d951-222">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="5d951-222">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="5d951-223">No se pudo recuperar el valor de columna completo porque el búfer especificado es menor que el tamaño de la columna.</span><span class="sxs-lookup"><span data-stu-id="5d951-223">The entire column value could not be retrieved because the given buffer is smaller than the size of the column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d951-224">JET_wrnColumnNull</span><span class="sxs-lookup"><span data-stu-id="5d951-224">JET_wrnColumnNull</span></span></p></td>
<td><p><span data-ttu-id="5d951-225">El valor de columna recuperado es <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="5d951-225">The column value retrieved is <strong>NULL</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5d951-226">Si se ejecuta correctamente, el valor de columna de la columna especificada se copia en el búfer especificado.</span><span class="sxs-lookup"><span data-stu-id="5d951-226">On success, the column value for the given column, is copied into the given buffer.</span></span> <span data-ttu-id="5d951-227">Se copia un valor menor que el de la columna con la advertencia JET_wrnBufferTruncated se devuelve.</span><span class="sxs-lookup"><span data-stu-id="5d951-227">Less than all of the column value is copied with the warning JET_wrnBufferTruncated is returned.</span></span> <span data-ttu-id="5d951-228">Si se proporciona *pcbActual* , se devuelve el tamaño real del valor de la columna.</span><span class="sxs-lookup"><span data-stu-id="5d951-228">If the *pcbActual* was given, the actual size of the column value is returned.</span></span> <span data-ttu-id="5d951-229">Tenga en cuenta que los valores **null** tienen una longitud de 0 (cero) y, por tanto, establecerán el tamaño devuelto en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="5d951-229">Note that **NULL** values have 0 (zero) length and will thus set the returned size to 0 (zero).</span></span> <span data-ttu-id="5d951-230">Si la columna recuperada era una columna con varios valores y se ha especificado *pretinfo* , y JET_bitReturnTag se estableció como una opción, el número de secuencia del valor de la columna se devuelve en pretinfo- \> itagSequence.</span><span class="sxs-lookup"><span data-stu-id="5d951-230">If the column retrieved was a multi-valued column, and *pretinfo* was given, and JET_bitReturnTag was set as an option, then the sequence number of the column value is returned in pretinfo-\>itagSequence.</span></span>

<span data-ttu-id="5d951-231">En caso de error, la ubicación del cursor se deja sin modificar y no se copia ningún dato en el búfer proporcionado.</span><span class="sxs-lookup"><span data-stu-id="5d951-231">On failure, the cursor location is left unchanged and no data is copied into the provided buffer.</span></span>

#### <a name="remarks"></a><span data-ttu-id="5d951-232">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d951-232">Remarks</span></span>

<span data-ttu-id="5d951-233">Esta llamada se usa solo una vez para recuperar datos de tamaño fijo o conocido para las columnas que no son de varios valores.</span><span class="sxs-lookup"><span data-stu-id="5d951-233">This call is used just once to retrieve data of fixed or known size for non-multi-valued columns.</span></span> <span data-ttu-id="5d951-234">Sin embargo, cuando los datos de columna tienen un tamaño desconocido, esta llamada se usa normalmente dos veces.</span><span class="sxs-lookup"><span data-stu-id="5d951-234">However, when column data is of unknown size, this call is typically used twice.</span></span> <span data-ttu-id="5d951-235">Se llama primero para determinar el tamaño de los datos para que pueda asignar el espacio de almacenamiento necesario.</span><span class="sxs-lookup"><span data-stu-id="5d951-235">It is called first to determine the size of the data so it can allocate the necessary storage space.</span></span> <span data-ttu-id="5d951-236">A continuación, se vuelve a realizar la misma llamada para recuperar los datos de la columna.</span><span class="sxs-lookup"><span data-stu-id="5d951-236">Then, the same call is made again to retrieve the column data.</span></span> <span data-ttu-id="5d951-237">Cuando se desconoce el número real de valores, ya que una columna tiene varios valores, normalmente se usa la llamada tres veces.</span><span class="sxs-lookup"><span data-stu-id="5d951-237">When the actual number of values is unknown, because a column is multi-valued, the call is typically used three times.</span></span> <span data-ttu-id="5d951-238">En primer lugar, obtenga el número de valores y, a continuación, dos veces más para asignar el almacenamiento y recuperar los datos reales.</span><span class="sxs-lookup"><span data-stu-id="5d951-238">First to get the number of values and then twice more to allocate storage and retrieve the actual data.</span></span>

<span data-ttu-id="5d951-239">Para recuperar todos los valores de una columna con varios valores, se puede realizar una llamada repetida a esta función con un valor de pretinfo- \> itagSequence a partir de 1 y aumentar en cada llamada subsiguiente.</span><span class="sxs-lookup"><span data-stu-id="5d951-239">Retrieving all the values for a multi-valued column can be done by repeatedly calling this function with a pretinfo-\>itagSequence value beginning at 1 and increasing on each subsequent call.</span></span> <span data-ttu-id="5d951-240">Se sabe que el último valor de la columna se recupera cuando se devuelve un JET_wrnColumnNull de la función.</span><span class="sxs-lookup"><span data-stu-id="5d951-240">The last column value is known to be retrieved when a JET_wrnColumnNull is returned from the function.</span></span> <span data-ttu-id="5d951-241">Tenga en cuenta que este método no se puede hacer si la columna de varios valores tiene valores **null** explícitos establecidos en su secuencia de valores, ya que estos valores se omitirán.</span><span class="sxs-lookup"><span data-stu-id="5d951-241">Note that this method cannot be done if the multi-value column has explicit **NULL** values set in its value sequence, since these values would be skipped.</span></span> <span data-ttu-id="5d951-242">Si una aplicación desea recuperar todos los valores de columna con varios valores, incluidos los que se establecen explícitamente en **null**, se debe usar [JetRetrieveColumns](./jetretrievecolumns-function.md) en lugar de **JetRetrieveColumn**.</span><span class="sxs-lookup"><span data-stu-id="5d951-242">If an application desires to retrieve all multi-valued column values, including those explicitly set to **NULL**, then [JetRetrieveColumns](./jetretrievecolumns-function.md) must be used instead of **JetRetrieveColumn**.</span></span> <span data-ttu-id="5d951-243">Tenga en cuenta que esta función no devuelve el número de valores para una función con varios valores cuando se proporciona un valor de *itagSequence* de 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="5d951-243">Note that this function does not return the number of values for a multi-valued function when an *itagSequence* value of 0 (zero) is given.</span></span> <span data-ttu-id="5d951-244">Solo [JetRetrieveColumns](./jetretrievecolumns-function.md) devolverá el número de valores de un valor de columna cuando se pasa un valor de *itagSequence* de 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="5d951-244">Only [JetRetrieveColumns](./jetretrievecolumns-function.md) will return the number of values of a column value when an *itagSequence* value of 0 (zero) is passed.</span></span>

<span data-ttu-id="5d951-245">Si se llama a esta función en el nivel de transacción 0 (cero), por ejemplo, la sesión que realiza la llamada no se realiza en una transacción, se abre y se cierra una transacción dentro de la función.</span><span class="sxs-lookup"><span data-stu-id="5d951-245">If this function is called at transaction level 0 (zero), for example, the calling session is not itself in a transaction, then a transaction is opened and closed within the function.</span></span> <span data-ttu-id="5d951-246">El propósito de esto es devolver resultados coherentes en caso de que un valor Long abarque páginas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="5d951-246">The purpose of this is to return consistent results in the case that a long value spans database pages.</span></span> <span data-ttu-id="5d951-247">Tenga en cuenta que la transacción se libera entre las llamadas de función y una serie de llamadas a esta función cuando la sesión no está en una transacción puede devolver datos actualizados después de la primera llamada a esta función.</span><span class="sxs-lookup"><span data-stu-id="5d951-247">Note that the transaction is released between function calls and a series of calls to this function when the session is not in a transaction may return data updated after the first call to this function.</span></span>

<span data-ttu-id="5d951-248">Se recuperará el valor predeterminado de la columna cuando la columna no se haya establecido explícitamente en otro valor, a menos que se establezca la opción JET_bitRetrieveIgnoreDefault.</span><span class="sxs-lookup"><span data-stu-id="5d951-248">The default column value will be retrieved when the column has not been set explicitly to another value, unless the JET_bitRetrieveIgnoreDefault option is set.</span></span>

<span data-ttu-id="5d951-249">Recuperar el valor de la columna AutoIncrement del búfer de copia antes de la inserción es un medio común para identificar un registro de forma exclusiva para la vinculación al insertar datos normalizados en varias tablas.</span><span class="sxs-lookup"><span data-stu-id="5d951-249">Retrieving the autoincrement column value from the copy buffer prior to insert is a common means of identifying a record uniquely for linkage when inserting normalized data into multiple tables.</span></span> <span data-ttu-id="5d951-250">El valor de incremento automático se asigna cuando se inicia la operación de inserción y se puede recuperar del búfer de copia en cualquier momento hasta que se complete la actualización.</span><span class="sxs-lookup"><span data-stu-id="5d951-250">The autoincrement value is allocated when the insert operation begins and can be retrieved from the copy buffer at any time until the update is complete.</span></span>

<span data-ttu-id="5d951-251">Cuando se recuperan todas las columnas etiquetadas, con varios valores y dispersas, al establecer *columnid* en 0 (cero), las columnas se recuperan en orden *columnid* desde el valor de *columnid* más bajo a *columnid* superior.</span><span class="sxs-lookup"><span data-stu-id="5d951-251">When retrieving all tagged, multi-valued, and sparse columns, by setting *columnid* to 0 (zero), columns are retrieved in *columnid* order from lowest *columnid* to highest *columnid*.</span></span> <span data-ttu-id="5d951-252">Se devuelve el mismo orden de valores de columna cada vez que se recuperan los valores de columna.</span><span class="sxs-lookup"><span data-stu-id="5d951-252">The same order of column values is returned each time column values are retrieved.</span></span> <span data-ttu-id="5d951-253">El orden es determinista.</span><span class="sxs-lookup"><span data-stu-id="5d951-253">The order is deterministic.</span></span>

#### <a name="requirements"></a><span data-ttu-id="5d951-254">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d951-254">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d951-255"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="5d951-255"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5d951-256">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="5d951-256">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d951-257"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="5d951-257"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5d951-258">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5d951-258">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d951-259"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="5d951-259"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5d951-260">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="5d951-260">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d951-261"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="5d951-261"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="5d951-262">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="5d951-262">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d951-263"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="5d951-263"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="5d951-264">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="5d951-264">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="5d951-265">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5d951-265">See Also</span></span>

[<span data-ttu-id="5d951-266">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="5d951-266">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="5d951-267">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5d951-267">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5d951-268">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="5d951-268">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="5d951-269">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="5d951-269">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="5d951-270">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="5d951-270">JET_RETINFO</span></span>](./jet-retinfo-structure.md)  
[<span data-ttu-id="5d951-271">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="5d951-271">JetSetColumn</span></span>](./jetretrievekey-function.md)  
[<span data-ttu-id="5d951-272">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="5d951-272">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)
