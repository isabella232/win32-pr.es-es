---
description: 'Más información acerca de: estructura de JET_OPENTEMPORARYTABLE'
title: Estructura de JET_OPENTEMPORARYTABLE
TOCTitle: JET_OPENTEMPORARYTABLE Structure
ms:assetid: 23f4fb0f-ca60-498b-9b8e-14de6188eb87
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269206(v=EXCHG.10)
ms:contentKeyID: 32765509
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
ms.openlocfilehash: 51ae9026098e82538940bde2ef182ba0a7a11c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360770"
---
# <a name="jet_opentemporarytable-structure"></a><span data-ttu-id="dd59e-103">Estructura de JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="dd59e-103">JET_OPENTEMPORARYTABLE Structure</span></span>


<span data-ttu-id="dd59e-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="dd59e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_opentemporarytable-structure"></a><span data-ttu-id="dd59e-105">Estructura de JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="dd59e-105">JET_OPENTEMPORARYTABLE Structure</span></span>

<span data-ttu-id="dd59e-106">La estructura **JET_OPENTEMPORARYTABLE** contiene una colección fácilmente extensible de parámetros para la función **JET_OPENTEMPORARYTABLE** .</span><span class="sxs-lookup"><span data-stu-id="dd59e-106">The **JET_OPENTEMPORARYTABLE** structure contains an easily extensible collection of parameters for the **JET_OPENTEMPORARYTABLE** function.</span></span> <span data-ttu-id="dd59e-107">Esta estructura es la tabla temporal equivalente a la estructura [JET_TABLECREATE](./jet-tablecreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="dd59e-107">This structure is the temporary table equivalent of the [JET_TABLECREATE](./jet-tablecreate-structure.md) structure.</span></span>

<span data-ttu-id="dd59e-108">**Windows Vista:** La estructura de **JET_OPENTEMPORARYTABLE** se introduce en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dd59e-108">**Windows Vista:** The **JET_OPENTEMPORARYTABLE** structure is introduced in Windows Vista.</span></span>

```cpp
    typedef struct tagJET_OPENTEMPORARYTABLE {
      unsigned long cbStruct;
      const JET_COLUMNDEF* prgcolumndef;
      unsigned long ccolumn;
      JET_UNICODEINDEX* pidxunicode;
      JET_GRBIT grbit;
      JET_COLUMNID* prgcolumnid;
      unsigned long cbKeyMost;
      unsigned long cbVarSegMac;
      JET_TABLEID tableid;
    } JET_OPENTEMPORARYTABLE;
```

### <a name="members"></a><span data-ttu-id="dd59e-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="dd59e-109">Members</span></span>

<span data-ttu-id="dd59e-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="dd59e-110">**cbStruct**</span></span>

<span data-ttu-id="dd59e-111">Tamaño de esta estructura en bytes (para una futura ampliación).</span><span class="sxs-lookup"><span data-stu-id="dd59e-111">The size of this structure in bytes (for future expansion).</span></span> <span data-ttu-id="dd59e-112">Debe establecerse en sizeof (JET_TABLECREATE) en bytes.</span><span class="sxs-lookup"><span data-stu-id="dd59e-112">It must be set to sizeof( JET_TABLECREATE ) in bytes.</span></span>

<span data-ttu-id="dd59e-113">**prgcolumndef**</span><span class="sxs-lookup"><span data-stu-id="dd59e-113">**prgcolumndef**</span></span>

<span data-ttu-id="dd59e-114">Definiciones de columna para las columnas creadas en la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="dd59e-114">Column definitions for the columns created in the temporary table.</span></span>

<span data-ttu-id="dd59e-115">Existen limitaciones **importantes** para las opciones de definición de columna que se utilizan con una tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="dd59e-115">**Important** limitations exist for the column definition options that are used with a temporary table.</span></span> <span data-ttu-id="dd59e-116">Vea la sección Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="dd59e-116">See the Remarks section for more information.</span></span>

<span data-ttu-id="dd59e-117">Además de las opciones de definición de columna habituales, también se pueden especificar cero o más de las opciones siguientes que solo son relevantes en el contexto de una tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="dd59e-117">In addition to the usual column definition options, zero or more of the following options can also be specified that are relevant only in the context of a temporary table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dd59e-118">Value</span><span class="sxs-lookup"><span data-stu-id="dd59e-118">Value</span></span></p></th>
<th><p><span data-ttu-id="dd59e-119">Significado</span><span class="sxs-lookup"><span data-stu-id="dd59e-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dd59e-120">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="dd59e-120">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="dd59e-121">El criterio de ordenación de la columna de clave para la tabla temporal debe ser descendente en lugar de ascendente.</span><span class="sxs-lookup"><span data-stu-id="dd59e-121">The sort order of the key column for the temporary table should be descending rather than ascending.</span></span> <span data-ttu-id="dd59e-122">Si se especifica esta opción sin JET_bitColumnTTKey, se omite esta opción.</span><span class="sxs-lookup"><span data-stu-id="dd59e-122">If this option is specified without JET_bitColumnTTKey then this option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd59e-123">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="dd59e-123">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="dd59e-124">La columna será una columna de clave para la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="dd59e-124">The column will be a key column for the temporary table.</span></span></p>
<p><span data-ttu-id="dd59e-125">El orden de las definiciones de columna con esta opción especificada en la matriz de entrada determinará la prioridad de cada columna de clave para la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="dd59e-125">The order of the column definitions with this option specified in the input array will determine the precedence of each key column for the temporary table.</span></span> <span data-ttu-id="dd59e-126">La primera definición de columna de la matriz que tiene esta opción establecida será la columna de clave más significativa, etc.</span><span class="sxs-lookup"><span data-stu-id="dd59e-126">The first column definition in the array that has this option set will be the most significant key column and so on.</span></span> <span data-ttu-id="dd59e-127">Si se solicitan más columnas de clave de las que puede admitir el motor de base de datos, esta opción se omite para las columnas de clave no admitidas.</span><span class="sxs-lookup"><span data-stu-id="dd59e-127">If more key columns are requested than can be supported by the database engine then this option is ignored for the unsupportable key columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dd59e-128">**ccolumn**</span><span class="sxs-lookup"><span data-stu-id="dd59e-128">**ccolumn**</span></span>

<span data-ttu-id="dd59e-129">Vea *prgcolumndef*.</span><span class="sxs-lookup"><span data-stu-id="dd59e-129">See *prgcolumndef*.</span></span>

<span data-ttu-id="dd59e-130">**pidxunicode**</span><span class="sxs-lookup"><span data-stu-id="dd59e-130">**pidxunicode**</span></span>

<span data-ttu-id="dd59e-131">El identificador de configuración regional y las marcas de normalización que se van a usar para comparar los datos de columna de clave Unicode en la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="dd59e-131">The locale ID and normalization flags to use to compare any Unicode key column data in the temporary table.</span></span>

<span data-ttu-id="dd59e-132">Cuando este parámetro no está presente y cuando el parámetro *LCID* no está presente, se utilizará el LCID predeterminado para comparar las columnas de clave Unicode de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="dd59e-132">When this parameter is not present and when the *lcid* parameter is not present, then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="dd59e-133">El LCID predeterminado es la configuración regional en Inglés de EE. UU.</span><span class="sxs-lookup"><span data-stu-id="dd59e-133">The default LCID is the U.S. English locale.</span></span>

<span data-ttu-id="dd59e-134">Cuando este parámetro no está presente, se usarán las marcas de normalización predeterminadas para comparar los datos de columna de clave Unicode en la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="dd59e-134">When this parameter is not present, then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="dd59e-135">Las marcas de normalización predeterminadas son: NORM_IGNORECASE, NORM_IGNOREKANATYPE y NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="dd59e-135">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span>

<span data-ttu-id="dd59e-136">**grbit**</span><span class="sxs-lookup"><span data-stu-id="dd59e-136">**grbit**</span></span>

<span data-ttu-id="dd59e-137">Grupo de bits que especifica cero o más de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="dd59e-137">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dd59e-138">Value</span><span class="sxs-lookup"><span data-stu-id="dd59e-138">Value</span></span></p></th>
<th><p><span data-ttu-id="dd59e-139">Significado</span><span class="sxs-lookup"><span data-stu-id="dd59e-139">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dd59e-140">JET_bitTTIndexed</span><span class="sxs-lookup"><span data-stu-id="dd59e-140">JET_bitTTIndexed</span></span></p></td>
<td><p><span data-ttu-id="dd59e-141">Esta opción solicita que la tabla temporal sea lo suficientemente flexible como para permitir el uso de <a href="gg294103(v=exchg.10).md">JetSeek</a> para buscar registros por clave de índice.</span><span class="sxs-lookup"><span data-stu-id="dd59e-141">This option requests that the temporary table be flexible enough to permit the use of <a href="gg294103(v=exchg.10).md">JetSeek</a> to look up records by index key.</span></span></p>
<p><span data-ttu-id="dd59e-142">Si esta funcionalidad no es necesaria, es mejor no solicitarlo.</span><span class="sxs-lookup"><span data-stu-id="dd59e-142">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="dd59e-143">Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</span><span class="sxs-lookup"><span data-stu-id="dd59e-143">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd59e-144">JET_bitTTUnique</span><span class="sxs-lookup"><span data-stu-id="dd59e-144">JET_bitTTUnique</span></span></p></td>
<td><p><span data-ttu-id="dd59e-145">Solicita que los registros con claves de índice duplicadas se quiten del conjunto final de registros de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="dd59e-145">Requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span></p>
<p><span data-ttu-id="dd59e-146">Antes de Windows Server 2003, el motor de base de datos siempre asumió que esta opción está en vigor debido al hecho de que todos los índices clúster también deben ser una clave principal y, por tanto, deben ser únicos.</span><span class="sxs-lookup"><span data-stu-id="dd59e-146">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="dd59e-147">A partir de Windows Server 2003, ahora es posible crear una tabla temporal que no quita los duplicados cuando también se especifica la opción de JET_bitTTForwardOnly.</span><span class="sxs-lookup"><span data-stu-id="dd59e-147">As of Windows Server 2003, it is now possible to create a temporary table that does not remove duplicates when the JET_bitTTForwardOnly option is also specified.</span></span></p>
<p><span data-ttu-id="dd59e-148">No es posible saber qué duplicado se realizará correctamente y qué duplicados se descartarán, en general.</span><span class="sxs-lookup"><span data-stu-id="dd59e-148">It is not possible to know which duplicate will succeed and which duplicates will be discarded, in general.</span></span> <span data-ttu-id="dd59e-149">Sin embargo, cuando se solicita la opción de JET_bitTTErrorOnDuplicateInsertion, el primer registro con una clave de índice determinada que se va a insertar en la tabla temporal siempre se realizará correctamente.</span><span class="sxs-lookup"><span data-stu-id="dd59e-149">However, when the JET_bitTTErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always succeed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd59e-150">JET_bitTTUpdatable</span><span class="sxs-lookup"><span data-stu-id="dd59e-150">JET_bitTTUpdatable</span></span></p></td>
<td><p><span data-ttu-id="dd59e-151">Solicita que la tabla temporal sea lo suficientemente flexible como para permitir que se modifiquen posteriormente los registros que se han insertado previamente.</span><span class="sxs-lookup"><span data-stu-id="dd59e-151">Requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="dd59e-152">Si esta funcionalidad no es necesaria, es mejor no solicitarlo.</span><span class="sxs-lookup"><span data-stu-id="dd59e-152">If this functionality it not required then it is best to not request it.</span></span></p>
<p><span data-ttu-id="dd59e-153">Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</span><span class="sxs-lookup"><span data-stu-id="dd59e-153">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd59e-154">JET_bitTTScrollable</span><span class="sxs-lookup"><span data-stu-id="dd59e-154">JET_bitTTScrollable</span></span></p></td>
<td><p><span data-ttu-id="dd59e-155">Solicita que la tabla temporal sea lo suficientemente flexible como para permitir que los registros se examinen en orden y dirección arbitrarios mediante <a href="gg294117(v=exchg.10).md">JetMove</a>.</span><span class="sxs-lookup"><span data-stu-id="dd59e-155">Requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p>
<p><span data-ttu-id="dd59e-156">Si no se necesita esta funcionalidad, es mejor no solicitarla.</span><span class="sxs-lookup"><span data-stu-id="dd59e-156">If this functionality is not required then it is best to not request it.</span></span> <span data-ttu-id="dd59e-157">Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</span><span class="sxs-lookup"><span data-stu-id="dd59e-157">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd59e-158">JET_bitTTSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="dd59e-158">JET_bitTTSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="dd59e-159">Solicita que los valores de columna de clave <strong>null</strong> se ordenen más cerca del final del índice que los valores de columna de clave no NULL.</span><span class="sxs-lookup"><span data-stu-id="dd59e-159">Requests that <strong>NULL</strong> key column values sort closer to the end of the index than non-NULL key column values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd59e-160">JET_bitTTForceMaterialization</span><span class="sxs-lookup"><span data-stu-id="dd59e-160">JET_bitTTForceMaterialization</span></span></p></td>
<td><p><span data-ttu-id="dd59e-161">Obliga al administrador de tablas temporal a abandonar la búsqueda de la mejor estrategia para usar la administración de la tabla temporal, lo que dará lugar a un rendimiento mejorado.</span><span class="sxs-lookup"><span data-stu-id="dd59e-161">Forces the temporary table manager to abandon the search for the best strategy to use managing the temporary table that will result in enhanced performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd59e-162">JET_bitTTErrorOnDuplicateInsertion</span><span class="sxs-lookup"><span data-stu-id="dd59e-162">JET_bitTTErrorOnDuplicateInsertion</span></span></p></td>
<td><p><span data-ttu-id="dd59e-163">Cualquier intento de insertar un registro con la misma clave de índice que un registro insertado anteriormente producirá un error inmediatamente con JET_errKeyDuplicate.</span><span class="sxs-lookup"><span data-stu-id="dd59e-163">Any attempt to insert a record with the same index key as a previously inserted record will immediately fail with JET_errKeyDuplicate.</span></span> <span data-ttu-id="dd59e-164">Si no se solicita esta opción, se detectará un duplicado inmediatamente y se producirá un error, o se quitará de forma silenciosa más adelante, en función de la estrategia elegida por el motor de base de datos para implementar la tabla temporal, en función de la funcionalidad solicitada.</span><span class="sxs-lookup"><span data-stu-id="dd59e-164">If this option is not requested then a duplicate is detected immediately and fails, or is silently removed later, depending on the strategy chosen by the database engine to implement the temporary table, based on the requested functionality.</span></span></p>
<p><span data-ttu-id="dd59e-165">Si esta funcionalidad no es necesaria, es mejor no solicitarlo.</span><span class="sxs-lookup"><span data-stu-id="dd59e-165">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="dd59e-166">Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</span><span class="sxs-lookup"><span data-stu-id="dd59e-166">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd59e-167">JET_bitTTForwardOnly</span><span class="sxs-lookup"><span data-stu-id="dd59e-167">JET_bitTTForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="dd59e-168">La tabla temporal solo se crea si el administrador de tablas temporales puede usar la implementación optimizada para los resultados intermedios de la consulta.</span><span class="sxs-lookup"><span data-stu-id="dd59e-168">The temporary table is only created if the temporary table manager can use the implementation that is optimized for intermediate query results.</span></span> <span data-ttu-id="dd59e-169">Si alguna característica de la tabla temporal impidiera el uso de esta optimización, la operación producirá un error con JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="dd59e-169">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span></p>
<p><span data-ttu-id="dd59e-170">Un efecto secundario de esta opción es permitir que la tabla temporal contenga registros con claves de índice duplicadas.</span><span class="sxs-lookup"><span data-stu-id="dd59e-170">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="dd59e-171">Consulte JET_bitTTUnique para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="dd59e-171">See JET_bitTTUnique for more information.</span></span></p>
<p><span data-ttu-id="dd59e-172"><strong>Windows Server 2003:  </strong> Esta opción solo está disponible en Windows Server 2003 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="dd59e-172"><strong>Windows Server 2003:  </strong>This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dd59e-173">**prgcolumnid**</span><span class="sxs-lookup"><span data-stu-id="dd59e-173">**prgcolumnid**</span></span>

<span data-ttu-id="dd59e-174">Búfer de salida que recibe la matriz de identificadores de columna generados durante la creación de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="dd59e-174">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span>

<span data-ttu-id="dd59e-175">Los identificadores de columna de esta matriz se corresponden exactamente con la matriz de entrada de definiciones de columna.</span><span class="sxs-lookup"><span data-stu-id="dd59e-175">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="dd59e-176">Como resultado, el tamaño de este búfer debe corresponder al tamaño de la matriz de entrada.</span><span class="sxs-lookup"><span data-stu-id="dd59e-176">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

<span data-ttu-id="dd59e-177">**cbKeyMost**</span><span class="sxs-lookup"><span data-stu-id="dd59e-177">**cbKeyMost**</span></span>

<span data-ttu-id="dd59e-178">Tamaño máximo de una clave que representa una fila determinada.</span><span class="sxs-lookup"><span data-stu-id="dd59e-178">The maximum size for a key representing a given row.</span></span>

<span data-ttu-id="dd59e-179">Se puede establecer el tamaño máximo de la clave para controlar cómo se truncan las claves.</span><span class="sxs-lookup"><span data-stu-id="dd59e-179">The maximum key size may be set to control how keys are truncated.</span></span> <span data-ttu-id="dd59e-180">El truncamiento de claves es importante porque puede afectar a la diferencia entre las filas.</span><span class="sxs-lookup"><span data-stu-id="dd59e-180">Key truncation is important because it can affect when rows are considered to be distinct.</span></span>

<span data-ttu-id="dd59e-181">Si este parámetro se establece en 0 o JET_cbKeyMostMin (255), el tamaño de clave máximo y su semántica serán idénticos al tamaño de clave máximo admitido por Windows Server 2003 y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="dd59e-181">If this parameter is set to 0 or JET_cbKeyMostMin (255) then the maximum key size and its semantics will remain identical to the maximum key size supported by Windows Server 2003 and previous releases.</span></span> <span data-ttu-id="dd59e-182">Este parámetro también se puede establecer en un valor mayor como una función del tamaño de página de la base de datos para la instancia (JET_paramDatabasePageSize).</span><span class="sxs-lookup"><span data-stu-id="dd59e-182">This parameter may also be set to a larger value as a function of the database page size for the instance (JET_paramDatabasePageSize).</span></span> <span data-ttu-id="dd59e-183">Consulte JET_paramKeyMost para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="dd59e-183">See JET_paramKeyMost for more information.</span></span>

<span data-ttu-id="dd59e-184">**cbVarSegMac**</span><span class="sxs-lookup"><span data-stu-id="dd59e-184">**cbVarSegMac**</span></span>

<span data-ttu-id="dd59e-185">La cantidad máxima de datos que se usarán de cualquier columna de longitud variable para construir una clave para una fila determinada.</span><span class="sxs-lookup"><span data-stu-id="dd59e-185">The maximum amount of data that will be used from any variable length column to construct a key for a given row.</span></span>

<span data-ttu-id="dd59e-186">Este parámetro se puede utilizar para controlar la cantidad de espacio de clave consumida por una columna de clave determinada.</span><span class="sxs-lookup"><span data-stu-id="dd59e-186">This parameter may be used to control the amount of key space consumed by any given key column.</span></span> <span data-ttu-id="dd59e-187">Este límite se encuentra en bytes.</span><span class="sxs-lookup"><span data-stu-id="dd59e-187">This limit is in bytes.</span></span> <span data-ttu-id="dd59e-188">Si este parámetro es cero o es igual que el parámetro *cbKeyMost* , no se aplica ningún límite.</span><span class="sxs-lookup"><span data-stu-id="dd59e-188">If this parameter is zero or is the same as the *cbKeyMost* parameter then no limit is in effect.</span></span>

<span data-ttu-id="dd59e-189">**TABLEID**</span><span class="sxs-lookup"><span data-stu-id="dd59e-189">**tableid**</span></span>

<span data-ttu-id="dd59e-190">El identificador de la tabla temporal creada como resultado de una llamada correcta a [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span><span class="sxs-lookup"><span data-stu-id="dd59e-190">The table handle for the temporary table created as a result of a successful call to [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="dd59e-191">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd59e-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dd59e-192"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="dd59e-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="dd59e-193">Requiere Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dd59e-193">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd59e-194"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="dd59e-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="dd59e-195">Requiere Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="dd59e-195">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd59e-196"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="dd59e-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="dd59e-197">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="dd59e-197">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="dd59e-198">Consulte también</span><span class="sxs-lookup"><span data-stu-id="dd59e-198">See Also</span></span>

[<span data-ttu-id="dd59e-199">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="dd59e-199">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="dd59e-200">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="dd59e-200">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="dd59e-201">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="dd59e-201">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="dd59e-202">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="dd59e-202">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="dd59e-203">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="dd59e-203">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="dd59e-204">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="dd59e-204">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="dd59e-205">JetOpenTemporaryTable</span><span class="sxs-lookup"><span data-stu-id="dd59e-205">JetOpenTemporaryTable</span></span>](./jetopentemporarytable-function.md)  
[<span data-ttu-id="dd59e-206">Parámetros del sistema del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="dd59e-206">Extensible Storage Engine System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
