---
title: Método CreateInstanceFromPropertyData de la clase MicrosoftDNS_MXType
description: El método CreateInstanceFromPropertyData crea una instancia de un registro de recursos de intercambio de correo (MR).
ms.assetid: 5724b14a-bb64-460c-ac49-28bac85b8620
keywords:
- CreateInstanceFromPropertyData el método DNS
- Método CreateInstanceFromPropertyData DNS, clase MicrosoftDNS_MXType
- MicrosoftDNS_MXType de clase DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8154e8ccdc6ac18824e2d56597ac8e0f186f3912
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150343"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mxtype-class"></a><span data-ttu-id="338a5-106">Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS MXType</span><span class="sxs-lookup"><span data-stu-id="338a5-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MXType class</span></span>

<span data-ttu-id="338a5-107">El método **CreateInstanceFromPropertyData** crea una instancia de un registro de recursos de intercambio de correo (MR).</span><span class="sxs-lookup"><span data-stu-id="338a5-107">The **CreateInstanceFromPropertyData** method instantiates a Mail Exchanger (MR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="338a5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="338a5-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           uint16              Preference,
  [in]           string              MailExchange,
  [out, ref]     MicrosoftDNS_MXType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="338a5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="338a5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="338a5-110">*DnsServerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="338a5-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="338a5-111">FQDN o dirección IP del servidor DNS que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="338a5-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="338a5-112">*ContainerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="338a5-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="338a5-113">Nombre del contenedor de la zona, la memoria caché o la instancia de RootHints que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="338a5-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="338a5-114">*Nombrepropietario* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="338a5-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="338a5-115">Nombre del propietario del RR.</span><span class="sxs-lookup"><span data-stu-id="338a5-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="338a5-116">*RecordClass* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="338a5-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="338a5-117">Clase del RR.</span><span class="sxs-lookup"><span data-stu-id="338a5-117">Class of the RR.</span></span> <span data-ttu-id="338a5-118">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="338a5-118">Default value is 1.</span></span> <span data-ttu-id="338a5-119">Los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="338a5-119">The following values are valid.</span></span>



| <span data-ttu-id="338a5-120">Value</span><span class="sxs-lookup"><span data-stu-id="338a5-120">Value</span></span>                                                                                                | <span data-ttu-id="338a5-121">Significado</span><span class="sxs-lookup"><span data-stu-id="338a5-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="338a5-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="338a5-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="338a5-123">EN (Internet)</span><span class="sxs-lookup"><span data-stu-id="338a5-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="338a5-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="338a5-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="338a5-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="338a5-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="338a5-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="338a5-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="338a5-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="338a5-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="338a5-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="338a5-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="338a5-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="338a5-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="338a5-130">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="338a5-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="338a5-131">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="338a5-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="338a5-132">*Preferencia* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="338a5-132">*Preference* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="338a5-133">Preferencia asignada a este RR entre otros en el mismo propietario.</span><span class="sxs-lookup"><span data-stu-id="338a5-133">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="338a5-134">Se prefieren los valores inferiores.</span><span class="sxs-lookup"><span data-stu-id="338a5-134">Lower values are preferred.</span></span>

</dd> <dt>

<span data-ttu-id="338a5-135">*MailExchange* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="338a5-135">*MailExchange* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="338a5-136">FQDN que especifica un host que desea actuar como intercambio de correo electrónico para el nombre del propietario.</span><span class="sxs-lookup"><span data-stu-id="338a5-136">FQDN specifying a host willing to act as a mail exchange for the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="338a5-137">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="338a5-137">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="338a5-138">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="338a5-138">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="338a5-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="338a5-139">Return value</span></span>

<span data-ttu-id="338a5-140">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="338a5-140">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="338a5-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="338a5-141">Requirements</span></span>



| <span data-ttu-id="338a5-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="338a5-142">Requirement</span></span> | <span data-ttu-id="338a5-143">Value</span><span class="sxs-lookup"><span data-stu-id="338a5-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="338a5-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="338a5-144">Minimum supported client</span></span><br/> | <span data-ttu-id="338a5-145">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="338a5-145">None supported</span></span><br/>                                                              |
| <span data-ttu-id="338a5-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="338a5-146">Minimum supported server</span></span><br/> | <span data-ttu-id="338a5-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="338a5-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="338a5-148">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="338a5-148">Namespace</span></span><br/>                | <span data-ttu-id="338a5-149">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="338a5-149">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="338a5-150">MOF</span><span class="sxs-lookup"><span data-stu-id="338a5-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="338a5-151"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="338a5-151"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="338a5-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="338a5-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="338a5-153">**MicrosoftDNS \_ MXType**</span><span class="sxs-lookup"><span data-stu-id="338a5-153">**MicrosoftDNS\_MXType**</span></span>](microsoftdns-mxtype.md)
</dt> <dt>

[<span data-ttu-id="338a5-154">**Método Modify de la \_ clase MicrosoftDNS MXType**</span><span class="sxs-lookup"><span data-stu-id="338a5-154">**Modify Method of the MicrosoftDNS\_MXType Class**</span></span>](microsoftdns-mxtype-modify.md)
</dt> <dt>

[<span data-ttu-id="338a5-155">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="338a5-155">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





