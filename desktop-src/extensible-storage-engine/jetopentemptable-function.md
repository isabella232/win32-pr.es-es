---
description: 'Más información acerca de: JetOpenTempTable (función)'
title: Función JetOpenTempTable
TOCTitle: JetOpenTempTable Function
ms:assetid: 29261333-a1bc-4159-9046-c32c36f47410
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269211(v=EXCHG.10)
ms:contentKeyID: 32765514
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 66c58abc5cff433bb4d944e39c283ba712d7cebf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696217"
---
# <a name="jetopentemptable-function"></a><span data-ttu-id="cdb51-103">Función JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="cdb51-103">JetOpenTempTable Function</span></span>


<span data-ttu-id="cdb51-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="cdb51-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentemptable-function"></a><span data-ttu-id="cdb51-105">Función JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="cdb51-105">JetOpenTempTable Function</span></span>

<span data-ttu-id="cdb51-106">La función **JetOpenTempTable** crea una tabla temporal con un índice único.</span><span class="sxs-lookup"><span data-stu-id="cdb51-106">The **JetOpenTempTable** function creates a temporary table with a single index.</span></span> <span data-ttu-id="cdb51-107">Una tabla temporal almacena y recupera registros como una tabla normal creada mediante [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="cdb51-107">A temporary table stores and retrieves records just like an ordinary table created using [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span> <span data-ttu-id="cdb51-108">Sin embargo, las tablas temporales son mucho más rápidas que las normales debido a su naturaleza volátil.</span><span class="sxs-lookup"><span data-stu-id="cdb51-108">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="cdb51-109">También se pueden usar para ordenar de forma muy rápida y realizar una eliminación duplicada en conjuntos de registros cuando se tiene acceso a ellos de forma puramente secuencial.</span><span class="sxs-lookup"><span data-stu-id="cdb51-109">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span>

```cpp
    JET_ERR JET_API JetOpenTempTable(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a><span data-ttu-id="cdb51-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cdb51-110">Parameters</span></span>

<span data-ttu-id="cdb51-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="cdb51-111">*sesid*</span></span>

<span data-ttu-id="cdb51-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="cdb51-112">The session to use.</span></span>

<span data-ttu-id="cdb51-113">*prgcolumndef*</span><span class="sxs-lookup"><span data-stu-id="cdb51-113">*prgcolumndef*</span></span>

<span data-ttu-id="cdb51-114">Definiciones de columna para las columnas creadas en la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="cdb51-114">Column definitions for the columns created in the temporary table.</span></span>

<span data-ttu-id="cdb51-115">Existen limitaciones **importantes** para las opciones de definición de columna que se utilizan con una tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="cdb51-115">**Important**   limitations exist for the column definition options that are used with a temporary table.</span></span> <span data-ttu-id="cdb51-116">Vea la sección Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="cdb51-116">See the Remarks section for more information.</span></span>

<span data-ttu-id="cdb51-117">Además de las opciones de definición de columna habituales, también se pueden especificar cero o más de las opciones siguientes que solo son relevantes en el contexto de una tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="cdb51-117">In addition to the usual column definition options, zero or more of the following options can also be specified that are relevant only in the context of a temporary table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cdb51-118">Value</span><span class="sxs-lookup"><span data-stu-id="cdb51-118">Value</span></span></p></th>
<th><p><span data-ttu-id="cdb51-119">Significado</span><span class="sxs-lookup"><span data-stu-id="cdb51-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdb51-120">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="cdb51-120">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="cdb51-121">El criterio de ordenación de la columna de clave para la tabla temporal debe ser descendente en lugar de ascendente.</span><span class="sxs-lookup"><span data-stu-id="cdb51-121">The sort order of the key column for the temporary table should be descending rather than ascending.</span></span> <span data-ttu-id="cdb51-122">Si se especifica esta opción sin JET_bitColumnTTKey, se omite esta opción.</span><span class="sxs-lookup"><span data-stu-id="cdb51-122">If this option is specified without JET_bitColumnTTKey then this option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdb51-123">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="cdb51-123">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="cdb51-124">La columna será una columna de clave para la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="cdb51-124">The column will be a key column for the temporary table.</span></span></p>
<p><span data-ttu-id="cdb51-125">El orden de las definiciones de columna con esta opción especificada en la matriz de entrada determinará la prioridad de cada columna de clave para la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="cdb51-125">The order of the column definitions with this option specified in the input array will determine the precedence of each key column for the temporary table.</span></span> <span data-ttu-id="cdb51-126">La primera definición de columna de la matriz que tiene esta opción establecida será la columna de clave más significativa, etc.</span><span class="sxs-lookup"><span data-stu-id="cdb51-126">The first column definition in the array that has this option set will be the most significant key column and so on.</span></span> <span data-ttu-id="cdb51-127">Si se solicitan más columnas de clave de las que puede admitir el motor de base de datos, esta opción se omite para las columnas de clave no admitidas.</span><span class="sxs-lookup"><span data-stu-id="cdb51-127">If more key columns are requested than can be supported by the database engine then this option is ignored for the unsupportable key columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cdb51-128">*ccolumn*</span><span class="sxs-lookup"><span data-stu-id="cdb51-128">*ccolumn*</span></span>

<span data-ttu-id="cdb51-129">Vea *prgcolumndef*.</span><span class="sxs-lookup"><span data-stu-id="cdb51-129">See *prgcolumndef*.</span></span>

<span data-ttu-id="cdb51-130">*grbit*</span><span class="sxs-lookup"><span data-stu-id="cdb51-130">*grbit*</span></span>

<span data-ttu-id="cdb51-131">Grupo de bits que especifica cero o más de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="cdb51-131">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cdb51-132">Value</span><span class="sxs-lookup"><span data-stu-id="cdb51-132">Value</span></span></p></th>
<th><p><span data-ttu-id="cdb51-133">Significado</span><span class="sxs-lookup"><span data-stu-id="cdb51-133">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdb51-134">JET_bitTTErrorOnDuplicateInsertion</span><span class="sxs-lookup"><span data-stu-id="cdb51-134">JET_bitTTErrorOnDuplicateInsertion</span></span></p></td>
<td><p><span data-ttu-id="cdb51-135">Cualquier intento de insertar un registro con la misma clave de índice que un registro insertado anteriormente producirá un error inmediatamente con JET_errKeyDuplicate.</span><span class="sxs-lookup"><span data-stu-id="cdb51-135">Any attempt to insert a record with the same index key as a previously inserted record will immediately fail with JET_errKeyDuplicate.</span></span> <span data-ttu-id="cdb51-136">Si no se solicita esta opción, se detectará un duplicado inmediatamente y se producirá un error, o se quitará de forma silenciosa más adelante, en función de la estrategia elegida por el motor de base de datos para implementar la tabla temporal, en función de la funcionalidad solicitada.</span><span class="sxs-lookup"><span data-stu-id="cdb51-136">If this option is not requested then a duplicate is detected immediately and fails, or is silently removed later, depending on the strategy chosen by the database engine to implement the temporary table, based on the requested functionality.</span></span></p>
<p><span data-ttu-id="cdb51-137">Si esta funcionalidad no es necesaria, es mejor no solicitarlo.</span><span class="sxs-lookup"><span data-stu-id="cdb51-137">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="cdb51-138">Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</span><span class="sxs-lookup"><span data-stu-id="cdb51-138">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdb51-139">JET_bitTTForceMaterialization</span><span class="sxs-lookup"><span data-stu-id="cdb51-139">JET_bitTTForceMaterialization</span></span></p></td>
<td><p><span data-ttu-id="cdb51-140">Obliga al administrador de tablas temporal a abandonar la búsqueda de la mejor estrategia para usar la administración de la tabla temporal, lo que dará lugar a un rendimiento mejorado.</span><span class="sxs-lookup"><span data-stu-id="cdb51-140">Forces the temporary table manager to abandon the search for the best strategy to use managing the temporary table that will result in enhanced performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdb51-141">JET_bitTTForwardOnly</span><span class="sxs-lookup"><span data-stu-id="cdb51-141">JET_bitTTForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="cdb51-142">La tabla temporal solo se crea si el administrador de tablas temporales puede usar la implementación optimizada para los resultados intermedios de la consulta.</span><span class="sxs-lookup"><span data-stu-id="cdb51-142">The temporary table is only created if the temporary table manager can use the implementation that is optimized for intermediate query results.</span></span> <span data-ttu-id="cdb51-143">Si alguna característica de la tabla temporal impidiera el uso de esta optimización, la operación producirá un error con JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="cdb51-143">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span></p>
<p><span data-ttu-id="cdb51-144">Un efecto secundario de esta opción es permitir que la tabla temporal contenga registros con claves de índice duplicadas.</span><span class="sxs-lookup"><span data-stu-id="cdb51-144">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="cdb51-145">Consulte JET_bitTTUnique para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="cdb51-145">See JET_bitTTUnique for more information.</span></span></p>
<p><span data-ttu-id="cdb51-146">Esta opción solo está disponible en Windows Server 2003 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="cdb51-146">This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdb51-147">JET_bitTTIndexed</span><span class="sxs-lookup"><span data-stu-id="cdb51-147">JET_bitTTIndexed</span></span></p></td>
<td><p><span data-ttu-id="cdb51-148">Esta opción solicita que la tabla temporal sea lo suficientemente flexible como para permitir el uso de <a href="gg294103(v=exchg.10).md">JetSeek</a> para buscar registros por clave de índice.</span><span class="sxs-lookup"><span data-stu-id="cdb51-148">This option requests that the temporary table be flexible enough to permit the use of <a href="gg294103(v=exchg.10).md">JetSeek</a> to look up records by index key.</span></span></p>
<p><span data-ttu-id="cdb51-149">Si esta funcionalidad no es necesaria, es mejor no solicitarlo.</span><span class="sxs-lookup"><span data-stu-id="cdb51-149">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="cdb51-150">Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</span><span class="sxs-lookup"><span data-stu-id="cdb51-150">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdb51-151">JET_bitTTUnique</span><span class="sxs-lookup"><span data-stu-id="cdb51-151">JET_bitTTUnique</span></span></p></td>
<td><p><span data-ttu-id="cdb51-152">Solicita que los registros con claves de índice duplicadas se quiten del conjunto final de registros de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="cdb51-152">Requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span></p>
<p><span data-ttu-id="cdb51-153">Antes de Windows Server 2003, el motor de base de datos siempre asumió que esta opción está en vigor debido al hecho de que todos los índices clúster también deben ser una clave principal y, por tanto, deben ser únicos.</span><span class="sxs-lookup"><span data-stu-id="cdb51-153">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="cdb51-154">A partir de Windows Server 2003, ahora es posible crear una tabla temporal que no quita los duplicados cuando también se especifica la opción de JET_bitTTForwardOnly.</span><span class="sxs-lookup"><span data-stu-id="cdb51-154">As of Windows Server 2003, it is now possible to create a temporary table that does not remove duplicates when the JET_bitTTForwardOnly option is also specified.</span></span></p>
<p><span data-ttu-id="cdb51-155">No es posible saber qué duplicado se realizará correctamente y qué duplicados se descartarán, en general.</span><span class="sxs-lookup"><span data-stu-id="cdb51-155">It is not possible to know which duplicate will succeed and which duplicates will be discarded, in general.</span></span> <span data-ttu-id="cdb51-156">Sin embargo, cuando se solicita la opción de JET_bitTTErrorOnDuplicateInsertion, el primer registro con una clave de índice determinada que se va a insertar en la tabla temporal siempre se realizará correctamente.</span><span class="sxs-lookup"><span data-stu-id="cdb51-156">However, when the JET_bitTTErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always succeed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdb51-157">JET_bitTTUpdatable</span><span class="sxs-lookup"><span data-stu-id="cdb51-157">JET_bitTTUpdatable</span></span></p></td>
<td><p><span data-ttu-id="cdb51-158">Solicita que la tabla temporal sea lo suficientemente flexible como para permitir que se modifiquen posteriormente los registros que se han insertado previamente.</span><span class="sxs-lookup"><span data-stu-id="cdb51-158">Requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="cdb51-159">Si esta funcionalidad no es necesaria, es mejor no solicitarlo.</span><span class="sxs-lookup"><span data-stu-id="cdb51-159">If this functionality it not required then it is best to not request it.</span></span></p>
<p><span data-ttu-id="cdb51-160">Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</span><span class="sxs-lookup"><span data-stu-id="cdb51-160">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdb51-161">JET_bitTTScrollable</span><span class="sxs-lookup"><span data-stu-id="cdb51-161">JET_bitTTScrollable</span></span></p></td>
<td><p><span data-ttu-id="cdb51-162">Solicita que la tabla temporal sea lo suficientemente flexible como para permitir que los registros se examinen en orden y dirección arbitrarios mediante <a href="gg294117(v=exchg.10).md">JetMove</a>.</span><span class="sxs-lookup"><span data-stu-id="cdb51-162">Requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p>
<p><span data-ttu-id="cdb51-163">Si no se necesita esta funcionalidad, es mejor no solicitarla.</span><span class="sxs-lookup"><span data-stu-id="cdb51-163">If this functionality is not required then it is best to not request it.</span></span> <span data-ttu-id="cdb51-164">Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</span><span class="sxs-lookup"><span data-stu-id="cdb51-164">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdb51-165">JET_bitTTSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="cdb51-165">JET_bitTTSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="cdb51-166">Solicita que los valores de columna de clave NULL se ordenen más cerca del final del índice que los valores de columna de clave no NULL.</span><span class="sxs-lookup"><span data-stu-id="cdb51-166">Requests that NULL key column values sort closer to the end of the index than non-NULL key column values.</span></span></p>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdb51-167">JET_bitTTIntrinsicLVsOnly</span><span class="sxs-lookup"><span data-stu-id="cdb51-167">JET_bitTTIntrinsicLVsOnly</span></span></p></td>
<td><p><span data-ttu-id="cdb51-168">Solicitudes para permitir solo valores largos intrínsecos.</span><span class="sxs-lookup"><span data-stu-id="cdb51-168">Requests to permit only intrinsic long values.</span></span></p>
<p><span data-ttu-id="cdb51-169"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> se introduce en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cdb51-169"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cdb51-170">*ptableid*</span><span class="sxs-lookup"><span data-stu-id="cdb51-170">*ptableid*</span></span>

<span data-ttu-id="cdb51-171">Búfer de salida que recibe el nuevo cursor abierto en la tabla temporal recién creada.</span><span class="sxs-lookup"><span data-stu-id="cdb51-171">The output buffer that receives the new cursor opened on the newly created temporary table.</span></span>

<span data-ttu-id="cdb51-172">*prgcolumnid*</span><span class="sxs-lookup"><span data-stu-id="cdb51-172">*prgcolumnid*</span></span>

<span data-ttu-id="cdb51-173">Búfer de salida que recibe la matriz de identificadores de columna generados durante la creación de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="cdb51-173">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span>

<span data-ttu-id="cdb51-174">Los identificadores de columna de esta matriz se corresponden exactamente con la matriz de entrada de definiciones de columna.</span><span class="sxs-lookup"><span data-stu-id="cdb51-174">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="cdb51-175">Como resultado, el tamaño de este búfer debe corresponder al tamaño de la matriz de entrada.</span><span class="sxs-lookup"><span data-stu-id="cdb51-175">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

### <a name="return-value"></a><span data-ttu-id="cdb51-176">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cdb51-176">Return Value</span></span>

<span data-ttu-id="cdb51-177">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="cdb51-177">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="cdb51-178">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="cdb51-178">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cdb51-179">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="cdb51-179">Return code</span></span></p></th>
<th><p><span data-ttu-id="cdb51-180">Descripción</span><span class="sxs-lookup"><span data-stu-id="cdb51-180">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdb51-181">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="cdb51-181">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="cdb51-182">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="cdb51-182">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdb51-183">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="cdb51-183">JET_errCannotMaterializeForwardOnlySort</span></span></p></td>
<td><p><span data-ttu-id="cdb51-184">Error de <strong>JetOpenTempTable</strong> porque se especificó JET_bitTTForwardOnly y no se pudo crear la tabla temporal tal y como se especificó mediante la optimización de solo avance.</span><span class="sxs-lookup"><span data-stu-id="cdb51-184"><strong>JetOpenTempTable</strong> failed because JET_bitTTForwardOnly was specified and the temporary table as specified could not be created using the forward-only optimization.</span></span> <span data-ttu-id="cdb51-185">Este error solo lo devolverán Windows Server 2003 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="cdb51-185">This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdb51-186">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="cdb51-186">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="cdb51-187">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="cdb51-187">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdb51-188">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="cdb51-188">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="cdb51-189">No se pudo crear el índice porque se especificó una definición de índice no válida.</span><span class="sxs-lookup"><span data-stu-id="cdb51-189">The index could not be created because an invalid index definition was specified.</span></span></p>
<p><span data-ttu-id="cdb51-190"><strong>JetOpenTempTable</strong> devolverá este error cuando:</span><span class="sxs-lookup"><span data-stu-id="cdb51-190"><strong>JetOpenTempTable</strong> will return this error when:</span></span></p>
<ul>
<li><p><span data-ttu-id="cdb51-191">Se especifica la configuración regional independiente del idioma.</span><span class="sxs-lookup"><span data-stu-id="cdb51-191">The Language Neutral locale is specified.</span></span></p></li>
<li><p><span data-ttu-id="cdb51-192">Se especifica un conjunto no válido de marcas de normalización.</span><span class="sxs-lookup"><span data-stu-id="cdb51-192">An invalid set of normalization flags is specified.</span></span></p></li>
</ul>
<p><span data-ttu-id="cdb51-193">Este error solo lo devolverá Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="cdb51-193">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdb51-194">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="cdb51-194">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="cdb51-195">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="cdb51-195">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="cdb51-196">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="cdb51-196">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdb51-197">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="cdb51-197">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="cdb51-198">El campo CP del <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> no se estableció en una página de códigos válida.</span><span class="sxs-lookup"><span data-stu-id="cdb51-198">The cp field of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid code page.</span></span> <span data-ttu-id="cdb51-199">Los únicos valores válidos para las columnas de texto son inglés (1252) y Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="cdb51-199">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="cdb51-200">Un valor de 0 significa que se usará el valor predeterminado (Inglés, 1252).</span><span class="sxs-lookup"><span data-stu-id="cdb51-200">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdb51-201">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="cdb51-201">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="cdb51-202">El campo <em>coltyp</em> de la <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> no se ha establecido en un tipo de columna válido.</span><span class="sxs-lookup"><span data-stu-id="cdb51-202">The <em>coltyp</em> field of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdb51-203">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="cdb51-203">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="cdb51-204">No se pudo crear el índice porque se intentó usar un ID. de configuración regional no válido.</span><span class="sxs-lookup"><span data-stu-id="cdb51-204">The index could not be created because an attempt was made to use an invalid locale ID.</span></span> <span data-ttu-id="cdb51-205">Es posible que el ID. de configuración regional no sea válido o que el paquete de idioma asociado no esté instalado.</span><span class="sxs-lookup"><span data-stu-id="cdb51-205">The locale ID may either be completely invalid or the associated language pack may not be installed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdb51-206">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="cdb51-206">JET_errInvalidLCMapStringFlags</span></span></p></td>
<td><p><span data-ttu-id="cdb51-207">No se pudo crear el índice porque se intentó usar un conjunto no válido de marcas de normalización.</span><span class="sxs-lookup"><span data-stu-id="cdb51-207">The index could not be created because an attempt was made to use an invalid set of normalization flags.</span></span> <span data-ttu-id="cdb51-208">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="cdb51-208">This error will only be returned by Windows XP and later releases.</span></span> <span data-ttu-id="cdb51-209">En Windows 2000, las marcas de normalización no válidas producirán JET_errIndexInvalidDef en su lugar.</span><span class="sxs-lookup"><span data-stu-id="cdb51-209">On Windows 2000, invalid normalization flags will result in JET_errIndexInvalidDef instead.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdb51-210">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="cdb51-210">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="cdb51-211">El identificador de sesión no es válido o hace referencia a una sesión cerrada.</span><span class="sxs-lookup"><span data-stu-id="cdb51-211">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="cdb51-212"><strong>Nota:</strong>  Este error no se devuelve en todas las circunstancias.</span><span class="sxs-lookup"><span data-stu-id="cdb51-212"><strong>Note</strong>  This error is not returned under all circumstances.</span></span> <span data-ttu-id="cdb51-213">Los identificadores se validan solo en función del mejor esfuerzo.</span><span class="sxs-lookup"><span data-stu-id="cdb51-213">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdb51-214">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="cdb51-214">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="cdb51-215">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="cdb51-215">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdb51-216">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="cdb51-216">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="cdb51-217">No se pudo realizar la operación porque el motor no puede asignar los recursos necesarios para abrir un nuevo cursor.</span><span class="sxs-lookup"><span data-stu-id="cdb51-217">The operation failed because the engine cannot allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="cdb51-218">Los recursos de cursor se configuran mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="cdb51-218">Cursor resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdb51-219">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="cdb51-219">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="cdb51-220">No se pudo realizar la operación porque no se pudo asignar suficiente memoria para completarla.</span><span class="sxs-lookup"><span data-stu-id="cdb51-220">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="cdb51-221"><strong>JetOpenTempTable</strong> puede devolver JET_errOutOfMemory si el espacio de direcciones del proceso de host está demasiado fragmentado.</span><span class="sxs-lookup"><span data-stu-id="cdb51-221"><strong>JetOpenTempTable</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="cdb51-222">El administrador de tablas temporales asignará siempre un fragmento de 1 MB de espacio de direcciones para cada tabla temporal creada independientemente de la cantidad de datos que se van a almacenar.</span><span class="sxs-lookup"><span data-stu-id="cdb51-222">The temporary table manager will always allocate a 1MB chunk of address space for every temporary table created regardless of the amount of data to be stored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdb51-223">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="cdb51-223">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="cdb51-224">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="cdb51-224">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdb51-225">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="cdb51-225">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="cdb51-226">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="cdb51-226">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="cdb51-227">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="cdb51-227">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdb51-228">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="cdb51-228">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="cdb51-229">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="cdb51-229">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdb51-230">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="cdb51-230">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="cdb51-231">Se intentó agregar demasiadas columnas a la tabla.</span><span class="sxs-lookup"><span data-stu-id="cdb51-231">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="cdb51-232">Una tabla no puede tener más de JET_ccolFixedMost columnas fijas, ni más de JET_ccolVarMost columnas de longitud variable, ni más de JET_ccolTaggedMost columnas etiquetadas.</span><span class="sxs-lookup"><span data-stu-id="cdb51-232">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdb51-233">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="cdb51-233">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="cdb51-234">No se pudo realizar la operación porque el motor no puede asignar los recursos necesarios para almacenar en memoria caché los índices de la tabla.</span><span class="sxs-lookup"><span data-stu-id="cdb51-234">The operation failed because the engine cannot allocate the resources required to cache the indexes of the table.</span></span> <span data-ttu-id="cdb51-235">El número de índices cuyo esquema se puede almacenar en caché se configura mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="cdb51-235">The number of indexes whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdb51-236">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="cdb51-236">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="cdb51-237">No se pudo realizar la operación porque el motor no puede asignar los recursos necesarios para almacenar en caché el esquema de la tabla.</span><span class="sxs-lookup"><span data-stu-id="cdb51-237">The operation failed because the engine cannot allocate the resources required to cache the schema of the table.</span></span> <span data-ttu-id="cdb51-238">El número de tablas cuyo esquema se puede almacenar en caché se configura mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="cdb51-238">The number of tables whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdb51-239">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="cdb51-239">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="cdb51-240">No se pudo realizar la operación porque el motor no puede asignar los recursos necesarios para crear una tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="cdb51-240">The operation failed because the engine cannot allocate the resources required to create a temporary table.</span></span> <span data-ttu-id="cdb51-241">Los recursos de tabla temporal se configuran mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span><span class="sxs-lookup"><span data-stu-id="cdb51-241">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cdb51-242">Si se ejecuta correctamente, se devolverá un cursor abierto en la tabla temporal recién creada.</span><span class="sxs-lookup"><span data-stu-id="cdb51-242">On success, a cursor opened on the newly created temporary table will be returned.</span></span> <span data-ttu-id="cdb51-243">El estado de la base de datos temporal se preparará para contener la nueva tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="cdb51-243">The state of the temporary database will be prepared to contain the new temporary table.</span></span> <span data-ttu-id="cdb51-244">El estado de las bases de datos normales que use el motor de base de datos permanecerá sin cambios.</span><span class="sxs-lookup"><span data-stu-id="cdb51-244">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

<span data-ttu-id="cdb51-245">En caso de error, no se creará la tabla temporal y no se devolverá un cursor.</span><span class="sxs-lookup"><span data-stu-id="cdb51-245">On failure, the temporary table will not be created and a cursor will not be returned.</span></span> <span data-ttu-id="cdb51-246">Se puede cambiar el estado de la base de datos temporal.</span><span class="sxs-lookup"><span data-stu-id="cdb51-246">The state of the temporary database may be changed.</span></span> <span data-ttu-id="cdb51-247">El estado de las bases de datos normales que use el motor de base de datos permanecerá sin cambios.</span><span class="sxs-lookup"><span data-stu-id="cdb51-247">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cdb51-248">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cdb51-248">Remarks</span></span>

<span data-ttu-id="cdb51-249">Las tablas temporales no admiten el complemento completo de las opciones de definición de columna que normalmente admite el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="cdb51-249">Temporary tables do not support the full complement of column definition options that are ordinarily supported by the database engine.</span></span> <span data-ttu-id="cdb51-250">De hecho, solo se admiten JET_bitColumnFixed y JET_bitColumnTagged.</span><span class="sxs-lookup"><span data-stu-id="cdb51-250">In fact, only JET_bitColumnFixed and JET_bitColumnTagged are supported.</span></span> <span data-ttu-id="cdb51-251">Esto significa que no es posible crear una columna de incremento automático, versión o multivalor en una tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="cdb51-251">This means that it is not possible to create an auto-increment, version, or multi-valued column in a temporary table.</span></span> <span data-ttu-id="cdb51-252">Por último, no se admiten las columnas de actualización de custodia porque no son útiles en una tabla temporal, ya que solo se pueden usar en una sesión a la vez.</span><span class="sxs-lookup"><span data-stu-id="cdb51-252">Finally, escrow update columns are not supported because they are not useful in a temporary table since they can only be used by one session at a time.</span></span> <span data-ttu-id="cdb51-253">Si se solicita alguna de estas opciones, se omitirán.</span><span class="sxs-lookup"><span data-stu-id="cdb51-253">If any of these options are requested then they will be ignored.</span></span>

<span data-ttu-id="cdb51-254">Las tablas temporales no admiten valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="cdb51-254">Temporary tables do not support default values.</span></span> <span data-ttu-id="cdb51-255">Si se proporciona una definición de columna que contiene una especificación de valor predeterminado, se omitirá esa especificación.</span><span class="sxs-lookup"><span data-stu-id="cdb51-255">If a column definition is provided that contains a default value specification then that specification will be ignored.</span></span>

<span data-ttu-id="cdb51-256">Las tablas temporales se devuelven al autor de la llamada como resultado de muchas funciones de ESE diferentes.</span><span class="sxs-lookup"><span data-stu-id="cdb51-256">Temporary tables are returned to the caller as a result of many different ESE functions.</span></span> <span data-ttu-id="cdb51-257">Por ejemplo, [JetGetIndexInfo](./jetgetindexinfo-function.md) con la opción JET_IdxInfo establecida en el parámetro *InfoLevel* devolverá una tabla temporal que contenga una lista de todas las columnas de clave de un índice determinado.</span><span class="sxs-lookup"><span data-stu-id="cdb51-257">For example, [JetGetIndexInfo](./jetgetindexinfo-function.md) with the JET_IdxInfo option set in the *InfoLevel* parameter will return a temporary table containing a list of all the key columns in a given index.</span></span> <span data-ttu-id="cdb51-258">Las tablas temporales siguen las mismas reglas del ciclo de vida que las tablas temporales normales, como se describe aquí.</span><span class="sxs-lookup"><span data-stu-id="cdb51-258">The temporary tables follow the same lifecycle rules as ordinary temporary tables as described here.</span></span>

<span data-ttu-id="cdb51-259">El motor de base de datos también usa internamente las tablas temporales para muchas tareas.</span><span class="sxs-lookup"><span data-stu-id="cdb51-259">Temporary tables are also used internally by the database engine for many tasks.</span></span> <span data-ttu-id="cdb51-260">Lo más importante de estas tareas es la creación de un índice en una tabla existente.</span><span class="sxs-lookup"><span data-stu-id="cdb51-260">The most important of these tasks is the creation of an index over an existing table.</span></span> <span data-ttu-id="cdb51-261">Se utilizará una tabla temporal para ordenar las claves de índice utilizadas para construir ese índice.</span><span class="sxs-lookup"><span data-stu-id="cdb51-261">A temporary table will be used to sort the index keys used to construct that index.</span></span>

<span data-ttu-id="cdb51-262">Todas las tablas temporales se almacenan en la base de datos temporal.</span><span class="sxs-lookup"><span data-stu-id="cdb51-262">All temporary tables are stored in the temporary database.</span></span> <span data-ttu-id="cdb51-263">La base de datos temporal es un archivo de base de datos Especial que se mantiene durante la vigencia de una instancia de ESE y se elimina cuando se cierra o se reinicia la instancia.</span><span class="sxs-lookup"><span data-stu-id="cdb51-263">The temporary database is a special database file that is maintained during the lifetime of an ESE instance and is deleted when that instance is shut down or restarted.</span></span> <span data-ttu-id="cdb51-264">La ubicación de la base de datos temporal se puede configurar mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md) con [JET_paramTempPath](./temporary-database-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="cdb51-264">The location of the temporary database can be configured using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramTempPath](./temporary-database-parameters.md).</span></span> <span data-ttu-id="cdb51-265">La selección de ubicación de la base de datos temporal en el disco en relación con los archivos de registro de transacciones y los archivos de base de datos puede ser importante si la aplicación hace un uso intensivo de tablas temporales o crea índices con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="cdb51-265">Placement of the temporary database on disk relative to your transaction log files and database files may be important if your application makes heavy use of temporary tables or creates indexes frequently.</span></span>

<span data-ttu-id="cdb51-266">El ciclo de vida de una tabla temporal está asociado a los cursores que hacen referencia a él.</span><span class="sxs-lookup"><span data-stu-id="cdb51-266">The lifecycle of a temporary table is tied to the cursors that reference it.</span></span> <span data-ttu-id="cdb51-267">Si se cierran todos los cursores que hacen referencia a una tabla temporal, ya sea implícita o explícitamente, se eliminará la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="cdb51-267">If all the cursors that reference a temporary table are closed, either implicitly or explicitly, then the temporary table will be deleted.</span></span> <span data-ttu-id="cdb51-268">Si una tabla temporal se crea dentro de una transacción y esa transacción se revierte posteriormente, se eliminará la tabla temporal, ya que todos los cursores que hagan referencia a ella en este momento se cerrarán implícitamente.</span><span class="sxs-lookup"><span data-stu-id="cdb51-268">If a temporary table is created inside a transaction and that transaction is subsequently rolled back then the temporary table will be deleted because any cursors that referenced it at this time will be implicitly closed.</span></span> <span data-ttu-id="cdb51-269">Los nuevos cursores solo pueden hacer referencia a una tabla temporal mediante el uso de [JetDupCursor](./jetdupcursor-function.md).</span><span class="sxs-lookup"><span data-stu-id="cdb51-269">New cursors may reference a temporary table only through the use of [JetDupCursor](./jetdupcursor-function.md).</span></span> <span data-ttu-id="cdb51-270">En este caso, los nuevos cursores se colocarán en la primera entrada de índice de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="cdb51-270">In this case, the new cursors will be positioned on the first index entry of the temporary table.</span></span> <span data-ttu-id="cdb51-271">[JetDupCursor](./jetdupcursor-function.md) solo funcionará durante ciertas fases de uso de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="cdb51-271">[JetDupCursor](./jetdupcursor-function.md) will only work during certain phases of use for the temporary table.</span></span> <span data-ttu-id="cdb51-272">Para obtener más información, consulte las notas sobre las funcionalidades de cursor de tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="cdb51-272">See the remarks concerning temporary table cursor capabilities for more information.</span></span> <span data-ttu-id="cdb51-273">No es posible hacer referencia a una tabla temporal de más de una sesión a la vez.</span><span class="sxs-lookup"><span data-stu-id="cdb51-273">It is not possible to reference a temporary table from more than one session at a time.</span></span>

<span data-ttu-id="cdb51-274">Hay un problema importante en [JetDupCursor](./jetdupcursor-function.md) que afecta a las tablas temporales.</span><span class="sxs-lookup"><span data-stu-id="cdb51-274">There is an important problem in [JetDupCursor](./jetdupcursor-function.md) that affects temporary tables.</span></span> <span data-ttu-id="cdb51-275">Si se realiza un intento de duplicar una tabla temporal que está en modo de solo avance, el cursor resultante no se creará correctamente y dejará de funcionar.</span><span class="sxs-lookup"><span data-stu-id="cdb51-275">If an attempt is made to duplicate a temporary table that is in forward-only mode then the resulting cursor will not be created properly and will malfunction.</span></span> <span data-ttu-id="cdb51-276">Todavía es seguro duplicar un cursor sobre una tabla temporal materializada.</span><span class="sxs-lookup"><span data-stu-id="cdb51-276">It is still safe to duplicate a cursor over a materialized temporary table.</span></span>

<span data-ttu-id="cdb51-277">El administrador de tablas temporales puede optar por implementar una tabla temporal de tres maneras.</span><span class="sxs-lookup"><span data-stu-id="cdb51-277">The temporary table manager may choose to implement a temporary table in three ways.</span></span> <span data-ttu-id="cdb51-278">El primer método consiste en mantener una tabla en memoria.</span><span class="sxs-lookup"><span data-stu-id="cdb51-278">The first method is to maintain an in-memory table.</span></span> <span data-ttu-id="cdb51-279">Esta estrategia es la más rápida, pero solo se puede usar para tablas temporales pequeñas y sencillas.</span><span class="sxs-lookup"><span data-stu-id="cdb51-279">This strategy is the fastest but can only be used for small, simple temporary tables.</span></span> <span data-ttu-id="cdb51-280">El segundo método consiste en crear una ordenación basada en disco que se puede controlar mediante un iterador de solo avance.</span><span class="sxs-lookup"><span data-stu-id="cdb51-280">The second method is to create a disk-based sort that can be driven using a forward-only iterator.</span></span> <span data-ttu-id="cdb51-281">Esta estrategia solo se puede usar en determinadas circunstancias y es la manera más rápida de ordenar y quitar duplicados de un conjunto de datos muy grande.</span><span class="sxs-lookup"><span data-stu-id="cdb51-281">This strategy can only be used under certain circumstances and is the fastest way to sort and remove duplicates from a very large data set.</span></span> <span data-ttu-id="cdb51-282">El tercer método consiste en crear un árbol B + en la base de datos temporal para almacenar la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="cdb51-282">The third method is to create a B+ Tree in the temporary database to hold the temporary table.</span></span> <span data-ttu-id="cdb51-283">Esta estrategia es la más lenta, pero la más versátil, y se conoce como una tabla temporal materializada.</span><span class="sxs-lookup"><span data-stu-id="cdb51-283">This strategy is the slowest, but the most versatile, and is referred to as a materialized temporary table.</span></span> <span data-ttu-id="cdb51-284">Estas estrategias se pueden usar en combinación para lograr en última instancia la funcionalidad solicitada de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="cdb51-284">These strategies may be used in combination to ultimately achieve the functionality requested of the temporary table.</span></span>

<span data-ttu-id="cdb51-285">Cuando la tabla temporal no se materializa, se usa en principalmente dos fases principales.</span><span class="sxs-lookup"><span data-stu-id="cdb51-285">When the temporary table is not materialized then it is used in primarily two major phases.</span></span> <span data-ttu-id="cdb51-286">La primera fase es la fase de inserción en la que la tabla se rellena con su conjunto de datos inicial.</span><span class="sxs-lookup"><span data-stu-id="cdb51-286">The first phase is the insertion phase where the table is populated with its initial data set.</span></span> <span data-ttu-id="cdb51-287">Durante esta fase, solo se permite la inserción de datos.</span><span class="sxs-lookup"><span data-stu-id="cdb51-287">During this phase, only data insertion is allowed.</span></span> <span data-ttu-id="cdb51-288">Esta fase finaliza cuando se realiza un intento de trasladar el cursor mediante [JetMove](./jetmove-function.md) o [JetSeek](./jetseek-function.md).</span><span class="sxs-lookup"><span data-stu-id="cdb51-288">This phase ends when an attempt is made to move the cursor using [JetMove](./jetmove-function.md) or [JetSeek](./jetseek-function.md).</span></span> <span data-ttu-id="cdb51-289">La segunda fase es la fase de extracción de datos.</span><span class="sxs-lookup"><span data-stu-id="cdb51-289">The second phase is the data extraction phase.</span></span> <span data-ttu-id="cdb51-290">Durante esta fase, los datos almacenados en la tabla temporal se pueden extraer según las capacidades solicitadas cuando se creó la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="cdb51-290">During this phase, the data stored in the temporary table may be extracted according to the capabilities requested when the temporary table was created.</span></span>

<span data-ttu-id="cdb51-291">**Funciones de cursor de tabla temporal**</span><span class="sxs-lookup"><span data-stu-id="cdb51-291">**Temporary Table Cursor Capabilities**</span></span>

<span data-ttu-id="cdb51-292">Cuando se materializa la tabla temporal, el cursor tiene las siguientes capacidades, pero puede estar más limitado por las opciones solicitadas:</span><span class="sxs-lookup"><span data-stu-id="cdb51-292">When the temporary table is materialized, the cursor has the following capabilities but may be further limited by the options requested:</span></span>

  - [<span data-ttu-id="cdb51-293">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="cdb51-293">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="cdb51-294">JetDelete</span><span class="sxs-lookup"><span data-stu-id="cdb51-294">JetDelete</span></span>](./jetdelete-function.md)

  - [<span data-ttu-id="cdb51-295">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="cdb51-295">JetDupCursor</span></span>](./jetdupcursor-function.md)

  - [<span data-ttu-id="cdb51-296">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="cdb51-296">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="cdb51-297">JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="cdb51-297">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)

  - [<span data-ttu-id="cdb51-298">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="cdb51-298">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="cdb51-299">JetGetCursorInfo</span><span class="sxs-lookup"><span data-stu-id="cdb51-299">JetGetCursorInfo</span></span>](./jetgetcursorinfo-function.md)

  - [<span data-ttu-id="cdb51-300">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="cdb51-300">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="cdb51-301">JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="cdb51-301">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)

  - [<span data-ttu-id="cdb51-302">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="cdb51-302">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="cdb51-303">JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="cdb51-303">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)

  - [<span data-ttu-id="cdb51-304">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="cdb51-304">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="cdb51-305">JetMove</span><span class="sxs-lookup"><span data-stu-id="cdb51-305">JetMove</span></span>](./jetmove-function.md)

  - [<span data-ttu-id="cdb51-306">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="cdb51-306">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)

  - [<span data-ttu-id="cdb51-307">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="cdb51-307">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="cdb51-308">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="cdb51-308">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="cdb51-309">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="cdb51-309">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="cdb51-310">JetSeek</span><span class="sxs-lookup"><span data-stu-id="cdb51-310">JetSeek</span></span>](./jetseek-function.md)

  - [<span data-ttu-id="cdb51-311">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="cdb51-311">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="cdb51-312">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="cdb51-312">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="cdb51-313">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="cdb51-313">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)

  - [<span data-ttu-id="cdb51-314">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="cdb51-314">JetSetLS</span></span>](./jetsetls-function.md)

  - [<span data-ttu-id="cdb51-315">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="cdb51-315">JetUpdate</span></span>](./jetupdate-function.md)

<span data-ttu-id="cdb51-316">Cuando la tabla temporal no se materializa y se encuentra en la fase de inserción, el cursor tiene las siguientes capacidades, pero puede estar más limitado por las opciones solicitadas:</span><span class="sxs-lookup"><span data-stu-id="cdb51-316">When the temporary table is not materialized and is in the insert phase, the cursor has the following capabilities but may be further limited by the options requested:</span></span>

  - [<span data-ttu-id="cdb51-317">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="cdb51-317">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="cdb51-318">JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="cdb51-318">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)

  - [<span data-ttu-id="cdb51-319">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="cdb51-319">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="cdb51-320">JetMove</span><span class="sxs-lookup"><span data-stu-id="cdb51-320">JetMove</span></span>](./jetmove-function.md)
    
    <span data-ttu-id="cdb51-321">**Nota:**  Provoca la transición a la fase de extracción.</span><span class="sxs-lookup"><span data-stu-id="cdb51-321">**Note**  Causes transition to the extract phase.</span></span>

  - [<span data-ttu-id="cdb51-322">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="cdb51-322">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)

  - [<span data-ttu-id="cdb51-323">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="cdb51-323">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="cdb51-324">JetSeek</span><span class="sxs-lookup"><span data-stu-id="cdb51-324">JetSeek</span></span>](./jetseek-function.md)
    
    <span data-ttu-id="cdb51-325">**Nota:**  Provoca la transición a la fase de extracción.</span><span class="sxs-lookup"><span data-stu-id="cdb51-325">**Note**  Causes transition to the extract phase.</span></span>

  - [<span data-ttu-id="cdb51-326">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="cdb51-326">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="cdb51-327">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="cdb51-327">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="cdb51-328">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="cdb51-328">JetUpdate</span></span>](./jetupdate-function.md)

<span data-ttu-id="cdb51-329">Cuando la tabla temporal no se materializa y se encuentra en la fase de extracción, el cursor tiene las siguientes capacidades, pero puede estar más limitado por las opciones solicitadas:</span><span class="sxs-lookup"><span data-stu-id="cdb51-329">When the temporary table is not materialized and is in the extract phase, the cursor has the following capabilities but may be further limited by the options requested:</span></span>

  - [<span data-ttu-id="cdb51-330">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="cdb51-330">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="cdb51-331">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="cdb51-331">JetDupCursor</span></span>](./jetdupcursor-function.md)
    
    <span data-ttu-id="cdb51-332">**Nota:**  Si se realiza un intento de duplicar una tabla temporal que está en modo de solo avance, el cursor resultante no se creará correctamente y dejará de funcionar.</span><span class="sxs-lookup"><span data-stu-id="cdb51-332">**Note**  If an attempt is made to duplicate a temporary table that is in forward-only mode then the resulting cursor will not be created properly and will malfunction.</span></span> <span data-ttu-id="cdb51-333">Todavía es seguro duplicar un cursor sobre una tabla temporal materializada.</span><span class="sxs-lookup"><span data-stu-id="cdb51-333">It is still safe to duplicate a cursor over a materialized temporary table.</span></span>

  - [<span data-ttu-id="cdb51-334">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="cdb51-334">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="cdb51-335">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="cdb51-335">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="cdb51-336">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="cdb51-336">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="cdb51-337">JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="cdb51-337">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)

  - [<span data-ttu-id="cdb51-338">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="cdb51-338">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="cdb51-339">JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="cdb51-339">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)

  - [<span data-ttu-id="cdb51-340">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="cdb51-340">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="cdb51-341">JetMove</span><span class="sxs-lookup"><span data-stu-id="cdb51-341">JetMove</span></span>](./jetmove-function.md)

  - [<span data-ttu-id="cdb51-342">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="cdb51-342">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="cdb51-343">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="cdb51-343">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="cdb51-344">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="cdb51-344">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="cdb51-345">JetSeek</span><span class="sxs-lookup"><span data-stu-id="cdb51-345">JetSeek</span></span>](./jetseek-function.md)

  - [<span data-ttu-id="cdb51-346">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="cdb51-346">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)

  - [<span data-ttu-id="cdb51-347">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="cdb51-347">JetSetLS</span></span>](./jetsetls-function.md)

#### <a name="requirements"></a><span data-ttu-id="cdb51-348">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdb51-348">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdb51-349"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="cdb51-349"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="cdb51-350">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="cdb51-350">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdb51-351"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="cdb51-351"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cdb51-352">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="cdb51-352">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdb51-353"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="cdb51-353"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="cdb51-354">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="cdb51-354">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdb51-355"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="cdb51-355"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="cdb51-356">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="cdb51-356">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdb51-357"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="cdb51-357"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="cdb51-358">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="cdb51-358">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="cdb51-359">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cdb51-359">See Also</span></span>

[<span data-ttu-id="cdb51-360">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="cdb51-360">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="cdb51-361">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="cdb51-361">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="cdb51-362">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="cdb51-362">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="cdb51-363">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="cdb51-363">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="cdb51-364">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="cdb51-364">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="cdb51-365">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="cdb51-365">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="cdb51-366">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="cdb51-366">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="cdb51-367">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="cdb51-367">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="cdb51-368">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="cdb51-368">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="cdb51-369">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="cdb51-369">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="cdb51-370">JetMove</span><span class="sxs-lookup"><span data-stu-id="cdb51-370">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="cdb51-371">JetRollback</span><span class="sxs-lookup"><span data-stu-id="cdb51-371">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="cdb51-372">JetSeek</span><span class="sxs-lookup"><span data-stu-id="cdb51-372">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="cdb51-373">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="cdb51-373">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="cdb51-374">Parámetros temporales de base de datos</span><span class="sxs-lookup"><span data-stu-id="cdb51-374">Temporary Database Parameters</span></span>](./temporary-database-parameters.md)
