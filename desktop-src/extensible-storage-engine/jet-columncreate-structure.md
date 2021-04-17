---
description: 'Más información acerca de: estructura de JET_COLUMNCREATE'
title: Estructura de JET_COLUMNCREATE
TOCTitle: JET_COLUMNCREATE Structure
ms:assetid: 553263a9-7d2c-4bd7-ad77-1dfb6d21ef2c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269252(v=EXCHG.10)
ms:contentKeyID: 32765554
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
ms.openlocfilehash: ee2d9d194a03cf575eb0296163526c1c50301cf4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697404"
---
# <a name="jet_columncreate-structure"></a><span data-ttu-id="ded7a-103">Estructura de JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="ded7a-103">JET_COLUMNCREATE Structure</span></span>


<span data-ttu-id="ded7a-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ded7a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columncreate-structure"></a><span data-ttu-id="ded7a-105">Estructura de JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="ded7a-105">JET_COLUMNCREATE Structure</span></span>

<span data-ttu-id="ded7a-106">La estructura **JET_COLUMNCREATE** describe una columna que se va a crear en una base de datos.</span><span class="sxs-lookup"><span data-stu-id="ded7a-106">The **JET_COLUMNCREATE** structure describes a column to create in a database.</span></span>

```cpp
    typedef struct tag_JET_COLUMNCREATE {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_COLTYP coltyp;
      unsigned long cbMax;
      JET_GRBIT grbit;
      void* pvDefault;
      unsigned long cbDefault;
      unsigned long cp;
      JET_COLUMNID columnid;
      JET_ERR err;
    } JET_COLUMNCREATE;
```

### <a name="members"></a><span data-ttu-id="ded7a-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ded7a-107">Members</span></span>

<span data-ttu-id="ded7a-108">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="ded7a-108">**cbStruct**</span></span>

<span data-ttu-id="ded7a-109">Tamaño de la estructura, en bytes.</span><span class="sxs-lookup"><span data-stu-id="ded7a-109">The size of the structure, in bytes.</span></span> <span data-ttu-id="ded7a-110">Este campo debe inicializarse en **sizeof (JET_COLUMNCREATE)**.</span><span class="sxs-lookup"><span data-stu-id="ded7a-110">This field must be initialized to **sizeof( JET_COLUMNCREATE )**.</span></span>

<span data-ttu-id="ded7a-111">**szColumnName**</span><span class="sxs-lookup"><span data-stu-id="ded7a-111">**szColumnName**</span></span>

<span data-ttu-id="ded7a-112">Nombre de la columna que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="ded7a-112">The name of the column to create.</span></span> <span data-ttu-id="ded7a-113">El nombre debe cumplir los siguientes criterios:</span><span class="sxs-lookup"><span data-stu-id="ded7a-113">The name must meet the following criteria:</span></span>

  - <span data-ttu-id="ded7a-114">Debe tener menos de JET_cbNameMost caracteres de longitud, sin incluir el carácter NULL de terminación.</span><span class="sxs-lookup"><span data-stu-id="ded7a-114">It must be fewer than JET_cbNameMost characters in length, not including the terminating NULL.</span></span>

<!-- end list -->

  - <span data-ttu-id="ded7a-115">Solo debe contener caracteres de los siguientes conjuntos: de 0 a 9, de la a a la Z, de la a a la z y de todos los demás signos de puntuación, salvo el signo de exclamación ( \! ), la coma (,), el corchete de apertura () y el \[ corchete de cierre ( \] ), es decir, los caracteres ASCII 0x20, de 0x22</span><span class="sxs-lookup"><span data-stu-id="ded7a-115">It must contain characters only from the following sets: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]), that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, 0x5d through 0x7f.</span></span>

<!-- end list -->

  - <span data-ttu-id="ded7a-116">No puede comenzar con un espacio.</span><span class="sxs-lookup"><span data-stu-id="ded7a-116">It cannot begin with a space.</span></span>

<!-- end list -->

  - <span data-ttu-id="ded7a-117">Debe contener al menos un carácter que no sea un espacio.</span><span class="sxs-lookup"><span data-stu-id="ded7a-117">It must contain at least one non-space character.</span></span>

<span data-ttu-id="ded7a-118">**coltyp**</span><span class="sxs-lookup"><span data-stu-id="ded7a-118">**coltyp**</span></span>

<span data-ttu-id="ded7a-119">El tipo de la columna (por ejemplo, texto, binario o numérico).</span><span class="sxs-lookup"><span data-stu-id="ded7a-119">The type of the column (for example, text, binary, or numerical).</span></span> <span data-ttu-id="ded7a-120">Para obtener más información, vea [JET_COLTYP](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="ded7a-120">For more information, see [JET_COLTYP](./jet-coltyp.md).</span></span>

<span data-ttu-id="ded7a-121">**cbMax**</span><span class="sxs-lookup"><span data-stu-id="ded7a-121">**cbMax**</span></span>

<span data-ttu-id="ded7a-122">La longitud máxima, en bytes, de una columna de longitud variable.</span><span class="sxs-lookup"><span data-stu-id="ded7a-122">The maximum length, in bytes, of a variable-length column.</span></span> <span data-ttu-id="ded7a-123">Longitud de la columna para las columnas de longitud fija.</span><span class="sxs-lookup"><span data-stu-id="ded7a-123">The length of the column for fixed-length columns.</span></span>

<span data-ttu-id="ded7a-124">**grbit**</span><span class="sxs-lookup"><span data-stu-id="ded7a-124">**grbit**</span></span>

<span data-ttu-id="ded7a-125">Grupo de bits que contiene las opciones de esta estructura y que incluye cero o más de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="ded7a-125">A group of bits that contain the options for this structure, and which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ded7a-126">Value</span><span class="sxs-lookup"><span data-stu-id="ded7a-126">Value</span></span></p></th>
<th><p><span data-ttu-id="ded7a-127">Significado</span><span class="sxs-lookup"><span data-stu-id="ded7a-127">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ded7a-128">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="ded7a-128">JET_bitColumnFixed</span></span></p></td>
<td><p><span data-ttu-id="ded7a-129">La columna es fija.</span><span class="sxs-lookup"><span data-stu-id="ded7a-129">The column is fixed.</span></span> <span data-ttu-id="ded7a-130">Siempre usará la misma cantidad de espacio en una fila, independientemente de la cantidad de datos que se estén almacenando en la columna.</span><span class="sxs-lookup"><span data-stu-id="ded7a-130">It will always use the same amount of space in a row, regardless of how much data is being stored in the column.</span></span> <span data-ttu-id="ded7a-131">No se puede usar JET_bitColumnFixed con JET_bitColumnTagged.</span><span class="sxs-lookup"><span data-stu-id="ded7a-131">JET_bitColumnFixed cannot be used with JET_bitColumnTagged.</span></span> <span data-ttu-id="ded7a-132">Este bit no se puede usar con valores Long como <strong>JET_coltypLongText</strong> y <strong>JET_coltypLongBinary</strong>.</span><span class="sxs-lookup"><span data-stu-id="ded7a-132">This bit cannot be used with long values such as <strong>JET_coltypLongText</strong> and <strong>JET_coltypLongBinary</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ded7a-133">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="ded7a-133">JET_bitColumnTagged</span></span></p></td>
<td><p><span data-ttu-id="ded7a-134">La columna está etiquetada.</span><span class="sxs-lookup"><span data-stu-id="ded7a-134">The column is tagged.</span></span> <span data-ttu-id="ded7a-135">Las columnas etiquetadas no ocupan espacio en la base de datos si no contienen datos.</span><span class="sxs-lookup"><span data-stu-id="ded7a-135">Tagged columns do not take up any space in the database if they do not contain data.</span></span> <span data-ttu-id="ded7a-136">Este bit no se puede usar con JET_bitColumnFixed.</span><span class="sxs-lookup"><span data-stu-id="ded7a-136">This bit cannot be used with JET_bitColumnFixed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ded7a-137">JET_bitColumnNotNULL</span><span class="sxs-lookup"><span data-stu-id="ded7a-137">JET_bitColumnNotNULL</span></span></p></td>
<td><p><span data-ttu-id="ded7a-138">La columna nunca se debe establecer en un valor NULL.</span><span class="sxs-lookup"><span data-stu-id="ded7a-138">The column must never be set to a NULL value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ded7a-139">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="ded7a-139">JET_bitColumnAutoincrement</span></span></p></td>
<td><p><span data-ttu-id="ded7a-140">La columna se incrementa automáticamente.</span><span class="sxs-lookup"><span data-stu-id="ded7a-140">The column is automatically incremented.</span></span> <span data-ttu-id="ded7a-141">El número es un número cada vez mayor y se garantiza que es único dentro de una tabla.</span><span class="sxs-lookup"><span data-stu-id="ded7a-141">The number is an increasing number, and is guaranteed to be unique within a table.</span></span> <span data-ttu-id="ded7a-142">Sin embargo, es posible que el número no sea continuo.</span><span class="sxs-lookup"><span data-stu-id="ded7a-142">The number, however, might not be continuous.</span></span> <span data-ttu-id="ded7a-143">Por ejemplo, si se insertan cinco filas en una tabla, la columna AutoIncrement puede contener los valores {1, 2, 6, 7, 8}.</span><span class="sxs-lookup"><span data-stu-id="ded7a-143">For example, if five rows are inserted into a table, the autoincrement column could contain the values { 1, 2, 6, 7, 8 }.</span></span></p>
<p><span data-ttu-id="ded7a-144"><strong>Windows 2000:  </strong> Este bit solo se puede usar en columnas de tipo <strong>JET_coltypLong</strong>.</span><span class="sxs-lookup"><span data-stu-id="ded7a-144"><strong>Windows 2000:  </strong>This bit can be used only on columns of type <strong>JET_coltypLong</strong>.</span></span></p>
<p><span data-ttu-id="ded7a-145"><strong>Windows Server 2003 y versiones posteriores:  </strong> Este bit solo se puede usar en columnas de tipo <strong>JET_coltypLong</strong> o <strong>JET_coltypCurrency</strong>.</span><span class="sxs-lookup"><span data-stu-id="ded7a-145"><strong>Windows Server 2003 and later:  </strong>This bit can only be used on columns of type <strong>JET_coltypLong</strong> or <strong>JET_coltypCurrency</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ded7a-146">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="ded7a-146">JET_bitColumnUpdatable</span></span></p></td>
<td><p><span data-ttu-id="ded7a-147">Este bit solo es válido en las llamadas a <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span><span class="sxs-lookup"><span data-stu-id="ded7a-147">This bit is valid only on calls to <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ded7a-148">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="ded7a-148">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="ded7a-149">Este bit solo es válido en las llamadas a <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span><span class="sxs-lookup"><span data-stu-id="ded7a-149">This bit is valid only on calls to <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ded7a-150">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="ded7a-150">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="ded7a-151">Este bit solo es válido en las llamadas a <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span><span class="sxs-lookup"><span data-stu-id="ded7a-151">This bit is valid only on calls to <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ded7a-152">JET_bitColumnMultiValued</span><span class="sxs-lookup"><span data-stu-id="ded7a-152">JET_bitColumnMultiValued</span></span></p></td>
<td><p><span data-ttu-id="ded7a-153">La columna puede tener varios valores.</span><span class="sxs-lookup"><span data-stu-id="ded7a-153">The column can be multi-valued.</span></span> <span data-ttu-id="ded7a-154">Una columna con varios valores puede tener cero, uno o más valores asociados.</span><span class="sxs-lookup"><span data-stu-id="ded7a-154">A multi-valued column can have zero, one, or more values associated with it.</span></span> <span data-ttu-id="ded7a-155">Los distintos valores de una columna con varios valores se identifican por el miembro <strong>itagSequence</strong> de varias estructuras, por ejemplo, <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a> <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span><span class="sxs-lookup"><span data-stu-id="ded7a-155">The various values in a multi-valued column are identified by the <strong>itagSequence</strong> member of various structures, for example, <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span></span> <span data-ttu-id="ded7a-156">Las columnas con varios valores deben ser columnas etiquetadas; es decir, no pueden ser columnas de longitud fija o de longitud variable.</span><span class="sxs-lookup"><span data-stu-id="ded7a-156">Multi-valued columns must be tagged columns; that is, they cannot be fixed-length or variable-length columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ded7a-157">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="ded7a-157">JET_bitColumnEscrowUpdate</span></span></p></td>
<td><p><span data-ttu-id="ded7a-158">La columna es una columna de actualización de custodia.</span><span class="sxs-lookup"><span data-stu-id="ded7a-158">The column is an escrow update column.</span></span> <span data-ttu-id="ded7a-159">Una columna de actualización de custodia se puede actualizar simultáneamente en diferentes sesiones con <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> y mantener la coherencia transaccional.</span><span class="sxs-lookup"><span data-stu-id="ded7a-159">An escrow update column can be updated concurrently by different sessions with <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> and maintain transactional consistency.</span></span></p>
<ul>
<li><p><span data-ttu-id="ded7a-160">Solo se puede crear una columna de actualización de custodia cuando la tabla está vacía.</span><span class="sxs-lookup"><span data-stu-id="ded7a-160">An escrow update column can be created only when the table is empty.</span></span></p></li>
<li><p><span data-ttu-id="ded7a-161">Una columna de actualización de custodia debe ser del tipo <strong>JET_coltypLong.</strong></span><span class="sxs-lookup"><span data-stu-id="ded7a-161">An escrow update column must be of type <strong>JET_coltypLong.</strong></span></span></p></li>
<li><p><span data-ttu-id="ded7a-162">Una columna de actualización de custodia debe tener un valor predeterminado (es decir, <strong>cbDefault</strong> debe ser positivo).</span><span class="sxs-lookup"><span data-stu-id="ded7a-162">An escrow update column must have a default value (that is <strong>cbDefault</strong> must be positive).</span></span></p></li>
<li><p><span data-ttu-id="ded7a-163">JET_bitColumnEscrowUpdate no se pueden usar junto con las constantes siguientes:</span><span class="sxs-lookup"><span data-stu-id="ded7a-163">JET_bitColumnEscrowUpdate cannot be used in conjunction with the following constants:</span></span></p>
<ul>
<li><p><span data-ttu-id="ded7a-164">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="ded7a-164">JET_bitColumnTagged</span></span></p></li>
<li><p><span data-ttu-id="ded7a-165">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="ded7a-165">JET_bitColumnVersion</span></span></p></li>
<li><p><span data-ttu-id="ded7a-166">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="ded7a-166">JET_bitColumnAutoincrement</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ded7a-167">JET_bitColumnUnversioned</span><span class="sxs-lookup"><span data-stu-id="ded7a-167">JET_bitColumnUnversioned</span></span></p></td>
<td><p><span data-ttu-id="ded7a-168">La columna se crea sin una versión.</span><span class="sxs-lookup"><span data-stu-id="ded7a-168">The column is created without a version.</span></span> <span data-ttu-id="ded7a-169">Se producirá un error en otras transacciones que intenten agregar una columna con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="ded7a-169">Other transactions attempting to add a column with the same name will fail.</span></span> <span data-ttu-id="ded7a-170">Este bit solo es útil con <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span><span class="sxs-lookup"><span data-stu-id="ded7a-170">This bit is only useful with <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span></span> <span data-ttu-id="ded7a-171">No se puede utilizar dentro de una transacción.</span><span class="sxs-lookup"><span data-stu-id="ded7a-171">It cannot be used within a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ded7a-172">JET_bitColumnMaybeNull</span><span class="sxs-lookup"><span data-stu-id="ded7a-172">JET_bitColumnMaybeNull</span></span></p></td>
<td><p><span data-ttu-id="ded7a-173">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="ded7a-173">Reserved for future use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ded7a-174">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="ded7a-174">JET_bitColumnFinalize</span></span></p></td>
<td><p><span data-ttu-id="ded7a-175">Use JET_bitColumnDeleteOnZero en lugar de JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="ded7a-175">Use JET_bitColumnDeleteOnZero instead of JET_bitColumnFinalize.</span></span> <span data-ttu-id="ded7a-176">JET_bitColumnFinalize especifica que una columna se puede finalizar.</span><span class="sxs-lookup"><span data-stu-id="ded7a-176">JET_bitColumnFinalize specifies that a column can be finalized.</span></span> <span data-ttu-id="ded7a-177">Cuando una columna que se puede finalizar tiene una columna de actualización de custodia que llega a cero, se eliminará la fila.</span><span class="sxs-lookup"><span data-stu-id="ded7a-177">When a column that can be finalized has an escrow update column that reaches zero, the row will be deleted.</span></span> <span data-ttu-id="ded7a-178">En su lugar, las versiones futuras pueden invocar una función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="ded7a-178">Future versions can invoke a callback function instead.</span></span> <span data-ttu-id="ded7a-179">Para obtener más información, vea <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span><span class="sxs-lookup"><span data-stu-id="ded7a-179">For more information, see <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span></span> <span data-ttu-id="ded7a-180">Una columna que se puede finalizar debe ser una columna de actualización de custodia.</span><span class="sxs-lookup"><span data-stu-id="ded7a-180">A column that can be finalized must be an escrow update column.</span></span> <span data-ttu-id="ded7a-181">No se puede usar JET_bitColumnFinalize con JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="ded7a-181">JET_bitColumnFinalize cannot be used with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ded7a-182">JET_bitColumnUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="ded7a-182">JET_bitColumnUserDefinedDefault</span></span></p></td>
<td><p><span data-ttu-id="ded7a-183">La función de devolución de llamada, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>, proporciona el valor predeterminado de una columna.</span><span class="sxs-lookup"><span data-stu-id="ded7a-183">The default value for a column is provided by the callback function, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span></span> <span data-ttu-id="ded7a-184">Una columna que tiene un valor predeterminado definido por el usuario debe ser una columna etiquetada.</span><span class="sxs-lookup"><span data-stu-id="ded7a-184">A column that has a user-defined default must be a tagged column.</span></span> <span data-ttu-id="ded7a-185"><strong>pvDefault</strong> debe apuntar a una estructura <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> y <strong>cbDefault</strong> debe establecerse en sizeof (<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</span><span class="sxs-lookup"><span data-stu-id="ded7a-185"><strong>pvDefault</strong> must point to a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure, and <strong>cbDefault</strong> must be set to sizeof(<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</span></span></p>
<p><span data-ttu-id="ded7a-186">JET_bitColumnUserDefinedDefault no se pueden usar junto con las constantes siguientes:</span><span class="sxs-lookup"><span data-stu-id="ded7a-186">JET_bitColumnUserDefinedDefault cannot be used in conjunction with the following constants:</span></span></p>
<ul>
<li><p><span data-ttu-id="ded7a-187">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="ded7a-187">JET_bitColumnFixed</span></span></p></li>
<li><p><span data-ttu-id="ded7a-188">JET_bitColumnNotNULL</span><span class="sxs-lookup"><span data-stu-id="ded7a-188">JET_bitColumnNotNULL</span></span></p></li>
<li><p><span data-ttu-id="ded7a-189">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="ded7a-189">JET_bitColumnVersion</span></span></p></li>
<li><p><span data-ttu-id="ded7a-190">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="ded7a-190">JET_bitColumnAutoincrement</span></span></p></li>
<li><p><span data-ttu-id="ded7a-191">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="ded7a-191">JET_bitColumnUpdatable</span></span></p></li>
<li><p><span data-ttu-id="ded7a-192">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="ded7a-192">JET_bitColumnEscrowUpdate</span></span></p></li>
<li><p><span data-ttu-id="ded7a-193">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="ded7a-193">JET_bitColumnFinalize</span></span></p></li>
<li><p><span data-ttu-id="ded7a-194">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="ded7a-194">JET_bitColumnDeleteOnZero</span></span></p></li>
<li><p><span data-ttu-id="ded7a-195">JET_bitColumnMaybeNull</span><span class="sxs-lookup"><span data-stu-id="ded7a-195">JET_bitColumnMaybeNull</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ded7a-196">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="ded7a-196">JET_bitColumnDeleteOnZero</span></span></p></td>
<td><p><span data-ttu-id="ded7a-197">La columna es una columna de actualización de custodia y, cuando llega a cero, se elimina el registro.</span><span class="sxs-lookup"><span data-stu-id="ded7a-197">The column is an escrow update column, and when it reaches zero, the record will be deleted.</span></span> <span data-ttu-id="ded7a-198">Un uso común de una columna que se puede finalizar es usarlo como un campo de recuento de referencias y cuando el campo llega a cero, se elimina el registro.</span><span class="sxs-lookup"><span data-stu-id="ded7a-198">A common use for a column that can be finalized is to use it as a reference count field, and when the field reaches zero the record gets deleted.</span></span> <span data-ttu-id="ded7a-199">JET_bitColumnDeleteOnZero está relacionado con JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="ded7a-199">JET_bitColumnDeleteOnZero is related to JET_bitColumnFinalize.</span></span> <span data-ttu-id="ded7a-200">Una columna de eliminación en cero debe ser una columna de actualización de custodia.</span><span class="sxs-lookup"><span data-stu-id="ded7a-200">A delete-on-zero column must be an escrow update column.</span></span> <span data-ttu-id="ded7a-201">No se puede usar JET_bitColumnDeleteOnZero con JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="ded7a-201">JET_bitColumnDeleteOnZero cannot be used with JET_bitColumnFinalize.</span></span> <span data-ttu-id="ded7a-202">No se puede usar JET_bitColumnDeleteOnZero con columnas predeterminadas definidas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="ded7a-202">JET_bitColumnDeleteOnZero cannot be used with user defined default columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ded7a-203">**pvDefault**</span><span class="sxs-lookup"><span data-stu-id="ded7a-203">**pvDefault**</span></span>

<span data-ttu-id="ded7a-204">Apunta a un búfer que será el valor predeterminado de una columna.</span><span class="sxs-lookup"><span data-stu-id="ded7a-204">Points to a buffer which will be the default value for a column.</span></span> <span data-ttu-id="ded7a-205">La longitud del búfer es **cbDefault**.</span><span class="sxs-lookup"><span data-stu-id="ded7a-205">The length of the buffer is **cbDefault**.</span></span> <span data-ttu-id="ded7a-206">Si no hay ningún valor predeterminado, **pvDefault** debe establecerse en NULL y **cbDefault** debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="ded7a-206">If there is no default, **pvDefault** should be set to NULL and **cbDefault** should be set to zero.</span></span> <span data-ttu-id="ded7a-207">Si *grbit* ha establecido JET_bitColumnUserDefinedDefault, **pvDefault** se interpretará como un puntero a una estructura de JET_USERDEFINEDDEFAULT.</span><span class="sxs-lookup"><span data-stu-id="ded7a-207">If *grbit* has JET_bitColumnUserDefinedDefault set, **pvDefault** will be interpreted as a pointer to a JET_USERDEFINEDDEFAULT structure.</span></span> <span data-ttu-id="ded7a-208">Los valores predeterminados no pueden ser mayores de 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="ded7a-208">Default values cannot be larger than 255 bytes.</span></span> <span data-ttu-id="ded7a-209">Si un valor predeterminado es mayor que 255 bytes, se truncará silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="ded7a-209">If a default value is larger than 255 bytes, it will be silently truncated.</span></span>

<span data-ttu-id="ded7a-210">**cbDefault**</span><span class="sxs-lookup"><span data-stu-id="ded7a-210">**cbDefault**</span></span>

<span data-ttu-id="ded7a-211">Tamaño, en bytes, del búfer especificado por **pvDefault**.</span><span class="sxs-lookup"><span data-stu-id="ded7a-211">The size, in bytes, of the buffer specified by **pvDefault**.</span></span>

<span data-ttu-id="ded7a-212">**cp**</span><span class="sxs-lookup"><span data-stu-id="ded7a-212">**cp**</span></span>

<span data-ttu-id="ded7a-213">Página de códigos de la columna.</span><span class="sxs-lookup"><span data-stu-id="ded7a-213">The code page for the column.</span></span> <span data-ttu-id="ded7a-214">Los únicos valores válidos para las columnas de texto son inglés (1252) y Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="ded7a-214">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="ded7a-215">Un valor de cero significa que se usará el valor predeterminado (Inglés, 1252).</span><span class="sxs-lookup"><span data-stu-id="ded7a-215">A value of zero means the default will be used (English, 1252).</span></span> <span data-ttu-id="ded7a-216">Si la columna no es una columna de texto, la página de códigos se establece automáticamente en cero.</span><span class="sxs-lookup"><span data-stu-id="ded7a-216">If the column is not a text column, the code page automatically gets set to zero.</span></span>

<span data-ttu-id="ded7a-217">**columnid**</span><span class="sxs-lookup"><span data-stu-id="ded7a-217">**columnid**</span></span>

<span data-ttu-id="ded7a-218">Si se ejecuta correctamente, el identificador de columna de la columna recién creada se devolverá en este campo.</span><span class="sxs-lookup"><span data-stu-id="ded7a-218">On success, the column identifier of the newly-created column will be passed back in this field.</span></span> <span data-ttu-id="ded7a-219">En caso de error, el valor es indefinido.</span><span class="sxs-lookup"><span data-stu-id="ded7a-219">On failure, the value is undefined.</span></span>

<span data-ttu-id="ded7a-220">**ERR**</span><span class="sxs-lookup"><span data-stu-id="ded7a-220">**err**</span></span>

<span data-ttu-id="ded7a-221">El campo **Err** contendrá el estado de creación de esta columna.</span><span class="sxs-lookup"><span data-stu-id="ded7a-221">The **err** field will contain the status of creating this column.</span></span> <span data-ttu-id="ded7a-222">Consulte [JetAddColumn](./jetaddcolumn-function.md) para obtener una lista de los valores devueltos probables.</span><span class="sxs-lookup"><span data-stu-id="ded7a-222">See [JetAddColumn](./jetaddcolumn-function.md) for a list of likely return values.</span></span>

### <a name="requirements"></a><span data-ttu-id="ded7a-223">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ded7a-223">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ded7a-224"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="ded7a-224"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ded7a-225">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ded7a-225">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ded7a-226"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ded7a-226"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ded7a-227">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ded7a-227">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ded7a-228"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="ded7a-228"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ded7a-229">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="ded7a-229">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ded7a-230"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="ded7a-230"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="ded7a-231">Se implementa como <strong>JET_COLUMNCREATE_W</strong> (Unicode) y <strong>JET_COLUMNCREATE_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="ded7a-231">Implemented as <strong>JET_COLUMNCREATE_W</strong> (Unicode) and <strong>JET_COLUMNCREATE_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="ded7a-232">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ded7a-232">See Also</span></span>

[<span data-ttu-id="ded7a-233">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="ded7a-233">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="ded7a-234">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="ded7a-234">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="ded7a-235">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ded7a-235">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ded7a-236">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="ded7a-236">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="ded7a-237">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="ded7a-237">JET_RETINFO</span></span>](./jet-retinfo-structure.md)  
[<span data-ttu-id="ded7a-238">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="ded7a-238">JET_SETINFO</span></span>](./jet-setinfo-structure.md)  
[<span data-ttu-id="ded7a-239">JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="ded7a-239">JET_SETCOLUMN</span></span>](./jet-setcolumn-structure.md)  
[<span data-ttu-id="ded7a-240">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="ded7a-240">JET_RETRIEVECOLUMN</span></span>](./jet-retrievecolumn-structure.md)  
[<span data-ttu-id="ded7a-241">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="ded7a-241">JET_ENUMCOLUMNVALUE</span></span>](./jet-enumcolumnvalue-structure.md)  
[<span data-ttu-id="ded7a-242">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="ded7a-242">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="ded7a-243">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="ded7a-243">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="ded7a-244">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="ded7a-244">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="ded7a-245">JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="ded7a-245">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)  
[<span data-ttu-id="ded7a-246">JetRenameColumn</span><span class="sxs-lookup"><span data-stu-id="ded7a-246">JetRenameColumn</span></span>](./jetrenamecolumn-function.md)  
[<span data-ttu-id="ded7a-247">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="ded7a-247">JetSetColumns</span></span>](./jetsetcolumns-function.md)
