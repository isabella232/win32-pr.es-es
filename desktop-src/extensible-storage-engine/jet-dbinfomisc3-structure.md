---
description: 'Más información acerca de: estructura de JET_DBINFOMISC3'
title: Estructura de JET_DBINFOMISC3
TOCTitle: JET_DBINFOMISC3 Structure
ms:assetid: ffb23ac1-21ad-4dc6-98f8-aa4e6ef395ac
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294148(v=EXCHG.10)
ms:contentKeyID: 32765762
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
ms.openlocfilehash: 761afe13638d7905b5d4a639b7100108ce6ec977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275384"
---
# <a name="jet_dbinfomisc3-structure"></a><span data-ttu-id="a21a1-103">Estructura de JET_DBINFOMISC3</span><span class="sxs-lookup"><span data-stu-id="a21a1-103">JET_DBINFOMISC3 Structure</span></span>


<span data-ttu-id="a21a1-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a21a1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dbinfomisc3-structure"></a><span data-ttu-id="a21a1-105">Estructura de JET_DBINFOMISC3</span><span class="sxs-lookup"><span data-stu-id="a21a1-105">JET_DBINFOMISC3 Structure</span></span>

<span data-ttu-id="a21a1-106">La estructura **JET_DBINFOMISC3** contiene información diversa sobre una base de datos.</span><span class="sxs-lookup"><span data-stu-id="a21a1-106">The **JET_DBINFOMISC3** structure holds miscellaneous information about a database.</span></span> <span data-ttu-id="a21a1-107">Esta es la información contenida en el encabezado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="a21a1-107">This is the information that is contained in the database header.</span></span>

```cpp
    typedef struct {
      unsigned long ulVersion;
      unsigned long ulUpdate;
      JET_SIGNATURE signDb;
      unsigned long dbstate;
      JET_LGPOS lgposConsistent;
      JET_LOGTIME logtimeConsistent;
      JET_LOGTIME logtimeAttach;
      JET_LGPOS lgposAttach;
      JET_LOGTIME logtimeDetach;
      JET_LGPOS lgposDetach;
      JET_SIGNATURE signLog;
      JET_BKINFO bkinfoFullPrev;
      JET_BKINFO bkinfoIncPrev;
      JET_BKINFO bkinfoFullCur;
      unsigned long fShadowingDisabled;
      unsigned long fUpgradeDb;
      unsigned long dwMajorVersion;
      unsigned long dwMinorVersion;
      unsigned long dwBuildNumber;
      long lSPNumber;
      unsigned long cbPageSize;
      unsigned long genMinRequired;
      unsigned long genMaxRequired;
      JET_LOGTIME logtimeGenMaxCreate;
      unsigned long ulRepairCount;
      JET_LOGTIME logtimeRepair;
      unsigned long ulRepairCountOld;
      unsigned long ulECCFixSuccess;
      JET_LOGTIME logtimeECCFixSuccess;
      unsigned long ulECCFixSuccessOld;
      unsigned long ulECCFixFail;
      JET_LOGTIME logtimeECCFixFail;
      unsigned long ulECCFixFailOld;
      unsigned long ulBadChecksum;
      JET_LOGTIME logtimeBadChecksum;
      unsigned long ulBadChecksumOld;
      unsigned long genCommitted;
    } JET_DBINFOMISC3;
```

### <a name="members"></a><span data-ttu-id="a21a1-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a21a1-108">Members</span></span>

<span data-ttu-id="a21a1-109">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="a21a1-109">**ulVersion**</span></span>

<span data-ttu-id="a21a1-110">Versión nativa del motor de base de datos que creó la base de datos.</span><span class="sxs-lookup"><span data-stu-id="a21a1-110">The native version of the database engine that created the database.</span></span> <span data-ttu-id="a21a1-111">Vea [JetGetVersion](./jetgetversion-function.md) para recuperar la versión nativa del motor de base de datos actual.</span><span class="sxs-lookup"><span data-stu-id="a21a1-111">See [JetGetVersion](./jetgetversion-function.md) to retrieve the native version for the current database engine.</span></span>

<span data-ttu-id="a21a1-112">**ulUpdate**</span><span class="sxs-lookup"><span data-stu-id="a21a1-112">**ulUpdate**</span></span>

<span data-ttu-id="a21a1-113">Realiza un seguimiento de las actualizaciones de formato de base de datos incrementales que son compatibles con versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="a21a1-113">Tracks incremental database format updates that are backward compatible.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a21a1-114">ulVersion, ulUpdate =</span><span class="sxs-lookup"><span data-stu-id="a21a1-114">ulVersion, ulUpdate =</span></span></p></th>
<th><p><span data-ttu-id="a21a1-115">Significado</span><span class="sxs-lookup"><span data-stu-id="a21a1-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a21a1-116">0x620, 0</span><span class="sxs-lookup"><span data-stu-id="a21a1-116">0x620,0</span></span></p></td>
<td><p><span data-ttu-id="a21a1-117">Formato original de la versión beta del sistema operativo (4/22/97).</span><span class="sxs-lookup"><span data-stu-id="a21a1-117">Original operating system Beta format (4/22/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a21a1-118">0x620, 1</span><span class="sxs-lookup"><span data-stu-id="a21a1-118">0x620,1</span></span></p></td>
<td><p><span data-ttu-id="a21a1-119">Agregue columnas en el catálogo para la indización condicional y OLD (5/29/97).</span><span class="sxs-lookup"><span data-stu-id="a21a1-119">Add columns in the catalog for conditional indexing and OLD (5/29/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a21a1-120">0x620, 2</span><span class="sxs-lookup"><span data-stu-id="a21a1-120">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="a21a1-121">Agregue la marca fLocalizedText en IDB (6/5/97).</span><span class="sxs-lookup"><span data-stu-id="a21a1-121">Add the fLocalizedText flag in IDB (6/5/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a21a1-122">0x620, 3</span><span class="sxs-lookup"><span data-stu-id="a21a1-122">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="a21a1-123">Agregue SPLIT_BUFFER a las páginas raíz del árbol de espacio (10/30/97).</span><span class="sxs-lookup"><span data-stu-id="a21a1-123">Add SPLIT_BUFFER to space tree root pages (10/30/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a21a1-124">0x620, 2</span><span class="sxs-lookup"><span data-stu-id="a21a1-124">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="a21a1-125">Revertir revisión para que ESE97 siga siendo compatible con el avance (1/28/98).</span><span class="sxs-lookup"><span data-stu-id="a21a1-125">Revert revision in order for ESE97 to remain forward-compatible (1/28/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a21a1-126">0x620, 3</span><span class="sxs-lookup"><span data-stu-id="a21a1-126">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="a21a1-127">Agregue nuevas columnas etiquetadas al catálogo ( &quot; CallbackData &quot; y &quot; CallbackDependencies &quot; ).</span><span class="sxs-lookup"><span data-stu-id="a21a1-127">Add new tagged columns to catalog (&quot;CallbackData&quot; and &quot;CallbackDependencies&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a21a1-128">0x620, 4</span><span class="sxs-lookup"><span data-stu-id="a21a1-128">0x620,4</span></span></p></td>
<td><p><span data-ttu-id="a21a1-129">Compatibilidad con SLV: signSLV, fSLVExists en el encabezado dB (5/5/98).</span><span class="sxs-lookup"><span data-stu-id="a21a1-129">SLV support: signSLV, fSLVExists in db header (5/5/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a21a1-130">0x620, 5</span><span class="sxs-lookup"><span data-stu-id="a21a1-130">0x620,5</span></span></p></td>
<td><p><span data-ttu-id="a21a1-131">Nuevo árbol de espacio SLV (5/29/98).</span><span class="sxs-lookup"><span data-stu-id="a21a1-131">New SLV space tree (5/29/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a21a1-132">0x620, 6</span><span class="sxs-lookup"><span data-stu-id="a21a1-132">0x620,6</span></span></p></td>
<td><p><span data-ttu-id="a21a1-133">Mapa de espacio SLV (10/12/98).</span><span class="sxs-lookup"><span data-stu-id="a21a1-133">SLV space map (10/12/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a21a1-134">0x620, 7</span><span class="sxs-lookup"><span data-stu-id="a21a1-134">0x620,7</span></span></p></td>
<td><p><span data-ttu-id="a21a1-135">IDXSEG de 4 bytes (12/10/98).</span><span class="sxs-lookup"><span data-stu-id="a21a1-135">4-byte IDXSEG (12/10/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a21a1-136">0x620, 8</span><span class="sxs-lookup"><span data-stu-id="a21a1-136">0x620,8</span></span></p></td>
<td><p><span data-ttu-id="a21a1-137">Nuevo formato de columna de plantilla (1/25/99).</span><span class="sxs-lookup"><span data-stu-id="a21a1-137">New template column format (1/25/99).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a21a1-138">0x620, 9</span><span class="sxs-lookup"><span data-stu-id="a21a1-138">0x620,9</span></span></p></td>
<td><p><span data-ttu-id="a21a1-139">Columnas de plantilla ordenadas (6/24/99).</span><span class="sxs-lookup"><span data-stu-id="a21a1-139">Sorted template columns (6/24/99).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a21a1-140">0x620, A</span><span class="sxs-lookup"><span data-stu-id="a21a1-140">0x620,A</span></span></p></td>
<td><p><span data-ttu-id="a21a1-141">Base de código combinado (3/26/2003).</span><span class="sxs-lookup"><span data-stu-id="a21a1-141">Merged code base (3/26/2003).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a21a1-142">0x620, B</span><span class="sxs-lookup"><span data-stu-id="a21a1-142">0x620,B</span></span></p></td>
<td><p><span data-ttu-id="a21a1-143">Nuevo formato de suma de comprobación (1/08/2004).</span><span class="sxs-lookup"><span data-stu-id="a21a1-143">New checksum format (1/08/2004).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a21a1-144">0x620, C</span><span class="sxs-lookup"><span data-stu-id="a21a1-144">0x620,C</span></span></p></td>
<td><p><span data-ttu-id="a21a1-145">Mayor longitud de clave máxima en 1000/2000 bytes para páginas de 4/8 KB (1/15/2004).</span><span class="sxs-lookup"><span data-stu-id="a21a1-145">Increased max key length to 1000/2000 bytes for 4/8kb pages (1/15/2004).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a21a1-146">0x620, D</span><span class="sxs-lookup"><span data-stu-id="a21a1-146">0x620,D</span></span></p></td>
<td><p><span data-ttu-id="a21a1-147">Sugerencias de espacio de catálogo, space_header. V2 (7/15/2007).</span><span class="sxs-lookup"><span data-stu-id="a21a1-147">Catalog space hints, space_header.v2 (7/15/2007).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a21a1-148">0x620, E</span><span class="sxs-lookup"><span data-stu-id="a21a1-148">0x620,E</span></span></p></td>
<td><p><span data-ttu-id="a21a1-149">Agregue un nuevo formato de nodo/extensión a Space Manager y úselo para grupos de espacio reservados (8/9/2007).</span><span class="sxs-lookup"><span data-stu-id="a21a1-149">Add new node/extent format to space manager, use it for reserved pools of space (8/9/2007).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a21a1-150">0x620, F</span><span class="sxs-lookup"><span data-stu-id="a21a1-150">0x620,F</span></span></p></td>
<td><p><span data-ttu-id="a21a1-151">Compresión para valores Long intrínsecos (10/30/2007).</span><span class="sxs-lookup"><span data-stu-id="a21a1-151">Compression for intrinsic long-values (10/30/2007).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a21a1-152">0x620, 10</span><span class="sxs-lookup"><span data-stu-id="a21a1-152">0x620,10</span></span></p></td>
<td><p><span data-ttu-id="a21a1-153">Compresión para valores Long separados (12/05/2007).</span><span class="sxs-lookup"><span data-stu-id="a21a1-153">Compression for separated long-values (12/05/2007).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a21a1-154">0x620, 11</span><span class="sxs-lookup"><span data-stu-id="a21a1-154">0x620,11</span></span></p></td>
<td><p><span data-ttu-id="a21a1-155">Nuevo tamaño de fragmento de LV para páginas grandes (12/29/2007).</span><span class="sxs-lookup"><span data-stu-id="a21a1-155">New LV chunk size for large pages (12/29/2007).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a21a1-156">**signDb**</span><span class="sxs-lookup"><span data-stu-id="a21a1-156">**signDb**</span></span>

<span data-ttu-id="a21a1-157">Firma de la base de datos (incluida la hora de creación).</span><span class="sxs-lookup"><span data-stu-id="a21a1-157">Signature of the database (including creation time).</span></span> <span data-ttu-id="a21a1-158">Esta estructura es de 28 bytes.</span><span class="sxs-lookup"><span data-stu-id="a21a1-158">This structure is 28 bytes.</span></span>

<span data-ttu-id="a21a1-159">**dbstate**</span><span class="sxs-lookup"><span data-stu-id="a21a1-159">**dbstate**</span></span>

<span data-ttu-id="a21a1-160">Este es el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="a21a1-160">This is the database state.</span></span>

<span data-ttu-id="a21a1-161">Las siguientes opciones están disponibles para este miembro.</span><span class="sxs-lookup"><span data-stu-id="a21a1-161">The following options are available for this member.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a21a1-162">Value</span><span class="sxs-lookup"><span data-stu-id="a21a1-162">Value</span></span></p></th>
<th><p><span data-ttu-id="a21a1-163">Significado</span><span class="sxs-lookup"><span data-stu-id="a21a1-163">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a21a1-164">JET_dbstateJustCreated</span><span class="sxs-lookup"><span data-stu-id="a21a1-164">JET_dbstateJustCreated</span></span><br />
<span data-ttu-id="a21a1-165">1</span><span class="sxs-lookup"><span data-stu-id="a21a1-165">1</span></span></p></td>
<td><p><span data-ttu-id="a21a1-166">Se acaba de crear la base de datos.</span><span class="sxs-lookup"><span data-stu-id="a21a1-166">The database was just created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a21a1-167">JET_dbstateDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="a21a1-167">JET_dbstateDirtyShutdown</span></span><br />
<span data-ttu-id="a21a1-168">2</span><span class="sxs-lookup"><span data-stu-id="a21a1-168">2</span></span></p></td>
<td><p><span data-ttu-id="a21a1-169">La base de datos requiere que se ejecute la recuperación de hardware o software para que se pueda usar o mover.</span><span class="sxs-lookup"><span data-stu-id="a21a1-169">The database requires hard or soft recovery to be run in order to become usable or moveable.</span></span> <span data-ttu-id="a21a1-170">No debe intentar trasladar las bases de datos en este estado.</span><span class="sxs-lookup"><span data-stu-id="a21a1-170">One should not try to move databases in this state.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a21a1-171">JET_dbstateCleanShutdown</span><span class="sxs-lookup"><span data-stu-id="a21a1-171">JET_dbstateCleanShutdown</span></span><br />
<span data-ttu-id="a21a1-172">3</span><span class="sxs-lookup"><span data-stu-id="a21a1-172">3</span></span></p></td>
<td><p><span data-ttu-id="a21a1-173">La base de datos está en un estado limpio.</span><span class="sxs-lookup"><span data-stu-id="a21a1-173">The database is in a clean state.</span></span> <span data-ttu-id="a21a1-174">La base de datos se puede adjuntar sin ningún archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="a21a1-174">The database can be attached without any log files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a21a1-175">JET_dbstateBeingConverted</span><span class="sxs-lookup"><span data-stu-id="a21a1-175">JET_dbstateBeingConverted</span></span><br />
<span data-ttu-id="a21a1-176">4</span><span class="sxs-lookup"><span data-stu-id="a21a1-176">4</span></span></p></td>
<td><p><span data-ttu-id="a21a1-177">La base de datos se está actualizando.</span><span class="sxs-lookup"><span data-stu-id="a21a1-177">The database is being upgraded.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a21a1-178">JET_dbstateForceDetach</span><span class="sxs-lookup"><span data-stu-id="a21a1-178">JET_dbstateForceDetach</span></span><br />
<span data-ttu-id="a21a1-179">5</span><span class="sxs-lookup"><span data-stu-id="a21a1-179">5</span></span></p></td>
<td><p><span data-ttu-id="a21a1-180">Interno.</span><span class="sxs-lookup"><span data-stu-id="a21a1-180">Internal.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a21a1-181">**lgposConsistent**</span><span class="sxs-lookup"><span data-stu-id="a21a1-181">**lgposConsistent**</span></span>

<span data-ttu-id="a21a1-182">Es NULL si la base de datos está en un estado sucio.</span><span class="sxs-lookup"><span data-stu-id="a21a1-182">Null if the database is in a dirty state.</span></span> <span data-ttu-id="a21a1-183">Esta es la posición del registro que se usó cuando la base de datos se realizó por última vez en un estado de cierre correcto.</span><span class="sxs-lookup"><span data-stu-id="a21a1-183">This is the log position that was used when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="a21a1-184">**logtimeConsistent**</span><span class="sxs-lookup"><span data-stu-id="a21a1-184">**logtimeConsistent**</span></span>

<span data-ttu-id="a21a1-185">Es NULL si la base de datos está en un estado sucio.</span><span class="sxs-lookup"><span data-stu-id="a21a1-185">Null if the database is in a dirty state.</span></span> <span data-ttu-id="a21a1-186">Esta es la hora a la que la base de datos se realizó por última vez en un estado de cierre correcto.</span><span class="sxs-lookup"><span data-stu-id="a21a1-186">This is the time when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="a21a1-187">**logtimeAttach**</span><span class="sxs-lookup"><span data-stu-id="a21a1-187">**logtimeAttach**</span></span>

<span data-ttu-id="a21a1-188">La hora a la que se adjuntó la base de datos por última vez con [JetAttachDatabase](./jetattachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="a21a1-188">The time when the database was last attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="a21a1-189">**lgposAttach**</span><span class="sxs-lookup"><span data-stu-id="a21a1-189">**lgposAttach**</span></span>

<span data-ttu-id="a21a1-190">La posición del registro que se usó la última vez que se adjuntó la base de datos con [JetAttachDatabase](./jetattachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="a21a1-190">The log position that was used the last time the database was attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="a21a1-191">**logtimeDetach**</span><span class="sxs-lookup"><span data-stu-id="a21a1-191">**logtimeDetach**</span></span>

<span data-ttu-id="a21a1-192">La hora a la que la base de datos se desconectó por última vez con [JetDetachDatabase](./jetdetachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="a21a1-192">The time when the database was last detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="a21a1-193">**lgposDetach**</span><span class="sxs-lookup"><span data-stu-id="a21a1-193">**lgposDetach**</span></span>

<span data-ttu-id="a21a1-194">La posición del registro que se usó la última vez que la base de datos se desasoció con [JetDetachDatabase](./jetdetachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="a21a1-194">The log position that was used the last time the database was detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="a21a1-195">**signLog**</span><span class="sxs-lookup"><span data-stu-id="a21a1-195">**signLog**</span></span>

<span data-ttu-id="a21a1-196">Es compatible con la infraestructura de ESE y no se puede usar en el código.</span><span class="sxs-lookup"><span data-stu-id="a21a1-196">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="a21a1-197">**bkinfoFullPrev**</span><span class="sxs-lookup"><span data-stu-id="a21a1-197">**bkinfoFullPrev**</span></span>

<span data-ttu-id="a21a1-198">Es compatible con la infraestructura de ESE y no se puede usar en el código.</span><span class="sxs-lookup"><span data-stu-id="a21a1-198">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="a21a1-199">**bkinfoIncPrev**</span><span class="sxs-lookup"><span data-stu-id="a21a1-199">**bkinfoIncPrev**</span></span>

<span data-ttu-id="a21a1-200">Es compatible con la infraestructura de ESE y no se puede usar en el código.</span><span class="sxs-lookup"><span data-stu-id="a21a1-200">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="a21a1-201">**bkinfoFullCur**</span><span class="sxs-lookup"><span data-stu-id="a21a1-201">**bkinfoFullCur**</span></span>

<span data-ttu-id="a21a1-202">Es compatible con la infraestructura de ESE y no se puede usar en el código.</span><span class="sxs-lookup"><span data-stu-id="a21a1-202">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="a21a1-203">**fShadowingDisabled**</span><span class="sxs-lookup"><span data-stu-id="a21a1-203">**fShadowingDisabled**</span></span>

<span data-ttu-id="a21a1-204">Es compatible con la infraestructura de ESE y no se puede usar en el código.</span><span class="sxs-lookup"><span data-stu-id="a21a1-204">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="a21a1-205">**fUpgradeDb**</span><span class="sxs-lookup"><span data-stu-id="a21a1-205">**fUpgradeDb**</span></span>

<span data-ttu-id="a21a1-206">Es compatible con la infraestructura de ESE y no se puede usar en el código.</span><span class="sxs-lookup"><span data-stu-id="a21a1-206">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="a21a1-207">**dwMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="a21a1-207">**dwMajorVersion**</span></span>

<span data-ttu-id="a21a1-208">Representa los números de versión de Windows NT cuando se actualizaron los índices de las bases de datos.</span><span class="sxs-lookup"><span data-stu-id="a21a1-208">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="a21a1-209">Se utiliza para actualizar los índices.</span><span class="sxs-lookup"><span data-stu-id="a21a1-209">Used for updating indexes.</span></span>

<span data-ttu-id="a21a1-210">**dwMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="a21a1-210">**dwMinorVersion**</span></span>

<span data-ttu-id="a21a1-211">Representa los números de versión de Windows NT cuando se actualizaron los índices de las bases de datos.</span><span class="sxs-lookup"><span data-stu-id="a21a1-211">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="a21a1-212">Se utiliza para actualizar los índices.</span><span class="sxs-lookup"><span data-stu-id="a21a1-212">Used for updating indexes.</span></span>

<span data-ttu-id="a21a1-213">**dwBuildNumber**</span><span class="sxs-lookup"><span data-stu-id="a21a1-213">**dwBuildNumber**</span></span>

<span data-ttu-id="a21a1-214">Representa los números de versión de Windows NT cuando se actualizaron los índices de las bases de datos.</span><span class="sxs-lookup"><span data-stu-id="a21a1-214">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="a21a1-215">Se utiliza para actualizar los índices.</span><span class="sxs-lookup"><span data-stu-id="a21a1-215">Used for updating indexes.</span></span>

<span data-ttu-id="a21a1-216">**lSPNumber**</span><span class="sxs-lookup"><span data-stu-id="a21a1-216">**lSPNumber**</span></span>

<span data-ttu-id="a21a1-217">Representa los números de versión de Windows NT cuando se actualizaron los índices de las bases de datos.</span><span class="sxs-lookup"><span data-stu-id="a21a1-217">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="a21a1-218">Se utiliza para actualizar los índices.</span><span class="sxs-lookup"><span data-stu-id="a21a1-218">Used for updating indexes.</span></span>

<span data-ttu-id="a21a1-219">**cbPageSize**</span><span class="sxs-lookup"><span data-stu-id="a21a1-219">**cbPageSize**</span></span>

<span data-ttu-id="a21a1-220">Tamaño de página de base de datos.</span><span class="sxs-lookup"><span data-stu-id="a21a1-220">Database page size.</span></span> <span data-ttu-id="a21a1-221">0 significa que el tamaño de página es 4 KB.</span><span class="sxs-lookup"><span data-stu-id="a21a1-221">0 means the page size is 4 KB.</span></span>

<span data-ttu-id="a21a1-222">Este valor se recupera solo si JET_DbInfoMisc se pasó a [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) o [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="a21a1-222">This value is retrieved only if JET_DbInfoMisc was passed to [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) or [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span></span>

<span data-ttu-id="a21a1-223">**genMinRequired**</span><span class="sxs-lookup"><span data-stu-id="a21a1-223">**genMinRequired**</span></span>

<span data-ttu-id="a21a1-224">Representa la generación de registro mínima necesaria para reproducir los registros.</span><span class="sxs-lookup"><span data-stu-id="a21a1-224">Represents the minimum log generation required for replaying the logs.</span></span> <span data-ttu-id="a21a1-225">Normalmente, es lo mismo que la generación de puntos de control.</span><span class="sxs-lookup"><span data-stu-id="a21a1-225">This is typically the same as the checkpoint generation.</span></span>

<span data-ttu-id="a21a1-226">**genMaxRequired**</span><span class="sxs-lookup"><span data-stu-id="a21a1-226">**genMaxRequired**</span></span>

<span data-ttu-id="a21a1-227">Representa la generación de registro máxima necesaria para reproducir los registros.</span><span class="sxs-lookup"><span data-stu-id="a21a1-227">Represents the maximum log generation required for replaying the logs.</span></span>

<span data-ttu-id="a21a1-228">**logtimeGenMaxCreate**</span><span class="sxs-lookup"><span data-stu-id="a21a1-228">**logtimeGenMaxCreate**</span></span>

<span data-ttu-id="a21a1-229">Representa la fecha y hora de creación del archivo de registro genMax.</span><span class="sxs-lookup"><span data-stu-id="a21a1-229">Represents the creation date and time of the genMax log file.</span></span>

<span data-ttu-id="a21a1-230">**ulRepairCount**</span><span class="sxs-lookup"><span data-stu-id="a21a1-230">**ulRepairCount**</span></span>

<span data-ttu-id="a21a1-231">Número de veces que se ha llamado a una reparación en esta base de datos.</span><span class="sxs-lookup"><span data-stu-id="a21a1-231">The number of times a repair has been called on this database.</span></span>

<span data-ttu-id="a21a1-232">**logtimeRepair**</span><span class="sxs-lookup"><span data-stu-id="a21a1-232">**logtimeRepair**</span></span>

<span data-ttu-id="a21a1-233">Representa la fecha y hora en que se ejecutó la última reparación.</span><span class="sxs-lookup"><span data-stu-id="a21a1-233">Represents the date and time the last repair was run.</span></span>

<span data-ttu-id="a21a1-234">**ulRepairCountOld**</span><span class="sxs-lookup"><span data-stu-id="a21a1-234">**ulRepairCountOld**</span></span>

<span data-ttu-id="a21a1-235">El número de veces que la reparación se ha ejecutado en esta base de datos antes de la última desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="a21a1-235">The number of times the repair had been run on this database before the last defragmentation.</span></span>

<span data-ttu-id="a21a1-236">**ulECCFixSuccess**</span><span class="sxs-lookup"><span data-stu-id="a21a1-236">**ulECCFixSuccess**</span></span>

<span data-ttu-id="a21a1-237">Número de veces que se corrigió un error de un bit y resultó en una buena página.</span><span class="sxs-lookup"><span data-stu-id="a21a1-237">The number of times a one bit error was fixed and resulted in a good page.</span></span>

<span data-ttu-id="a21a1-238">**logtimeECCFixSuccess**</span><span class="sxs-lookup"><span data-stu-id="a21a1-238">**logtimeECCFixSuccess**</span></span>

<span data-ttu-id="a21a1-239">Representa la fecha y hora en que se corrigió el último error de bit y resultó en una buena página.</span><span class="sxs-lookup"><span data-stu-id="a21a1-239">Represents the date and time the last one bit error was fixed and resulted in a good page.</span></span>

<span data-ttu-id="a21a1-240">**ulECCFixSuccessOld**</span><span class="sxs-lookup"><span data-stu-id="a21a1-240">**ulECCFixSuccessOld**</span></span>

<span data-ttu-id="a21a1-241">Representa el número de veces que se corrigió un error de un bit y resultó en una buena página antes de la última reparación.</span><span class="sxs-lookup"><span data-stu-id="a21a1-241">Represents the number of times a one bit error was fixed and resulted in a good page before last repair.</span></span>

<span data-ttu-id="a21a1-242">**ulECCFixFail**</span><span class="sxs-lookup"><span data-stu-id="a21a1-242">**ulECCFixFail**</span></span>

<span data-ttu-id="a21a1-243">Número de veces que se corrigió un error de un bit y resultó en una página incorrecta.</span><span class="sxs-lookup"><span data-stu-id="a21a1-243">The number of times a one bit error was fixed and resulted in a bad page.</span></span>

<span data-ttu-id="a21a1-244">**logtimeECCFixFail**</span><span class="sxs-lookup"><span data-stu-id="a21a1-244">**logtimeECCFixFail**</span></span>

<span data-ttu-id="a21a1-245">Representa la fecha y hora en que se corrigió el último error de bit y resultó en una página incorrecta.</span><span class="sxs-lookup"><span data-stu-id="a21a1-245">Represents the date and time the last one bit error was fixed and resulted in a bad page.</span></span>

<span data-ttu-id="a21a1-246">**ulECCFixFailOld**</span><span class="sxs-lookup"><span data-stu-id="a21a1-246">**ulECCFixFailOld**</span></span>

<span data-ttu-id="a21a1-247">Número de veces que se corrigió un error de un bit y resultó en una página incorrecta antes de la última reparación.</span><span class="sxs-lookup"><span data-stu-id="a21a1-247">The number of times a one bit error was fixed and resulted in a bad page before last repair.</span></span>

<span data-ttu-id="a21a1-248">**ulBadChecksum**</span><span class="sxs-lookup"><span data-stu-id="a21a1-248">**ulBadChecksum**</span></span>

<span data-ttu-id="a21a1-249">Número de veces que se ha encontrado un error de ECC/checksum que no se pudo corregir.</span><span class="sxs-lookup"><span data-stu-id="a21a1-249">The number of times a non-correctable ECC/checksum error was found.</span></span>

<span data-ttu-id="a21a1-250">**logtimeBadChecksum**</span><span class="sxs-lookup"><span data-stu-id="a21a1-250">**logtimeBadChecksum**</span></span>

<span data-ttu-id="a21a1-251">Representa la fecha y hora en que se encontró el último error de ECC o suma de comprobación que no se pudo corregir.</span><span class="sxs-lookup"><span data-stu-id="a21a1-251">Represents the date and time the last non-correctable ECC/checksum error was found.</span></span>

<span data-ttu-id="a21a1-252">**ulBadChecksumOld**</span><span class="sxs-lookup"><span data-stu-id="a21a1-252">**ulBadChecksumOld**</span></span>

<span data-ttu-id="a21a1-253">Número de veces que se ha encontrado un error de ECC/checksum no corregible antes de la última reparación.</span><span class="sxs-lookup"><span data-stu-id="a21a1-253">The number of times a non-correctable ECC/checksum error was found before last repair.</span></span>

<span data-ttu-id="a21a1-254">**genCommitted**</span><span class="sxs-lookup"><span data-stu-id="a21a1-254">**genCommitted**</span></span>

<span data-ttu-id="a21a1-255">Generación del registro actual.</span><span class="sxs-lookup"><span data-stu-id="a21a1-255">The current log generation.</span></span> <span data-ttu-id="a21a1-256">Puede ser menor que genMaxRequired si JET_paramWaypointLatency es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="a21a1-256">This can be less than genMaxRequired if JET_paramWaypointLatency is non-zero.</span></span>

### <a name="requirements"></a><span data-ttu-id="a21a1-257">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a21a1-257">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a21a1-258"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="a21a1-258"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a21a1-259">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a21a1-259">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a21a1-260"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a21a1-260"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a21a1-261">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a21a1-261">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a21a1-262"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a21a1-262"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a21a1-263">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="a21a1-263">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="a21a1-264">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a21a1-264">See Also</span></span>

[<span data-ttu-id="a21a1-265">JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="a21a1-265">JET_BKINFO</span></span>](./jet-bkinfo-structure.md)  
[<span data-ttu-id="a21a1-266">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="a21a1-266">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="a21a1-267">JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="a21a1-267">JET_LGPOS</span></span>](./jet-lgpos-structure.md)  
[<span data-ttu-id="a21a1-268">JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="a21a1-268">JET_SIGNATURE</span></span>](./jet-signature-structure.md)  
[<span data-ttu-id="a21a1-269">JetGetDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="a21a1-269">JetGetDatabaseInfo</span></span>](./jetgetdatabaseinfo-function.md)  
[<span data-ttu-id="a21a1-270">JetGetDatabaseFileInfo</span><span class="sxs-lookup"><span data-stu-id="a21a1-270">JetGetDatabaseFileInfo</span></span>](./jetgetdatabasefileinfo-function.md)
