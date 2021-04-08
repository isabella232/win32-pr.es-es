---
title: Método Modify de la clase MicrosoftDNS_SOAType
description: El método Modify actualiza un registro de recursos de inicio de autoridad (SOA).
ms.assetid: 531b770d-9ac9-43da-8595-fbc175b51b23
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_SOAType clase
- MicrosoftDNS_SOAType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_SOAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ff40abc7f4e93b7122a1c48889c17f9efc4f625
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078991"
---
# <a name="modify-method-of-the-microsoftdns_soatype-class"></a><span data-ttu-id="0db74-106">Método Modify de la \_ clase MicrosoftDNS SOAType</span><span class="sxs-lookup"><span data-stu-id="0db74-106">Modify method of the MicrosoftDNS\_SOAType class</span></span>

<span data-ttu-id="0db74-107">El método **Modify** actualiza un registro de recursos de inicio de autoridad (SOA).</span><span class="sxs-lookup"><span data-stu-id="0db74-107">The **Modify** method updates a Start Of Authority (SOA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="0db74-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0db74-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               SerialNumber,
  [in, optional] string               PrimaryServer,
  [in, optional] string               ResponsibleParty,
  [in, optional] uint32               RefreshInterval,
  [in, optional] uint32               RetryDelay,
  [in, optional] uint32               ExpireLimit,
  [in, optional] uint32               MinimumTTL,
  [out, ref]     MicrosoftDNS_SOAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="0db74-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0db74-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0db74-110">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0db74-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0db74-111">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="0db74-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="0db74-112">*SerialNumber* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0db74-112">*SerialNumber* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0db74-113">Número de serie SOA que representa el número de veces que se ha actualizado la zona, utilizada por [*los servidores secundarios*](s-gly.md) para determinar si es necesaria la transferencia de zona.</span><span class="sxs-lookup"><span data-stu-id="0db74-113">SOA serial number representing the number of times the zone has been updated, used by [*secondary servers*](s-gly.md) to determine whether zone transfer is necessary.</span></span>

</dd> <dt>

<span data-ttu-id="0db74-114">*PrimaryServer* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0db74-114">*PrimaryServer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0db74-115">Nombre del servidor principal.</span><span class="sxs-lookup"><span data-stu-id="0db74-115">Name of the primary server.</span></span>

</dd> <dt>

<span data-ttu-id="0db74-116">*ResponsibleParty* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0db74-116">*ResponsibleParty* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0db74-117">Dirección de buzón del usuario responsable, en forma de alias. Domain, como xyz.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="0db74-117">Mailbox address of the responsible party, in the form of alias.domain, such as xyz.microsoft.com.</span></span> <span data-ttu-id="0db74-118">Observe el uso de un punto en lugar de un símbolo de arroba (@).</span><span class="sxs-lookup"><span data-stu-id="0db74-118">Note the use of a period rather than an at symbol (@).</span></span>

</dd> <dt>

<span data-ttu-id="0db74-119">*RefreshInterval* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0db74-119">*RefreshInterval* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0db74-120">Tiempo, en segundos, antes de que se actualice la zona que contiene este registro.</span><span class="sxs-lookup"><span data-stu-id="0db74-120">Time, in seconds, before the zone containing this record should be refreshed.</span></span>

</dd> <dt>

<span data-ttu-id="0db74-121">*RetryDelay* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0db74-121">*RetryDelay* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0db74-122">Tiempo, en segundos, que el servidor DNS debe retrasarse entre los intentos de resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="0db74-122">Time, in seconds, the DNS Server should delay between name resolution attempts.</span></span>

</dd> <dt>

<span data-ttu-id="0db74-123">*ExpireLimit* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0db74-123">*ExpireLimit* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0db74-124">Tiempo, en segundos, que los servidores secundarios deben esperar una respuesta del servidor principal antes de descartar las copias del archivo de zona como no válidas.</span><span class="sxs-lookup"><span data-stu-id="0db74-124">Time, in seconds, that secondary servers should wait for a response from the primary server before discarding their copies of the zone file as invalid.</span></span>

</dd> <dt>

<span data-ttu-id="0db74-125">*MinimumTTL* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0db74-125">*MinimumTTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0db74-126">Tiempo de TTL, en segundos, aplicado a los registros de recursos de la zona que no especifican su propio TTL.</span><span class="sxs-lookup"><span data-stu-id="0db74-126">TTL time, in seconds, applied to resource records in the zone that do not specify their own TTL.</span></span>

</dd> <dt>

<span data-ttu-id="0db74-127">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="0db74-127">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="0db74-128">Referencia al objeto modificado</span><span class="sxs-lookup"><span data-stu-id="0db74-128">Reference to the modified object</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0db74-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0db74-129">Return value</span></span>

<span data-ttu-id="0db74-130">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="0db74-130">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0db74-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0db74-131">Remarks</span></span>

<span data-ttu-id="0db74-132">Los parámetros no especificados se dejan sin cambios en el registro modificado.</span><span class="sxs-lookup"><span data-stu-id="0db74-132">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="0db74-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0db74-133">Requirements</span></span>



| <span data-ttu-id="0db74-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="0db74-134">Requirement</span></span> | <span data-ttu-id="0db74-135">Value</span><span class="sxs-lookup"><span data-stu-id="0db74-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0db74-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0db74-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0db74-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0db74-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="0db74-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0db74-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0db74-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0db74-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0db74-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0db74-140">Namespace</span></span><br/>                | <span data-ttu-id="0db74-141">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="0db74-141">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="0db74-142">MOF</span><span class="sxs-lookup"><span data-stu-id="0db74-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0db74-143"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0db74-143"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0db74-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="0db74-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0db74-145">**MicrosoftDNS \_ SOAType**</span><span class="sxs-lookup"><span data-stu-id="0db74-145">**MicrosoftDNS\_SOAType**</span></span>](microsoftdns-soatype.md)
</dt> <dt>

[<span data-ttu-id="0db74-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="0db74-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





