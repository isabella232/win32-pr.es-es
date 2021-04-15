---
title: Método AgeAllRecords de la clase MicrosoftDNS_Zone
description: El método AgeAllRecords habilita la detección de registros de algunos o todos los registros que no son NS y no SOA de una zona.
ms.assetid: 0e0df1ab-6c7c-4bc4-b292-8f89095970eb
keywords:
- AgeAllRecords el método DNS
- Método AgeAllRecords DNS, clase MicrosoftDNS_Zone
- MicrosoftDNS_Zone de clase DNS, método AgeAllRecords
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.AgeAllRecords
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81c70a1435f96091070b2aee4ed7f079e5a6529a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492370"
---
# <a name="ageallrecords-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="27840-106">Método AgeAllRecords de la \_ clase de zona MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="27840-106">AgeAllRecords method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="27840-107">El método **AgeAllRecords** habilita la detección de registros de algunos o todos los registros que no son NS y no SOA de una zona.</span><span class="sxs-lookup"><span data-stu-id="27840-107">The **AgeAllRecords** method enables aging for some or all non-NS and non-SOA records in a zone.</span></span>

## <a name="syntax"></a><span data-ttu-id="27840-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="27840-108">Syntax</span></span>


```mof
uint32 AgeAllRecords(
  [in, optional] string  NodeName,
  [in, optional] boolean ApplyToSubtree
);
```



## <a name="parameters"></a><span data-ttu-id="27840-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="27840-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27840-110">*Nodename* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="27840-110">*NodeName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="27840-111">Nombre del nodo que se va a edad.</span><span class="sxs-lookup"><span data-stu-id="27840-111">Name of the node to age.</span></span>

</dd> <dt>

<span data-ttu-id="27840-112">*ApplyToSubtree* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="27840-112">*ApplyToSubtree* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="27840-113">Especifica si la detección debe aplicarse a todos los registros del subárbol.</span><span class="sxs-lookup"><span data-stu-id="27840-113">Specifies whether aging should apply to all records in the subtree.</span></span> <span data-ttu-id="27840-114">Establézcalo en TRUE para aplicar la detección de registros obsoletos a todos los registros del subárbol, empezando por NodeName.</span><span class="sxs-lookup"><span data-stu-id="27840-114">Set to TRUE to apply aging to all records in the subtree, beginning with NodeName.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27840-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="27840-115">Return value</span></span>

<span data-ttu-id="27840-116">ERROR \_ correcto indica que la detección se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="27840-116">ERROR\_SUCCESS indicates the aging was successfully completed.</span></span> <span data-ttu-id="27840-117">Cualquier otro valor es un código de error.</span><span class="sxs-lookup"><span data-stu-id="27840-117">Any other value is an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="27840-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="27840-118">Remarks</span></span>

<span data-ttu-id="27840-119">Si no se especifica *nodename* , todos los registros estarán sujetos a detección y eliminación de registros obsoletos.</span><span class="sxs-lookup"><span data-stu-id="27840-119">If *NodeName* is not specified, all records will be subject to aging and scavenging.</span></span>

<span data-ttu-id="27840-120">Si se especifica *nodename* y *ApplyToSubtree* no se especifica o se establece en cero, los registros del nodo especificado estarán sujetos a la detección y eliminación de registros obsoletos.</span><span class="sxs-lookup"><span data-stu-id="27840-120">If *NodeName* is specified and *ApplyToSubtree* is not specified or set to zero, records at the specified node will be subjected to aging and scavenging.</span></span>

<span data-ttu-id="27840-121">Si se especifica *nodename* y *ApplyToSubtree* se establece en 1, todos los registros del subárbol que se inicia en *nodename* estarán sujetos a la detección y eliminación de registros obsoletos.</span><span class="sxs-lookup"><span data-stu-id="27840-121">If *NodeName* is specified and *ApplyToSubtree* is set to 1, all records of the subtree starting at *NodeName* will be subjected to aging and scavenging.</span></span> <span data-ttu-id="27840-122">La marca de tiempo se establece en la hora actual para todos los RRs no NS y no SOA con los nombres de propietario identificados por los parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="27840-122">The time stamp is set to the current time for all non-NS and non-SOA RRs with the owner name(s) identified by the input parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="27840-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27840-123">Requirements</span></span>



| <span data-ttu-id="27840-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="27840-124">Requirement</span></span> | <span data-ttu-id="27840-125">Value</span><span class="sxs-lookup"><span data-stu-id="27840-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="27840-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27840-126">Minimum supported client</span></span><br/> | <span data-ttu-id="27840-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="27840-127">None supported</span></span><br/>                                                              |
| <span data-ttu-id="27840-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27840-128">Minimum supported server</span></span><br/> | <span data-ttu-id="27840-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="27840-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="27840-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="27840-130">Namespace</span></span><br/>                | <span data-ttu-id="27840-131">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="27840-131">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="27840-132">MOF</span><span class="sxs-lookup"><span data-stu-id="27840-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="27840-133"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="27840-133"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27840-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="27840-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27840-135">**\_Zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="27840-135">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="27840-136">**Método ChangeZoneType de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="27840-136">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="27840-137">**Método CreateZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="27840-137">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="27840-138">**Método ForceRefresh de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="27840-138">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="27840-139">**Método GetDistinguishedName de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="27840-139">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="27840-140">**Método PauseZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="27840-140">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="27840-141">**Método ReloadZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="27840-141">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="27840-142">**Método ResetSecondaries de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="27840-142">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="27840-143">**Método ResumeZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="27840-143">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="27840-144">**Método UpdateFromDS de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="27840-144">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="27840-145">**Método WriteBackZone de la \_ clase de zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="27840-145">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





