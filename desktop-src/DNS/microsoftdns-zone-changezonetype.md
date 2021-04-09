---
title: Método ChangeZoneType de la clase MicrosoftDNS_Zone
description: El método ChangeZoneType cambia el tipo de una zona.
ms.assetid: a0a9f495-fdbb-4258-a313-ee9551da762f
keywords:
- ChangeZoneType el método DNS
- Método ChangeZoneType DNS, clase MicrosoftDNS_Zone
- MicrosoftDNS_Zone de clase DNS, método ChangeZoneType
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ChangeZoneType
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1611eda876532f32534e24257478b3a5986af3aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079250"
---
# <a name="changezonetype-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="6473b-106">Método ChangeZoneType de la \_ clase de zona MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="6473b-106">ChangeZoneType method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="6473b-107">El método **ChangeZoneType** cambia el tipo de una zona.</span><span class="sxs-lookup"><span data-stu-id="6473b-107">The **ChangeZoneType** method changes the type of a zone.</span></span>

## <a name="syntax"></a><span data-ttu-id="6473b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6473b-108">Syntax</span></span>


```mof
void ChangeZoneType(
  [in]           uint32            ZoneType,
  [in, optional] string            DataFileName,
  [in, optional] string            IpAddr[],
  [in, optional] string            AdminEmailName,
  [out, ref]     MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a><span data-ttu-id="6473b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6473b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6473b-110">*ZoneType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6473b-110">*ZoneType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6473b-111">Tipo de zona.</span><span class="sxs-lookup"><span data-stu-id="6473b-111">Type of zone.</span></span> <span data-ttu-id="6473b-112">Los valores válidos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="6473b-112">Valid values are the following:</span></span>



| <span data-ttu-id="6473b-113">Value</span><span class="sxs-lookup"><span data-stu-id="6473b-113">Value</span></span>                                                                        | <span data-ttu-id="6473b-114">Significado</span><span class="sxs-lookup"><span data-stu-id="6473b-114">Meaning</span></span>                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="6473b-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6473b-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="6473b-116">Zona principal.</span><span class="sxs-lookup"><span data-stu-id="6473b-116">Primary zone.</span></span><br/>   |
| <dl> <span data-ttu-id="6473b-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6473b-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="6473b-118">Zona secundaria.</span><span class="sxs-lookup"><span data-stu-id="6473b-118">Secondary zone.</span></span><br/> |
| <dl> <span data-ttu-id="6473b-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6473b-119"><dt>2</dt></span></span> </dl> | <span data-ttu-id="6473b-120">Zona de rutas internas.</span><span class="sxs-lookup"><span data-stu-id="6473b-120">Stub zone.</span></span><br/>      |
| <dl> <span data-ttu-id="6473b-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="6473b-121"><dt>3</dt></span></span> </dl> | <span data-ttu-id="6473b-122">Reenviador de zona.</span><span class="sxs-lookup"><span data-stu-id="6473b-122">Zone forwarder.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6473b-123">*Nombre de archivo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="6473b-123">*DataFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6473b-124">Nombre del archivo de datos asociado a la zona.</span><span class="sxs-lookup"><span data-stu-id="6473b-124">Name of the data file associated with the zone.</span></span>

</dd> <dt>

<span data-ttu-id="6473b-125">*DirIP* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="6473b-125">*IpAddr* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6473b-126">Dirección IP del servidor DNS de maestro para la zona.</span><span class="sxs-lookup"><span data-stu-id="6473b-126">IP address of the mater DNS Server for the zone.</span></span>

</dd> <dt>

<span data-ttu-id="6473b-127">*AdminEmailName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="6473b-127">*AdminEmailName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6473b-128">Dirección de correo electrónico del administrador responsable de la zona.</span><span class="sxs-lookup"><span data-stu-id="6473b-128">Email address of the administrator responsible for the zone.</span></span>

</dd> <dt>

<span data-ttu-id="6473b-129">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="6473b-129">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="6473b-130">RR de tipo **la \_ zona MicrosoftDns**.</span><span class="sxs-lookup"><span data-stu-id="6473b-130">RR of type **MicrosoftDns\_Zone**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6473b-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6473b-131">Return value</span></span>

<span data-ttu-id="6473b-132">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6473b-132">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6473b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6473b-133">Requirements</span></span>



| <span data-ttu-id="6473b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="6473b-134">Requirement</span></span> | <span data-ttu-id="6473b-135">Value</span><span class="sxs-lookup"><span data-stu-id="6473b-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6473b-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6473b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6473b-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6473b-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6473b-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6473b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6473b-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6473b-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6473b-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6473b-140">Namespace</span></span><br/>                | <span data-ttu-id="6473b-141">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="6473b-141">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="6473b-142">MOF</span><span class="sxs-lookup"><span data-stu-id="6473b-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6473b-143"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6473b-143"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6473b-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="6473b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6473b-145">**\_Zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6473b-145">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="6473b-146">**Método AgeAllRecords de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6473b-146">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="6473b-147">**Método CreateZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6473b-147">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="6473b-148">**Método ForceRefresh de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6473b-148">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="6473b-149">**Método GetDistinguishedName de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6473b-149">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="6473b-150">**Método PauseZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6473b-150">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="6473b-151">**Método ReloadZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6473b-151">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="6473b-152">**Método ResetSecondaries de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6473b-152">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="6473b-153">**Método ResumeZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6473b-153">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="6473b-154">**Método UpdateFromDS de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6473b-154">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="6473b-155">**Método WriteBackZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6473b-155">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





