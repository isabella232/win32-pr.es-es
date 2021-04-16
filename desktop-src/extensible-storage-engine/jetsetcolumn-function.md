---
description: 'Más información acerca de: JetSetColumn (función)'
title: Función JetSetColumn
TOCTitle: JetSetColumn Function
ms:assetid: f8877519-86d5-4e59-95a8-1927c70cd6b4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294137(v=EXCHG.10)
ms:contentKeyID: 32765751
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumn
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3c1fd267bea6bbb995a13ce65f97f1f531572a52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705745"
---
# <a name="jetsetcolumn-function"></a><span data-ttu-id="02c34-103">Función JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="02c34-103">JetSetColumn Function</span></span>


<span data-ttu-id="02c34-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="02c34-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcolumn-function"></a><span data-ttu-id="02c34-105">Función JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="02c34-105">JetSetColumn Function</span></span>

<span data-ttu-id="02c34-106">La función **JetSetColumn** modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual.</span><span class="sxs-lookup"><span data-stu-id="02c34-106">The **JetSetColumn** function modifies a single column value in a modified record to be inserted or to update the current record.</span></span> <span data-ttu-id="02c34-107">Puede sobrescribir un valor existente, agregar un nuevo valor a una secuencia de valores en una columna con varios valores, quitar un valor de una secuencia de valores de una columna con varios valores o actualizar todo o parte de un valor Long, una columna de tipo [JET_coltypLongText](./jet-coltyp.md) o [JET_coltypLongBinary](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="02c34-107">It can overwrite an existing value, add a new value to a sequence of values in a multi-valued column, remove a value from a sequence of values in a multi-valued column, or update all or part of a long value, a column of type [JET_coltypLongText](./jet-coltyp.md) or [JET_coltypLongBinary](./jet-coltyp.md).</span></span>

```cpp
    JET_ERR JET_API JetSetColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __in_opt      const void* pvData,
      __in          unsigned long cbData,
      __in          JET_GRBIT grbit,
      __in_opt      JET_SETINFO* psetinfo
    );
```

### <a name="parameters"></a><span data-ttu-id="02c34-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="02c34-108">Parameters</span></span>

<span data-ttu-id="02c34-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="02c34-109">*sesid*</span></span>

<span data-ttu-id="02c34-110">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="02c34-110">The session to use for this call.</span></span>

<span data-ttu-id="02c34-111">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="02c34-111">*tableid*</span></span>

<span data-ttu-id="02c34-112">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="02c34-112">The cursor to use for this call.</span></span>

<span data-ttu-id="02c34-113">*columnid*</span><span class="sxs-lookup"><span data-stu-id="02c34-113">*columnid*</span></span>

<span data-ttu-id="02c34-114">[JET_COLUMNID](./jet-columnid.md) de la columna que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="02c34-114">The [JET_COLUMNID](./jet-columnid.md) of the column to be retrieved.</span></span> <span data-ttu-id="02c34-115">Como alternativa, se puede proporcionar un valor de *columnid* de 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="02c34-115">Alternatively, a *columnid* value of 0 (zero) can be given.</span></span> <span data-ttu-id="02c34-116">Cuando se proporciona *columnid* 0 (cero), todas las columnas etiquetadas, las columnas dispersas y con varios valores, se tratan como una sola columna.</span><span class="sxs-lookup"><span data-stu-id="02c34-116">When *columnid* 0 (zero) is given, all tagged columns, sparse and multi-valued columns, are treated as a single column.</span></span> <span data-ttu-id="02c34-117">Esto facilita la recuperación de todas las columnas dispersas que se encuentran en un registro.</span><span class="sxs-lookup"><span data-stu-id="02c34-117">This facilitates retrieving all sparse columns that are present in a record.</span></span>

<span data-ttu-id="02c34-118">*pvData*</span><span class="sxs-lookup"><span data-stu-id="02c34-118">*pvData*</span></span>

<span data-ttu-id="02c34-119">Búfer de entrada que contiene los datos que se van a usar para el valor de columna.</span><span class="sxs-lookup"><span data-stu-id="02c34-119">Input buffer containing data to use for column value.</span></span>

<span data-ttu-id="02c34-120">*cbData*</span><span class="sxs-lookup"><span data-stu-id="02c34-120">*cbData*</span></span>

<span data-ttu-id="02c34-121">Tamaño en bytes del búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="02c34-121">Size in bytes of the input buffer.</span></span>

<span data-ttu-id="02c34-122">*grbit*</span><span class="sxs-lookup"><span data-stu-id="02c34-122">*grbit*</span></span>

<span data-ttu-id="02c34-123">Grupo de bits que contiene las opciones que se van a usar para esta llamada, que incluyen cero o más de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="02c34-123">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="02c34-124">Value</span><span class="sxs-lookup"><span data-stu-id="02c34-124">Value</span></span></p></th>
<th><p><span data-ttu-id="02c34-125">Significado</span><span class="sxs-lookup"><span data-stu-id="02c34-125">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02c34-126">JET_bitSetAppendLV</span><span class="sxs-lookup"><span data-stu-id="02c34-126">JET_bitSetAppendLV</span></span></p></td>
<td><p><span data-ttu-id="02c34-127">Esta opción se utiliza para anexar datos a una columna de tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>.</span><span class="sxs-lookup"><span data-stu-id="02c34-127">This option is used to append data to a column of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>.</span></span> <span data-ttu-id="02c34-128">Se puede lograr el mismo comportamiento determinando el tamaño del valor Long existente y especificando <em>ibLongValue</em> en <em>psetinfo</em>.</span><span class="sxs-lookup"><span data-stu-id="02c34-128">The same behavior can be achieved by determining the size of the existing long value and specifying <em>ibLongValue</em> in <em>psetinfo</em>.</span></span> <span data-ttu-id="02c34-129">Sin embargo, es más fácil usar esta <em>grbit</em> , ya que no es necesario conocer el tamaño del valor de la columna existente.</span><span class="sxs-lookup"><span data-stu-id="02c34-129">However, it's simpler to use this <em>grbit</em> since knowing the size of the existing column value is not necessary.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c34-130">JET_bitSetOverwriteLV</span><span class="sxs-lookup"><span data-stu-id="02c34-130">JET_bitSetOverwriteLV</span></span></p></td>
<td><p><span data-ttu-id="02c34-131">Esta opción se usa para reemplazar el valor Long existente con los datos proporcionados recientemente.</span><span class="sxs-lookup"><span data-stu-id="02c34-131">This option is used replace the existing long value with the newly provided data.</span></span> <span data-ttu-id="02c34-132">Cuando se usa esta opción, es como si el valor Long existente se hubiera establecido en la longitud 0 (cero) antes de establecer los datos nuevos.</span><span class="sxs-lookup"><span data-stu-id="02c34-132">When this option is used, it is as though the existing long value has been set to 0 (zero) length prior to setting the new data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c34-133">JET_bitSetRevertToDefaultValue</span><span class="sxs-lookup"><span data-stu-id="02c34-133">JET_bitSetRevertToDefaultValue</span></span></p></td>
<td><p><span data-ttu-id="02c34-134">Esta opción solo es aplicable para columnas etiquetadas, dispersas o con varios valores.</span><span class="sxs-lookup"><span data-stu-id="02c34-134">This option is only applicable for tagged, sparse or multi-valued columns.</span></span> <span data-ttu-id="02c34-135">Hace que la columna devuelva el valor de columna predeterminado en operaciones de recuperación de columna posteriores.</span><span class="sxs-lookup"><span data-stu-id="02c34-135">It causes the column to return the default column value on subsequent retrieve column operations.</span></span> <span data-ttu-id="02c34-136">Se quitan todos los valores de columna existentes.</span><span class="sxs-lookup"><span data-stu-id="02c34-136">All existing column values are removed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c34-137">JET_bitSetSeparateLV</span><span class="sxs-lookup"><span data-stu-id="02c34-137">JET_bitSetSeparateLV</span></span></p></td>
<td><p><span data-ttu-id="02c34-138">Esta opción se usa para forzar un valor largo, columnas de tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, que se almacenarán por separado del resto de datos de registro.</span><span class="sxs-lookup"><span data-stu-id="02c34-138">This option is used to force a long value, columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, to be stored separately from the remainder of record data.</span></span> <span data-ttu-id="02c34-139">Esto ocurre normalmente cuando el tamaño del valor Long impide que se almacene con los datos de registro restantes.</span><span class="sxs-lookup"><span data-stu-id="02c34-139">This occurs normally when the size of the long value prevents it from being stored with remaining record data.</span></span> <span data-ttu-id="02c34-140">Sin embargo, esta opción se puede usar para forzar el almacenamiento del valor largo por separado.</span><span class="sxs-lookup"><span data-stu-id="02c34-140">However, this option can be used to force the long value to be stored separately.</span></span> <span data-ttu-id="02c34-141">Tenga en cuenta que no se puede forzar la separación de los valores Long de cuatro bytes de menor tamaño.</span><span class="sxs-lookup"><span data-stu-id="02c34-141">Note that long values four bytes in size of smaller cannot be forced to be separate.</span></span> <span data-ttu-id="02c34-142">En estos casos, se omite la opción.</span><span class="sxs-lookup"><span data-stu-id="02c34-142">In such cases, the option is ignored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c34-143">JET_bitSetSizeLV</span><span class="sxs-lookup"><span data-stu-id="02c34-143">JET_bitSetSizeLV</span></span></p></td>
<td><p><span data-ttu-id="02c34-144">Esta opción se usa para interpretar el búfer de entrada como un número entero de bytes que se establecerá como la longitud del valor largo descrito por el <em>columnid</em> determinado y, si se proporciona, el número de secuencia en psetinfo- &gt; itagSequence.</span><span class="sxs-lookup"><span data-stu-id="02c34-144">This option is used to interpret the input buffer as a integer number of bytes to set as the length of the long value described by the given <em>columnid</em> and if provided, the sequence number in psetinfo-&gt;itagSequence.</span></span> <span data-ttu-id="02c34-145">Si el tamaño dado es mayor que el valor de columna existente, la columna se extenderá con 0s.</span><span class="sxs-lookup"><span data-stu-id="02c34-145">If the size given is larger than the existing column value, the column will be extended with 0s.</span></span> <span data-ttu-id="02c34-146">Si el tamaño es menor que el valor de la columna existente, el valor se truncará.</span><span class="sxs-lookup"><span data-stu-id="02c34-146">If the size is smaller than the existing column value then the value will be truncated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c34-147">JET_bitSetUniqueMultiValues</span><span class="sxs-lookup"><span data-stu-id="02c34-147">JET_bitSetUniqueMultiValues</span></span></p></td>
<td><p><span data-ttu-id="02c34-148">Esta opción se utiliza para exigir que todos los valores de una columna con varios valores sean distintos.</span><span class="sxs-lookup"><span data-stu-id="02c34-148">This option is used to enforce that all values in a multi-valued column are distinct.</span></span> <span data-ttu-id="02c34-149">Esta opción compara los datos de la columna de origen, sin ninguna transformación, con otros valores de columna existentes y se devuelve un error si se encuentra un duplicado.</span><span class="sxs-lookup"><span data-stu-id="02c34-149">This option compares the source column data, without any transformations, to other existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="02c34-150">Si se proporciona esta opción, no se pueden proporcionar también JET_bitSetAppendLV, JET_bitSetOverwriteLV y JET_bitSetSizeLV.</span><span class="sxs-lookup"><span data-stu-id="02c34-150">If this option is given, then JET_bitSetAppendLV, JET_bitSetOverwriteLV and JET_bitSetSizeLV cannot also be given.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c34-151">JET_bitSetUniqueNormalizedMultiValues</span><span class="sxs-lookup"><span data-stu-id="02c34-151">JET_bitSetUniqueNormalizedMultiValues</span></span></p></td>
<td><p><span data-ttu-id="02c34-152">Esta opción se utiliza para exigir que todos los valores de una columna con varios valores sean distintos.</span><span class="sxs-lookup"><span data-stu-id="02c34-152">This option is used to enforce that all values in a multi-valued column are distinct.</span></span> <span data-ttu-id="02c34-153">Esta opción compara la transformación normalizada clave de datos de columna con otros valores de columna existentes transformados de forma similar y se devuelve un error si se encuentra un duplicado.</span><span class="sxs-lookup"><span data-stu-id="02c34-153">This option compares the key normalized transformation of column data, to other similarly transformed existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="02c34-154">Si se proporciona esta opción, no se pueden proporcionar también JET_bitSetAppendLV, JET_bitSetOverwriteLV y JET_bitSetSizeLV.</span><span class="sxs-lookup"><span data-stu-id="02c34-154">If this option is given, then JET_bitSetAppendLV, JET_bitSetOverwriteLV and JET_bitSetSizeLV cannot also be given.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c34-155">JET_bitSetZeroLength</span><span class="sxs-lookup"><span data-stu-id="02c34-155">JET_bitSetZeroLength</span></span></p></td>
<td><p><span data-ttu-id="02c34-156">Esta opción se usa para establecer un valor de longitud cero.</span><span class="sxs-lookup"><span data-stu-id="02c34-156">This option is used to set a value to zero length.</span></span> <span data-ttu-id="02c34-157">Normalmente, un valor de columna se establece en <strong>null</strong> pasando un cbMax de 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="02c34-157">Normally, a column value is set to <strong>NULL</strong> by passing a cbMax of 0 (zero).</span></span> <span data-ttu-id="02c34-158">Sin embargo, para algunos tipos, como <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, un valor de columna puede ser una longitud de 0 (cero) en lugar de <strong>null</strong>, y esta opción se usa para diferenciar entre la longitud <strong>null</strong> y 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="02c34-158">However, for some types, like <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, a column value can be 0 (zero) length instead of <strong>NULL</strong>, and this option is used to differentiate between <strong>NULL</strong> and 0 (zero) length.</span></span></p>
<p><span data-ttu-id="02c34-159"><strong>Nota:</strong>  En general, si la columna es una columna de longitud fija, este bit se omite y la columna se establece en <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="02c34-159"><strong>Note</strong>  In general, if the column is a fixed-length column, this bit is ignored and the column is set to <strong>NULL</strong>.</span></span> <span data-ttu-id="02c34-160">Sin embargo, si la columna es una columna etiquetada de longitud fija, la longitud de la columna se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="02c34-160">However, if the column is a fixed-length tagged column, the column length is set to 0.</span></span> <span data-ttu-id="02c34-161">Cuando la columna etiquetada de longitud fija está establecida en una longitud de 0, los intentos de recuperar la columna con <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> o <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a> se realizarán correctamente, pero la longitud real que se devuelve en el parámetro <em>cbActual</em> es 0.</span><span class="sxs-lookup"><span data-stu-id="02c34-161">When the fixed-length tagged column is set to 0 length, attempts to retrieve the column with <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> or <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a> will succeed, but the actual length that is returned in the <em>cbActual</em> parameter is 0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c34-162">JET_bitSetIntrinsicLV</span><span class="sxs-lookup"><span data-stu-id="02c34-162">JET_bitSetIntrinsicLV</span></span></p></td>
<td><p><span data-ttu-id="02c34-163">Esta opción se usa para almacenar el valor largo completo en el registro.</span><span class="sxs-lookup"><span data-stu-id="02c34-163">This option is used to store the entire long value in the record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c34-164">JET_bitSetCompressed</span><span class="sxs-lookup"><span data-stu-id="02c34-164">JET_bitSetCompressed</span></span></p></td>
<td><p><span data-ttu-id="02c34-165">Esta opción se utiliza para intentar la compresión de datos al almacenar los datos.</span><span class="sxs-lookup"><span data-stu-id="02c34-165">This option is used to attempt data compression when storing the data.</span></span></p>
<p><span data-ttu-id="02c34-166"><strong>Windows 7:</strong>  JET_bitSetCompressed se presenta en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="02c34-166"><strong>Windows 7:</strong>  JET_bitSetCompressed is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c34-167">JET_bitSetUncompressed</span><span class="sxs-lookup"><span data-stu-id="02c34-167">JET_bitSetUncompressed</span></span></p></td>
<td><p><span data-ttu-id="02c34-168">Esta opción se usa para no intentar la compresión al almacenar los datos.</span><span class="sxs-lookup"><span data-stu-id="02c34-168">This option is used not attempt compression when storing the data.</span></span></p>
<p><span data-ttu-id="02c34-169"><strong>Windows 7:</strong>  JET_bitSetUnCompressed se presenta en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="02c34-169"><strong>Windows 7:</strong>  JET_bitSetUnCompressed is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="02c34-170">*psetinfo*</span><span class="sxs-lookup"><span data-stu-id="02c34-170">*psetinfo*</span></span>

<span data-ttu-id="02c34-171">Puntero a los parámetros de entrada opcionales que se pueden establecer para esta función mediante la estructura [JET_SETINFO](./jet-setinfo-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="02c34-171">Pointer to optional input parameters that can be set for this function using the [JET_SETINFO](./jet-setinfo-structure.md) structure.</span></span>

<span data-ttu-id="02c34-172">Si *psetinfo* se proporciona como **null** , la función se comporta como si se hubiera especificado un valor de *itagSequence* de 1 y un valor de *ibLongValue* de 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="02c34-172">If *psetinfo* is given as **NULL** then the function behaves as though an *itagSequence* of 1 and an *ibLongValue* of 0 (zero) were given.</span></span> <span data-ttu-id="02c34-173">Esto hace que el conjunto de columnas establezca el primer valor de una columna con varios valores y que se establezcan datos largos a partir del desplazamiento 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="02c34-173">This causes column set to set the first value of a multi-valued column, and to set long data beginning at offset 0 (zero).</span></span>

<span data-ttu-id="02c34-174">Se pueden establecer las siguientes opciones para este parámetro:</span><span class="sxs-lookup"><span data-stu-id="02c34-174">The following options can be set for this parameter:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="02c34-175">Value</span><span class="sxs-lookup"><span data-stu-id="02c34-175">Value</span></span></p></th>
<th><p><span data-ttu-id="02c34-176">Significado</span><span class="sxs-lookup"><span data-stu-id="02c34-176">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02c34-177">ibLongValue</span><span class="sxs-lookup"><span data-stu-id="02c34-177">ibLongValue</span></span></p></td>
<td><p><span data-ttu-id="02c34-178">Desplazamiento binario en un valor de columna largo donde deben comenzar los datos establecidos.</span><span class="sxs-lookup"><span data-stu-id="02c34-178">Binary offset into a long column value where set data should begin.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c34-179">itagSequence</span><span class="sxs-lookup"><span data-stu-id="02c34-179">itagSequence</span></span></p></td>
<td><p><span data-ttu-id="02c34-180">Número de secuencia del valor de columna multivalor deseado que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="02c34-180">Sequence number of the desired multi-valued column value to set.</span></span> <span data-ttu-id="02c34-181">Si <em>itagSequence</em> se establece en 0 (cero), el valor proporcionado debe anexarse al final de la secuencia de valores multivalor.</span><span class="sxs-lookup"><span data-stu-id="02c34-181">If <em>itagSequence</em> is set to 0 (zero), then the value provided should be appended to then end of the sequence of multi-valued values.</span></span> <span data-ttu-id="02c34-182">Si el número de secuencia proporcionado es mayor que el último valor de varios valores existente, el valor especificado se anexa al final de la secuencia de valores.</span><span class="sxs-lookup"><span data-stu-id="02c34-182">If the sequence number provided is greater than the last existing multi-valued value, then again the given value is appended to the end of the sequence of values.</span></span> <span data-ttu-id="02c34-183">Si el número de secuencia corresponde a un valor existente, ese valor se reemplaza por el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="02c34-183">If the sequence number corresponds to an existing value then that value is replaced with the given value.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="02c34-184">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02c34-184">Return Value</span></span>

<span data-ttu-id="02c34-185">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="02c34-185">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="02c34-186">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="02c34-186">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="02c34-187">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="02c34-187">Return code</span></span></p></th>
<th><p><span data-ttu-id="02c34-188">Descripción</span><span class="sxs-lookup"><span data-stu-id="02c34-188">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02c34-189">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="02c34-189">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="02c34-190">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="02c34-190">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c34-191">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="02c34-191">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="02c34-192">El ID. de columna especificado está fuera de los límites legales de un identificador de columna.</span><span class="sxs-lookup"><span data-stu-id="02c34-192">The column ID given is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c34-193">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="02c34-193">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="02c34-194">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="02c34-194">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c34-195">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="02c34-195">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="02c34-196">La columna descrita por el <em>columnid</em> determinado no existe en la tabla.</span><span class="sxs-lookup"><span data-stu-id="02c34-196">The column described by the given <em>columnid</em> does not exist in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c34-197">JET_errColumnNotUpdatable</span><span class="sxs-lookup"><span data-stu-id="02c34-197">JET_errColumnNotUpdatable</span></span></p></td>
<td><p><span data-ttu-id="02c34-198">Se intentó actualizar un valor Long durante una operación de eliminación de la actualización original.</span><span class="sxs-lookup"><span data-stu-id="02c34-198">An illegal attempt was made to update a long value during a insert copy delete original update operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c34-199">JET_errColumnTooBig</span><span class="sxs-lookup"><span data-stu-id="02c34-199">JET_errColumnTooBig</span></span></p></td>
<td><p><span data-ttu-id="02c34-200">Los datos de los valores de columna especificados en el búfer de entrada superan el límite de tamaño, ya sea natural para una columna de longitud fija o configurados para columnas binarias o de texto de longitud fija.</span><span class="sxs-lookup"><span data-stu-id="02c34-200">The given column value data given in the input buffer exceeds the size limitation either natural for a fixed length column or configured for fixed length text or binary columns.</span></span> <span data-ttu-id="02c34-201">Este error también se devuelve al pasar más de 1024 bytes de datos para una columna larga y al establecer la marca de JET_bitSetIntrinsicLV.</span><span class="sxs-lookup"><span data-stu-id="02c34-201">This error is also returned when passing more than 1024 bytes of data for a long column and setting the JET_bitSetIntrinsicLV flag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c34-202">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="02c34-202">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="02c34-203">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="02c34-203">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="02c34-204"><strong>Windows XP:</strong>  Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="02c34-204"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c34-205">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="02c34-205">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="02c34-206">El tamaño de los datos del valor de la columna dado no coincide con el tipo de datos de longitud fija.</span><span class="sxs-lookup"><span data-stu-id="02c34-206">The given column value data size does not match what is natural for the fixed length data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c34-207">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="02c34-207">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="02c34-208">Se realizó un intento no válido de actualizar una columna de incremento automático durante una operación de inserción o actualización, o bien para actualizar una columna de versión durante una operación de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="02c34-208">An illegal attempt was made to update an auto-increment column either during an insert or update operation, or to update a version column during a replace operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c34-209">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="02c34-209">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="02c34-210">Las opciones proporcionadas son desconocidas o una combinación no válida de valores de bits conocidos.</span><span class="sxs-lookup"><span data-stu-id="02c34-210">The options supplied are unknown or an illegal combination of known bit settings.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c34-211">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="02c34-211">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="02c34-212">El psetinfo especificado- &gt; cbStruct no es un tamaño válido para la estructura de <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> .</span><span class="sxs-lookup"><span data-stu-id="02c34-212">The given psetinfo-&gt;cbStruct is not a valid size for the <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c34-213">JET_errMultiValuedDuplicate</span><span class="sxs-lookup"><span data-stu-id="02c34-213">JET_errMultiValuedDuplicate</span></span></p></td>
<td><p><span data-ttu-id="02c34-214">La operación establecer columna intentó crear un valor duplicado y especificó JET_bitSetUniqueMultiValues o JET_bitSetUniqueNormalizedMultiValues.</span><span class="sxs-lookup"><span data-stu-id="02c34-214">The set column operation attempted to create a duplicate value and specified either JET_bitSetUniqueMultiValues or JET_bitSetUniqueNormalizedMultiValues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c34-215">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="02c34-215">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="02c34-216">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="02c34-216">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c34-217">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="02c34-217">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="02c34-218">Se intentó actualizar un valor de columna largo cuando la sesión que realiza la llamada no se encontraba en una transacción.</span><span class="sxs-lookup"><span data-stu-id="02c34-218">An illegal attempt was made to update a long column value when the calling session was not in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c34-219">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="02c34-219">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="02c34-220">Se hizo un intento no válido de establecer una columna que no es<strong>null</strong> en <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="02c34-220">An illegal attempt was made to set a non-<strong>NULL</strong> column to <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c34-221">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="02c34-221">JET_errColumnIllegalNull</span></span></p></td>
<td><p><span data-ttu-id="02c34-222">Igual que JET_errNullInvalid.</span><span class="sxs-lookup"><span data-stu-id="02c34-222">Same as JET_errNullInvalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c34-223">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="02c34-223">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="02c34-224">No se pudo establecer el valor de la columna en el valor del búfer de entrada porque habría hecho que el registro superara su límite de tamaño de página relacionado.</span><span class="sxs-lookup"><span data-stu-id="02c34-224">The column value could not be set to the value in the input buffer because it would have caused the record to exceed its page size related size limitation.</span></span> <span data-ttu-id="02c34-225">Las columnas de tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> pueden almacenarse independientemente de los datos de registro restantes.</span><span class="sxs-lookup"><span data-stu-id="02c34-225">Columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> can be stored separately from the remaining record data.</span></span> <span data-ttu-id="02c34-226">Sin embargo, otras columnas deben almacenarse con el registro y pueden provocar que se supere la limitación del tamaño del registro.</span><span class="sxs-lookup"><span data-stu-id="02c34-226">However, other columns must be stored with the record and can cause the record size limitation to be exceeded.</span></span> <span data-ttu-id="02c34-227">Las columnas de tipo Long requieren 5 bytes de espacio en el registro como una vinculación y esto puede provocar que se devuelva JET_errRecordTooBig.</span><span class="sxs-lookup"><span data-stu-id="02c34-227">Even long columns require 5-bytes of space within the record as a linkage and this too can lead to JET_errRecordTooBig being returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c34-228">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="02c34-228">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="02c34-229">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="02c34-229">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c34-230">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="02c34-230">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="02c34-231">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="02c34-231">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="02c34-232"><strong>Windows XP:</strong>  Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="02c34-232"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c34-233">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="02c34-233">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="02c34-234">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="02c34-234">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c34-235">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="02c34-235">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="02c34-236">El cursor no está actualmente en proceso de insertar un nuevo registro o actualizar un registro existente.</span><span class="sxs-lookup"><span data-stu-id="02c34-236">The cursor is not currently in the process of either inserting a new record or updating an existing record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c34-237">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="02c34-237">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="02c34-238">Este error se producirá cuando el tamaño configurado del almacén de versiones no sea suficiente para contener todas las actualizaciones pendientes.</span><span class="sxs-lookup"><span data-stu-id="02c34-238">This error will occur when the configured size of the version store is insufficient to hold all outstanding updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c34-239">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="02c34-239">JET_wrnColumnMaxTruncated</span></span></p></td>
<td><p><span data-ttu-id="02c34-240">El valor de la columna en el búfer de entrada superó la longitud máxima configurada para una columna de longitud variable y se truncó.</span><span class="sxs-lookup"><span data-stu-id="02c34-240">The column value in the input buffer exceeded the maximum configured length for a variable length column and was truncated.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="02c34-241">Si se ejecuta correctamente, la parte deseada de un valor de columna para la columna especificada se establece con los datos copiados desde el búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="02c34-241">On success, the desired portion of a column value for the given column is set with data copied from the input buffer.</span></span> <span data-ttu-id="02c34-242">Es posible que se haya truncado el conjunto de datos si ha superado la longitud máxima especificada para una columna de longitud variable.</span><span class="sxs-lookup"><span data-stu-id="02c34-242">The data set may have been truncated if it exceeded the maximum length specified for a variable length column.</span></span>

<span data-ttu-id="02c34-243">En caso de error, la ubicación del cursor permanece sin cambios y no se actualiza ningún dato del valor de columna en el búfer de copia.</span><span class="sxs-lookup"><span data-stu-id="02c34-243">On failure, the cursor location is left unchanged and no column value data is updated in the copy buffer.</span></span>

#### <a name="remarks"></a><span data-ttu-id="02c34-244">Observaciones</span><span class="sxs-lookup"><span data-stu-id="02c34-244">Remarks</span></span>

<span data-ttu-id="02c34-245">Establecer valores Long, los valores de las columnas [JET_coltypLongBinary](./jet-coltyp.md) de tipo [JET_coltypLongText](./jet-coltyp.md) o [JET_coltypLongBinary](./jet-coltyp.md), debe realizarse solo cuando la sesión de llamada está en una transacción.</span><span class="sxs-lookup"><span data-stu-id="02c34-245">Setting long values, values for columns [JET_coltypLongBinary](./jet-coltyp.md) of type [JET_coltypLongText](./jet-coltyp.md) or [JET_coltypLongBinary](./jet-coltyp.md), should be done only when the calling session is in a transaction.</span></span> <span data-ttu-id="02c34-246">Si la sesión que realiza la llamada no está en una transacción, las modificaciones realizadas en valores largos que se almacenan por separado se pueden confirmar por completo incluso cuando se cancela la operación de actualización posteriormente.</span><span class="sxs-lookup"><span data-stu-id="02c34-246">If the calling session is not in a transaction, modifications to long values which are stored separately may be committed fully even when the update operation is later cancelled.</span></span> <span data-ttu-id="02c34-247">Si la sesión que realiza la llamada está en una transacción, los efectos de la actualización se pueden revertir por completo cancelando la actualización y revirtiendo la transacción de la sesión.</span><span class="sxs-lookup"><span data-stu-id="02c34-247">If the calling session is in a transaction, then the effects of the update can be fully rolled back by canceling the update and rolling back the session transaction.</span></span>

<span data-ttu-id="02c34-248">No se realizan actualizaciones de índice como resultado de las operaciones de **JetSetColumn** .</span><span class="sxs-lookup"><span data-stu-id="02c34-248">Index updates are not performed as a result of **JetSetColumn** operations.</span></span> <span data-ttu-id="02c34-249">En su lugar, los índices solo se actualizan una vez completadas todas las modificaciones de las columnas y se llama a [JetUpdate](./jetupdate-function.md) .</span><span class="sxs-lookup"><span data-stu-id="02c34-249">Instead, indexes are updated only after all column modifications are complete and [JetUpdate](./jetupdate-function.md) is called.</span></span> <span data-ttu-id="02c34-250">Esto permite la actualización más eficaz de los índices cuando los índices implican que se está modificando más de una columna.</span><span class="sxs-lookup"><span data-stu-id="02c34-250">This permits the most efficient updating of indexes when indexes involve more than one column being modified.</span></span>

<span data-ttu-id="02c34-251">Un registro tiene un tamaño limitado según el tamaño de la página de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="02c34-251">A record is limited in size based on the database page size.</span></span> <span data-ttu-id="02c34-252">Los valores largos del registro de más de cinco bytes se almacenarán por separado del registro en caso de que los datos del registro superen su límite como resultado de una operación **JetSetColumn** .</span><span class="sxs-lookup"><span data-stu-id="02c34-252">Any long values in the record larger than five bytes will be stored separate from the record should the data in the record exceed its limit as a result of a **JetSetColumn** operation.</span></span> <span data-ttu-id="02c34-253">El JET_errRecordTooBig de error solo se devolverá después de que todos los datos de columna de registro separables se hayan almacenado por separado del registro y el registro supere el límite de tamaño del registro.</span><span class="sxs-lookup"><span data-stu-id="02c34-253">The error JET_errRecordTooBig will only be returned after all separable record column data has been stored separately from the record and the record still exceeds the record size limit.</span></span>

#### <a name="requirements"></a><span data-ttu-id="02c34-254">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02c34-254">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02c34-255"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="02c34-255"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="02c34-256">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="02c34-256">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c34-257"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="02c34-257"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="02c34-258">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="02c34-258">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c34-259"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="02c34-259"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="02c34-260">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="02c34-260">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c34-261"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="02c34-261"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="02c34-262">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="02c34-262">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c34-263"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="02c34-263"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="02c34-264">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="02c34-264">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="02c34-265">Consulte también</span><span class="sxs-lookup"><span data-stu-id="02c34-265">See Also</span></span>

[<span data-ttu-id="02c34-266">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="02c34-266">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="02c34-267">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="02c34-267">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="02c34-268">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="02c34-268">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="02c34-269">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="02c34-269">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="02c34-270">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="02c34-270">JET_SETINFO</span></span>](./jet-setinfo-structure.md)  
[<span data-ttu-id="02c34-271">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="02c34-271">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="02c34-272">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="02c34-272">JetSetColumns</span></span>](./jetsetcolumns-function.md)
