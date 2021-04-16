---
description: 'Más información acerca de: estructura de JET_DBINFOMISC'
title: Estructura de JET_DBINFOMISC
TOCTitle: JET_DBINFOMISC Structure
ms:assetid: ff287087-35b8-495e-9922-418ec2439e19
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294147(v=EXCHG.10)
ms:contentKeyID: 32765761
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 649e16e956e5dcd272e6201f779cdddd352a7bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540094"
---
# <a name="jet_dbinfomisc-structure"></a><span data-ttu-id="ca568-103">Estructura de JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="ca568-103">JET_DBINFOMISC Structure</span></span>


<span data-ttu-id="ca568-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ca568-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dbinfomisc-structure"></a><span data-ttu-id="ca568-105">Estructura de JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="ca568-105">JET_DBINFOMISC Structure</span></span>

<span data-ttu-id="ca568-106">La estructura **JET_DBINFOMISC** contiene información diversa sobre una base de datos.</span><span class="sxs-lookup"><span data-stu-id="ca568-106">The **JET_DBINFOMISC** structure holds miscellaneous information about a database.</span></span> <span data-ttu-id="ca568-107">Esta es la información contenida en el encabezado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="ca568-107">This is the information that is contained in the database header.</span></span>

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
    } JET_DBINFOMISC;
```

### <a name="members"></a><span data-ttu-id="ca568-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ca568-108">Members</span></span>

<span data-ttu-id="ca568-109">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="ca568-109">**ulVersion**</span></span>

<span data-ttu-id="ca568-110">Versión nativa del motor de base de datos que creó la base de datos.</span><span class="sxs-lookup"><span data-stu-id="ca568-110">The native version of the database engine that created the database.</span></span> <span data-ttu-id="ca568-111">Vea [JetGetVersion](./jetgetversion-function.md) para recuperar la versión nativa del motor de base de datos actual.</span><span class="sxs-lookup"><span data-stu-id="ca568-111">See [JetGetVersion](./jetgetversion-function.md) to retrieve the native version for the current database engine.</span></span>

<span data-ttu-id="ca568-112">**ulUpdate**</span><span class="sxs-lookup"><span data-stu-id="ca568-112">**ulUpdate**</span></span>

<span data-ttu-id="ca568-113">Realiza un seguimiento de las actualizaciones de formato de base de datos incrementales que son compatibles con versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="ca568-113">Tracks incremental database format updates that are backward compatible.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ca568-114">ulVersion, ulUpdate =</span><span class="sxs-lookup"><span data-stu-id="ca568-114">ulVersion, ulUpdate =</span></span></p></th>
<th><p><span data-ttu-id="ca568-115">Significado</span><span class="sxs-lookup"><span data-stu-id="ca568-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca568-116">0x620, 0</span><span class="sxs-lookup"><span data-stu-id="ca568-116">0x620,0</span></span></p></td>
<td><p><span data-ttu-id="ca568-117">Formato original de la versión beta del sistema operativo (4/22/97).</span><span class="sxs-lookup"><span data-stu-id="ca568-117">Original operating system Beta format (4/22/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca568-118">0x620, 1</span><span class="sxs-lookup"><span data-stu-id="ca568-118">0x620,1</span></span></p></td>
<td><p><span data-ttu-id="ca568-119">Agregue columnas en el catálogo para la indización condicional y OLD (5/29/97).</span><span class="sxs-lookup"><span data-stu-id="ca568-119">Add columns in the catalog for conditional indexing and OLD (5/29/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca568-120">0x620, 2</span><span class="sxs-lookup"><span data-stu-id="ca568-120">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="ca568-121">Agregue la marca fLocalizedText en IDB (6/5/97).</span><span class="sxs-lookup"><span data-stu-id="ca568-121">Add the fLocalizedText flag in IDB (6/5/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca568-122">0x620, 3</span><span class="sxs-lookup"><span data-stu-id="ca568-122">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="ca568-123">Agregue SPLIT_BUFFER a las páginas raíz del árbol de espacio (10/30/97).</span><span class="sxs-lookup"><span data-stu-id="ca568-123">Add SPLIT_BUFFER to space tree root pages (10/30/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca568-124">0x620, 2</span><span class="sxs-lookup"><span data-stu-id="ca568-124">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="ca568-125">Revertir revisión para que ESE97 siga siendo compatible con el avance (1/28/98).</span><span class="sxs-lookup"><span data-stu-id="ca568-125">Revert revision in order for ESE97 to remain forward-compatible (1/28/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca568-126">0x620, 3</span><span class="sxs-lookup"><span data-stu-id="ca568-126">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="ca568-127">Agregue nuevas columnas etiquetadas al catálogo ( &quot; CallbackData &quot; y &quot; CallbackDependencies &quot; ).</span><span class="sxs-lookup"><span data-stu-id="ca568-127">Add new tagged columns to catalog (&quot;CallbackData&quot; and &quot;CallbackDependencies&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca568-128">0x620, 4</span><span class="sxs-lookup"><span data-stu-id="ca568-128">0x620,4</span></span></p></td>
<td><p><span data-ttu-id="ca568-129">Compatibilidad con SLV: signSLV, fSLVExists en el encabezado dB (5/5/98).</span><span class="sxs-lookup"><span data-stu-id="ca568-129">SLV support: signSLV, fSLVExists in db header (5/5/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca568-130">0x620, 5</span><span class="sxs-lookup"><span data-stu-id="ca568-130">0x620,5</span></span></p></td>
<td><p><span data-ttu-id="ca568-131">Nuevo árbol de espacio SLV (5/29/98).</span><span class="sxs-lookup"><span data-stu-id="ca568-131">New SLV space tree (5/29/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca568-132">0x620, 6</span><span class="sxs-lookup"><span data-stu-id="ca568-132">0x620,6</span></span></p></td>
<td><p><span data-ttu-id="ca568-133">Mapa de espacio SLV (10/12/98).</span><span class="sxs-lookup"><span data-stu-id="ca568-133">SLV space map (10/12/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca568-134">0x620, 7</span><span class="sxs-lookup"><span data-stu-id="ca568-134">0x620,7</span></span></p></td>
<td><p><span data-ttu-id="ca568-135">IDXSEG de 4 bytes (12/10/98).</span><span class="sxs-lookup"><span data-stu-id="ca568-135">4-byte IDXSEG (12/10/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca568-136">0x620, 8</span><span class="sxs-lookup"><span data-stu-id="ca568-136">0x620,8</span></span></p></td>
<td><p><span data-ttu-id="ca568-137">Nuevo formato de columna de plantilla (1/25/99).</span><span class="sxs-lookup"><span data-stu-id="ca568-137">New template column format (1/25/99).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca568-138">0x620, 9</span><span class="sxs-lookup"><span data-stu-id="ca568-138">0x620,9</span></span></p></td>
<td><p><span data-ttu-id="ca568-139">Columnas de plantilla ordenadas (6/24/99).</span><span class="sxs-lookup"><span data-stu-id="ca568-139">Sorted template columns (6/24/99).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca568-140">0x623, 0</span><span class="sxs-lookup"><span data-stu-id="ca568-140">0x623,0</span></span></p></td>
<td><p><span data-ttu-id="ca568-141">Nuevo administrador de espacio (5/15/99).</span><span class="sxs-lookup"><span data-stu-id="ca568-141">New Space Manager (5/15/99).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ca568-142">**signDb**</span><span class="sxs-lookup"><span data-stu-id="ca568-142">**signDb**</span></span>

<span data-ttu-id="ca568-143">Firma de la base de datos (incluida la hora de creación).</span><span class="sxs-lookup"><span data-stu-id="ca568-143">Signature of the database (including creation time).</span></span> <span data-ttu-id="ca568-144">Esta estructura es de 28 bytes.</span><span class="sxs-lookup"><span data-stu-id="ca568-144">This structure is 28 bytes.</span></span>

<span data-ttu-id="ca568-145">**dbstate**</span><span class="sxs-lookup"><span data-stu-id="ca568-145">**dbstate**</span></span>

<span data-ttu-id="ca568-146">Este es el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="ca568-146">This is the database state.</span></span>

<span data-ttu-id="ca568-147">Las siguientes opciones están disponibles para este miembro.</span><span class="sxs-lookup"><span data-stu-id="ca568-147">The following options are available for this member.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ca568-148">Value</span><span class="sxs-lookup"><span data-stu-id="ca568-148">Value</span></span></p></th>
<th><p><span data-ttu-id="ca568-149">Significado</span><span class="sxs-lookup"><span data-stu-id="ca568-149">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca568-150">JET_dbstateJustCreated</span><span class="sxs-lookup"><span data-stu-id="ca568-150">JET_dbstateJustCreated</span></span><br />
<span data-ttu-id="ca568-151">1</span><span class="sxs-lookup"><span data-stu-id="ca568-151">1</span></span></p></td>
<td><p><span data-ttu-id="ca568-152">Se acaba de crear la base de datos.</span><span class="sxs-lookup"><span data-stu-id="ca568-152">The database was just created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca568-153">JET_dbstateDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="ca568-153">JET_dbstateDirtyShutdown</span></span><br />
<span data-ttu-id="ca568-154">2</span><span class="sxs-lookup"><span data-stu-id="ca568-154">2</span></span></p></td>
<td><p><span data-ttu-id="ca568-155">La base de datos requiere que se ejecute la recuperación de hardware o software para que se pueda usar o mover.</span><span class="sxs-lookup"><span data-stu-id="ca568-155">The database requires hard or soft recovery to be run in order to become usable or moveable.</span></span> <span data-ttu-id="ca568-156">No debe intentar trasladar las bases de datos en este estado.</span><span class="sxs-lookup"><span data-stu-id="ca568-156">One should not try to move databases in this state.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca568-157">JET_dbstateCleanShutdown</span><span class="sxs-lookup"><span data-stu-id="ca568-157">JET_dbstateCleanShutdown</span></span><br />
<span data-ttu-id="ca568-158">3</span><span class="sxs-lookup"><span data-stu-id="ca568-158">3</span></span></p></td>
<td><p><span data-ttu-id="ca568-159">La base de datos está en un estado limpio.</span><span class="sxs-lookup"><span data-stu-id="ca568-159">The database is in a clean state.</span></span> <span data-ttu-id="ca568-160">La base de datos se puede adjuntar sin ningún archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="ca568-160">The database can be attached without any log files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca568-161">JET_dbstateBeingConverted</span><span class="sxs-lookup"><span data-stu-id="ca568-161">JET_dbstateBeingConverted</span></span><br />
<span data-ttu-id="ca568-162">4</span><span class="sxs-lookup"><span data-stu-id="ca568-162">4</span></span></p></td>
<td><p><span data-ttu-id="ca568-163">La base de datos se está actualizando.</span><span class="sxs-lookup"><span data-stu-id="ca568-163">The database is being upgraded.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca568-164">JET_dbstateForceDetach</span><span class="sxs-lookup"><span data-stu-id="ca568-164">JET_dbstateForceDetach</span></span><br />
<span data-ttu-id="ca568-165">5</span><span class="sxs-lookup"><span data-stu-id="ca568-165">5</span></span></p></td>
<td><p><span data-ttu-id="ca568-166">Interno.</span><span class="sxs-lookup"><span data-stu-id="ca568-166">Internal.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ca568-167">**lgposConsistent**</span><span class="sxs-lookup"><span data-stu-id="ca568-167">**lgposConsistent**</span></span>

<span data-ttu-id="ca568-168">Es NULL si la base de datos está en un estado sucio.</span><span class="sxs-lookup"><span data-stu-id="ca568-168">Null if the database is in a dirty state.</span></span> <span data-ttu-id="ca568-169">Esta es la posición del registro que se usó cuando la base de datos se realizó por última vez en un estado de cierre correcto.</span><span class="sxs-lookup"><span data-stu-id="ca568-169">This is the log position that was used when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="ca568-170">**logtimeConsistent**</span><span class="sxs-lookup"><span data-stu-id="ca568-170">**logtimeConsistent**</span></span>

<span data-ttu-id="ca568-171">Es NULL si la base de datos está en un estado sucio.</span><span class="sxs-lookup"><span data-stu-id="ca568-171">Null if the database is in a dirty state.</span></span> <span data-ttu-id="ca568-172">Esta es la hora a la que la base de datos se realizó por última vez en un estado de cierre correcto.</span><span class="sxs-lookup"><span data-stu-id="ca568-172">This is the time when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="ca568-173">**logtimeAttach**</span><span class="sxs-lookup"><span data-stu-id="ca568-173">**logtimeAttach**</span></span>

<span data-ttu-id="ca568-174">La hora a la que se adjuntó la base de datos por última vez con [JetAttachDatabase](./jetattachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="ca568-174">The time when the database was last attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="ca568-175">**lgposAttach**</span><span class="sxs-lookup"><span data-stu-id="ca568-175">**lgposAttach**</span></span>

<span data-ttu-id="ca568-176">La posición del registro que se usó la última vez que se adjuntó la base de datos con [JetAttachDatabase](./jetattachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="ca568-176">The log position that was used the last time the database was attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="ca568-177">**logtimeDetach**</span><span class="sxs-lookup"><span data-stu-id="ca568-177">**logtimeDetach**</span></span>

<span data-ttu-id="ca568-178">La hora a la que la base de datos se desconectó por última vez con [JetDetachDatabase](./jetdetachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="ca568-178">The time when the database was last detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="ca568-179">**lgposDetach**</span><span class="sxs-lookup"><span data-stu-id="ca568-179">**lgposDetach**</span></span>

<span data-ttu-id="ca568-180">La posición del registro que se usó la última vez que la base de datos se desasoció con [JetDetachDatabase](./jetdetachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="ca568-180">The log position that was used the last time the database was detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="ca568-181">**signLog**</span><span class="sxs-lookup"><span data-stu-id="ca568-181">**signLog**</span></span>

<span data-ttu-id="ca568-182">Es compatible con la infraestructura de ESE y no se puede usar en el código.</span><span class="sxs-lookup"><span data-stu-id="ca568-182">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="ca568-183">**bkinfoFullPrev**</span><span class="sxs-lookup"><span data-stu-id="ca568-183">**bkinfoFullPrev**</span></span>

<span data-ttu-id="ca568-184">Es compatible con la infraestructura de ESE y no se puede usar en el código.</span><span class="sxs-lookup"><span data-stu-id="ca568-184">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="ca568-185">**bkinfoIncPrev**</span><span class="sxs-lookup"><span data-stu-id="ca568-185">**bkinfoIncPrev**</span></span>

<span data-ttu-id="ca568-186">Es compatible con la infraestructura de ESE y no se puede usar en el código.</span><span class="sxs-lookup"><span data-stu-id="ca568-186">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="ca568-187">**bkinfoFullCur**</span><span class="sxs-lookup"><span data-stu-id="ca568-187">**bkinfoFullCur**</span></span>

<span data-ttu-id="ca568-188">Es compatible con la infraestructura de ESE y no se puede usar en el código.</span><span class="sxs-lookup"><span data-stu-id="ca568-188">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="ca568-189">**fShadowingDisabled**</span><span class="sxs-lookup"><span data-stu-id="ca568-189">**fShadowingDisabled**</span></span>

<span data-ttu-id="ca568-190">Es compatible con la infraestructura de ESE y no se puede usar en el código.</span><span class="sxs-lookup"><span data-stu-id="ca568-190">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="ca568-191">**fUpgradeDb**</span><span class="sxs-lookup"><span data-stu-id="ca568-191">**fUpgradeDb**</span></span>

<span data-ttu-id="ca568-192">Es compatible con la infraestructura de ESE y no se puede usar en el código.</span><span class="sxs-lookup"><span data-stu-id="ca568-192">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="ca568-193">**dwMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="ca568-193">**dwMajorVersion**</span></span>

<span data-ttu-id="ca568-194">Representa los números de versión de Windows NT cuando se actualizaron los índices de las bases de datos.</span><span class="sxs-lookup"><span data-stu-id="ca568-194">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="ca568-195">Se utiliza para actualizar los índices.</span><span class="sxs-lookup"><span data-stu-id="ca568-195">Used for updating indexes.</span></span>

<span data-ttu-id="ca568-196">**dwMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="ca568-196">**dwMinorVersion**</span></span>

<span data-ttu-id="ca568-197">Representa los números de versión de Windows NT cuando se actualizaron los índices de las bases de datos.</span><span class="sxs-lookup"><span data-stu-id="ca568-197">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="ca568-198">Se utiliza para actualizar los índices.</span><span class="sxs-lookup"><span data-stu-id="ca568-198">Used for updating indexes.</span></span>

<span data-ttu-id="ca568-199">**dwBuildNumber**</span><span class="sxs-lookup"><span data-stu-id="ca568-199">**dwBuildNumber**</span></span>

<span data-ttu-id="ca568-200">Representa los números de versión de Windows NT cuando se actualizaron los índices de las bases de datos.</span><span class="sxs-lookup"><span data-stu-id="ca568-200">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="ca568-201">Se utiliza para actualizar los índices.</span><span class="sxs-lookup"><span data-stu-id="ca568-201">Used for updating indexes.</span></span>

<span data-ttu-id="ca568-202">**lSPNumber**</span><span class="sxs-lookup"><span data-stu-id="ca568-202">**lSPNumber**</span></span>

<span data-ttu-id="ca568-203">Representa los números de versión de Windows NT cuando se actualizaron los índices de las bases de datos.</span><span class="sxs-lookup"><span data-stu-id="ca568-203">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="ca568-204">Se utiliza para actualizar los índices.</span><span class="sxs-lookup"><span data-stu-id="ca568-204">Used for updating indexes.</span></span>

<span data-ttu-id="ca568-205">**cbPageSize**</span><span class="sxs-lookup"><span data-stu-id="ca568-205">**cbPageSize**</span></span>

<span data-ttu-id="ca568-206">Tamaño de página de base de datos.</span><span class="sxs-lookup"><span data-stu-id="ca568-206">Database page size.</span></span> <span data-ttu-id="ca568-207">0 significa que el tamaño de página es 4 KB.</span><span class="sxs-lookup"><span data-stu-id="ca568-207">0 means the page size is 4 KB.</span></span>

<span data-ttu-id="ca568-208">Este valor se recupera solo si JET_DbInfoMisc se pasó a [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) o [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="ca568-208">This value is retrieved only if JET_DbInfoMisc was passed to [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) or [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="ca568-209">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca568-209">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca568-210"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="ca568-210"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ca568-211">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ca568-211">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca568-212"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ca568-212"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ca568-213">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ca568-213">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca568-214"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="ca568-214"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ca568-215">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="ca568-215">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="ca568-216">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ca568-216">See Also</span></span>

[<span data-ttu-id="ca568-217">JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="ca568-217">JET_BKINFO</span></span>](./jet-bkinfo-structure.md)  
[<span data-ttu-id="ca568-218">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="ca568-218">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="ca568-219">JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="ca568-219">JET_LGPOS</span></span>](./jet-lgpos-structure.md)  
[<span data-ttu-id="ca568-220">JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="ca568-220">JET_SIGNATURE</span></span>](./jet-signature-structure.md)  
[<span data-ttu-id="ca568-221">JetGetDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="ca568-221">JetGetDatabaseInfo</span></span>](./jetgetdatabaseinfo-function.md)  
[<span data-ttu-id="ca568-222">JetGetDatabaseFileInfo</span><span class="sxs-lookup"><span data-stu-id="ca568-222">JetGetDatabaseFileInfo</span></span>](./jetgetdatabasefileinfo-function.md)
