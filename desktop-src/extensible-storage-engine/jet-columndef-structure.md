---
description: 'Más información acerca de: estructura de JET_COLUMNDEF'
title: Estructura de JET_COLUMNDEF
TOCTitle: JET_COLUMNDEF Structure
ms:assetid: ee1fc473-bff5-438e-98ae-247de12e76f9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294130(v=EXCHG.10)
ms:contentKeyID: 32765744
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
ms.openlocfilehash: c541b5801c95f4b269e33360f5ffa2404ff8fc06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003083"
---
# <a name="jet_columndef-structure"></a><span data-ttu-id="d3075-103">Estructura de JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="d3075-103">JET_COLUMNDEF Structure</span></span>


<span data-ttu-id="d3075-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d3075-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columndef-structure"></a><span data-ttu-id="d3075-105">Estructura de JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="d3075-105">JET_COLUMNDEF Structure</span></span>

<span data-ttu-id="d3075-106">La estructura **JET_COLUMNDEF** define los datos que se pueden almacenar en una columna.</span><span class="sxs-lookup"><span data-stu-id="d3075-106">The **JET_COLUMNDEF** structure defines the data that can be stored in a column.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_COLUMNID columnid;
      JET_COLTYP coltyp;
      unsigned short wCountry;
      unsigned short langid;
      unsigned short cp;
      unsigned short wCollate;
      unsigned long cbMax;
      JET_GRBIT grbit;
    } JET_COLUMNDEF;
```

### <a name="members"></a><span data-ttu-id="d3075-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="d3075-107">Members</span></span>

<span data-ttu-id="d3075-108">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="d3075-108">**cbStruct**</span></span>

<span data-ttu-id="d3075-109">Tamaño de la estructura, en bytes.</span><span class="sxs-lookup"><span data-stu-id="d3075-109">The size of the structure, in bytes.</span></span> <span data-ttu-id="d3075-110">Debe establecerse en sizeof (JET_COLUMNDEF).</span><span class="sxs-lookup"><span data-stu-id="d3075-110">It must be set to sizeof( JET_COLUMNDEF).</span></span>

<span data-ttu-id="d3075-111">**columnid**</span><span class="sxs-lookup"><span data-stu-id="d3075-111">**columnid**</span></span>

<span data-ttu-id="d3075-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="d3075-112">Reserved.</span></span> <span data-ttu-id="d3075-113">**columnid** debe establecerse en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="d3075-113">**columnid** must be set to 0 (zero).</span></span>

<span data-ttu-id="d3075-114">**coltyp**</span><span class="sxs-lookup"><span data-stu-id="d3075-114">**coltyp**</span></span>

<span data-ttu-id="d3075-115">El tipo de la columna (por ejemplo, texto, binario o numérico).</span><span class="sxs-lookup"><span data-stu-id="d3075-115">The type of the column (for example, text, binary, or numerical).</span></span> <span data-ttu-id="d3075-116">Para obtener más información, vea [JET_COLTYP](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="d3075-116">For more information, see [JET_COLTYP](./jet-coltyp.md).</span></span>

<span data-ttu-id="d3075-117">**wCountry**</span><span class="sxs-lookup"><span data-stu-id="d3075-117">**wCountry**</span></span>

<span data-ttu-id="d3075-118">Reservado.</span><span class="sxs-lookup"><span data-stu-id="d3075-118">Reserved.</span></span> <span data-ttu-id="d3075-119">**wCountry** debe establecerse en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="d3075-119">**wCountry** must be set to 0 (zero).</span></span>

<span data-ttu-id="d3075-120">**langid**</span><span class="sxs-lookup"><span data-stu-id="d3075-120">**langid**</span></span>

<span data-ttu-id="d3075-121">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="d3075-121">Obsolete.</span></span> <span data-ttu-id="d3075-122">**langid** debe establecerse en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="d3075-122">**langid** should be set to 0 (zero).</span></span>

<span data-ttu-id="d3075-123">**cp**</span><span class="sxs-lookup"><span data-stu-id="d3075-123">**cp**</span></span>

<span data-ttu-id="d3075-124">Página de códigos de la columna.</span><span class="sxs-lookup"><span data-stu-id="d3075-124">The code page for the column.</span></span> <span data-ttu-id="d3075-125">Los únicos valores válidos para las columnas de texto son inglés (1252) y Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="d3075-125">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="d3075-126">Un valor de cero significa que se usará el valor predeterminado (Inglés, 1252).</span><span class="sxs-lookup"><span data-stu-id="d3075-126">A value of zero means the default will be used (English, 1252).</span></span> <span data-ttu-id="d3075-127">Si la columna no es una columna de texto, la página de códigos se establece automáticamente en cero.</span><span class="sxs-lookup"><span data-stu-id="d3075-127">If the column is not a text column, the code page automatically gets set to zero.</span></span>

<span data-ttu-id="d3075-128">**wCollate**</span><span class="sxs-lookup"><span data-stu-id="d3075-128">**wCollate**</span></span>

<span data-ttu-id="d3075-129">Reservado.</span><span class="sxs-lookup"><span data-stu-id="d3075-129">Reserved.</span></span> <span data-ttu-id="d3075-130">**wCollate** debe establecerse en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="d3075-130">**wCollate** must be set to 0 (zero).</span></span>

<span data-ttu-id="d3075-131">**cbMax**</span><span class="sxs-lookup"><span data-stu-id="d3075-131">**cbMax**</span></span>

<span data-ttu-id="d3075-132">La longitud máxima, en bytes, de una columna de longitud variable o la longitud de una columna de longitud fija.</span><span class="sxs-lookup"><span data-stu-id="d3075-132">The maximum length, in bytes, of a variable-length column, or the length of a fixed-length column.</span></span>

<span data-ttu-id="d3075-133">**grbit**</span><span class="sxs-lookup"><span data-stu-id="d3075-133">**grbit**</span></span>

<span data-ttu-id="d3075-134">Grupo de bits que contiene las opciones que se van a usar para esta llamada, que incluyen cero o más de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d3075-134">A group of bits that contain the options to be used for this call, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d3075-135">Value</span><span class="sxs-lookup"><span data-stu-id="d3075-135">Value</span></span></p></th>
<th><p><span data-ttu-id="d3075-136">Significado</span><span class="sxs-lookup"><span data-stu-id="d3075-136">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d3075-137">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="d3075-137">JET_bitColumnFixed</span></span></p></td>
<td><p><span data-ttu-id="d3075-138">Se corregirá la columna.</span><span class="sxs-lookup"><span data-stu-id="d3075-138">The column will be fixed.</span></span> <span data-ttu-id="d3075-139">Siempre usará la misma cantidad de espacio en una fila, independientemente de la cantidad de datos que se estén almacenando en la columna.</span><span class="sxs-lookup"><span data-stu-id="d3075-139">It will always use the same amount of space in a row, regardless of how much data is being stored in the column.</span></span> <span data-ttu-id="d3075-140">No se puede usar JET_bitColumnFixed con JET_bitColumnTagged.</span><span class="sxs-lookup"><span data-stu-id="d3075-140">JET_bitColumnFixed cannot be used with JET_bitColumnTagged.</span></span> <span data-ttu-id="d3075-141">Este bit no se puede usar con valores Long (es decir <strong>JET_coltypLongText</strong> y <strong>JET_coltypLongBinary</strong>).</span><span class="sxs-lookup"><span data-stu-id="d3075-141">This bit cannot be used with long values (that is <strong>JET_coltypLongText</strong> and <strong>JET_coltypLongBinary</strong>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3075-142">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="d3075-142">JET_bitColumnTagged</span></span></p></td>
<td><p><span data-ttu-id="d3075-143">La columna se etiquetará.</span><span class="sxs-lookup"><span data-stu-id="d3075-143">The column will be tagged.</span></span> <span data-ttu-id="d3075-144">Las columnas etiquetadas no ocupan espacio en la base de datos si no contienen datos.</span><span class="sxs-lookup"><span data-stu-id="d3075-144">Tagged columns do not take up any space in the database if they do not contain data.</span></span> <span data-ttu-id="d3075-145">Este bit no se puede usar con JET_bitColumnFixed.</span><span class="sxs-lookup"><span data-stu-id="d3075-145">This bit cannot be used with JET_bitColumnFixed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3075-146">JET_bitColumnNotNULL</span><span class="sxs-lookup"><span data-stu-id="d3075-146">JET_bitColumnNotNULL</span></span></p></td>
<td><p><span data-ttu-id="d3075-147">La columna nunca se debe establecer en un valor NULL.</span><span class="sxs-lookup"><span data-stu-id="d3075-147">The column must never be set to a NULL value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3075-148">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="d3075-148">JET_bitColumnVersion</span></span></p></td>
<td><p><span data-ttu-id="d3075-149">La columna es una columna de versión que especifica la versión de la fila.</span><span class="sxs-lookup"><span data-stu-id="d3075-149">The column is a version column that specifies the version of the row.</span></span> <span data-ttu-id="d3075-150">El valor de esta columna comienza en cero y se incrementa automáticamente para cada actualización de la fila.</span><span class="sxs-lookup"><span data-stu-id="d3075-150">The value of this column starts at zero and will be automatically incremented for each update on the row.</span></span></p>
<p><span data-ttu-id="d3075-151">Este bit solo se puede aplicar a columnas de <strong>JET_coltypLong</strong> .</span><span class="sxs-lookup"><span data-stu-id="d3075-151">This bit can only be applied to <strong>JET_coltypLong</strong> columns.</span></span> <span data-ttu-id="d3075-152">Este bit no se puede usar con JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate o JET_bitColumnTagged.</span><span class="sxs-lookup"><span data-stu-id="d3075-152">This bit cannot be used with JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, or JET_bitColumnTagged.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3075-153">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="d3075-153">JET_bitColumnAutoincrement</span></span></p></td>
<td><p><span data-ttu-id="d3075-154">La columna se incrementará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="d3075-154">The column will automatically be incremented.</span></span> <span data-ttu-id="d3075-155">El número es un número cada vez mayor y se garantiza que es único dentro de una tabla.</span><span class="sxs-lookup"><span data-stu-id="d3075-155">The number is an increasing number, and is guaranteed to be unique within a table.</span></span> <span data-ttu-id="d3075-156">Sin embargo, los números podrían no ser continuos.</span><span class="sxs-lookup"><span data-stu-id="d3075-156">The numbers, however, might not be continuous.</span></span> <span data-ttu-id="d3075-157">Por ejemplo, si se insertan cinco filas en una tabla, la &quot; columna AutoIncrement &quot; puede contener los valores {1, 2, 6, 7, 8}.</span><span class="sxs-lookup"><span data-stu-id="d3075-157">For example, if five rows are inserted into a table, the &quot;autoincrement&quot; column could contain the values { 1, 2, 6, 7, 8 }.</span></span> <span data-ttu-id="d3075-158">Este bit solo se puede usar en columnas de tipo <strong>JET_coltypLong</strong> o <strong>JET_coltypCurrency</strong>.</span><span class="sxs-lookup"><span data-stu-id="d3075-158">This bit can only be used on columns of type <strong>JET_coltypLong</strong> or <strong>JET_coltypCurrency</strong>.</span></span></p>
<p><span data-ttu-id="d3075-159"><strong>Windows 2000:  </strong> En Windows 2000, este bit solo se puede usar en columnas de tipo <strong>JET_coltypLong</strong>.</span><span class="sxs-lookup"><span data-stu-id="d3075-159"><strong>Windows 2000:  </strong>In Windows 2000, this bit can only be used on columns of type <strong>JET_coltypLong</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3075-160">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="d3075-160">JET_bitColumnUpdatable</span></span></p></td>
<td><p><span data-ttu-id="d3075-161">Este bit solo es válido en las llamadas a <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span><span class="sxs-lookup"><span data-stu-id="d3075-161">This bit is valid only on calls to <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3075-162">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="d3075-162">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="d3075-163">Este bit solo es válido en las llamadas a <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</span><span class="sxs-lookup"><span data-stu-id="d3075-163">This bit is valid only on calls to <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3075-164">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="d3075-164">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="d3075-165">Este bit solo es válido en las llamadas a <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span><span class="sxs-lookup"><span data-stu-id="d3075-165">This bit is valid only on calls to <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3075-166">JET_bitColumnMultiValued</span><span class="sxs-lookup"><span data-stu-id="d3075-166">JET_bitColumnMultiValued</span></span></p></td>
<td><p><span data-ttu-id="d3075-167">La columna puede tener varios valores.</span><span class="sxs-lookup"><span data-stu-id="d3075-167">The column can be multi-valued.</span></span> <span data-ttu-id="d3075-168">Una columna con varios valores puede tener cero, uno o más valores asociados.</span><span class="sxs-lookup"><span data-stu-id="d3075-168">A multi-valued column can have zero, one, or more values associated with it.</span></span> <span data-ttu-id="d3075-169">Los distintos valores de una columna con varios valores se identifican mediante un número denominado miembro <strong>itagSequence</strong> , que pertenece a varias estructuras, entre las que se incluyen: <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>y <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span><span class="sxs-lookup"><span data-stu-id="d3075-169">The various values in a multi-valued column are identified by a number called the <strong>itagSequence</strong> member, which belongs to various structures, including: <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, and <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span></span> <span data-ttu-id="d3075-170">Las columnas con varios valores deben ser columnas etiquetadas; es decir, no pueden ser columnas de longitud fija o de longitud variable.</span><span class="sxs-lookup"><span data-stu-id="d3075-170">Multi-valued columns must be tagged columns; that is, they cannot be fixed-length or variable-length columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3075-171">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="d3075-171">JET_bitColumnEscrowUpdate</span></span></p></td>
<td><p><span data-ttu-id="d3075-172">Especifica que una columna es una columna de actualización de custodia.</span><span class="sxs-lookup"><span data-stu-id="d3075-172">Specifies that a column is an escrow update column.</span></span> <span data-ttu-id="d3075-173">Una columna de actualización de custodia se puede actualizar simultáneamente mediante sesiones diferentes con <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> y mantendrá la coherencia transaccional.</span><span class="sxs-lookup"><span data-stu-id="d3075-173">An escrow update column can be updated concurrently by different sessions with <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> and will maintain transactional consistency.</span></span> <span data-ttu-id="d3075-174">Una columna de actualización de custodia también debe cumplir las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="d3075-174">An escrow update column must also meet the following conditions:</span></span></p>
<ul>
<li><p><span data-ttu-id="d3075-175">Solo se puede crear una columna de actualización de custodia cuando la tabla está vacía.</span><span class="sxs-lookup"><span data-stu-id="d3075-175">An escrow update column can be created only when the table is empty.</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="d3075-176">Una columna de actualización de custodia debe ser del tipo <strong>JET_coltypLong</strong>.</span><span class="sxs-lookup"><span data-stu-id="d3075-176">An escrow update column must be of type <strong>JET_coltypLong</strong>.</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="d3075-177">Una columna de actualización de custodia debe tener un valor predeterminado (es decir, <strong>cbDefault</strong> debe ser positivo).</span><span class="sxs-lookup"><span data-stu-id="d3075-177">An escrow update column must have a default value (that is <strong>cbDefault</strong> must be positive).</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="d3075-178">No se puede usar JET_bitColumnEscrowUpdate junto con JET_bitColumnTagged, JET_bitColumnVersion o JET_bitColumnAutoincrement.</span><span class="sxs-lookup"><span data-stu-id="d3075-178">JET_bitColumnEscrowUpdate cannot be used in conjunction with JET_bitColumnTagged, JET_bitColumnVersion, or JET_bitColumnAutoincrement.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3075-179">JET_bitColumnUnversioned</span><span class="sxs-lookup"><span data-stu-id="d3075-179">JET_bitColumnUnversioned</span></span></p></td>
<td><p><span data-ttu-id="d3075-180">La columna se creará en una sin información de versión.</span><span class="sxs-lookup"><span data-stu-id="d3075-180">The column will be created in an without version information.</span></span> <span data-ttu-id="d3075-181">Esto significa que se producirá un error en otras transacciones que intenten agregar una columna con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="d3075-181">This means that other transactions that attempt to add a column with the same name will fail.</span></span> <span data-ttu-id="d3075-182">Este bit solo es útil con <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span><span class="sxs-lookup"><span data-stu-id="d3075-182">This bit is only useful with <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span></span> <span data-ttu-id="d3075-183">No se puede utilizar dentro de una transacción.</span><span class="sxs-lookup"><span data-stu-id="d3075-183">It cannot be used within a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3075-184">JET_bitColumnMaybeNull</span><span class="sxs-lookup"><span data-stu-id="d3075-184">JET_bitColumnMaybeNull</span></span></p></td>
<td><p><span data-ttu-id="d3075-185">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d3075-185">Reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3075-186">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="d3075-186">JET_bitColumnFinalize</span></span></p></td>
<td><p><span data-ttu-id="d3075-187">Use JET_bitColumnDeleteOnZero en lugar de JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="d3075-187">Use JET_bitColumnDeleteOnZero instead of JET_bitColumnFinalize.</span></span> <span data-ttu-id="d3075-188">JET_bitColumnFinalize que se puede finalizar una columna.</span><span class="sxs-lookup"><span data-stu-id="d3075-188">JET_bitColumnFinalize that a column can be finalized.</span></span> <span data-ttu-id="d3075-189">Cuando una columna que se puede finalizar tiene una columna de actualización de custodia que llega a cero, se eliminará la fila.</span><span class="sxs-lookup"><span data-stu-id="d3075-189">When a column that can be finalized has an escrow update column that reaches zero, the row will be deleted.</span></span> <span data-ttu-id="d3075-190">En su lugar, las versiones futuras podrían invocar una función de devolución de llamada (para obtener más información, vea <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>).</span><span class="sxs-lookup"><span data-stu-id="d3075-190">Future versions might invoke a callback function instead (For more information, see <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>).</span></span> <span data-ttu-id="d3075-191">Una columna que se puede finalizar debe ser una columna de actualización de custodia.</span><span class="sxs-lookup"><span data-stu-id="d3075-191">A column that can be finalized must be an escrow update column.</span></span> <span data-ttu-id="d3075-192">No se puede usar JET_bitColumnFinalize con JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="d3075-192">JET_bitColumnFinalize cannot be used with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3075-193">JET_bitColumnUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="d3075-193">JET_bitColumnUserDefinedDefault</span></span></p></td>
<td><p><span data-ttu-id="d3075-194">La función de devolución de llamada proporcionará el valor predeterminado de una columna.</span><span class="sxs-lookup"><span data-stu-id="d3075-194">The default value for a column will be provided by a callback function.</span></span> <span data-ttu-id="d3075-195">Vea <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span><span class="sxs-lookup"><span data-stu-id="d3075-195">See <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span></span> <span data-ttu-id="d3075-196">Una columna que tiene un valor predeterminado definido por el usuario debe ser una columna etiquetada.</span><span class="sxs-lookup"><span data-stu-id="d3075-196">A column that has a user-defined default must be a tagged column.</span></span> <span data-ttu-id="d3075-197">Especificar JET_bitColumnUserDefinedDefault significa que <strong>pvDefault</strong> debe apuntar a una estructura de <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> y <strong>cbDefault</strong> debe establecerse en sizeof ( <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> ).</span><span class="sxs-lookup"><span data-stu-id="d3075-197">Specifying JET_bitColumnUserDefinedDefault means that <strong>pvDefault</strong> must point to a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure, and <strong>cbDefault</strong> must be set to sizeof( <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> ).</span></span></p>
<ul>
<li><p><span data-ttu-id="d3075-198">JET_bitColumnUserDefinedDefault no se pueden usar junto con JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero o JET_bitColumnMaybeNull.</span><span class="sxs-lookup"><span data-stu-id="d3075-198">JET_bitColumnUserDefinedDefault cannot be used in conjunction with JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero, or JET_bitColumnMaybeNull.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3075-199">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="d3075-199">JET_bitColumnDeleteOnZero</span></span></p></td>
<td><p><span data-ttu-id="d3075-200">La columna es una columna de actualización de custodia y, cuando llega a cero, se elimina el registro.</span><span class="sxs-lookup"><span data-stu-id="d3075-200">The column is an escrow update column, and when it reaches zero, the record will be deleted.</span></span> <span data-ttu-id="d3075-201">Un uso común de una columna que se puede finalizar es usarlo como un campo de recuento de referencias y cuando el campo llega a cero, se elimina el registro.</span><span class="sxs-lookup"><span data-stu-id="d3075-201">A common use for a column that can be finalized is to use it as a reference count field, and when the field reaches zero the record gets deleted.</span></span> <span data-ttu-id="d3075-202">JET_bitColumnDeleteOnZero está relacionado con JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="d3075-202">JET_bitColumnDeleteOnZero is related to JET_bitColumnFinalize.</span></span> <span data-ttu-id="d3075-203">Una columna de eliminación en cero debe ser una columna de actualización de custodia.</span><span class="sxs-lookup"><span data-stu-id="d3075-203">A Delete-on-zero column must be an escrow update column.</span></span> <span data-ttu-id="d3075-204">No se puede usar JET_bitColumnDeleteOnZero con JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="d3075-204">JET_bitColumnDeleteOnZero cannot be used with JET_bitColumnFinalize.</span></span> <span data-ttu-id="d3075-205">No se puede usar JET_bitColumnDeleteOnZero con columnas predeterminadas definidas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="d3075-205">JET_bitColumnDeleteOnZero cannot be used with user defined default columns.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="d3075-206">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3075-206">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d3075-207"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="d3075-207"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d3075-208">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="d3075-208">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3075-209"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d3075-209"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d3075-210">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d3075-210">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3075-211"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="d3075-211"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d3075-212">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="d3075-212">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="d3075-213">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d3075-213">See Also</span></span>

[<span data-ttu-id="d3075-214">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="d3075-214">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="d3075-215">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="d3075-215">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="d3075-216">JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="d3075-216">JET_COLUMNCREATE</span></span>](./jet-columncreate-structure.md)  
[<span data-ttu-id="d3075-217">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="d3075-217">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="d3075-218">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d3075-218">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d3075-219">JET_USERDEFINEDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="d3075-219">JET_USERDEFINEDDEFAULT</span></span>](./jet-userdefineddefault-structure.md)  
[<span data-ttu-id="d3075-220">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="d3075-220">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="d3075-221">JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="d3075-221">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)  
[<span data-ttu-id="d3075-222">JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="d3075-222">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)  
[<span data-ttu-id="d3075-223">JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="d3075-223">JetOpenTempTable</span></span>](./jetopentemptable-function.md)  
[<span data-ttu-id="d3075-224">JetOpenTempTable2</span><span class="sxs-lookup"><span data-stu-id="d3075-224">JetOpenTempTable2</span></span>](./jetopentemptable2-function.md)  
[<span data-ttu-id="d3075-225">JetOpenTempTable3</span><span class="sxs-lookup"><span data-stu-id="d3075-225">JetOpenTempTable3</span></span>](./jetopentemptable3-function.md)  
[<span data-ttu-id="d3075-226">JetRenameColumn</span><span class="sxs-lookup"><span data-stu-id="d3075-226">JetRenameColumn</span></span>](./jetrenamecolumn-function.md)
