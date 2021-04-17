---
description: 'Más información acerca de: estructura de JET_TABLECREATE3'
title: Estructura de JET_TABLECREATE3
TOCTitle: JET_TABLECREATE3 Structure
ms:assetid: 61909569-e704-494b-a56d-b64d1a2ee157
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269264(v=EXCHG.10)
ms:contentKeyID: 32765566
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 587649b592f2b0d213a481c3bfbecc723240e486
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705456"
---
# <a name="jet_tablecreate3-structure"></a><span data-ttu-id="3c783-103">Estructura de JET_TABLECREATE3</span><span class="sxs-lookup"><span data-stu-id="3c783-103">JET_TABLECREATE3 Structure</span></span>


<span data-ttu-id="3c783-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3c783-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="3c783-105">La estructura de **JET_TABLECREATE3** contiene la información necesaria para crear una tabla rellenada con columnas e índices en una base de datos del motor de almacenamiento extensible (ese) y que designa una función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="3c783-105">The **JET_TABLECREATE3** structure contains the information that is needed to create a table populated with columns and indexes in an Extensible Storage Engine (ESE) database, and that designates a callback function.</span></span> <span data-ttu-id="3c783-106">La función [JetCreateTableColumnIndex3](./jetcreatetablecolumnindex3-function.md) utiliza la estructura **JET_TABLECREATE3** .</span><span class="sxs-lookup"><span data-stu-id="3c783-106">The **JET_TABLECREATE3** structure is used by the [JetCreateTableColumnIndex3](./jetcreatetablecolumnindex3-function.md) function.</span></span>

<span data-ttu-id="3c783-107">La estructura de **JET_TABLECREATE3** se presentó en el sistema operativo Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3c783-107">The **JET_TABLECREATE3** structure was introduced in the Windows 7 operating system.</span></span>

``` cpp
typedef struct tagJET_TABLECREATE3 {
  unsigned long cbStruct;
  tchar* szTableName;
  tchar* szTemplateTableName;
  unsigned long ulPages;
  unsigned long ulDensity;
  JET_COLUMNCREATE* rgcolumncreate;
  unsigned long cColumns;
    JET_INDEXCREATE2* rgindexcreate;
  unsigned long cIndexes;
  tchar* szCallback;
  JET_CBTYP cbtyp;
  JET_GRBIT grbit;
  JET_TABLEID tableid;
  un  JET_GRBIT grbit;
  JET_SPACEHINTS* pSeqSpacehints;
  JET_SPACEHINTS* pLVSpacehints;
  unsigned long cbSeparateLV;
  JET_TABLEID tableid;
  unsigned long cCreated;
} JET_TABLECREATE3;>
```

### <a name="members"></a><span data-ttu-id="3c783-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="3c783-108">Members</span></span>

<span data-ttu-id="3c783-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="3c783-109">**cbStruct**</span></span>

<span data-ttu-id="3c783-110">Tamaño de esta estructura en bytes (para una futura ampliación).</span><span class="sxs-lookup"><span data-stu-id="3c783-110">The size of this structure in bytes (for future expansion).</span></span> <span data-ttu-id="3c783-111">Debe establecerse en sizeof (JET_TABLECREATE3) en bytes.</span><span class="sxs-lookup"><span data-stu-id="3c783-111">It must be set to sizeof( JET_TABLECREATE3 ) in bytes.</span></span>

<span data-ttu-id="3c783-112">**szTableName**</span><span class="sxs-lookup"><span data-stu-id="3c783-112">**szTableName**</span></span>

<span data-ttu-id="3c783-113">El objeto de la tabla que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="3c783-113">The name of the table to create.</span></span>

<span data-ttu-id="3c783-114">El nombre debe cumplir las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="3c783-114">The name must meet the following conditions:</span></span>

  - <span data-ttu-id="3c783-115">Debe tener un valor menor que JET_cbNameMost, sin incluir el carácter null de terminación.</span><span class="sxs-lookup"><span data-stu-id="3c783-115">It must have a value that is less than JET_cbNameMost, not including the terminating null.</span></span>

  - <span data-ttu-id="3c783-116">Debe estar formado por el siguiente conjunto de caracteres: de 0 a 9, de la a a la Z, de la a a la z y de todos los demás signos de puntuación, excepto el signo de exclamación ( \! ), la coma (,), el corchete de apertura () y el \[ corchete de cierre ( \] ); es decir, los caracteres ASCII 0x20, de</span><span class="sxs-lookup"><span data-stu-id="3c783-116">It must consist of the following set of characters: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]); that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="3c783-117">No debe comenzar con un espacio.</span><span class="sxs-lookup"><span data-stu-id="3c783-117">It must not begin with a space.</span></span>

  - <span data-ttu-id="3c783-118">Debe contener al menos un carácter que no sea un espacio.</span><span class="sxs-lookup"><span data-stu-id="3c783-118">It must consist of at least one non-space character.</span></span>

<span data-ttu-id="3c783-119">**szTemplateTableName**</span><span class="sxs-lookup"><span data-stu-id="3c783-119">**szTemplateTableName**</span></span>

<span data-ttu-id="3c783-120">Nombre de una tabla existente de la que se va a heredar el lenguaje de definición de datos (DDL) base.</span><span class="sxs-lookup"><span data-stu-id="3c783-120">The name of an existing table from which to inherit the base data definition language (DDL).</span></span> <span data-ttu-id="3c783-121">El uso de una tabla de plantilla permite la creación sencilla de muchas tablas con columnas e índices idénticos.</span><span class="sxs-lookup"><span data-stu-id="3c783-121">Use of a template table allows for the easy creation of many tables with identical columns and indexes.</span></span>

<span data-ttu-id="3c783-122">**ulPages**</span><span class="sxs-lookup"><span data-stu-id="3c783-122">**ulPages**</span></span>

<span data-ttu-id="3c783-123">Número inicial de páginas de base de datos que se van a asignar a la tabla.</span><span class="sxs-lookup"><span data-stu-id="3c783-123">The initial number of database pages to allocate for the table.</span></span> <span data-ttu-id="3c783-124">Si se especifica un número mayor que uno, se puede reducir la fragmentación si se insertan muchas filas en esta tabla.</span><span class="sxs-lookup"><span data-stu-id="3c783-124">Specifying a number larger than one can reduce fragmentation if many rows are inserted into this table.</span></span>

<span data-ttu-id="3c783-125">**ulDensity**</span><span class="sxs-lookup"><span data-stu-id="3c783-125">**ulDensity**</span></span>

<span data-ttu-id="3c783-126">Densidad de la tabla, en puntos porcentuales.</span><span class="sxs-lookup"><span data-stu-id="3c783-126">The table density, in percentage points.</span></span> <span data-ttu-id="3c783-127">El número debe ser 0 o estar comprendido entre 20 y 100.</span><span class="sxs-lookup"><span data-stu-id="3c783-127">The number must be either 0 or in the range of 20 through 100.</span></span> <span data-ttu-id="3c783-128">Pasar 0 significa que se debe usar el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="3c783-128">Passing 0 means that the default value should be used.</span></span> <span data-ttu-id="3c783-129">El valor predeterminado es 80.</span><span class="sxs-lookup"><span data-stu-id="3c783-129">The default value is 80.</span></span>

<span data-ttu-id="3c783-130">**rgcolumncreate**</span><span class="sxs-lookup"><span data-stu-id="3c783-130">**rgcolumncreate**</span></span>

<span data-ttu-id="3c783-131">Matriz de estructuras de [JET_COLUMNCREATE](./jet-columncreate-structure.md) , cada una de las cuales corresponde a una columna que se va a crear en la nueva tabla.</span><span class="sxs-lookup"><span data-stu-id="3c783-131">An array of [JET_COLUMNCREATE](./jet-columncreate-structure.md) structures, each of which corresponds to a column to be created in the new table.</span></span>

<span data-ttu-id="3c783-132">**cColumns**</span><span class="sxs-lookup"><span data-stu-id="3c783-132">**cColumns**</span></span>

<span data-ttu-id="3c783-133">El número de elementos [JET_COLUMNCREATE](./jet-columncreate-structure.md) en el parámetro *rgcolumncreate* .</span><span class="sxs-lookup"><span data-stu-id="3c783-133">The number of [JET_COLUMNCREATE](./jet-columncreate-structure.md) elements in the *rgcolumncreate* parameter.</span></span>

<span data-ttu-id="3c783-134">**rgindexcreate**</span><span class="sxs-lookup"><span data-stu-id="3c783-134">**rgindexcreate**</span></span>

<span data-ttu-id="3c783-135">Matriz de estructuras de [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) , cada una de las cuales corresponde a un índice que se va a crear en la nueva tabla.</span><span class="sxs-lookup"><span data-stu-id="3c783-135">An array of [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structures, each of which corresponds to an index to be created in the new table.</span></span>

<span data-ttu-id="3c783-136">**cIndexes**</span><span class="sxs-lookup"><span data-stu-id="3c783-136">**cIndexes**</span></span>

<span data-ttu-id="3c783-137">El número de elementos [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) en el parámetro *rgindexcreate* .</span><span class="sxs-lookup"><span data-stu-id="3c783-137">The number of [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) elements in the *rgindexcreate* parameter.</span></span>

<span data-ttu-id="3c783-138">**szCallback**</span><span class="sxs-lookup"><span data-stu-id="3c783-138">**szCallback**</span></span>

<span data-ttu-id="3c783-139">Función a la que se llama durante ciertos eventos.</span><span class="sxs-lookup"><span data-stu-id="3c783-139">The function that gets called during certain events.</span></span> <span data-ttu-id="3c783-140">**cbtyp** determina cuándo se llamará a la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="3c783-140">**cbtyp** determines when the callback function will be called.</span></span>

<span data-ttu-id="3c783-141">El formato de **szCallback** debe ser "función de módulo \! ", por ejemplo, "alpha \! beta" hace referencia a la función beta del módulo denominado "Alpha".</span><span class="sxs-lookup"><span data-stu-id="3c783-141">The format of **szCallback** must be "module\!function" — for example, "alpha\!beta" refers to the beta function in the module named "alpha".</span></span>

<span data-ttu-id="3c783-142">El prototipo de la función debe coincidir con la función de devolución de llamada [JET_CALLBACK](./jet-callback-callback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="3c783-142">The prototype of the function must match the [JET_CALLBACK](./jet-callback-callback-function.md) callback function.</span></span>

<span data-ttu-id="3c783-143">**cbtyp**</span><span class="sxs-lookup"><span data-stu-id="3c783-143">**cbtyp**</span></span>

<span data-ttu-id="3c783-144">Describe el tipo de función de devolución de llamada designado por **szCallback**.</span><span class="sxs-lookup"><span data-stu-id="3c783-144">Describes the type of callback function designated by **szCallback**.</span></span> <span data-ttu-id="3c783-145">Para obtener más información, vea [JET_CBTYP](./jet-cbtyp.md).</span><span class="sxs-lookup"><span data-stu-id="3c783-145">For more information, see [JET_CBTYP](./jet-cbtyp.md).</span></span>

<span data-ttu-id="3c783-146">Este campo de bits se compone de uno o varios de los valores de bit que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="3c783-146">This bitfield is composed of one or more of the bit values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3c783-147">Value</span><span class="sxs-lookup"><span data-stu-id="3c783-147">Value</span></span></p></th>
<th><p><span data-ttu-id="3c783-148">Significado</span><span class="sxs-lookup"><span data-stu-id="3c783-148">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3c783-149">JET_cbtypFinalize</span><span class="sxs-lookup"><span data-stu-id="3c783-149">JET_cbtypFinalize</span></span></p></td>
<td><p><span data-ttu-id="3c783-150">Se llamará a la función de devolución de llamada cuando una columna que se pueda finalizar haya pasado a cero.</span><span class="sxs-lookup"><span data-stu-id="3c783-150">The callback function will be called when a column that can be finalized has gone to zero.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c783-151">JET_cbtypBeforeInsert</span><span class="sxs-lookup"><span data-stu-id="3c783-151">JET_cbtypBeforeInsert</span></span></p></td>
<td><p><span data-ttu-id="3c783-152">Se llamará a la función de devolución de llamada antes de la inserción del registro.</span><span class="sxs-lookup"><span data-stu-id="3c783-152">The callback function will be called prior to record insertion.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c783-153">JET_cbtypAfterInsert</span><span class="sxs-lookup"><span data-stu-id="3c783-153">JET_cbtypAfterInsert</span></span></p></td>
<td><p><span data-ttu-id="3c783-154">Se llamará a la función de devolución de llamada después de que el motor de base de datos haya terminado de insertar un registro.</span><span class="sxs-lookup"><span data-stu-id="3c783-154">The callback function will be called after the database engine has finished inserting a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c783-155">JET_cbtypBeforeReplace</span><span class="sxs-lookup"><span data-stu-id="3c783-155">JET_cbtypBeforeReplace</span></span></p></td>
<td><p><span data-ttu-id="3c783-156">Se llamará a la función de devolución de llamada antes de la modificación de un registro.</span><span class="sxs-lookup"><span data-stu-id="3c783-156">The callback function will be called prior to the modification of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c783-157">JET_cbtypAfterReplace</span><span class="sxs-lookup"><span data-stu-id="3c783-157">JET_cbtypAfterReplace</span></span></p></td>
<td><p><span data-ttu-id="3c783-158">Se llamará a la función de devolución de llamada después de finalizar la modificación de un registro.</span><span class="sxs-lookup"><span data-stu-id="3c783-158">The callback function will be called after finishing the modification of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c783-159">JET_cbtypBeforeDelete</span><span class="sxs-lookup"><span data-stu-id="3c783-159">JET_cbtypBeforeDelete</span></span></p></td>
<td><p><span data-ttu-id="3c783-160">Se llamará a la función de devolución de llamada antes de la eliminación de un registro.</span><span class="sxs-lookup"><span data-stu-id="3c783-160">The callback function will be called prior to the deletion of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c783-161">JET_cbtypAfterDelete</span><span class="sxs-lookup"><span data-stu-id="3c783-161">JET_cbtypAfterDelete</span></span></p></td>
<td><p><span data-ttu-id="3c783-162">Se llamará a la función de devolución de llamada después de que se haya eliminado un registro.</span><span class="sxs-lookup"><span data-stu-id="3c783-162">The callback function will be called after a record has been deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c783-163">JET_cbtypUserDefinedDefaultValue</span><span class="sxs-lookup"><span data-stu-id="3c783-163">JET_cbtypUserDefinedDefaultValue</span></span></p></td>
<td><p><span data-ttu-id="3c783-164">Se llamará a la función de devolución de llamada para calcular un valor predeterminado definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="3c783-164">The callback function will be called to calculate a user-defined default.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c783-165">JET_cbtypFreeCursorLS</span><span class="sxs-lookup"><span data-stu-id="3c783-165">JET_cbtypFreeCursorLS</span></span></p></td>
<td><p><span data-ttu-id="3c783-166">Se llamará a la función de devolución de llamada cuando se debe liberar el almacenamiento local asociado a un cursor.</span><span class="sxs-lookup"><span data-stu-id="3c783-166">The callback function will be called when the local storage that is associated with a cursor must be freed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c783-167">JET_cbtypFreeTableLS</span><span class="sxs-lookup"><span data-stu-id="3c783-167">JET_cbtypFreeTableLS</span></span></p></td>
<td><p><span data-ttu-id="3c783-168">Se llamará a la función de devolución de llamada cuando se debe liberar el almacenamiento local asociado a una tabla.</span><span class="sxs-lookup"><span data-stu-id="3c783-168">The callback function will be called when the local storage that is associated with a table must be freed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3c783-169">**grbit**</span><span class="sxs-lookup"><span data-stu-id="3c783-169">**grbit**</span></span>

<span data-ttu-id="3c783-170">Grupo de bits que contiene cero o más valores de la opción de llamada que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="3c783-170">A group of bits that contains zero or more of the call option values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3c783-171">Value</span><span class="sxs-lookup"><span data-stu-id="3c783-171">Value</span></span></p></th>
<th><p><span data-ttu-id="3c783-172">Significado</span><span class="sxs-lookup"><span data-stu-id="3c783-172">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3c783-173">JET_bitTableCreateFixedDDL</span><span class="sxs-lookup"><span data-stu-id="3c783-173">JET_bitTableCreateFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="3c783-174">Impide las operaciones DDL en la tabla (por ejemplo, agregar o quitar columnas).</span><span class="sxs-lookup"><span data-stu-id="3c783-174">Prevents DDL operations on the table (such as adding or removing columns).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c783-175">JET_bitTableCreateTemplateTable</span><span class="sxs-lookup"><span data-stu-id="3c783-175">JET_bitTableCreateTemplateTable</span></span></p></td>
<td><p><span data-ttu-id="3c783-176">Hace que la tabla sea una tabla de plantilla.</span><span class="sxs-lookup"><span data-stu-id="3c783-176">Causes the table to be a template table.</span></span> <span data-ttu-id="3c783-177">Las nuevas tablas pueden especificar el nombre de esta tabla como su tabla de plantilla.</span><span class="sxs-lookup"><span data-stu-id="3c783-177">New tables can then specify the name of this table as their template table.</span></span> <span data-ttu-id="3c783-178">La configuración de JET_bitTableCreateTemplateTable implica JET_bitTableCreateFixedDDL.</span><span class="sxs-lookup"><span data-stu-id="3c783-178">Setting JET_bitTableCreateTemplateTable implies JET_bitTableCreateFixedDDL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c783-179">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="3c783-179">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span></span></p></td>
<td><p><span data-ttu-id="3c783-180">Se debe usar junto con JET_bitTableCreateTemplateTable.</span><span class="sxs-lookup"><span data-stu-id="3c783-180">Must be used in conjunction with JET_bitTableCreateTemplateTable.</span></span> <span data-ttu-id="3c783-181">Desusado.</span><span class="sxs-lookup"><span data-stu-id="3c783-181">Deprecated.</span></span> <span data-ttu-id="3c783-182">No utilizar.</span><span class="sxs-lookup"><span data-stu-id="3c783-182">Do not use.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3c783-183">**pSeqSpacehints**</span><span class="sxs-lookup"><span data-stu-id="3c783-183">**pSeqSpacehints**</span></span>

<span data-ttu-id="3c783-184">Puntero a una estructura de [JET_SPACEHINTS](./jet-spacehints-structure.md) para el índice secuencial predeterminado.</span><span class="sxs-lookup"><span data-stu-id="3c783-184">A pointer to a [JET_SPACEHINTS](./jet-spacehints-structure.md) structure for default sequential index.</span></span>

<span data-ttu-id="3c783-185">**pSeqSpacehints** se presentó en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3c783-185">**pSeqSpacehints** was introduced in Windows 7.</span></span>

<span data-ttu-id="3c783-186">**pLVSpacehints**</span><span class="sxs-lookup"><span data-stu-id="3c783-186">**pLVSpacehints**</span></span>

<span data-ttu-id="3c783-187">Puntero a una estructura de [JET_SPACEHINTS](./jet-spacehints-structure.md) para un árbol de valores largos separados.</span><span class="sxs-lookup"><span data-stu-id="3c783-187">A pointer to a [JET_SPACEHINTS](./jet-spacehints-structure.md) structure for a Separated Long Value tree.</span></span>

<span data-ttu-id="3c783-188">**pLVSpacehints** se presentó en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3c783-188">**pLVSpacehints** was introduced in Windows 7.</span></span>

<span data-ttu-id="3c783-189">**cbSeparateLV**</span><span class="sxs-lookup"><span data-stu-id="3c783-189">**cbSeparateLV**</span></span>

<span data-ttu-id="3c783-190">Tamaño para separar una LV intrínseca del registro principal.</span><span class="sxs-lookup"><span data-stu-id="3c783-190">The size to separate an intrinsic LV from the primary record.</span></span> <span data-ttu-id="3c783-191">Cualquier estructura de c de valor largo para un árbol de LV separado.</span><span class="sxs-lookup"><span data-stu-id="3c783-191">Any long-value c structure for a Separated LV tree.</span></span> <span data-ttu-id="3c783-192">Para obtener más información, consulte ng-Value en [JET_SPACEHINTS](./jet-spacehints-structure.md).</span><span class="sxs-lookup"><span data-stu-id="3c783-192">For more information, see ng-value in [JET_SPACEHINTS](./jet-spacehints-structure.md).</span></span> <span data-ttu-id="3c783-193">Las columnas de valor largo menores que este valor pueden estar separadas si el registro es demasiado grande.</span><span class="sxs-lookup"><span data-stu-id="3c783-193">Long-value columns smaller than this value may be separated if the record becomes too large.</span></span>

<span data-ttu-id="3c783-194">**cbSeparateLV** se presentó en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3c783-194">**cbSeparateLV** was introduced in Windows 7.</span></span>

<span data-ttu-id="3c783-195">**TABLEID**</span><span class="sxs-lookup"><span data-stu-id="3c783-195">**tableid**</span></span>

<span data-ttu-id="3c783-196">Un campo de salida que contiene el [JET_TABLEID](./jet-tableid.md) de la nueva tabla si la llamada a la API se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="3c783-196">An output field that holds the [JET_TABLEID](./jet-tableid.md) of the new table if the API call succeeds.</span></span> <span data-ttu-id="3c783-197">Si se produce un error en la llamada API, el valor es indefinido.</span><span class="sxs-lookup"><span data-stu-id="3c783-197">If the API call fails, the value is undefined.</span></span> <span data-ttu-id="3c783-198">Esta tabla se abre exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="3c783-198">This table is opened exclusively.</span></span>

<span data-ttu-id="3c783-199">**Creado**</span><span class="sxs-lookup"><span data-stu-id="3c783-199">**cCreated**</span></span>

<span data-ttu-id="3c783-200">Un campo de salida que contiene el recuento de objetos que se crean si la llamada de API se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="3c783-200">An output field that contains the count of objects that are created if the API call succeeds.</span></span> <span data-ttu-id="3c783-201">Si se produce un error en la llamada API, el valor es indefinido.</span><span class="sxs-lookup"><span data-stu-id="3c783-201">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="3c783-202">El recuento de objetos que se crean es igual a la suma de las columnas, las tablas y los índices que se han creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="3c783-202">The count of objects that are created is equal to the sum of columns, tables, and indexes that are successfully created.</span></span>

### <a name="requirements"></a><span data-ttu-id="3c783-203">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c783-203">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3c783-204"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="3c783-204"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3c783-205">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3c783-205">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c783-206"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="3c783-206"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3c783-207">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3c783-207">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c783-208"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="3c783-208"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3c783-209">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="3c783-209">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c783-210"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="3c783-210"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="3c783-211">Se implementa como <strong>JET_TABLECREATE3_W</strong> (Unicode) y <strong>JET_TABLECREATE3_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="3c783-211">Implemented as <strong>JET_TABLECREATE3_W</strong> (Unicode) and <strong>JET_TABLECREATE3_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="3c783-212">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c783-212">See also</span></span>

[<span data-ttu-id="3c783-213">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="3c783-213">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="3c783-214">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="3c783-214">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="3c783-215">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="3c783-215">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="3c783-216">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3c783-216">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3c783-217">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="3c783-217">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="3c783-218">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="3c783-218">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="3c783-219">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="3c783-219">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="3c783-220">JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="3c783-220">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="3c783-221">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="3c783-221">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="3c783-222">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="3c783-222">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="3c783-223">JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="3c783-223">JetDefragment2</span></span>](./jetdefragment2-function.md)
