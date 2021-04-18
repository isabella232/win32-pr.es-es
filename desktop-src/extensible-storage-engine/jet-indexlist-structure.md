---
description: 'Más información acerca de: estructura de JET_INDEXLIST'
title: Estructura de JET_INDEXLIST
TOCTitle: JET_INDEXLIST Structure
ms:assetid: 0c092b48-e583-49f3-8f5e-1428a84d9265
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269185(v=EXCHG.10)
ms:contentKeyID: 32765488
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
ms.openlocfilehash: a696d1c52a42cad2b3b67b047984b48d77637a1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360998"
---
# <a name="jet_indexlist-structure"></a><span data-ttu-id="1488a-103">Estructura de JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="1488a-103">JET_INDEXLIST Structure</span></span>


<span data-ttu-id="1488a-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1488a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_indexlist-structure"></a><span data-ttu-id="1488a-105">Estructura de JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="1488a-105">JET_INDEXLIST Structure</span></span>

<span data-ttu-id="1488a-106">La estructura de **JET_INDEXLIST** contiene la información necesaria para atravesar una tabla temporal creada por las funciones [JetGetIndexInfo](./jetgetindexinfo-function.md) o [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) .</span><span class="sxs-lookup"><span data-stu-id="1488a-106">The **JET_INDEXLIST** structure contains the necessary information to traverse a temporary table that is created by the [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) functions.</span></span> <span data-ttu-id="1488a-107">Cada fila de la tabla temporal describe una columna de un índice.</span><span class="sxs-lookup"><span data-stu-id="1488a-107">Each row in the temporary table describes a column of an index.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      gned long cRecord;
      JET_COLUMNID columnidindexname;
      JET_COLUMNID columnidgrbitIndex;
      JET_COLUMNID columnidcKey;
      JET_COLUMNID columnidcEntry;
      JET_COLUMNID columnidcPage;
      JET_COLUMNID columnidcColumn;
      JET_COLUMNID columnidiColumn;
      JET_COLUMNID columnidcolumnid;
      JET_COLUMNID columnidcoltyp;
      JET_COLUMNID columnidCountry;
      JET_COLUMNID columnidLangid;
      JET_COLUMNID columnidCp;
      JET_COLUMNID columnidCollate;
      JET_COLUMNID columnidgrbitColumn;
      JET_COLUMNID columnidcolumnname;
      JET_COLUMNID columnidLCMapFlags;
    } JET_INDEXLIST;
```

### <a name="members"></a><span data-ttu-id="1488a-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="1488a-108">Members</span></span>

<span data-ttu-id="1488a-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="1488a-109">**cbStruct**</span></span>

<span data-ttu-id="1488a-110">Tamaño de la estructura en bytes.</span><span class="sxs-lookup"><span data-stu-id="1488a-110">The size of the structure in bytes.</span></span> <span data-ttu-id="1488a-111">La llamada a la API actualizará este campo, por lo que el llamador debe asegurarse de que este valor coincide con sizeof (JET_INDEXLIST).</span><span class="sxs-lookup"><span data-stu-id="1488a-111">The API call will update this field, so the caller should ensure that this value matches sizeof( JET_INDEXLIST ).</span></span>

<span data-ttu-id="1488a-112">**TABLEID**</span><span class="sxs-lookup"><span data-stu-id="1488a-112">**tableid**</span></span>

<span data-ttu-id="1488a-113">Identificador de tabla de la tabla temporal que se creó.</span><span class="sxs-lookup"><span data-stu-id="1488a-113">The table identifier of the temporary table that was created.</span></span> <span data-ttu-id="1488a-114">Es responsabilidad del llamador cerrar la tabla.</span><span class="sxs-lookup"><span data-stu-id="1488a-114">It is the responsibility of the caller to close the table.</span></span>

<span data-ttu-id="1488a-115">**cRecord**</span><span class="sxs-lookup"><span data-stu-id="1488a-115">**cRecord**</span></span>

<span data-ttu-id="1488a-116">El número de registros de la tabla temporal que se creó.</span><span class="sxs-lookup"><span data-stu-id="1488a-116">The number of records in the temporary table that was created.</span></span>

<span data-ttu-id="1488a-117">**columnidindexname**</span><span class="sxs-lookup"><span data-stu-id="1488a-117">**columnidindexname**</span></span>

<span data-ttu-id="1488a-118">Identificador de columna del nombre del índice.</span><span class="sxs-lookup"><span data-stu-id="1488a-118">The column identifier of the name of the index.</span></span>

<span data-ttu-id="1488a-119">Esta columna es un [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="1488a-119">This column is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="1488a-120">**columnidgrbitIndex**</span><span class="sxs-lookup"><span data-stu-id="1488a-120">**columnidgrbitIndex**</span></span>

<span data-ttu-id="1488a-121">Identificador de columna del *grbits* que se usa en el índice.</span><span class="sxs-lookup"><span data-stu-id="1488a-121">The column identifier of the *grbits* used on the index.</span></span> <span data-ttu-id="1488a-122">Consulte [JET_INDEXCREATE](./jet-indexcreate-structure.md) para obtener una lista de bits válidos.</span><span class="sxs-lookup"><span data-stu-id="1488a-122">See [JET_INDEXCREATE](./jet-indexcreate-structure.md) for a list of valid bits.</span></span>

<span data-ttu-id="1488a-123">Esta columna es un [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="1488a-123">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="1488a-124">**columnidcKey**</span><span class="sxs-lookup"><span data-stu-id="1488a-124">**columnidcKey**</span></span>

<span data-ttu-id="1488a-125">Identificador de columna del número de claves del índice.</span><span class="sxs-lookup"><span data-stu-id="1488a-125">The column identifier of the number of keys in the index.</span></span>

<span data-ttu-id="1488a-126">Esta columna es un [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="1488a-126">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="1488a-127">**columnidcEntry**</span><span class="sxs-lookup"><span data-stu-id="1488a-127">**columnidcEntry**</span></span>

<span data-ttu-id="1488a-128">Identificador de columna del número de entradas del índice.</span><span class="sxs-lookup"><span data-stu-id="1488a-128">The column identifier of the number of entries in the index.</span></span>

<span data-ttu-id="1488a-129">Esta columna es un [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="1488a-129">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="1488a-130">**columnidcPage**</span><span class="sxs-lookup"><span data-stu-id="1488a-130">**columnidcPage**</span></span>

<span data-ttu-id="1488a-131">Identificador de columna del número de páginas que usa el índice. Esta columna es un [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="1488a-131">The column identifier of the number of pages the index uses.This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="1488a-132">**columnidcColumn**</span><span class="sxs-lookup"><span data-stu-id="1488a-132">**columnidcColumn**</span></span>

<span data-ttu-id="1488a-133">El identificador de columna del número total de columnas que abarca el índice.</span><span class="sxs-lookup"><span data-stu-id="1488a-133">The column identifier of the total number of columns that the index spans.</span></span>

<span data-ttu-id="1488a-134">Esta columna es un [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="1488a-134">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="1488a-135">**columnidiColumn**</span><span class="sxs-lookup"><span data-stu-id="1488a-135">**columnidiColumn**</span></span>

<span data-ttu-id="1488a-136">Identificador de columna del número de columnas del índice.</span><span class="sxs-lookup"><span data-stu-id="1488a-136">The column identifier of the number of the columns in the index.</span></span> <span data-ttu-id="1488a-137">Para obtener más información, consulte la sección Comentarios de este tema.</span><span class="sxs-lookup"><span data-stu-id="1488a-137">For more information, see the Remarks section of this topic.</span></span>

<span data-ttu-id="1488a-138">Esta columna es un [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="1488a-138">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1488a-139">Value</span><span class="sxs-lookup"><span data-stu-id="1488a-139">Value</span></span></p></th>
<th><p><span data-ttu-id="1488a-140">Significado</span><span class="sxs-lookup"><span data-stu-id="1488a-140">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1488a-141">cIndexInfoCols</span><span class="sxs-lookup"><span data-stu-id="1488a-141">cIndexInfoCols</span></span><br />
<span data-ttu-id="1488a-142">15</span><span class="sxs-lookup"><span data-stu-id="1488a-142">15</span></span></p></td>
<td><p><span data-ttu-id="1488a-143">Especifica que se permiten 15 columnas.</span><span class="sxs-lookup"><span data-stu-id="1488a-143">Specifies that 15 columns are allowed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1488a-144">cColumnInfoCols</span><span class="sxs-lookup"><span data-stu-id="1488a-144">cColumnInfoCols</span></span><br />
<span data-ttu-id="1488a-145">14</span><span class="sxs-lookup"><span data-stu-id="1488a-145">14</span></span></p></td>
<td><p><span data-ttu-id="1488a-146">Especifica que se permiten 14 columnas.</span><span class="sxs-lookup"><span data-stu-id="1488a-146">Specifies that 14 columns are allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1488a-147">cObjectInfoCols</span><span class="sxs-lookup"><span data-stu-id="1488a-147">cObjectInfoCols</span></span><br />
<span data-ttu-id="1488a-148">9</span><span class="sxs-lookup"><span data-stu-id="1488a-148">9</span></span></p></td>
<td><p><span data-ttu-id="1488a-149">Especifica que se permiten 9 columnas.</span><span class="sxs-lookup"><span data-stu-id="1488a-149">Specifies that 9 columns are allowed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1488a-150">**columnidcolumnid**</span><span class="sxs-lookup"><span data-stu-id="1488a-150">**columnidcolumnid**</span></span>

<span data-ttu-id="1488a-151">El identificador de columna de la columna que está indizada. Para obtener más información, consulte la sección Comentarios de este tema.</span><span class="sxs-lookup"><span data-stu-id="1488a-151">The column identifier of the column that is indexed.For more information, see the Remarks section of this topic.</span></span> <span data-ttu-id="1488a-152">Esta columna es un [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="1488a-152">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="1488a-153">**columnidcoltyp**</span><span class="sxs-lookup"><span data-stu-id="1488a-153">**columnidcoltyp**</span></span>

<span data-ttu-id="1488a-154">Identificador de columna del coltyp de la columna que está indizada.</span><span class="sxs-lookup"><span data-stu-id="1488a-154">The column identifier of the coltyp of the column which is indexed.</span></span> <span data-ttu-id="1488a-155">Para obtener más información, consulte la sección Comentarios de este tema.</span><span class="sxs-lookup"><span data-stu-id="1488a-155">For more information, see the Remarks section of this topic.</span></span> <span data-ttu-id="1488a-156">Esta columna es un [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="1488a-156">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="1488a-157">**columnidCountry**</span><span class="sxs-lookup"><span data-stu-id="1488a-157">**columnidCountry**</span></span>

<span data-ttu-id="1488a-158">Identificador de columna del código de país de la columna indizada.</span><span class="sxs-lookup"><span data-stu-id="1488a-158">The column identifier of the country code of the column that is indexed.</span></span> <span data-ttu-id="1488a-159">El código de país está en desuso.</span><span class="sxs-lookup"><span data-stu-id="1488a-159">The country code is deprecated.</span></span>

<span data-ttu-id="1488a-160">Esta columna es un [JET_coltypShort](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="1488a-160">This column is a [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="1488a-161">**columnidLangid**</span><span class="sxs-lookup"><span data-stu-id="1488a-161">**columnidLangid**</span></span>

<span data-ttu-id="1488a-162">Identificador de columna del identificador de idioma (LCID) en el que se creó el índice.</span><span class="sxs-lookup"><span data-stu-id="1488a-162">The column identifier of the language identifier (LCID) under which the index was created.</span></span> <span data-ttu-id="1488a-163">Para obtener más información, vea [JET_INDEXCREATE](./jet-indexcreate-structure.md).</span><span class="sxs-lookup"><span data-stu-id="1488a-163">For more information, see [JET_INDEXCREATE](./jet-indexcreate-structure.md).</span></span>

<span data-ttu-id="1488a-164">Esta columna es un [JET_coltypShort](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="1488a-164">This column is a [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="1488a-165">**columnidCp**</span><span class="sxs-lookup"><span data-stu-id="1488a-165">**columnidCp**</span></span>

<span data-ttu-id="1488a-166">El identificador de columna de la página de códigos en la que se creó el índice.</span><span class="sxs-lookup"><span data-stu-id="1488a-166">The column identifier of the code page under which the index was created.</span></span> <span data-ttu-id="1488a-167">Para obtener más información, vea [JET_COLUMNCREATE](./jet-columncreate-structure.md).</span><span class="sxs-lookup"><span data-stu-id="1488a-167">For more information, see [JET_COLUMNCREATE](./jet-columncreate-structure.md).</span></span>

<span data-ttu-id="1488a-168">Esta columna es un [JET_coltypShort](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="1488a-168">This column is a [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="1488a-169">**columnidCollate**</span><span class="sxs-lookup"><span data-stu-id="1488a-169">**columnidCollate**</span></span>

<span data-ttu-id="1488a-170">El identificador de columna de la secuencia de intercalación en la que se creó el índice.</span><span class="sxs-lookup"><span data-stu-id="1488a-170">The column identifier of the collation sequence under which the index was created.</span></span> <span data-ttu-id="1488a-171">La secuencia de intercalación está en desuso.</span><span class="sxs-lookup"><span data-stu-id="1488a-171">The collation sequence is deprecated.</span></span>

<span data-ttu-id="1488a-172">Esta columna es un [JET_coltypShort](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="1488a-172">This column is a [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="1488a-173">**columnidgrbitColumn**</span><span class="sxs-lookup"><span data-stu-id="1488a-173">**columnidgrbitColumn**</span></span>

<span data-ttu-id="1488a-174">Identificador de columna del *grbits* que se aplica al orden de la columna en el índice.</span><span class="sxs-lookup"><span data-stu-id="1488a-174">The column identifier of the *grbits* that apply to the order of the column in the index.</span></span>

<span data-ttu-id="1488a-175">Los datos de esta columna se pueden ordenar como JET_bitKeyAscending o JET_bitKeyDescending.</span><span class="sxs-lookup"><span data-stu-id="1488a-175">The data for this column can be ordered as JET_bitKeyAscending or JET_bitKeyDescending.</span></span> <span data-ttu-id="1488a-176">Esta columna es un [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="1488a-176">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span> <span data-ttu-id="1488a-177">Por ejemplo, un índice definido como "-column1 \\ 0 + columna2 \\ 0" tendrá JET_bitKeyDescending para "column1" y JET_bitKeyAscending para "columna2".</span><span class="sxs-lookup"><span data-stu-id="1488a-177">For example, an index defined as "-column1\\0+column2\\0" will have JET_bitKeyDescending for "column1", and JET_bitKeyAscending for "column2".</span></span>

<span data-ttu-id="1488a-178">Las siguientes opciones son válidas para este miembro.</span><span class="sxs-lookup"><span data-stu-id="1488a-178">The following options are valid for this member.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1488a-179">Value</span><span class="sxs-lookup"><span data-stu-id="1488a-179">Value</span></span></p></th>
<th><p><span data-ttu-id="1488a-180">Significado</span><span class="sxs-lookup"><span data-stu-id="1488a-180">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1488a-181">JET_bitKeyAscending</span><span class="sxs-lookup"><span data-stu-id="1488a-181">JET_bitKeyAscending</span></span></p></td>
<td><p><span data-ttu-id="1488a-182">Un segmento de índice en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="1488a-182">An index segment in ascending order.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1488a-183">JET_bitKeyDescending</span><span class="sxs-lookup"><span data-stu-id="1488a-183">JET_bitKeyDescending</span></span></p></td>
<td><p><span data-ttu-id="1488a-184">Un segmento de índice en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="1488a-184">An index segment in descending order.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1488a-185">**columnidcolumnname**</span><span class="sxs-lookup"><span data-stu-id="1488a-185">**columnidcolumnname**</span></span>

<span data-ttu-id="1488a-186">Identificador de columna del nombre de la columna.</span><span class="sxs-lookup"><span data-stu-id="1488a-186">The column identifier of the name of the column.</span></span>

<span data-ttu-id="1488a-187">Esta columna es un [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="1488a-187">This column is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="1488a-188">**columnidLCMapFlags**</span><span class="sxs-lookup"><span data-stu-id="1488a-188">**columnidLCMapFlags**</span></span>

<span data-ttu-id="1488a-189">El identificador de columna de las marcas que se usan para crear el índice.</span><span class="sxs-lookup"><span data-stu-id="1488a-189">The column identifier of the flags that are used to create the index.</span></span> <span data-ttu-id="1488a-190">Para obtener más información, consulte la sección **dwMapFlags** de [JET_UNICODEINDEX](./jet-unicodeindex-structure.md).</span><span class="sxs-lookup"><span data-stu-id="1488a-190">For more information, see the **dwMapFlags** section of [JET_UNICODEINDEX](./jet-unicodeindex-structure.md).</span></span>

<span data-ttu-id="1488a-191">Esta columna es un [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="1488a-191">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

### <a name="remarks"></a><span data-ttu-id="1488a-192">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1488a-192">Remarks</span></span>

<span data-ttu-id="1488a-193">Cada fila de la tabla temporal corresponde a una columna de un índice determinado.</span><span class="sxs-lookup"><span data-stu-id="1488a-193">Each row in the temporary table corresponds to a column in a particular index.</span></span>

<span data-ttu-id="1488a-194">Por ejemplo, el índice "+ A \\ 0 + B \\ 0 + C 0 \\ + D \\ 0 + E \\ 0" tiene más de cinco columnas y ocupará cinco filas en la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="1488a-194">For example, the index "+A\\0+B\\0+C\\0+D\\0+E\\0" is more than five columns, and it will occupy five rows in the temporary table.</span></span> <span data-ttu-id="1488a-195">Cada una de estas cinco filas tendrá un valor de 5 en la columna identificada por la columna columnid.</span><span class="sxs-lookup"><span data-stu-id="1488a-195">Each of these five rows will have a value of 5 in the column that is identified by columnid column.</span></span> <span data-ttu-id="1488a-196">Pero cada fila tendrá un valor diferente para la columna columnid, que va de 0 a 4.</span><span class="sxs-lookup"><span data-stu-id="1488a-196">But each row will have a different value for columnid column, ranging from 0 to 4.</span></span>

<span data-ttu-id="1488a-197">El número de claves de un índice determinado corresponde al número de valores únicos para los que un llamador puede buscar y obtener una coincidencia exacta.</span><span class="sxs-lookup"><span data-stu-id="1488a-197">The number of keys in a particular index corresponds to the number of unique values for which a caller can seek and get an exact match.</span></span> <span data-ttu-id="1488a-198">El número de entradas es el número de filas que coincide con un índice.</span><span class="sxs-lookup"><span data-stu-id="1488a-198">The number of entries is the number of rows that an index matches.</span></span> <span data-ttu-id="1488a-199">Si un índice tiene una restricción de unicidad, el número de claves es igual al número de entradas.</span><span class="sxs-lookup"><span data-stu-id="1488a-199">If an index has a uniqueness constraint, then the number of keys is equal to the number of entries.</span></span> <span data-ttu-id="1488a-200">Por ejemplo, si una tabla contiene la siguiente información y se crea un índice sobre la columna denominada "Key", hay tres claves (100, 200 y 500), pero hay cuatro entradas ("this", "is", "a" y "example").</span><span class="sxs-lookup"><span data-stu-id="1488a-200">For example, if a table contains the following information and an index is created over the column named "key", then there are three keys (100, 200, and 500), but there are four entries ("this", "is", "an", and "example").</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1488a-201">Clave</span><span class="sxs-lookup"><span data-stu-id="1488a-201">Key</span></span></p></th>
<th><p><span data-ttu-id="1488a-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="1488a-202">Entry</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1488a-203">100</span><span class="sxs-lookup"><span data-stu-id="1488a-203">100</span></span></p></td>
<td><p><span data-ttu-id="1488a-204">&quot;this&quot;</span><span class="sxs-lookup"><span data-stu-id="1488a-204">&quot;this&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1488a-205">100</span><span class="sxs-lookup"><span data-stu-id="1488a-205">100</span></span></p></td>
<td><p><span data-ttu-id="1488a-206">&quot;is&quot;</span><span class="sxs-lookup"><span data-stu-id="1488a-206">&quot;is&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1488a-207">200</span><span class="sxs-lookup"><span data-stu-id="1488a-207">200</span></span></p></td>
<td><p><span data-ttu-id="1488a-208">&quot;alternativa&quot;</span><span class="sxs-lookup"><span data-stu-id="1488a-208">&quot;an&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1488a-209">500</span><span class="sxs-lookup"><span data-stu-id="1488a-209">500</span></span></p></td>
<td><p><span data-ttu-id="1488a-210">&quot;example&quot;</span><span class="sxs-lookup"><span data-stu-id="1488a-210">&quot;example&quot;</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="1488a-211">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1488a-211">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1488a-212"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="1488a-212"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1488a-213">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="1488a-213">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1488a-214"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="1488a-214"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1488a-215">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="1488a-215">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1488a-216"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="1488a-216"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1488a-217">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="1488a-217">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="1488a-218">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1488a-218">See Also</span></span>

[<span data-ttu-id="1488a-219">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="1488a-219">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="1488a-220">JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="1488a-220">JET_COLUMNCREATE</span></span>](./jet-columncreate-structure.md)  
[<span data-ttu-id="1488a-221">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="1488a-221">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="1488a-222">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1488a-222">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1488a-223">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="1488a-223">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="1488a-224">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="1488a-224">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="1488a-225">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="1488a-225">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="1488a-226">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="1488a-226">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="1488a-227">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="1488a-227">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="1488a-228">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="1488a-228">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="1488a-229">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="1488a-229">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)
