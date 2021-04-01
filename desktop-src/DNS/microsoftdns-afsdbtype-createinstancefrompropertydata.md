---
title: Método CreateInstanceFromPropertyData de la clase MicrosoftDNS_AFSDBType
description: El método CreateInstanceFromPropertyData crea una instancia de un registro de recursos del servidor de base de datos del sistema de archivos de Andrew (AFSDB).
ms.assetid: 2cd0434d-0c18-468f-95f3-7a77375596a3
keywords:
- CreateInstanceFromPropertyData el método DNS
- Método CreateInstanceFromPropertyData DNS, clase MicrosoftDNS_AFSDBType
- MicrosoftDNS_AFSDBType de clase DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04efd6e18ef4267d9887252f91e8a215fcf3ee88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996402"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_afsdbtype-class"></a><span data-ttu-id="35ba3-106">Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS AFSDBType</span><span class="sxs-lookup"><span data-stu-id="35ba3-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_AFSDBType class</span></span>

<span data-ttu-id="35ba3-107">El método **CreateInstanceFromPropertyData** crea una instancia de un registro de recursos del servidor de base de datos del sistema de archivos de Andrew (AFSDB).</span><span class="sxs-lookup"><span data-stu-id="35ba3-107">The **CreateInstanceFromPropertyData** method instantiates an Andrew File System Database Server (AFSDB) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="35ba3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35ba3-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           uint16                 Subtype,
  [in]           string                 ServerName,
  [out, ref]     MicrosoftDNS_AFSDBType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="35ba3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35ba3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35ba3-110">*DnsServerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="35ba3-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35ba3-111">FQDN o dirección IP del servidor DNS que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="35ba3-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="35ba3-112">*ContainerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="35ba3-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35ba3-113">Nombre del contenedor de la zona, la memoria caché o la instancia de RootHints que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="35ba3-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="35ba3-114">*Nombrepropietario* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="35ba3-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35ba3-115">Nombre del propietario del RR.</span><span class="sxs-lookup"><span data-stu-id="35ba3-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="35ba3-116">*RecordClass* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="35ba3-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="35ba3-117">Clase del RR.</span><span class="sxs-lookup"><span data-stu-id="35ba3-117">Class of the RR.</span></span> <span data-ttu-id="35ba3-118">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="35ba3-118">Default value is 1.</span></span> <span data-ttu-id="35ba3-119">Los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="35ba3-119">The following values are valid.</span></span>



| <span data-ttu-id="35ba3-120">Value</span><span class="sxs-lookup"><span data-stu-id="35ba3-120">Value</span></span>                                                                                                | <span data-ttu-id="35ba3-121">Significado</span><span class="sxs-lookup"><span data-stu-id="35ba3-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="35ba3-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="35ba3-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="35ba3-123">EN (Internet)</span><span class="sxs-lookup"><span data-stu-id="35ba3-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="35ba3-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="35ba3-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="35ba3-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="35ba3-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="35ba3-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="35ba3-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="35ba3-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="35ba3-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="35ba3-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="35ba3-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="35ba3-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="35ba3-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="35ba3-130">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="35ba3-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="35ba3-131">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="35ba3-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="35ba3-132">*Subtipo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="35ba3-132">*Subtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35ba3-133">Subtipo del servidor AFS del host.</span><span class="sxs-lookup"><span data-stu-id="35ba3-133">Subtype of the host AFS server.</span></span> <span data-ttu-id="35ba3-134">Para el subtipo 1 (valor = 1), el host tiene un servidor de ubicación del volumen AFS versión 3,0 para la celda AFS con nombre.</span><span class="sxs-lookup"><span data-stu-id="35ba3-134">For subtype 1 (value=1), the host has an AFS version 3.0 Volume Location Server for the named AFS cell.</span></span> <span data-ttu-id="35ba3-135">En el caso del subtipo 2 (valor = 2), el host tiene un servidor de nombres autenticado que contiene el nodo del directorio raíz de la celda para la celda de DCE/NCA con nombre.</span><span class="sxs-lookup"><span data-stu-id="35ba3-135">In the case of subtype 2 (value=2), the host has an authenticated name server holding the cell-root directory node for the named DCE/NCA cell.</span></span>

</dd> <dt>

<span data-ttu-id="35ba3-136">*NombreDeServidor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="35ba3-136">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35ba3-137">FQDN que especifica un host que tiene un servidor para la celda AFS especificada en el nombre del propietario.</span><span class="sxs-lookup"><span data-stu-id="35ba3-137">FQDN specifying a host that has a server for the AFS cell specified in the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="35ba3-138">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="35ba3-138">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="35ba3-139">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="35ba3-139">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35ba3-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35ba3-140">Return value</span></span>

<span data-ttu-id="35ba3-141">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="35ba3-141">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="35ba3-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35ba3-142">Requirements</span></span>



| <span data-ttu-id="35ba3-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="35ba3-143">Requirement</span></span> | <span data-ttu-id="35ba3-144">Value</span><span class="sxs-lookup"><span data-stu-id="35ba3-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35ba3-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35ba3-145">Minimum supported client</span></span><br/> | <span data-ttu-id="35ba3-146">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="35ba3-146">None supported</span></span><br/>                                                              |
| <span data-ttu-id="35ba3-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35ba3-147">Minimum supported server</span></span><br/> | <span data-ttu-id="35ba3-148">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="35ba3-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="35ba3-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="35ba3-149">Namespace</span></span><br/>                | <span data-ttu-id="35ba3-150">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="35ba3-150">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="35ba3-151">MOF</span><span class="sxs-lookup"><span data-stu-id="35ba3-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35ba3-152"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35ba3-152"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35ba3-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="35ba3-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35ba3-154">**MicrosoftDNS \_ AFSDBType**</span><span class="sxs-lookup"><span data-stu-id="35ba3-154">**MicrosoftDNS\_AFSDBType**</span></span>](microsoftdns-afsdbtype.md)
</dt> <dt>

[<span data-ttu-id="35ba3-155">**Método Modify de la \_ clase MicrosoftDNS AFSDBType**</span><span class="sxs-lookup"><span data-stu-id="35ba3-155">**Modify Method of the MicrosoftDNS\_AFSDBType Class**</span></span>](microsoftdns-afsdbtype-modify.md)
</dt> <dt>

[<span data-ttu-id="35ba3-156">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="35ba3-156">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





