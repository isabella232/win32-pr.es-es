---
description: 'Más información acerca de: JetAddColumn (función)'
title: Función JetAddColumn
TOCTitle: JetAddColumn Function
ms:assetid: e146f784-2cbd-42c0-bf64-b37dc6f9ee43
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294122(v=EXCHG.10)
ms:contentKeyID: 32765736
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAddColumnW
- JetAddColumnA
- JetAddColumn
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1b8c3eac113daeae43ec4a8e62b7fcda9ddbf9f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720670"
---
# <a name="jetaddcolumn-function"></a><span data-ttu-id="53901-103">Función JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="53901-103">JetAddColumn Function</span></span>


<span data-ttu-id="53901-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="53901-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetaddcolumn-function"></a><span data-ttu-id="53901-105">Función JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="53901-105">JetAddColumn Function</span></span>

<span data-ttu-id="53901-106">La función **JetAddColumn** agrega una nueva columna a una tabla existente en una base de datos ese.</span><span class="sxs-lookup"><span data-stu-id="53901-106">The **JetAddColumn** function adds a new column to an existing table in an ESE database.</span></span>

```cpp
    JET_ERR JET_API JetAddColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szColumnName,
      __in          const JET_COLUMNDEF* pcolumndef,
      __in_opt      const void* pvDefault,
      __in          unsigned long cbDefault,
      __out_opt     JET_COLUMNID* pcolumnid
    );
```

### <a name="parameters"></a><span data-ttu-id="53901-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="53901-107">Parameters</span></span>

<span data-ttu-id="53901-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="53901-108">*sesid*</span></span>

<span data-ttu-id="53901-109">Contexto de sesión de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="53901-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="53901-110">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="53901-110">*tableid*</span></span>

<span data-ttu-id="53901-111">Tabla a la que se va a agregar la columna.</span><span class="sxs-lookup"><span data-stu-id="53901-111">The table to which to add the column.</span></span>

<span data-ttu-id="53901-112">*szColumnName*</span><span class="sxs-lookup"><span data-stu-id="53901-112">*szColumnName*</span></span>

<span data-ttu-id="53901-113">Nombre de la columna que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="53901-113">The name of the column to add.</span></span> <span data-ttu-id="53901-114">El nombre debe cumplir los siguientes criterios:</span><span class="sxs-lookup"><span data-stu-id="53901-114">The name must meet the following criteria:</span></span>

  - <span data-ttu-id="53901-115">Debe tener menos de JET_cbNameMost caracteres de longitud, sin incluir el carácter **null** de terminación.</span><span class="sxs-lookup"><span data-stu-id="53901-115">It must be fewer than JET_cbNameMost characters in length, not including the terminating **NULL**.</span></span>

  - <span data-ttu-id="53901-116">Solo debe contener caracteres de los siguientes conjuntos: de 0 a 9, de la a a la Z, de la a a la z y de todos los demás signos de puntuación, excepto el signo de exclamación ( \! ), la coma (,), el corchete de apertura () y el \[ corchete de cierre ( \] ), es decir, los caracteres ASCII 0x20, 0x22 a</span><span class="sxs-lookup"><span data-stu-id="53901-116">It must contain characters only from the following sets: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]) — that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="53901-117">No puede comenzar con un espacio.</span><span class="sxs-lookup"><span data-stu-id="53901-117">It cannot begin with a space.</span></span>

  - <span data-ttu-id="53901-118">Debe contener al menos un carácter que no sea un espacio.</span><span class="sxs-lookup"><span data-stu-id="53901-118">It must contain at least one non-space character.</span></span>

<span data-ttu-id="53901-119">*pcolumndef*</span><span class="sxs-lookup"><span data-stu-id="53901-119">*pcolumndef*</span></span>

<span data-ttu-id="53901-120">Puntero a una estructura de [JET_COLUMNDEF](./jet-columndef-structure.md) , que define los datos que se pueden almacenar en una columna.</span><span class="sxs-lookup"><span data-stu-id="53901-120">A pointer to a [JET_COLUMNDEF](./jet-columndef-structure.md) structure, which defines the data that can be stored in a column.</span></span>

<span data-ttu-id="53901-121">*pvDefault*</span><span class="sxs-lookup"><span data-stu-id="53901-121">*pvDefault*</span></span>

<span data-ttu-id="53901-122">Un puntero a un búfer que contiene el valor predeterminado de la columna.</span><span class="sxs-lookup"><span data-stu-id="53901-122">A pointer to a buffer that contains the default value for the column.</span></span> <span data-ttu-id="53901-123">La longitud del búfer es **cbDefault**.</span><span class="sxs-lookup"><span data-stu-id="53901-123">The length of the buffer is **cbDefault**.</span></span> <span data-ttu-id="53901-124">Si no hay ningún valor predeterminado, establezca **pvDefault** en **null** y **cbDefault** en cero.</span><span class="sxs-lookup"><span data-stu-id="53901-124">If there is no default, set **pvDefault** to **NULL** and **cbDefault** to zero.</span></span> <span data-ttu-id="53901-125">Los valores predeterminados no pueden ser mayores que JET_cbColumnMost bytes para las columnas fijas o JET_cbLVDefaultValueMost bytes para valores largos.</span><span class="sxs-lookup"><span data-stu-id="53901-125">Default values cannot be larger than JET_cbColumnMost bytes for fixed columns or JET_cbLVDefaultValueMost bytes for long values.</span></span> <span data-ttu-id="53901-126">Si un valor predeterminado es mayor que, se truncará en modo silencioso.</span><span class="sxs-lookup"><span data-stu-id="53901-126">If a default value is larger than that, it will be silently truncated.</span></span>

<span data-ttu-id="53901-127">Si *grbit* ha establecido JET_bitColumnUserDefinedDefault, **pvDefault** se interpretará como un puntero a una estructura de [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="53901-127">If *grbit* has JET_bitColumnUserDefinedDefault set, **pvDefault** will be interpreted as a pointer to a [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) structure.</span></span>

<span data-ttu-id="53901-128">*cbDefault*</span><span class="sxs-lookup"><span data-stu-id="53901-128">*cbDefault*</span></span>

<span data-ttu-id="53901-129">Tamaño, en bytes, del búfer que se especifica en **pvDefault**.</span><span class="sxs-lookup"><span data-stu-id="53901-129">The size, in bytes, of the buffer that is specified in **pvDefault**.</span></span>

<span data-ttu-id="53901-130">*pcolumnid*</span><span class="sxs-lookup"><span data-stu-id="53901-130">*pcolumnid*</span></span>

<span data-ttu-id="53901-131">Puntero a una estructura de [JET_COLUMNID](./jet-columnid.md) , que, si se ejecuta correctamente, recibirá el identificador de la columna recién creada.</span><span class="sxs-lookup"><span data-stu-id="53901-131">A pointer to a [JET_COLUMNID](./jet-columnid.md) structure, which, on success, will receive the identifier of the newly created column.</span></span> <span data-ttu-id="53901-132">En caso de error, el valor es indefinido.</span><span class="sxs-lookup"><span data-stu-id="53901-132">On failure, the value is undefined.</span></span>

### <a name="return-value"></a><span data-ttu-id="53901-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53901-133">Return Value</span></span>

<span data-ttu-id="53901-134">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="53901-134">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="53901-135">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="53901-135">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="53901-136">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="53901-136">Return code</span></span></p></th>
<th><p><span data-ttu-id="53901-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="53901-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53901-138">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="53901-138">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="53901-139">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="53901-139">The operation was successful.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53901-140">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="53901-140">JET_errFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="53901-141">Se intentó modificar la definición de datos de una tabla de DDL fija.</span><span class="sxs-lookup"><span data-stu-id="53901-141">An attempt was made to modify the data definition of a fixed DDL table.</span></span> <span data-ttu-id="53901-142">Un ejemplo de una tabla con DDL fijos es una tabla de plantillas.</span><span class="sxs-lookup"><span data-stu-id="53901-142">An example of a table with fixed DDL is a Template Table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53901-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="53901-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="53901-144">Se pasó un parámetro no válido a la API.</span><span class="sxs-lookup"><span data-stu-id="53901-144">An invalid parameter was passed into the API.</span></span> <span data-ttu-id="53901-145">Algunos ejemplos de parámetros no válidos son:</span><span class="sxs-lookup"><span data-stu-id="53901-145">Some examples of invalid parameters are:</span></span></p>
<ul>
<li><p><span data-ttu-id="53901-146">Se pasa el tamaño incorrecto de la estructura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> en su miembro <em>cbStruct</em> .</span><span class="sxs-lookup"><span data-stu-id="53901-146">Passing in the wrong size of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure in its <em>cbStruct</em> member.</span></span></p></li>
<li><p><span data-ttu-id="53901-147">Pasar JET_bitColumnUserDefinedDefault, pero no establecer <strong>cbDefault</strong> en sizeof (<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</span><span class="sxs-lookup"><span data-stu-id="53901-147">Passing in JET_bitColumnUserDefinedDefault, but not setting <strong>cbDefault</strong> to sizeof(<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53901-148">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="53901-148">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="53901-149">Se intentó agregar una columna con el conjunto de JET_bitColumnUnversioned bits, pero la sesión se encuentra actualmente en una transacción.</span><span class="sxs-lookup"><span data-stu-id="53901-149">An attempt was made to add a column with the JET_bitColumnUnversioned bit set, but the session is currently in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53901-150">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="53901-150">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="53901-151">Ya existe una columna.</span><span class="sxs-lookup"><span data-stu-id="53901-151">A column already exists.</span></span> <span data-ttu-id="53901-152">Se intentó agregar una columna sin información de versión y esa columna ya existe.</span><span class="sxs-lookup"><span data-stu-id="53901-152">An attempt was made to add a column without version information, and that column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53901-153">JET_errTableNotEmpty</span><span class="sxs-lookup"><span data-stu-id="53901-153">JET_errTableNotEmpty</span></span></p></td>
<td><p><span data-ttu-id="53901-154">La tabla contiene datos.</span><span class="sxs-lookup"><span data-stu-id="53901-154">The table contains data.</span></span> <span data-ttu-id="53901-155">Una columna de actualización de custodia solo puede agregarse a una tabla vacía.</span><span class="sxs-lookup"><span data-stu-id="53901-155">An Escrow Update column can only be added to an empty table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53901-156">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="53901-156">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="53901-157">El registro es demasiado grande.</span><span class="sxs-lookup"><span data-stu-id="53901-157">The record is too big.</span></span> <span data-ttu-id="53901-158">La suma del parámetro <strong>cbMax</strong> para las columnas fijas no debe superar un valor determinado.</span><span class="sxs-lookup"><span data-stu-id="53901-158">The sum of the <strong>cbMax</strong> parameter for the fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53901-159">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="53901-159">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="53901-160">Se intentó agregar demasiadas columnas a la tabla.</span><span class="sxs-lookup"><span data-stu-id="53901-160">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="53901-161">Una tabla no puede tener más de JET_ccolFixedMost columnas fijas, ni más de JET_ccolVarMost columnas de longitud variable, ni más de JET_ccolTaggedMost columnas etiquetadas.</span><span class="sxs-lookup"><span data-stu-id="53901-161">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53901-162">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="53901-162">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="53901-163">Se intentó agregar una columna redundante.</span><span class="sxs-lookup"><span data-stu-id="53901-163">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="53901-164">No debe haber más de una columna de incremento automático y no más de una columna de versión por tabla.</span><span class="sxs-lookup"><span data-stu-id="53901-164">There should be no more than one autoincrement column, and no more than one version column per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53901-165">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="53901-165">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="53901-166">No se pudo resolver la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="53901-166">The callback function could not be resolved.</span></span> <span data-ttu-id="53901-167">Es posible que no se haya encontrado el archivo DLL o que no se haya encontrado la función del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="53901-167">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="53901-168">El registro de eventos proporcionará más detalles si está habilitado el registro suficiente.</span><span class="sxs-lookup"><span data-stu-id="53901-168">The event log will provide more details if sufficient logging is enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53901-169">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="53901-169">JET_wrnColumnMaxTruncated</span></span></p></td>
<td><p><span data-ttu-id="53901-170">ADVERTENCIA que indica que la longitud máxima (<strong>cbMax</strong>) de una columna fija o de variable era mayor que JET_cbColumnMost.</span><span class="sxs-lookup"><span data-stu-id="53901-170">A warning indicating that the maximum length (<strong>cbMax</strong>) of a fixed or variable column was greater than JET_cbColumnMost.</span></span> <span data-ttu-id="53901-171">Este límite no se aplica a los valores largos (es decir <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> y <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span><span class="sxs-lookup"><span data-stu-id="53901-171">This limit does not apply to Long Values (that is <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> and <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53901-172">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="53901-172">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="53901-173">Se pasó un nombre no válido como <strong>szColumnName</strong>.</span><span class="sxs-lookup"><span data-stu-id="53901-173">An invalid name was passed as <strong>szColumnName</strong>.</span></span> <span data-ttu-id="53901-174">Para obtener más información sobre las restricciones, vea los criterios de <strong>szColumnName</strong>.</span><span class="sxs-lookup"><span data-stu-id="53901-174">For more information about the restrictions, see the criteria for <strong>szColumnName</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53901-175">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="53901-175">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="53901-176">El campo <strong>coltyp</strong> no se estableció en un tipo de columna válido.</span><span class="sxs-lookup"><span data-stu-id="53901-176">The <strong>coltyp</strong> field was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53901-177">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="53901-177">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="53901-178">El parámetro <strong>CP</strong> de la estructura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> no se estableció en una página de códigos válida.</span><span class="sxs-lookup"><span data-stu-id="53901-178">The <strong>cp</strong> parameter of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="53901-179">Los únicos valores válidos para las columnas de texto son inglés (1252) y Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="53901-179">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="53901-180">Un valor de 0 significa que se usará el valor predeterminado (Inglés, 1252).</span><span class="sxs-lookup"><span data-stu-id="53901-180">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53901-181">JET_errTaggedNotNULL</span><span class="sxs-lookup"><span data-stu-id="53901-181">JET_errTaggedNotNULL</span></span></p></td>
<td><p><span data-ttu-id="53901-182">No se puede usar JET_bitColumnNotNULL con columnas etiquetadas, de valor Long o de SLV.</span><span class="sxs-lookup"><span data-stu-id="53901-182">JET_bitColumnNotNULL cannot be used with tagged, Long Value, or SLV columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53901-183">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="53901-183">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="53901-184">Se especificó una combinación no válida de <em>grbits</em> .</span><span class="sxs-lookup"><span data-stu-id="53901-184">An invalid combination of <em>grbits</em> was specified.</span></span> <span data-ttu-id="53901-185">Algunos de los motivos de este error son:</span><span class="sxs-lookup"><span data-stu-id="53901-185">Some of the reasons for this error are:</span></span></p>
<ul>
<li><p><span data-ttu-id="53901-186">JET_bitColumnFixed se usó en una columna etiquetada, un valor largo o SLV.</span><span class="sxs-lookup"><span data-stu-id="53901-186">JET_bitColumnFixed was used on a tagged, Long Value, or SLV column.</span></span></p></li>
<li><p><span data-ttu-id="53901-187">JET_bitColumnEscrowUpdate se usó en una columna que no era de tipo <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span><span class="sxs-lookup"><span data-stu-id="53901-187">JET_bitColumnEscrowUpdate was used on a column that was not of type <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span></span></p></li>
<li><p><span data-ttu-id="53901-188">JET_bitColumnEscrowUpdate se usó en una columna de versión (JET_bitColumnVersion).</span><span class="sxs-lookup"><span data-stu-id="53901-188">JET_bitColumnEscrowUpdate was used on a Version column (JET_bitColumnVersion).</span></span></p></li>
<li><p><span data-ttu-id="53901-189">JET_bitColumnEscrowUpdate se usó en una columna AutoIncrememnt (JET_bitColumnAutoincrement).</span><span class="sxs-lookup"><span data-stu-id="53901-189">JET_bitColumnEscrowUpdate was used on an AutoIncrememnt column (JET_bitColumnAutoincrement).</span></span></p></li>
<li><p><span data-ttu-id="53901-190">JET_bitColumnEscrowUpdate se usó en una columna que no tenía un valor predeterminado (<strong>cbDefault</strong> era igual a cero).</span><span class="sxs-lookup"><span data-stu-id="53901-190">JET_bitColumnEscrowUpdate was used on a column that did not have a default value (<strong>cbDefault</strong> was equal to zero).</span></span></p></li>
<li><p><span data-ttu-id="53901-191">JET_bitColumnFinalize se usó en una columna que no era una columna de actualización de custodia (no se estableció JET_bitColumnEscrowUpdate).</span><span class="sxs-lookup"><span data-stu-id="53901-191">JET_bitColumnFinalize was used on a column that was not an Escrow Update column (JET_bitColumnEscrowUpdate was not set).</span></span></p></li>
<li><p><span data-ttu-id="53901-192">JET_bitColumnDeleteOnZero se usó en una columna que no era una columna de actualización de custodia (no se estableció JET_bitColumnEscrowUpdate).</span><span class="sxs-lookup"><span data-stu-id="53901-192">JET_bitColumnDeleteOnZero was used on a column that was not an Escrow Update column (JET_bitColumnEscrowUpdate was not set).</span></span></p></li>
<li><p><span data-ttu-id="53901-193">JET_bitColumnAutoincrement se usó en una columna que no se <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span><span class="sxs-lookup"><span data-stu-id="53901-193">JET_bitColumnAutoincrement was used on a column that was not <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span></span></p>
<p><span data-ttu-id="53901-194"><strong>Windows 2000:  </strong> Este motivo del código de error solo se utiliza en Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="53901-194"><strong>Windows 2000:  </strong>This reason for the error code is used only in Windows 2000.</span></span></p>
<p><span data-ttu-id="53901-195">JET_bitColumnAutoincrement se usó en una columna que no era <a href="gg269213(v=exchg.10).md">JET_coltypLong</a> ni <a href="gg269213(v=exchg.10).md">JET_coltypCurrency</a>.</span><span class="sxs-lookup"><span data-stu-id="53901-195">JET_bitColumnAutoincrement was used on a column that was neither <a href="gg269213(v=exchg.10).md">JET_coltypLong</a> nor <a href="gg269213(v=exchg.10).md">JET_coltypCurrency</a>.</span></span></p>
<p><span data-ttu-id="53901-196"><strong>Windows XP:  </strong> Este motivo del código de error se utiliza en Windows XP y en los sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="53901-196"><strong>Windows XP:  </strong>This reason for the error code is used in Windows XP and later operating systems.</span></span></p></li>
<li><p><span data-ttu-id="53901-197">JET_bitColumnVersion se usó en una columna que no se <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span><span class="sxs-lookup"><span data-stu-id="53901-197">JET_bitColumnVersion was used on a column that was not <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span></span></p></li>
<li><p><span data-ttu-id="53901-198">JET_bitColumnVersion se usó en una columna de incremento automático.</span><span class="sxs-lookup"><span data-stu-id="53901-198">JET_bitColumnVersion was used on an autoincrement column.</span></span></p></li>
<li><p><span data-ttu-id="53901-199">JET_bitColumnUserDefinedDefault se usó junto con JET_bitColumnFixed.</span><span class="sxs-lookup"><span data-stu-id="53901-199">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnFixed.</span></span></p></li>
<li><p><span data-ttu-id="53901-200">JET_bitColumnUserDefinedDefault se usó junto con JET_bitColumnNotNULL.</span><span class="sxs-lookup"><span data-stu-id="53901-200">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnNotNULL.</span></span></p></li>
<li><p><span data-ttu-id="53901-201">JET_bitColumnUserDefinedDefault se usó junto con JET_bitColumnVersion.</span><span class="sxs-lookup"><span data-stu-id="53901-201">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnVersion.</span></span></p></li>
<li><p><span data-ttu-id="53901-202">JET_bitColumnUserDefinedDefault se usó junto con JET_bitColumnAutoincrement.</span><span class="sxs-lookup"><span data-stu-id="53901-202">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnAutoincrement.</span></span></p></li>
<li><p><span data-ttu-id="53901-203">JET_bitColumnUserDefinedDefault se usó junto con JET_bitColumnUpdatable.</span><span class="sxs-lookup"><span data-stu-id="53901-203">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnUpdatable.</span></span></p></li>
<li><p><span data-ttu-id="53901-204">JET_bitColumnUserDefinedDefault se usó junto con JET_bitColumnEscrowUpdate.</span><span class="sxs-lookup"><span data-stu-id="53901-204">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnEscrowUpdate.</span></span></p></li>
<li><p><span data-ttu-id="53901-205">JET_bitColumnUserDefinedDefault se usó junto con JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="53901-205">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnFinalize.</span></span></p></li>
<li><p><span data-ttu-id="53901-206">JET_bitColumnUserDefinedDefault se usó junto con JET_bitColumnDeleteOnZero.</span><span class="sxs-lookup"><span data-stu-id="53901-206">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnDeleteOnZero.</span></span></p></li>
<li><p><span data-ttu-id="53901-207">JET_bitColumnUserDefinedDefault se usó junto con JET_bitColumnMaybeNull.</span><span class="sxs-lookup"><span data-stu-id="53901-207">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnMaybeNull.</span></span></p></li>
<li><p><span data-ttu-id="53901-208">JET_bitColumnUserDefinedDefault se usó en una columna no etiquetada (que es fija o variable).</span><span class="sxs-lookup"><span data-stu-id="53901-208">JET_bitColumnUserDefinedDefault was used on a non-tagged column (that is fixed or variable).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53901-209">JET_errMultiValuedColumnMustBeTagged</span><span class="sxs-lookup"><span data-stu-id="53901-209">JET_errMultiValuedColumnMustBeTagged</span></span></p></td>
<td><p><span data-ttu-id="53901-210">Una columna con varios valores (JET_bitColumnMultiValued) solo se puede usar en una columna de valor largo o etiquetado (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span><span class="sxs-lookup"><span data-stu-id="53901-210">A multi-valued column (JET_bitColumnMultiValued) can only be used on a tagged or Long Value (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>) column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53901-211">JET_errCannotBeTagged</span><span class="sxs-lookup"><span data-stu-id="53901-211">JET_errCannotBeTagged</span></span></p></td>
<td><p><span data-ttu-id="53901-212">Se intentó utilizar una columna etiquetada cuando es posible que la columna no esté etiquetada.</span><span class="sxs-lookup"><span data-stu-id="53901-212">An attempt was made to use a tagged column when the column might not be tagged.</span></span> <span data-ttu-id="53901-213">Algunas de las restricciones para impedir las columnas etiquetadas son:</span><span class="sxs-lookup"><span data-stu-id="53901-213">Some of the constraints for disallowing tagged columns are:</span></span></p>
<ul>
<li><p><span data-ttu-id="53901-214">No se puede usar una columna de actualización de custodia (JET_bitColumnEscrowUpdate) en una columna de valor largo o etiquetado (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span><span class="sxs-lookup"><span data-stu-id="53901-214">An Escrow Update column (JET_bitColumnEscrowUpdate) cannot be used on a tagged or Long Value (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>) column.</span></span></p></li>
<li><p><span data-ttu-id="53901-215">Es posible que una columna de incremento automático no esté etiquetada.</span><span class="sxs-lookup"><span data-stu-id="53901-215">An autoincrement column might not be tagged.</span></span></p></li>
<li><p><span data-ttu-id="53901-216">Es posible que una columna de versión no esté etiquetada.</span><span class="sxs-lookup"><span data-stu-id="53901-216">A Version column might not be tagged.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53901-217">JET_errExclusiveTableLockRequired</span><span class="sxs-lookup"><span data-stu-id="53901-217">JET_errExclusiveTableLockRequired</span></span></p></td>
<td><p><span data-ttu-id="53901-218">Se requiere un bloqueo exclusivo en la tabla para esta operación.</span><span class="sxs-lookup"><span data-stu-id="53901-218">An exclusive lock on the table was required for this operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53901-219">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="53901-219">JET_wrnColumnMaxTruncated</span></span></p></td>
<td><p><span data-ttu-id="53901-220">ADVERTENCIA que indica que la longitud máxima (<em>cbMax</em>) de una columna fija o de variable era mayor que JET_cbColumnMost.</span><span class="sxs-lookup"><span data-stu-id="53901-220">A warning indicating that the maximum length (<em>cbMax</em>) of a fixed or variable column was greater than JET_cbColumnMost.</span></span> <span data-ttu-id="53901-221">Este límite no se aplica a los valores largos (es decir <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> y <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span><span class="sxs-lookup"><span data-stu-id="53901-221">This limit does not apply to Long Values (that is <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> and <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="53901-222">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53901-222">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53901-223"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="53901-223"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="53901-224">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="53901-224">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53901-225"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="53901-225"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="53901-226">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="53901-226">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53901-227"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="53901-227"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="53901-228">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="53901-228">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53901-229"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="53901-229"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="53901-230">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="53901-230">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53901-231"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="53901-231"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="53901-232">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="53901-232">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53901-233"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="53901-233"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="53901-234">Se implementa como <strong>JetAddColumnW</strong> (Unicode) y <strong>JetAddColumnA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="53901-234">Implemented as <strong>JetAddColumnW</strong> (Unicode) and <strong>JetAddColumnA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="53901-235">Consulte también</span><span class="sxs-lookup"><span data-stu-id="53901-235">See Also</span></span>

[<span data-ttu-id="53901-236">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="53901-236">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="53901-237">JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="53901-237">JET_COLUMNCREATE</span></span>](./jet-columncreate-structure.md)  
[<span data-ttu-id="53901-238">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="53901-238">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="53901-239">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="53901-239">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="53901-240">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="53901-240">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="53901-241">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="53901-241">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="53901-242">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="53901-242">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="53901-243">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="53901-243">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="53901-244">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="53901-244">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="53901-245">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="53901-245">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
