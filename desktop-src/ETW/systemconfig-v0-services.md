---
description: 'SystemConfig_V0_Services clase : esta clase es la clase de tipo de evento para los eventos de configuración de servicio.'
ms.assetid: 1e6c2061-f1a2-4253-a0c4-4b45b2feceda
title: SystemConfig_V0_Services clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Services
- SystemConfig_V0_Services.ServiceName
- SystemConfig_V0_Services.DisplayName
- SystemConfig_V0_Services.ProcessName
- SystemConfig_V0_Services.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: b69ca7cf4ee4e16a5fbcb6a5f10c659f713ab458
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105933"
---
# <a name="systemconfig_v0_services-class"></a><span data-ttu-id="6029e-103">SystemConfig \_ V0 \_ Services (clase)</span><span class="sxs-lookup"><span data-stu-id="6029e-103">SystemConfig\_V0\_Services class</span></span>

<span data-ttu-id="6029e-104">Esta clase es la clase de tipo de evento para los eventos de configuración de servicio.</span><span class="sxs-lookup"><span data-stu-id="6029e-104">This class is the event type class for service configuration events.</span></span>

<span data-ttu-id="6029e-105">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="6029e-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6029e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6029e-106">Syntax</span></span>

``` syntax
[EventType(15), EventTypeName("Services")]
class SystemConfig_V0_Services : SystemConfig_V0
{
  char16 ServiceName[];
  char16 DisplayName[];
  char16 ProcessName[];
  uint32 ProcessId;
};
```

## <a name="members"></a><span data-ttu-id="6029e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6029e-107">Members</span></span>

<span data-ttu-id="6029e-108">La **clase SystemConfig \_ V0 \_ Services** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6029e-108">The **SystemConfig\_V0\_Services** class has these types of members:</span></span>

-   [<span data-ttu-id="6029e-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6029e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6029e-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6029e-110">Properties</span></span>

<span data-ttu-id="6029e-111">La **clase SystemConfig \_ V0 \_ Services** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6029e-111">The **SystemConfig\_V0\_Services** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6029e-112">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="6029e-112">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6029e-113">Tipo de datos: **matriz char16**</span><span class="sxs-lookup"><span data-stu-id="6029e-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="6029e-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6029e-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6029e-115">Calificadores: **WmiDataId** (2), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="6029e-115">Qualifiers: **WmiDataId** (2), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="6029e-116">Nombre para mostrar del servicio.</span><span class="sxs-lookup"><span data-stu-id="6029e-116">Display name of the service.</span></span> <span data-ttu-id="6029e-117">El nombre se conserva entre mayúsculas y minúsculas en Service Control Manager.</span><span class="sxs-lookup"><span data-stu-id="6029e-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="6029e-118">Sin embargo, las comparaciones de nombres para mostrar siempre se realizan sin distinción entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="6029e-118">However, display name comparisons are always case-insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="6029e-119">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="6029e-119">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6029e-120">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="6029e-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6029e-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6029e-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6029e-122">Calificadores: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="6029e-122">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="6029e-123">Identificador del proceso en el que se ejecuta el servicio.</span><span class="sxs-lookup"><span data-stu-id="6029e-123">Identifier of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="6029e-124">**ProcessName**</span><span class="sxs-lookup"><span data-stu-id="6029e-124">**ProcessName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6029e-125">Tipo de datos: **matriz char16**</span><span class="sxs-lookup"><span data-stu-id="6029e-125">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="6029e-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6029e-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6029e-127">Calificadores: **WmiDataId** (3), **Max** (34)</span><span class="sxs-lookup"><span data-stu-id="6029e-127">Qualifiers: **WmiDataId** (3), **Max** (34)</span></span>
</dt> </dl>

<span data-ttu-id="6029e-128">Nombre del proceso en el que se ejecuta el servicio.</span><span class="sxs-lookup"><span data-stu-id="6029e-128">Name of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="6029e-129">**Servicename**</span><span class="sxs-lookup"><span data-stu-id="6029e-129">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6029e-130">Tipo de datos: **matriz char16**</span><span class="sxs-lookup"><span data-stu-id="6029e-130">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="6029e-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6029e-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6029e-132">Calificadores: **WmiDataId** (1), **Max** (34)</span><span class="sxs-lookup"><span data-stu-id="6029e-132">Qualifiers: **WmiDataId** (1), **Max** (34)</span></span>
</dt> </dl>

<span data-ttu-id="6029e-133">Identificador único del servicio.</span><span class="sxs-lookup"><span data-stu-id="6029e-133">Unique identifier of the service.</span></span> <span data-ttu-id="6029e-134">El identificador proporciona una indicación de la funcionalidad que proporciona el servicio.</span><span class="sxs-lookup"><span data-stu-id="6029e-134">The identifier provides an indication of the functionality the service provides.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6029e-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6029e-135">Requirements</span></span>



| <span data-ttu-id="6029e-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="6029e-136">Requirement</span></span> | <span data-ttu-id="6029e-137">Valor</span><span class="sxs-lookup"><span data-stu-id="6029e-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6029e-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6029e-138">Minimum supported client</span></span><br/> | <span data-ttu-id="6029e-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6029e-139">None supported</span></span><br/>                            |
| <span data-ttu-id="6029e-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6029e-140">Minimum supported server</span></span><br/> | <span data-ttu-id="6029e-141">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6029e-141">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6029e-142">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6029e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6029e-143">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="6029e-143">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




