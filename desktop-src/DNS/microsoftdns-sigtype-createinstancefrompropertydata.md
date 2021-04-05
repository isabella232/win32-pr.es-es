---
title: Método CreateInstanceFromPropertyData de la clase MicrosoftDNS_SIGType
description: El método CreateInstanceFromPropertyData crea una instancia de un registro de recursos de firma (SIG).
ms.assetid: 8e83e56f-d2b3-4b71-be70-7d2640d49845
keywords:
- CreateInstanceFromPropertyData el método DNS
- Método CreateInstanceFromPropertyData DNS, clase MicrosoftDNS_SIGType
- MicrosoftDNS_SIGType de clase DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c21660572d9557e6425b459c5694a7eeee4722cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078993"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_sigtype-class"></a><span data-ttu-id="24145-106">Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS SIGType</span><span class="sxs-lookup"><span data-stu-id="24145-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_SIGType class</span></span>

<span data-ttu-id="24145-107">El método **CreateInstanceFromPropertyData** crea una instancia de un registro de recursos de firma (SIG).</span><span class="sxs-lookup"><span data-stu-id="24145-107">The **CreateInstanceFromPropertyData** method instantiates a Signature (SIG) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="24145-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="24145-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               TypeCovered,
  [in]           uint16               Algorithm,
  [in]           uint16               Labels,
  [in]           uint32               OriginalTTL,
  [in]           uint32               SignatureExpiration,
  [in]           uint32               SignatureInception,
  [in]           uint16               KeyTag,
  [in]           string               SignerName,
  [in]           string               Signature,
  [out, ref]     MicrosoftDNS_SIGType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="24145-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="24145-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24145-110">*DnsServerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="24145-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24145-111">FQDN o dirección IP del servidor DNS que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="24145-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="24145-112">*ContainerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="24145-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24145-113">Nombre del contenedor de la zona, la memoria caché o la instancia de RootHints que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="24145-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="24145-114">*Nombrepropietario* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="24145-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24145-115">Nombre del propietario del RR.</span><span class="sxs-lookup"><span data-stu-id="24145-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="24145-116">*RecordClass* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="24145-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="24145-117">Clase del RR.</span><span class="sxs-lookup"><span data-stu-id="24145-117">Class of the RR.</span></span> <span data-ttu-id="24145-118">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="24145-118">Default value is 1.</span></span> <span data-ttu-id="24145-119">Los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="24145-119">The following values are valid.</span></span>



| <span data-ttu-id="24145-120">Value</span><span class="sxs-lookup"><span data-stu-id="24145-120">Value</span></span>                                                                                                | <span data-ttu-id="24145-121">Significado</span><span class="sxs-lookup"><span data-stu-id="24145-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="24145-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="24145-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="24145-123">EN (Internet)</span><span class="sxs-lookup"><span data-stu-id="24145-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="24145-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="24145-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="24145-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="24145-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="24145-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="24145-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="24145-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="24145-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="24145-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="24145-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="24145-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="24145-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="24145-130">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="24145-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="24145-131">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="24145-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="24145-132">*TypeCovered* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="24145-132">*TypeCovered* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24145-133">Tipo de RR que se trata en este SIG.</span><span class="sxs-lookup"><span data-stu-id="24145-133">Type of RR covered by this SIG.</span></span>

</dd> <dt>

<span data-ttu-id="24145-134">*Algoritmo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="24145-134">*Algorithm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24145-135">Algoritmo usado con la clave especificada en el registro de recursos.</span><span class="sxs-lookup"><span data-stu-id="24145-135">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="24145-136">Los valores asignados se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="24145-136">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="24145-137">Value</span><span class="sxs-lookup"><span data-stu-id="24145-137">Value</span></span>                                                                                                | <span data-ttu-id="24145-138">Significado</span><span class="sxs-lookup"><span data-stu-id="24145-138">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="24145-139"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="24145-139"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="24145-140">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="24145-140">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="24145-141"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="24145-141"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="24145-142">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="24145-142">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="24145-143"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="24145-143"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="24145-144">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="24145-144">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="24145-145"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="24145-145"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="24145-146">Criptografía de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="24145-146">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="24145-147">*Etiquetas* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="24145-147">*Labels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24145-148">Recuento sin signo de etiquetas en el nombre de propietario del RR de firma original.</span><span class="sxs-lookup"><span data-stu-id="24145-148">Unsigned count of labels in the original SIG RR owner name.</span></span> <span data-ttu-id="24145-149">El recuento no incluye la etiqueta NULL para la raíz ni ningún carácter comodín inicial.</span><span class="sxs-lookup"><span data-stu-id="24145-149">The count does not include the NULL label for the root, nor any initial wildcards.</span></span>

</dd> <dt>

<span data-ttu-id="24145-150">*OriginalTTL* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="24145-150">*OriginalTTL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24145-151">TTL del conjunto de RR firmado por el SIG.</span><span class="sxs-lookup"><span data-stu-id="24145-151">TTL of the RR set signed by the SIG.</span></span>

</dd> <dt>

<span data-ttu-id="24145-152">*SignatureExpiration* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="24145-152">*SignatureExpiration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24145-153">Fecha de expiración de la firma, expresada en segundos desde el comienzo del 1 de enero de 1970, hora del meridiano de Greenwich (GMT), excluyendo los segundos bisiestos.</span><span class="sxs-lookup"><span data-stu-id="24145-153">Signature expiration date, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="24145-154">*SignatureInception* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="24145-154">*SignatureInception* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24145-155">Fecha y hora en las que la firma es válida, expresada en segundos desde el comienzo del 1 de enero de 1970, hora del meridiano de Greenwich (GMT), excluyendo los segundos bisiestos.</span><span class="sxs-lookup"><span data-stu-id="24145-155">Date and time at which the Signature becomes valid, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="24145-156">*KeyTag* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="24145-156">*KeyTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24145-157">Método usado para elegir una clave que comprueba un SIG.</span><span class="sxs-lookup"><span data-stu-id="24145-157">Method used to choose a key that verifies an SIG.</span></span> <span data-ttu-id="24145-158">Vea RFC 2535, Apéndice C para el método usado para calcular un KeyTag.</span><span class="sxs-lookup"><span data-stu-id="24145-158">See RFC 2535, Appendix C for the method used to calculate a KeyTag.</span></span>

</dd> <dt>

<span data-ttu-id="24145-159">*SignerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="24145-159">*SignerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24145-160">Nombre de dominio del firmante que generó el RR SIG.</span><span class="sxs-lookup"><span data-stu-id="24145-160">Domain name of the signer that generated the SIG RR.</span></span>

</dd> <dt>

<span data-ttu-id="24145-161">*Firma* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="24145-161">*Signature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24145-162">Firma, representada en base 64, con el formato definido en RFC 2535, Apéndice A.</span><span class="sxs-lookup"><span data-stu-id="24145-162">Signature, represented in base 64, formatted as defined in RFC 2535, Appendix A.</span></span>

</dd> <dt>

<span data-ttu-id="24145-163">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="24145-163">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="24145-164">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="24145-164">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24145-165">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="24145-165">Return value</span></span>

<span data-ttu-id="24145-166">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="24145-166">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="24145-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24145-167">Requirements</span></span>



| <span data-ttu-id="24145-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="24145-168">Requirement</span></span> | <span data-ttu-id="24145-169">Value</span><span class="sxs-lookup"><span data-stu-id="24145-169">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="24145-170">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24145-170">Minimum supported client</span></span><br/> | <span data-ttu-id="24145-171">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="24145-171">None supported</span></span><br/>                                                              |
| <span data-ttu-id="24145-172">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24145-172">Minimum supported server</span></span><br/> | <span data-ttu-id="24145-173">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="24145-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="24145-174">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="24145-174">Namespace</span></span><br/>                | <span data-ttu-id="24145-175">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="24145-175">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="24145-176">MOF</span><span class="sxs-lookup"><span data-stu-id="24145-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24145-177"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="24145-177"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24145-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="24145-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24145-179">**MicrosoftDNS \_ SIGType**</span><span class="sxs-lookup"><span data-stu-id="24145-179">**MicrosoftDNS\_SIGType**</span></span>](microsoftdns-sigtype.md)
</dt> <dt>

[<span data-ttu-id="24145-180">**Método Modify de la \_ clase MicrosoftDNS SIGType**</span><span class="sxs-lookup"><span data-stu-id="24145-180">**Modify Method of the MicrosoftDNS\_SIGType Class**</span></span>](microsoftdns-sigtype-modify.md)
</dt> <dt>

[<span data-ttu-id="24145-181">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="24145-181">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





