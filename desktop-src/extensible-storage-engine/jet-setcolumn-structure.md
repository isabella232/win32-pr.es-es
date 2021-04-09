---
description: 'Más información acerca de: estructura de JET_SETCOLUMN'
title: Estructura de JET_SETCOLUMN
TOCTitle: JET_SETCOLUMN Structure
ms:assetid: 3fdb8ec0-3c40-44f3-9859-72e22a504b90
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269233(v=EXCHG.10)
ms:contentKeyID: 32765535
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a170132fd4d832133e0f0bcad4a3499fa743db38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809038"
---
# <a name="jet_setcolumn-structure"></a><span data-ttu-id="39a05-103">Estructura de JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="39a05-103">JET_SETCOLUMN Structure</span></span>


<span data-ttu-id="39a05-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="39a05-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_setcolumn-structure"></a><span data-ttu-id="39a05-105">Estructura de JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="39a05-105">JET_SETCOLUMN Structure</span></span>

<span data-ttu-id="39a05-106">La estructura **JET_SETCOLUMN** contiene los parámetros de entrada y salida de [JetSetColumns](./jetsetcolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="39a05-106">The **JET_SETCOLUMN** structure contains input and output parameters for [JetSetColumns](./jetsetcolumns-function.md).</span></span> <span data-ttu-id="39a05-107">Los campos de la estructura describen qué valor de columna se va a establecer, cómo se establece y dónde se obtienen los datos del conjunto de columnas.</span><span class="sxs-lookup"><span data-stu-id="39a05-107">Fields in the structure describe what column value to set, how to set it, and where to get the column set data.</span></span>

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      const void* pvData;
      unsigned long cbData;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_ERR err;
    } JET_SETCOLUMN;
```

### <a name="members"></a><span data-ttu-id="39a05-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="39a05-108">Members</span></span>

<span data-ttu-id="39a05-109">**columnid**</span><span class="sxs-lookup"><span data-stu-id="39a05-109">**columnid**</span></span>

<span data-ttu-id="39a05-110">Identificador de columna de una columna que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="39a05-110">The column identifier for a column to set.</span></span>

<span data-ttu-id="39a05-111">**pvData**</span><span class="sxs-lookup"><span data-stu-id="39a05-111">**pvData**</span></span>

<span data-ttu-id="39a05-112">Puntero a los datos que se van a establecer en una columna.</span><span class="sxs-lookup"><span data-stu-id="39a05-112">A pointer to data to set into a column.</span></span>

<span data-ttu-id="39a05-113">**cbData**</span><span class="sxs-lookup"><span data-stu-id="39a05-113">**cbData**</span></span>

<span data-ttu-id="39a05-114">Tamaño de la asignación, en bytes, que empieza en **pvData** en bytes.</span><span class="sxs-lookup"><span data-stu-id="39a05-114">The size of allocation, in bytes, starting at **pvData** in bytes.</span></span>

<span data-ttu-id="39a05-115">**grbit**</span><span class="sxs-lookup"><span data-stu-id="39a05-115">**grbit**</span></span>

<span data-ttu-id="39a05-116">Grupo de bits que contiene las opciones que se van a usar para esta llamada, que incluyen cero o más de los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="39a05-116">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="39a05-117">Value</span><span class="sxs-lookup"><span data-stu-id="39a05-117">Value</span></span></p></th>
<th><p><span data-ttu-id="39a05-118">Significado</span><span class="sxs-lookup"><span data-stu-id="39a05-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39a05-119">JET_bitSetAppendLV</span><span class="sxs-lookup"><span data-stu-id="39a05-119">JET_bitSetAppendLV</span></span></p></td>
<td><p><span data-ttu-id="39a05-120">Anexa datos a una columna de tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>.</span><span class="sxs-lookup"><span data-stu-id="39a05-120">Appends data to a column of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>.</span></span> <span data-ttu-id="39a05-121">Se puede lograr el mismo comportamiento determinando el tamaño del valor Long existente y especificando <strong>ibLongValue</strong> en <strong>psetinfo</strong>.</span><span class="sxs-lookup"><span data-stu-id="39a05-121">The same behavior can be achieved by determining the size of the existing long value and specifying <strong>ibLongValue</strong> in <strong>psetinfo</strong>.</span></span> <span data-ttu-id="39a05-122">Sin embargo, es más fácil usar este <em>grbit</em>, ya que no es necesario conocer el tamaño del valor de la columna existente.</span><span class="sxs-lookup"><span data-stu-id="39a05-122">However, it's simpler to use this <em>grbit</em>, since knowing the size of the existing column value is not necessary.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39a05-123">JET_bitSetOverwriteLV</span><span class="sxs-lookup"><span data-stu-id="39a05-123">JET_bitSetOverwriteLV</span></span></p></td>
<td><p><span data-ttu-id="39a05-124">Reemplaza el valor Long existente por los nuevos datos.</span><span class="sxs-lookup"><span data-stu-id="39a05-124">Replaces the existing long value with the new data.</span></span> <span data-ttu-id="39a05-125">Cuando se usa esta opción, es como si el valor Long existente se hubiera establecido en la longitud 0 (cero) antes de establecer los datos nuevos.</span><span class="sxs-lookup"><span data-stu-id="39a05-125">When this option is used, it is as though the existing long value has been set to 0 (zero) length prior to setting the new data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39a05-126">JET_bitSetSizeLV</span><span class="sxs-lookup"><span data-stu-id="39a05-126">JET_bitSetSizeLV</span></span></p></td>
<td><p><span data-ttu-id="39a05-127">Interpreta el búfer de entrada como un número entero de bytes que se establecerá como la longitud del valor largo descrito por el columnid determinado y, si se proporciona, el número de secuencia en psetinfo- &gt; itagSequence.</span><span class="sxs-lookup"><span data-stu-id="39a05-127">Interprets the input buffer as an integer number of bytes to set as the length of the long value described by the given columnid and if provided, the sequence number in psetinfo-&gt;itagSequence.</span></span> <span data-ttu-id="39a05-128">Si el tamaño dado es mayor que el valor de columna existente, la columna se extenderá con 0s.</span><span class="sxs-lookup"><span data-stu-id="39a05-128">If the size given is larger than the existing column value, the column will be extended with 0s.</span></span> <span data-ttu-id="39a05-129">Si el tamaño es menor que el valor de la columna existente, el valor se truncará.</span><span class="sxs-lookup"><span data-stu-id="39a05-129">If the size is smaller than the existing column value then the value will be truncated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39a05-130">JET_bitSetZeroLength</span><span class="sxs-lookup"><span data-stu-id="39a05-130">JET_bitSetZeroLength</span></span></p></td>
<td><p><span data-ttu-id="39a05-131">Establece un valor de longitud cero.</span><span class="sxs-lookup"><span data-stu-id="39a05-131">Sets a value to zero length.</span></span> <span data-ttu-id="39a05-132">Normalmente, un valor de columna se establece en NULL pasando un cbMax de 0.</span><span class="sxs-lookup"><span data-stu-id="39a05-132">Normally, a column value is set to NULL by passing a cbMax of 0.</span></span> <span data-ttu-id="39a05-133">Sin embargo, para algunos tipos, como <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, un valor de columna puede tener una longitud de 0 en lugar de NULL, y esta opción se usa para diferenciar entre NULL y 0.</span><span class="sxs-lookup"><span data-stu-id="39a05-133">However, for some types, like <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, a column value can be 0 length instead of NULL, and this option is used to differentiate between NULL and 0 length.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39a05-134">JET_bitSetSeparateLV</span><span class="sxs-lookup"><span data-stu-id="39a05-134">JET_bitSetSeparateLV</span></span></p></td>
<td><p><span data-ttu-id="39a05-135">Fuerza un valor Long, columnas de tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, que se almacenarán por separado del resto de datos de registro.</span><span class="sxs-lookup"><span data-stu-id="39a05-135">Forces a long value, columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, to be stored separately from the remainder of record data.</span></span> <span data-ttu-id="39a05-136">Esto ocurre normalmente cuando el tamaño del valor Long impide que se almacene con los datos de registro restantes.</span><span class="sxs-lookup"><span data-stu-id="39a05-136">This occurs normally when the size of the long value prevents it from being stored with remaining record data.</span></span> <span data-ttu-id="39a05-137">Sin embargo, esta opción se puede usar para forzar el almacenamiento del valor largo por separado.</span><span class="sxs-lookup"><span data-stu-id="39a05-137">However, this option can be used to force the long value to be stored separately.</span></span> <span data-ttu-id="39a05-138">Tenga en cuenta que no se puede forzar la separación de los valores largos de cuatro bytes o de menor tamaño.</span><span class="sxs-lookup"><span data-stu-id="39a05-138">Note that long values four bytes in size or smaller cannot be forced to be separate.</span></span> <span data-ttu-id="39a05-139">En estos casos, se omite la opción.</span><span class="sxs-lookup"><span data-stu-id="39a05-139">In such cases, the option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39a05-140">JET_bitSetUniqueMultiValues</span><span class="sxs-lookup"><span data-stu-id="39a05-140">JET_bitSetUniqueMultiValues</span></span></p></td>
<td><p><span data-ttu-id="39a05-141">Aplica valores distintos en una columna con varios valores.</span><span class="sxs-lookup"><span data-stu-id="39a05-141">Enforces distinct values in a multi-valued column.</span></span> <span data-ttu-id="39a05-142">Esta opción compara los datos de la columna de origen, sin ninguna transformación, con otros valores de columna existentes y se devuelve un error si se encuentra un duplicado.</span><span class="sxs-lookup"><span data-stu-id="39a05-142">This option compares the source column data, without any transformations, to other existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="39a05-143">Si se proporciona esta opción, no se pueden proporcionar también JET_bitSetAppendLv, JET_bitSetOverwriteLV y JET_bitSetSizeLV.</span><span class="sxs-lookup"><span data-stu-id="39a05-143">If this option is given, then JET_bitSetAppendLv, JET_bitSetOverwriteLV, and JET_bitSetSizeLV cannot also be given.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39a05-144">JET_bitSetUniqueNormalizedMultiValues</span><span class="sxs-lookup"><span data-stu-id="39a05-144">JET_bitSetUniqueNormalizedMultiValues</span></span></p></td>
<td><p><span data-ttu-id="39a05-145">Aplica valores distintos en una columna con varios valores.</span><span class="sxs-lookup"><span data-stu-id="39a05-145">Enforces distinct values in a multi-valued column.</span></span> <span data-ttu-id="39a05-146">Esta opción compara la transformación normalizada de datos de columna con otros valores de columna existentes transformados de forma similar y se devuelve un error si se encuentra un duplicado.</span><span class="sxs-lookup"><span data-stu-id="39a05-146">This option compares the key normalized transformation of column data to other similarly transformed existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="39a05-147">Si se proporciona esta opción, no se pueden proporcionar también JET_bitSetAppendLv, JET_bitSetOverwriteLV y JET_bitSetSizeLV.</span><span class="sxs-lookup"><span data-stu-id="39a05-147">If this option is given, then JET_bitSetAppendLv, JET_bitSetOverwriteLV, and JET_bitSetSizeLV cannot also be given.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39a05-148">JET_bitSetRevertToDefaultValue</span><span class="sxs-lookup"><span data-stu-id="39a05-148">JET_bitSetRevertToDefaultValue</span></span></p></td>
<td><p><span data-ttu-id="39a05-149">Hace que la columna devuelva el valor de columna predeterminado en operaciones de recuperación de columnas posteriores.</span><span class="sxs-lookup"><span data-stu-id="39a05-149">Causes the column to return the default column value on subsequent retrieve column operations.</span></span> <span data-ttu-id="39a05-150">Se quitan todos los valores de columna existentes.</span><span class="sxs-lookup"><span data-stu-id="39a05-150">All existing column values are removed.</span></span> <span data-ttu-id="39a05-151">Esta opción solo es aplicable para columnas etiquetadas, dispersas o con varios valores.</span><span class="sxs-lookup"><span data-stu-id="39a05-151">This option is only applicable for tagged, sparse, or multi-valued columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39a05-152">JET_bitSetIntrinsicLV</span><span class="sxs-lookup"><span data-stu-id="39a05-152">JET_bitSetIntrinsicLV</span></span></p></td>
<td><p><span data-ttu-id="39a05-153">Mantiene el valor largo, las columnas de tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o JET_coltypeLongBinary, que se almacenan con los datos de registro restantes si es posible.</span><span class="sxs-lookup"><span data-stu-id="39a05-153">Keeps the long value, columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or JET_coltypeLongBinary, stored with the remaining record data if possible.</span></span> <span data-ttu-id="39a05-154">Normalmente, las columnas de tipo Long se almacenan por separado cuando su longitud supera los 1024 bytes o, de lo contrario, haría que la longitud del registro superara su límite de tamaño de página relacionado.</span><span class="sxs-lookup"><span data-stu-id="39a05-154">Normally, long columns are stored separately when their length exceeds 1024 bytes or would otherwise cause the record length to exceed its page size related size limitation.</span></span> <span data-ttu-id="39a05-155">Sin embargo, si se establece esta opción, la operación establecer columna producirá un error JET_errColumnTooBig en lugar de almacenar el valor de esta columna de forma independiente de los datos de registro restantes.</span><span class="sxs-lookup"><span data-stu-id="39a05-155">However, if this option is set, the set column operation will fail with error JET_errColumnTooBig rather than store this column value separate from the remaining record data.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="39a05-156">**ibLongValue**</span><span class="sxs-lookup"><span data-stu-id="39a05-156">**ibLongValue**</span></span>

<span data-ttu-id="39a05-157">Desplazamiento al primer byte que se va a recuperar de una columna de tipo [JET_coltypLongBinary](./jet-coltyp.md), o [JET_coltypLongText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="39a05-157">The offset to the first byte to be retrieved from a column of type [JET_coltypLongBinary](./jet-coltyp.md), or [JET_coltypLongText](./jet-coltyp.md).</span></span>

<span data-ttu-id="39a05-158">**itagSequence**</span><span class="sxs-lookup"><span data-stu-id="39a05-158">**itagSequence**</span></span>

<span data-ttu-id="39a05-159">Describe el número de secuencia de un valor en una columna con varios valores.</span><span class="sxs-lookup"><span data-stu-id="39a05-159">Describes the sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="39a05-160">Un valor de **itagSequence** de 0 indica que el conjunto de valores de columna debe agregarse como una nueva instancia de una columna con varios valores.</span><span class="sxs-lookup"><span data-stu-id="39a05-160">An **itagSequence** of 0 indicates that the column value set should be added as a new instance of a multi-valued column.</span></span>

<span data-ttu-id="39a05-161">**ERR**</span><span class="sxs-lookup"><span data-stu-id="39a05-161">**err**</span></span>

<span data-ttu-id="39a05-162">Códigos de error y advertencias devueltos por la operación establecer columna.</span><span class="sxs-lookup"><span data-stu-id="39a05-162">Error codes and warnings returned from the set column operation.</span></span>

### <a name="requirements"></a><span data-ttu-id="39a05-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39a05-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39a05-164"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="39a05-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="39a05-165">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="39a05-165">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39a05-166"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="39a05-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="39a05-167">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="39a05-167">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39a05-168"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="39a05-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="39a05-169">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="39a05-169">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="39a05-170">Consulte también</span><span class="sxs-lookup"><span data-stu-id="39a05-170">See Also</span></span>

[<span data-ttu-id="39a05-171">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="39a05-171">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="39a05-172">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="39a05-172">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="39a05-173">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="39a05-173">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="39a05-174">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="39a05-174">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="39a05-175">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="39a05-175">JetSetColumns</span></span>](./jetsetcolumns-function.md)
