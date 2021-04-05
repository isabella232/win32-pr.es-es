---
title: MicrosoftDNS_Zone (clase)
description: La \_ clase de zona MicrosoftDNS describe una zona DNS. Cada instancia de la \_ clase de zona MicrosoftDNS debe asignarse exactamente a un servidor DNS. Las zonas pueden estar asociadas a varias instancias de \_ las clases de dominio microsoftdns o microsoftdns \_ ResourceRecord.
ms.assetid: 9c59fa61-cca5-4718-ad40-8d2c6ed5fc2d
keywords:
- DNS de la clase MicrosoftDNS_Zone
- MicrosoftDNS_Zone de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone
- MicrosoftDNS_Zone.PauseZone
- MicrosoftDNS_Zone.ResumeZone
- MicrosoftDNS_Zone.ReloadZone
- MicrosoftDNS_Zone.ForceRefresh
- MicrosoftDNS_Zone.UpdateFromDS
- MicrosoftDNS_Zone.WriteBackZone
- MicrosoftDNS_Zone.AgeAllRecords
- MicrosoftDNS_Zone.CreateZone
- MicrosoftDNS_Zone.ChangeZoneType
- MicrosoftDNS_Zone.ResetSecondaries
- MicrosoftDNS_Zone.GetDistinguishedName
- MicrosoftDNS_Zone.ZoneType
- MicrosoftDNS_Zone.DsIntegrated
- MicrosoftDNS_Zone.AllowUpdate
- MicrosoftDNS_Zone.DataFile
- MicrosoftDNS_Zone.DisableWINSRecordReplication
- MicrosoftDNS_Zone.Notify
- MicrosoftDNS_Zone.SecureSecondaries
- MicrosoftDNS_Zone.Paused
- MicrosoftDNS_Zone.Shutdown
- MicrosoftDNS_Zone.Reverse
- MicrosoftDNS_Zone.AutoCreated
- MicrosoftDNS_Zone.UseWins
- MicrosoftDNS_Zone.UseNBStat
- MicrosoftDNS_Zone.Aging
- MicrosoftDNS_Zone.RefreshInterval
- MicrosoftDNS_Zone.NoRefreshInterval
- MicrosoftDNS_Zone.AvailForScavengeTime
- MicrosoftDNS_Zone.MasterServers
- MicrosoftDNS_Zone.LocalMasterServers
- MicrosoftDNS_Zone.ScavengeServers
- MicrosoftDNS_Zone.SecondaryServers
- MicrosoftDNS_Zone.NotifyServers
- MicrosoftDNS_Zone.ForwarderTimeout
- MicrosoftDNS_Zone.ForwarderSlave
- MicrosoftDNS_Zone.LastSuccessfulSoaCheck
- MicrosoftDNS_Zone.LastSuccessfulXfr
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b15119c7a5cdc1dba2998e17b5c69a4d0e15c6ca
ms.sourcegitcommit: 03fb201e1ea36e353c335ff063ed993fb5993e61
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104079870"
---
# <a name="microsoftdns_zone-class"></a><span data-ttu-id="9c6f9-107">MicrosoftDNS ( \_ clase de zona)</span><span class="sxs-lookup"><span data-stu-id="9c6f9-107">MicrosoftDNS\_Zone class</span></span>

> [!NOTE]
> <span data-ttu-id="9c6f9-108">Este artículo contiene referencias al término esclavo, un término que Microsoft ya no usa.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-108">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="9c6f9-109">Cuando se quite el término del software, se quitará también del artículo.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-109">When the term is removed from the software, we’ll remove it from this article.</span></span>

> [!NOTE]
> <span data-ttu-id="9c6f9-110">Este artículo contiene referencias al término servidor maestro, un término que Microsoft ya no usa.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-110">This article contains references to the term master server, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="9c6f9-111">Cuando se quite el término del software, se quitará también del artículo.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-111">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="9c6f9-112">La clase de **\_ zona MicrosoftDNS** describe una zona DNS.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-112">The **MicrosoftDNS\_Zone** class describes a DNS Zone.</span></span> <span data-ttu-id="9c6f9-113">Cada instancia de la clase de **\_ zona MicrosoftDNS** debe asignarse exactamente a un servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-113">Every instance of the **MicrosoftDNS\_Zone** class must be assigned to exactly one DNS Server.</span></span> <span data-ttu-id="9c6f9-114">Las zonas pueden estar asociadas a varias instancias de las clases de [**\_ dominio Microsoftdns**](microsoftdns-domain.md) o [**microsoftdns \_ ResourceRecord**](microsoftdns-resourcerecord.md) .</span><span class="sxs-lookup"><span data-stu-id="9c6f9-114">Zones may be associated with multiple instances of [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) or [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) classes.</span></span>

<span data-ttu-id="9c6f9-115">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-115">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c6f9-116">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c6f9-116">Syntax</span></span>

``` syntax
class MicrosoftDNS_Zone : MicrosoftDNS_Domain
{
  uint32  ZoneType;
  boolean DsIntegrated;
  uint32  AllowUpdate;
  string  DataFile;
  boolean DisableWINSRecordReplication;
  uint32  Notify;
  uint32  SecureSecondaries;
  boolean Paused;
  boolean Shutdown;
  boolean Reverse;
  boolean AutoCreated;
  boolean UseWins;
  boolean UseNBStat;
  boolean Aging;
  uint32  RefreshInterval;
  uint32  NoRefreshInterval;
  uint32  AvailForScavengeTime;
  string  MasterServers[];
  string  LocalMasterServers[];
  string  ScavengeServers[];
  string  SecondaryServers[];
  string  NotifyServers[];
  uint32  ForwarderTimeout;
  boolean ForwarderSlave;
  uint32  LastSuccessfulSoaCheck;
  uint32  LastSuccessfulXfr;
};
```

## <a name="members"></a><span data-ttu-id="9c6f9-117">Miembros</span><span class="sxs-lookup"><span data-stu-id="9c6f9-117">Members</span></span>

<span data-ttu-id="9c6f9-118">La clase de **\_ zona MicrosoftDNS** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9c6f9-118">The **MicrosoftDNS\_Zone** class has these types of members:</span></span>

-   [<span data-ttu-id="9c6f9-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="9c6f9-119">Methods</span></span>](#methods)
-   [<span data-ttu-id="9c6f9-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9c6f9-120">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9c6f9-121">Métodos</span><span class="sxs-lookup"><span data-stu-id="9c6f9-121">Methods</span></span>

<span data-ttu-id="9c6f9-122">La clase de **\_ zona MicrosoftDNS** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-122">The **MicrosoftDNS\_Zone** class has these methods.</span></span>



| <span data-ttu-id="9c6f9-123">Método</span><span class="sxs-lookup"><span data-stu-id="9c6f9-123">Method</span></span>                   | <span data-ttu-id="9c6f9-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c6f9-124">Description</span></span>                                                                                                                                                                                                |
|:-------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c6f9-125">**AgeAllRecords**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-125">**AgeAllRecords**</span></span>        | <span data-ttu-id="9c6f9-126">Habilita la detección de registros de algunos o de todos los registros que no son de y no SOA.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-126">Enables aging for some or all non-NS and non-SOA records.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="9c6f9-127">**ChangeZoneType**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-127">**ChangeZoneType**</span></span>       | <span data-ttu-id="9c6f9-128">Cambia los tipos de zona.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-128">Changes zone types.</span></span> <br/> <span data-ttu-id="9c6f9-129">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="9c6f9-129">Qualifiers: Implemented</span></span><br/>                                                                                                                                         |
| <span data-ttu-id="9c6f9-130">**CreateZone**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-130">**CreateZone**</span></span>           | <span data-ttu-id="9c6f9-131">Crea una nueva zona.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-131">Creates a new zone.</span></span> <br/> <span data-ttu-id="9c6f9-132">Calificadores: ninguno.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-132">Qualifiers: None.</span></span><br/>                                                                                                                                               |
| <span data-ttu-id="9c6f9-133">**ForceRefresh**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-133">**ForceRefresh**</span></span>         | <span data-ttu-id="9c6f9-134">Fuerza una actualización de la secundaria desde el servidor DNS maestro.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-134">Forces an update of the secondary from the Master DNS Server.</span></span> <br/> <span data-ttu-id="9c6f9-135">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="9c6f9-135">Qualifiers: Implemented</span></span><br/>                                                                                               |
| <span data-ttu-id="9c6f9-136">**GetDistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-136">**GetDistinguishedName**</span></span> | <span data-ttu-id="9c6f9-137">Obtiene el nombre distintivo de DS para la zona.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-137">Obtains DS distinguished Name for the zone.</span></span> <br/> <span data-ttu-id="9c6f9-138">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="9c6f9-138">Qualifiers: Implemented</span></span><br/>                                                                                                                 |
| <span data-ttu-id="9c6f9-139">**PauseZone**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-139">**PauseZone**</span></span>            | <span data-ttu-id="9c6f9-140">Pausa la zona.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-140">Pauses the Zone.</span></span> <br/> <span data-ttu-id="9c6f9-141">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="9c6f9-141">Qualifiers: Implemented</span></span><br/>                                                                                                                                            |
| <span data-ttu-id="9c6f9-142">**ReloadZone**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-142">**ReloadZone**</span></span>           | <span data-ttu-id="9c6f9-143">Vuelve a cargar la zona.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-143">Reloads the Zone.</span></span> <br/> <span data-ttu-id="9c6f9-144">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="9c6f9-144">Qualifiers: Implemented</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="9c6f9-145">**ResetSecondaries**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-145">**ResetSecondaries**</span></span>     | <span data-ttu-id="9c6f9-146">Restablece la matriz de direcciones IP secundarias.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-146">Resets the secondary ip address array.</span></span> <br/> <span data-ttu-id="9c6f9-147">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="9c6f9-147">Qualifiers: Implemented</span></span><br/>                                                                                                                      |
| <span data-ttu-id="9c6f9-148">**ResumeZone**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-148">**ResumeZone**</span></span>           | <span data-ttu-id="9c6f9-149">Reanuda la zona.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-149">Resumes the Zone.</span></span> <br/> <span data-ttu-id="9c6f9-150">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="9c6f9-150">Qualifiers: Implemented</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="9c6f9-151">**UpdateFromDS**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-151">**UpdateFromDS**</span></span>         | <span data-ttu-id="9c6f9-152">Fuerza una actualización de la zona desde el servicio de directorio (DS).</span><span class="sxs-lookup"><span data-stu-id="9c6f9-152">Forces an update of the Zone from the Directory Service (DS).</span></span> <span data-ttu-id="9c6f9-153">Para que este método sea válido, ZoneType debe ser 0 la zona debe estar almacenada en el DS.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-153">For this method to be valid, the ZoneType must be 0 the Zone must indeed be stored in the DS.</span></span> <br/> <span data-ttu-id="9c6f9-154">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="9c6f9-154">Qualifiers: Implemented</span></span><br/> |
| <span data-ttu-id="9c6f9-155">**WriteBackZone**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-155">**WriteBackZone**</span></span>        | <span data-ttu-id="9c6f9-156">Guarda los datos de la zona en su archivo de zona.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-156">Saves Zone data to its zone file.</span></span> <br/> <span data-ttu-id="9c6f9-157">Calificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="9c6f9-157">Qualifiers: Implemented, static</span></span><br/>                                                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="9c6f9-158">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9c6f9-158">Properties</span></span>

<span data-ttu-id="9c6f9-159">La clase de **\_ zona MicrosoftDNS** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-159">The **MicrosoftDNS\_Zone** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9c6f9-160">**Edad**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-160">**Aging**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f9-161">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-161">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9c6f9-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c6f9-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c6f9-163">Especifica el comportamiento de detección y eliminación de registros obsoletos de la zona.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-163">Specifies the aging and scavenging behavior of the zone.</span></span> <span data-ttu-id="9c6f9-164">Cero indica que la eliminación de registros obsoletos está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-164">Zero indicates scavenging is disabled.</span></span> <span data-ttu-id="9c6f9-165">Cuando se deshabilita la eliminación de registros obsoletos, no se actualizan las marcas de tiempo de los registros de la zona y los registros no se someten a la eliminación de registros obsoletos.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-165">When scavenging is disabled, the timestamps of records in the zone are not refreshed, and the records are not subjected to scavenging.</span></span> <span data-ttu-id="9c6f9-166">Cuando se establece en uno, los registros están sujetos a limpieza y sus marcas de tiempo se actualizan cuando el servidor recibe la solicitud de actualización dinámica de los registros.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-166">When set to one, records are subjected to scavenging and their timestamps are refreshed when the server receives the dynamic update request for the records.</span></span> <span data-ttu-id="9c6f9-167">En el caso de las zonas integradas en Active Directory, este valor se establece en la propiedad *DefaultAgingState* del servidor DNS donde se crea la zona.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-167">For Active Directory-integrated zones, this value is set to the *DefaultAgingState* property of the DNS Server where the zone is created.</span></span> <span data-ttu-id="9c6f9-168">En el caso de las zonas principales estándar, el valor predeterminado es cero.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-168">For standard primary zones, the default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="9c6f9-169">**Recibe**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-169">**AllowUpdate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f9-170">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c6f9-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c6f9-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c6f9-172">Indica si la zona acepta solicitudes de actualización dinámica.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-172">Indicates whether the Zone accepts dynamic update requests.</span></span>

</dd> <dt>

<span data-ttu-id="9c6f9-173">**Creado automáticamente**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-173">**AutoCreated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f9-174">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9c6f9-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c6f9-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c6f9-176">Indica si la zona se ha creado de forma autocreada.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-176">Indicates whether the Zone is autocreated.</span></span>

</dd> <dt>

<span data-ttu-id="9c6f9-177">**AvailForScavengeTime**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-177">**AvailForScavengeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f9-178">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c6f9-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c6f9-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c6f9-180">Especifica la hora a la que el servidor puede intentar la eliminación de registros obsoletos de la zona.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-180">Specifies the time when the server may attempt scavenging the zone.</span></span> <span data-ttu-id="9c6f9-181">Incluso si la zona está configurada para habilitar la eliminación de registros obsoletos, el servidor DNS no intentará limpiar esta zona hasta después de este momento.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-181">Even if the zone is configured to enable scavenging the DNS server will not attempt scavenging this zone until after this moment.</span></span> <span data-ttu-id="9c6f9-182">Este valor se establece en la hora actual más el intervalo de actualización de la zona cada vez que se carga la zona.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-182">This value is set to the current time plus the Refresh Interval of the zone whenever the zone is loaded.</span></span> <span data-ttu-id="9c6f9-183">Este parámetro se almacena localmente y no se replica en otras copias de la zona.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-183">This parameter is stored locally, and is not replicated to other copies of the zone.</span></span>

</dd> <dt>

<span data-ttu-id="9c6f9-184">**DataFile**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-184">**DataFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f9-185">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c6f9-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c6f9-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c6f9-187">Indica el nombre del archivo de zona.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-187">Indicates the name of the zone file.</span></span>

</dd> <dt>

<span data-ttu-id="9c6f9-188">**DisableWINSRecordReplication**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-188">**DisableWINSRecordReplication**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f9-189">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-189">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9c6f9-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c6f9-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c6f9-191">Indica si se replica el registro WINS.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-191">Indicates whether the WINS record is replicated.</span></span> <span data-ttu-id="9c6f9-192">Si se establece en TRUE, la replicación de registros WINS está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-192">If set to TRUE, WINS record replication is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="9c6f9-193">**DsIntegrated**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-193">**DsIntegrated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f9-194">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-194">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9c6f9-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c6f9-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c6f9-196">Especifica si la zona está integrada en DS.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-196">Specifies whether the zone is DS integrated.</span></span>

</dd> <dt>

<span data-ttu-id="9c6f9-197">**ForwarderSlave**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-197">**ForwarderSlave**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f9-198">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9c6f9-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c6f9-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c6f9-200">Indica si el DNS usa la recursividad cuando se resuelven los nombres de la zona de reenvío especificada.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-200">Indicates whether the DNS uses recursion when resolving the names for the specified forward zone.</span></span> <span data-ttu-id="9c6f9-201">Aplicable solo a zonas de reenvío condicional.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-201">Applicable to Conditional Forwarding zones only.</span></span>

</dd> <dt>

<span data-ttu-id="9c6f9-202">**ForwarderTimeout**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-202">**ForwarderTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f9-203">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c6f9-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c6f9-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c6f9-205">Indica el tiempo, en segundos, que un servidor DNS que reenvía una consulta para el nombre en la zona de avance espera la resolución del reenviador antes de intentar resolver la propia consulta.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-205">Indicates the time, in seconds, a DNS server forwarding a query for the name under the forward zone waits for resolution from the forwarder before attempting to resolve the query itself.</span></span> <span data-ttu-id="9c6f9-206">Este parámetro solo es aplicable a las zonas de reenvío.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-206">This parameter is applicable to the Forward zones only.</span></span>

</dd> <dt>

<span data-ttu-id="9c6f9-207">**LastSuccessfulSoaCheck**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-207">**LastSuccessfulSoaCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f9-208">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c6f9-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c6f9-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c6f9-210">Número de segundos desde el comienzo del 1 de enero de 1970 GMT, desde que se comprobó por última vez el número de serie de SOA de la zona.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-210">Number of seconds since the beginning of January 1, 1970 GMT, since the SOA serial number for the zone was last checked.</span></span>

</dd> <dt>

<span data-ttu-id="9c6f9-211">**LastSuccessfulXfr**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-211">**LastSuccessfulXfr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f9-212">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-212">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c6f9-213">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c6f9-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c6f9-214">Número de segundos desde el comienzo del 1 de enero de 1970 GMT, ya que la zona se transfirió por última vez desde un servidor maestro.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-214">Number of seconds since the beginning of January 1, 1970 GMT, since the zone was last transferred from a master server.</span></span>

</dd> <dt>

<span data-ttu-id="9c6f9-215">**LocalMasterServers**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-215">**LocalMasterServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f9-216">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-216">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9c6f9-217">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c6f9-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c6f9-218">Direcciones IP locales de los servidores DNS maestros para esta zona.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-218">Local IP addresses of the master DNS servers for this zone.</span></span> <span data-ttu-id="9c6f9-219">Si se establece, estos maestros sobrepasan los MasterServers encontrados en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-219">If set, these masters over-ride the MasterServers found in Active Directory.</span></span>

</dd> <dt>

<span data-ttu-id="9c6f9-220">**MasterServers**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-220">**MasterServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f9-221">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-221">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9c6f9-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c6f9-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c6f9-223">Direcciones IP de los servidores DNS maestros para esta zona.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-223">IP addresses of the master DNS servers for this zone.</span></span>

</dd> <dt>

<span data-ttu-id="9c6f9-224">**NoRefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-224">**NoRefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f9-225">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c6f9-226">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c6f9-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c6f9-227">Especifica el intervalo de tiempo entre la última actualización de la marca de tiempo de un registro y el momento más antiguo en el que se puede actualizar la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-227">Specifies the time interval between the last update of a record's timestamp and the earliest moment when the timestamp can be refreshed.</span></span>

</dd> <dt>

<span data-ttu-id="9c6f9-228">**Notificar**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-228">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f9-229">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-229">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c6f9-230">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c6f9-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c6f9-231">Indica si la zona maestra notifica los cambios en la base de datos de RRs a las secundarias.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-231">Indicates whether the master Zone notifies secondaries of any changes in its RRs database.</span></span> <span data-ttu-id="9c6f9-232">Establézcalo en 1 para notificar a las secundarias.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-232">Set to 1 to notify secondaries.</span></span>

</dd> <dt>

<span data-ttu-id="9c6f9-233">**NotifyServers**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-233">**NotifyServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f9-234">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-234">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9c6f9-235">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c6f9-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c6f9-236">Matriz de cadenas que enumeran las direcciones IP de los servidores DNS a los que se notificarán los cambios en esta zona.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-236">Array of strings enumerating IP addresses of DNS servers to be notified of changes in this zone.</span></span>

</dd> <dt>

<span data-ttu-id="9c6f9-237">**En pausa**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-237">**Paused**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f9-238">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-238">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9c6f9-239">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c6f9-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c6f9-240">Indica si la zona está en pausa.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-240">Indicates whether the Zone is paused.</span></span>

</dd> <dt>

<span data-ttu-id="9c6f9-241">**RefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-241">**RefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f9-242">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-242">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c6f9-243">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c6f9-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c6f9-244">Especifica el intervalo de actualización, durante el cual se espera que los registros con una marca de tiempo que no sea cero se actualicen para permanecer en la zona.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-244">Specifies the refresh interval, during which the records with nonzero timestamp are expected to be refreshed to remain in the zone.</span></span> <span data-ttu-id="9c6f9-245">Los registros que no se han actualizado mediante la expiración del intervalo de actualización podrían quitarse mediante la siguiente eliminación de registros obsoletos realizada por un servidor.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-245">Records that have not been refreshed by expiration of the Refresh interval could be removed by the next scavenging performed by a server.</span></span> <span data-ttu-id="9c6f9-246">Este valor nunca debe ser menor que el período de actualización más largo de los registros registrados en la zona.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-246">This value should never be less than the longest refresh period of the records registered in the zone.</span></span> <span data-ttu-id="9c6f9-247">Los valores demasiado pequeños pueden dar lugar a la eliminación de registros DNS válidos.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-247">Values that are too small may lead to removal of valid DNS records.</span></span> <span data-ttu-id="9c6f9-248">los valores demasiado grandes prolongan la duración de los registros obsoletos.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-248">values that are too large prolong the lifetime of stale records.</span></span> <span data-ttu-id="9c6f9-249">Este valor se establece en la propiedad *defaultrefreshinterval,* del servidor DNS donde se crea la zona.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-249">This value is set to the *DefaultRefreshInterval* property of the DNS server where the zone is created.</span></span>

</dd> <dt>

<span data-ttu-id="9c6f9-250">**Viceversa**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-250">**Reverse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f9-251">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9c6f9-252">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c6f9-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c6f9-253">Indica si la zona es inversa (TRUE) o adelantada (FALSE).</span><span class="sxs-lookup"><span data-stu-id="9c6f9-253">Indicates whether the Zone is reverse (TRUE) or forward (FALSE).</span></span>

</dd> <dt>

<span data-ttu-id="9c6f9-254">**ScavengeServers**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-254">**ScavengeServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f9-255">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-255">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9c6f9-256">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c6f9-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c6f9-257">Matriz de cadenas que enumera la lista de direcciones IP de los servidores DNS que pueden realizar la eliminación de registros obsoletos de esta zona.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-257">Array of strings that enumerates the list of IP addresses of DNS servers that are allowed to perform scavenging of stale records of this zone.</span></span> <span data-ttu-id="9c6f9-258">Si no se especifica la lista, se permite a cualquier servidor DNS principal autorizado para la zona borrar la zona cuando se cumplen otros requisitos previos.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-258">If the list is not specified, any primary DNS server authoritative for the zone is allowed to scavenge the zone when other prerequisites are met.</span></span>

</dd> <dt>

<span data-ttu-id="9c6f9-259">**SecondaryServers**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-259">**SecondaryServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f9-260">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-260">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9c6f9-261">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c6f9-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c6f9-262">Matriz de cadenas que enumeran las direcciones IP de los servidores DNS que permiten recibir esta zona a través de la replicación de zona.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-262">Array of strings enumerating IP addresses of DNS servers allowed to receive this zone through zone replication.</span></span>

</dd> <dt>

<span data-ttu-id="9c6f9-263">**SecureSecondaries**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-263">**SecureSecondaries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f9-264">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c6f9-265">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c6f9-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c6f9-266">Indica si se permite la transferencia de zona solo a las secundarias designadas.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-266">Indicates whether zone transfer is allowed to designated secondaries only.</span></span> <span data-ttu-id="9c6f9-267">Las secundarias designadas son servidores DNS cuyas direcciones IP se enumeran en SecondariesIPAddressesArray.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-267">Designated secondaries are DNS Servers whose IP addresses are listed in SecondariesIPAddressesArray.</span></span>

</dd> <dt>

<span data-ttu-id="9c6f9-268">**Apagar**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-268">**Shutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f9-269">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-269">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9c6f9-270">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c6f9-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c6f9-271">Indica si la copia de la zona ha expirado.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-271">Indicates whether the copy of the Zone is expired.</span></span> <span data-ttu-id="9c6f9-272">Si es TRUE, la zona ha expirado o se ha cerrado.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-272">If TRUE, the Zone is expired, or shut down.</span></span>

</dd> <dt>

<span data-ttu-id="9c6f9-273">**UseNBStat**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-273">**UseNBStat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f9-274">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9c6f9-275">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c6f9-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c6f9-276">Este valor booleano indica si la zona utiliza la búsqueda inversa de NBStat.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-276">This Boolean indicates whether the Zone uses NBStat reverse lookup.</span></span>

</dd> <dt>

<span data-ttu-id="9c6f9-277">**UseWins**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-277">**UseWins**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f9-278">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-278">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9c6f9-279">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c6f9-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c6f9-280">Indica si la zona utiliza la búsqueda de WINS.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-280">Indicates whether the Zone uses WINS look up.</span></span>

</dd> <dt>

<span data-ttu-id="9c6f9-281">**ZoneType**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-281">**ZoneType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f9-282">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-282">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c6f9-283">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c6f9-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c6f9-284">Indica el tipo de la zona.</span><span class="sxs-lookup"><span data-stu-id="9c6f9-284">Indicates the type of the Zone.</span></span> <span data-ttu-id="9c6f9-285">Los valores válidos son:</span><span class="sxs-lookup"><span data-stu-id="9c6f9-285">Valid values are:</span></span>

-   <span data-ttu-id="9c6f9-286">DS integrado</span><span class="sxs-lookup"><span data-stu-id="9c6f9-286">DS integrated</span></span>
-   <span data-ttu-id="9c6f9-287">Principal</span><span class="sxs-lookup"><span data-stu-id="9c6f9-287">Primary</span></span>
-   <span data-ttu-id="9c6f9-288">Secundario</span><span class="sxs-lookup"><span data-stu-id="9c6f9-288">Secondary</span></span>

<span data-ttu-id="9c6f9-289">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="9c6f9-289">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="9c6f9-290">Valores adicionales:</span><span class="sxs-lookup"><span data-stu-id="9c6f9-290">Additional values:</span></span>

-   <span data-ttu-id="9c6f9-291">Cache</span><span class="sxs-lookup"><span data-stu-id="9c6f9-291">Cache</span></span>
-   <span data-ttu-id="9c6f9-292">Agrupa</span><span class="sxs-lookup"><span data-stu-id="9c6f9-292">Stub</span></span>
-   <span data-ttu-id="9c6f9-293">Reenviador</span><span class="sxs-lookup"><span data-stu-id="9c6f9-293">Forwarder</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9c6f9-294">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c6f9-294">Requirements</span></span>



| <span data-ttu-id="9c6f9-295">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c6f9-295">Requirement</span></span> | <span data-ttu-id="9c6f9-296">Value</span><span class="sxs-lookup"><span data-stu-id="9c6f9-296">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c6f9-297">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c6f9-297">Minimum supported client</span></span><br/> | <span data-ttu-id="9c6f9-298">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9c6f9-298">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9c6f9-299">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c6f9-299">Minimum supported server</span></span><br/> | <span data-ttu-id="9c6f9-300">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9c6f9-300">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9c6f9-301">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9c6f9-301">Namespace</span></span><br/>                | <span data-ttu-id="9c6f9-302">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="9c6f9-302">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="9c6f9-303">MOF</span><span class="sxs-lookup"><span data-stu-id="9c6f9-303">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c6f9-304"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9c6f9-304"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c6f9-305">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c6f9-305">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c6f9-306">**\_Dominio MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-306">**MicrosoftDNS\_Domain**</span></span>](microsoftdns-domain.md)
</dt> <dt>

[<span data-ttu-id="9c6f9-307">**Método AgeAllRecords de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-307">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="9c6f9-308">**Método ChangeZoneType de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-308">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="9c6f9-309">**Método CreateZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-309">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="9c6f9-310">**Método ForceRefresh de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-310">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="9c6f9-311">**Método GetDistinguishedName de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-311">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="9c6f9-312">**Método PauseZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-312">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="9c6f9-313">**Método ReloadZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-313">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="9c6f9-314">**Método ResetSecondaries de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-314">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="9c6f9-315">**Método ResumeZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-315">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="9c6f9-316">**Método UpdateFromDS de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-316">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="9c6f9-317">**Método WriteBackZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="9c6f9-317">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





