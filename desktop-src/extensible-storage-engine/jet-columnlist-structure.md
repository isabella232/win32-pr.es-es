---
description: 'Más información acerca de: estructura de JET_COLUMNLIST'
title: Estructura de JET_COLUMNLIST
TOCTitle: JET_COLUMNLIST Structure
ms:assetid: 3899676f-c96e-4f15-9089-4faea6808bc2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269228(v=EXCHG.10)
ms:contentKeyID: 32765530
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
ms.openlocfilehash: 9bce36c818dd35408d95c770540ff4865bdf639b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715406"
---
# <a name="jet_columnlist-structure"></a><span data-ttu-id="066a5-103">Estructura de JET_COLUMNLIST</span><span class="sxs-lookup"><span data-stu-id="066a5-103">JET_COLUMNLIST Structure</span></span>


<span data-ttu-id="066a5-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="066a5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columnlist-structure"></a><span data-ttu-id="066a5-105">Estructura de JET_COLUMNLIST</span><span class="sxs-lookup"><span data-stu-id="066a5-105">JET_COLUMNLIST Structure</span></span>

<span data-ttu-id="066a5-106">La estructura de **JET_COLUMNLIST** contiene la información necesaria para recorrer la tabla temporal creada por las funciones [JetGetColumnInfo](./jetgetcolumninfo-function.md) y [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) .</span><span class="sxs-lookup"><span data-stu-id="066a5-106">The **JET_COLUMNLIST** structure contains the information necessary to traverse the temporary table that is created by the [JetGetColumnInfo](./jetgetcolumninfo-function.md) and [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) functions.</span></span> <span data-ttu-id="066a5-107">Cada fila de la tabla temporal describe una columna de la tabla especificada en la llamada de API.</span><span class="sxs-lookup"><span data-stu-id="066a5-107">Each row in the temporary table describes a column in the table given in the API call.</span></span> <span data-ttu-id="066a5-108">Esta estructura se usa solo con [JetGetColumnInfo](./jetgetcolumninfo-function.md) y [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="066a5-108">This structure is used with only with [JetGetColumnInfo](./jetgetcolumninfo-function.md) and [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidPresentationOrder;
      JET_COLUMNID columnidcolumnname;
      JET_COLUMNID columnidcolumnid;
      JET_COLUMNID columnidcoltyp;
      JET_COLUMNID columnidCountry;
      JET_COLUMNID columnidLangid;
      JET_COLUMNID columnidCp;
      JET_COLUMNID columnidCollate;
      JET_COLUMNID columnidcbMax;
      JET_COLUMNID columnidgrbit;
      JET_COLUMNID columnidDefault;
      JET_COLUMNID columnidBaseTableName;
      JET_COLUMNID columnidBaseColumnName;
      JET_COLUMNID columnidDefinitionName;
    } JET_COLUMNLIST;
```

### <a name="members"></a><span data-ttu-id="066a5-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="066a5-109">Members</span></span>

<span data-ttu-id="066a5-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="066a5-110">**cbStruct**</span></span>

<span data-ttu-id="066a5-111">Tamaño de la estructura en bytes.</span><span class="sxs-lookup"><span data-stu-id="066a5-111">The size of the structure in bytes.</span></span> <span data-ttu-id="066a5-112">La llamada a la API actualizará este campo, por lo que el llamador debe asegurarse de que este valor coincide con sizeof (JET_COLUMNLIST).</span><span class="sxs-lookup"><span data-stu-id="066a5-112">The API call will update this field, so the caller should ensure that this value matches sizeof( JET_COLUMNLIST ).</span></span>

<span data-ttu-id="066a5-113">**TABLEID**</span><span class="sxs-lookup"><span data-stu-id="066a5-113">**tableid**</span></span>

<span data-ttu-id="066a5-114">Identificador de tabla de la tabla temporal que se creó.</span><span class="sxs-lookup"><span data-stu-id="066a5-114">The table identifier of the temporary table that was created.</span></span> <span data-ttu-id="066a5-115">Es responsabilidad del llamador cerrar la tabla.</span><span class="sxs-lookup"><span data-stu-id="066a5-115">It is the responsibility of the caller to close the table.</span></span>

<span data-ttu-id="066a5-116">**cRecord**</span><span class="sxs-lookup"><span data-stu-id="066a5-116">**cRecord**</span></span>

<span data-ttu-id="066a5-117">El número de registros de la tabla temporal que creó la llamada API.</span><span class="sxs-lookup"><span data-stu-id="066a5-117">The number of records in the temporary table that was created by the API call.</span></span>

<span data-ttu-id="066a5-118">**columnidPresentationOrder**</span><span class="sxs-lookup"><span data-stu-id="066a5-118">**columnidPresentationOrder**</span></span>

<span data-ttu-id="066a5-119">Identificador de columna del orden de presentación.</span><span class="sxs-lookup"><span data-stu-id="066a5-119">The column identifier of the presentation order.</span></span>

<span data-ttu-id="066a5-120">El orden de presentación se usa para ordenar las filas de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="066a5-120">The presentation order is used to sort the rows of the temporary table.</span></span> <span data-ttu-id="066a5-121">El orden de presentación es un [JET_coltypLong](./jet-coltyp.md)fijo.</span><span class="sxs-lookup"><span data-stu-id="066a5-121">The presentation order is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span> <span data-ttu-id="066a5-122">Si el nivel de información que se especificó no era un nivel compacto, también se marca como JET_bitColumnTTKey.</span><span class="sxs-lookup"><span data-stu-id="066a5-122">If the information level that was specified was not a compact level, then it is also marked as JET_bitColumnTTKey.</span></span>

<span data-ttu-id="066a5-123">**columnidcolumnname**</span><span class="sxs-lookup"><span data-stu-id="066a5-123">**columnidcolumnname**</span></span>

<span data-ttu-id="066a5-124">Identificador de columna del nombre de la columna.</span><span class="sxs-lookup"><span data-stu-id="066a5-124">The column identifier of the name of the column.</span></span>

<span data-ttu-id="066a5-125">Si el nivel de información especificado no es compacto, también se marca como JET_bitColumnTTKey.</span><span class="sxs-lookup"><span data-stu-id="066a5-125">If the information level specified was not compact, then it is also marked as JET_bitColumnTTKey.</span></span>

<span data-ttu-id="066a5-126">**columnidcolumnid**</span><span class="sxs-lookup"><span data-stu-id="066a5-126">**columnidcolumnid**</span></span>

<span data-ttu-id="066a5-127">Identificador de columna del identificador de columna.</span><span class="sxs-lookup"><span data-stu-id="066a5-127">The column identifier of the column identifier.</span></span>

<span data-ttu-id="066a5-128">El identificador de columna es un [JET_coltypLong](./jet-coltyp.md)fijo.</span><span class="sxs-lookup"><span data-stu-id="066a5-128">The column identifier is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="066a5-129">**columnidcoltyp**</span><span class="sxs-lookup"><span data-stu-id="066a5-129">**columnidcoltyp**</span></span>

<span data-ttu-id="066a5-130">Identificador de columna del tipo de columna.</span><span class="sxs-lookup"><span data-stu-id="066a5-130">The column identifier of the column type.</span></span>

<span data-ttu-id="066a5-131">El tipo de columna es un [JET_coltypLong](./jet-coltyp.md)fijo.</span><span class="sxs-lookup"><span data-stu-id="066a5-131">The column type is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="066a5-132">**columnidCountry**</span><span class="sxs-lookup"><span data-stu-id="066a5-132">**columnidCountry**</span></span>

<span data-ttu-id="066a5-133">Identificador de columna del código de país.</span><span class="sxs-lookup"><span data-stu-id="066a5-133">The column identifier of the country code.</span></span>

<span data-ttu-id="066a5-134">El código de país es un [JET_coltypShort](./jet-coltyp.md)fijo.</span><span class="sxs-lookup"><span data-stu-id="066a5-134">The country code is a fixed [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="066a5-135">**columnidLangid**</span><span class="sxs-lookup"><span data-stu-id="066a5-135">**columnidLangid**</span></span>

<span data-ttu-id="066a5-136">Identificador de columna del identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="066a5-136">The column identifier of the language identifier.</span></span>

<span data-ttu-id="066a5-137">El identificador de idioma es un [JET_coltypShort](./jet-coltyp.md)fijo.</span><span class="sxs-lookup"><span data-stu-id="066a5-137">The language identifier is a fixed [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="066a5-138">**columnidCp**</span><span class="sxs-lookup"><span data-stu-id="066a5-138">**columnidCp**</span></span>

<span data-ttu-id="066a5-139">El identificador de columna de la página de códigos.</span><span class="sxs-lookup"><span data-stu-id="066a5-139">The column identifier of the code page.</span></span>

<span data-ttu-id="066a5-140">La página de códigos es un [JET_coltypShort](./jet-coltyp.md)fijo.</span><span class="sxs-lookup"><span data-stu-id="066a5-140">The code page is a fixed [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="066a5-141">**columnidCollate**</span><span class="sxs-lookup"><span data-stu-id="066a5-141">**columnidCollate**</span></span>

<span data-ttu-id="066a5-142">El identificador de columna de la secuencia de intercalación.</span><span class="sxs-lookup"><span data-stu-id="066a5-142">The column identifier of the collation sequence.</span></span>

<span data-ttu-id="066a5-143">La secuencia de intercalación es un [JET_coltypShort](./jet-coltyp.md)fijo.</span><span class="sxs-lookup"><span data-stu-id="066a5-143">The collation sequence is a fixed [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="066a5-144">**columnidcbMax**</span><span class="sxs-lookup"><span data-stu-id="066a5-144">**columnidcbMax**</span></span>

<span data-ttu-id="066a5-145">Identificador de columna del campo **cbMax** .</span><span class="sxs-lookup"><span data-stu-id="066a5-145">The column identifier of the **cbMax** field.</span></span>

<span data-ttu-id="066a5-146">**CbMax** es un [JET_coltypLong](./jet-coltyp.md)fijo.</span><span class="sxs-lookup"><span data-stu-id="066a5-146">The **cbMax** is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="066a5-147">**columnidgrbit**</span><span class="sxs-lookup"><span data-stu-id="066a5-147">**columnidgrbit**</span></span>

<span data-ttu-id="066a5-148">Identificador de columna del *grbits* de la columna.</span><span class="sxs-lookup"><span data-stu-id="066a5-148">The column identifier of the *grbits* of the column.</span></span> <span data-ttu-id="066a5-149">El campo *grbit* es un [JET_coltypLong](./jet-coltyp.md)fijo.</span><span class="sxs-lookup"><span data-stu-id="066a5-149">The *grbit* field is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span> <span data-ttu-id="066a5-150">Para obtener más información sobre estos bits, vea [JET_COLUMNDEF](./jet-columndef-structure.md).</span><span class="sxs-lookup"><span data-stu-id="066a5-150">For more information about these bits, see [JET_COLUMNDEF](./jet-columndef-structure.md).</span></span>

<span data-ttu-id="066a5-151">A continuación se muestran los posibles valores para **columnidgrbit**:</span><span class="sxs-lookup"><span data-stu-id="066a5-151">The following are possible values for **columnidgrbit**:</span></span>

<span data-ttu-id="066a5-152">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="066a5-152">JET_bitColumnTagged</span></span>

<span data-ttu-id="066a5-153">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="066a5-153">JET_bitColumnFixed</span></span>

<span data-ttu-id="066a5-154">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="066a5-154">JET_bitColumnUpdatable</span></span>

<span data-ttu-id="066a5-155">JET_bitColumnNotNULL</span><span class="sxs-lookup"><span data-stu-id="066a5-155">JET_bitColumnNotNULL</span></span>

<span data-ttu-id="066a5-156">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="066a5-156">JET_bitColumnAutoincrement</span></span>

<span data-ttu-id="066a5-157">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="066a5-157">JET_bitColumnVersion</span></span>

<span data-ttu-id="066a5-158">JET_bitColumnMultiValued</span><span class="sxs-lookup"><span data-stu-id="066a5-158">JET_bitColumnMultiValued</span></span>

<span data-ttu-id="066a5-159">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="066a5-159">JET_bitColumnEscrowUpdate</span></span>

<span data-ttu-id="066a5-160">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="066a5-160">JET_bitColumnFinalize</span></span>

<span data-ttu-id="066a5-161">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="066a5-161">JET_bitColumnDeleteOnZero</span></span>

<span data-ttu-id="066a5-162">JET_bitColumnUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="066a5-162">JET_bitColumnUserDefinedDefault</span></span>

<span data-ttu-id="066a5-163">**columnidDefault**</span><span class="sxs-lookup"><span data-stu-id="066a5-163">**columnidDefault**</span></span>

<span data-ttu-id="066a5-164">Identificador de columna del valor predeterminado de la columna.</span><span class="sxs-lookup"><span data-stu-id="066a5-164">The column identifier of the default value of the column.</span></span>

<span data-ttu-id="066a5-165">El valor predeterminado es un [JET_coltypLongBinary](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="066a5-165">The default value is a [JET_coltypLongBinary](./jet-coltyp.md).</span></span>

<span data-ttu-id="066a5-166">**columnidBaseTableName**</span><span class="sxs-lookup"><span data-stu-id="066a5-166">**columnidBaseTableName**</span></span>

<span data-ttu-id="066a5-167">El identificador de columna del nombre de la tabla de la que se derivó la tabla.</span><span class="sxs-lookup"><span data-stu-id="066a5-167">The column identifier of the name of the table from which the table was derived.</span></span>

<span data-ttu-id="066a5-168">El nombre de la tabla es un [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="066a5-168">The table name is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="066a5-169">**columnidBaseColumnName**</span><span class="sxs-lookup"><span data-stu-id="066a5-169">**columnidBaseColumnName**</span></span>

<span data-ttu-id="066a5-170">Identificador de columna del nombre de la columna de la que se derivó la columna.</span><span class="sxs-lookup"><span data-stu-id="066a5-170">The column identifier of the name of the column from which the column was derived.</span></span>

<span data-ttu-id="066a5-171">El nombre de la columna es un [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="066a5-171">The column name is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="066a5-172">**columnidDefinitionName**</span><span class="sxs-lookup"><span data-stu-id="066a5-172">**columnidDefinitionName**</span></span>

<span data-ttu-id="066a5-173">Identificador de columna del nombre de la definición de columna.</span><span class="sxs-lookup"><span data-stu-id="066a5-173">The column identifier of the name of the column definition.</span></span>

<span data-ttu-id="066a5-174">El nombre de la definición de columna es un [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="066a5-174">The column definition name is a [JET_coltypText](./jet-coltyp.md).</span></span>

### <a name="remarks"></a><span data-ttu-id="066a5-175">Observaciones</span><span class="sxs-lookup"><span data-stu-id="066a5-175">Remarks</span></span>

<span data-ttu-id="066a5-176">De forma predeterminada, el orden de las filas de la tabla temporal se ordena por el nombre de la columna.</span><span class="sxs-lookup"><span data-stu-id="066a5-176">By default, the order of the rows in the temporary table is sorted by the name of the column.</span></span> <span data-ttu-id="066a5-177">También se puede ordenar por identificador de columna.</span><span class="sxs-lookup"><span data-stu-id="066a5-177">It can also be sorted by column identifier.</span></span> <span data-ttu-id="066a5-178">Para obtener más información sobre cómo ordenar por identificador de columna, vea [JetGetColumnInfo](./jetgetcolumninfo-function.md) y [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="066a5-178">For more information about how to sort by column identifier, see [JetGetColumnInfo](./jetgetcolumninfo-function.md) and [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).</span></span>

<span data-ttu-id="066a5-179">La llamada a [JetGetColumnInfo](./jetgetcolumninfo-function.md) o [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) puede especificar una forma compacta de los resultados.</span><span class="sxs-lookup"><span data-stu-id="066a5-179">The call to [JetGetColumnInfo](./jetgetcolumninfo-function.md) or [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) might specify a compact form of results.</span></span> <span data-ttu-id="066a5-180">Si alguna columna se ha heredado de una tabla de plantilla, los resultados de Compact no las almacenarán.</span><span class="sxs-lookup"><span data-stu-id="066a5-180">If any columns have been inherited from a template table, the compact results will not store them.</span></span>

### <a name="requirements"></a><span data-ttu-id="066a5-181">Requisitos</span><span class="sxs-lookup"><span data-stu-id="066a5-181">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="066a5-182"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="066a5-182"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="066a5-183">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="066a5-183">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066a5-184"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="066a5-184"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="066a5-185">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="066a5-185">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066a5-186"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="066a5-186"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="066a5-187">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="066a5-187">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="066a5-188">Consulte también</span><span class="sxs-lookup"><span data-stu-id="066a5-188">See Also</span></span>

[<span data-ttu-id="066a5-189">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="066a5-189">JET_COLTYP</span></span>](./jet-coltyp.md)

[<span data-ttu-id="066a5-190">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="066a5-190">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)

[<span data-ttu-id="066a5-191">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="066a5-191">JET_COLUMNID</span></span>](./jet-columnid.md)

[<span data-ttu-id="066a5-192">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="066a5-192">JET_ERR</span></span>](./jet-err.md)

[<span data-ttu-id="066a5-193">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="066a5-193">JET_GRBIT</span></span>](./jet-grbit.md)

[<span data-ttu-id="066a5-194">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="066a5-194">JET_SESID</span></span>](./jet-sesid.md)

[<span data-ttu-id="066a5-195">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="066a5-195">JET_TABLEID</span></span>](./jet-tableid.md)

[<span data-ttu-id="066a5-196">JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="066a5-196">JetGetColumnInfo</span></span>](./jetgetcolumninfo-function.md)

[<span data-ttu-id="066a5-197">JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="066a5-197">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)
