---
title: Método ForceRefresh de la clase MicrosoftDNS_Zone
description: El método ForceRefresh fuerza una actualización del servidor DNS secundario desde el servidor maestro.
ms.assetid: 8dde1703-53c3-4d1e-bfb3-f6d5d1666740
keywords:
- ForceRefresh el método DNS
- Método ForceRefresh DNS, clase MicrosoftDNS_Zone
- MicrosoftDNS_Zone de clase DNS, método ForceRefresh
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ForceRefresh
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85390230b0a0852ee479bc8b7e396972f6e69080
ms.sourcegitcommit: 03fb201e1ea36e353c335ff063ed993fb5993e61
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105659255"
---
# <a name="forcerefresh-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="c7d43-106">Método ForceRefresh de la \_ clase de zona MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="c7d43-106">ForceRefresh method of the MicrosoftDNS\_Zone class</span></span>

> [!NOTE]
> <span data-ttu-id="c7d43-107">Este artículo contiene referencias al término servidor maestro, un término que Microsoft ya no usa.</span><span class="sxs-lookup"><span data-stu-id="c7d43-107">This article contains references to the term master server, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="c7d43-108">Cuando se quite el término del software, se quitará también del artículo.</span><span class="sxs-lookup"><span data-stu-id="c7d43-108">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="c7d43-109">El método **ForceRefresh** fuerza una actualización del servidor DNS secundario desde el servidor maestro.</span><span class="sxs-lookup"><span data-stu-id="c7d43-109">The **ForceRefresh** method forces an update of the secondary DNS Server from the master server.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7d43-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7d43-110">Syntax</span></span>


```mof
void ForceRefresh();
```



## <a name="parameters"></a><span data-ttu-id="c7d43-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c7d43-111">Parameters</span></span>

<span data-ttu-id="c7d43-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c7d43-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c7d43-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c7d43-113">Return value</span></span>

<span data-ttu-id="c7d43-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c7d43-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7d43-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7d43-115">Requirements</span></span>



| <span data-ttu-id="c7d43-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7d43-116">Requirement</span></span> | <span data-ttu-id="c7d43-117">Value</span><span class="sxs-lookup"><span data-stu-id="c7d43-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7d43-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7d43-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c7d43-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c7d43-119">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c7d43-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7d43-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c7d43-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c7d43-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c7d43-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c7d43-122">Namespace</span></span><br/>                | <span data-ttu-id="c7d43-123">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="c7d43-123">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c7d43-124">MOF</span><span class="sxs-lookup"><span data-stu-id="c7d43-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7d43-125"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7d43-125"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7d43-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7d43-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7d43-127">**\_Zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c7d43-127">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="c7d43-128">**Método AgeAllRecords de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c7d43-128">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="c7d43-129">**Método ChangeZoneType de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c7d43-129">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="c7d43-130">**Método CreateZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c7d43-130">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="c7d43-131">**Método GetDistinguishedName de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c7d43-131">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="c7d43-132">**Método PauseZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c7d43-132">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="c7d43-133">**Método ReloadZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c7d43-133">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="c7d43-134">**Método ResetSecondaries de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c7d43-134">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="c7d43-135">**Método ResumeZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c7d43-135">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="c7d43-136">**Método UpdateFromDS de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c7d43-136">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="c7d43-137">**Método WriteBackZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c7d43-137">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





