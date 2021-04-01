---
title: Tipos de NapTypes. h de NAP
description: 'Nota: la plataforma de protección de acceso a redes no está disponible a partir de Windows 10. los tipos de la API de protección de acceso a redes (NAP) son los siguientes.'
ms.assetid: 54f2866b-4333-4fc8-bb25-b7d4ae72b7dc
keywords:
- ProbationTime
- ProtocolMaxSize
- NapComponentId
- SystemHealthEntityId
- EnforcementEntityId
- SystemHealthEntityCount
- EnforcementEntityCount
- StringCorrelationId
- ConnectionId
- Porcentaje
- MessageId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5780d73701354a12b244c5e5ea6167c2cfba70d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996890"
---
# <a name="nap-datatypes"></a><span data-ttu-id="12faa-114">Tipos de texto de NAP</span><span class="sxs-lookup"><span data-stu-id="12faa-114">NAP Datatypes</span></span>

> [!Note]  
> <span data-ttu-id="12faa-115">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="12faa-115">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="12faa-116">Los tipos de la API de protección de acceso a redes (NAP) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="12faa-116">The datatypes for the Network Access Protection (NAP) API are as follows.</span></span>


```C++
typedef FILETIME ProbationTime;
typedef UINT32 ProtocolMaxSize;
typedef UINT32 NapComponentId;
typedef NapComponentId SystemHealthEntityId;
typedef NapComponentId EnforcementEntityId;
typedef UINT16 SystemHealthEntityCount;
typedef UINT16 EnforcementEntityCount;
typedef CountedString StringCorrelationId;
typedef GUID ConnectionId;
typedef UINT8 Percentage;
typedef UINT32 MessageId;
```



<dl> <dt>

<span data-ttu-id="12faa-117">**ProbationTime**</span><span class="sxs-lookup"><span data-stu-id="12faa-117">**ProbationTime**</span></span>
</dt> <dd>

<span data-ttu-id="12faa-118">Una estructura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) que contiene una hora relacionada con el período de prueba de un equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="12faa-118">A [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that contains a time related to a client machine's probation.</span></span>

</dd> <dt>

<span data-ttu-id="12faa-119">**ProtocolMaxSize**</span><span class="sxs-lookup"><span data-stu-id="12faa-119">**ProtocolMaxSize**</span></span>
</dt> <dd>

<span data-ttu-id="12faa-120">Valor que especifica el intervalo de valores posibles para el tamaño máximo, en bytes, de un paquete [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) tal y como lo define el intervalo ([**minProtocolMaxSize, maxProtocolMaxSize**](nap-type-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="12faa-120">A value that specifies the range of possible values for the maximum size, in bytes, of an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet as defined by range([**minProtocolMaxSize, maxProtocolMaxSize**](nap-type-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="12faa-121">**NapComponentId**</span><span class="sxs-lookup"><span data-stu-id="12faa-121">**NapComponentId**</span></span>
</dt> <dd>

<span data-ttu-id="12faa-122">Identificador único de 4 bytes que usan Sha, SHV y clientes de cumplimiento para identificarse.</span><span class="sxs-lookup"><span data-stu-id="12faa-122">A unique 4-byte identifier used by SHAs, SHVs and enforcement clients to identify themselves.</span></span> <span data-ttu-id="12faa-123">Los tres primeros bytes son el código SMI asignado por IETF del proveedor y el último byte identifica el propio componente.</span><span class="sxs-lookup"><span data-stu-id="12faa-123">The first three bytes are the IETF-assigned SMI code of the vendor, and the last byte identifies the component itself.</span></span>

</dd> <dt>

<span data-ttu-id="12faa-124">**SystemHealthEntityId**</span><span class="sxs-lookup"><span data-stu-id="12faa-124">**SystemHealthEntityId**</span></span>
</dt> <dd>

<span data-ttu-id="12faa-125">Valor de **NapComponentId** que se usa para identificar pares Sha/SHV.</span><span class="sxs-lookup"><span data-stu-id="12faa-125">A **NapComponentId** value used to identify SHA/SHV pairs.</span></span>

</dd> <dt>

<span data-ttu-id="12faa-126">**EnforcementEntityId**</span><span class="sxs-lookup"><span data-stu-id="12faa-126">**EnforcementEntityId**</span></span>
</dt> <dd>

<span data-ttu-id="12faa-127">Valor de **NapComponentId** que se usa para identificar los clientes de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="12faa-127">A **NapComponentId** value used to identify enforcement clients.</span></span>

</dd> <dt>

<span data-ttu-id="12faa-128">**SystemHealthEntityCount**</span><span class="sxs-lookup"><span data-stu-id="12faa-128">**SystemHealthEntityCount**</span></span>
</dt> <dd>

<span data-ttu-id="12faa-129">Valor que especifica el número de Sha registrados en el sistema NAP en el intervalo de 0 (cero) a [**maxSystemHealthEntityCount**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="12faa-129">A value that specifies the number of registered SHAs in the NAP system in the range 0 (zero) to [**maxSystemHealthEntityCount**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="12faa-130">**EnforcementEntityCount**</span><span class="sxs-lookup"><span data-stu-id="12faa-130">**EnforcementEntityCount**</span></span>
</dt> <dd>

<span data-ttu-id="12faa-131">Valor que especifica el número de clientes de cumplimiento en el sistema NAP en el intervalo de 0 (cero) a [**maxEnforcerCount**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="12faa-131">A value that specifies the number of enforcement clients in the NAP system in the range 0 (zero) to [**maxEnforcerCount**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="12faa-132">**StringCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="12faa-132">**StringCorrelationId**</span></span>
</dt> <dd>

<span data-ttu-id="12faa-133">La versión [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) de una estructura [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) usada para emparejar [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) con **SoHResponses**.</span><span class="sxs-lookup"><span data-stu-id="12faa-133">The [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) version of a [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) structure used to pair [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) to **SoHResponses**.</span></span>

</dd> <dt>

<span data-ttu-id="12faa-134">**ConnectionId**</span><span class="sxs-lookup"><span data-stu-id="12faa-134">**ConnectionId**</span></span>
</dt> <dd>

<span data-ttu-id="12faa-135">Un identificador único global (GUID) único que se usa para identificar las conexiones NAP mantenidas por los clientes de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="12faa-135">A unique Globally Unique Identifier (GUID) used to identify a NAP connections maintained by enforcement clients.</span></span>

</dd> <dt>

<span data-ttu-id="12faa-136">**Porcentaje**</span><span class="sxs-lookup"><span data-stu-id="12faa-136">**Percentage**</span></span>
</dt> <dd>

<span data-ttu-id="12faa-137">Un valor que contiene el porcentaje comprendido entre 0 (cero) y 100 de corrección completada</span><span class="sxs-lookup"><span data-stu-id="12faa-137">A value that contains the percentage between 0 (zero) and 100 of remediation that is complete</span></span>

</dd> <dt>

<span data-ttu-id="12faa-138">**MessageId**</span><span class="sxs-lookup"><span data-stu-id="12faa-138">**MessageId**</span></span>
</dt> <dd>

<span data-ttu-id="12faa-139">Un valor único que se usa para identificar los mensajes del sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="12faa-139">A unique value used to identify NAP system messages.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="12faa-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12faa-140">Requirements</span></span>



| <span data-ttu-id="12faa-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="12faa-141">Requirement</span></span> | <span data-ttu-id="12faa-142">Value</span><span class="sxs-lookup"><span data-stu-id="12faa-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12faa-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12faa-143">Minimum supported client</span></span><br/> | <span data-ttu-id="12faa-144">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="12faa-144">Windows Vista \[desktop apps only\]</span></span><br/>                                                                                                                      |
| <span data-ttu-id="12faa-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12faa-145">Minimum supported server</span></span><br/> | <span data-ttu-id="12faa-146">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="12faa-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                                |
| <span data-ttu-id="12faa-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="12faa-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="12faa-148"><dt>NapTypes. h; </dt> <dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="12faa-148"><dt>NapTypes.h; </dt> <dt>NapEnforcementClient.h</dt></span></span> </dl> |



 

