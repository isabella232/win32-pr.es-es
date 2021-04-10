---
description: 'Más información acerca de: estructura de JET_TABLECREATE'
title: Estructura de JET_TABLECREATE
TOCTitle: JET_TABLECREATE Structure
ms:assetid: ff06325c-d61e-4239-b2d4-868f557f5f76
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294146(v=EXCHG.10)
ms:contentKeyID: 32765760
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
ms.openlocfilehash: f96b73daaf446023a7fe3a5729dcb1c90b5f14e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153779"
---
# <a name="jet_tablecreate-structure"></a><span data-ttu-id="098f3-103">Estructura de JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="098f3-103">JET_TABLECREATE Structure</span></span>


<span data-ttu-id="098f3-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="098f3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_tablecreate-structure"></a><span data-ttu-id="098f3-105">Estructura de JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="098f3-105">JET_TABLECREATE Structure</span></span>

<span data-ttu-id="098f3-106">La estructura **JET_TABLECREATE** contiene la información necesaria para crear una tabla rellenada con columnas e índices en una base de datos ese.</span><span class="sxs-lookup"><span data-stu-id="098f3-106">The **JET_TABLECREATE** structure contains the information that is necessary to create a table populated with columns and indexes in an ESE database.</span></span> <span data-ttu-id="098f3-107">[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) utiliza la estructura de **JET_TABLECREATE**</span><span class="sxs-lookup"><span data-stu-id="098f3-107">The **JET_TABLECREATE** structure is used by [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)</span></span>

```cpp
    typedef struct tagJET_TABLECREATE {
      unsigned long cbStruct;
      tchar* szTableName;
      tchar* szTemplateTableName;
      unsigned long ulPages;
      unsigned long ulDensity;
      JET_COLUMNCREATE* rgcolumncreate;
      unsigned long cColumns;
      JET_INDEXCREATE* rgindexcreate;
      unsigned long cIndexes;
      JET_GRBIT grbit;
      JET_TABLEID tableid;
      unsigned long cCreated;
    } JET_TABLECREATE;
```

### <a name="members"></a><span data-ttu-id="098f3-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="098f3-108">Members</span></span>

<span data-ttu-id="098f3-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="098f3-109">**cbStruct**</span></span>

<span data-ttu-id="098f3-110">Tamaño de esta estructura en bytes (para una futura ampliación).</span><span class="sxs-lookup"><span data-stu-id="098f3-110">The size of this structure in bytes (for future expansion).</span></span> <span data-ttu-id="098f3-111">Debe establecerse en sizeof (JET_TABLECREATE) en bytes.</span><span class="sxs-lookup"><span data-stu-id="098f3-111">It must be set to sizeof( JET_TABLECREATE ) in bytes.</span></span>

<span data-ttu-id="098f3-112">**szTableName**</span><span class="sxs-lookup"><span data-stu-id="098f3-112">**szTableName**</span></span>

<span data-ttu-id="098f3-113">El objeto de la tabla que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="098f3-113">The name of the table to create.</span></span>

<span data-ttu-id="098f3-114">El nombre debe cumplir las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="098f3-114">The name must use meet the following conditions:</span></span>

  - <span data-ttu-id="098f3-115">Tener un valor inferior a JET_cbNameMost, sin incluir el carácter NULL de terminación.</span><span class="sxs-lookup"><span data-stu-id="098f3-115">Have a value less than JET_cbNameMost, not including the terminating NULL.</span></span>

<!-- end list -->

  - <span data-ttu-id="098f3-116">Consta del siguiente conjunto de caracteres: de 0 a 9, de la a a la Z, de la a a la z, y todos los demás signos de puntuación, excepto el signo de exclamación ( \! ), la coma (,), el corchete de apertura () y el \[ corchete de cierre ( \] ), es decir, caracteres ASCII 0x20, de 0x22 a 0x2d,</span><span class="sxs-lookup"><span data-stu-id="098f3-116">Consist of the following set of characters: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]), that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

<!-- end list -->

  - <span data-ttu-id="098f3-117">No comienza con un espacio.</span><span class="sxs-lookup"><span data-stu-id="098f3-117">Not begin with a space.</span></span>

<!-- end list -->

  - <span data-ttu-id="098f3-118">Consta de al menos un carácter que no sea un espacio.</span><span class="sxs-lookup"><span data-stu-id="098f3-118">Consist of at least one non-space character.</span></span>

<span data-ttu-id="098f3-119">**szTemplateTableName**</span><span class="sxs-lookup"><span data-stu-id="098f3-119">**szTemplateTableName**</span></span>

<span data-ttu-id="098f3-120">Nombre de una tabla ya existente de la que se va a heredar el DDL base (lenguaje de definición de datos).</span><span class="sxs-lookup"><span data-stu-id="098f3-120">The name of an already-existing table from which to inherit base DDL (Data Definition Language).</span></span> <span data-ttu-id="098f3-121">El uso de una tabla de plantilla permite la creación sencilla de muchas tablas con columnas e índices idénticos.</span><span class="sxs-lookup"><span data-stu-id="098f3-121">Use of a template table allows for the easy creation of many tables with identical columns and indexes.</span></span>

<span data-ttu-id="098f3-122">**ulPages**</span><span class="sxs-lookup"><span data-stu-id="098f3-122">**ulPages**</span></span>

<span data-ttu-id="098f3-123">Número inicial de páginas de base de datos que se van a asignar a la tabla.</span><span class="sxs-lookup"><span data-stu-id="098f3-123">The initial number of database pages to allocate for the table.</span></span> <span data-ttu-id="098f3-124">Si se especifica un número mayor que uno, se puede reducir la fragmentación si se insertan muchas filas en esta tabla.</span><span class="sxs-lookup"><span data-stu-id="098f3-124">Specifying a number larger than one can reduce fragmentation if many rows are inserted into this table.</span></span>

<span data-ttu-id="098f3-125">**ulDensity**</span><span class="sxs-lookup"><span data-stu-id="098f3-125">**ulDensity**</span></span>

<span data-ttu-id="098f3-126">Densidad de la tabla, en puntos porcentuales.</span><span class="sxs-lookup"><span data-stu-id="098f3-126">The table density, in percentage points.</span></span> <span data-ttu-id="098f3-127">El número debe ser 0 o estar comprendido entre 20 y 100.</span><span class="sxs-lookup"><span data-stu-id="098f3-127">The number must be either 0 or in the range of 20 through 100.</span></span> <span data-ttu-id="098f3-128">Pasar 0 significa que se debe usar el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="098f3-128">Passing 0 means that the default value should be used.</span></span> <span data-ttu-id="098f3-129">El valor predeterminado es 80.</span><span class="sxs-lookup"><span data-stu-id="098f3-129">The default is 80.</span></span>

<span data-ttu-id="098f3-130">**rgcolumncreate**</span><span class="sxs-lookup"><span data-stu-id="098f3-130">**rgcolumncreate**</span></span>

<span data-ttu-id="098f3-131">Matriz de estructuras de [JET_COLUMNCREATE](./jet-columncreate-structure.md) , cada una de las cuales corresponde a una columna que se va a crear en la nueva tabla.</span><span class="sxs-lookup"><span data-stu-id="098f3-131">An array of [JET_COLUMNCREATE](./jet-columncreate-structure.md) structures, each of which corresponds to a column to be created in the new table.</span></span>

<span data-ttu-id="098f3-132">**cColumns**</span><span class="sxs-lookup"><span data-stu-id="098f3-132">**cColumns**</span></span>

<span data-ttu-id="098f3-133">El número de elementos [JET_COLUMNCREATE](./jet-columncreate-structure.md) en **rgcolumncreate**.</span><span class="sxs-lookup"><span data-stu-id="098f3-133">The number of [JET_COLUMNCREATE](./jet-columncreate-structure.md) elements in **rgcolumncreate**.</span></span>

<span data-ttu-id="098f3-134">**rgindexcreate**</span><span class="sxs-lookup"><span data-stu-id="098f3-134">**rgindexcreate**</span></span>

<span data-ttu-id="098f3-135">Matriz de estructuras de [JET_INDEXCREATE](./jet-indexcreate-structure.md) , cada una de las cuales corresponde a un índice que se va a crear en la nueva tabla.</span><span class="sxs-lookup"><span data-stu-id="098f3-135">An array of [JET_INDEXCREATE](./jet-indexcreate-structure.md) structures, each of which corresponds to an index to be created in the new table.</span></span>

<span data-ttu-id="098f3-136">**cIndexes**</span><span class="sxs-lookup"><span data-stu-id="098f3-136">**cIndexes**</span></span>

<span data-ttu-id="098f3-137">El número de elementos [JET_INDEXCREATE](./jet-indexcreate-structure.md) en **rgindexcreate**.</span><span class="sxs-lookup"><span data-stu-id="098f3-137">The number of [JET_INDEXCREATE](./jet-indexcreate-structure.md) elements in **rgindexcreate**.</span></span>

<span data-ttu-id="098f3-138">**grbit**</span><span class="sxs-lookup"><span data-stu-id="098f3-138">**grbit**</span></span>

<span data-ttu-id="098f3-139">Grupo de bits que contiene las opciones de esta llamada, que incluyen cero o más de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="098f3-139">A group of bits that contain the options for this call, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="098f3-140">Value</span><span class="sxs-lookup"><span data-stu-id="098f3-140">Value</span></span></p></th>
<th><p><span data-ttu-id="098f3-141">Significado</span><span class="sxs-lookup"><span data-stu-id="098f3-141">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="098f3-142">JET_bitTableCreateFixedDDL</span><span class="sxs-lookup"><span data-stu-id="098f3-142">JET_bitTableCreateFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="098f3-143">La configuración de JET_bitTableCreateFixedDDL impide las operaciones DDL en la tabla (por ejemplo, agregar o quitar columnas).</span><span class="sxs-lookup"><span data-stu-id="098f3-143">Setting JET_bitTableCreateFixedDDL prevents DDL operations on the table (such as adding or removing columns).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="098f3-144">JET_bitTableCreateTemplateTable</span><span class="sxs-lookup"><span data-stu-id="098f3-144">JET_bitTableCreateTemplateTable</span></span></p></td>
<td><p><span data-ttu-id="098f3-145">La configuración de JET_bitTableCreateTemplateTable hace que la tabla sea una tabla de plantilla.</span><span class="sxs-lookup"><span data-stu-id="098f3-145">Setting JET_bitTableCreateTemplateTable causes the table to be a template table.</span></span> <span data-ttu-id="098f3-146">Las nuevas tablas pueden especificar el nombre de esta tabla como su tabla de plantilla.</span><span class="sxs-lookup"><span data-stu-id="098f3-146">New tables can then specify the name of this table as their template table.</span></span> <span data-ttu-id="098f3-147">La configuración de JET_bitTableCreateTemplateTable implica JET_bitTableCreateFixedDDL.</span><span class="sxs-lookup"><span data-stu-id="098f3-147">Setting JET_bitTableCreateTemplateTable implies JET_bitTableCreateFixedDDL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="098f3-148">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="098f3-148">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span></span></p></td>
<td><p><span data-ttu-id="098f3-149">Desusado.</span><span class="sxs-lookup"><span data-stu-id="098f3-149">Deprecated.</span></span> <span data-ttu-id="098f3-150">No utilizar.</span><span class="sxs-lookup"><span data-stu-id="098f3-150">Do not use.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="098f3-151">**TABLEID**</span><span class="sxs-lookup"><span data-stu-id="098f3-151">**tableid**</span></span>

<span data-ttu-id="098f3-152">Un campo de salida que contiene el [JET_TABLEID](./jet-tableid.md) de la nueva tabla si la llamada a la API se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="098f3-152">An output field that holds the [JET_TABLEID](./jet-tableid.md) of the new table if the API call succeeds.</span></span> <span data-ttu-id="098f3-153">Si se produce un error en la llamada API, el valor es indefinido.</span><span class="sxs-lookup"><span data-stu-id="098f3-153">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="098f3-154">**Creado**</span><span class="sxs-lookup"><span data-stu-id="098f3-154">**cCreated**</span></span>

<span data-ttu-id="098f3-155">Un campo de salida que contiene el recuento de objetos creados si la llamada de API se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="098f3-155">An output field that contains the count of objects created if the API call succeeds.</span></span> <span data-ttu-id="098f3-156">Si se produce un error en la llamada API, el valor es indefinido.</span><span class="sxs-lookup"><span data-stu-id="098f3-156">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="098f3-157">El recuento de objetos que se crean es igual a la suma de las columnas, las tablas y los índices que se han creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="098f3-157">The count of objects that are created is equal to the sum of columns, tables, and indexes that are successfully created.</span></span>

### <a name="requirements"></a><span data-ttu-id="098f3-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="098f3-158">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="098f3-159"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="098f3-159"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="098f3-160">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="098f3-160">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="098f3-161"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="098f3-161"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="098f3-162">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="098f3-162">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="098f3-163"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="098f3-163"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="098f3-164">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="098f3-164">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="098f3-165"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="098f3-165"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="098f3-166">Se implementa como <strong>JET_TABLECREATE_W</strong> (Unicode) y <strong>JET_TABLECREATE_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="098f3-166">Implemented as <strong>JET_TABLECREATE_W</strong> (Unicode) and <strong>JET_TABLECREATE_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="098f3-167">Consulte también</span><span class="sxs-lookup"><span data-stu-id="098f3-167">See Also</span></span>

[<span data-ttu-id="098f3-168">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="098f3-168">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="098f3-169">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="098f3-169">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="098f3-170">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="098f3-170">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="098f3-171">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="098f3-171">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="098f3-172">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="098f3-172">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="098f3-173">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="098f3-173">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="098f3-174">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="098f3-174">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="098f3-175">JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="098f3-175">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="098f3-176">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="098f3-176">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="098f3-177">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="098f3-177">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
