---
title: Método CreateZone de la clase MicrosoftDNS_Zone
description: El método CreateZone crea una zona DNS.
ms.assetid: 55756284-20ef-4d38-a8d9-357f53a6fa4d
keywords:
- CreateZone el método DNS
- Método CreateZone DNS, clase MicrosoftDNS_Zone
- MicrosoftDNS_Zone de clase DNS, método CreateZone
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.CreateZone
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7e3780db9036e0fd7c87d91c769c3c6f5c6aaf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079548"
---
# <a name="createzone-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="faf5b-106">Método CreateZone de la \_ clase de zona MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="faf5b-106">CreateZone method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="faf5b-107">El método **CreateZone** crea una zona DNS.</span><span class="sxs-lookup"><span data-stu-id="faf5b-107">The **CreateZone** method creates a DNS zone.</span></span>

## <a name="syntax"></a><span data-ttu-id="faf5b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="faf5b-108">Syntax</span></span>


```mof
void CreateZone(
  [in]           string            ZoneName,
  [in]           uint32            ZoneType,
  [in]           boolean           DsIntegrated,
  [in, optional] string            DataFileName,
  [in, optional] string            IpAddr[],
  [in, optional] string            AdminEmailName,
  [out, ref]     MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a><span data-ttu-id="faf5b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="faf5b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="faf5b-110">*Nombre_zona* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="faf5b-110">*ZoneName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faf5b-111">Cadena que representa el nombre de la zona.</span><span class="sxs-lookup"><span data-stu-id="faf5b-111">String representing the name of the zone.</span></span>

</dd> <dt>

<span data-ttu-id="faf5b-112">*ZoneType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="faf5b-112">*ZoneType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faf5b-113">Tipo de zona.</span><span class="sxs-lookup"><span data-stu-id="faf5b-113">Type of zone.</span></span> <span data-ttu-id="faf5b-114">Los valores válidos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="faf5b-114">Valid values are the following:</span></span>



| <span data-ttu-id="faf5b-115">Value</span><span class="sxs-lookup"><span data-stu-id="faf5b-115">Value</span></span>                                                                        | <span data-ttu-id="faf5b-116">Significado</span><span class="sxs-lookup"><span data-stu-id="faf5b-116">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="faf5b-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="faf5b-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="faf5b-118">AD integrado.</span><span class="sxs-lookup"><span data-stu-id="faf5b-118">AD integrated.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="faf5b-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="faf5b-119"><dt>2</dt></span></span> </dl> | <span data-ttu-id="faf5b-120">Zona secundaria.</span><span class="sxs-lookup"><span data-stu-id="faf5b-120">Secondary zone.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="faf5b-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="faf5b-121"><dt>3</dt></span></span> </dl> | <span data-ttu-id="faf5b-122">Zona de rutas internas.</span><span class="sxs-lookup"><span data-stu-id="faf5b-122">Stub zone.</span></span><br/> <span data-ttu-id="faf5b-123">**Windows Server 2003:** Este tipo de zona se introduce en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="faf5b-123">**Windows Server 2003:** This zone type is introduced in Windows Server 2003.</span></span><br/>      |
| <dl> <span data-ttu-id="faf5b-124"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="faf5b-124"><dt>4</dt></span></span> </dl> | <span data-ttu-id="faf5b-125">Reenviador de zona.</span><span class="sxs-lookup"><span data-stu-id="faf5b-125">Zone forwarder.</span></span><br/> <span data-ttu-id="faf5b-126">**Windows Server 2003:** Este tipo de zona se introduce en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="faf5b-126">**Windows Server 2003:** This zone type is introduced in Windows Server 2003.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="faf5b-127">*DsIntegrated* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="faf5b-127">*DsIntegrated* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faf5b-128">Indica si los datos de zona se almacenan en el Active Directory o en archivos.</span><span class="sxs-lookup"><span data-stu-id="faf5b-128">Indicates whether zone data is stored in the Active Directory or in files.</span></span> <span data-ttu-id="faf5b-129">Si es TRUE, los datos se almacenan en el Active Directory; Si es FALSE, los datos se almacenan en archivos.</span><span class="sxs-lookup"><span data-stu-id="faf5b-129">If TRUE, the data is stored in the Active Directory; if FALSE, the data is stored in files.</span></span>

</dd> <dt>

<span data-ttu-id="faf5b-130">*Nombre de archivo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="faf5b-130">*DataFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="faf5b-131">Nombre del archivo de datos asociado a la zona.</span><span class="sxs-lookup"><span data-stu-id="faf5b-131">Name of the data file associated with the zone.</span></span>

</dd> <dt>

<span data-ttu-id="faf5b-132">*DirIP* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="faf5b-132">*IpAddr* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="faf5b-133">Dirección IP del servidor DNS maestro de la zona.</span><span class="sxs-lookup"><span data-stu-id="faf5b-133">IP address of the master DNS Server for the zone.</span></span>

</dd> <dt>

<span data-ttu-id="faf5b-134">*AdminEmailName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="faf5b-134">*AdminEmailName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="faf5b-135">Dirección de correo electrónico del administrador responsable de la zona.</span><span class="sxs-lookup"><span data-stu-id="faf5b-135">Email address of the administrator responsible for the zone.</span></span>

</dd> <dt>

<span data-ttu-id="faf5b-136">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="faf5b-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="faf5b-137">RR de tipo **la \_ zona MicrosoftDns**.</span><span class="sxs-lookup"><span data-stu-id="faf5b-137">RR of type **MicrosoftDns\_Zone**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="faf5b-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="faf5b-138">Return value</span></span>

<span data-ttu-id="faf5b-139">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="faf5b-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="faf5b-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="faf5b-140">Requirements</span></span>



| <span data-ttu-id="faf5b-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="faf5b-141">Requirement</span></span> | <span data-ttu-id="faf5b-142">Value</span><span class="sxs-lookup"><span data-stu-id="faf5b-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="faf5b-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="faf5b-143">Minimum supported client</span></span><br/> | <span data-ttu-id="faf5b-144">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="faf5b-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="faf5b-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="faf5b-145">Minimum supported server</span></span><br/> | <span data-ttu-id="faf5b-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="faf5b-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="faf5b-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="faf5b-147">Namespace</span></span><br/>                | <span data-ttu-id="faf5b-148">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="faf5b-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="faf5b-149">MOF</span><span class="sxs-lookup"><span data-stu-id="faf5b-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="faf5b-150"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="faf5b-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faf5b-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="faf5b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faf5b-152">**\_Zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="faf5b-152">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="faf5b-153">**Método AgeAllRecords de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="faf5b-153">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="faf5b-154">**Método ChangeZoneType de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="faf5b-154">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="faf5b-155">**Método ForceRefresh de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="faf5b-155">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="faf5b-156">**Método GetDistinguishedName de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="faf5b-156">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="faf5b-157">**Método PauseZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="faf5b-157">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="faf5b-158">**Método ReloadZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="faf5b-158">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="faf5b-159">**Método ResetSecondaries de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="faf5b-159">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="faf5b-160">**Método ResumeZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="faf5b-160">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="faf5b-161">**Método UpdateFromDS de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="faf5b-161">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="faf5b-162">**Método WriteBackZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="faf5b-162">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





