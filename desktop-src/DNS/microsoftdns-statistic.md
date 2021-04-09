---
title: MicrosoftDNS_Statistic (clase)
description: La \_ clase de estadística MicrosoftDNS representa una única estadística de servidor DNS.
ms.assetid: 49ee79d6-b93f-4a9b-8054-1ad290d092d6
keywords:
- DNS de la clase MicrosoftDNS_Statistic
- MicrosoftDNS_Statistic de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_Statistic
- MicrosoftDNS_Statistic.DnsServerName
- MicrosoftDNS_Statistic.CollectionName
- MicrosoftDNS_Statistic.CollectionId
- MicrosoftDNS_Statistic.Name
- MicrosoftDNS_Statistic.Value
- MicrosoftDNS_Statistic.StringValue
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77e26f1738c046e446fa898c4fdff2f6e8855730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079648"
---
# <a name="microsoftdns_statistic-class"></a><span data-ttu-id="64d76-105">\_Clase de estadística MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="64d76-105">MicrosoftDNS\_Statistic class</span></span>

<span data-ttu-id="64d76-106">La clase de **\_ estadística MicrosoftDNS** representa una única estadística de servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="64d76-106">The **MicrosoftDNS\_Statistic** class represents a single DNS Server statistic.</span></span>

<span data-ttu-id="64d76-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="64d76-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="64d76-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="64d76-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_Statistic
{
  string DnsServerName;
  string CollectionName;
  uint32 CollectionId;
  string Name;
  uint32 Value;
  string StringValue;
};
```

## <a name="members"></a><span data-ttu-id="64d76-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="64d76-109">Members</span></span>

<span data-ttu-id="64d76-110">La clase de **\_ estadística MicrosoftDNS** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="64d76-110">The **MicrosoftDNS\_Statistic** class has these types of members:</span></span>

-   [<span data-ttu-id="64d76-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="64d76-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="64d76-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="64d76-112">Properties</span></span>

<span data-ttu-id="64d76-113">La clase de **\_ estadística MicrosoftDNS** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="64d76-113">The **MicrosoftDNS\_Statistic** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="64d76-114">**Recopilación**</span><span class="sxs-lookup"><span data-stu-id="64d76-114">**CollectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64d76-115">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="64d76-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="64d76-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="64d76-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64d76-117">Representación numérica de **CollectionName**.</span><span class="sxs-lookup"><span data-stu-id="64d76-117">Numeric representation of **CollectionName**.</span></span>

</dd> <dt>

<span data-ttu-id="64d76-118">**CollectionName**</span><span class="sxs-lookup"><span data-stu-id="64d76-118">**CollectionName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64d76-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="64d76-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64d76-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="64d76-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64d76-121">Nombre de la colección a la que pertenece la estadística.</span><span class="sxs-lookup"><span data-stu-id="64d76-121">Name of the collection to which the statistic belongs.</span></span>

</dd> <dt>

<span data-ttu-id="64d76-122">**DnsServerName**</span><span class="sxs-lookup"><span data-stu-id="64d76-122">**DnsServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64d76-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="64d76-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64d76-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="64d76-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64d76-125">Indica el FQDN o la dirección IP del servidor DNS que contiene la estadística.</span><span class="sxs-lookup"><span data-stu-id="64d76-125">Indicates the FQDN or IP address of the DNS Server that contains the statistic.</span></span>

</dd> <dt>

<span data-ttu-id="64d76-126">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="64d76-126">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64d76-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="64d76-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64d76-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="64d76-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64d76-129">Nombre de la estadística.</span><span class="sxs-lookup"><span data-stu-id="64d76-129">Name of the statistic.</span></span>

</dd> <dt>

<span data-ttu-id="64d76-130">**StringValue**</span><span class="sxs-lookup"><span data-stu-id="64d76-130">**StringValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64d76-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="64d76-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64d76-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="64d76-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64d76-133">Valor de cadena de la estadística, que solo se usa cuando el valor de la estadística no se representa como DWORD.</span><span class="sxs-lookup"><span data-stu-id="64d76-133">String value of the statistic, used only when the statistic value is not represented as a DWORD.</span></span>

</dd> <dt>

<span data-ttu-id="64d76-134">**Valor**</span><span class="sxs-lookup"><span data-stu-id="64d76-134">**Value**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64d76-135">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="64d76-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="64d76-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="64d76-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64d76-137">Valor numérico de la estadística, representado como DWORD.</span><span class="sxs-lookup"><span data-stu-id="64d76-137">Numeric value of the statistic, represented as a DWORD.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="64d76-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64d76-138">Requirements</span></span>



| <span data-ttu-id="64d76-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="64d76-139">Requirement</span></span> | <span data-ttu-id="64d76-140">Value</span><span class="sxs-lookup"><span data-stu-id="64d76-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="64d76-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64d76-141">Minimum supported client</span></span><br/> | <span data-ttu-id="64d76-142">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="64d76-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="64d76-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64d76-143">Minimum supported server</span></span><br/> | <span data-ttu-id="64d76-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="64d76-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="64d76-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="64d76-145">Namespace</span></span><br/>                | <span data-ttu-id="64d76-146">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="64d76-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="64d76-147">MOF</span><span class="sxs-lookup"><span data-stu-id="64d76-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64d76-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="64d76-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64d76-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="64d76-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64d76-150">MicrosoftDNS \_ StatisticCollection</span><span class="sxs-lookup"><span data-stu-id="64d76-150">MicrosoftDNS\_StatisticCollection</span></span>](microsoftdns-statisticcollection.md)
</dt> </dl>

 

 





