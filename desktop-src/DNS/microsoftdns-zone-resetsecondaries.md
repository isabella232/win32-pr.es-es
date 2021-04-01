---
title: Método ResetSecondaries de la clase MicrosoftDNS_Zone
description: El método ResetSecondaries restablece las direcciones IP de los servidores DNS secundarios de la zona.
ms.assetid: b9a47714-f180-40cf-831a-f59e804a4ca2
keywords:
- ResetSecondaries el método DNS
- Método ResetSecondaries DNS, clase MicrosoftDNS_Zone
- MicrosoftDNS_Zone de clase DNS, método ResetSecondaries
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ResetSecondaries
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a78d65b2153782c38d6d91d34f642860e896ed1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996711"
---
# <a name="resetsecondaries-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="7aebc-106">Método ResetSecondaries de la \_ clase de zona MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="7aebc-106">ResetSecondaries method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="7aebc-107">El método **ResetSecondaries** restablece las direcciones IP de los servidores DNS secundarios de la zona.</span><span class="sxs-lookup"><span data-stu-id="7aebc-107">The **ResetSecondaries** method resets the IP addresses for secondary DNS Servers in the zone.</span></span>

## <a name="syntax"></a><span data-ttu-id="7aebc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7aebc-108">Syntax</span></span>


```mof
void ResetSecondaries(
  [in]       string            SecondaryServers[],
  [in]       uint32            SecureSecondaries,
  [in]       string            NotifyServers[],
  [in]       uint32            Notify,
  [out, ref] MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a><span data-ttu-id="7aebc-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7aebc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7aebc-110">*SecondaryServers* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7aebc-110">*SecondaryServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7aebc-111">Matriz de direcciones IP para los servidores DNS secundarios.</span><span class="sxs-lookup"><span data-stu-id="7aebc-111">Array of IP addresses for secondary DNS Servers.</span></span>

</dd> <dt>

<span data-ttu-id="7aebc-112">*SecureSecondaries* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7aebc-112">*SecureSecondaries* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7aebc-113">Especifica la seguridad que se va a aplicar y debe ser una de las siguientes:</span><span class="sxs-lookup"><span data-stu-id="7aebc-113">Specifies the security to be applied and must be one of the following:</span></span>

-   <span data-ttu-id="7aebc-114">ZONA \_ SECSECURE \_ sin \_ seguridad</span><span class="sxs-lookup"><span data-stu-id="7aebc-114">ZONE\_SECSECURE\_NO\_SECURITY</span></span>
-   <span data-ttu-id="7aebc-115">\_solo zona SECSECURE \_ NS \_</span><span class="sxs-lookup"><span data-stu-id="7aebc-115">ZONE\_SECSECURE\_NS\_ONLY</span></span>
-   <span data-ttu-id="7aebc-116">\_ \_ solo lista de SECSECURE de zona \_</span><span class="sxs-lookup"><span data-stu-id="7aebc-116">ZONE\_SECSECURE\_LIST\_ONLY</span></span>
-   <span data-ttu-id="7aebc-117">ZONA \_ SECSECURE \_ no \_ XFR</span><span class="sxs-lookup"><span data-stu-id="7aebc-117">ZONE\_SECSECURE\_NO\_XFR</span></span>

</dd> <dt>

<span data-ttu-id="7aebc-118">*NotifyServers* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7aebc-118">*NotifyServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7aebc-119">Dirección IP de los servidores DNS a los que se notificará cuando cambie la zona.</span><span class="sxs-lookup"><span data-stu-id="7aebc-119">IP address of DNS Servers to be notified when the zone changes.</span></span>

</dd> <dt>

<span data-ttu-id="7aebc-120">*Notificar* \[ a de\]</span><span class="sxs-lookup"><span data-stu-id="7aebc-120">*Notify* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7aebc-121">Configuración de notificación y debe ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="7aebc-121">Notification setting and must be one of the following:</span></span>

-   <span data-ttu-id="7aebc-122">notificación de zona \_ \_ desactivada</span><span class="sxs-lookup"><span data-stu-id="7aebc-122">ZONE\_NOTIFY\_OFF</span></span>
-   <span data-ttu-id="7aebc-123">ZONA de \_ notificación de \_ todos los \_ secundarios</span><span class="sxs-lookup"><span data-stu-id="7aebc-123">ZONE\_NOTIFY\_ALL\_SECONDARIES</span></span>
-   <span data-ttu-id="7aebc-124">\_solo lista de notificaciones de zona \_ \_</span><span class="sxs-lookup"><span data-stu-id="7aebc-124">ZONE\_NOTIFY\_LIST\_ONLY</span></span>

</dd> <dt>

<span data-ttu-id="7aebc-125">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="7aebc-125">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="7aebc-126">RR de tipo [**la \_ zona MicrosoftDNS**](microsoftdns-zone.md).</span><span class="sxs-lookup"><span data-stu-id="7aebc-126">RR of type [**MicrosoftDNS\_Zone**](microsoftdns-zone.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7aebc-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7aebc-127">Return value</span></span>

<span data-ttu-id="7aebc-128">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="7aebc-128">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7aebc-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7aebc-129">Requirements</span></span>



| <span data-ttu-id="7aebc-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="7aebc-130">Requirement</span></span> | <span data-ttu-id="7aebc-131">Value</span><span class="sxs-lookup"><span data-stu-id="7aebc-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7aebc-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7aebc-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7aebc-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7aebc-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="7aebc-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7aebc-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7aebc-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7aebc-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7aebc-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7aebc-136">Namespace</span></span><br/>                | <span data-ttu-id="7aebc-137">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="7aebc-137">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="7aebc-138">MOF</span><span class="sxs-lookup"><span data-stu-id="7aebc-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7aebc-139"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7aebc-139"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7aebc-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="7aebc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7aebc-141">**\_Zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="7aebc-141">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="7aebc-142">**Método AgeAllRecords de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="7aebc-142">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="7aebc-143">**Método ChangeZoneType de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="7aebc-143">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="7aebc-144">**Método CreateZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="7aebc-144">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="7aebc-145">**Método ForceRefresh de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="7aebc-145">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="7aebc-146">**Método GetDistinguishedName de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="7aebc-146">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="7aebc-147">**Método PauseZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="7aebc-147">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="7aebc-148">**Método ReloadZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="7aebc-148">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="7aebc-149">**Método ResumeZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="7aebc-149">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="7aebc-150">**Método UpdateFromDS de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="7aebc-150">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="7aebc-151">**Método WriteBackZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="7aebc-151">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





