---
title: Método UpdateFromDS de la clase MicrosoftDNS_Zone
description: El método UpdateFromDS fuerza una actualización de la zona desde el servicio de directorio (DS).
ms.assetid: 471f0754-1221-4d1d-8ffd-36c1ab54b7e5
keywords:
- UpdateFromDS el método DNS
- Método UpdateFromDS DNS, clase MicrosoftDNS_Zone
- MicrosoftDNS_Zone de clase DNS, método UpdateFromDS
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.UpdateFromDS
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8fd0ba4db9b182379ce2ec93508c7a3bab354a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151249"
---
# <a name="updatefromds-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="653cb-106">Método UpdateFromDS de la \_ clase de zona MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="653cb-106">UpdateFromDS method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="653cb-107">El método **UpdateFromDS** fuerza una actualización de la zona desde el servicio de directorio (DS).</span><span class="sxs-lookup"><span data-stu-id="653cb-107">The **UpdateFromDS** method forces an update of the zone from the Directory Service (DS).</span></span>

## <a name="syntax"></a><span data-ttu-id="653cb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="653cb-108">Syntax</span></span>


```mof
void UpdateFromDS();
```



## <a name="parameters"></a><span data-ttu-id="653cb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="653cb-109">Parameters</span></span>

<span data-ttu-id="653cb-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="653cb-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="653cb-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="653cb-111">Return value</span></span>

<span data-ttu-id="653cb-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="653cb-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="653cb-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="653cb-113">Remarks</span></span>

<span data-ttu-id="653cb-114">Para ejecutar correctamente este método, ZoneType debe ser cero y la zona debe estar almacenada en el DS.</span><span class="sxs-lookup"><span data-stu-id="653cb-114">In order to successfully execute this method, the ZoneType must be zero, and the zone must be stored on the DS.</span></span>

## <a name="requirements"></a><span data-ttu-id="653cb-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="653cb-115">Requirements</span></span>



| <span data-ttu-id="653cb-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="653cb-116">Requirement</span></span> | <span data-ttu-id="653cb-117">Value</span><span class="sxs-lookup"><span data-stu-id="653cb-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="653cb-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="653cb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="653cb-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="653cb-119">None supported</span></span><br/>                                                              |
| <span data-ttu-id="653cb-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="653cb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="653cb-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="653cb-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="653cb-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="653cb-122">Namespace</span></span><br/>                | <span data-ttu-id="653cb-123">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="653cb-123">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="653cb-124">MOF</span><span class="sxs-lookup"><span data-stu-id="653cb-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="653cb-125"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="653cb-125"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="653cb-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="653cb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="653cb-127">**\_Zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="653cb-127">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="653cb-128">**Método AgeAllRecords de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="653cb-128">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="653cb-129">**Método ChangeZoneType de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="653cb-129">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="653cb-130">**Método CreateZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="653cb-130">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="653cb-131">**Método ForceRefresh de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="653cb-131">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="653cb-132">**Método GetDistinguishedName de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="653cb-132">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="653cb-133">**Método PauseZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="653cb-133">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="653cb-134">**Método ReloadZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="653cb-134">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="653cb-135">**Método ResetSecondaries de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="653cb-135">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="653cb-136">**Método ResumeZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="653cb-136">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="653cb-137">**Método WriteBackZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="653cb-137">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





