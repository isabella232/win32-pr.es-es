---
description: 'Más información acerca de: estructura de JET_COLUMNBASE'
title: Estructura de JET_COLUMNBASE
TOCTitle: JET_COLUMNBASE Structure
ms:assetid: 171275c3-966d-409d-ad20-a8f240f7500d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269194(v=EXCHG.10)
ms:contentKeyID: 32765497
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
ms.openlocfilehash: 9276c36a08a429f44568b3a909af77f5ae038c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678505"
---
# <a name="jet_columnbase-structure"></a><span data-ttu-id="5c667-103">Estructura de JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="5c667-103">JET_COLUMNBASE Structure</span></span>


<span data-ttu-id="5c667-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5c667-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columnbase-structure"></a><span data-ttu-id="5c667-105">Estructura de JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="5c667-105">JET_COLUMNBASE Structure</span></span>

<span data-ttu-id="5c667-106">La estructura **JET_COLUMNBASE** describe los parámetros de una columna base.</span><span class="sxs-lookup"><span data-stu-id="5c667-106">The **JET_COLUMNBASE** structure describes the parameters of a base column.</span></span> <span data-ttu-id="5c667-107">Las funciones [JetGetColumnInfo](./jetgetcolumninfo-function.md) y [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) usan la estructura **JET_COLUMNBASE** .</span><span class="sxs-lookup"><span data-stu-id="5c667-107">The [JetGetColumnInfo](./jetgetcolumninfo-function.md) and [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) functions use the **JET_COLUMNBASE** structure.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_COLUMNID columnid;
      JET_COLTYP coltyp;
      unsigned short wCountry;
      unsigned short langid;
      unsigned short cp;
      unsigned short wFiller;
      unsigned long cbMax;
      JET_GRBIT grbit;
      tchar szBaseTableName[256];
      tchar szBaseColumnName[256];
    } JET_COLUMNBASE;
```

### <a name="members"></a><span data-ttu-id="5c667-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="5c667-108">Members</span></span>

<span data-ttu-id="5c667-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="5c667-109">**cbStruct**</span></span>

<span data-ttu-id="5c667-110">Tamaño de esta estructura, en bytes.</span><span class="sxs-lookup"><span data-stu-id="5c667-110">The size of this structure, in bytes.</span></span> <span data-ttu-id="5c667-111">Establezca **cbStruct** en sizeof (JET_COLUMNBASE).</span><span class="sxs-lookup"><span data-stu-id="5c667-111">Set **cbStruct** to sizeof( JET_COLUMNBASE ).</span></span>

<span data-ttu-id="5c667-112">**columnid**</span><span class="sxs-lookup"><span data-stu-id="5c667-112">**columnid**</span></span>

<span data-ttu-id="5c667-113">Reservado.</span><span class="sxs-lookup"><span data-stu-id="5c667-113">Reserved.</span></span> <span data-ttu-id="5c667-114">Establezca **columnid** en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="5c667-114">Set **columnid** to 0 (zero).</span></span>

<span data-ttu-id="5c667-115">**coltyp**</span><span class="sxs-lookup"><span data-stu-id="5c667-115">**coltyp**</span></span>

<span data-ttu-id="5c667-116">El tipo de la columna (por ejemplo, texto, binario o numérico).</span><span class="sxs-lookup"><span data-stu-id="5c667-116">The type of the column (for example, text, binary, or numerical).</span></span> <span data-ttu-id="5c667-117">Para obtener más información, vea [JET_COLTYP](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="5c667-117">For more information, see [JET_COLTYP](./jet-coltyp.md).</span></span>

<span data-ttu-id="5c667-118">**wCountry**</span><span class="sxs-lookup"><span data-stu-id="5c667-118">**wCountry**</span></span>

<span data-ttu-id="5c667-119">Reservado.</span><span class="sxs-lookup"><span data-stu-id="5c667-119">Reserved.</span></span> <span data-ttu-id="5c667-120">Se establece en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="5c667-120">Set to 0 (zero).</span></span>

<span data-ttu-id="5c667-121">**langid**</span><span class="sxs-lookup"><span data-stu-id="5c667-121">**langid**</span></span>

<span data-ttu-id="5c667-122">Reservado.</span><span class="sxs-lookup"><span data-stu-id="5c667-122">Reserved.</span></span> <span data-ttu-id="5c667-123">Se establece en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="5c667-123">Set to 0 (zero).</span></span>

<span data-ttu-id="5c667-124">**cp**</span><span class="sxs-lookup"><span data-stu-id="5c667-124">**cp**</span></span>

<span data-ttu-id="5c667-125">Página de códigos de la columna.</span><span class="sxs-lookup"><span data-stu-id="5c667-125">The code page for the column.</span></span> <span data-ttu-id="5c667-126">Los únicos valores válidos para las columnas de texto son inglés (1252) y Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="5c667-126">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="5c667-127">Un valor de cero significa que se usará el valor predeterminado (Inglés, 1252).</span><span class="sxs-lookup"><span data-stu-id="5c667-127">A value of zero means the default will be used (English, 1252).</span></span> <span data-ttu-id="5c667-128">Si la columna no es una columna de texto, la página de códigos se establece automáticamente en cero.</span><span class="sxs-lookup"><span data-stu-id="5c667-128">If the column is not a text column, the code page is automatically set to zero.</span></span>

<span data-ttu-id="5c667-129">**wFiller**</span><span class="sxs-lookup"><span data-stu-id="5c667-129">**wFiller**</span></span>

<span data-ttu-id="5c667-130">Reservado.</span><span class="sxs-lookup"><span data-stu-id="5c667-130">Reserved.</span></span> <span data-ttu-id="5c667-131">Se establece en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="5c667-131">Set to 0 (zero).</span></span>

<span data-ttu-id="5c667-132">**cbMax**</span><span class="sxs-lookup"><span data-stu-id="5c667-132">**cbMax**</span></span>

<span data-ttu-id="5c667-133">La longitud máxima, en bytes, de una columna de longitud variable, o la longitud real, en bytes, de una columna de longitud fija.</span><span class="sxs-lookup"><span data-stu-id="5c667-133">The maximum length, in bytes, of a variable-length column, or the actual length, in bytes, of a fixed-length column.</span></span>

<span data-ttu-id="5c667-134">**grbit**</span><span class="sxs-lookup"><span data-stu-id="5c667-134">**grbit**</span></span>

<span data-ttu-id="5c667-135">Opciones de la columna, incluidos cero o más de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="5c667-135">Options for the column, including zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5c667-136">Value</span><span class="sxs-lookup"><span data-stu-id="5c667-136">Value</span></span></p></th>
<th><p><span data-ttu-id="5c667-137">Significado</span><span class="sxs-lookup"><span data-stu-id="5c667-137">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c667-138">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="5c667-138">JET_bitColumnFixed</span></span></p></td>
<td><p><span data-ttu-id="5c667-139">La columna es fija y ocupa la misma cantidad de espacio en una fila, independientemente de la cantidad de datos que contenga.</span><span class="sxs-lookup"><span data-stu-id="5c667-139">The column is fixed and occupies the same amount of space in a row regardless of how much data it contains.</span></span> <span data-ttu-id="5c667-140">JET_bitColumnFixed no se pueden combinar con JET_bitColumnTagged y no se pueden usar cuando el miembro <strong>coltyp</strong> está establecido en <strong>JET_coltypLongText</strong> o <strong>JET_coltypLongBinary</strong>.</span><span class="sxs-lookup"><span data-stu-id="5c667-140">JET_bitColumnFixed cannot be combined with JET_bitColumnTagged, and cannot be used when the <strong>coltyp</strong> member is set to <strong>JET_coltypLongText</strong> or <strong>JET_coltypLongBinary</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c667-141">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="5c667-141">JET_bitColumnTagged</span></span></p></td>
<td><p><span data-ttu-id="5c667-142">La columna está etiquetada y ocupa espacio en la base de datos solo si contiene datos.</span><span class="sxs-lookup"><span data-stu-id="5c667-142">The column is tagged and occupies space in the database only if it contains data.</span></span> <span data-ttu-id="5c667-143">JET_bitColumnTagged no se pueden combinar con JET_bitColumnFixed, JET_bitColumnVersion o JET_bitColumnEscrowUpdate.</span><span class="sxs-lookup"><span data-stu-id="5c667-143">JET_bitColumnTagged cannot be combined with JET_bitColumnFixed, JET_bitColumnVersion, or JET_bitColumnEscrowUpdate.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c667-144">JET_bitColumnNotNULL</span><span class="sxs-lookup"><span data-stu-id="5c667-144">JET_bitColumnNotNULL</span></span></p></td>
<td><p><span data-ttu-id="5c667-145">La columna no se debe establecer en un valor <strong>null</strong> .</span><span class="sxs-lookup"><span data-stu-id="5c667-145">The column must not be set to a <strong>NULL</strong> value.</span></span></p>
<p><span data-ttu-id="5c667-146">JET_bitColumnNotNULL no se pueden combinar con JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="5c667-146">JET_bitColumnNotNULL cannot be combined with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c667-147">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="5c667-147">JET_bitColumnVersion</span></span></p></td>
<td><p><span data-ttu-id="5c667-148">La columna es una columna de versión que especifica la versión de la fila.</span><span class="sxs-lookup"><span data-stu-id="5c667-148">The column is a version column that specifies the version of the row.</span></span> <span data-ttu-id="5c667-149">El valor de esta columna comienza en cero y se incrementa automáticamente para cada actualización de la fila.</span><span class="sxs-lookup"><span data-stu-id="5c667-149">The value of this column starts at zero and is automatically incremented for each update of the row.</span></span></p>
<p><span data-ttu-id="5c667-150">JET_bitColumnVersion solo se puede usar cuando el miembro <strong>coltyp</strong> está establecido en <strong>JET_coltypLong</strong> y no se puede combinar con JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, JET_bitColumnTagged o JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="5c667-150">JET_bitColumnVersion can be used only when the <strong>coltyp</strong> member is set to <strong>JET_coltypLong</strong> and cannot be combined with JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, JET_bitColumnTagged, or JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c667-151">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="5c667-151">JET_bitColumnAutoincrement</span></span></p></td>
<td><p><span data-ttu-id="5c667-152">La columna se incrementa automáticamente.</span><span class="sxs-lookup"><span data-stu-id="5c667-152">The column is automatically incremented.</span></span> <span data-ttu-id="5c667-153">El número es un número cada vez mayor y se garantiza que es único dentro de una tabla.</span><span class="sxs-lookup"><span data-stu-id="5c667-153">The number is an increasing number, and is guaranteed to be unique within a table.</span></span> <span data-ttu-id="5c667-154">Sin embargo, los números no pueden ser secuenciales.</span><span class="sxs-lookup"><span data-stu-id="5c667-154">The numbers, however, may not be sequential.</span></span> <span data-ttu-id="5c667-155">Por ejemplo, si se insertan cinco filas en una tabla, la columna incrementada automáticamente puede contener los valores {1, 2, 6, 7, 8}.</span><span class="sxs-lookup"><span data-stu-id="5c667-155">For example, if five rows are inserted into a table, the automatically incremented column could contain the values { 1, 2, 6, 7, 8 }.</span></span></p>
<p><span data-ttu-id="5c667-156">JET_bitColumnAutoincrement solo se puede usar cuando el miembro <strong>coltyp</strong> se establece en <strong>JET_coltypLong</strong> o <strong>JET_coltypCurrency</strong> y no se puede combinar con JET_bitColumnEscrowUpdate, JET_bitColumnUserDefinedDefault o JET_bitColumnVersion.</span><span class="sxs-lookup"><span data-stu-id="5c667-156">JET_bitColumnAutoincrement can be used only when the <strong>coltyp</strong> member is set to <strong>JET_coltypLong</strong> or <strong>JET_coltypCurrency</strong> and cannot be combined with JET_bitColumnEscrowUpdate, JET_bitColumnUserDefinedDefault, or JET_bitColumnVersion.</span></span></p>
<p><span data-ttu-id="5c667-157"><strong>Windows 2000:  </strong> JET_bitColumnVersion solo se puede usar cuando el miembro <strong>coltyp</strong> está establecido en <strong>JET_coltypLong</strong>.</span><span class="sxs-lookup"><span data-stu-id="5c667-157"><strong>Windows 2000:  </strong>JET_bitColumnVersion can be used only when the <strong>coltyp</strong> member is set to <strong>JET_coltypLong</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c667-158">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="5c667-158">JET_bitColumnUpdatable</span></span></p></td>
<td><p><span data-ttu-id="5c667-159">Válido solo para llamadas a <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span><span class="sxs-lookup"><span data-stu-id="5c667-159">Valid only for calls to <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span></span> <span data-ttu-id="5c667-160">JET_bitColumnUpdatable no se pueden combinar con JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="5c667-160">JET_bitColumnUpdatable cannot be combined with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c667-161">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="5c667-161">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="5c667-162">Solo es válido en las llamadas a <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</span><span class="sxs-lookup"><span data-stu-id="5c667-162">Valid only on calls to <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c667-163">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="5c667-163">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="5c667-164">Solo es válido en las llamadas a <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span><span class="sxs-lookup"><span data-stu-id="5c667-164">Valid only on calls to <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c667-165">JET_bitColumnMultiValued</span><span class="sxs-lookup"><span data-stu-id="5c667-165">JET_bitColumnMultiValued</span></span></p></td>
<td><p><span data-ttu-id="5c667-166">La columna puede tener varios valores.</span><span class="sxs-lookup"><span data-stu-id="5c667-166">The column can be multi-valued.</span></span> <span data-ttu-id="5c667-167">Una columna con varios valores puede tener cero, uno o más valores asociados.</span><span class="sxs-lookup"><span data-stu-id="5c667-167">A multi-valued column can have zero, one, or more values associated with it.</span></span> <span data-ttu-id="5c667-168">Los distintos valores de una columna con varios valores se identifican por un número en el miembro <strong>itagSequence</strong> de varias estructuras, por ejemplo, <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a> <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span><span class="sxs-lookup"><span data-stu-id="5c667-168">The various values in a multi-valued column are identified by a number in the <strong>itagSequence</strong> member of various structures, for example, <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span></span> <span data-ttu-id="5c667-169">Las columnas con varios valores deben ser columnas etiquetadas; es decir, puede que no sean columnas de longitud fija o de longitud variable.</span><span class="sxs-lookup"><span data-stu-id="5c667-169">Multi-valued columns must be tagged columns; that is, they may not be fixed-length or variable-length columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c667-170">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="5c667-170">JET_bitColumnEscrowUpdate</span></span></p></td>
<td><p><span data-ttu-id="5c667-171">Especifica que una columna es una columna de actualización de custodia que se puede actualizar simultáneamente mediante sesiones diferentes con <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> y tendrá coherencia transaccional.</span><span class="sxs-lookup"><span data-stu-id="5c667-171">Specifies that a column is an escrow update column that can be updated concurrently by different sessions with <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> and will have transactional consistency.</span></span></p>
<ul>
<li><p><span data-ttu-id="5c667-172">Solo se puede crear una columna de actualización de custodia cuando la tabla está vacía.</span><span class="sxs-lookup"><span data-stu-id="5c667-172">An escrow update column can be created only when the table is empty.</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="5c667-173">En el caso de una columna de actualización de custodia, el miembro <strong>coltyp</strong> debe establecerse en <strong>JET_coltypLong.</strong></span><span class="sxs-lookup"><span data-stu-id="5c667-173">For an escrow update column, the <strong>coltyp</strong> member must be set to <strong>JET_coltypLong.</strong></span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="5c667-174">Una columna de actualización de custodia debe tener un valor predeterminado (es decir, <strong>cbDefault</strong> debe ser positivo).</span><span class="sxs-lookup"><span data-stu-id="5c667-174">An escrow update column must have a default value (that is <strong>cbDefault</strong> must be positive).</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="5c667-175">JET_bitColumnEscrowUpdate no se pueden combinar con JET_bitColumnTagged, JET_bitColumnVersion o JET_bitColumnAutoincrement.</span><span class="sxs-lookup"><span data-stu-id="5c667-175">JET_bitColumnEscrowUpdate cannot be combined with JET_bitColumnTagged, JET_bitColumnVersion, or JET_bitColumnAutoincrement.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c667-176">JET_bitColumnUnversioned</span><span class="sxs-lookup"><span data-stu-id="5c667-176">JET_bitColumnUnversioned</span></span></p></td>
<td><p><span data-ttu-id="5c667-177">La columna se crea sin un número de versión.</span><span class="sxs-lookup"><span data-stu-id="5c667-177">The column is created without a version number.</span></span> <span data-ttu-id="5c667-178">Esto significa que se producirá un error en otras transacciones que intenten agregar una columna con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="5c667-178">This means that other transactions attempting to add a column with the same name will fail.</span></span> <span data-ttu-id="5c667-179">JET_bitColumnUnversioned solo se usa con <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span><span class="sxs-lookup"><span data-stu-id="5c667-179">JET_bitColumnUnversioned is used only with <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span></span> <span data-ttu-id="5c667-180">No se puede utilizar dentro de una transacción.</span><span class="sxs-lookup"><span data-stu-id="5c667-180">It cannot be used within a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c667-181">JET_bitColumnMaybeNull</span><span class="sxs-lookup"><span data-stu-id="5c667-181">JET_bitColumnMaybeNull</span></span></p></td>
<td><p><span data-ttu-id="5c667-182">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="5c667-182">Reserved for future use.</span></span></p>
<p><span data-ttu-id="5c667-183">JET_bitColumnMaybeNull no se pueden combinar con JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="5c667-183">JET_bitColumnMaybeNull cannot be combined with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c667-184">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="5c667-184">JET_bitColumnFinalize</span></span></p></td>
<td><p><span data-ttu-id="5c667-185">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="5c667-185">Do not use.</span></span> <span data-ttu-id="5c667-186">En su lugar, use JET_bitColumnDeleteOnZero.</span><span class="sxs-lookup"><span data-stu-id="5c667-186">Use JET_bitColumnDeleteOnZero instead.</span></span></p>
<p><span data-ttu-id="5c667-187">La columna se puede finalizar.</span><span class="sxs-lookup"><span data-stu-id="5c667-187">The column can be finalized.</span></span> <span data-ttu-id="5c667-188">Una columna que se puede finalizar es una columna de actualización de custodia que hace que se elimine la fila cuando la columna llega a cero.</span><span class="sxs-lookup"><span data-stu-id="5c667-188">A column that can be finalized is an escrow update column that causes the row to be deleted when the column reaches zero.</span></span> <span data-ttu-id="5c667-189">En su lugar, las versiones futuras pueden invocar una función de devolución de llamada (vea <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>).</span><span class="sxs-lookup"><span data-stu-id="5c667-189">Future versions may invoke a callback function instead (See <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>).</span></span> <span data-ttu-id="5c667-190">Una columna que se puede finalizar debe ser una columna de actualización de custodia.</span><span class="sxs-lookup"><span data-stu-id="5c667-190">A column that can be finalized must be an escrow update column.</span></span> <span data-ttu-id="5c667-191">JET_bitColumnFinalize no se pueden combinar con JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="5c667-191">JET_bitColumnFinalize cannot be combined with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c667-192">JET_bitColumnUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="5c667-192">JET_bitColumnUserDefinedDefault</span></span></p></td>
<td><p><span data-ttu-id="5c667-193">La función de devolución de llamada proporcionará el valor predeterminado de una columna.</span><span class="sxs-lookup"><span data-stu-id="5c667-193">The default value for a column will be provided by a callback function.</span></span> <span data-ttu-id="5c667-194">Vea <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span><span class="sxs-lookup"><span data-stu-id="5c667-194">See <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span></span> <span data-ttu-id="5c667-195">Una columna que tiene un valor predeterminado definido por el usuario debe ser una columna etiquetada.</span><span class="sxs-lookup"><span data-stu-id="5c667-195">A column that has a user-defined default must be a tagged column.</span></span> <span data-ttu-id="5c667-196">Si se especifica JET_bitColumnUserDefinedDefault, <strong>pvDefault</strong> debe apuntar a una estructura de <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> y <strong>cbDefault</strong> debe establecerse en sizeof (JET_USERDEFINEDDEFAULT).</span><span class="sxs-lookup"><span data-stu-id="5c667-196">If JET_bitColumnUserDefinedDefault is specified, the <strong>pvDefault</strong> must point to a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure, and <strong>cbDefault</strong> must be set to sizeof( JET_USERDEFINEDDEFAULT ).</span></span></p>
<p><span data-ttu-id="5c667-197">JET_bitColumnUserDefinedDefault no se pueden combinar con JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero o JET_bitColumnMaybeNull.</span><span class="sxs-lookup"><span data-stu-id="5c667-197">JET_bitColumnUserDefinedDefault cannot be combined with JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero, or JET_bitColumnMaybeNull.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c667-198">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="5c667-198">JET_bitColumnDeleteOnZero</span></span></p></td>
<td><p><span data-ttu-id="5c667-199">La columna es una columna de actualización de custodia y, cuando llega a cero, se elimina el registro.</span><span class="sxs-lookup"><span data-stu-id="5c667-199">The column is an escrow update column and when it reaches zero, the record will be deleted.</span></span> <span data-ttu-id="5c667-200">Un uso común de las columnas delete-on-Zero es como campos de recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="5c667-200">A common use for delete-on-zero columns is as reference count fields.</span></span> <span data-ttu-id="5c667-201">Cuando el número de referencias llega a cero, se elimina el registro.</span><span class="sxs-lookup"><span data-stu-id="5c667-201">When the number of references fall to zero, the record is deleted.</span></span> <span data-ttu-id="5c667-202">Una columna de eliminación en cero debe ser una columna de actualización de custodia.</span><span class="sxs-lookup"><span data-stu-id="5c667-202">A delete-on-zero column must be an escrow update column.</span></span></p>
<p><span data-ttu-id="5c667-203">JET_bitColumnDeleteOnZero reemplaza JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="5c667-203">JET_bitColumnDeleteOnZero replaces JET_bitColumnFinalize.</span></span></p>
<p><span data-ttu-id="5c667-204">JET_bitColumnDeleteOnZero no se pueden combinar con JET_bitColumnFinalize o JET_bitColumnUserDefinedDefault, y no se pueden usar con columnas predeterminadas definidas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="5c667-204">JET_bitColumnDeleteOnZero cannot be combined with JET_bitColumnFinalize or JET_bitColumnUserDefinedDefault, and cannot be used with user-defined default columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5c667-205">**szBaseTableName**</span><span class="sxs-lookup"><span data-stu-id="5c667-205">**szBaseTableName**</span></span>

<span data-ttu-id="5c667-206">Tabla de la que la tabla actual hereda su DDL.</span><span class="sxs-lookup"><span data-stu-id="5c667-206">The table from which the current table inherits its DDL.</span></span>

<span data-ttu-id="5c667-207">**szBaseColumnName**</span><span class="sxs-lookup"><span data-stu-id="5c667-207">**szBaseColumnName**</span></span>

<span data-ttu-id="5c667-208">Nombre de la columna de la tabla de plantilla.</span><span class="sxs-lookup"><span data-stu-id="5c667-208">The name of the column in the template table.</span></span>

### <a name="remarks"></a><span data-ttu-id="5c667-209">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c667-209">Remarks</span></span>

<span data-ttu-id="5c667-210">**JET_COLUMNBASE** contiene gran parte de la misma información que [JET_COLUMNDEF](./jet-columndef-structure.md), pero agrega campos de cadena para describir la tabla base (si se ha utilizado un DDL jerárquico).</span><span class="sxs-lookup"><span data-stu-id="5c667-210">**JET_COLUMNBASE** contains much of the same information as [JET_COLUMNDEF](./jet-columndef-structure.md), but it adds string fields to describe the base table (if a hierarchical DDL was used).</span></span>

### <a name="requirements"></a><span data-ttu-id="5c667-211">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c667-211">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c667-212"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="5c667-212"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5c667-213">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="5c667-213">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c667-214"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="5c667-214"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5c667-215">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5c667-215">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c667-216"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="5c667-216"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5c667-217">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="5c667-217">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c667-218"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="5c667-218"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="5c667-219">Se implementa como <strong>JET_COLUMNBASE_W</strong> (Unicode) y <strong>JET_COLUMNBASE_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="5c667-219">Implemented as <strong>JET_COLUMNBASE_W</strong> (Unicode) and <strong>JET_COLUMNBASE_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="5c667-220">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5c667-220">See Also</span></span>

[<span data-ttu-id="5c667-221">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="5c667-221">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="5c667-222">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="5c667-222">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="5c667-223">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="5c667-223">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="5c667-224">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="5c667-224">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="5c667-225">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="5c667-225">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="5c667-226">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="5c667-226">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="5c667-227">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="5c667-227">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="5c667-228">JET_USERDEFINEDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="5c667-228">JET_USERDEFINEDDEFAULT</span></span>](./jet-userdefineddefault-structure.md)  
[<span data-ttu-id="5c667-229">JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="5c667-229">JetGetColumnInfo</span></span>](./jetgetcolumninfo-function.md)  
[<span data-ttu-id="5c667-230">JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="5c667-230">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)  
[<span data-ttu-id="5c667-231">JetRenameColumn</span><span class="sxs-lookup"><span data-stu-id="5c667-231">JetRenameColumn</span></span>](./jetrenamecolumn-function.md)
