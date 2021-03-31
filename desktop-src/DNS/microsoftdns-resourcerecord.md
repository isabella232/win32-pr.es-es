---
title: MicrosoftDNS_ResourceRecord (clase)
description: La \_ clase MicrosoftDNS ResourceRecord representa las propiedades generales de un RR de DNS. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 84d6d106-fcc9-44ae-8db2-181c60489aec
keywords:
- DNS de la clase MicrosoftDNS_ResourceRecord
- MicrosoftDNS_ResourceRecord de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord
- MicrosoftDNS_ResourceRecord.CreateInstanceFromTextRepresentation
- MicrosoftDNS_ResourceRecord.GetObjectByTextRepresentation
- MicrosoftDNS_ResourceRecord.DnsServerName
- MicrosoftDNS_ResourceRecord.ContainerName
- MicrosoftDNS_ResourceRecord.DomainName
- MicrosoftDNS_ResourceRecord.OwnerName
- MicrosoftDNS_ResourceRecord.RecordClass 1
- MicrosoftDNS_ResourceRecord.TTL
- MicrosoftDNS_ResourceRecord.TimeStamp
- MicrosoftDNS_ResourceRecord.RecordData
- MicrosoftDNS_ResourceRecord.TextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe546ceabb5590ccd4907448af5efd5e2d4fe2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996546"
---
# <a name="microsoftdns_resourcerecord-class"></a><span data-ttu-id="db3db-105">MicrosoftDNS ( \_ clase ResourceRecord)</span><span class="sxs-lookup"><span data-stu-id="db3db-105">MicrosoftDNS\_ResourceRecord class</span></span>

<span data-ttu-id="db3db-106">La clase **MicrosoftDNS \_ ResourceRecord** representa las propiedades generales de un RR de DNS.</span><span class="sxs-lookup"><span data-stu-id="db3db-106">The **MicrosoftDNS\_ResourceRecord** class represents the general properties of a DNS RR.</span></span>

<span data-ttu-id="db3db-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="db3db-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="db3db-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="db3db-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_ResourceRecord : CIM_LogicalElement
{
  string DnsServerName;
  string ContainerName;
  string DomainName;
  string OwnerName;
  uint16 RecordClass=1;
  uint32 TTL;
  uint32 TimeStamp;
  string RecordData;
  string TextRepresentation;
};
```

## <a name="members"></a><span data-ttu-id="db3db-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="db3db-109">Members</span></span>

<span data-ttu-id="db3db-110">La clase **MicrosoftDNS \_ ResourceRecord** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="db3db-110">The **MicrosoftDNS\_ResourceRecord** class has these types of members:</span></span>

-   [<span data-ttu-id="db3db-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="db3db-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="db3db-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="db3db-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="db3db-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="db3db-113">Methods</span></span>

<span data-ttu-id="db3db-114">La clase **MicrosoftDNS \_ ResourceRecord** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="db3db-114">The **MicrosoftDNS\_ResourceRecord** class has these methods.</span></span>



| <span data-ttu-id="db3db-115">Método</span><span class="sxs-lookup"><span data-stu-id="db3db-115">Method</span></span>                                   | <span data-ttu-id="db3db-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="db3db-116">Description</span></span>                                                                                                                                                                                                                                                            |
|:-----------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db3db-117">**CreateInstanceFromTextRepresentation**</span><span class="sxs-lookup"><span data-stu-id="db3db-117">**CreateInstanceFromTextRepresentation**</span></span> | <span data-ttu-id="db3db-118">Analiza el RR de la cadena TextRepresentation y con el servidor DNS de entrada y los nombres de contenedor, define y crea instancias de un objeto ResourceRecord.</span><span class="sxs-lookup"><span data-stu-id="db3db-118">Parses the RR in the TextRepresentation string, and with the input DNS Server and Container Names, defines, and instantiates a ResourceRecord object.</span></span> <span data-ttu-id="db3db-119">El método devuelve una referencia al nuevo objeto como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="db3db-119">The method returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="db3db-120">Calificadores: Ninguno</span><span class="sxs-lookup"><span data-stu-id="db3db-120">Qualifiers: None</span></span><br/> |
| <span data-ttu-id="db3db-121">**GetObjectByTextRepresentation**</span><span class="sxs-lookup"><span data-stu-id="db3db-121">**GetObjectByTextRepresentation**</span></span>        | <span data-ttu-id="db3db-122">Recupera una instancia existente de la \_ subclase MicrosoftDns ResourceRecord, representada por la cadena TextRepresentation junto con el servidor DNS y el nombre del contenedor.</span><span class="sxs-lookup"><span data-stu-id="db3db-122">Retrieves an existing instance of the MicrosoftDns\_ResourceRecord subclass, represented by the TextRepresentation string along with the DNS Server and Container Name.</span></span> <br/> <span data-ttu-id="db3db-123">Calificadores: Ninguno</span><span class="sxs-lookup"><span data-stu-id="db3db-123">Qualifiers: None</span></span><br/>                                                        |



 

### <a name="properties"></a><span data-ttu-id="db3db-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="db3db-124">Properties</span></span>

<span data-ttu-id="db3db-125">La clase **MicrosoftDNS \_ ResourceRecord** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="db3db-125">The **MicrosoftDNS\_ResourceRecord** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="db3db-126">**ContainerName**</span><span class="sxs-lookup"><span data-stu-id="db3db-126">**ContainerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db3db-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="db3db-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db3db-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db3db-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db3db-129">Indica el nombre del contenedor de la zona, la memoria caché o la instancia de RootHints que contiene el RR.</span><span class="sxs-lookup"><span data-stu-id="db3db-129">Indicates the name of the Container for the Zone, Cache, or RootHints instance that contains the RR.</span></span>

</dd> <dt>

<span data-ttu-id="db3db-130">**DnsServerName**</span><span class="sxs-lookup"><span data-stu-id="db3db-130">**DnsServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db3db-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="db3db-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db3db-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db3db-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db3db-133">Indica el FQDN o la dirección IP del servidor DNS que contiene el RR.</span><span class="sxs-lookup"><span data-stu-id="db3db-133">Indicates the FQDN or IP address of the DNS Server that contains the RR.</span></span>

</dd> <dt>

<span data-ttu-id="db3db-134">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="db3db-134">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db3db-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="db3db-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db3db-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db3db-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db3db-137">Representa el FQDN del dominio que contiene el RR.</span><span class="sxs-lookup"><span data-stu-id="db3db-137">Represents the FQDN of the Domain that contains the RR.</span></span> <span data-ttu-id="db3db-138">Esta propiedad puede contener las cadenas \\ . Almacenar en caché \\ o \\ .. RootHints \\ si la memoria caché interna o RootHints contiene el RR, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="db3db-138">This property may contain the strings \\..Cache\\ or \\..RootHints\\ if the internal cache or RootHints contain the RR, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="db3db-139">**OwnerName**</span><span class="sxs-lookup"><span data-stu-id="db3db-139">**OwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db3db-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="db3db-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db3db-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db3db-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db3db-142">Nombre del propietario del RR.</span><span class="sxs-lookup"><span data-stu-id="db3db-142">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="db3db-143">**RecordClass = 1**</span><span class="sxs-lookup"><span data-stu-id="db3db-143">**RecordClass=1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db3db-144">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="db3db-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="db3db-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db3db-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db3db-146">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="db3db-146">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="db3db-147">Esta cadena representa la clase del registro de recursos.</span><span class="sxs-lookup"><span data-stu-id="db3db-147">This string represents the class of the Resource Record.</span></span> <span data-ttu-id="db3db-148">Los valores válidos son:</span><span class="sxs-lookup"><span data-stu-id="db3db-148">Valid values include:</span></span>

<span data-ttu-id="db3db-149">1: en (Internet)</span><span class="sxs-lookup"><span data-stu-id="db3db-149">1: IN (Internet)</span></span>

<span data-ttu-id="db3db-150">2: CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="db3db-150">2: CS (CSNET)</span></span>

<span data-ttu-id="db3db-151">3: CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="db3db-151">3: CH (CHAOS)</span></span>

<span data-ttu-id="db3db-152">4: HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="db3db-152">4: HS (Hesiod)</span></span>

</dd> <dt>

<span data-ttu-id="db3db-153">**RecordData**</span><span class="sxs-lookup"><span data-stu-id="db3db-153">**RecordData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db3db-154">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="db3db-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db3db-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db3db-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db3db-156">Datos de registro de recursos.</span><span class="sxs-lookup"><span data-stu-id="db3db-156">Resource record data.</span></span>

</dd> <dt>

<span data-ttu-id="db3db-157">**TextRepresentation**</span><span class="sxs-lookup"><span data-stu-id="db3db-157">**TextRepresentation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db3db-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="db3db-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db3db-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db3db-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db3db-160">Representación de texto de todo el RR.</span><span class="sxs-lookup"><span data-stu-id="db3db-160">Text representation of the entire RR.</span></span>

</dd> <dt>

<span data-ttu-id="db3db-161">**Indicaciones**</span><span class="sxs-lookup"><span data-stu-id="db3db-161">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db3db-162">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db3db-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db3db-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db3db-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db3db-164">Hora a la que se actualizó por última vez el RR, expresado en horas transcurridas desde el 1 de enero de 1601, hora del meridiano de Greenwich (GMT).</span><span class="sxs-lookup"><span data-stu-id="db3db-164">Time at which the RR was last refreshed, expressed in elapsed hours since January 1, 1601, Greenwich Mean Time (GMT).</span></span>

</dd> <dt>

<span data-ttu-id="db3db-165">**TTL**</span><span class="sxs-lookup"><span data-stu-id="db3db-165">**TTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db3db-166">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db3db-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db3db-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db3db-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db3db-168">Tiempo, en segundos, que un [*solucionador*](r-gly.md)DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="db3db-168">Time, in seconds, that the RR can be cached by a DNS [*resolver*](r-gly.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="db3db-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db3db-169">Requirements</span></span>



| <span data-ttu-id="db3db-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="db3db-170">Requirement</span></span> | <span data-ttu-id="db3db-171">Value</span><span class="sxs-lookup"><span data-stu-id="db3db-171">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="db3db-172">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db3db-172">Minimum supported client</span></span><br/> | <span data-ttu-id="db3db-173">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="db3db-173">None supported</span></span><br/>                                                              |
| <span data-ttu-id="db3db-174">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db3db-174">Minimum supported server</span></span><br/> | <span data-ttu-id="db3db-175">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="db3db-175">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="db3db-176">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="db3db-176">Namespace</span></span><br/>                | <span data-ttu-id="db3db-177">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="db3db-177">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="db3db-178">MOF</span><span class="sxs-lookup"><span data-stu-id="db3db-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db3db-179"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="db3db-179"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db3db-180">Vea también</span><span class="sxs-lookup"><span data-stu-id="db3db-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db3db-181">**Método CreateInstanceFromTextRepresentation de la \_ clase MicrosoftDNS ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="db3db-181">**CreateInstanceFromTextRepresentation Method of the MicrosoftDNS\_ResourceRecord Class**</span></span>](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> <dt>

[<span data-ttu-id="db3db-182">**Método GetObjectByTextRepresentation de la \_ clase MicrosoftDNS ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="db3db-182">**GetObjectByTextRepresentation Method of the MicrosoftDNS\_ResourceRecord Class**</span></span>](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





