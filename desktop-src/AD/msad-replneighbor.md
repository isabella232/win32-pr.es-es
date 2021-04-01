---
title: MSAD_ReplNeighbor (clase)
description: Representa la \_ estructura de vecinos de REPL de DS \_ , que contiene la información de estado de la replicación de entrada para un par de contexto de nomenclatura (NC) y de servidor de origen determinados.
ms.assetid: fdd3934b-a3f6-49ad-827b-077bcd21cf23
ms.tgt_platform: multiple
keywords:
- MSAD_ReplNeighbor clase Active Directory
- Active Directory de MSAD_ReplNeighbor de clase, se describe
topic_type:
- apiref
api_name:
- MSAD_ReplNeighbor
- MSAD_ReplNeighbor.NamingContextDN
- MSAD_ReplNeighbor.SourceDsaObjGuid
- MSAD_ReplNeighbor.NamingContextObjGuid
- MSAD_ReplNeighbor.SourceDsaDN
- MSAD_ReplNeighbor.SourceDsaAddress
- MSAD_ReplNeighbor.SourceDsaInvocationID
- MSAD_ReplNeighbor.AsyncIntersiteTransportDN
- MSAD_ReplNeighbor.AsyncIntersiteTransportObjGuid
- MSAD_ReplNeighbor.USNLastObjChangeSynced
- MSAD_ReplNeighbor.USNAttributeFilter
- MSAD_ReplNeighbor.TimeOfLastSyncSuccess
- MSAD_ReplNeighbor.TimeOfLastSyncAttempt
- MSAD_ReplNeighbor.LastSyncResult
- MSAD_ReplNeighbor.NumConsecutiveSyncFailures
- MSAD_ReplNeighbor.ReplicaFlags
- MSAD_ReplNeighbor.Writeable
- MSAD_ReplNeighbor.SyncOnStartup
- MSAD_ReplNeighbor.DoScheduledSyncs
- MSAD_ReplNeighbor.UseAsyncIntersiteTransport
- MSAD_ReplNeighbor.TwoWaySync
- MSAD_ReplNeighbor.FullSyncInProgress
- MSAD_ReplNeighbor.FullSyncNextPacket
- MSAD_ReplNeighbor.NeverSynced
- MSAD_ReplNeighbor.IgnoreChangeNotifications
- MSAD_ReplNeighbor.DisableScheduledSync
- MSAD_ReplNeighbor.CompressChanges
- MSAD_ReplNeighbor.NoChangeNotifications
- MSAD_ReplNeighbor.SourceDsaSite
- MSAD_ReplNeighbor.SourceDsaCN
- MSAD_ReplNeighbor.Domain
- MSAD_ReplNeighbor.IsDeletedSourceDsa
- MSAD_ReplNeighbor.ModifiedNumConsecutiveSyncFailures
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9554c73c7fb84aad10ae6dda51480a7644d8434a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996436"
---
# <a name="msad_replneighbor-class"></a><span data-ttu-id="85d52-105">MSAD \_ ReplNeighbor (clase)</span><span class="sxs-lookup"><span data-stu-id="85d52-105">MSAD\_ReplNeighbor class</span></span>

<span data-ttu-id="85d52-106">Representa la estructura de [**\_ \_ vecinos de REPL de DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw) , que contiene la información de estado de la replicación de entrada para un determinado contexto de nomenclatura (NC) y de servidor de origen, tal y como lo devuelve la función [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) .</span><span class="sxs-lookup"><span data-stu-id="85d52-106">Represents the [**DS\_REPL\_NEIGHBOR**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw) structure, which contains the inbound replication state information for a particular naming context (NC) and source server pair, as returned by the [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="85d52-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85d52-107">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplNeighbor
{
  String   NamingContextDN;
  String   SourceDsaObjGuid;
  String   NamingContextObjGuid;
  String   SourceDsaDN;
  String   SourceDsaAddress;
  String   SourceDsaInvocationID;
  String   AsyncIntersiteTransportDN;
  String   AsyncIntersiteTransportObjGuid;
  uint64   USNLastObjChangeSynced;
  uint64   USNAttributeFilter;
  datetime TimeOfLastSyncSuccess;
  datetime TimeOfLastSyncAttempt;
  uint32   LastSyncResult;
  uint32   NumConsecutiveSyncFailures;
  uint32   ReplicaFlags;
  boolean  Writeable = FALSE;
  boolean  SyncOnStartup = FALSE;
  boolean  DoScheduledSyncs = FALSE;
  boolean  UseAsyncIntersiteTransport = FALSE;
  boolean  TwoWaySync = FALSE;
  boolean  FullSyncInProgress = FALSE;
  boolean  FullSyncNextPacket = FALSE;
  boolean  NeverSynced = FALSE;
  boolean  IgnoreChangeNotifications = FALSE;
  boolean  DisableScheduledSync = FALSE;
  boolean  CompressChanges = FALSE;
  boolean  NoChangeNotifications = FALSE;
  String   SourceDsaSite;
  String   SourceDsaCN;
  String   Domain;
  boolean  IsDeletedSourceDsa = FALSE;
  uint32   ModifiedNumConsecutiveSyncFailures;
};
```

## <a name="members"></a><span data-ttu-id="85d52-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="85d52-108">Members</span></span>

<span data-ttu-id="85d52-109">La clase **MSAD \_ ReplNeighbor** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="85d52-109">The **MSAD\_ReplNeighbor** class has these types of members:</span></span>

-   [<span data-ttu-id="85d52-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="85d52-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="85d52-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="85d52-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="85d52-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="85d52-112">Methods</span></span>

<span data-ttu-id="85d52-113">La clase **MSAD \_ ReplNeighbor** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="85d52-113">The **MSAD\_ReplNeighbor** class has these methods.</span></span>



| <span data-ttu-id="85d52-114">Método</span><span class="sxs-lookup"><span data-stu-id="85d52-114">Method</span></span>                                                           | <span data-ttu-id="85d52-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="85d52-115">Description</span></span>                                                                   |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="85d52-116">**SyncNamingContext**</span><span class="sxs-lookup"><span data-stu-id="85d52-116">**SyncNamingContext**</span></span>](syncnamingcontext-msad-replneighbor.md) | <span data-ttu-id="85d52-117">Sincroniza un contexto de nomenclatura de destino con uno de sus orígenes.</span><span class="sxs-lookup"><span data-stu-id="85d52-117">Synchronizes a destination naming context with one of its sources.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="85d52-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="85d52-118">Properties</span></span>

<span data-ttu-id="85d52-119">La clase **MSAD \_ ReplNeighbor** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="85d52-119">The **MSAD\_ReplNeighbor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="85d52-120">**AsyncIntersiteTransportDN**</span><span class="sxs-lookup"><span data-stu-id="85d52-120">**AsyncIntersiteTransportDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85d52-121">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85d52-123">Obtiene la ruta de acceso X. 500 del objeto [**interSiteTransport**](/windows/desktop/ADSchema/c-intersitetransport) que corresponde al transporte en el que se realiza la replicación.</span><span class="sxs-lookup"><span data-stu-id="85d52-123">Gets the X.500 path of the [**interSiteTransport**](/windows/desktop/ADSchema/c-intersitetransport) object that corresponds to the transport over which replication is performed.</span></span> <span data-ttu-id="85d52-124">Establezca en **null** para la replicación de RPC/IP.</span><span class="sxs-lookup"><span data-stu-id="85d52-124">Set to **NULL** for RPC/IP replication.</span></span>

</dd> <dt>

<span data-ttu-id="85d52-125">**AsyncIntersiteTransportObjGuid**</span><span class="sxs-lookup"><span data-stu-id="85d52-125">**AsyncIntersiteTransportObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85d52-126">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85d52-128">Obtiene el GUID del objeto de transporte entre sitios que corresponde a la propiedad **AsyncIntersiteTransportDN** .</span><span class="sxs-lookup"><span data-stu-id="85d52-128">Gets the GUID of the intersite transport object that corresponds to the **AsyncIntersiteTransportDN** property.</span></span>

</dd> <dt>

<span data-ttu-id="85d52-129">**CompressChanges**</span><span class="sxs-lookup"><span data-stu-id="85d52-129">**CompressChanges**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-130">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="85d52-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85d52-132">Obtiene el valor que indica si se ha establecido la marca de **NBR de replicación de DS para \_ \_ \_ comprimir \_ cambios** en la propiedad **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="85d52-132">Gets the value that indicates whether the **DS\_REPL\_NBR\_COMPRESS\_CHANGES** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="85d52-133">**DisableScheduledSync**</span><span class="sxs-lookup"><span data-stu-id="85d52-133">**DisableScheduledSync**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-134">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="85d52-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85d52-136">Obtiene el valor que indica si se ha establecido en la propiedad **ReplicaFlags** la propiedad NBR de la **replicación de DS \_ \_ \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="85d52-136">Gets the value that indicates whether the **DS\_REPL\_NBR\_DISABLE\_SCHEDULED\_SYNC** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="85d52-137">**Dominio**</span><span class="sxs-lookup"><span data-stu-id="85d52-137">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85d52-138">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85d52-140">Obtiene el nombre canónico del dominio del NC replicado.</span><span class="sxs-lookup"><span data-stu-id="85d52-140">Gets the canonical name of the domain of the replicated NC.</span></span>

</dd> <dt>

<span data-ttu-id="85d52-141">**DoScheduledSyncs**</span><span class="sxs-lookup"><span data-stu-id="85d52-141">**DoScheduledSyncs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-142">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="85d52-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85d52-144">Obtiene el valor que indica si se ha establecido la marca de **\_ \_ \_ \_ \_ sincronización programada de NBR de replicación de DS** en la propiedad **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="85d52-144">Gets the value that indicates whether the **DS\_REPL\_NBR\_DO\_SCHEDULED\_SYNCS** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="85d52-145">**FullSyncInProgress**</span><span class="sxs-lookup"><span data-stu-id="85d52-145">**FullSyncInProgress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-146">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="85d52-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85d52-148">Obtiene el valor que indica si se ha establecido la marca **\_ \_ \_ \_ de NBR de sincronización completa \_ en \_ curso en** la propiedad **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="85d52-148">Gets the value that indicates whether the **DS\_REPL\_NBR\_FULL\_SYNC\_IN\_PROGRESS** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="85d52-149">**FullSyncNextPacket**</span><span class="sxs-lookup"><span data-stu-id="85d52-149">**FullSyncNextPacket**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-150">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="85d52-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85d52-152">Obtiene el valor que indica si se ha establecido en la propiedad **ReplicaFlags** la marca de **\_ \_ \_ \_ \_ \_ paquete de sincronización completa de NBR de replicación de DS** .</span><span class="sxs-lookup"><span data-stu-id="85d52-152">Gets the value that indicates whether the **DS\_REPL\_NBR\_FULL\_SYNC\_NEXT\_PACKET** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="85d52-153">**IgnoreChangeNotifications**</span><span class="sxs-lookup"><span data-stu-id="85d52-153">**IgnoreChangeNotifications**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-154">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="85d52-154">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85d52-156">Obtiene el valor que indica si se ha establecido en la propiedad **ReplicaFlags** el marcador **\_ REPL de \_ NBR \_ omitir \_ \_ notificaciones de cambios** .</span><span class="sxs-lookup"><span data-stu-id="85d52-156">Gets the value that indicates whether the **DS\_REPL\_NBR\_IGNORE\_CHANGE\_NOTIFICATIONS** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="85d52-157">**IsDeletedSourceDsa**</span><span class="sxs-lookup"><span data-stu-id="85d52-157">**IsDeletedSourceDsa**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-158">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="85d52-158">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85d52-160">Obtiene el valor que indica si esta conexión representa un controlador de dominio de origen que se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="85d52-160">Gets the value that indicates whether this connection represents a source DC that has been deleted.</span></span> <span data-ttu-id="85d52-161">**True** si esta conexión representa un controlador de dominio de origen que se ha eliminado; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="85d52-161">**TRUE** if this connection represents a source DC that has been deleted; otherwise, **FALSE**.</span></span> <span data-ttu-id="85d52-162">Por diseño, el DS seguirá replicando estas conexiones durante algún tiempo durante algún tiempo después de que se elimine el controlador de dominio de origen.</span><span class="sxs-lookup"><span data-stu-id="85d52-162">By design, the DS will continue to replicate these connections for some time for some time after the source DC is deleted.</span></span>

</dd> <dt>

<span data-ttu-id="85d52-163">**LastSyncResult**</span><span class="sxs-lookup"><span data-stu-id="85d52-163">**LastSyncResult**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-164">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85d52-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85d52-166">Obtiene el código de error **HRESULT** para el último intento de replicación.</span><span class="sxs-lookup"><span data-stu-id="85d52-166">Gets the **HRESULT** error code for the last replication attempt.</span></span>

</dd> <dt>

<span data-ttu-id="85d52-167">**ModifiedNumConsecutiveSyncFailures**</span><span class="sxs-lookup"><span data-stu-id="85d52-167">**ModifiedNumConsecutiveSyncFailures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-168">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85d52-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85d52-170">Obtiene el número de intentos de replicación erróneos consecutivos, sin incluir las conexiones que se espera que generen un error.</span><span class="sxs-lookup"><span data-stu-id="85d52-170">Gets the number of consecutive failed replication attempts, not including the connections that are expected to fail.</span></span> <span data-ttu-id="85d52-171">Por ejemplo, si la propiedad **IsDeletedSourceDsa** está establecida en **true**, se espera que se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="85d52-171">For example, if the **IsDeletedSourceDsa** property is set to **TRUE**, it is expected to fail.</span></span>

</dd> <dt>

<span data-ttu-id="85d52-172">**NamingContextDN**</span><span class="sxs-lookup"><span data-stu-id="85d52-172">**NamingContextDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-173">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85d52-173">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85d52-175">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="85d52-175">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="85d52-176">Obtiene la ruta de acceso X. 500 para el NC que replica esta conexión.</span><span class="sxs-lookup"><span data-stu-id="85d52-176">Gets the X.500 path for the NC that is replicated by this connection.</span></span>

</dd> <dt>

<span data-ttu-id="85d52-177">**NamingContextObjGuid**</span><span class="sxs-lookup"><span data-stu-id="85d52-177">**NamingContextObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-178">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85d52-178">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85d52-180">Obtiene el GUID para el NC replicado.</span><span class="sxs-lookup"><span data-stu-id="85d52-180">Gets the GUID for the replicated NC.</span></span>

</dd> <dt>

<span data-ttu-id="85d52-181">**NeverSynced**</span><span class="sxs-lookup"><span data-stu-id="85d52-181">**NeverSynced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-182">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="85d52-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85d52-184">Obtiene el valor que indica si se ha establecido la marca de **NBR de replicación de DS no \_ \_ \_ \_ sincronizado nunca** en la propiedad **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="85d52-184">Gets the value that indicates whether the **DS\_REPL\_NBR\_NEVER\_SYNCED** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="85d52-185">**NoChangeNotifications**</span><span class="sxs-lookup"><span data-stu-id="85d52-185">**NoChangeNotifications**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-186">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="85d52-186">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85d52-188">Obtiene el valor que indica si se ha establecido la marca de **NBR de replicación de DS \_ \_ \_ no hay \_ \_ notificaciones de cambios** en la propiedad **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="85d52-188">Gets the value that indicates whether the **DS\_REPL\_NBR\_NO\_CHANGE\_NOTIFICATIONS** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="85d52-189">**NumConsecutiveSyncFailures**</span><span class="sxs-lookup"><span data-stu-id="85d52-189">**NumConsecutiveSyncFailures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-190">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85d52-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85d52-192">Obtiene el número de intentos de replicación erróneos consecutivos.</span><span class="sxs-lookup"><span data-stu-id="85d52-192">Gets the number of consecutive failed replication attempts.</span></span>

</dd> <dt>

<span data-ttu-id="85d52-193">**ReplicaFlags**</span><span class="sxs-lookup"><span data-stu-id="85d52-193">**ReplicaFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-194">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85d52-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85d52-196">Obtiene el conjunto de marcadores que especifican los atributos y las opciones para los datos de replicación.</span><span class="sxs-lookup"><span data-stu-id="85d52-196">Gets the set of flags that specify attributes and options for the replication data.</span></span> <span data-ttu-id="85d52-197">Esta propiedad puede ser cero o una combinación de uno o varios de los siguientes marcadores.</span><span class="sxs-lookup"><span data-stu-id="85d52-197">This property can be zero or a combination of one or more of the following flags.</span></span>

<dt>

<span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>

<span data-ttu-id="85d52-198"><span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>**DS \_ REPL \_ NBR \_ grabable** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="85d52-198"><span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>**DS\_REPL\_NBR\_WRITEABLE** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="85d52-199">La copia local del contexto de nomenclatura es de escritura.</span><span class="sxs-lookup"><span data-stu-id="85d52-199">The local copy of the naming context is writable.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>

<span data-ttu-id="85d52-200"><span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>**DS \_ REPL \_ NBR \_ Sync \_ ON \_ Startup** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="85d52-200"><span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>**DS\_REPL\_NBR\_SYNC\_ON\_STARTUP** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="85d52-201">La replicación de este contexto de nomenclatura desde este origen se intenta cuando se arranca el servidor de destino.</span><span class="sxs-lookup"><span data-stu-id="85d52-201">Replication of this naming context from this source is attempted when the destination server is booted.</span></span> <span data-ttu-id="85d52-202">Esta marca normalmente solo se aplica a vecinos dentro del sitio.</span><span class="sxs-lookup"><span data-stu-id="85d52-202">This flag usually only applies to intra-site neighbors.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>

<span data-ttu-id="85d52-203"><span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>**DS \_ NBR de REPL \_ \_ realiza \_ \_ sincronizaciones programadas** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="85d52-203"><span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>**DS\_REPL\_NBR\_DO\_SCHEDULED\_SYNCS** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="85d52-204">La replicación se realiza según una programación.</span><span class="sxs-lookup"><span data-stu-id="85d52-204">Perform replication on a schedule.</span></span> <span data-ttu-id="85d52-205">Normalmente, esta marca se establece a menos que la programación para este contexto de nomenclatura o origen sea "Never", es decir, la programación vacía.</span><span class="sxs-lookup"><span data-stu-id="85d52-205">This flag is usually set unless the schedule for this naming context or source is "never", that is, the empty schedule.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>

<span data-ttu-id="85d52-206"><span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>**DS \_ REPL \_ NBR \_ usar \_ el \_ \_ transporte asincrónico entre sitios** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="85d52-206"><span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>**DS\_REPL\_NBR\_USE\_ASYNC\_INTERSITE\_TRANSPORT** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="85d52-207">La replicación se realiza indirectamente a través del servicio de mensajería entre sitios.</span><span class="sxs-lookup"><span data-stu-id="85d52-207">Perform replication indirectly through the Inter-Site Messaging Service.</span></span> <span data-ttu-id="85d52-208">Este marcador sólo se establece en la replicación a través de SMTP.</span><span class="sxs-lookup"><span data-stu-id="85d52-208">This flag is set only when replicating over SMTP.</span></span> <span data-ttu-id="85d52-209">Esta marca no se establece en la réplica a través de RPC/IP entre sitios.</span><span class="sxs-lookup"><span data-stu-id="85d52-209">This flag is not set when replicating over inter-site RPC/IP.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>

<span data-ttu-id="85d52-210"><span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>**DS \_ \_ \_ \_ \_ Sincronización de NBR bidireccional de REPL** (512 (0x200))</span><span class="sxs-lookup"><span data-stu-id="85d52-210"><span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>**DS\_REPL\_NBR\_TWO\_WAY\_SYNC** (512 (0x200))</span></span>


</dt> <dd>

<span data-ttu-id="85d52-211">Si se establece, indica que cuando se completa la replicación de entrada, el servidor de destino debe indicar al servidor de origen que se sincronice en la dirección inversa.</span><span class="sxs-lookup"><span data-stu-id="85d52-211">If set, indicates that when inbound replication is complete, the destination server must tell the source server to synchronize in the reverse direction.</span></span> <span data-ttu-id="85d52-212">Esta característica se utiliza en escenarios de acceso telefónico en los que sólo uno de los dos servidores puede iniciar una conexión de acceso telefónico.</span><span class="sxs-lookup"><span data-stu-id="85d52-212">This feature is used in dial-up scenarios where only one of the two servers can initiate a dial-up connection.</span></span> <span data-ttu-id="85d52-213">Por ejemplo, esta opción se puede usar en una oficina central y en una sucursal, donde la sucursal se conecta a la oficina central corporativa a través de Internet por medio de una conexión de ISP de acceso telefónico.</span><span class="sxs-lookup"><span data-stu-id="85d52-213">For example, this option could be used in a corporate headquarters and branch office, where the branch office connects to the corporate headquarters over the Internet by means of a dial-up ISP connection.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>

<span data-ttu-id="85d52-214"><span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>**DS \_ REPL \_ NBR \_ devuelven \_ objetos \_ primarios** (2048 (0x800))</span><span class="sxs-lookup"><span data-stu-id="85d52-214"><span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>**DS\_REPL\_NBR\_RETURN\_OBJECT\_PARENTS** (2048 (0x800))</span></span>


</dt> <dd>

<span data-ttu-id="85d52-215">Este vecino está devolviendo los objetos primarios antes que los objetos secundarios.</span><span class="sxs-lookup"><span data-stu-id="85d52-215">This neighbor is in a state where it returns parent objects before children objects.</span></span> <span data-ttu-id="85d52-216">Ha entrado en este estado después de recibir un objeto secundario antes que el elemento primario correspondiente.</span><span class="sxs-lookup"><span data-stu-id="85d52-216">It goes into this state after it receives a child object before its parent.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>

<span data-ttu-id="85d52-217"><span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>**DS \_ \_ \_ Sincronización completa de REPL NBR \_ \_ en \_ curso** (65536 (0x10000))</span><span class="sxs-lookup"><span data-stu-id="85d52-217"><span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>**DS\_REPL\_NBR\_FULL\_SYNC\_IN\_PROGRESS** (65536 (0x10000))</span></span>


</dt> <dd>

<span data-ttu-id="85d52-218">El servidor de destino está realizando una sincronización completa desde el servidor de origen.</span><span class="sxs-lookup"><span data-stu-id="85d52-218">The destination server is performing a full synchronization from the source server.</span></span> <span data-ttu-id="85d52-219">Las sincronizaciones completas no usan vectores que crean actualizaciones (por ejemplo [**, \_ \_ cursores de replicación de DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)) para filtrar las actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="85d52-219">Full synchronizations do not use vectors that create updates (such as [**DS\_REPL\_CURSORS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)) for filtering updates.</span></span> <span data-ttu-id="85d52-220">Las sincronizaciones completas no se usan como parte del Protocolo de replicación predeterminado.</span><span class="sxs-lookup"><span data-stu-id="85d52-220">Full synchronizations are not used as a part of the default replication protocol.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>

<span data-ttu-id="85d52-221"><span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>**DS \_ \_ \_ \_ \_ Siguiente \_ paquete de sincronización completa de REPL NBR** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="85d52-221"><span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>**DS\_REPL\_NBR\_FULL\_SYNC\_NEXT\_PACKET** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="85d52-222">El último paquete del origen indicó una modificación de un objeto que el servidor de destino aún no ha creado.</span><span class="sxs-lookup"><span data-stu-id="85d52-222">The last packet from the source indicated a modification of an object that the destination server has not yet created.</span></span> <span data-ttu-id="85d52-223">El siguiente paquete que se va a solicitar indica al servidor de origen que ponga todos los atributos del objeto modificado en el paquete.</span><span class="sxs-lookup"><span data-stu-id="85d52-223">The next packet to be requested instructs the source server to put all attributes of the modified object into the packet.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>

<span data-ttu-id="85d52-224"><span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>**DS \_ REPL \_ NBR \_ nunca se \_ sincronizó** (2097152 (0x200000))</span><span class="sxs-lookup"><span data-stu-id="85d52-224"><span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>**DS\_REPL\_NBR\_NEVER\_SYNCED** (2097152 (0x200000))</span></span>


</dt> <dd>

<span data-ttu-id="85d52-225">Nunca se ha realizado una sincronización correcta desde este origen.</span><span class="sxs-lookup"><span data-stu-id="85d52-225">A synchronization has never been successfully completed from this source.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>

<span data-ttu-id="85d52-226"><span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>**DS \_ REPL \_ NBR \_ adelantado** (16777216 (0x1000000))</span><span class="sxs-lookup"><span data-stu-id="85d52-226"><span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>**DS\_REPL\_NBR\_PREEMPTED** (16777216 (0x1000000))</span></span>


</dt> <dd>

<span data-ttu-id="85d52-227">El motor de replicación ha detenido temporalmente el procesamiento de este vecino para poder atender a otro vecino de prioridad más alta, ya sea para esta partición o para otra partición.</span><span class="sxs-lookup"><span data-stu-id="85d52-227">The replication engine has temporarily stopped processing this neighbor in order to service another higher-priority neighbor, either for this partition or for another partition.</span></span> <span data-ttu-id="85d52-228">El motor de replicación reanudará el procesamiento de este vecino cuando finalice el trabajo de prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="85d52-228">The replication engine will resume processing this neighbor after the higher-priority work is completed.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>

<span data-ttu-id="85d52-229"><span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>**DS \_ REPL \_ NBR \_ omitir \_ \_ notificaciones de cambios** (67108864 (0x4000000))</span><span class="sxs-lookup"><span data-stu-id="85d52-229"><span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>**DS\_REPL\_NBR\_IGNORE\_CHANGE\_NOTIFICATIONS** (67108864 (0x4000000))</span></span>


</dt> <dd>

<span data-ttu-id="85d52-230">Este vecino está configurado para deshabilitar las sincronizaciones basadas en notificaciones.</span><span class="sxs-lookup"><span data-stu-id="85d52-230">This neighbor is set to disable notification-based synchronizations.</span></span> <span data-ttu-id="85d52-231">Dentro de un sitio, los controladores de dominio se sincronizan entre sí basándose en las notificaciones de cambios.</span><span class="sxs-lookup"><span data-stu-id="85d52-231">Within a site, domain controllers synchronize with each other based on notifications when changes occur.</span></span> <span data-ttu-id="85d52-232">Esta configuración impide que este vecino realice sincronizaciones que se desencadenan mediante notificaciones.</span><span class="sxs-lookup"><span data-stu-id="85d52-232">This setting prevents this neighbor from performing synchronizations that are triggered by notifications.</span></span> <span data-ttu-id="85d52-233">El vecino seguirá realizando sincronizaciones en función de su programación o en respuesta a las sincronizaciones solicitadas manualmente.</span><span class="sxs-lookup"><span data-stu-id="85d52-233">The neighbor will still do synchronizations based on its schedule, or in response to manually requested synchronizations.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>

<span data-ttu-id="85d52-234"><span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>**DS \_ REPL \_ NBR \_ deshabilitar la \_ \_ sincronización programada** (134217728 (0x8000000))</span><span class="sxs-lookup"><span data-stu-id="85d52-234"><span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>**DS\_REPL\_NBR\_DISABLE\_SCHEDULED\_SYNC** (134217728 (0x8000000))</span></span>


</dt> <dd>

<span data-ttu-id="85d52-235">Este vecino está configurado para no realizar sincronizaciones en función de su programación.</span><span class="sxs-lookup"><span data-stu-id="85d52-235">This neighbor is set to not perform synchronizations based on its schedule.</span></span> <span data-ttu-id="85d52-236">La única manera en que este vecino realiza sincronizaciones es responder a las notificaciones de cambio o a las sincronizaciones solicitadas manualmente.</span><span class="sxs-lookup"><span data-stu-id="85d52-236">The only way this neighbor will perform synchronizations is in response to change notifications or to manually requested synchronizations.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>

<span data-ttu-id="85d52-237"><span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>**DS \_ NBR de REPL- \_ \_ comprimir \_ cambios** (268435456 (0x10000000))</span><span class="sxs-lookup"><span data-stu-id="85d52-237"><span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>**DS\_REPL\_NBR\_COMPRESS\_CHANGES** (268435456 (0x10000000))</span></span>


</dt> <dd>

<span data-ttu-id="85d52-238">Los cambios recibidos de este origen se comprimirán.</span><span class="sxs-lookup"><span data-stu-id="85d52-238">Changes received from this source are to be compressed.</span></span> <span data-ttu-id="85d52-239">Normalmente, la compresión solo se produce si el servidor de origen está en un sitio diferente.</span><span class="sxs-lookup"><span data-stu-id="85d52-239">Compression usually occurs only if the source server is in a different site.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>

<span data-ttu-id="85d52-240"><span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>**DS \_ REPL \_ NBR \_ no \_ \_ notificaciones de cambios** (536870912 (0x20000000))</span><span class="sxs-lookup"><span data-stu-id="85d52-240"><span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>**DS\_REPL\_NBR\_NO\_CHANGE\_NOTIFICATIONS** (536870912 (0x20000000))</span></span>


</dt> <dd>

<span data-ttu-id="85d52-241">No deberían recibirse notificaciones de cambios desde este origen.</span><span class="sxs-lookup"><span data-stu-id="85d52-241">No change notifications should be received from this source.</span></span> <span data-ttu-id="85d52-242">Normalmente solo se establece si el servidor de origen está en un sitio diferente.</span><span class="sxs-lookup"><span data-stu-id="85d52-242">Usually set only if the source server is in a different site.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>

<span data-ttu-id="85d52-243"><span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>**DS \_ \_Conjunto de \_ \_ atributos parciales \_ de REPL NBR** (1073741824 (0x40000000))</span><span class="sxs-lookup"><span data-stu-id="85d52-243"><span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>**DS\_REPL\_NBR\_PARTIAL\_ATTRIBUTE\_SET** (1073741824 (0x40000000))</span></span>


</dt> <dd>

<span data-ttu-id="85d52-244">Este vecino está recompilando el contenido de esta réplica debido a un cambio en el conjunto de atributos parciales.</span><span class="sxs-lookup"><span data-stu-id="85d52-244">This neighbor is in a state where it is rebuilding the contents of this replica because of a change in the partial attribute set.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="85d52-245">**SourceDsaAddress**</span><span class="sxs-lookup"><span data-stu-id="85d52-245">**SourceDsaAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-246">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85d52-246">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-247">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85d52-248">Obtiene la dirección DNS del controlador de dominio de origen.</span><span class="sxs-lookup"><span data-stu-id="85d52-248">Gets the DNS address of the source DC.</span></span>

> [!Note]  
> <span data-ttu-id="85d52-249">Esta cadena contiene un GUID modificado, no el nombre DNS canónico que se usa habitualmente.</span><span class="sxs-lookup"><span data-stu-id="85d52-249">This string contains a modified GUID, not the commonly used canonical DNS name.</span></span>

 

</dd> <dt>

<span data-ttu-id="85d52-250">**SourceDsaCN**</span><span class="sxs-lookup"><span data-stu-id="85d52-250">**SourceDsaCN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-251">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85d52-251">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-252">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85d52-253">Obtiene el componente de ruta de acceso del objeto DSA que representa el controlador de dominio de origen.</span><span class="sxs-lookup"><span data-stu-id="85d52-253">Gets the object path component for the DSA that represents the source DC.</span></span> <span data-ttu-id="85d52-254">Esta cadena suele ser similar al nombre del equipo, pero no siempre es idéntica.</span><span class="sxs-lookup"><span data-stu-id="85d52-254">This string is often similar to the computer name but is not always identical.</span></span>

</dd> <dt>

<span data-ttu-id="85d52-255">**SourceDsaDN**</span><span class="sxs-lookup"><span data-stu-id="85d52-255">**SourceDsaDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-256">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85d52-256">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-257">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85d52-258">Obtiene la ruta de acceso X. 500 del DSA que representa el controlador de dominio de origen.</span><span class="sxs-lookup"><span data-stu-id="85d52-258">Gets the X.500 path for the DSA that represents the source DC.</span></span>

</dd> <dt>

<span data-ttu-id="85d52-259">**SourceDsaInvocationID**</span><span class="sxs-lookup"><span data-stu-id="85d52-259">**SourceDsaInvocationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-260">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85d52-260">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-261">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85d52-262">Obtiene el identificador de invocación utilizado por el servidor de origen a partir de la última replicación.</span><span class="sxs-lookup"><span data-stu-id="85d52-262">Gets the invocation ID that was used by the source server as of the last replication.</span></span>

</dd> <dt>

<span data-ttu-id="85d52-263">**SourceDsaObjGuid**</span><span class="sxs-lookup"><span data-stu-id="85d52-263">**SourceDsaObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-264">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85d52-264">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-265">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85d52-266">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="85d52-266">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="85d52-267">Obtiene el GUID para el agente de servicios de directorio (DSA) que representa el controlador de dominio de origen (DC).</span><span class="sxs-lookup"><span data-stu-id="85d52-267">Gets the GUID for the directory service agent (DSA) that represents the source domain controller (DC).</span></span>

</dd> <dt>

<span data-ttu-id="85d52-268">**SourceDsaSite**</span><span class="sxs-lookup"><span data-stu-id="85d52-268">**SourceDsaSite**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-269">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85d52-269">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-270">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85d52-271">Obtiene el sitio que contiene el controlador de dominio de origen.</span><span class="sxs-lookup"><span data-stu-id="85d52-271">Gets the site that contains the source DC.</span></span>

</dd> <dt>

<span data-ttu-id="85d52-272">**SyncOnStartup**</span><span class="sxs-lookup"><span data-stu-id="85d52-272">**SyncOnStartup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-273">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="85d52-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-274">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85d52-275">Obtiene el valor que indica si se ha establecido en la propiedad **ReplicaFlags** la propiedad **\_ \_ NBR \_ de REPL de la sincronización en el indicador \_ de \_ Inicio** .</span><span class="sxs-lookup"><span data-stu-id="85d52-275">Gets the value that indicates whether the **DS\_REPL\_NBR\_SYNC\_ON\_STARTUP** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="85d52-276">**TimeOfLastSyncAttempt**</span><span class="sxs-lookup"><span data-stu-id="85d52-276">**TimeOfLastSyncAttempt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-277">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="85d52-277">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-278">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85d52-279">Obtiene la marca de tiempo del último intento de replicación.</span><span class="sxs-lookup"><span data-stu-id="85d52-279">Gets the timestamp for the last replication attempt.</span></span>

</dd> <dt>

<span data-ttu-id="85d52-280">**TimeOfLastSyncSuccess**</span><span class="sxs-lookup"><span data-stu-id="85d52-280">**TimeOfLastSyncSuccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-281">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="85d52-281">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-282">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85d52-283">Obtiene la marca de tiempo del último intento de replicación correcto.</span><span class="sxs-lookup"><span data-stu-id="85d52-283">Gets the timestamp for the last successful replication attempt.</span></span>

</dd> <dt>

<span data-ttu-id="85d52-284">**TwoWaySync**</span><span class="sxs-lookup"><span data-stu-id="85d52-284">**TwoWaySync**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-285">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="85d52-285">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-286">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85d52-287">Obtiene el valor que indica si se ha establecido la marca de **\_ sincronización DS REPL \_ NBR \_ \_ Biway \_** en la propiedad **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="85d52-287">Gets the value that indicates whether the **DS\_REPL\_NBR\_TWO\_WAY\_SYNC** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="85d52-288">**UseAsyncIntersiteTransport**</span><span class="sxs-lookup"><span data-stu-id="85d52-288">**UseAsyncIntersiteTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-289">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="85d52-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-290">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85d52-291">Obtiene el valor que indica si se ha establecido en la propiedad **ReplicaFlags** el marcador REPL de NBR de uso de la marca de **\_ \_ \_ \_ \_ \_ transporte entre sitios asincrónica** .</span><span class="sxs-lookup"><span data-stu-id="85d52-291">Gets the value that indicates whether the **DS\_REPL\_NBR\_USE\_ASYNC\_INTERSITE\_TRANSPORT** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="85d52-292">**USNAttributeFilter**</span><span class="sxs-lookup"><span data-stu-id="85d52-292">**USNAttributeFilter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-293">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="85d52-293">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-294">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85d52-295">Obtiene el valor de la propiedad **USNLastObjChangeSynced** al final del último ciclo de replicación completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="85d52-295">Gets the **USNLastObjChangeSynced** property value at the end of the last successful completed replication cycle.</span></span> <span data-ttu-id="85d52-296">Cero si no se ha completado correctamente ningún ciclo de replicación.</span><span class="sxs-lookup"><span data-stu-id="85d52-296">Zero if there were no successfully completed replication cycles.</span></span>

</dd> <dt>

<span data-ttu-id="85d52-297">**USNLastObjChangeSynced**</span><span class="sxs-lookup"><span data-stu-id="85d52-297">**USNLastObjChangeSynced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-298">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="85d52-298">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-299">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85d52-300">Obtiene el valor de atributo [**sin modificar**](/windows/desktop/ADSchema/a-usnchanged) de la última actualización de objeto que se recibió.</span><span class="sxs-lookup"><span data-stu-id="85d52-300">Gets the [**unchanged**](/windows/desktop/ADSchema/a-usnchanged) attribute value of the last object update that was received.</span></span>

</dd> <dt>

<span data-ttu-id="85d52-301">**Writeable (Grabable)**</span><span class="sxs-lookup"><span data-stu-id="85d52-301">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d52-302">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="85d52-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="85d52-303">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85d52-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85d52-304">Obtiene el valor que indica si se ha establecido la marca de escritura de NBR de replicación de DS en la propiedad **ReplicaFlags** . **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="85d52-304">Gets the value that indicates whether the **DS\_REPL\_NBR\_WRITEABLE** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="85d52-305">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85d52-305">Requirements</span></span>



| <span data-ttu-id="85d52-306">Requisito</span><span class="sxs-lookup"><span data-stu-id="85d52-306">Requirement</span></span> | <span data-ttu-id="85d52-307">Value</span><span class="sxs-lookup"><span data-stu-id="85d52-307">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="85d52-308">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85d52-308">Minimum supported client</span></span><br/> | <span data-ttu-id="85d52-309">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="85d52-309">None supported</span></span><br/>                                                               |
| <span data-ttu-id="85d52-310">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85d52-310">Minimum supported server</span></span><br/> | <span data-ttu-id="85d52-311">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85d52-311">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="85d52-312">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="85d52-312">Namespace</span></span><br/>                | <span data-ttu-id="85d52-313">\\MicrosoftActiveDirectory raíz</span><span class="sxs-lookup"><span data-stu-id="85d52-313">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="85d52-314">MOF</span><span class="sxs-lookup"><span data-stu-id="85d52-314">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85d52-315"><dt>ReplProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="85d52-315"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="85d52-316">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="85d52-316">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85d52-317"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85d52-317"><dt>Replprov.dll</dt></span></span> </dl> |



 

