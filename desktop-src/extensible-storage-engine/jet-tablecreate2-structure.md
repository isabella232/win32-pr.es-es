---
description: 'Más información acerca de: estructura de JET_TABLECREATE2'
title: Estructura de JET_TABLECREATE2
TOCTitle: JET_TABLECREATE2 Structure
ms:assetid: 2029e684-0d10-44e7-8033-d9cdbdffd7a4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269203(v=EXCHG.10)
ms:contentKeyID: 32765506
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
ms.openlocfilehash: d7ce983d393954c0d82f0d4e43108ff845d31571
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913754"
---
# <a name="jet_tablecreate2-structure"></a><span data-ttu-id="2324f-103">Estructura de JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="2324f-103">JET_TABLECREATE2 Structure</span></span>


<span data-ttu-id="2324f-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2324f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_tablecreate2-structure"></a><span data-ttu-id="2324f-105">Estructura de JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="2324f-105">JET_TABLECREATE2 Structure</span></span>

<span data-ttu-id="2324f-106">La estructura **JET_TABLECREATE2** contiene la información necesaria para crear una tabla rellenada con columnas e índices en una base de datos ese y que designa una función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="2324f-106">The **JET_TABLECREATE2** structure contains the information that is needed to create a table populated with columns and indexes in an ESE database, and that designates a callback function.</span></span> <span data-ttu-id="2324f-107">[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)utiliza la estructura de **JET_TABLECREATE2** .</span><span class="sxs-lookup"><span data-stu-id="2324f-107">The **JET_TABLECREATE2** structure is used by [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md).</span></span>

<span data-ttu-id="2324f-108">**Windows XP:** La estructura de **JET_TABLECREATE2** se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2324f-108">**Windows XP:** The **JET_TABLECREATE2** structure is introduced in Windows XP.</span></span>

```cpp
    typedef struct tagJET_TABLECREATE2 {
      unsigned long cbStruct;
      tchar* szTableName;
      tchar* szTemplateTableName;
      unsigned long ulPages;
      unsigned long ulDensity;
      JET_COLUMNCREATE* rgcolumncreate;
      unsigned long cColumns;
      JET_INDEXCREATE* rgindexcreate;
      unsigned long cIndexes;
      tchar* szCallback;
      JET_CBTYP cbtyp;
      JET_GRBIT grbit;
      JET_TABLEID tableid;
      unsigned long cCreated;
    } JET_TABLECREATE2;
```

### <a name="members"></a><span data-ttu-id="2324f-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="2324f-109">Members</span></span>

<span data-ttu-id="2324f-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="2324f-110">**cbStruct**</span></span>

<span data-ttu-id="2324f-111">Tamaño de esta estructura en bytes (para una futura ampliación).</span><span class="sxs-lookup"><span data-stu-id="2324f-111">The size of this structure in bytes (for future expansion).</span></span> <span data-ttu-id="2324f-112">Debe establecerse en sizeof (JET_TABLECREATE2) en bytes.</span><span class="sxs-lookup"><span data-stu-id="2324f-112">It must be set to sizeof( JET_TABLECREATE2 ) in bytes.</span></span>

<span data-ttu-id="2324f-113">**szTableName**</span><span class="sxs-lookup"><span data-stu-id="2324f-113">**szTableName**</span></span>

<span data-ttu-id="2324f-114">Nombre de la tabla que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="2324f-114">The name of table to create.</span></span>

<span data-ttu-id="2324f-115">El nombre debe cumplir las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="2324f-115">The name must use meet the following conditions:</span></span>

  - <span data-ttu-id="2324f-116">Tener un valor inferior a JET_cbNameMost, sin incluir el carácter NULL de terminación.</span><span class="sxs-lookup"><span data-stu-id="2324f-116">Have a value less than JET_cbNameMost, not including the terminating NULL.</span></span>

<!-- end list -->

  - <span data-ttu-id="2324f-117">Consta del siguiente conjunto de caracteres: de 0 a 9, de la a a la Z, de la a a la z, y todos los demás signos de puntuación, excepto el signo de exclamación ( \! ), la coma (,), el corchete de apertura () y el \[ corchete de cierre ( \] ), es decir, caracteres ASCII 0x20, de 0x22 a 0x2d,</span><span class="sxs-lookup"><span data-stu-id="2324f-117">Consist of the following set of characters: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]), that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

<!-- end list -->

  - <span data-ttu-id="2324f-118">No comienza con un espacio.</span><span class="sxs-lookup"><span data-stu-id="2324f-118">Not begin with a space.</span></span>

<!-- end list -->

  - <span data-ttu-id="2324f-119">Consta de al menos un carácter que no sea un espacio.</span><span class="sxs-lookup"><span data-stu-id="2324f-119">Consist of at least one non-space character.</span></span>

<span data-ttu-id="2324f-120">**szTemplateTableName**</span><span class="sxs-lookup"><span data-stu-id="2324f-120">**szTemplateTableName**</span></span>

<span data-ttu-id="2324f-121">Nombre de una tabla ya existente de la que se va a heredar el DDL base (lenguaje de definición de datos).</span><span class="sxs-lookup"><span data-stu-id="2324f-121">The name of an already-existing table from which to inherit base DDL (Data Definition Language).</span></span> <span data-ttu-id="2324f-122">El uso de una tabla de plantilla permite crear fácilmente muchas tablas con columnas e índices idénticos.</span><span class="sxs-lookup"><span data-stu-id="2324f-122">Using a template table allows easy creation of many tables with identical columns and indexes.</span></span>

<span data-ttu-id="2324f-123">**ulPages**</span><span class="sxs-lookup"><span data-stu-id="2324f-123">**ulPages**</span></span>

<span data-ttu-id="2324f-124">Número inicial de páginas de base de datos que se van a asignar a la tabla.</span><span class="sxs-lookup"><span data-stu-id="2324f-124">The initial number of database pages to allocate for the table.</span></span> <span data-ttu-id="2324f-125">Si se especifica un número mayor que uno, se puede reducir la fragmentación si se insertan muchas filas en esta tabla.</span><span class="sxs-lookup"><span data-stu-id="2324f-125">Specifying a number larger than one can reduce fragmentation if many rows are inserted into this table.</span></span>

<span data-ttu-id="2324f-126">**ulDensity**</span><span class="sxs-lookup"><span data-stu-id="2324f-126">**ulDensity**</span></span>

<span data-ttu-id="2324f-127">Densidad de la tabla, en puntos porcentuales.</span><span class="sxs-lookup"><span data-stu-id="2324f-127">The table density, in percentage points.</span></span> <span data-ttu-id="2324f-128">El número debe ser 0 o estar comprendido entre 20 y 100.</span><span class="sxs-lookup"><span data-stu-id="2324f-128">The number must be either 0 or in the range of 20 through 100.</span></span> <span data-ttu-id="2324f-129">Pasar 0 significa que se debe usar el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2324f-129">Passing 0 means that the default value should be used.</span></span> <span data-ttu-id="2324f-130">El valor predeterminado es 80.</span><span class="sxs-lookup"><span data-stu-id="2324f-130">The default is 80.</span></span>

<span data-ttu-id="2324f-131">**rgcolumncreate**</span><span class="sxs-lookup"><span data-stu-id="2324f-131">**rgcolumncreate**</span></span>

<span data-ttu-id="2324f-132">Matriz de estructuras de [JET_COLUMNCREATE](./jet-columncreate-structure.md) , cada una de las cuales corresponde a una columna que se va a crear en la nueva tabla.</span><span class="sxs-lookup"><span data-stu-id="2324f-132">An array of [JET_COLUMNCREATE](./jet-columncreate-structure.md) structures, each of which corresponds to a column to be created in the new table.</span></span>

<span data-ttu-id="2324f-133">**cColumns**</span><span class="sxs-lookup"><span data-stu-id="2324f-133">**cColumns**</span></span>

<span data-ttu-id="2324f-134">el número de elementos [JET_COLUMNCREATE](./jet-columncreate-structure.md) en **rgcolumncreate**.</span><span class="sxs-lookup"><span data-stu-id="2324f-134">the number of [JET_COLUMNCREATE](./jet-columncreate-structure.md) elements in **rgcolumncreate**.</span></span>

<span data-ttu-id="2324f-135">**rgindexcreate**</span><span class="sxs-lookup"><span data-stu-id="2324f-135">**rgindexcreate**</span></span>

<span data-ttu-id="2324f-136">Matriz de estructuras de [JET_INDEXCREATE](./jet-indexcreate-structure.md) , cada una de las cuales corresponde a un índice que se va a crear en la nueva tabla.</span><span class="sxs-lookup"><span data-stu-id="2324f-136">An array of [JET_INDEXCREATE](./jet-indexcreate-structure.md) structures, each of which corresponds to an index to be created in the new table.</span></span>

<span data-ttu-id="2324f-137">**cIndexes**</span><span class="sxs-lookup"><span data-stu-id="2324f-137">**cIndexes**</span></span>

<span data-ttu-id="2324f-138">El número de elementos [JET_INDEXCREATE](./jet-indexcreate-structure.md) en **rgindexcreate**.</span><span class="sxs-lookup"><span data-stu-id="2324f-138">The number of [JET_INDEXCREATE](./jet-indexcreate-structure.md) elements in **rgindexcreate**.</span></span>

<span data-ttu-id="2324f-139">**szCallback**</span><span class="sxs-lookup"><span data-stu-id="2324f-139">**szCallback**</span></span>

<span data-ttu-id="2324f-140">Función a la que se llama durante ciertos eventos.</span><span class="sxs-lookup"><span data-stu-id="2324f-140">The function that gets called during certain events.</span></span> <span data-ttu-id="2324f-141">**cbtyp** determina cuándo se llamará a la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="2324f-141">**cbtyp** determines when the callback function will be called.</span></span>

<span data-ttu-id="2324f-142">El formato de **szCallback** debe ser "función de módulo \! ", por ejemplo, "alpha \! beta" hace referencia a la función beta del módulo denominado "Alpha".</span><span class="sxs-lookup"><span data-stu-id="2324f-142">The format of **szCallback** must be "module\!function"—for example, "alpha\!beta" refers to the beta function in the module named "alpha".</span></span> <span data-ttu-id="2324f-143">El prototipo de la función debe coincidir con [JET_CALLBACK](./jet-callback-callback-function.md).</span><span class="sxs-lookup"><span data-stu-id="2324f-143">The prototype of the function must match [JET_CALLBACK](./jet-callback-callback-function.md).</span></span> <span data-ttu-id="2324f-144">Para obtener más información, vea [JET_CALLBACK](./jet-callback-callback-function.md).</span><span class="sxs-lookup"><span data-stu-id="2324f-144">For more information, see [JET_CALLBACK](./jet-callback-callback-function.md).</span></span>

<span data-ttu-id="2324f-145">**cbtyp**</span><span class="sxs-lookup"><span data-stu-id="2324f-145">**cbtyp**</span></span>

<span data-ttu-id="2324f-146">Describe el tipo de función de devolución de llamada designado por **szCallback**.</span><span class="sxs-lookup"><span data-stu-id="2324f-146">Describes the type of callback function designated by **szCallback**.</span></span> <span data-ttu-id="2324f-147">Para obtener más información, vea [JET_CBTYP](./jet-cbtyp.md).</span><span class="sxs-lookup"><span data-stu-id="2324f-147">For more information, see [JET_CBTYP](./jet-cbtyp.md).</span></span> <span data-ttu-id="2324f-148">Este campo de bits se compone de uno o varios de los bits siguientes.</span><span class="sxs-lookup"><span data-stu-id="2324f-148">This bitfield is composed of one or more of the following bits.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2324f-149">Value</span><span class="sxs-lookup"><span data-stu-id="2324f-149">Value</span></span></p></th>
<th><p><span data-ttu-id="2324f-150">Significado</span><span class="sxs-lookup"><span data-stu-id="2324f-150">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2324f-151">JET_cbtypFinalize</span><span class="sxs-lookup"><span data-stu-id="2324f-151">JET_cbtypFinalize</span></span></p></td>
<td><p><span data-ttu-id="2324f-152">Se llamará a la función de devolución de llamada cuando una columna que se pueda finalizar haya pasado a cero.</span><span class="sxs-lookup"><span data-stu-id="2324f-152">The callback function will be called when a column that can be finalized has gone to zero.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2324f-153">JET_cbtypBeforeInsert</span><span class="sxs-lookup"><span data-stu-id="2324f-153">JET_cbtypBeforeInsert</span></span></p></td>
<td><p><span data-ttu-id="2324f-154">Se llamará a la función de devolución de llamada antes de la inserción del registro.</span><span class="sxs-lookup"><span data-stu-id="2324f-154">The callback function will be called prior to record insertion.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2324f-155">JET_cbtypAfterInsert</span><span class="sxs-lookup"><span data-stu-id="2324f-155">JET_cbtypAfterInsert</span></span></p></td>
<td><p><span data-ttu-id="2324f-156">Se llamará a la función de devolución de llamada una vez que el motor de base de datos haya terminado de insertar un registro.</span><span class="sxs-lookup"><span data-stu-id="2324f-156">The callback function will be called once the database engine has finished inserting a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2324f-157">JET_cbtypBeforeReplace</span><span class="sxs-lookup"><span data-stu-id="2324f-157">JET_cbtypBeforeReplace</span></span></p></td>
<td><p><span data-ttu-id="2324f-158">Se llamará a la función de devolución de llamada antes de modificar un registro.</span><span class="sxs-lookup"><span data-stu-id="2324f-158">The callback function will be called prior to modification of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2324f-159">JET_cbtypAfterReplace</span><span class="sxs-lookup"><span data-stu-id="2324f-159">JET_cbtypAfterReplace</span></span></p></td>
<td><p><span data-ttu-id="2324f-160">Se llamará a la función de devolución de llamada después de finalizar la modificación de un registro.</span><span class="sxs-lookup"><span data-stu-id="2324f-160">The callback function will be called after finishing modification of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2324f-161">JET_cbtypBeforeDelete</span><span class="sxs-lookup"><span data-stu-id="2324f-161">JET_cbtypBeforeDelete</span></span></p></td>
<td><p><span data-ttu-id="2324f-162">Se llamará a la función de devolución de llamada antes de eliminar un registro.</span><span class="sxs-lookup"><span data-stu-id="2324f-162">The callback function will be called prior to deletion of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2324f-163">JET_cbtypAfterDelete</span><span class="sxs-lookup"><span data-stu-id="2324f-163">JET_cbtypAfterDelete</span></span></p></td>
<td><p><span data-ttu-id="2324f-164">Se llamará a la función de devolución de llamada después de que se haya eliminado un registro.</span><span class="sxs-lookup"><span data-stu-id="2324f-164">The callback function will be called after a record has been deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2324f-165">JET_cbtypUserDefinedDefaultValue</span><span class="sxs-lookup"><span data-stu-id="2324f-165">JET_cbtypUserDefinedDefaultValue</span></span></p></td>
<td><p><span data-ttu-id="2324f-166">Se llamará a la función de devolución de llamada para calcular un valor predeterminado definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="2324f-166">The callback function will be called to calculate a user-defined default.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2324f-167">JET_cbtypOnlineDefragCompleted</span><span class="sxs-lookup"><span data-stu-id="2324f-167">JET_cbtypOnlineDefragCompleted</span></span></p></td>
<td><p><span data-ttu-id="2324f-168">Se llamará a la función de devolución de llamada después de que se haya completado una llamada a <a href="gg294095(v=exchg.10).md">JetDefragment2</a> .</span><span class="sxs-lookup"><span data-stu-id="2324f-168">The callback function will be called after a call to <a href="gg294095(v=exchg.10).md">JetDefragment2</a> has completed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2324f-169">JET_cbtypFreeCursorLS</span><span class="sxs-lookup"><span data-stu-id="2324f-169">JET_cbtypFreeCursorLS</span></span></p></td>
<td><p><span data-ttu-id="2324f-170">Se llamará a la función de devolución de llamada cuando se debe liberar el almacenamiento local asociado a un cursor.</span><span class="sxs-lookup"><span data-stu-id="2324f-170">The callback function will be called when the local storage that is associated with a cursor must be freed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2324f-171">JET_cbtypFreeTableLS</span><span class="sxs-lookup"><span data-stu-id="2324f-171">JET_cbtypFreeTableLS</span></span></p></td>
<td><p><span data-ttu-id="2324f-172">Se llamará a la función de devolución de llamada cuando se debe liberar el almacenamiento local asociado a una tabla.</span><span class="sxs-lookup"><span data-stu-id="2324f-172">The callback function will be called when the local storage that is associated with a table must be freed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2324f-173">**grbit**</span><span class="sxs-lookup"><span data-stu-id="2324f-173">**grbit**</span></span>

<span data-ttu-id="2324f-174">Grupo de bits que contiene las opciones de esta llamada, que incluyen cero o más de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="2324f-174">A group of bits that contain the options for this call, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2324f-175">Value</span><span class="sxs-lookup"><span data-stu-id="2324f-175">Value</span></span></p></th>
<th><p><span data-ttu-id="2324f-176">Significado</span><span class="sxs-lookup"><span data-stu-id="2324f-176">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2324f-177">JET_bitTableCreateFixedDDL</span><span class="sxs-lookup"><span data-stu-id="2324f-177">JET_bitTableCreateFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="2324f-178">La configuración de JET_bitTableCreateFixedDDL impide las operaciones DDL en la tabla (por ejemplo, agregar o quitar columnas).</span><span class="sxs-lookup"><span data-stu-id="2324f-178">Setting JET_bitTableCreateFixedDDL prevents DDL operations on the table (such as adding or removing columns).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2324f-179">JET_bitTableCreateTemplateTable</span><span class="sxs-lookup"><span data-stu-id="2324f-179">JET_bitTableCreateTemplateTable</span></span></p></td>
<td><p><span data-ttu-id="2324f-180">La configuración de JET_bitTableCreateTemplateTable hace que la tabla sea una tabla de plantilla.</span><span class="sxs-lookup"><span data-stu-id="2324f-180">Setting JET_bitTableCreateTemplateTable causes the table to be a template table.</span></span> <span data-ttu-id="2324f-181">Las nuevas tablas pueden especificar el nombre de esta tabla como su tabla de plantilla.</span><span class="sxs-lookup"><span data-stu-id="2324f-181">New tables can then specify the name of this table as their template table.</span></span> <span data-ttu-id="2324f-182">La configuración de JET_bitTableCreateTemplateTable implica JET_bitTableCreateFixedDDL.</span><span class="sxs-lookup"><span data-stu-id="2324f-182">Setting JET_bitTableCreateTemplateTable implies JET_bitTableCreateFixedDDL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2324f-183">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="2324f-183">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span></span></p></td>
<td><p><span data-ttu-id="2324f-184">Se debe usar junto con JET_bitTableCreateTemplateTable.</span><span class="sxs-lookup"><span data-stu-id="2324f-184">Must be used in conjunction with JET_bitTableCreateTemplateTable.</span></span> <span data-ttu-id="2324f-185">Desusado.</span><span class="sxs-lookup"><span data-stu-id="2324f-185">Deprecated.</span></span> <span data-ttu-id="2324f-186">No utilizar.</span><span class="sxs-lookup"><span data-stu-id="2324f-186">Do not use.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2324f-187">**TABLEID**</span><span class="sxs-lookup"><span data-stu-id="2324f-187">**tableid**</span></span>

<span data-ttu-id="2324f-188">Un campo de salida que contiene el [JET_TABLEID](./jet-tableid.md) de la nueva tabla si la llamada a la API se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="2324f-188">An output field that holds the [JET_TABLEID](./jet-tableid.md) of the new table if the API call succeeds.</span></span> <span data-ttu-id="2324f-189">Si se produce un error en la llamada API, el valor es indefinido.</span><span class="sxs-lookup"><span data-stu-id="2324f-189">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="2324f-190">**Creado**</span><span class="sxs-lookup"><span data-stu-id="2324f-190">**cCreated**</span></span>

<span data-ttu-id="2324f-191">Un campo de salida que contiene el recuento de objetos que se crean si la llamada de API se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="2324f-191">An output field that contains the count of objects that are created if the API call succeeds.</span></span> <span data-ttu-id="2324f-192">Si se produce un error en la llamada API, el valor es indefinido.</span><span class="sxs-lookup"><span data-stu-id="2324f-192">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="2324f-193">El recuento de objetos que se crea es igual a la suma de las columnas, las tablas y los índices que se han creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="2324f-193">The count of objects that is created is equal to the sum of columns, tables, and indexes that are successfully created.</span></span>

### <a name="requirements"></a><span data-ttu-id="2324f-194">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2324f-194">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2324f-195"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="2324f-195"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2324f-196">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2324f-196">Requires Windows  Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2324f-197"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="2324f-197"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2324f-198">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2324f-198">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2324f-199"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="2324f-199"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2324f-200">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="2324f-200">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2324f-201"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="2324f-201"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="2324f-202">Se implementa como <strong>JET_TABLECREATE2_W</strong> (Unicode) y <strong>JET_TABLECREATE2_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="2324f-202">Implemented as <strong>JET_TABLECREATE2_W</strong> (Unicode) and <strong>JET_TABLECREATE2_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="2324f-203">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2324f-203">See Also</span></span>

[<span data-ttu-id="2324f-204">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="2324f-204">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="2324f-205">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="2324f-205">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="2324f-206">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="2324f-206">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="2324f-207">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="2324f-207">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="2324f-208">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="2324f-208">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="2324f-209">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="2324f-209">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="2324f-210">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="2324f-210">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="2324f-211">JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="2324f-211">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="2324f-212">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="2324f-212">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="2324f-213">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="2324f-213">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="2324f-214">JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="2324f-214">JetDefragment2</span></span>](./jetdefragment2-function.md)
