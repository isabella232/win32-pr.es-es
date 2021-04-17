---
description: 'Más información acerca de: JetOpenTempTable2 (función)'
title: Función JetOpenTempTable2
TOCTitle: JetOpenTempTable2 Function
ms:assetid: 788ec4f9-b0c3-409b-850c-7567dec47024
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269302(v=EXCHG.10)
ms:contentKeyID: 32765594
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 324bcde75c0ba9376c8ad9f5e98df585b1d341e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697442"
---
# <a name="jetopentemptable2-function"></a><span data-ttu-id="9edd7-103">Función JetOpenTempTable2</span><span class="sxs-lookup"><span data-stu-id="9edd7-103">JetOpenTempTable2 Function</span></span>


<span data-ttu-id="9edd7-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9edd7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentemptable2-function"></a><span data-ttu-id="9edd7-105">Función JetOpenTempTable2</span><span class="sxs-lookup"><span data-stu-id="9edd7-105">JetOpenTempTable2 Function</span></span>

<span data-ttu-id="9edd7-106">La función **JetOpenTempTable2** crea una tabla temporal con un índice único que se puede usar para almacenar y recuperar registros como una tabla normal creada con [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="9edd7-106">The **JetOpenTempTable2** function creates a temporary table with a single index that can be used to store and retrieve records just like an ordinary table created using [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span> <span data-ttu-id="9edd7-107">Esta función también tiene un identificador de configuración regional que se puede utilizar para comparar los datos de la columna de clave Unicode en la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="9edd7-107">This function also has a Locale ID that can be used to compare Unicode key column data in the temporary table.</span></span> <span data-ttu-id="9edd7-108">Sin embargo, las tablas temporales son mucho más rápidas que las normales debido a su naturaleza volátil.</span><span class="sxs-lookup"><span data-stu-id="9edd7-108">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="9edd7-109">También se pueden usar para ordenar de forma muy rápida y realizar una eliminación duplicada en conjuntos de registros cuando se tiene acceso a ellos de forma puramente secuencial.</span><span class="sxs-lookup"><span data-stu-id="9edd7-109">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span>

```cpp
    JET_ERR JET_API JetOpenTempTable2(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in          unsigned long lcid,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a><span data-ttu-id="9edd7-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9edd7-110">Parameters</span></span>

<span data-ttu-id="9edd7-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="9edd7-111">*sesid*</span></span>

<span data-ttu-id="9edd7-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="9edd7-112">The session to use.</span></span>

<span data-ttu-id="9edd7-113">*prgcolumndef*</span><span class="sxs-lookup"><span data-stu-id="9edd7-113">*prgcolumndef*</span></span>

<span data-ttu-id="9edd7-114">Definiciones de columna de las columnas que se van a crear en la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="9edd7-114">The column definitions of the columns to be created in the temporary table.</span></span>

<span data-ttu-id="9edd7-115">Existen limitaciones importantes para las opciones de definición de columna que se utilizan con una tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="9edd7-115">Important limitations exist for the column definition options that are used with a temporary table.</span></span> <span data-ttu-id="9edd7-116">Vea la sección Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="9edd7-116">See the Remarks section for more information.</span></span>

<span data-ttu-id="9edd7-117">Además de las opciones de definición de columna habituales, también se pueden especificar cero o más de las opciones siguientes que solo son relevantes en el contexto de una tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="9edd7-117">In addition to the usual column definition options, zero or more of the following options can also be specified that are relevant only in the context of a temporary table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9edd7-118">Value</span><span class="sxs-lookup"><span data-stu-id="9edd7-118">Value</span></span></p></th>
<th><p><span data-ttu-id="9edd7-119">Significado</span><span class="sxs-lookup"><span data-stu-id="9edd7-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9edd7-120">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="9edd7-120">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="9edd7-121">El criterio de ordenación de la columna de clave para la tabla temporal debe ser descendente en lugar de ascendente.</span><span class="sxs-lookup"><span data-stu-id="9edd7-121">The sort order of the key column for the temporary table should be descending rather than ascending.</span></span> <span data-ttu-id="9edd7-122">Si se especifica esta opción sin JET_bitColumnTTKey, se omite esta opción.</span><span class="sxs-lookup"><span data-stu-id="9edd7-122">If this option is specified without JET_bitColumnTTKey then this option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9edd7-123">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="9edd7-123">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="9edd7-124">La columna será una columna de clave para la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="9edd7-124">The column will be a key column for the temporary table.</span></span></p>
<p><span data-ttu-id="9edd7-125">El orden de las definiciones de columna con esta opción especificada en la matriz de entrada determinará la prioridad de cada columna de clave para la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="9edd7-125">The order of the column definitions with this option specified in the input array will determine the precedence of each key column for the temporary table.</span></span> <span data-ttu-id="9edd7-126">La primera definición de columna de la matriz con esta opción establecida será la columna de clave más significativa, etc.</span><span class="sxs-lookup"><span data-stu-id="9edd7-126">The first column definition in the array with this option set will be the most significant key column and so on.</span></span> <span data-ttu-id="9edd7-127">Si se solicitan más columnas de clave de las que puede admitir el motor de base de datos, esta opción se omite para las columnas de clave no admitidas.</span><span class="sxs-lookup"><span data-stu-id="9edd7-127">If more key columns are requested than can be supported by the database engine then this option is ignored for the unsupportable key columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9edd7-128">*ccolumn*</span><span class="sxs-lookup"><span data-stu-id="9edd7-128">*ccolumn*</span></span>

<span data-ttu-id="9edd7-129">Vea *prgcolumndef*.</span><span class="sxs-lookup"><span data-stu-id="9edd7-129">See *prgcolumndef*.</span></span>

<span data-ttu-id="9edd7-130">*lcid*</span><span class="sxs-lookup"><span data-stu-id="9edd7-130">*lcid*</span></span>

<span data-ttu-id="9edd7-131">IDENTIFICADOR de configuración regional que se va a usar para comparar los datos de columna de clave Unicode de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="9edd7-131">The locale ID to use to compare any Unicode key column data in the temporary table.</span></span>

<span data-ttu-id="9edd7-132">Se puede usar cualquier configuración regional siempre que se haya instalado en el equipo el paquete de idioma adecuado.</span><span class="sxs-lookup"><span data-stu-id="9edd7-132">Any locale may be used as long as the appropriate language pack has been installed on the machine.</span></span> <span data-ttu-id="9edd7-133">La única excepción es que la configuración regional neutra de idioma (LCID de cero) no es válida.</span><span class="sxs-lookup"><span data-stu-id="9edd7-133">The one exception is that the Language Neutral locale (LCID of zero) is illegal.</span></span>

<span data-ttu-id="9edd7-134">En Windows Server 2003 y versiones posteriores, si se especifica la configuración regional neutra de idioma para este parámetro, se usará en su lugar el ID. de configuración regional predeterminado (Inglés de EE. UU.).</span><span class="sxs-lookup"><span data-stu-id="9edd7-134">On Windows Server 2003 and later, if the Language Neutral locale is specified for this parameter then the default locale ID (U.S. English) will be used instead.</span></span> <span data-ttu-id="9edd7-135">Esto es para permitir un valor de cero para indicar el valor predeterminado en lugar de un valor no válido.</span><span class="sxs-lookup"><span data-stu-id="9edd7-135">This is to allow a value of zero to signify the default rather than an illegal value.</span></span>

<span data-ttu-id="9edd7-136">Cuando este parámetro no está presente y cuando el parámetro *pidxunicode* no está presente, se usará el LCID predeterminado para comparar los datos de columna de clave Unicode en la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="9edd7-136">When this parameter is not present and when the *pidxunicode* parameter is not present, then the default LCID will be used to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="9edd7-137">El LCID predeterminado es la configuración regional en Inglés de EE. UU.</span><span class="sxs-lookup"><span data-stu-id="9edd7-137">The default LCID is the U.S. English locale.</span></span>

<span data-ttu-id="9edd7-138">*grbit*</span><span class="sxs-lookup"><span data-stu-id="9edd7-138">*grbit*</span></span>

<span data-ttu-id="9edd7-139">Grupo de bits que contiene las opciones que se van a usar para esta llamada, que incluyen cero o más de los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="9edd7-139">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9edd7-140">Value</span><span class="sxs-lookup"><span data-stu-id="9edd7-140">Value</span></span></p></th>
<th><p><span data-ttu-id="9edd7-141">Significado</span><span class="sxs-lookup"><span data-stu-id="9edd7-141">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9edd7-142">JET_bitTTErrorOnDuplicateInsertion</span><span class="sxs-lookup"><span data-stu-id="9edd7-142">JET_bitTTErrorOnDuplicateInsertion</span></span></p></td>
<td><p><span data-ttu-id="9edd7-143">Esta opción solicita que se produzca inmediatamente un error al intentar insertar un registro con la misma clave de índice que un registro insertado previamente con JET_errKeyDuplicate.</span><span class="sxs-lookup"><span data-stu-id="9edd7-143">This option requests that any attempt to insert a record with the same index key as a previously inserted record will immediately fail with JET_errKeyDuplicate.</span></span> <span data-ttu-id="9edd7-144">Si no se solicita esta opción, un duplicado puede detectarse inmediatamente y producir un error, o bien se puede quitar de forma silenciosa más adelante según la estrategia elegida por el motor de base de datos para implementar la tabla temporal en función de la funcionalidad solicitada.</span><span class="sxs-lookup"><span data-stu-id="9edd7-144">If this option is not requested then a duplicate may be detected immediately and fail or may be silently removed later depending on the strategy chosen by the database engine to implement the temporary table based on the requested functionality.</span></span></p>
<p><span data-ttu-id="9edd7-145">Si esta funcionalidad no es necesaria, es mejor no solicitarlo.</span><span class="sxs-lookup"><span data-stu-id="9edd7-145">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="9edd7-146">Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</span><span class="sxs-lookup"><span data-stu-id="9edd7-146">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9edd7-147">JET_bitTTForceMaterialization</span><span class="sxs-lookup"><span data-stu-id="9edd7-147">JET_bitTTForceMaterialization</span></span></p></td>
<td><p><span data-ttu-id="9edd7-148">Esta opción obliga al administrador de tablas temporales a abandonar cualquier intento de elegir una estrategia de Clever para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</span><span class="sxs-lookup"><span data-stu-id="9edd7-148">This option forces the temporary table manager to abandon any attempt to choose a clever strategy for managing the temporary table that will result in enhanced performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9edd7-149">JET_bitTTForwardOnly</span><span class="sxs-lookup"><span data-stu-id="9edd7-149">JET_bitTTForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="9edd7-150">Esta opción solicita que la tabla temporal se cree solo si el administrador de tablas temporales puede usar la implementación optimizada para los resultados intermedios de la consulta.</span><span class="sxs-lookup"><span data-stu-id="9edd7-150">This option requests that the temporary table only be created if the temporary table manager can use the implementation optimized for intermediate query results.</span></span> <span data-ttu-id="9edd7-151">Si alguna característica de la tabla temporal impidiera el uso de esta optimización, la operación producirá un error con JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="9edd7-151">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span></p>
<p><span data-ttu-id="9edd7-152">Un efecto secundario de esta opción es permitir que la tabla temporal contenga registros con claves de índice duplicadas.</span><span class="sxs-lookup"><span data-stu-id="9edd7-152">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="9edd7-153">Consulte JET_bitTTUnique para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="9edd7-153">See JET_bitTTUnique for more information.</span></span></p>
<p><span data-ttu-id="9edd7-154">Esta opción solo está disponible en Windows Server 2003 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="9edd7-154">This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9edd7-155">JET_bitTTIndexed</span><span class="sxs-lookup"><span data-stu-id="9edd7-155">JET_bitTTIndexed</span></span></p></td>
<td><p><span data-ttu-id="9edd7-156">Esta opción solicita que la tabla temporal sea lo suficientemente flexible como para permitir el uso de <a href="gg294103(v=exchg.10).md">JetSeek</a> para buscar registros por clave de índice.</span><span class="sxs-lookup"><span data-stu-id="9edd7-156">This option requests that the temporary table be flexible enough to permit the use of <a href="gg294103(v=exchg.10).md">JetSeek</a> to look up records by index key.</span></span></p>
<p><span data-ttu-id="9edd7-157">Si esta funcionalidad no es necesaria, es mejor no solicitarlo.</span><span class="sxs-lookup"><span data-stu-id="9edd7-157">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="9edd7-158">Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</span><span class="sxs-lookup"><span data-stu-id="9edd7-158">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9edd7-159">JET_bitTTScrollable</span><span class="sxs-lookup"><span data-stu-id="9edd7-159">JET_bitTTScrollable</span></span></p></td>
<td><p><span data-ttu-id="9edd7-160">Esta opción solicita que la tabla temporal sea lo suficientemente flexible como para permitir que los registros se examinen en orden y dirección arbitrarios con <a href="gg294117(v=exchg.10).md">JetMove</a>.</span><span class="sxs-lookup"><span data-stu-id="9edd7-160">This option requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p>
<p><span data-ttu-id="9edd7-161">Si esta funcionalidad no es necesaria, es mejor no solicitarlo.</span><span class="sxs-lookup"><span data-stu-id="9edd7-161">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="9edd7-162">Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</span><span class="sxs-lookup"><span data-stu-id="9edd7-162">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9edd7-163">JET_bitTTSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="9edd7-163">JET_bitTTSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="9edd7-164">Esta opción solicita que los valores de columna de clave NULL se ordenen más cerca del final del índice que los valores de columna de clave no NULL.</span><span class="sxs-lookup"><span data-stu-id="9edd7-164">This option requests that NULL key column values sort closer to the end of the index than non-NULL key column values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9edd7-165">JET_bitTTUnique</span><span class="sxs-lookup"><span data-stu-id="9edd7-165">JET_bitTTUnique</span></span></p></td>
<td><p><span data-ttu-id="9edd7-166">Esta opción solicita que los registros con claves de índice duplicadas se quiten del conjunto final de registros de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="9edd7-166">This option requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span></p>
<p><span data-ttu-id="9edd7-167">Antes de Windows Server 2003, el motor de base de datos siempre asumió que esta opción está en vigor debido al hecho de que todos los índices clúster también deben ser una clave principal y, por tanto, deben ser únicos.</span><span class="sxs-lookup"><span data-stu-id="9edd7-167">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="9edd7-168">A partir de Windows Server 2003, ahora es posible crear una tabla temporal que no quita los duplicados cuando también se especifica la opción de JET_bitTTForwardOnly.</span><span class="sxs-lookup"><span data-stu-id="9edd7-168">As of Windows Server 2003, it is now possible to create a temporary table that does NOT remove duplicates when the JET_bitTTForwardOnly option is also specified.</span></span></p>
<p><span data-ttu-id="9edd7-169">No es posible saber qué duplicado ganará y qué duplicados se descartarán en general.</span><span class="sxs-lookup"><span data-stu-id="9edd7-169">It is not possible to know which duplicate will win and which duplicates will be discarded in general.</span></span> <span data-ttu-id="9edd7-170">Sin embargo, cuando se solicita la opción de JET_bitTTErrorOnDuplicateInsertion, el primer registro con una clave de índice determinada que se va a insertar en la tabla temporal siempre ganará.</span><span class="sxs-lookup"><span data-stu-id="9edd7-170">However, when the JET_bitTTErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always win.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9edd7-171">JET_bitTTUpdatable</span><span class="sxs-lookup"><span data-stu-id="9edd7-171">JET_bitTTUpdatable</span></span></p></td>
<td><p><span data-ttu-id="9edd7-172">Esta opción solicita que la tabla temporal sea lo suficientemente flexible como para permitir que se modifiquen posteriormente los registros que se han insertado previamente.</span><span class="sxs-lookup"><span data-stu-id="9edd7-172">This option requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="9edd7-173">Si esta funcionalidad no es necesaria, es mejor no solicitarlo.</span><span class="sxs-lookup"><span data-stu-id="9edd7-173">If this functionality it not required then it is best to not request it.</span></span></p>
<p><span data-ttu-id="9edd7-174">Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</span><span class="sxs-lookup"><span data-stu-id="9edd7-174">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9edd7-175">JET_bitTTIntrinsicLVsOnly</span><span class="sxs-lookup"><span data-stu-id="9edd7-175">JET_bitTTIntrinsicLVsOnly</span></span></p></td>
<td><p><span data-ttu-id="9edd7-176">Solicitudes para permitir solo valores largos intrínsecos.</span><span class="sxs-lookup"><span data-stu-id="9edd7-176">Requests to permit only intrinsic long values.</span></span></p>
<p><span data-ttu-id="9edd7-177"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> se introduce en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9edd7-177"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9edd7-178">*ptableid*</span><span class="sxs-lookup"><span data-stu-id="9edd7-178">*ptableid*</span></span>

<span data-ttu-id="9edd7-179">Búfer de salida que recibirá el nuevo cursor abierto en la tabla temporal recién creada.</span><span class="sxs-lookup"><span data-stu-id="9edd7-179">The output buffer that will receive the new cursor opened on the newly created temporary table.</span></span>

<span data-ttu-id="9edd7-180">*prgcolumnid*</span><span class="sxs-lookup"><span data-stu-id="9edd7-180">*prgcolumnid*</span></span>

<span data-ttu-id="9edd7-181">Búfer de salida que recibirá la matriz de identificadores de columna generados durante la creación de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="9edd7-181">The output buffer that will receive the array of column IDs generated during the creation of the temporary table.</span></span>

<span data-ttu-id="9edd7-182">Los identificadores de columna de esta matriz se corresponden exactamente con la matriz de entrada de definiciones de columna.</span><span class="sxs-lookup"><span data-stu-id="9edd7-182">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="9edd7-183">Como resultado, el tamaño de este búfer debe corresponder al tamaño de la matriz de entrada.</span><span class="sxs-lookup"><span data-stu-id="9edd7-183">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

### <a name="return-value"></a><span data-ttu-id="9edd7-184">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9edd7-184">Return Value</span></span>

<span data-ttu-id="9edd7-185">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="9edd7-185">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="9edd7-186">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9edd7-186">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9edd7-187">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9edd7-187">Return code</span></span></p></th>
<th><p><span data-ttu-id="9edd7-188">Descripción</span><span class="sxs-lookup"><span data-stu-id="9edd7-188">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9edd7-189">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="9edd7-189">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="9edd7-190">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="9edd7-190">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9edd7-191">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="9edd7-191">JET_errCannotMaterializeForwardOnlySort</span></span></p></td>
<td><p><span data-ttu-id="9edd7-192">Error de <strong>JetOpenTempTable2</strong> porque se especificó JET_bitTTForwardOnly y no se pudo crear la tabla temporal tal y como se especificó mediante la optimización de solo avance.</span><span class="sxs-lookup"><span data-stu-id="9edd7-192"><strong>JetOpenTempTable2</strong> failed because JET_bitTTForwardOnly was specified and the temporary table as specified could not be created using the forward-only optimization.</span></span> <span data-ttu-id="9edd7-193">Este error solo lo devolverán Windows Server 2003 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="9edd7-193">This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9edd7-194">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="9edd7-194">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="9edd7-195">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="9edd7-195">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9edd7-196">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="9edd7-196">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="9edd7-197">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="9edd7-197">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="9edd7-198">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="9edd7-198">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9edd7-199">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="9edd7-199">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="9edd7-200">El campo CP del <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> no se estableció en una página de códigos válida.</span><span class="sxs-lookup"><span data-stu-id="9edd7-200">The cp field of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid code page.</span></span> <span data-ttu-id="9edd7-201">Los únicos valores válidos para las columnas de texto son inglés (1252) y Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="9edd7-201">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="9edd7-202">Un valor de 0 significa que se usará el valor predeterminado (Inglés, 1252).</span><span class="sxs-lookup"><span data-stu-id="9edd7-202">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9edd7-203">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="9edd7-203">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="9edd7-204">El campo <em>coltyp</em> de la <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> no se ha establecido en un tipo de columna válido.</span><span class="sxs-lookup"><span data-stu-id="9edd7-204">The <em>coltyp</em> field of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9edd7-205">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="9edd7-205">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="9edd7-206">No se pudo crear el índice porque se especificó una definición de índice no válida.</span><span class="sxs-lookup"><span data-stu-id="9edd7-206">The index could not be created because an invalid index definition was specified.</span></span></p>
<p><span data-ttu-id="9edd7-207"><strong>JetOpenTempTable2</strong> devolverá este error cuando:</span><span class="sxs-lookup"><span data-stu-id="9edd7-207"><strong>JetOpenTempTable2</strong> will return this error when:</span></span></p>
<ul>
<li><p><span data-ttu-id="9edd7-208">Se especifica la configuración regional independiente del idioma.</span><span class="sxs-lookup"><span data-stu-id="9edd7-208">The Language Neutral locale is specified.</span></span></p></li>
<li><p><span data-ttu-id="9edd7-209">Se especifica un conjunto no válido de marcas de normalización.</span><span class="sxs-lookup"><span data-stu-id="9edd7-209">An invalid set of normalization flags is specified.</span></span></p></li>
</ul>
<p><span data-ttu-id="9edd7-210">Este error solo lo devolverá Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="9edd7-210">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9edd7-211">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="9edd7-211">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="9edd7-212">No se pudo crear el índice porque se intentó usar un ID. de configuración regional no válido.</span><span class="sxs-lookup"><span data-stu-id="9edd7-212">The index could not be created because an attempt was made to use an invalid locale ID.</span></span> <span data-ttu-id="9edd7-213">Es posible que el ID. de configuración regional no sea válido o que el paquete de idioma asociado no esté instalado.</span><span class="sxs-lookup"><span data-stu-id="9edd7-213">The locale ID may either be completely invalid or the associated language pack may not be installed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9edd7-214">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="9edd7-214">JET_errInvalidLCMapStringFlags</span></span></p></td>
<td><p><span data-ttu-id="9edd7-215">No se pudo crear el índice porque se intentó usar un conjunto no válido de marcas de normalización.</span><span class="sxs-lookup"><span data-stu-id="9edd7-215">The index could not be created because an attempt was made to use an invalid set of normalization flags.</span></span> <span data-ttu-id="9edd7-216">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="9edd7-216">This error will only be returned by Windows XP and later releases.</span></span> <span data-ttu-id="9edd7-217">En Windows 2000, las marcas de normalización no válidas producirán JET_errIndexInvalidDef en su lugar.</span><span class="sxs-lookup"><span data-stu-id="9edd7-217">On Windows 2000, invalid normalization flags will result in JET_errIndexInvalidDef instead.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9edd7-218">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="9edd7-218">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="9edd7-219">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="9edd7-219">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9edd7-220">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="9edd7-220">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="9edd7-221">No se pudo realizar la operación porque el motor no puede asignar los recursos necesarios para abrir un nuevo cursor.</span><span class="sxs-lookup"><span data-stu-id="9edd7-221">The operation failed because the engine cannot allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="9edd7-222">Los recursos de cursor se configuran mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="9edd7-222">Cursor resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9edd7-223">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="9edd7-223">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="9edd7-224">No se pudo realizar la operación porque no se pudo asignar suficiente memoria para completarla.</span><span class="sxs-lookup"><span data-stu-id="9edd7-224">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="9edd7-225"><strong>JetOpenTempTable2</strong> puede devolver JET_errOutOfMemory si el espacio de direcciones del proceso de host está demasiado fragmentado.</span><span class="sxs-lookup"><span data-stu-id="9edd7-225"><strong>JetOpenTempTable2</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="9edd7-226">El administrador de tablas temporales asignará siempre un fragmento de 1 MB de espacio de direcciones para cada tabla temporal creada independientemente de la cantidad de datos que se van a almacenar.</span><span class="sxs-lookup"><span data-stu-id="9edd7-226">The temporary table manager will always allocate a 1MB chunk of address space for every temporary table created regardless of the amount of data to be stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9edd7-227">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="9edd7-227">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="9edd7-228">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="9edd7-228">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9edd7-229">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="9edd7-229">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="9edd7-230">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="9edd7-230">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="9edd7-231">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="9edd7-231">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9edd7-232">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="9edd7-232">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="9edd7-233">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="9edd7-233">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9edd7-234">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="9edd7-234">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="9edd7-235">Se intentó agregar demasiadas columnas a la tabla.</span><span class="sxs-lookup"><span data-stu-id="9edd7-235">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="9edd7-236">Una tabla no puede tener más de JET_ccolFixedMost columnas fijas, ni más de JET_ccolVarMost columnas de longitud variable, ni más de JET_ccolTaggedMost columnas etiquetadas.</span><span class="sxs-lookup"><span data-stu-id="9edd7-236">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9edd7-237">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="9edd7-237">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="9edd7-238">No se pudo realizar la operación porque el motor no puede asignar los recursos necesarios para almacenar en memoria caché los índices de la tabla.</span><span class="sxs-lookup"><span data-stu-id="9edd7-238">The operation failed because the engine cannot allocate the resources required to cache the indexes of the table.</span></span> <span data-ttu-id="9edd7-239">El número de índices cuyo esquema se puede almacenar en caché se configura mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="9edd7-239">The number of indexes whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9edd7-240">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="9edd7-240">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="9edd7-241">No se pudo realizar la operación porque el motor no puede asignar los recursos necesarios para almacenar en caché el esquema de la tabla.</span><span class="sxs-lookup"><span data-stu-id="9edd7-241">The operation failed because the engine cannot allocate the resources required to cache the schema of the table.</span></span> <span data-ttu-id="9edd7-242">El número de tablas cuyo esquema se puede almacenar en caché se configura mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="9edd7-242">The number of tables whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9edd7-243">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="9edd7-243">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="9edd7-244">No se pudo realizar la operación porque el motor no puede asignar los recursos necesarios para crear una tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="9edd7-244">The operation failed because the engine cannot allocate the resources required to create a temporary table.</span></span> <span data-ttu-id="9edd7-245">Los recursos de tabla temporal se configuran mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span><span class="sxs-lookup"><span data-stu-id="9edd7-245">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9edd7-246">Si se ejecuta correctamente, se devolverá un cursor abierto en la tabla temporal recién creada.</span><span class="sxs-lookup"><span data-stu-id="9edd7-246">On success, a cursor opened on the newly created temporary table will be returned.</span></span> <span data-ttu-id="9edd7-247">El estado de la base de datos temporal se preparará para contener la nueva tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="9edd7-247">The state of the temporary database will be prepared to contain the new temporary table.</span></span> <span data-ttu-id="9edd7-248">El estado de las bases de datos normales que use el motor de base de datos permanecerá sin cambios.</span><span class="sxs-lookup"><span data-stu-id="9edd7-248">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

<span data-ttu-id="9edd7-249">En caso de error, no se creará la tabla temporal y no se devolverá un cursor.</span><span class="sxs-lookup"><span data-stu-id="9edd7-249">On failure, the temporary table will not be created and a cursor will not be returned.</span></span> <span data-ttu-id="9edd7-250">Se puede cambiar el estado de la base de datos temporal.</span><span class="sxs-lookup"><span data-stu-id="9edd7-250">The state of the temporary database may be changed.</span></span> <span data-ttu-id="9edd7-251">El estado de las bases de datos normales que use el motor de base de datos permanecerá sin cambios.</span><span class="sxs-lookup"><span data-stu-id="9edd7-251">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="9edd7-252">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9edd7-252">Remarks</span></span>

<span data-ttu-id="9edd7-253">Vea [JetOpenTempTable](./jetopentemptable-function.md).</span><span class="sxs-lookup"><span data-stu-id="9edd7-253">See [JetOpenTempTable](./jetopentemptable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="9edd7-254">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9edd7-254">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9edd7-255"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="9edd7-255"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9edd7-256">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="9edd7-256">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9edd7-257"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9edd7-257"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9edd7-258">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9edd7-258">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9edd7-259"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="9edd7-259"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9edd7-260">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="9edd7-260">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9edd7-261"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="9edd7-261"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9edd7-262">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="9edd7-262">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9edd7-263"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="9edd7-263"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9edd7-264">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="9edd7-264">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9edd7-265">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9edd7-265">See Also</span></span>

[<span data-ttu-id="9edd7-266">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="9edd7-266">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="9edd7-267">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="9edd7-267">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="9edd7-268">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9edd7-268">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9edd7-269">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="9edd7-269">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="9edd7-270">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9edd7-270">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="9edd7-271">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="9edd7-271">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="9edd7-272">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="9edd7-272">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="9edd7-273">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="9edd7-273">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="9edd7-274">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="9edd7-274">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="9edd7-275">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="9edd7-275">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="9edd7-276">JetMove</span><span class="sxs-lookup"><span data-stu-id="9edd7-276">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="9edd7-277">JetRollback</span><span class="sxs-lookup"><span data-stu-id="9edd7-277">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="9edd7-278">JetSeek</span><span class="sxs-lookup"><span data-stu-id="9edd7-278">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="9edd7-279">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="9edd7-279">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="9edd7-280">Parámetros del sistema</span><span class="sxs-lookup"><span data-stu-id="9edd7-280">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
