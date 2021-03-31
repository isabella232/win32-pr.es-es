---
description: 'Más información acerca de: estructura de JET_INDEXCREATE'
title: Estructura de JET_INDEXCREATE
TOCTitle: JET_INDEXCREATE Structure
ms:assetid: 0c55f25c-d42a-49ba-a1fe-549850fdc9a6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269186(v=EXCHG.10)
ms:contentKeyID: 32765489
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
ms.openlocfilehash: 4c465d81dce628497b1b9210fb08b37a3003e2e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815606"
---
# <a name="jet_indexcreate-structure"></a><span data-ttu-id="5a885-103">Estructura de JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="5a885-103">JET_INDEXCREATE Structure</span></span>


<span data-ttu-id="5a885-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5a885-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="5a885-105">La estructura de **JET_INDEXCREATE** contiene la información necesaria para crear un índice sobre los datos en una base de datos del motor de almacenamiento extensible (ese).</span><span class="sxs-lookup"><span data-stu-id="5a885-105">The **JET_INDEXCREATE** structure contains the information needed to create an index over data in an Extensible Storage Engine (ESE) database.</span></span> <span data-ttu-id="5a885-106">La estructura la usan funciones como [JetCreateIndex2](./jetcreateindex2-function.md)y en estructuras como [JET_TABLECREATE](./jet-tablecreate-structure.md) y [JET_TABLECREATE2](./jet-tablecreate2-structure.md).</span><span class="sxs-lookup"><span data-stu-id="5a885-106">The structure is used by functions such as [JetCreateIndex2](./jetcreateindex2-function.md), and in structures such as [JET_TABLECREATE](./jet-tablecreate-structure.md) and [JET_TABLECREATE2](./jet-tablecreate2-structure.md).</span></span>

``` c++
typedef struct tagJET_INDEXCREATE {
  unsigned long cbStruct;
  tchar* szIndexName;
  tchar* szKey;
  unsigned long cbKey;
  JET_GRBIT grbit;
  unsigned long ulDensity;
  union {
    unsigned long lcid;
    JET_UNICODEINDEX* pidxunicode;
  };
  union {
    unsigned long cbVarSegMac;
    JET_TUPLELIMITS* ptuplelimits;
  };
  JET_CONDITIONALCOLUMN* rgconditionalcolumn;
  unsigned long cConditionalColumn;
  JET_ERR err;
  unsigned long cbKeyMost;
} JET_INDEXCREATE;
```

### <a name="members"></a><span data-ttu-id="5a885-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="5a885-107">Members</span></span>

<span data-ttu-id="5a885-108">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="5a885-108">**cbStruct**</span></span>

<span data-ttu-id="5a885-109">Tamaño, en bytes, de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="5a885-109">The size, in bytes, of this structure.</span></span> <span data-ttu-id="5a885-110">Establezca este miembro en sizeof (JET_INDEXCREATE).</span><span class="sxs-lookup"><span data-stu-id="5a885-110">Set this member to sizeof( JET_INDEXCREATE ).</span></span>

<span data-ttu-id="5a885-111">**szIndexName**</span><span class="sxs-lookup"><span data-stu-id="5a885-111">**szIndexName**</span></span>

<span data-ttu-id="5a885-112">Nombre del índice que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="5a885-112">The name of the index to create.</span></span>

<span data-ttu-id="5a885-113">El nombre del índice debe cumplir las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="5a885-113">The name of the index must meet the following conditions:</span></span>

  - <span data-ttu-id="5a885-114">Debe ser menor que JET_cbNameMost, sin incluir el carácter null de terminación.</span><span class="sxs-lookup"><span data-stu-id="5a885-114">It must be less than JET_cbNameMost, not including the terminating null.</span></span>

  - <span data-ttu-id="5a885-115">Debe constar de los siguientes caracteres: 0 (cero) a 9, de la a a la Z, de la a a la z y todos los demás signos de puntuación excepto " \! "</span><span class="sxs-lookup"><span data-stu-id="5a885-115">It must consist of the following characters: 0 (zero) through 9, A through Z, a through z, and all other punctuation except for "\!"</span></span> <span data-ttu-id="5a885-116">(signo de exclamación), "," (coma), " \[ " (corchete de apertura) y " \] " (corchete de cierre), es decir, caracteres ASCII 0x20, 0x22 a 0x2d, 0x2f a 0x5a, 0x5c, 0x5d a 0x7F.</span><span class="sxs-lookup"><span data-stu-id="5a885-116">(exclamation point), "," (comma), "\[" (opening bracket), and "\]" (closing bracket) — that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="5a885-117">No debe comenzar con un espacio.</span><span class="sxs-lookup"><span data-stu-id="5a885-117">It must not begin with a space.</span></span>

  - <span data-ttu-id="5a885-118">Debe contener al menos un carácter que no sea un espacio.</span><span class="sxs-lookup"><span data-stu-id="5a885-118">It must consist of at least one nonspace character.</span></span>

<span data-ttu-id="5a885-119">**szKey**</span><span class="sxs-lookup"><span data-stu-id="5a885-119">**szKey**</span></span>

<span data-ttu-id="5a885-120">Puntero a una cadena terminada en NULL de tokens delimitados por null.</span><span class="sxs-lookup"><span data-stu-id="5a885-120">A pointer to a double-null-terminated string of null-delimited tokens.</span></span>

<span data-ttu-id="5a885-121">Cada token tiene el formato " \<direction-specifier\> \<column-name\> ", donde Direction-Specification es "+" o "-".</span><span class="sxs-lookup"><span data-stu-id="5a885-121">Each token is of the form "\<direction-specifier\>\<column-name\>", where direction-specification is either "+" or "-".</span></span> <span data-ttu-id="5a885-122">Por ejemplo, un **szKey** de "+ ABC \\ 0-Def \\ 0 + GHI \\ 0" indexará las tres columnas "ABC" (en orden ascendente), "def" (en orden descendente) y "GHI" (en orden ascendente).</span><span class="sxs-lookup"><span data-stu-id="5a885-122">For example, a **szKey** of "+abc\\0-def\\0+ghi\\0" will index over the three columns "abc" (in ascending order), "def" (in descending order), and "ghi" (in ascending order).</span></span> <span data-ttu-id="5a885-123">En el lenguaje C, los literales de cadena tienen un terminador **null** implícito; por lo tanto, la cadena anterior se terminará con un valor NULL nulo.</span><span class="sxs-lookup"><span data-stu-id="5a885-123">In the C language, string literals have an implied **NULL** terminator; therefore, the above string will be terminated by a double-NULL.</span></span>

<span data-ttu-id="5a885-124">El número de columnas especificado en **szKey** no puede superar el valor de **JET_ccolKeyMost** (una constante dependiente de la versión).</span><span class="sxs-lookup"><span data-stu-id="5a885-124">The number of columns specified in **szKey** may not exceed the value of **JET_ccolKeyMost** (a version-dependent constant).</span></span>

<span data-ttu-id="5a885-125">Al menos una columna debe tener un nombre en **szKey**.</span><span class="sxs-lookup"><span data-stu-id="5a885-125">At least one column must be named in **szKey**.</span></span>

<span data-ttu-id="5a885-126">Comportamiento obsoleto: después del terminador de doble nulo, es posible especificar un identificador de idioma (una palabra que se pasa a MAKELCID (langid, SORT_DEFAULT)) como una manera de especificar el LCID para el índice.</span><span class="sxs-lookup"><span data-stu-id="5a885-126">Obsolete behavior: After the double-NULL terminator, it is possible to specify a language ID (a WORD which gets passed into MAKELCID( langid, SORT_DEFAULT ) ) as a way to specify the LCID for the index.</span></span> <span data-ttu-id="5a885-127">No es válido especificar un identificador de idioma en **szKey** y un LCID en [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) (estableciendo JET_bitIndexUnicode en *grbit*).</span><span class="sxs-lookup"><span data-stu-id="5a885-127">It is illegal to specify both a language ID in **szKey** and an LCID in [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) (by setting JET_bitIndexUnicode in *grbit*).</span></span>

<span data-ttu-id="5a885-128">En desuso: después del identificador de idioma, es posible pasar **cbVarSegMac** como un USHORT.</span><span class="sxs-lookup"><span data-stu-id="5a885-128">Deprecated: After the language ID, it is possible to pass **cbVarSegMac** as a USHORT.</span></span> <span data-ttu-id="5a885-129">El comportamiento es indefinido si USHORT se establece en **szKey** y si **cbVarSegMac** se establece en la estructura.</span><span class="sxs-lookup"><span data-stu-id="5a885-129">The behavior is undefined if the USHORT is set both in **szKey** and if **cbVarSegMac** is set in the structure.</span></span>

<span data-ttu-id="5a885-130">**cbKey**</span><span class="sxs-lookup"><span data-stu-id="5a885-130">**cbKey**</span></span>

<span data-ttu-id="5a885-131">La longitud, en bytes, de **szKey** , incluidos los dos valores NULL de terminación.</span><span class="sxs-lookup"><span data-stu-id="5a885-131">The length, in bytes, of **szKey** including the two terminating nulls.</span></span>

<span data-ttu-id="5a885-132">**grbit**</span><span class="sxs-lookup"><span data-stu-id="5a885-132">**grbit**</span></span>

<span data-ttu-id="5a885-133">Grupo de bits que incluye cero o más de los valores enumerados en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="5a885-133">A group of bits that includes zero or more of the values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5a885-134">Value</span><span class="sxs-lookup"><span data-stu-id="5a885-134">Value</span></span></p></th>
<th><p><span data-ttu-id="5a885-135">Significado</span><span class="sxs-lookup"><span data-stu-id="5a885-135">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a885-136">JET_bitIndexUnique</span><span class="sxs-lookup"><span data-stu-id="5a885-136">JET_bitIndexUnique</span></span></p></td>
<td><p><span data-ttu-id="5a885-137">No se permiten entradas de índice duplicadas (claves).</span><span class="sxs-lookup"><span data-stu-id="5a885-137">Duplicate index entries (keys) are not allowed.</span></span> <span data-ttu-id="5a885-138">Esto se aplica cuando se llama a <a href="gg269288(v=exchg.10).md">JetUpdate</a> , no cuando se llama a <a href="gg294137(v=exchg.10).md">JetSetColumn</a> .</span><span class="sxs-lookup"><span data-stu-id="5a885-138">This is enforced when <a href="gg269288(v=exchg.10).md">JetUpdate</a> is called, not when <a href="gg294137(v=exchg.10).md">JetSetColumn</a> is called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a885-139">JET_bitIndexPrimary</span><span class="sxs-lookup"><span data-stu-id="5a885-139">JET_bitIndexPrimary</span></span></p></td>
<td><p><span data-ttu-id="5a885-140">El índice es un índice principal (clúster).</span><span class="sxs-lookup"><span data-stu-id="5a885-140">The index is a primary (clustered) index.</span></span> <span data-ttu-id="5a885-141">Cada tabla debe tener exactamente un índice principal.</span><span class="sxs-lookup"><span data-stu-id="5a885-141">Every table must have exactly one primary index.</span></span> <span data-ttu-id="5a885-142">Si no se define un índice principal explícitamente en una tabla, el motor de base de datos creará su propio índice principal.</span><span class="sxs-lookup"><span data-stu-id="5a885-142">If no primary index is explicitly defined over a table, the database engine will create its own primary index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a885-143">JET_bitIndexDisallowNull</span><span class="sxs-lookup"><span data-stu-id="5a885-143">JET_bitIndexDisallowNull</span></span></p></td>
<td><p><span data-ttu-id="5a885-144">Ninguna de las columnas en las que se crea el índice puede contener un valor <strong>null</strong> .</span><span class="sxs-lookup"><span data-stu-id="5a885-144">None of the columns over which the index is created can contain a <strong>NULL</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a885-145">JET_bitIndexIgnoreNull</span><span class="sxs-lookup"><span data-stu-id="5a885-145">JET_bitIndexIgnoreNull</span></span></p></td>
<td><p><span data-ttu-id="5a885-146">No agregue una entrada de índice para una fila si todas las columnas que se van a indizar son <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="5a885-146">Do not add an index entry for a row if all of the columns being indexed are <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a885-147">JET_bitIndexIgnoreAnyNull</span><span class="sxs-lookup"><span data-stu-id="5a885-147">JET_bitIndexIgnoreAnyNull</span></span></p></td>
<td><p><span data-ttu-id="5a885-148">No agregue una entrada de índice para una fila si alguna de las columnas que se van a indizar es <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="5a885-148">Do not add an index entry for a row if any of the columns being indexed are <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a885-149">JET_bitIndexIgnoreFirstNull</span><span class="sxs-lookup"><span data-stu-id="5a885-149">JET_bitIndexIgnoreFirstNull</span></span></p></td>
<td><p><span data-ttu-id="5a885-150">No agregue una entrada de índice para una fila si la primera columna que se va a indizar es <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="5a885-150">Do not add an index entry for a row if the first column being indexed is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a885-151">JET_bitIndexLazyFlush</span><span class="sxs-lookup"><span data-stu-id="5a885-151">JET_bitIndexLazyFlush</span></span></p></td>
<td><p><span data-ttu-id="5a885-152">Las operaciones de índice se registrarán de forma diferida.</span><span class="sxs-lookup"><span data-stu-id="5a885-152">Index operations will be logged lazily.</span></span></p>
<p><span data-ttu-id="5a885-153">JET_bitIndexLazyFlush no afecta a la Laziness de las actualizaciones de datos.</span><span class="sxs-lookup"><span data-stu-id="5a885-153">JET_bitIndexLazyFlush does not affect the laziness of data updates.</span></span> <span data-ttu-id="5a885-154">Si la terminación del proceso interrumpe la operación de indexación, la recuperación de software seguirá pudiendo ser capaz de obtener la base de datos en un estado coherente, pero es posible que el índice no esté presente.</span><span class="sxs-lookup"><span data-stu-id="5a885-154">If the indexing operation is interrupted by process termination, Soft Recovery will still be able to able to get the database to a consistent state, but the index might not be present.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a885-155">JET_bitIndexEmpty</span><span class="sxs-lookup"><span data-stu-id="5a885-155">JET_bitIndexEmpty</span></span></p></td>
<td><p><span data-ttu-id="5a885-156">No intente compilar el índice, ya que todas las entradas se evaluarían como <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="5a885-156">Do not attempt to build the index, because all entries would evaluate to <strong>NULL</strong>.</span></span> <span data-ttu-id="5a885-157"><strong>grbit</strong> también debe especificar JET_bitIgnoreAnyNull cuando se pasa JET_bitIndexEmpty.</span><span class="sxs-lookup"><span data-stu-id="5a885-157"><strong>grbit</strong> must also specify JET_bitIgnoreAnyNull when JET_bitIndexEmpty is passed.</span></span> <span data-ttu-id="5a885-158">Se trata de una mejora del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="5a885-158">This is a performance enhancement.</span></span> <span data-ttu-id="5a885-159">Por ejemplo, si se agrega una nueva columna a una tabla, se crea un índice sobre esta columna recién agregada y se examinan todos los registros de la tabla, aunque no se agreguen al índice.</span><span class="sxs-lookup"><span data-stu-id="5a885-159">For example, if a new column is added to a table, an index is created over this newly added column, and all the records in the table are scanned even though they are not added to the index.</span></span> <span data-ttu-id="5a885-160">Al especificar JET_bitIndexEmpty se omite el examen de la tabla, lo que podría tardar mucho tiempo.</span><span class="sxs-lookup"><span data-stu-id="5a885-160">Specifying JET_bitIndexEmpty skips the scanning of the table, which could potentially take a long time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a885-161">JET_bitIndexUnversioned</span><span class="sxs-lookup"><span data-stu-id="5a885-161">JET_bitIndexUnversioned</span></span></p></td>
<td><p><span data-ttu-id="5a885-162">Hace que la creación de índices sea visible para otras transacciones.</span><span class="sxs-lookup"><span data-stu-id="5a885-162">Causes index creation to be visible to other transactions.</span></span> <span data-ttu-id="5a885-163">Normalmente, una sesión de una transacción no podrá ver una operación de creación de índices en otra sesión.</span><span class="sxs-lookup"><span data-stu-id="5a885-163">Typically a session in a transaction will not be able to see an index creation operation in another session.</span></span> <span data-ttu-id="5a885-164">Esta marca puede ser útil si es probable que otra transacción cree el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="5a885-164">This flag can be useful if another transaction is likely to create the same index.</span></span> <span data-ttu-id="5a885-165">La segunda operación index-Create producirá un error en lugar de producir potencialmente muchas operaciones de base de datos innecesarias.</span><span class="sxs-lookup"><span data-stu-id="5a885-165">The second index-create will fail instead of potentially causing many unnecessary database operations.</span></span> <span data-ttu-id="5a885-166">Es posible que la segunda transacción no pueda usar el índice inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="5a885-166">The second transaction might not be able to use the index immediately.</span></span> <span data-ttu-id="5a885-167">La operación de creación de índices debe completarse antes de poderse usar.</span><span class="sxs-lookup"><span data-stu-id="5a885-167">The index creation operation has to complete before it is usable.</span></span> <span data-ttu-id="5a885-168">La sesión no debe estar actualmente en una transacción para crear un índice sin información de versión.</span><span class="sxs-lookup"><span data-stu-id="5a885-168">The session must not currently be in a transaction to create an index without version information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a885-169">JET_bitIndexSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="5a885-169">JET_bitIndexSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="5a885-170">Si se especifica esta marca, se ordenarán los valores <strong>null</strong> después de los datos de todas las columnas del índice.</span><span class="sxs-lookup"><span data-stu-id="5a885-170">Specifying this flag causes <strong>NULL</strong> values to be sorted after data for all columns in the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a885-171">JET_bitIndexUnicode</span><span class="sxs-lookup"><span data-stu-id="5a885-171">JET_bitIndexUnicode</span></span></p></td>
<td><p><span data-ttu-id="5a885-172">La especificación de esta marca afecta a la interpretación del campo de Unión LCID/pidxunicde en la estructura.</span><span class="sxs-lookup"><span data-stu-id="5a885-172">Specifying this flag affects the interpretation of the lcid/pidxunicde union field in the structure.</span></span> <span data-ttu-id="5a885-173">Establecer el bit significa que el campo <strong>pidxunicode</strong> apunta realmente a una estructura de <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> .</span><span class="sxs-lookup"><span data-stu-id="5a885-173">Setting the bit means that the <strong>pidxunicode</strong> field actually points to a <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure.</span></span> <span data-ttu-id="5a885-174">JET_bitIndexUnicode no es necesario para indizar los datos Unicode.</span><span class="sxs-lookup"><span data-stu-id="5a885-174">JET_bitIndexUnicode is not required in order to index Unicode data.</span></span> <span data-ttu-id="5a885-175">Solo se usa para personalizar la normalización de datos Unicode.</span><span class="sxs-lookup"><span data-stu-id="5a885-175">It is only used to customize the normalization of Unicode data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a885-176">JET_bitIndexTuples</span><span class="sxs-lookup"><span data-stu-id="5a885-176">JET_bitIndexTuples</span></span></p></td>
<td><p><span data-ttu-id="5a885-177">Especifica que el índice es un índice de tupla.</span><span class="sxs-lookup"><span data-stu-id="5a885-177">Specifies that the index is a tuple index.</span></span> <span data-ttu-id="5a885-178">Consulte <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> para obtener una descripción de un índice de tupla.</span><span class="sxs-lookup"><span data-stu-id="5a885-178">See <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> for a description of a tuple index.</span></span></p>
<p><span data-ttu-id="5a885-179">JET_bitIndexTuples se presentó en el sistema operativo Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5a885-179">JET_bitIndexTuples was introduced in the Windows XP operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a885-180">JET_bitIndexTupleLimits</span><span class="sxs-lookup"><span data-stu-id="5a885-180">JET_bitIndexTupleLimits</span></span></p></td>
<td><p><span data-ttu-id="5a885-181">La especificación de esta marca afecta a la interpretación del campo de Unión <strong>cbVarSegMac/ptuplelimits</strong> de la estructura.</span><span class="sxs-lookup"><span data-stu-id="5a885-181">Specifying this flag affects the interpretation of the <strong>cbVarSegMac/ptuplelimits</strong> union field in the structure.</span></span> <span data-ttu-id="5a885-182">Establecer este bit significa que el campo <strong>ptuplelimits</strong> apunta realmente a una estructura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> para permitir límites de índice de tupla personalizados (implica JET_bitIndexTuples).</span><span class="sxs-lookup"><span data-stu-id="5a885-182">Setting this bit means that the <strong>ptuplelimits</strong> field actually points to a <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure to allow custom tuple index limits (implies JET_bitIndexTuples).</span></span></p>
<p><span data-ttu-id="5a885-183">JET_bitIndexTupleLimits se presentó en el sistema operativo Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5a885-183">JET_bitIndexTupleLimits was introduced in the Windows Server 2003 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a885-184">JET_bitIndexCrossProduct 0x00004000</span><span class="sxs-lookup"><span data-stu-id="5a885-184">JET_bitIndexCrossProduct 0x00004000</span></span></p></td>
<td><p><span data-ttu-id="5a885-185">Si se especifica esta marca para un índice que tiene más de una columna de clave que es una columna de varios valores, se creará una entrada de índice para cada resultado de un producto cruzado de todos los valores de esas columnas de clave.</span><span class="sxs-lookup"><span data-stu-id="5a885-185">Specifying this flag for an index that has more than one key column that is a multivalued column will result in an index entry being created for each result of a cross product of all the values in those key columns.</span></span> <span data-ttu-id="5a885-186">De lo contrario, el índice solo tendrá una entrada para cada uno de los valores de la columna de clave más importante que sea una columna de varios valores y cada una de esas entradas de índice usaría el primer valor de varios de las demás columnas de clave que sean columnas de varios valores.</span><span class="sxs-lookup"><span data-stu-id="5a885-186">Otherwise, the index would only have one entry for each multivalue in the most significant key column that is a multivalued column and each of those index entries would use the first multivalue from any other key columns that are multivalued columns.</span></span></p>
<p><span data-ttu-id="5a885-187">Por ejemplo, si especificó esta marca para un índice en la columna A que tiene los valores &quot; rojo &quot; y &quot; azul &quot; y sobre la columna B que tiene los valores &quot; 1 &quot; y &quot; 2 &quot; , se crearán las siguientes entradas de índice: &quot; rojo &quot; , &quot; 1 &quot; ; &quot; rojo &quot; , &quot; 2 &quot; ; &quot; azul &quot; , &quot; 1 &quot; ; &quot; azul &quot; , &quot; 2 &quot; .</span><span class="sxs-lookup"><span data-stu-id="5a885-187">For example, if you specified this flag for an index over column A that has the values &quot;red&quot; and &quot;blue&quot; and over column B that has the values &quot;1&quot; and &quot;2&quot; then the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;red&quot;, &quot;2&quot;; &quot;blue&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;2&quot;.</span></span> <span data-ttu-id="5a885-188">De lo contrario, se crearán las siguientes entradas de índice: &quot; rojo &quot; , &quot; 1 &quot; ; &quot; azul &quot; , &quot; 1 &quot; .</span><span class="sxs-lookup"><span data-stu-id="5a885-188">Otherwise, the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;1&quot;.</span></span></p>
<p><span data-ttu-id="5a885-189">JET_bitIndexCrossProduct se presentó en el sistema operativo Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5a885-189">JET_bitIndexCrossProduct was introduced in the Windows Vista operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a885-190">JET_bitIndexKeyMost 0x00008000</span><span class="sxs-lookup"><span data-stu-id="5a885-190">JET_bitIndexKeyMost 0x00008000</span></span></p></td>
<td><p><span data-ttu-id="5a885-191">Si se especifica esta marca, el índice usará el tamaño de clave máximo especificado en el campo <strong>cbKeyMost</strong> de la estructura.</span><span class="sxs-lookup"><span data-stu-id="5a885-191">Specifying this flag will cause the index to use the maximum key size specified in the <strong>cbKeyMost</strong> field in the structure.</span></span> <span data-ttu-id="5a885-192">De lo contrario, el índice usará JET_cbKeyMost (255) como tamaño máximo de la clave.</span><span class="sxs-lookup"><span data-stu-id="5a885-192">Otherwise, the index will use JET_cbKeyMost (255) as its maximum key size.</span></span></p>
<p><span data-ttu-id="5a885-193">JET_bitIndexKeyMost se presentó en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5a885-193">JET_bitIndexKeyMost was introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a885-194">JET_bitIndexDisallowTruncation 0x00010000</span><span class="sxs-lookup"><span data-stu-id="5a885-194">JET_bitIndexDisallowTruncation 0x00010000</span></span></p></td>
<td><p><span data-ttu-id="5a885-195">Si se especifica este marcador, se producirá un error en cualquier actualización del índice que dé lugar a una clave truncada con JET_errKeyTruncated.</span><span class="sxs-lookup"><span data-stu-id="5a885-195">Specifying this flag will cause any update to the index that would result in a truncated key to fail with JET_errKeyTruncated.</span></span> <span data-ttu-id="5a885-196">De lo contrario, las claves se truncarán de forma silenciosa.</span><span class="sxs-lookup"><span data-stu-id="5a885-196">Otherwise, keys will be silently truncated.</span></span> <span data-ttu-id="5a885-197">Para obtener más información sobre el truncamiento de claves, vea la función <a href="gg269329(v=exchg.10).md">JetMakeKey</a> .</span><span class="sxs-lookup"><span data-stu-id="5a885-197">For more information on key truncation, see the <a href="gg269329(v=exchg.10).md">JetMakeKey</a> function.</span></span></p>
<p><span data-ttu-id="5a885-198"><strong>Windows Vista: JET_bitIndexDisallowTruncation</strong> se incorpora en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5a885-198"><strong>Windows Vista:  JET_bitIndexDisallowTruncation</strong> is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a885-199">JET_bitIndexNestedTable 0x00020000</span><span class="sxs-lookup"><span data-stu-id="5a885-199">JET_bitIndexNestedTable 0x00020000</span></span></p></td>
<td><p><span data-ttu-id="5a885-200">Si se especifica esta marca, se actualizará el índice en varias columnas con varios valores, pero solo con valores de la misma <strong>itagSequence</strong>.</span><span class="sxs-lookup"><span data-stu-id="5a885-200">Specifying this flag will cause update the index over multiple multivalued columns but only with values of same <strong>itagSequence</strong>.</span></span></p>
<p><span data-ttu-id="5a885-201">JET_bitIndexNestedTable se presentó en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5a885-201">JET_bitIndexNestedTable was introduced in Windows Vista.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5a885-202">**ulDensity**</span><span class="sxs-lookup"><span data-stu-id="5a885-202">**ulDensity**</span></span>

<span data-ttu-id="5a885-203">Densidad porcentual del árbol B + del índice inicial.</span><span class="sxs-lookup"><span data-stu-id="5a885-203">The percentage density of the initial index B+ tree.</span></span> <span data-ttu-id="5a885-204">Si se especifica un número menor que 100, se usa más espacio para crear el índice inicialmente, pero se permite el crecimiento futuro del índice, lo que evita la fragmentación interna.</span><span class="sxs-lookup"><span data-stu-id="5a885-204">Specifying a number less than 100 uses up more space to create the index initially, but allows future growth of the index to be in place, thus avoiding internal fragmentation.</span></span>

<span data-ttu-id="5a885-205">**lcid**</span><span class="sxs-lookup"><span data-stu-id="5a885-205">**lcid**</span></span>

<span data-ttu-id="5a885-206">Identificador de configuración regional (LCID) que se va a usar al normalizar los datos cuando el valor de JET_bitIndexUnicode no se especifica en el parámetro *grbit* .</span><span class="sxs-lookup"><span data-stu-id="5a885-206">The locale identifier (LCID) to use when normalizing the data when the JET_bitIndexUnicode value is not specified in the *grbit* parameter.</span></span> <span data-ttu-id="5a885-207">El LCID afecta a la normalización si el índice está en columnas Unicode.</span><span class="sxs-lookup"><span data-stu-id="5a885-207">The LCID affects the normalization if the index is over Unicode columns.</span></span>

<span data-ttu-id="5a885-208">**pidxunicode**</span><span class="sxs-lookup"><span data-stu-id="5a885-208">**pidxunicode**</span></span>

<span data-ttu-id="5a885-209">Puntero a una estructura de [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) si el valor de JET_bitIndexUnicode se especifica en el parámetro *grbit* .</span><span class="sxs-lookup"><span data-stu-id="5a885-209">A pointer to a [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) structure if the JET_bitIndexUnicode value is specified in the *grbit* parameter.</span></span> <span data-ttu-id="5a885-210">Esto permite al usuario especificar las marcas personalizadas que se pasan a la función [LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) durante la normalización Unicode.</span><span class="sxs-lookup"><span data-stu-id="5a885-210">This allows the user to specify custom flags that get passed to the [LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) function during Unicode normalization.</span></span>

<span data-ttu-id="5a885-211">**cbVarSegMac**</span><span class="sxs-lookup"><span data-stu-id="5a885-211">**cbVarSegMac**</span></span>

<span data-ttu-id="5a885-212">Longitud máxima, en bytes, de cada columna que se va a almacenar en el índice cuando el valor de JET_bitIndexTupleLimits no se especifica en el parámetro *grbit* .</span><span class="sxs-lookup"><span data-stu-id="5a885-212">The maximum length, in bytes, of each column to store in the index when the JET_bitIndexTupleLimits value is not specified in the *grbit* parameter.</span></span>

<span data-ttu-id="5a885-213">Especificar un valor de 0 (cero) para este campo es equivalente a:</span><span class="sxs-lookup"><span data-stu-id="5a885-213">Specifying a value of 0 (zero) for this field is equivalent to:</span></span>

  - <span data-ttu-id="5a885-214">Especificar JET_cbPrimaryKeyMost para un índice principal.</span><span class="sxs-lookup"><span data-stu-id="5a885-214">Specifying JET_cbPrimaryKeyMost for a primary index.</span></span>

  - <span data-ttu-id="5a885-215">Especificar JET_cbSecondaryKeyMost para un índice secundario.</span><span class="sxs-lookup"><span data-stu-id="5a885-215">Specifying JET_cbSecondaryKeyMost for a secondary index.</span></span>

<span data-ttu-id="5a885-216">**ptuplelimits**</span><span class="sxs-lookup"><span data-stu-id="5a885-216">**ptuplelimits**</span></span>

<span data-ttu-id="5a885-217">Puntero a una estructura de [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) si el valor de JET_bitIndexTupleLimits se especifica en el parámetro *grbit* .</span><span class="sxs-lookup"><span data-stu-id="5a885-217">A pointer to a [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure if the JET_bitIndexTupleLimits value is specified in the *grbit* parameter.</span></span>

<span data-ttu-id="5a885-218">ptuplelimits se presentó en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5a885-218">ptuplelimits was introduced in Windows Server 2003.</span></span>

<span data-ttu-id="5a885-219">**rgconditionalcolumn**</span><span class="sxs-lookup"><span data-stu-id="5a885-219">**rgconditionalcolumn**</span></span>

<span data-ttu-id="5a885-220">Un parámetro opcional para una matriz de estructuras [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) , que se usan para especificar las columnas condicionales en el índice.</span><span class="sxs-lookup"><span data-stu-id="5a885-220">An optional parameter to an array of [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) structures, which are used to specify the conditional columns in the index.</span></span>

<span data-ttu-id="5a885-221">**cConditionalColumn**</span><span class="sxs-lookup"><span data-stu-id="5a885-221">**cConditionalColumn**</span></span>

<span data-ttu-id="5a885-222">Recuento de estructuras de la matriz **rgconditionalcolumn** .</span><span class="sxs-lookup"><span data-stu-id="5a885-222">The count of structures in the **rgconditionalcolumn** array.</span></span>

<span data-ttu-id="5a885-223">**ERR**</span><span class="sxs-lookup"><span data-stu-id="5a885-223">**err**</span></span>

<span data-ttu-id="5a885-224">Contiene el código de retorno para crear este índice.</span><span class="sxs-lookup"><span data-stu-id="5a885-224">Contains the return code for creating this index.</span></span>

<span data-ttu-id="5a885-225">**cbKeyMost**</span><span class="sxs-lookup"><span data-stu-id="5a885-225">**cbKeyMost**</span></span>

<span data-ttu-id="5a885-226">Especifica el tamaño máximo permitido, en bytes, para las claves del índice.</span><span class="sxs-lookup"><span data-stu-id="5a885-226">Specifies the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="5a885-227">Este parámetro se omite si el valor de JET_bitIndexKeyMost no se especifica en el parámetro *grbit* .</span><span class="sxs-lookup"><span data-stu-id="5a885-227">This parameter is ignored if the JET_bitIndexKeyMost value is not specified in the *grbit* parameter.</span></span> <span data-ttu-id="5a885-228">Si este parámetro se establece en cero y se especifica JET_bitIndexKeyMost en el parámetro *grbit* , se producirá un error en la función de llamada con JET_err_InvalidDef.</span><span class="sxs-lookup"><span data-stu-id="5a885-228">If this parameter is set to zero, and JET_bitIndexKeyMost is specified in the *grbit* parameter, the calling function will fail with JET_err_InvalidDef.</span></span>

<span data-ttu-id="5a885-229">El tamaño máximo de clave compatible mínimo es JET_cbKeyMostMin (255), que es el tamaño de clave máximo heredado.</span><span class="sxs-lookup"><span data-stu-id="5a885-229">The minimum supported maximum key size is JET_cbKeyMostMin (255), which is the legacy maximum key size.</span></span>

<span data-ttu-id="5a885-230">El tamaño máximo de la clave depende del tamaño de página de la base de datos (JET_paramDatabasePageSize), como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="5a885-230">The maximum key size is dependent on the database page size (JET_paramDatabasePageSize), as follows:</span></span>

  - <span data-ttu-id="5a885-231">Si JET_paramDatabasePageSize = 2048, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost2KBytePage (500)</span><span class="sxs-lookup"><span data-stu-id="5a885-231">If JET_paramDatabasePageSize = 2048 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost2KBytePage (500)</span></span>

  - <span data-ttu-id="5a885-232">Si JET_paramDatabasePageSize = 4096, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost4KBytePage (1000)</span><span class="sxs-lookup"><span data-stu-id="5a885-232">If JET_paramDatabasePageSize = 4096 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost4KBytePage (1000)</span></span>

  - <span data-ttu-id="5a885-233">Si JET_paramDatabasePageSize = 8192, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost8KBytePage (2000)</span><span class="sxs-lookup"><span data-stu-id="5a885-233">If JET_paramDatabasePageSize = 8192 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost8KBytePage (2000)</span></span>

<span data-ttu-id="5a885-234">También se puede leer el tamaño máximo admitido para la instancia en el parámetro del sistema JET_paramKeyMost.</span><span class="sxs-lookup"><span data-stu-id="5a885-234">The maximum supported key size for the instance can also be read from the JET_paramKeyMost system parameter.</span></span>

<span data-ttu-id="5a885-235">**cbKeyMost** se presentó en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5a885-235">**cbKeyMost** was introduced in Windows Vista.</span></span>

### <a name="remarks"></a><span data-ttu-id="5a885-236">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5a885-236">Remarks</span></span>

<span data-ttu-id="5a885-237">ESE admite la indización de columnas de clave que contienen varios valores.</span><span class="sxs-lookup"><span data-stu-id="5a885-237">ESE supports indexing over key columns containing multiple values.</span></span> <span data-ttu-id="5a885-238">Para usar esta característica, la columna debe ser un tipo de columna etiquetado (JET_bitColumnTagged) y se debe marcar para que sus múltiples valores se indexen con JET_bitColumnMultiValued.</span><span class="sxs-lookup"><span data-stu-id="5a885-238">To use this feature, the column must be a tagged column type (JET_bitColumnTagged), and it must be flagged to have its multiple values indexed with JET_bitColumnMultiValued.</span></span> <span data-ttu-id="5a885-239">En las versiones de Windows anteriores a Windows Vista, solo se expandirá su valor en el índice de la primera columna de clave con varios valores del índice.</span><span class="sxs-lookup"><span data-stu-id="5a885-239">In versions of Windows earlier than Windows Vista, only the first multivalued key column in the index will have its values expanded in the index.</span></span> <span data-ttu-id="5a885-240">Todas las demás columnas con varios valores y etiquetas solo tendrán sus primeros valores expandidos en el índice.</span><span class="sxs-lookup"><span data-stu-id="5a885-240">All other multivalued and tagged columns will only have their first values expanded in the index.</span></span>

<span data-ttu-id="5a885-241">Suponiendo que las filas siguientes existen en una tabla (la columna alfa no tiene varios valores, mientras que las columnas beta, gamma y delta tienen varios valores) y se crea un índice como "+ alpha \\ 0 + beta \\ 0 + gamma \\ 0 + Delta \\ 0 \\ 0":</span><span class="sxs-lookup"><span data-stu-id="5a885-241">Assuming the following rows exist in a table (column Alpha is not multivalued, while columns Beta, Gamma, and Delta are multivalued), and an index is created as "+Alpha\\0+Beta\\0+Gamma\\0+Delta\\0\\0":</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5a885-242">Alpha</span><span class="sxs-lookup"><span data-stu-id="5a885-242">Alpha</span></span></p></th>
<th><p><span data-ttu-id="5a885-243">Beta</span><span class="sxs-lookup"><span data-stu-id="5a885-243">Beta</span></span></p></th>
<th><p><span data-ttu-id="5a885-244">Gamma</span><span class="sxs-lookup"><span data-stu-id="5a885-244">Gamma</span></span></p></th>
<th><p><span data-ttu-id="5a885-245">Delta</span><span class="sxs-lookup"><span data-stu-id="5a885-245">Delta</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a885-246">1</span><span class="sxs-lookup"><span data-stu-id="5a885-246">1</span></span></p></td>
<td><p><span data-ttu-id="5a885-247">ABC</span><span class="sxs-lookup"><span data-stu-id="5a885-247">ABC</span></span><br />
<span data-ttu-id="5a885-248">GHI</span><span class="sxs-lookup"><span data-stu-id="5a885-248">GHI</span></span><br />
<span data-ttu-id="5a885-249">JKL</span><span class="sxs-lookup"><span data-stu-id="5a885-249">JKL</span></span></p></td>
<td><p><span data-ttu-id="5a885-250">MNO</span><span class="sxs-lookup"><span data-stu-id="5a885-250">MNO</span></span><br />
<span data-ttu-id="5a885-251">PQR</span><span class="sxs-lookup"><span data-stu-id="5a885-251">PQR</span></span><br />
<span data-ttu-id="5a885-252">STU</span><span class="sxs-lookup"><span data-stu-id="5a885-252">STU</span></span></p></td>
<td><p><span data-ttu-id="5a885-253">VWX</span><span class="sxs-lookup"><span data-stu-id="5a885-253">VWX</span></span><br />
<span data-ttu-id="5a885-254">YZ</span><span class="sxs-lookup"><span data-stu-id="5a885-254">YZ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a885-255">2</span><span class="sxs-lookup"><span data-stu-id="5a885-255">2</span></span></p></td>
<td><p><span data-ttu-id="5a885-256">EL</span><span class="sxs-lookup"><span data-stu-id="5a885-256">THE</span></span></p></td>
<td><p><span data-ttu-id="5a885-257">LLUVIA</span><span class="sxs-lookup"><span data-stu-id="5a885-257">RAIN</span></span><br />
<span data-ttu-id="5a885-258">España</span><span class="sxs-lookup"><span data-stu-id="5a885-258">SPAIN</span></span></p></td>
<td><p><span data-ttu-id="5a885-259">IN</span><span class="sxs-lookup"><span data-stu-id="5a885-259">IN</span></span><br />
<span data-ttu-id="5a885-260">PASÓ</span><span class="sxs-lookup"><span data-stu-id="5a885-260">FALLS</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5a885-261">Se almacenarán las tuplas de índice en caída:</span><span class="sxs-lookup"><span data-stu-id="5a885-261">The falling index-tuples will be stored:</span></span>

<span data-ttu-id="5a885-262">{1, ABC, MNO, VWX}</span><span class="sxs-lookup"><span data-stu-id="5a885-262">{1,ABC,MNO,VWX}</span></span>  
<span data-ttu-id="5a885-263">{1, GHI, MNO, VWX}</span><span class="sxs-lookup"><span data-stu-id="5a885-263">{1,GHI,MNO,VWX}</span></span>  
<span data-ttu-id="5a885-264">{1, JKL, MNO, VWX}</span><span class="sxs-lookup"><span data-stu-id="5a885-264">{1,JKL,MNO,VWX}</span></span>  
<span data-ttu-id="5a885-265">{2,, RAIN, IN}</span><span class="sxs-lookup"><span data-stu-id="5a885-265">{2,THE,RAIN,IN}</span></span>

<span data-ttu-id="5a885-266">Tenga en cuenta que {2,, España, IN} no se almacena, aunque la columna alfa de la segunda fila tenga un solo multivalor.</span><span class="sxs-lookup"><span data-stu-id="5a885-266">Note that {2,THE,SPAIN,IN} is not stored, even though the Alpha column in the second row happens to have a single multivalue.</span></span>

<span data-ttu-id="5a885-267">En las versiones de Windows a partir de Windows Vista, todas las columnas con varios valores se pueden expandir en el índice especificando JET_bitIndexCrossProduct.</span><span class="sxs-lookup"><span data-stu-id="5a885-267">In versions of Windows starting with Windows Vista, all multivalued columns can be expanded in the index by specifying JET_bitIndexCrossProduct.</span></span>

### <a name="requirements"></a><span data-ttu-id="5a885-268">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a885-268">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a885-269"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="5a885-269"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5a885-270">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="5a885-270">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a885-271"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="5a885-271"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5a885-272">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5a885-272">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a885-273"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="5a885-273"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5a885-274">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="5a885-274">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a885-275"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="5a885-275"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="5a885-276">Se implementa como <strong>JET_ INDEXCREATE_W</strong> (Unicode) y <strong>JET_ INDEXCREATE_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="5a885-276">Implemented as <strong>JET_ INDEXCREATE_W</strong> (Unicode) and <strong>JET_ INDEXCREATE_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="5a885-277">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a885-277">See also</span></span>

[<span data-ttu-id="5a885-278">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="5a885-278">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="5a885-279">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="5a885-279">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="5a885-280">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5a885-280">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5a885-281">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="5a885-281">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="5a885-282">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="5a885-282">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="5a885-283">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="5a885-283">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="5a885-284">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="5a885-284">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="5a885-285">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="5a885-285">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="5a885-286">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="5a885-286">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="5a885-287">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="5a885-287">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="5a885-288">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="5a885-288">JetUpdate</span></span>](./jetupdate-function.md)
