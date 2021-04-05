---
title: Método CreateInstanceFromPropertyData de la clase MicrosoftDNS_KEYType
description: El método CreateInstanceFromPropertyData crea instancias de un registro de recursos de clave.
ms.assetid: 77d7b800-4077-46da-9199-e2abb5801978
keywords:
- CreateInstanceFromPropertyData el método DNS
- Método CreateInstanceFromPropertyData DNS, clase MicrosoftDNS_KEYType
- MicrosoftDNS_KEYType de clase DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b16dc8f3f591ba3aaf5ac9883cdd3a15c85146d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079739"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_keytype-class"></a><span data-ttu-id="8a0a7-106">Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS KEYType</span><span class="sxs-lookup"><span data-stu-id="8a0a7-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_KEYType class</span></span>

<span data-ttu-id="8a0a7-107">El método **CreateInstanceFromPropertyData** crea instancias de un registro de recursos de clave.</span><span class="sxs-lookup"><span data-stu-id="8a0a7-107">The **CreateInstanceFromPropertyData** method instantiates a KEY Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a0a7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a0a7-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               Flags,
  [in]           uint16               Protocol,
  [in]           uint16               Algorithm,
  [in]           string               PublicKey,
  [out, ref]     MicrosoftDNS_KEYType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="8a0a7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8a0a7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a0a7-110">*DnsServerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8a0a7-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a0a7-111">FQDN o dirección IP del servidor DNS que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="8a0a7-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="8a0a7-112">*ContainerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8a0a7-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a0a7-113">Nombre del contenedor de la zona, la memoria caché o la instancia de RootHints que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="8a0a7-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="8a0a7-114">*Nombrepropietario* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8a0a7-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a0a7-115">Nombre del propietario del RR.</span><span class="sxs-lookup"><span data-stu-id="8a0a7-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="8a0a7-116">*RecordClass* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8a0a7-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8a0a7-117">Clase del RR.</span><span class="sxs-lookup"><span data-stu-id="8a0a7-117">Class of the RR.</span></span> <span data-ttu-id="8a0a7-118">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="8a0a7-118">Default value is 1.</span></span> <span data-ttu-id="8a0a7-119">Los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="8a0a7-119">The following values are valid.</span></span>



| <span data-ttu-id="8a0a7-120">Value</span><span class="sxs-lookup"><span data-stu-id="8a0a7-120">Value</span></span>                                                                                                | <span data-ttu-id="8a0a7-121">Significado</span><span class="sxs-lookup"><span data-stu-id="8a0a7-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="8a0a7-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="8a0a7-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="8a0a7-123">EN (Internet)</span><span class="sxs-lookup"><span data-stu-id="8a0a7-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="8a0a7-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="8a0a7-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="8a0a7-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="8a0a7-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="8a0a7-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="8a0a7-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="8a0a7-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="8a0a7-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="8a0a7-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="8a0a7-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="8a0a7-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="8a0a7-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="8a0a7-130">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8a0a7-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8a0a7-131">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="8a0a7-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="8a0a7-132">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="8a0a7-132">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a0a7-133">Marcas usadas para especificar la asignación, como se describe en IETF RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="8a0a7-133">Flags used to specify mapping, as described in IETF RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="8a0a7-134">*Protocolo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="8a0a7-134">*Protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a0a7-135">Protocolo para el que se puede usar la clave especificada en el registro de recursos.</span><span class="sxs-lookup"><span data-stu-id="8a0a7-135">Protocol for which the key specified in the resource record can be used.</span></span> <span data-ttu-id="8a0a7-136">Los valores asignados se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8a0a7-136">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="8a0a7-137">Value</span><span class="sxs-lookup"><span data-stu-id="8a0a7-137">Value</span></span>                                                                                                    | <span data-ttu-id="8a0a7-138">Significado</span><span class="sxs-lookup"><span data-stu-id="8a0a7-138">Meaning</span></span>                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="8a0a7-139"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="8a0a7-139"><dt>**1**</dt></span></span> </dl>     | <span data-ttu-id="8a0a7-140">TLS</span><span class="sxs-lookup"><span data-stu-id="8a0a7-140">TLS</span></span><br/>           |
| <span id="2"></span><dl> <span data-ttu-id="8a0a7-141"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="8a0a7-141"><dt>**2**</dt></span></span> </dl>     | <span data-ttu-id="8a0a7-142">Correo electrónico</span><span class="sxs-lookup"><span data-stu-id="8a0a7-142">E-Mail</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="8a0a7-143"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="8a0a7-143"><dt>**3**</dt></span></span> </dl>     | <span data-ttu-id="8a0a7-144">DNSSEC</span><span class="sxs-lookup"><span data-stu-id="8a0a7-144">dnssec</span></span><br/>        |
| <span id="4"></span><dl> <span data-ttu-id="8a0a7-145"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="8a0a7-145"><dt>**4**</dt></span></span> </dl>     | <span data-ttu-id="8a0a7-146">IPsec</span><span class="sxs-lookup"><span data-stu-id="8a0a7-146">IPsec</span></span><br/>         |
| <span id="255"></span><dl> <span data-ttu-id="8a0a7-147"><dt>**255**</dt></span><span class="sxs-lookup"><span data-stu-id="8a0a7-147"><dt>**255**</dt></span></span> </dl> | <span data-ttu-id="8a0a7-148">Todos los protocolos</span><span class="sxs-lookup"><span data-stu-id="8a0a7-148">All protocols</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8a0a7-149">*Algoritmo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="8a0a7-149">*Algorithm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a0a7-150">Algoritmo usado con la clave especificada en el registro de recursos.</span><span class="sxs-lookup"><span data-stu-id="8a0a7-150">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="8a0a7-151">Los valores asignados se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8a0a7-151">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="8a0a7-152">Value</span><span class="sxs-lookup"><span data-stu-id="8a0a7-152">Value</span></span>                                                                                                | <span data-ttu-id="8a0a7-153">Significado</span><span class="sxs-lookup"><span data-stu-id="8a0a7-153">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="8a0a7-154"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="8a0a7-154"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="8a0a7-155">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="8a0a7-155">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="8a0a7-156"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="8a0a7-156"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="8a0a7-157">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="8a0a7-157">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="8a0a7-158"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="8a0a7-158"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="8a0a7-159">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="8a0a7-159">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="8a0a7-160"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="8a0a7-160"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="8a0a7-161">Criptografía de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="8a0a7-161">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8a0a7-162">*PublicKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8a0a7-162">*PublicKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a0a7-163">Clave pública, representada en base 64 como se describe en el Apéndice A de RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="8a0a7-163">Public key, represented in base 64 as described in Appendix A of RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="8a0a7-164">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="8a0a7-164">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="8a0a7-165">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="8a0a7-165">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a0a7-166">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8a0a7-166">Return value</span></span>

<span data-ttu-id="8a0a7-167">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8a0a7-167">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a0a7-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a0a7-168">Requirements</span></span>



| <span data-ttu-id="8a0a7-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a0a7-169">Requirement</span></span> | <span data-ttu-id="8a0a7-170">Value</span><span class="sxs-lookup"><span data-stu-id="8a0a7-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a0a7-171">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a0a7-171">Minimum supported client</span></span><br/> | <span data-ttu-id="8a0a7-172">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8a0a7-172">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8a0a7-173">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a0a7-173">Minimum supported server</span></span><br/> | <span data-ttu-id="8a0a7-174">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8a0a7-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8a0a7-175">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8a0a7-175">Namespace</span></span><br/>                | <span data-ttu-id="8a0a7-176">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="8a0a7-176">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="8a0a7-177">MOF</span><span class="sxs-lookup"><span data-stu-id="8a0a7-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a0a7-178"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a0a7-178"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a0a7-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a0a7-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a0a7-180">**El \_ KEYType de MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="8a0a7-180">**MicrosoftDNS\_KEYType**</span></span>](microsoftdns-keytype.md)
</dt> <dt>

[<span data-ttu-id="8a0a7-181">**Método Modify de la \_ clase MicrosoftDNS KEYType**</span><span class="sxs-lookup"><span data-stu-id="8a0a7-181">**Modify Method of the MicrosoftDNS\_KEYType Class**</span></span>](microsoftdns-keytype-modify.md)
</dt> <dt>

[<span data-ttu-id="8a0a7-182">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="8a0a7-182">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





