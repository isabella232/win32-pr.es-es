---
title: MicrosoftDNS_Server (clase)
description: La \_ clase de servidor MicrosoftDNS describe un servidor DNS. Cada instancia de esta clase puede estar asociada a una instancia de la \_ caché de microsoftdns, una instancia de microsoftdns \_ RootHints y varias instancias de la \_ zona microsoftdns.
ms.assetid: 768f5f96-d7a5-472f-afe6-63aa9c0e5258
keywords:
- DNS de la clase MicrosoftDNS_Server
- MicrosoftDNS_Server de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server
- MicrosoftDNS_Server.StartService
- MicrosoftDNS_Server.StopService
- MicrosoftDNS_Server.StartScavenging
- MicrosoftDNS_Server.GetDistinguishedName
- MicrosoftDNS_Server.Name
- MicrosoftDNS_Server.Version
- MicrosoftDNS_Server.LogLevel
- MicrosoftDNS_Server.LogFilePath
- MicrosoftDNS_Server.LogFileMaxSize
- MicrosoftDNS_Server.LogIPFilterList
- MicrosoftDNS_Server.EventLogLevel
- MicrosoftDNS_Server.RpcProtocol
- MicrosoftDNS_Server.NameCheckFlag
- MicrosoftDNS_Server.AddressAnswerLimit
- MicrosoftDNS_Server.RecursionRetry
- MicrosoftDNS_Server.RecursionTimeout
- MicrosoftDNS_Server.DsPollingInterval
- MicrosoftDNS_Server.DsTombstoneInterval
- MicrosoftDNS_Server.MaxCacheTTL
- MicrosoftDNS_Server.MaxNegativeCacheTTL
- MicrosoftDNS_Server.SendPort
- MicrosoftDNS_Server.XfrConnectTimeout
- MicrosoftDNS_Server.BootMethod
- MicrosoftDNS_Server.AllowUpdate
- MicrosoftDNS_Server.UpdateOptions
- MicrosoftDNS_Server.DsAvailable
- MicrosoftDNS_Server.DisableAutoReverseZones
- MicrosoftDNS_Server.AutoCacheUpdate
- MicrosoftDNS_Server.NoRecursion
- MicrosoftDNS_Server.RoundRobin
- MicrosoftDNS_Server.LocalNetPriority
- MicrosoftDNS_Server.StrictFileParsing
- MicrosoftDNS_Server.LooseWildcarding
- MicrosoftDNS_Server.BindSecondaries
- MicrosoftDNS_Server.WriteAuthorityNS
- MicrosoftDNS_Server.ForwardDelegations
- MicrosoftDNS_Server.SecureResponses
- MicrosoftDNS_Server.DisjointNets
- MicrosoftDNS_Server.AutoConfigFileZones
- MicrosoftDNS_Server.ScavengingInterval
- MicrosoftDNS_Server.DefaultRefreshInterval
- MicrosoftDNS_Server.DefaultNoRefreshInterval
- MicrosoftDNS_Server.DefaultAgingState
- MicrosoftDNS_Server.EDnsCacheTimeout
- MicrosoftDNS_Server.EnableEDnsProbes
- MicrosoftDNS_Server.EnableDnsSec
- MicrosoftDNS_Server.ServerAddresses
- MicrosoftDNS_Server.ListenAddresses
- MicrosoftDNS_Server.Forwarders
- MicrosoftDNS_Server.ForwardingTimeout
- MicrosoftDNS_Server.IsSlave
- MicrosoftDNS_Server.EnableDirectoryPartitions
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 854a90f5b0fa4d331bd0478d104e50dd70b0cd65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996001"
---
# <a name="microsoftdns_server-class"></a><span data-ttu-id="2c956-106">MicrosoftDNS ( \_ clase de servidor)</span><span class="sxs-lookup"><span data-stu-id="2c956-106">MicrosoftDNS\_Server class</span></span>

<span data-ttu-id="2c956-107">La clase de **\_ servidor MicrosoftDNS** describe un servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="2c956-107">The **MicrosoftDNS\_Server** class describes a DNS Server.</span></span> <span data-ttu-id="2c956-108">Cada instancia de esta clase puede estar asociada a una instancia de [**la \_ caché de microsoftdns**](microsoftdns-cache.md), una instancia de [**microsoftdns \_ RootHints**](microsoftdns-roothints.md)y varias instancias de la [**\_ zona microsoftdns**](microsoftdns-zone.md).</span><span class="sxs-lookup"><span data-stu-id="2c956-108">Every instance of this class may be associated with one instance of [**MicrosoftDNS\_Cache**](microsoftdns-cache.md), one instance of [**MicrosoftDNS\_RootHints**](microsoftdns-roothints.md), and multiple instances of [**MicrosoftDNS\_Zone**](microsoftdns-zone.md).</span></span>

<span data-ttu-id="2c956-109">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="2c956-109">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c956-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c956-110">Syntax</span></span>

``` syntax
class MicrosoftDNS_Server : CIM_Service
{
  string  Name;
  uint32  Version;
  uint32  LogLevel;
  string  LogFilePath;
  uint32  LogFileMaxSize;
  string  LogIPFilterList[];
  uint32  EventLogLevel;
  sint32  RpcProtocol;
  uint32  NameCheckFlag;
  uint32  AddressAnswerLimit;
  uint32  RecursionRetry;
  uint32  RecursionTimeout;
  uint32  DsPollingInterval;
  uint32  DsTombstoneInterval;
  uint32  MaxCacheTTL;
  uint32  MaxNegativeCacheTTL;
  uint32  SendPort;
  uint32  XfrConnectTimeout;
  uint32  BootMethod;
  uint32  AllowUpdate;
  uint32  UpdateOptions;
  boolean DsAvailable;
  boolean DisableAutoReverseZones;
  boolean AutoCacheUpdate;
  boolean NoRecursion;
  boolean RoundRobin;
  boolean LocalNetPriority;
  boolean StrictFileParsing;
  boolean LooseWildcarding;
  boolean BindSecondaries;
  boolean WriteAuthorityNS;
  uint32  ForwardDelegations;
  boolean SecureResponses;
  boolean DisjointNets;
  uint32  AutoConfigFileZones;
  uint32  ScavengingInterval;
  uint32  DefaultRefreshInterval;
  uint32  DefaultNoRefreshInterval;
  boolean DefaultAgingState;
  uint32  EDnsCacheTimeout;
  boolean EnableEDnsProbes;
  uint32  EnableDnsSec;
  string  ServerAddresses[];
  string  ListenAddresses[];
  string  Forwarders[];
  uint32  ForwardingTimeout;
  boolean IsSlave;
  boolean EnableDirectoryPartitions;
};
```

## <a name="members"></a><span data-ttu-id="2c956-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="2c956-111">Members</span></span>

<span data-ttu-id="2c956-112">La clase de **\_ servidor MicrosoftDNS** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2c956-112">The **MicrosoftDNS\_Server** class has these types of members:</span></span>

-   [<span data-ttu-id="2c956-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="2c956-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="2c956-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2c956-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2c956-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="2c956-115">Methods</span></span>

<span data-ttu-id="2c956-116">La clase de **\_ servidor MicrosoftDNS** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2c956-116">The **MicrosoftDNS\_Server** class has these methods.</span></span>



| <span data-ttu-id="2c956-117">Método</span><span class="sxs-lookup"><span data-stu-id="2c956-117">Method</span></span>                   | <span data-ttu-id="2c956-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c956-118">Description</span></span>                                                                      |
|:-------------------------|:---------------------------------------------------------------------------------|
| <span data-ttu-id="2c956-119">**GetDistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="2c956-119">**GetDistinguishedName**</span></span> | <span data-ttu-id="2c956-120">Recupera el nombre distintivo DNS de la zona.</span><span class="sxs-lookup"><span data-stu-id="2c956-120">Retrieves DNS distinguished name for the zone.</span></span><br/>                        |
| <span data-ttu-id="2c956-121">**StartScavenging**</span><span class="sxs-lookup"><span data-stu-id="2c956-121">**StartScavenging**</span></span>      | <span data-ttu-id="2c956-122">Inicia la eliminación de registros obsoletos en las zonas sometidas a limpieza.</span><span class="sxs-lookup"><span data-stu-id="2c956-122">Starts scavenging stale records in the zones subjected to scavenging.</span></span><br/> |
| <span data-ttu-id="2c956-123">**StartService**</span><span class="sxs-lookup"><span data-stu-id="2c956-123">**StartService**</span></span>         | <span data-ttu-id="2c956-124">Inicia el servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="2c956-124">Starts the DNS Server.</span></span><br/>                                                |
| <span data-ttu-id="2c956-125">**StopService**</span><span class="sxs-lookup"><span data-stu-id="2c956-125">**StopService**</span></span>          | <span data-ttu-id="2c956-126">Detiene el servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="2c956-126">Stops the DNS Server.</span></span><br/>                                                 |



 

### <a name="properties"></a><span data-ttu-id="2c956-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2c956-127">Properties</span></span>

<span data-ttu-id="2c956-128">La clase de **\_ servidor MicrosoftDNS** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2c956-128">The **MicrosoftDNS\_Server** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2c956-129">**AddressAnswerLimit**</span><span class="sxs-lookup"><span data-stu-id="2c956-129">**AddressAnswerLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-130">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c956-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-131">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-132">Número máximo de registros de host devueltos en respuesta a una solicitud de dirección.</span><span class="sxs-lookup"><span data-stu-id="2c956-132">Maximum number of host records returned in response to an address request.</span></span> <span data-ttu-id="2c956-133">Los valores entre 5 y 28 son válidos.</span><span class="sxs-lookup"><span data-stu-id="2c956-133">Values between 5 and 28 are valid.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-134">**Recibe**</span><span class="sxs-lookup"><span data-stu-id="2c956-134">**AllowUpdate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-135">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c956-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-137">Especifica si el servidor DNS acepta solicitudes de actualización dinámica.</span><span class="sxs-lookup"><span data-stu-id="2c956-137">Specifies whether the DNS Server accepts dynamic update requests.</span></span> <span data-ttu-id="2c956-138">Los valores válidos son los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2c956-138">Valid values are as shown in the following table.</span></span>



| <span data-ttu-id="2c956-139">Value</span><span class="sxs-lookup"><span data-stu-id="2c956-139">Value</span></span>                                                                                                | <span data-ttu-id="2c956-140">Significado</span><span class="sxs-lookup"><span data-stu-id="2c956-140">Meaning</span></span>                                                                                               |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="2c956-141"><dt>**0,1**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-141"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="2c956-142">Sin restricciones.</span><span class="sxs-lookup"><span data-stu-id="2c956-142">No Restrictions.</span></span><br/>                                                                           |
| <span id="1"></span><dl> <span data-ttu-id="2c956-143"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-143"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="2c956-144">No permite actualizaciones dinámicas de registros SOA.</span><span class="sxs-lookup"><span data-stu-id="2c956-144">Does not allow dynamic updates of SOA records.</span></span><br/>                                             |
| <span id="2"></span><dl> <span data-ttu-id="2c956-145"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-145"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="2c956-146">No permite actualizaciones dinámicas de registros NS en la raíz de la zona.</span><span class="sxs-lookup"><span data-stu-id="2c956-146">Does not allow dynamic updates of NS records at the zone root.</span></span><br/>                             |
| <span id="4"></span><dl> <span data-ttu-id="2c956-147"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-147"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="2c956-148">No permite actualizaciones dinámicas de registros NS que no estén en la raíz de la zona (registros NS de delegación).</span><span class="sxs-lookup"><span data-stu-id="2c956-148">Does not allow dynamic updates of NS records not at the zone root (delegation NS records).</span></span><br/> |



 

<span data-ttu-id="2c956-149">Sume estos valores para determinar el valor de configuración.</span><span class="sxs-lookup"><span data-stu-id="2c956-149">Sum these values to determine the setting value.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-150">**AutoCacheUpdate**</span><span class="sxs-lookup"><span data-stu-id="2c956-150">**AutoCacheUpdate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-151">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2c956-151">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-152">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-153">Indica si el servidor DNS intenta actualizar sus entradas de caché con los datos de los servidores raíz.</span><span class="sxs-lookup"><span data-stu-id="2c956-153">Indicates whether the DNS Server attempts to update its cache entries using data from root servers.</span></span> <span data-ttu-id="2c956-154">Cuando se inicia un servidor DNS, necesita una lista de "sugerencias" de servidor raíz NS y registros A para los servidores que históricamente se denominaba archivo caché.</span><span class="sxs-lookup"><span data-stu-id="2c956-154">When a DNS Server boots, it needs a list of root server 'hints' NS and A records for the servers historically called the cache file.</span></span> <span data-ttu-id="2c956-155">Los servidores DNS de Microsoft tienen una característica que les permite intentar volver a escribir un nuevo archivo caché en función de las respuestas de los servidores raíz.</span><span class="sxs-lookup"><span data-stu-id="2c956-155">Microsoft DNS Servers have a feature that enables them to attempt to write back a new cache file based on the responses from root servers.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-156">**AutoConfigFileZones**</span><span class="sxs-lookup"><span data-stu-id="2c956-156">**AutoConfigFileZones**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-157">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c956-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-158">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-159">Indica qué zonas principales estándar que son autoritativas para el nombre del servidor DNS deben actualizarse cuando cambia el servidor de nombres.</span><span class="sxs-lookup"><span data-stu-id="2c956-159">Indicates which standard primary zones that are authoritative for the name of the DNS Server must be updated when the name server changes.</span></span> <span data-ttu-id="2c956-160">Los valores válidos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="2c956-160">Valid values are as follows:</span></span>



| <span data-ttu-id="2c956-161">Value</span><span class="sxs-lookup"><span data-stu-id="2c956-161">Value</span></span>                                                                                                | <span data-ttu-id="2c956-162">Significado</span><span class="sxs-lookup"><span data-stu-id="2c956-162">Meaning</span></span>                                                    |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="2c956-163"><dt>**0,1**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-163"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="2c956-164">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2c956-164">None.</span></span><br/>                                           |
| <span id="1"></span><dl> <span data-ttu-id="2c956-165"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-165"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="2c956-166">Solo los servidores que permiten actualizaciones dinámicas.</span><span class="sxs-lookup"><span data-stu-id="2c956-166">Only servers that allow dynamic updates.</span></span><br/>        |
| <span id="2"></span><dl> <span data-ttu-id="2c956-167"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-167"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="2c956-168">Solo los servidores que no permiten actualizaciones dinámicas.</span><span class="sxs-lookup"><span data-stu-id="2c956-168">Only servers that do not allow dynamic updates.</span></span><br/> |
| <span id="4"></span><dl> <span data-ttu-id="2c956-169"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-169"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="2c956-170">Todos los servidores.</span><span class="sxs-lookup"><span data-stu-id="2c956-170">All servers.</span></span><br/>                                    |



 

<span data-ttu-id="2c956-171">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="2c956-171">The default value is 1.</span></span>

<span data-ttu-id="2c956-172">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="2c956-172">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="2c956-173">El número 3 representa todos los servidores.</span><span class="sxs-lookup"><span data-stu-id="2c956-173">The number 3 represents All servers.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-174">**BindSecondaries**</span><span class="sxs-lookup"><span data-stu-id="2c956-174">**BindSecondaries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-175">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2c956-175">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-176">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-176">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-177">Determina el formato del mensaje AXFR cuando se envía a los secundarios del servidor DNS que no son de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2c956-177">Determines the AXFR message format when sending to non-Microsoft DNS Server secondaries.</span></span> <span data-ttu-id="2c956-178">Cuando se establece en TRUE, el servidor DNS envía las transferencias a las secundarias del servidor DNS que no son de Microsoft en el formato sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="2c956-178">When set to TRUE, the DNS Server sends transfers to non-Microsoft DNS Server secondaries in the uncompressed format.</span></span> <span data-ttu-id="2c956-179">Cuando es FALSE, todas las transferencias se envían en el formato rápido.</span><span class="sxs-lookup"><span data-stu-id="2c956-179">When FALSE, all transfers are sent in the fast format.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-180">**BootMethod**</span><span class="sxs-lookup"><span data-stu-id="2c956-180">**BootMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-181">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c956-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-182">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-182">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-183">Método de inicialización del servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="2c956-183">Initialization method for the DNS Server.</span></span> <span data-ttu-id="2c956-184">En la siguiente tabla se muestran los valores válidos.</span><span class="sxs-lookup"><span data-stu-id="2c956-184">Valid values are shown in the following table.</span></span>



| <span data-ttu-id="2c956-185">Value</span><span class="sxs-lookup"><span data-stu-id="2c956-185">Value</span></span>                                                                                                | <span data-ttu-id="2c956-186">Significado</span><span class="sxs-lookup"><span data-stu-id="2c956-186">Meaning</span></span>                                      |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="2c956-187"><dt>**0,1**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-187"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="2c956-188">Sin inicializar.</span><span class="sxs-lookup"><span data-stu-id="2c956-188">Uninitialized.</span></span><br/>                    |
| <span id="1"></span><dl> <span data-ttu-id="2c956-189"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-189"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="2c956-190">Arranque desde el archivo.</span><span class="sxs-lookup"><span data-stu-id="2c956-190">Boot from file.</span></span><br/>                   |
| <span id="2"></span><dl> <span data-ttu-id="2c956-191"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-191"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="2c956-192">Arranque desde el registro.</span><span class="sxs-lookup"><span data-stu-id="2c956-192">Boot from registry.</span></span><br/>               |
| <span id="3"></span><dl> <span data-ttu-id="2c956-193"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-193"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="2c956-194">Arranque desde el directorio y el registro.</span><span class="sxs-lookup"><span data-stu-id="2c956-194">Boot from directory and registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2c956-195">**DefaultAgingState**</span><span class="sxs-lookup"><span data-stu-id="2c956-195">**DefaultAgingState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-196">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2c956-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-197">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-197">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-198">Valor predeterminado de **ScavengingInterval** establecido para todas las zonas integradas en Active Directory creadas en este servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="2c956-198">Default **ScavengingInterval** value set for all Active Directory-integrated zones created on this DNS Server.</span></span> <span data-ttu-id="2c956-199">El valor predeterminado es cero, lo que indica que la eliminación de registros obsoletos está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="2c956-199">The default value is zero, indicating scavenging is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-200">**DefaultNoRefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="2c956-200">**DefaultNoRefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-201">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c956-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-202">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-202">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-203">Intervalo sin actualización, en horas, establecido para todas las zonas integradas en Active Directory creadas en este servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="2c956-203">No-refresh interval, in hours, set for all Active Directory-integrated zones created on this DNS Server.</span></span> <span data-ttu-id="2c956-204">El valor predeterminado es 168 horas (siete días).</span><span class="sxs-lookup"><span data-stu-id="2c956-204">The default value is 168 hours (seven days).</span></span>

</dd> <dt>

<span data-ttu-id="2c956-205">**DefaultRefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="2c956-205">**DefaultRefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-206">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c956-206">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-207">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-207">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-208">Intervalo de actualización, en horas, establecido para todas las zonas integradas en Active Directory creadas en este servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="2c956-208">Refresh interval, in hours, set for all Active Directory-integrated zones created on this DNS Server.</span></span> <span data-ttu-id="2c956-209">El valor predeterminado es 168 horas (siete días).</span><span class="sxs-lookup"><span data-stu-id="2c956-209">The default value is 168 hours (seven days).</span></span>

</dd> <dt>

<span data-ttu-id="2c956-210">**DisableAutoReverseZones**</span><span class="sxs-lookup"><span data-stu-id="2c956-210">**DisableAutoReverseZones**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-211">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2c956-211">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-212">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-212">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-213">Indica si el servidor DNS crea automáticamente zonas de búsqueda inversa estándar.</span><span class="sxs-lookup"><span data-stu-id="2c956-213">Indicates whether the DNS Server automatically creates standard reverse look up zones.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-214">**DisjointNets**</span><span class="sxs-lookup"><span data-stu-id="2c956-214">**DisjointNets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-215">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2c956-215">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-216">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-216">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-217">Indica si se puede invalidar el enlace de puerto predeterminado para un socket que se usa para enviar consultas a servidores DNS remotos.</span><span class="sxs-lookup"><span data-stu-id="2c956-217">Indicates whether the default port binding for a socket used to send queries to remote DNS Servers can be overridden.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-218">**DsAvailable**</span><span class="sxs-lookup"><span data-stu-id="2c956-218">**DsAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-219">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2c956-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-220">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-220">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-221">Indica si hay un DS disponible en el servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="2c956-221">Indicates whether there is an available DS on the DNS Server.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-222">**DsPollingInterval**</span><span class="sxs-lookup"><span data-stu-id="2c956-222">**DsPollingInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-223">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c956-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-224">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-224">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-225">Intervalo, en segundos, para sondear las zonas integradas en el DS.</span><span class="sxs-lookup"><span data-stu-id="2c956-225">Interval, in seconds, to poll the DS-integrated zones.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-226">**DsTombstoneInterval**</span><span class="sxs-lookup"><span data-stu-id="2c956-226">**DsTombstoneInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-227">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c956-227">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-228">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-228">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-229">Duración de los registros de desecho en zonas integradas en el servicio de directorio, expresado en segundos.</span><span class="sxs-lookup"><span data-stu-id="2c956-229">Lifetime of tombstoned records in Directory Service integrated zones, expressed in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-230">**EDnsCacheTimeout**</span><span class="sxs-lookup"><span data-stu-id="2c956-230">**EDnsCacheTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-231">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c956-231">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-232">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-232">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-233">Duración, en segundos, de la información almacenada en caché que describe la versión de EDNS compatible con otros servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="2c956-233">Lifetime, in seconds, of the cached information describing the EDNS version supported by other DNS Servers.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-234">**EnableDirectoryPartitions**</span><span class="sxs-lookup"><span data-stu-id="2c956-234">**EnableDirectoryPartitions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-235">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2c956-235">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-236">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-236">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-237">Especifica si la compatibilidad con las particiones de directorio de aplicaciones está habilitada en el servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="2c956-237">Specifies whether support for application directory partitions is enabled on the DNS Server.</span></span>

<span data-ttu-id="2c956-238">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="2c956-238">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="2c956-239">Este método se denomina EnableDirectoryPartitionSupport.</span><span class="sxs-lookup"><span data-stu-id="2c956-239">This method is named EnableDirectoryPartitionSupport.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-240">**EnableDnsSec**</span><span class="sxs-lookup"><span data-stu-id="2c956-240">**EnableDnsSec**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-241">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c956-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-242">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-242">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-243">Especifica si el servidor DNS incluye RR específicos de DNSSEC, KEY, SIG y NXT en una respuesta, según la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="2c956-243">Specifies whether the DNS Server includes DNSSEC-specific RRs, KEY, SIG, and NXT in a response, per the following table:</span></span>



| <span data-ttu-id="2c956-244">Value</span><span class="sxs-lookup"><span data-stu-id="2c956-244">Value</span></span>                                                                                                | <span data-ttu-id="2c956-245">Significado</span><span class="sxs-lookup"><span data-stu-id="2c956-245">Meaning</span></span>                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="2c956-246"><dt>**0,1**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-246"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="2c956-247">No se incluye ningún registro DNSSEC en la respuesta a menos que la consulta solicite un conjunto de registros de recursos del tipo de registro DNSSEC.</span><span class="sxs-lookup"><span data-stu-id="2c956-247">No DNSSEC records are included in the response unless the query requested a resource record set of the DNSSEC record type.</span></span><br/>          |
| <span id="1"></span><dl> <span data-ttu-id="2c956-248"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-248"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="2c956-249">Los registros DNSSEC se incluyen en la respuesta según RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="2c956-249">DNSSEC records are included in the response according to RFC 2535.</span></span><br/>                                                                  |
| <span id="2"></span><dl> <span data-ttu-id="2c956-250"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-250"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="2c956-251">Los registros DNSSEC se incluyen en una respuesta solo si la consulta de cliente original contenía el registro de recursos OPT según RFC 2671</span><span class="sxs-lookup"><span data-stu-id="2c956-251">DNSSEC records are included in a response only if the original client query contained the OPT resource record according to RFC 2671</span></span><br/> |



 

<span data-ttu-id="2c956-252">Si una consulta solicita un conjunto de registros de recursos del tipo DNSSEC, el servidor DNS siempre responde con dichos registros, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="2c956-252">If a query requests a resource record set of the DNSSEC type, the DNS Server always responds with such records, if available.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-253">**EnableEDnsProbes**</span><span class="sxs-lookup"><span data-stu-id="2c956-253">**EnableEDnsProbes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-254">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2c956-254">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-255">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-255">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-256">Especifica el comportamiento del servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="2c956-256">Specifies the behavior of the DNS Server.</span></span> <span data-ttu-id="2c956-257">Si es TRUE, el servidor DNS responde siempre con los registros de recursos OPT según RFC 2671, a menos que el servidor remoto haya indicado que no admite EDNS en un intercambio anterior.</span><span class="sxs-lookup"><span data-stu-id="2c956-257">When TRUE, the DNS Server always responds with OPT resource records according to RFC 2671, unless the remote server has indicated it does not support EDNS in a prior exchange.</span></span> <span data-ttu-id="2c956-258">Si es FALSE, el servidor DNS responde a las consultas con OPC solo si se envían las OPC en la consulta original.</span><span class="sxs-lookup"><span data-stu-id="2c956-258">If FALSE, the DNS Server responds to queries with OPTs only if OPTs are sent in the original query.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-259">**EventLogLevel**</span><span class="sxs-lookup"><span data-stu-id="2c956-259">**EventLogLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-260">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c956-260">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-261">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-261">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-262">Indica qué eventos registra el servidor DNS en el registro del sistema de Visor de eventos.</span><span class="sxs-lookup"><span data-stu-id="2c956-262">Indicates which events the DNS Server records in the Event Viewer system log.</span></span> <span data-ttu-id="2c956-263">Se usan los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="2c956-263">The following values are used.</span></span>



| <span data-ttu-id="2c956-264">Value</span><span class="sxs-lookup"><span data-stu-id="2c956-264">Value</span></span>                                                                                                | <span data-ttu-id="2c956-265">Significado</span><span class="sxs-lookup"><span data-stu-id="2c956-265">Meaning</span></span>                                  |
|------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="2c956-266"><dt>**0,1**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-266"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="2c956-267">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2c956-267">None.</span></span><br/>                         |
| <span id="1"></span><dl> <span data-ttu-id="2c956-268"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-268"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="2c956-269">Solo registra errores.</span><span class="sxs-lookup"><span data-stu-id="2c956-269">Log only errors.</span></span><br/>              |
| <span id="2"></span><dl> <span data-ttu-id="2c956-270"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-270"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="2c956-271">Solo registra advertencias y errores.</span><span class="sxs-lookup"><span data-stu-id="2c956-271">Log only warnings and errors.</span></span><br/> |
| <span id="4"></span><dl> <span data-ttu-id="2c956-272"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-272"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="2c956-273">Registra todos los eventos.</span><span class="sxs-lookup"><span data-stu-id="2c956-273">Log all events.</span></span><br/>               |



 

</dd> <dt>

<span data-ttu-id="2c956-274">**ForwardDelegations**</span><span class="sxs-lookup"><span data-stu-id="2c956-274">**ForwardDelegations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-275">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c956-275">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-276">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-276">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-277">Especifica si se reenvían las consultas a zonas secundarias delegadas.</span><span class="sxs-lookup"><span data-stu-id="2c956-277">Specifies whether queries to delegated sub-zones are forwarded.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-278">**Reenviadores**</span><span class="sxs-lookup"><span data-stu-id="2c956-278">**Forwarders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-279">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="2c956-279">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2c956-280">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-280">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-281">Enumera la lista de direcciones IP de los reenviadores a los que el servidor DNS reenvía las consultas.</span><span class="sxs-lookup"><span data-stu-id="2c956-281">Enumerates the list of IP addresses of Forwarders to which the DNS Server forwards queries.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-282">**ForwardingTimeout**</span><span class="sxs-lookup"><span data-stu-id="2c956-282">**ForwardingTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-283">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c956-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-284">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-284">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-285">Tiempo, en segundos, que un servidor DNS que reenvía una consulta esperará la resolución del [*reenviador*](f-gly.md) antes de intentar resolver la propia consulta.</span><span class="sxs-lookup"><span data-stu-id="2c956-285">Time, in seconds, a DNS Server forwarding a query will wait for resolution from the [*forwarder*](f-gly.md) before attempting to resolve the query itself.</span></span>

<span data-ttu-id="2c956-286">Este valor no tiene sentido si el servidor de reenvío no está configurado para usar la recursividad.</span><span class="sxs-lookup"><span data-stu-id="2c956-286">This value is meaningless if the forwarding server is not set to use recursion.</span></span> <span data-ttu-id="2c956-287">Para determinar esto, Compruebe la propiedad booleana IsSlave.</span><span class="sxs-lookup"><span data-stu-id="2c956-287">To determine this, check the IsSlave Boolean property.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-288">**IsSlave**</span><span class="sxs-lookup"><span data-stu-id="2c956-288">**IsSlave**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-289">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2c956-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-290">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-290">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-291">**True** si el servidor DNS no utiliza la recursividad cuando se produce un error en la resolución de nombres a través de reenviadores.</span><span class="sxs-lookup"><span data-stu-id="2c956-291">**TRUE** if the DNS server does not use recursion when name-resolution through forwarders fails.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-292">**ListenAddresses**</span><span class="sxs-lookup"><span data-stu-id="2c956-292">**ListenAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-293">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="2c956-293">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2c956-294">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-294">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-295">Enumera la lista de direcciones IP en las que el servidor DNS puede recibir consultas.</span><span class="sxs-lookup"><span data-stu-id="2c956-295">Enumerates the list of IP addresses on which the DNS Server can receive queries.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-296">**LocalNetPriority**</span><span class="sxs-lookup"><span data-stu-id="2c956-296">**LocalNetPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-297">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2c956-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-298">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-298">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-299">Indica si el servidor DNS da prioridad a la dirección de red local al devolver los registros.</span><span class="sxs-lookup"><span data-stu-id="2c956-299">Indicates whether the DNS Server gives priority to the local net address when returning A records.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-300">**LogFileMaxSize**</span><span class="sxs-lookup"><span data-stu-id="2c956-300">**LogFileMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-301">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c956-301">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-302">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-302">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-303">Tamaño del registro de depuración del servidor DNS, en bytes.</span><span class="sxs-lookup"><span data-stu-id="2c956-303">Size of the DNS Server debug log, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-304">**LogFilePath**</span><span class="sxs-lookup"><span data-stu-id="2c956-304">**LogFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-305">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2c956-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-306">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-306">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-307">Nombre de archivo y ruta de acceso para el registro de depuración del servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="2c956-307">File name and path for the DNS Server debug log.</span></span> <span data-ttu-id="2c956-308">El valor predeterminado es% system32% \\ DNS \\ DNS. log.</span><span class="sxs-lookup"><span data-stu-id="2c956-308">Default is %system32%\\dns\\dns.log.</span></span> <span data-ttu-id="2c956-309">Las rutas de acceso relativas son relativas a% systemroot% \\ system32.</span><span class="sxs-lookup"><span data-stu-id="2c956-309">Relative paths are relative to %Systemroot%\\System32.</span></span> <span data-ttu-id="2c956-310">Se pueden usar rutas de acceso absolutas, pero no se admiten rutas de acceso UNC.</span><span class="sxs-lookup"><span data-stu-id="2c956-310">Absolute paths may be used, but UNC paths are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-311">**LogIPFilterList**</span><span class="sxs-lookup"><span data-stu-id="2c956-311">**LogIPFilterList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-312">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="2c956-312">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2c956-313">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-313">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-314">Lista de direcciones IP utilizadas para filtrar los eventos DNS escritos en el registro de depuración.</span><span class="sxs-lookup"><span data-stu-id="2c956-314">List of IP addresses used to filter DNS events written to the debug log.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-315">**LogLevel**</span><span class="sxs-lookup"><span data-stu-id="2c956-315">**LogLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-316">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c956-316">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-317">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-317">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-318">Indica qué directivas se activan en el registro del sistema de Visor de eventos.</span><span class="sxs-lookup"><span data-stu-id="2c956-318">Indicates which policies are activated in the Event Viewer system log.</span></span>

<span data-ttu-id="2c956-319">Debe establecerse en valores específicos basados en el siguiente algoritmo: cada Directiva (que se va a activar en el registro del sistema de Visor de eventos) se asigna a un valor específico.</span><span class="sxs-lookup"><span data-stu-id="2c956-319">Should be set to specific values based on the following algorithm: Every policy (to be activated in the Event Viewer system log) is assigned a specific value.</span></span>



| <span data-ttu-id="2c956-320">Value</span><span class="sxs-lookup"><span data-stu-id="2c956-320">Value</span></span>                                                                                                                  | <span data-ttu-id="2c956-321">Significado</span><span class="sxs-lookup"><span data-stu-id="2c956-321">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="2c956-322"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-322"><dt>**1**</dt></span></span> </dl>                   | <span data-ttu-id="2c956-323">Misma.</span><span class="sxs-lookup"><span data-stu-id="2c956-323">Query.</span></span><br/>                                   |
| <span id="16"></span><dl> <span data-ttu-id="2c956-324"><dt>**16**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-324"><dt>**16**</dt></span></span> </dl>                 | <span data-ttu-id="2c956-325">Notificar a.</span><span class="sxs-lookup"><span data-stu-id="2c956-325">Notify.</span></span><br/>                                  |
| <span id="32"></span><dl> <span data-ttu-id="2c956-326"><dt>**32**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-326"><dt>**32**</dt></span></span> </dl>                 | <span data-ttu-id="2c956-327">Actualizar:</span><span class="sxs-lookup"><span data-stu-id="2c956-327">Update.</span></span><br/>                                  |
| <span id="254"></span><dl> <span data-ttu-id="2c956-328"><dt>**254**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-328"><dt>**254**</dt></span></span> </dl>               | <span data-ttu-id="2c956-329">Transacciones que no son de consulta.</span><span class="sxs-lookup"><span data-stu-id="2c956-329">Nonquery transactions.</span></span><br/>                   |
| <span id="256"></span><dl> <span data-ttu-id="2c956-330"><dt>**256**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-330"><dt>**256**</dt></span></span> </dl>               | <span data-ttu-id="2c956-331">Preguntas.</span><span class="sxs-lookup"><span data-stu-id="2c956-331">Questions.</span></span><br/>                               |
| <span id="512"></span><dl> <span data-ttu-id="2c956-332"><dt>**512**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-332"><dt>**512**</dt></span></span> </dl>               | <span data-ttu-id="2c956-333">Contesta.</span><span class="sxs-lookup"><span data-stu-id="2c956-333">Answers.</span></span><br/>                                 |
| <span id="4096"></span><dl> <span data-ttu-id="2c956-334"><dt>**4096**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-334"><dt>**4096**</dt></span></span> </dl>             | <span data-ttu-id="2c956-335">Send.</span><span class="sxs-lookup"><span data-stu-id="2c956-335">Send.</span></span><br/>                                    |
| <span id="8192"></span><dl> <span data-ttu-id="2c956-336"><dt>**8192**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-336"><dt>**8192**</dt></span></span> </dl>             | <span data-ttu-id="2c956-337">Aparecen.</span><span class="sxs-lookup"><span data-stu-id="2c956-337">Receive.</span></span><br/>                                 |
| <span id="16384"></span><dl> <span data-ttu-id="2c956-338"><dt>**16384**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-338"><dt>**16384**</dt></span></span> </dl>           | <span data-ttu-id="2c956-339">Puertos.</span><span class="sxs-lookup"><span data-stu-id="2c956-339">UDP.</span></span><br/>                                     |
| <span id="32768"></span><dl> <span data-ttu-id="2c956-340"><dt>**32768**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-340"><dt>**32768**</dt></span></span> </dl>           | <span data-ttu-id="2c956-341">TCP.</span><span class="sxs-lookup"><span data-stu-id="2c956-341">TCP.</span></span><br/>                                     |
| <span id="65535"></span><dl> <span data-ttu-id="2c956-342"><dt>**65535**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-342"><dt>**65535**</dt></span></span> </dl>           | <span data-ttu-id="2c956-343">Todos los paquetes.</span><span class="sxs-lookup"><span data-stu-id="2c956-343">All packets.</span></span><br/>                             |
| <span id="65536"></span><dl> <span data-ttu-id="2c956-344"><dt>**65536**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-344"><dt>**65536**</dt></span></span> </dl>           | <span data-ttu-id="2c956-345">Transacción de escritura del servicio de directorio NT.</span><span class="sxs-lookup"><span data-stu-id="2c956-345">NT Directory Service write transaction.</span></span><br/>  |
| <span id="131072"></span><dl> <span data-ttu-id="2c956-346"><dt>**131 072**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-346"><dt>**131072**</dt></span></span> </dl>         | <span data-ttu-id="2c956-347">Transacción de actualización del servicio de directorio NT.</span><span class="sxs-lookup"><span data-stu-id="2c956-347">NT Directory Service update transaction.</span></span><br/> |
| <span id="16777216"></span><dl> <span data-ttu-id="2c956-348"><dt>**16777216**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-348"><dt>**16777216**</dt></span></span> </dl>     | <span data-ttu-id="2c956-349">Paquetes completos.</span><span class="sxs-lookup"><span data-stu-id="2c956-349">Full packets.</span></span><br/>                            |
| <span id="2147483648"></span><dl> <span data-ttu-id="2c956-350"><dt>**2147483648**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-350"><dt>**2147483648**</dt></span></span> </dl> | <span data-ttu-id="2c956-351">Escritura a través de.</span><span class="sxs-lookup"><span data-stu-id="2c956-351">Write through.</span></span><br/>                           |



 

<span data-ttu-id="2c956-352">La suma de los valores correspondientes a todas las directivas que se van a activar se indica en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="2c956-352">The sum of the values corresponding to all the policies to be activated is indicated in this property.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-353">**LooseWildcarding**</span><span class="sxs-lookup"><span data-stu-id="2c956-353">**LooseWildcarding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-354">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2c956-354">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-355">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-355">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-356">Indica si el servidor DNS realiza caracteres comodín sueltos.</span><span class="sxs-lookup"><span data-stu-id="2c956-356">Indicates whether the DNS Server performs loose wildcarding.</span></span> <span data-ttu-id="2c956-357">Si no está definida o es cero, el servidor sigue el comportamiento de los caracteres comodín especificados en el RFC de DNS.</span><span class="sxs-lookup"><span data-stu-id="2c956-357">If undefined or zero, the server follows the wildcarding behavior specified in the DNS RFC.</span></span> <span data-ttu-id="2c956-358">En este caso, se recomienda que un administrador incluya registros MX para todos los hosts que no puedan recibir correo.</span><span class="sxs-lookup"><span data-stu-id="2c956-358">In this case, an administrator is advised to include MX records for all hosts incapable of receiving mail.</span></span> <span data-ttu-id="2c956-359">Si es distinto de cero, el servidor busca el nodo comodín más cercano; en este caso, un administrador debe colocar registros MX en la raíz de la zona y en un nodo comodín (' \* ') directamente debajo de la raíz de la zona.</span><span class="sxs-lookup"><span data-stu-id="2c956-359">If nonzero, the server seeks the closest wildcard node; in this case, an administrator should put MX records at the zone root and in a wildcard node ('\*') directly below the zone root.</span></span> <span data-ttu-id="2c956-360">Además, los administradores deben colocar registros MX que hagan referencia a sí mismos en los hosts que reciben su propio correo.</span><span class="sxs-lookup"><span data-stu-id="2c956-360">Also, administrators should put self-referencing MX records on hosts that receive their own mail.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-361">**MaxCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="2c956-361">**MaxCacheTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-362">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c956-362">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-363">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-363">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-364">Tiempo máximo, en segundos, que el registro de una consulta de nombres recursivos puede permanecer en la memoria caché del servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="2c956-364">Maximum time, in seconds, the record of a recursive name query may remain in the DNS Server cache.</span></span> <span data-ttu-id="2c956-365">El servidor DNS elimina los registros de la memoria caché cuando expira el valor de esta entrada, incluso si el valor del campo TTL del registro es mayor.</span><span class="sxs-lookup"><span data-stu-id="2c956-365">The DNS Server deletes records from the cache when the value of this entry expires, even if the value of the TTL field in the record is greater.</span></span>

<span data-ttu-id="2c956-366">El valor predeterminado de esta propiedad es 86.400 segundos (1 día).</span><span class="sxs-lookup"><span data-stu-id="2c956-366">The default value of this property is 86,400 seconds (1 day).</span></span>

</dd> <dt>

<span data-ttu-id="2c956-367">**MaxNegativeCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="2c956-367">**MaxNegativeCacheTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-368">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c956-368">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-369">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-369">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-370">Tiempo máximo, en segundos, que el resultado de un error de nombre de una consulta recursiva puede permanecer en la memoria caché del servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="2c956-370">Maximum time, in seconds, a name error result from a recursive query may remain in the DNS Server cache.</span></span> <span data-ttu-id="2c956-371">DNS elimina los registros de la memoria caché cuando este temporizador expira, incluso si el campo TTL es mayor.</span><span class="sxs-lookup"><span data-stu-id="2c956-371">DNS deletes records from the cache when this timer expires, even if the TTL field is greater.</span></span> <span data-ttu-id="2c956-372">El valor predeterminado es 86.400 (un día).</span><span class="sxs-lookup"><span data-stu-id="2c956-372">Default value is 86,400 (one day).</span></span>

</dd> <dt>

<span data-ttu-id="2c956-373">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="2c956-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-374">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2c956-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-375">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c956-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c956-376">Nombre de dominio completo (FQDN) o dirección IP del servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="2c956-376">Fully qualified domain name (FQDN) or IP address of the DNS Server.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-377">**NameCheckFlag**</span><span class="sxs-lookup"><span data-stu-id="2c956-377">**NameCheckFlag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-378">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c956-378">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-379">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-379">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-380">Indica el conjunto de caracteres válidos que se van a usar en los nombres DNS.</span><span class="sxs-lookup"><span data-stu-id="2c956-380">Indicates the set of eligible characters to be used in DNS names.</span></span> <span data-ttu-id="2c956-381">Se usan los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="2c956-381">The following values are used.</span></span>



| <span data-ttu-id="2c956-382">Value</span><span class="sxs-lookup"><span data-stu-id="2c956-382">Value</span></span>                                                                                                | <span data-ttu-id="2c956-383">Significado</span><span class="sxs-lookup"><span data-stu-id="2c956-383">Meaning</span></span>                      |
|------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="2c956-384"><dt>**0,1**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-384"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="2c956-385">RFC estricto (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2c956-385">Strict RFC (ANSI)</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="2c956-386"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-386"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="2c956-387">No RFC (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2c956-387">Non RFC (ANSI)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="2c956-388"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-388"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="2c956-389">Multibyte (UTF8)</span><span class="sxs-lookup"><span data-stu-id="2c956-389">Multibyte (UTF8)</span></span><br/>  |



 

<span data-ttu-id="2c956-390">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="2c956-390">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="2c956-391">Un valor de "2" indica "any".</span><span class="sxs-lookup"><span data-stu-id="2c956-391">A value of "2" indicates "Any."</span></span>

</dd> <dt>

<span data-ttu-id="2c956-392">**Recursividad**</span><span class="sxs-lookup"><span data-stu-id="2c956-392">**NoRecursion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-393">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2c956-393">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-394">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-394">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-395">Indica si el servidor DNS realiza búsquedas recursivas.</span><span class="sxs-lookup"><span data-stu-id="2c956-395">Indicates whether the DNS Server performs recursive look ups.</span></span> <span data-ttu-id="2c956-396">TRUE indica que no se realizan búsquedas recursivas.</span><span class="sxs-lookup"><span data-stu-id="2c956-396">TRUE indicates recursive look ups are not performed.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-397">**RecursionRetry**</span><span class="sxs-lookup"><span data-stu-id="2c956-397">**RecursionRetry**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-398">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c956-398">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-399">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-399">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-400">Segundos transcurridos antes de volver a intentar una búsqueda recursiva.</span><span class="sxs-lookup"><span data-stu-id="2c956-400">Elapsed seconds before retrying a recursive look up.</span></span> <span data-ttu-id="2c956-401">Si la propiedad no está definida o es cero, los reintentos se realizan después de tres segundos.</span><span class="sxs-lookup"><span data-stu-id="2c956-401">If the property is undefined or zero, retries are made after three seconds.</span></span> <span data-ttu-id="2c956-402">No se recomienda a los usuarios modificar esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="2c956-402">Users are discouraged from altering this property.</span></span> <span data-ttu-id="2c956-403">Hay ciertas situaciones en las que se debe cambiar la propiedad; un ejemplo es cuando el servidor DNS se pone en contacto con los servidores remotos a través de un vínculo de baja velocidad y el servidor DNS vuelve a intentarlo antes de recibir la respuesta del DNS remoto.</span><span class="sxs-lookup"><span data-stu-id="2c956-403">There are certain situations when the property should be changed; one example is when the DNS Server contacts remote servers over a slow link, and the DNS Server is retrying before receiving response from the remote DNS.</span></span> <span data-ttu-id="2c956-404">En este caso, sería razonable aumentar el tiempo de espera para que sea ligeramente mayor que el tiempo de respuesta observado del DNS remoto.</span><span class="sxs-lookup"><span data-stu-id="2c956-404">In this case, raising the time out to be slightly longer than the observed response time from the remote DNS would be reasonable.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-405">**RecursionTimeout**</span><span class="sxs-lookup"><span data-stu-id="2c956-405">**RecursionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-406">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c956-406">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-407">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-407">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-408">Segundos transcurridos antes de que el servidor DNS proporcione una consulta recursiva.</span><span class="sxs-lookup"><span data-stu-id="2c956-408">Elapsed seconds before the DNS Server gives up recursive query.</span></span> <span data-ttu-id="2c956-409">Si la propiedad no está definida o es cero, el servidor DNS se muestra después de 15 segundos.</span><span class="sxs-lookup"><span data-stu-id="2c956-409">If the property is undefined or zero, the DNS Server gives up after 15 seconds.</span></span> <span data-ttu-id="2c956-410">En general, el tiempo de espera de 15 segundos es suficiente para permitir que cualquier respuesta pendiente vuelva al servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="2c956-410">In general, the 15-second time out is sufficient to allow any outstanding response to get back to the DNS Server.</span></span>

<span data-ttu-id="2c956-411">No se recomienda a los usuarios modificar esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="2c956-411">Users are discouraged from altering this property.</span></span> <span data-ttu-id="2c956-412">Un escenario en el que se debe cambiar la propiedad es cuando el servidor DNS se pone en contacto con los servidores remotos a través de un vínculo de baja velocidad y se observa que el servidor DNS rechaza las consultas (con errores del servidor \_ ) antes de que se reciban las respuestas.</span><span class="sxs-lookup"><span data-stu-id="2c956-412">One scenario where the property should be changed is when the DNS Server contacts remote servers over a slow link, and the DNS Server is observed rejecting queries (with SERVER\_FAILURE) before responses are received.</span></span>

<span data-ttu-id="2c956-413">Los solucionadores de cliente también reintentan las consultas, por lo que es necesaria una investigación cuidadosa para determinar si las respuestas remotas están asociadas realmente a la consulta que agotó el tiempo de espera. En este caso, la elevación del valor de tiempo de espera para que sea ligeramente mayor que el tiempo de respuesta observado del DNS remoto sería razonable.</span><span class="sxs-lookup"><span data-stu-id="2c956-413">Client resolvers also retry queries, so careful investigation is required to determine whether remote responses are actually associated with the query that timed out. In this case, raising the time out value to be slightly longer than the observed response time from the remote DNS would be reasonable.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-414">**RoundRobin**</span><span class="sxs-lookup"><span data-stu-id="2c956-414">**RoundRobin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-415">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2c956-415">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-416">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-416">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-417">Indica si el servidor DNS redondea Robins varios registros A.</span><span class="sxs-lookup"><span data-stu-id="2c956-417">Indicates whether the DNS Server round robins multiple A records.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-418">**RPC**</span><span class="sxs-lookup"><span data-stu-id="2c956-418">**RpcProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-419">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2c956-419">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-420">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-420">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-421">Protocolo RPC o protocolos en los que se ejecuta RPC administrativo.</span><span class="sxs-lookup"><span data-stu-id="2c956-421">RPC protocol or protocols over which administrative RPC runs.</span></span> <span data-ttu-id="2c956-422">El algoritmo siguiente se utiliza para asignar un valor específico:</span><span class="sxs-lookup"><span data-stu-id="2c956-422">The following algorithm is used to assign a specific value:</span></span>



| <span data-ttu-id="2c956-423">Value</span><span class="sxs-lookup"><span data-stu-id="2c956-423">Value</span></span>                                                                                                | <span data-ttu-id="2c956-424">Significado</span><span class="sxs-lookup"><span data-stu-id="2c956-424">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="2c956-425"><dt>**0,1**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-425"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="2c956-426">None</span><span class="sxs-lookup"><span data-stu-id="2c956-426">None</span></span><br/>        |
| <span id="1"></span><dl> <span data-ttu-id="2c956-427"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-427"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="2c956-428">TCP</span><span class="sxs-lookup"><span data-stu-id="2c956-428">TCP</span></span><br/>         |
| <span id="2"></span><dl> <span data-ttu-id="2c956-429"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-429"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="2c956-430">Canalizaciones con nombre</span><span class="sxs-lookup"><span data-stu-id="2c956-430">Named Pipes</span></span><br/> |
| <span id="4"></span><dl> <span data-ttu-id="2c956-431"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-431"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="2c956-432">LPC</span><span class="sxs-lookup"><span data-stu-id="2c956-432">LPC</span></span><br/>         |



 

<span data-ttu-id="2c956-433">La suma de los valores indica los protocolos usados.</span><span class="sxs-lookup"><span data-stu-id="2c956-433">The sum of the values indicates the protocols used.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-434">**ScavengingInterval**</span><span class="sxs-lookup"><span data-stu-id="2c956-434">**ScavengingInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-435">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c956-435">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-436">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-436">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-437">Intervalo, en horas, entre dos operaciones de eliminación de registros obsoletos consecutivas realizadas por el servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="2c956-437">Interval, in hours, between two consecutive scavenging operations performed by the DNS Server.</span></span> <span data-ttu-id="2c956-438">Cero indica que la eliminación de registros obsoletos está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="2c956-438">Zero indicates scavenging is disabled.</span></span> <span data-ttu-id="2c956-439">El valor predeterminado es 168 horas (siete días).</span><span class="sxs-lookup"><span data-stu-id="2c956-439">The default value is 168 hours (seven days).</span></span>

</dd> <dt>

<span data-ttu-id="2c956-440">**SecureResponses**</span><span class="sxs-lookup"><span data-stu-id="2c956-440">**SecureResponses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-441">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2c956-441">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-442">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-442">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-443">Indica si el servidor DNS guarda exclusivamente los registros de nombres en el mismo subárbol que el servidor que los proporcionó.</span><span class="sxs-lookup"><span data-stu-id="2c956-443">Indicates whether the DNS Server exclusively saves records of names in the same subtree as the server that provided them.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-444">**SendPort**</span><span class="sxs-lookup"><span data-stu-id="2c956-444">**SendPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-445">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c956-445">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-446">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-446">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-447">Puerto en el que el servidor DNS envía consultas UDP a otros servidores.</span><span class="sxs-lookup"><span data-stu-id="2c956-447">Port on which the DNS Server sends UDP queries to other servers.</span></span> <span data-ttu-id="2c956-448">De forma predeterminada, el servidor DNS envía consultas en un socket enlazado al puerto DNS.</span><span class="sxs-lookup"><span data-stu-id="2c956-448">By default, the DNS Server sends queries on a socket bound to the DNS port.</span></span>

<span data-ttu-id="2c956-449">En determinadas situaciones, no es la mejor configuración.</span><span class="sxs-lookup"><span data-stu-id="2c956-449">Under certain situations, this is not the best configuration.</span></span> <span data-ttu-id="2c956-450">Un caso obvio es cuando un administrador bloquea el puerto DNS con un firewall para evitar el acceso externo al servidor DNS, pero aún desea que el servidor pueda ponerse en contacto con los servidores DNS de Internet para proporcionar resolución de nombres para los clientes internos.</span><span class="sxs-lookup"><span data-stu-id="2c956-450">One obvious case is when an administrator blocks the DNS port with a firewall to prevent outside access to the DNS Server, but still wants the server to be able to contact Internet DNS Servers to provide name resolution for internal clients.</span></span> <span data-ttu-id="2c956-451">Otro caso es cuando el servidor DNS admite redes no contiguas (la propiedad **DisjointNets** establecida en true identifica este escenario).</span><span class="sxs-lookup"><span data-stu-id="2c956-451">Another case is when the DNS Server is supporting disjoint nets (the property **DisjointNets** set to TRUE identifies this scenario).</span></span> <span data-ttu-id="2c956-452">En estos casos, el establecimiento de la propiedad **SendOnNonDnsPort** en un valor distinto de cero indica al servidor DNS que se enlace a un puerto arbitrario para enviarlo a servidores DNS remotos.</span><span class="sxs-lookup"><span data-stu-id="2c956-452">In these cases, setting the **SendOnNonDnsPort** property to a nonzero value directs the DNS Server to bind to an arbitrary port for sending to remote DNS Servers.</span></span>

<span data-ttu-id="2c956-453">Si el valor de **SendOnNonDnsPort** es mayor que 1024, el servidor DNS se enlaza explícitamente con el valor de puerto especificado.</span><span class="sxs-lookup"><span data-stu-id="2c956-453">If the **SendOnNonDnsPort** value is greater than 1024, the DNS Server binds explicitly to the port value given.</span></span> <span data-ttu-id="2c956-454">Esta opción de configuración es útil cuando un administrador necesita corregir el puerto de consulta DNS para fines de Firewall.</span><span class="sxs-lookup"><span data-stu-id="2c956-454">This configuration option is useful when an administrator needs to fix the DNS query port for firewall purposes.</span></span>

<span data-ttu-id="2c956-455">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="2c956-455">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="2c956-456">Si se establece la propiedad puertoEnvío en un valor distinto de cero, el servidor DNS se enlaza a un puerto arbitrario para el envío a servidores DNS remotos.</span><span class="sxs-lookup"><span data-stu-id="2c956-456">Setting the SendPort property to a non-zero value causes the DNS server to bind to an arbitrary port for sending to remote DNS servers.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-457">**ServerAddresses**</span><span class="sxs-lookup"><span data-stu-id="2c956-457">**ServerAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-458">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="2c956-458">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2c956-459">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c956-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c956-460">Enumera la lista de direcciones IP para el servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="2c956-460">Enumerates the list of IP addresses for the DNS Server.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-461">**StrictFileParsing**</span><span class="sxs-lookup"><span data-stu-id="2c956-461">**StrictFileParsing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-462">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2c956-462">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-463">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-463">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-464">Indica si el servidor DNS analiza estrictamente [*los archivos de zona*](z-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="2c956-464">Indicates whether the DNS Server parses [*zone files*](z-gly.md) strictly.</span></span> <span data-ttu-id="2c956-465">Si no está definida o es cero, el servidor registrará y omitirá los datos incorrectos en el archivo de zona y continuará con la carga.</span><span class="sxs-lookup"><span data-stu-id="2c956-465">If undefined or zero, the server will log and ignore bad data in the zone file and continue to load.</span></span> <span data-ttu-id="2c956-466">Si es distinto de cero, el servidor registrará los errores de archivos de zona y se producirá un error en ellos.</span><span class="sxs-lookup"><span data-stu-id="2c956-466">If nonzero, the server will log and fail on zone file errors.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-467">**UpdateOptions**</span><span class="sxs-lookup"><span data-stu-id="2c956-467">**UpdateOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-468">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c956-468">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-469">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c956-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c956-470">Restringe el tipo de registros que se pueden actualizar dinámicamente en el servidor, que se usan además de los valores de **AllowUpdate** en objetos de servidor y zona.</span><span class="sxs-lookup"><span data-stu-id="2c956-470">Restricts the type of records that can be dynamically updated on the server, used in addition to the **AllowUpdate** settings on Server and Zone objects.</span></span>

<span data-ttu-id="2c956-471">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="2c956-471">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="2c956-472">0: sin restricciones.</span><span class="sxs-lookup"><span data-stu-id="2c956-472">0: No restrictions.</span></span>

<span data-ttu-id="2c956-473">1: no permitir actualizaciones dinámicas de registros SOA.</span><span class="sxs-lookup"><span data-stu-id="2c956-473">1: Do not allow dynamic updates of SOA records.</span></span>

<span data-ttu-id="2c956-474">2: no permitir actualizaciones dinámicas de registros NS en la raíz de la zona.</span><span class="sxs-lookup"><span data-stu-id="2c956-474">2: Do not allow dynamic updates of NS records at the zone root.</span></span>

<span data-ttu-id="2c956-475">4: no permitir actualizaciones dinámicas de registros NS que no se realicen en la raíz de la zona (registros NS de delegación).</span><span class="sxs-lookup"><span data-stu-id="2c956-475">4: Do not allow dynamic updates of NS records not at the zone root (delegation NS records).</span></span>

<span data-ttu-id="2c956-476">Sume estos valores para determinar el valor de configuración.</span><span class="sxs-lookup"><span data-stu-id="2c956-476">Sum these values to determine the setting value.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-477">**Versión**</span><span class="sxs-lookup"><span data-stu-id="2c956-477">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-478">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c956-478">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-479">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c956-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c956-480">Versión del servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="2c956-480">Version of the DNS Server.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-481">**WriteAuthorityNS**</span><span class="sxs-lookup"><span data-stu-id="2c956-481">**WriteAuthorityNS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-482">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2c956-482">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-483">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-483">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-484">Especifica si el servidor DNS escribe registros NS y SOA en la sección de autoridad en una respuesta correcta.</span><span class="sxs-lookup"><span data-stu-id="2c956-484">Specifies whether the DNS Server writes NS and SOA records to the authority section on successful response.</span></span>

</dd> <dt>

<span data-ttu-id="2c956-485">**XfrConnectTimeout**</span><span class="sxs-lookup"><span data-stu-id="2c956-485">**XfrConnectTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c956-486">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c956-486">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c956-487">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c956-487">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c956-488">Tiempo, en segundos, que el servidor DNS espera una conexión TCP correcta con un servidor remoto al intentar una transferencia de zona.</span><span class="sxs-lookup"><span data-stu-id="2c956-488">Time, in seconds, the DNS Server waits for a successful TCP connection to a remote server when attempting a zone transfer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c956-489">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c956-489">Requirements</span></span>



| <span data-ttu-id="2c956-490">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c956-490">Requirement</span></span> | <span data-ttu-id="2c956-491">Value</span><span class="sxs-lookup"><span data-stu-id="2c956-491">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c956-492">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c956-492">Minimum supported client</span></span><br/> | <span data-ttu-id="2c956-493">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2c956-493">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2c956-494">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c956-494">Minimum supported server</span></span><br/> | <span data-ttu-id="2c956-495">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2c956-495">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2c956-496">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2c956-496">Namespace</span></span><br/>                | <span data-ttu-id="2c956-497">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="2c956-497">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="2c956-498">MOF</span><span class="sxs-lookup"><span data-stu-id="2c956-498">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c956-499"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c956-499"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c956-500">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c956-500">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c956-501">**Método StartService de la \_ clase de servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="2c956-501">**StartService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startservice.md)
</dt> <dt>

[<span data-ttu-id="2c956-502">**Método StopService de la \_ clase de servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="2c956-502">**StopService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-stopservice.md)
</dt> <dt>

[<span data-ttu-id="2c956-503">**Método StartScavenging de la \_ clase de servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="2c956-503">**StartScavenging Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startscavenging.md)
</dt> <dt>

[<span data-ttu-id="2c956-504">**Método GetDistinguishedName de la \_ clase de servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="2c956-504">**GetDistinguishedName Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





