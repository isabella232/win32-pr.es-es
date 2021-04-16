---
title: Método CreateInstanceFromPropertyData de la clase MicrosoftDNS_ATMAType
description: El método CreateInstanceFromPropertyData crea una instancia de un registro de recursos de dirección ATM en nombre (ATMA).
ms.assetid: 0f3270fe-40d0-43f7-b4fc-95d96f9dd9f9
keywords:
- CreateInstanceFromPropertyData el método DNS
- Método CreateInstanceFromPropertyData DNS, clase MicrosoftDNS_ATMAType
- MicrosoftDNS_ATMAType de clase DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39fada3759e6384ae6f42a78bd132b9b8ad16f35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656538"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_atmatype-class"></a><span data-ttu-id="e9c08-106">Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS ATMAType</span><span class="sxs-lookup"><span data-stu-id="e9c08-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_ATMAType class</span></span>

<span data-ttu-id="e9c08-107">El método **CreateInstanceFromPropertyData** crea una instancia de un registro de recursos de dirección ATM en nombre (Atma).</span><span class="sxs-lookup"><span data-stu-id="e9c08-107">The **CreateInstanceFromPropertyData** method instantiates an ATM Address to Name (ATMA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9c08-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e9c08-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           uint16                Format,
  [in]           string                ATMAddress,
  [out, ref]     MicrosoftDNS_ATMAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="e9c08-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e9c08-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9c08-110">*DnsServerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e9c08-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9c08-111">FQDN o dirección IP del servidor DNS que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="e9c08-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="e9c08-112">*ContainerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e9c08-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9c08-113">Nombre del contenedor de la zona, la memoria caché o la instancia de RootHints que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="e9c08-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="e9c08-114">*Nombrepropietario* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e9c08-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9c08-115">Nombre del propietario del RR.</span><span class="sxs-lookup"><span data-stu-id="e9c08-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="e9c08-116">*RecordClass* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e9c08-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e9c08-117">Clase del RR.</span><span class="sxs-lookup"><span data-stu-id="e9c08-117">Class of the RR.</span></span> <span data-ttu-id="e9c08-118">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="e9c08-118">Default value is 1.</span></span> <span data-ttu-id="e9c08-119">Los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="e9c08-119">The following values are valid.</span></span>



| <span data-ttu-id="e9c08-120">Value</span><span class="sxs-lookup"><span data-stu-id="e9c08-120">Value</span></span>                                                                                                | <span data-ttu-id="e9c08-121">Significado</span><span class="sxs-lookup"><span data-stu-id="e9c08-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="e9c08-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="e9c08-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="e9c08-123">EN (Internet)</span><span class="sxs-lookup"><span data-stu-id="e9c08-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="e9c08-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="e9c08-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="e9c08-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="e9c08-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="e9c08-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="e9c08-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="e9c08-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="e9c08-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="e9c08-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="e9c08-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="e9c08-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="e9c08-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="e9c08-130">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e9c08-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e9c08-131">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="e9c08-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="e9c08-132">*Formato* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e9c08-132">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9c08-133">Formato de dirección ATM.</span><span class="sxs-lookup"><span data-stu-id="e9c08-133">ATM address format.</span></span> <span data-ttu-id="e9c08-134">Dos valores posibles para FORMAT son: 0, que indica el formato de dirección del sistema de finalización (AESA) de ATM y 1 que indica el formato E. 164.</span><span class="sxs-lookup"><span data-stu-id="e9c08-134">Two possible values for FORMAT are: 0 indicating ATM End System Address (AESA) format and 1 indicating E.164 format.</span></span>

</dd> <dt>

<span data-ttu-id="e9c08-135">*ATMAddress* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e9c08-135">*ATMAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9c08-136">Cadena de longitud variable de octetos que contiene la dirección ATM del nodo/propietario al que pertenece este RR.</span><span class="sxs-lookup"><span data-stu-id="e9c08-136">Variable length string of octets containing the ATM address of the node/owner to which this RR pertains.</span></span> <span data-ttu-id="e9c08-137">Los primeros cuatro bytes de la matriz se utilizan para almacenar el tamaño de la cadena de octeto.</span><span class="sxs-lookup"><span data-stu-id="e9c08-137">The first four bytes of the array are used to store the size of the octet string.</span></span> <span data-ttu-id="e9c08-138">El byte más significativo se almacena en byte 0.</span><span class="sxs-lookup"><span data-stu-id="e9c08-138">The most significant byte is stored in byte 0.</span></span>

</dd> <dt>

<span data-ttu-id="e9c08-139">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="e9c08-139">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e9c08-140">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="e9c08-140">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9c08-141">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e9c08-141">Return value</span></span>

<span data-ttu-id="e9c08-142">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e9c08-142">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9c08-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9c08-143">Requirements</span></span>



| <span data-ttu-id="e9c08-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9c08-144">Requirement</span></span> | <span data-ttu-id="e9c08-145">Value</span><span class="sxs-lookup"><span data-stu-id="e9c08-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9c08-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9c08-146">Minimum supported client</span></span><br/> | <span data-ttu-id="e9c08-147">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e9c08-147">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e9c08-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9c08-148">Minimum supported server</span></span><br/> | <span data-ttu-id="e9c08-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e9c08-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e9c08-150">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e9c08-150">Namespace</span></span><br/>                | <span data-ttu-id="e9c08-151">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="e9c08-151">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="e9c08-152">MOF</span><span class="sxs-lookup"><span data-stu-id="e9c08-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9c08-153"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9c08-153"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9c08-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9c08-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9c08-155">**MicrosoftDNS \_ ATMAType**</span><span class="sxs-lookup"><span data-stu-id="e9c08-155">**MicrosoftDNS\_ATMAType**</span></span>](microsoftdns-atmatype.md)
</dt> <dt>

[<span data-ttu-id="e9c08-156">**Método Modify de la \_ clase MicrosoftDNS ATMAType**</span><span class="sxs-lookup"><span data-stu-id="e9c08-156">**Modify Method of the MicrosoftDNS\_ATMAType Class**</span></span>](microsoftdns-atmatype-modify.md)
</dt> <dt>

[<span data-ttu-id="e9c08-157">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="e9c08-157">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





