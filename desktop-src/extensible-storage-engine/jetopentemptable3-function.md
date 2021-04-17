---
description: 'Más información acerca de: JetOpenTempTable3 (función)'
title: Función JetOpenTempTable3
TOCTitle: JetOpenTempTable3 Function
ms:assetid: 58d6e264-705e-402b-928f-96eefe5e9771
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269255(v=EXCHG.10)
ms:contentKeyID: 32765557
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable3
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7820f90ef0192c1f700759835bf1572b187cf3be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696216"
---
# <a name="jetopentemptable3-function"></a><span data-ttu-id="dc3a1-103">Función JetOpenTempTable3</span><span class="sxs-lookup"><span data-stu-id="dc3a1-103">JetOpenTempTable3 Function</span></span>


<span data-ttu-id="dc3a1-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="dc3a1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentemptable3-function"></a><span data-ttu-id="dc3a1-105">Función JetOpenTempTable3</span><span class="sxs-lookup"><span data-stu-id="dc3a1-105">JetOpenTempTable3 Function</span></span>

<span data-ttu-id="dc3a1-106">La función **JetOpenTempTable3** crea una tabla temporal con un índice único que se puede usar para almacenar y recuperar registros como una tabla normal creada con [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="dc3a1-106">The **JetOpenTempTable3** function creates a temporary table with a single index that can be used to store and retrieve records just like an ordinary table created using [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span> <span data-ttu-id="dc3a1-107">Sin embargo, las tablas temporales son mucho más rápidas que las normales debido a su naturaleza volátil.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-107">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="dc3a1-108">También se pueden usar para ordenar de forma muy rápida y realizar una eliminación duplicada en conjuntos de registros cuando se tiene acceso a ellos de forma puramente secuencial.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-108">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span>

```cpp
    JET_ERR JET_API JetOpenTempTable3(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in_opt      JET_UNICODEINDEX* pidxunicode,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a><span data-ttu-id="dc3a1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc3a1-109">Parameters</span></span>

<span data-ttu-id="dc3a1-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="dc3a1-110">*sesid*</span></span>

<span data-ttu-id="dc3a1-111">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-111">The session to use for this call.</span></span>

<span data-ttu-id="dc3a1-112">*prgcolumndef*</span><span class="sxs-lookup"><span data-stu-id="dc3a1-112">*prgcolumndef*</span></span>

<span data-ttu-id="dc3a1-113">Identifica las definiciones de columna de las columnas que se van a crear en la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-113">Identifies the column definitions of the columns to be created in the temporary table.</span></span>

<span data-ttu-id="dc3a1-114">Existen limitaciones importantes en las opciones de definición de columna que se pueden usar con una tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-114">Important limitations exist to the column definition options that may be used with a temporary table.</span></span> <span data-ttu-id="dc3a1-115">Vea la sección Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-115">See the Remarks section for more information.</span></span>

<span data-ttu-id="dc3a1-116">Además de las opciones de definición de columna habituales, también se pueden especificar cero o más de las opciones siguientes que solo son relevantes en el contexto de una tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-116">In addition to the usual column definition options, zero or more of the following options may also be specified that are relevant only in the context of a temporary table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dc3a1-117">Value</span><span class="sxs-lookup"><span data-stu-id="dc3a1-117">Value</span></span></p></th>
<th><p><span data-ttu-id="dc3a1-118">Significado</span><span class="sxs-lookup"><span data-stu-id="dc3a1-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc3a1-119">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="dc3a1-119">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-120">Esta opción indica que el criterio de ordenación de la columna de clave para la tabla temporal debe ser descendente en lugar de ascendente.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-120">This option indicates that the sort order of the key column for the temporary table should be descending rather than ascending.</span></span> <span data-ttu-id="dc3a1-121">Si se especifica esta opción sin JET_bitColumnTTKey, se omite esta opción.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-121">If this option is specified without JET_bitColumnTTKey then this option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc3a1-122">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="dc3a1-122">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-123">Esta opción indica que la columna será una columna de clave para la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-123">This option indicates that the column will be a key column for the temporary table.</span></span></p>
<p><span data-ttu-id="dc3a1-124">El orden de las definiciones de columna con esta opción especificada en la matriz de entrada determinará la prioridad de cada columna de clave para la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-124">The order of the column definitions with this option specified in the input array will determine the precedence of each key column for the temporary table.</span></span> <span data-ttu-id="dc3a1-125">La primera definición de columna de la matriz con esta opción establecida será la columna de clave más significativa, etc.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-125">The first column definition in the array with this option set will be the most significant key column and so on.</span></span> <span data-ttu-id="dc3a1-126">Si se solicitan más columnas de clave de las que puede admitir el motor de base de datos, esta opción se omite para las columnas de clave no admitidas.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-126">If more key columns are requested than can be supported by the database engine then this option is ignored for the unsupportable key columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dc3a1-127">*ccolumn*</span><span class="sxs-lookup"><span data-stu-id="dc3a1-127">*ccolumn*</span></span>

<span data-ttu-id="dc3a1-128">Vea *prgcolumndef*.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-128">See *prgcolumndef*.</span></span>

<span data-ttu-id="dc3a1-129">*pidxunicode*</span><span class="sxs-lookup"><span data-stu-id="dc3a1-129">*pidxunicode*</span></span>

<span data-ttu-id="dc3a1-130">El identificador de configuración regional y las marcas de normalización que se utilizarán para comparar los datos de columna de clave Unicode en la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-130">The Locale ID and normalization flags that will be used to compare any Unicode key column data in the temporary table.</span></span>

<span data-ttu-id="dc3a1-131">Cuando este parámetro no está presente, se usará el LCID predeterminado para comparar las columnas de clave Unicode de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-131">When this parameter is not present then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="dc3a1-132">El LCID predeterminado es la configuración regional en Inglés de EE. UU.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-132">The default LCID is the U.S. English locale.</span></span>

<span data-ttu-id="dc3a1-133">Cuando este parámetro no está presente, se usarán las marcas de normalización predeterminadas para comparar los datos de columna de clave Unicode en la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-133">When this parameter is not present then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="dc3a1-134">Las marcas de normalización predeterminadas son: NORM_IGNORECASE, NORM_IGNOREKANATYPE y NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-134">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span>

<span data-ttu-id="dc3a1-135">*grbit*</span><span class="sxs-lookup"><span data-stu-id="dc3a1-135">*grbit*</span></span>

<span data-ttu-id="dc3a1-136">Grupo de bits que contiene las opciones que se van a usar para esta llamada, que incluyen cero o más de los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-136">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dc3a1-137">Value</span><span class="sxs-lookup"><span data-stu-id="dc3a1-137">Value</span></span></p></th>
<th><p><span data-ttu-id="dc3a1-138">Significado</span><span class="sxs-lookup"><span data-stu-id="dc3a1-138">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc3a1-139">JET_bitTTErrorOnDuplicateInsertion</span><span class="sxs-lookup"><span data-stu-id="dc3a1-139">JET_bitTTErrorOnDuplicateInsertion</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-140">Esta opción solicita que se produzca inmediatamente un error al intentar insertar un registro con la misma clave de índice que un registro insertado previamente con JET_errKeyDuplicate.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-140">This option requests that any attempt to insert a record with the same index key as a previously inserted record will immediately fail with JET_errKeyDuplicate.</span></span> <span data-ttu-id="dc3a1-141">Si no se solicita esta opción, un duplicado puede detectarse inmediatamente y producir un error, o bien se puede quitar de forma silenciosa más adelante según la estrategia elegida por el motor de base de datos para implementar la tabla temporal en función de la funcionalidad solicitada.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-141">If this option is not requested then a duplicate may be detected immediately and fail or may be silently removed later depending on the strategy chosen by the database engine to implement the temporary table based on the requested functionality.</span></span></p>
<p><span data-ttu-id="dc3a1-142">Si esta funcionalidad no es necesaria, es mejor no solicitarlo.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-142">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="dc3a1-143">Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-143">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc3a1-144">JET_bitTTForceMaterialization</span><span class="sxs-lookup"><span data-stu-id="dc3a1-144">JET_bitTTForceMaterialization</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-145">Esta opción obliga al administrador de tablas temporales a abandonar cualquier intento de elegir una estrategia de Clever para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-145">This option forces the temporary table manager to abandon any attempt to choose a clever strategy for managing the temporary table that will result in enhanced performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc3a1-146">JET_bitTTForwardOnly</span><span class="sxs-lookup"><span data-stu-id="dc3a1-146">JET_bitTTForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-147">Esta opción solicita que la tabla temporal se cree solo si el administrador de tablas temporales puede usar la implementación optimizada para los resultados intermedios de la consulta.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-147">This option requests that the temporary table only be created if the temporary table manager can use the implementation optimized for intermediate query results.</span></span> <span data-ttu-id="dc3a1-148">Si alguna característica de la tabla temporal impidiera el uso de esta optimización, la operación producirá un error con JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-148">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span></p>
<p><span data-ttu-id="dc3a1-149">Un efecto secundario de esta opción es permitir que la tabla temporal contenga registros con claves de índice duplicadas.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-149">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="dc3a1-150">Consulte JET_bitTTUnique para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-150">See JET_bitTTUnique for more information.</span></span></p>
<p><span data-ttu-id="dc3a1-151">Esta opción solo está disponible en Windows Server 2003 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-151">This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc3a1-152">JET_bitTTIndexed</span><span class="sxs-lookup"><span data-stu-id="dc3a1-152">JET_bitTTIndexed</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-153">Esta opción solicita que la tabla temporal sea lo suficientemente flexible como para permitir el uso de <a href="gg294103(v=exchg.10).md">JetSeek</a> para buscar registros por clave de índice.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-153">This option requests that the temporary table be flexible enough to permit the use of <a href="gg294103(v=exchg.10).md">JetSeek</a> to look up records by index key.</span></span></p>
<p><span data-ttu-id="dc3a1-154">Si esta funcionalidad no es necesaria, es mejor no solicitarlo.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-154">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="dc3a1-155">Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-155">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc3a1-156">JET_bitTTUnique</span><span class="sxs-lookup"><span data-stu-id="dc3a1-156">JET_bitTTUnique</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-157">Esta opción solicita que los registros con claves de índice duplicadas se quiten del conjunto final de registros de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-157">This option requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span></p>
<p><span data-ttu-id="dc3a1-158">Antes de Windows Server 2003, el motor de base de datos siempre asumió que esta opción está en vigor debido al hecho de que todos los índices clúster también deben ser una clave principal y, por tanto, deben ser únicos.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-158">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="dc3a1-159">A partir de Windows Server 2003, ahora es posible crear una tabla temporal que no quita los duplicados cuando también se especifica la opción de JET_bitTTForwardOnly.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-159">As of Windows Server 2003, it is now possible to create a temporary table that does NOT remove duplicates when the JET_bitTTForwardOnly option is also specified.</span></span></p>
<p><span data-ttu-id="dc3a1-160">No es posible saber qué duplicado ganará y qué duplicados se descartarán en general.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-160">It is not possible to know which duplicate will win and which duplicates will be discarded in general.</span></span> <span data-ttu-id="dc3a1-161">Sin embargo, cuando se solicita la opción de JET_bitTTErrorOnDuplicateInsertion, el primer registro con una clave de índice determinada que se va a insertar en la tabla temporal siempre ganará.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-161">However, when the JET_bitTTErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always win.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc3a1-162">JET_bitTTUpdatable</span><span class="sxs-lookup"><span data-stu-id="dc3a1-162">JET_bitTTUpdatable</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-163">Esta opción solicita que la tabla temporal sea lo suficientemente flexible como para permitir que se modifiquen posteriormente los registros que se han insertado previamente.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-163">This option requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="dc3a1-164">Si esta funcionalidad no es necesaria, es mejor no solicitarlo.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-164">If this functionality it not required then it is best to not request it.</span></span></p>
<p><span data-ttu-id="dc3a1-165">Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-165">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc3a1-166">JET_bitTTScrollable</span><span class="sxs-lookup"><span data-stu-id="dc3a1-166">JET_bitTTScrollable</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-167">Esta opción solicita que la tabla temporal sea lo suficientemente flexible como para permitir que los registros se examinen en orden y dirección arbitrarios con <a href="gg294117(v=exchg.10).md">JetMove</a>.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-167">This option requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p>
<p><span data-ttu-id="dc3a1-168">Si esta funcionalidad no es necesaria, es mejor no solicitarlo.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-168">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="dc3a1-169">Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-169">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc3a1-170">JET_bitTTSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="dc3a1-170">JET_bitTTSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-171">Esta opción solicita que los valores de columna de clave NULL se ordenen más cerca del final del índice que los valores de columna de clave no NULL.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-171">This option requests that NULL key column values sort closer to the end of the index than non-NULL key column values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc3a1-172">JET_bitTTIntrinsicLVsOnly</span><span class="sxs-lookup"><span data-stu-id="dc3a1-172">JET_bitTTIntrinsicLVsOnly</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-173">Solicitudes para permitir solo valores largos intrínsecos.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-173">Requests to permit only intrinsic long values.</span></span></p>
<p><span data-ttu-id="dc3a1-174"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> se introduce en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-174"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dc3a1-175">*ptableid*</span><span class="sxs-lookup"><span data-stu-id="dc3a1-175">*ptableid*</span></span>

<span data-ttu-id="dc3a1-176">Búfer de salida que recibirá el nuevo cursor abierto en la tabla temporal recién creada.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-176">The output buffer that will receive the new cursor opened on the newly created temporary table.</span></span>

<span data-ttu-id="dc3a1-177">*prgcolumnid*</span><span class="sxs-lookup"><span data-stu-id="dc3a1-177">*prgcolumnid*</span></span>

<span data-ttu-id="dc3a1-178">Búfer de salida que recibirá la matriz de identificadores de columna generados durante la creación de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-178">The output buffer that will receive the array of column IDs generated during the creation of the temporary table.</span></span>

<span data-ttu-id="dc3a1-179">Los identificadores de columna de esta matriz se corresponden exactamente con la matriz de entrada de definiciones de columna.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-179">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="dc3a1-180">Como resultado, el tamaño de este búfer debe corresponder al tamaño de la matriz de entrada.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-180">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

### <a name="return-value"></a><span data-ttu-id="dc3a1-181">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc3a1-181">Return Value</span></span>

<span data-ttu-id="dc3a1-182">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-182">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="dc3a1-183">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="dc3a1-183">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dc3a1-184">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="dc3a1-184">Return code</span></span></p></th>
<th><p><span data-ttu-id="dc3a1-185">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc3a1-185">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc3a1-186">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="dc3a1-186">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-187">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-187">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc3a1-188">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="dc3a1-188">JET_errCannotMaterializeForwardOnlySort</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-189">Error de <strong>JetOpenTempTable3</strong> porque se especificó JET_bitTTForwardOnly y no se pudo crear la tabla temporal tal y como se especificó mediante la optimización de solo avance.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-189"><strong>JetOpenTempTable3</strong> failed because JET_bitTTForwardOnly was specified and the temporary table as specified could not be created using the forward-only optimization.</span></span> <span data-ttu-id="dc3a1-190">Este error solo lo devolverán Windows Server 2003 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-190">This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc3a1-191">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="dc3a1-191">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-192">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-192">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc3a1-193">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="dc3a1-193">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-194">No se pudo crear el índice porque se especificó una definición de índice no válida.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-194">The index could not be created because an invalid index definition was specified.</span></span> <span data-ttu-id="dc3a1-195"><strong>JetOpenTempTable3</strong> devolverá este error cuando:</span><span class="sxs-lookup"><span data-stu-id="dc3a1-195"><strong>JetOpenTempTable3</strong> will return this error when:</span></span></p>
<ul>
<li><p><span data-ttu-id="dc3a1-196">Se especifica la configuración regional independiente del idioma.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-196">The Language Neutral locale is specified.</span></span></p></li>
<li><p><span data-ttu-id="dc3a1-197">Se especifica un conjunto no válido de marcas de normalización.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-197">An invalid set of normalization flags is specified.</span></span></p></li>
</ul>
<p><span data-ttu-id="dc3a1-198">Este error solo lo devolverá Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-198">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc3a1-199">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="dc3a1-199">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-200">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-200">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="dc3a1-201">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-201">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc3a1-202">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="dc3a1-202">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-203">El miembro <strong>CP</strong> de la estructura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> no se ha establecido en una página de códigos válida.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-203">The <strong>cp</strong> member of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="dc3a1-204">Los únicos valores válidos para las columnas de texto son inglés (1252) y Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="dc3a1-204">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="dc3a1-205">Un valor de 0 significa que se usará el valor predeterminado (Inglés, 1252).</span><span class="sxs-lookup"><span data-stu-id="dc3a1-205">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc3a1-206">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="dc3a1-206">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-207">El miembro <strong>coltyp</strong> de la estructura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> no se ha establecido en un tipo de columna válido.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-207">The <strong>coltyp</strong> member of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc3a1-208">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="dc3a1-208">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-209">No se pudo crear el índice porque se intentó usar un ID. de configuración regional no válido.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-209">The index could not be created because an attempt was made to use an invalid locale ID.</span></span> <span data-ttu-id="dc3a1-210">Es posible que el ID. de configuración regional no sea válido o que el paquete de idioma asociado no esté instalado.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-210">The locale ID may either be completely invalid or the associated language pack may not be installed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc3a1-211">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="dc3a1-211">JET_errInvalidLCMapStringFlags</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-212">No se pudo crear el índice porque se intentó usar un conjunto no válido de marcas de normalización.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-212">The index could not be created because an attempt was made to use an invalid set of normalization flags.</span></span> <span data-ttu-id="dc3a1-213">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-213">This error will only be returned by Windows XP and later releases.</span></span> <span data-ttu-id="dc3a1-214">En Windows 2000, las marcas de normalización no válidas producirán JET_errIndexInvalidDef en su lugar.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-214">On Windows 2000, invalid normalization flags will result in JET_errIndexInvalidDef instead.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc3a1-215">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="dc3a1-215">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-216">El identificador de sesión no es válido o hace referencia a una sesión cerrada.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-216">The session handle is invalid or refers to a closed session.</span></span> <span data-ttu-id="dc3a1-217">Este error no se devuelve en todas las circunstancias.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-217">This error is not returned under all circumstances.</span></span> <span data-ttu-id="dc3a1-218">Los identificadores se validan solo en función del mejor esfuerzo.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-218">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc3a1-219">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="dc3a1-219">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-220">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-220">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc3a1-221">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="dc3a1-221">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-222">No se pudo realizar la operación porque el motor no puede asignar los recursos necesarios para abrir un nuevo cursor.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-222">The operation failed because the engine cannot allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="dc3a1-223">Los recursos de cursor se configuran mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-223">Cursor resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc3a1-224">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="dc3a1-224">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-225">No se pudo realizar la operación porque no se pudo asignar suficiente memoria para completarla.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-225">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="dc3a1-226"><strong>JetOpenTempTable3</strong> puede devolver JET_errOutOfMemory si el espacio de direcciones del proceso de host está demasiado fragmentado.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-226"><strong>JetOpenTempTable3</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="dc3a1-227">El administrador de tablas temporales asignará siempre un fragmento de 1 MB de espacio de direcciones para cada tabla temporal creada independientemente de la cantidad de datos que se van a almacenar.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-227">The temporary table manager will always allocate a 1MB chunk of address space for every temporary table created regardless of the amount of data to be stored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc3a1-228">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="dc3a1-228">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-229">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-229">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc3a1-230">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="dc3a1-230">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-231">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-231">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="dc3a1-232">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-232">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc3a1-233">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="dc3a1-233">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-234">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-234">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc3a1-235">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="dc3a1-235">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-236">Se intentó agregar demasiadas columnas a la tabla.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-236">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="dc3a1-237">Una tabla no puede tener más de JET_ccolFixedMost columnas fijas, ni más de JET_ccolVarMost columnas de longitud variable, ni más de JET_ccolTaggedMost columnas etiquetadas.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-237">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc3a1-238">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="dc3a1-238">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-239">No se pudo realizar la operación porque el motor no puede asignar los recursos necesarios para almacenar en memoria caché los índices de la tabla.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-239">The operation failed because the engine cannot allocate the resources required to cache the indexes of the table.</span></span> <span data-ttu-id="dc3a1-240">El número de índices cuyo esquema se puede almacenar en caché se configura mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-240">The number of indexes whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc3a1-241">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="dc3a1-241">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-242">No se pudo realizar la operación porque el motor no puede asignar los recursos necesarios para almacenar en caché el esquema de la tabla.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-242">The operation failed because the engine cannot allocate the resources required to cache the schema of the table.</span></span> <span data-ttu-id="dc3a1-243">El número de tablas cuyo esquema se puede almacenar en caché se configura mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-243">The number of tables whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc3a1-244">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="dc3a1-244">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="dc3a1-245">No se pudo realizar la operación porque el motor no puede asignar los recursos necesarios para crear una tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-245">The operation failed because the engine cannot allocate the resources required to create a temporary table.</span></span> <span data-ttu-id="dc3a1-246">Los recursos de tabla temporal se configuran mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-246">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dc3a1-247">Si se ejecuta correctamente, se devolverá un cursor abierto en la tabla temporal recién creada.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-247">On success, a cursor opened on the newly created temporary table will be returned.</span></span> <span data-ttu-id="dc3a1-248">El estado de la base de datos temporal se preparará para contener la nueva tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-248">The state of the temporary database will be prepared to contain the new temporary table.</span></span> <span data-ttu-id="dc3a1-249">El estado de las bases de datos normales que use el motor de base de datos permanecerá sin cambios.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-249">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

<span data-ttu-id="dc3a1-250">En caso de error, no se creará la tabla temporal y no se devolverá un cursor.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-250">On failure, the temporary table will not be created and a cursor will not be returned.</span></span> <span data-ttu-id="dc3a1-251">Se puede cambiar el estado de la base de datos temporal.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-251">The state of the temporary database may be changed.</span></span> <span data-ttu-id="dc3a1-252">El estado de las bases de datos normales que use el motor de base de datos permanecerá sin cambios.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-252">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

#### <a name="requirements"></a><span data-ttu-id="dc3a1-253">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc3a1-253">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc3a1-254"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="dc3a1-254"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="dc3a1-255">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-255">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc3a1-256"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="dc3a1-256"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="dc3a1-257">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-257">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc3a1-258"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="dc3a1-258"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="dc3a1-259">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-259">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc3a1-260"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="dc3a1-260"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="dc3a1-261">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-261">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc3a1-262"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="dc3a1-262"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="dc3a1-263">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-263">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="dc3a1-264">Consulte también</span><span class="sxs-lookup"><span data-stu-id="dc3a1-264">See Also</span></span>

[<span data-ttu-id="dc3a1-265">Errores del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="dc3a1-265">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="dc3a1-266">Parámetros de control de errores</span><span class="sxs-lookup"><span data-stu-id="dc3a1-266">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="dc3a1-267">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="dc3a1-267">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="dc3a1-268">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="dc3a1-268">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="dc3a1-269">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="dc3a1-269">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="dc3a1-270">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="dc3a1-270">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="dc3a1-271">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="dc3a1-271">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="dc3a1-272">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="dc3a1-272">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="dc3a1-273">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="dc3a1-273">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="dc3a1-274">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="dc3a1-274">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="dc3a1-275">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="dc3a1-275">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="dc3a1-276">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="dc3a1-276">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="dc3a1-277">JetMove</span><span class="sxs-lookup"><span data-stu-id="dc3a1-277">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="dc3a1-278">JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="dc3a1-278">JetOpenTempTable</span></span>](./jetopentemptable-function.md)  
[<span data-ttu-id="dc3a1-279">JetRollback</span><span class="sxs-lookup"><span data-stu-id="dc3a1-279">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="dc3a1-280">JetSeek</span><span class="sxs-lookup"><span data-stu-id="dc3a1-280">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="dc3a1-281">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="dc3a1-281">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="dc3a1-282">Parámetros del sistema</span><span class="sxs-lookup"><span data-stu-id="dc3a1-282">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
