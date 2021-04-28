---
description: 'SystemConfig_Services clase : esta clase es la clase de tipo de evento para los eventos de configuración del servicio.'
ms.assetid: 7cba9992-d154-44b8-87d8-b46a8438f607
title: SystemConfig_Services clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Services
- SystemConfig_Services.ProcessId
- SystemConfig_Services.ServiceState
- SystemConfig_Services.SubProcessTag
- SystemConfig_Services.ServiceName
- SystemConfig_Services.DisplayName
- SystemConfig_Services.ProcessName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 754b0e10c3882911c6e91fc2590c11739c3f7531
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106063"
---
# <a name="systemconfig_services-class"></a><span data-ttu-id="6b85f-103">Clase SystemConfig \_ Services</span><span class="sxs-lookup"><span data-stu-id="6b85f-103">SystemConfig\_Services class</span></span>

<span data-ttu-id="6b85f-104">Esta clase es la clase de tipo de evento para los eventos de configuración del servicio.</span><span class="sxs-lookup"><span data-stu-id="6b85f-104">This class is the event type class for service configuration events.</span></span>

<span data-ttu-id="6b85f-105">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="6b85f-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b85f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6b85f-106">Syntax</span></span>

``` syntax
[EventType(15), EventTypeName("Services")]
class SystemConfig_Services : SystemConfig
{
  uint32 ProcessId;
  uint32 ServiceState;
  uint32 SubProcessTag;
  string ServiceName[];
  string DisplayName[];
  string ProcessName[];
};
```

## <a name="members"></a><span data-ttu-id="6b85f-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6b85f-107">Members</span></span>

<span data-ttu-id="6b85f-108">La **clase SystemConfig \_ Services** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6b85f-108">The **SystemConfig\_Services** class has these types of members:</span></span>

-   [<span data-ttu-id="6b85f-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6b85f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6b85f-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6b85f-110">Properties</span></span>

<span data-ttu-id="6b85f-111">La **clase SystemConfig \_ Services** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6b85f-111">The **SystemConfig\_Services** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6b85f-112">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="6b85f-112">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b85f-113">Tipo de datos: **matriz de** cadenas</span><span class="sxs-lookup"><span data-stu-id="6b85f-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6b85f-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6b85f-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b85f-115">Calificadores: **WmiDataId** (5), **StringTermination("NullTerminated")**, **Format("w")**</span><span class="sxs-lookup"><span data-stu-id="6b85f-115">Qualifiers: **WmiDataId** (5), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="6b85f-116">Nombre para mostrar del servicio.</span><span class="sxs-lookup"><span data-stu-id="6b85f-116">Display name of the service.</span></span> <span data-ttu-id="6b85f-117">El nombre se conserva en el Administrador de control de servicios.</span><span class="sxs-lookup"><span data-stu-id="6b85f-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="6b85f-118">Sin embargo, las comparaciones de nombres para mostrar siempre se realizan sin distinción entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="6b85f-118">However, display name comparisons are always case-insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="6b85f-119">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="6b85f-119">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b85f-120">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="6b85f-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b85f-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6b85f-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b85f-122">Calificadores: **WmiDataId** (1), **Format("x")**</span><span class="sxs-lookup"><span data-stu-id="6b85f-122">Qualifiers: **WmiDataId** (1), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="6b85f-123">Identificador del proceso en el que se ejecuta el servicio.</span><span class="sxs-lookup"><span data-stu-id="6b85f-123">Identifier of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="6b85f-124">**ProcessName**</span><span class="sxs-lookup"><span data-stu-id="6b85f-124">**ProcessName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b85f-125">Tipo de datos: **matriz de** cadenas</span><span class="sxs-lookup"><span data-stu-id="6b85f-125">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6b85f-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6b85f-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b85f-127">Calificadores: **WmiDataId** (6), **StringTermination("NullTerminated")**, **Format("w")**</span><span class="sxs-lookup"><span data-stu-id="6b85f-127">Qualifiers: **WmiDataId** (6), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="6b85f-128">Nombre del proceso en el que se ejecuta el servicio.</span><span class="sxs-lookup"><span data-stu-id="6b85f-128">Name of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="6b85f-129">**Servicename**</span><span class="sxs-lookup"><span data-stu-id="6b85f-129">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b85f-130">Tipo de datos: **matriz de** cadenas</span><span class="sxs-lookup"><span data-stu-id="6b85f-130">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6b85f-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6b85f-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b85f-132">Calificadores: **WmiDataId** (4), **StringTermination("NullTerminated")**, **Format("w")**</span><span class="sxs-lookup"><span data-stu-id="6b85f-132">Qualifiers: **WmiDataId** (4), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="6b85f-133">Identificador único del servicio.</span><span class="sxs-lookup"><span data-stu-id="6b85f-133">Unique identifier of the service.</span></span> <span data-ttu-id="6b85f-134">El identificador proporciona una indicación de la funcionalidad que proporciona el servicio.</span><span class="sxs-lookup"><span data-stu-id="6b85f-134">The identifier provides an indication of the functionality the service provides.</span></span>

</dd> <dt>

<span data-ttu-id="6b85f-135">**ServiceState**</span><span class="sxs-lookup"><span data-stu-id="6b85f-135">**ServiceState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b85f-136">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="6b85f-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b85f-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6b85f-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b85f-138">Calificadores: **WmiDataId** (2), **Format("x")**</span><span class="sxs-lookup"><span data-stu-id="6b85f-138">Qualifiers: **WmiDataId** (2), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="6b85f-139">Estado actual del servicio.</span><span class="sxs-lookup"><span data-stu-id="6b85f-139">Current state of the service.</span></span> <span data-ttu-id="6b85f-140">Para ver los valores posibles, vea el **miembro dwCurrentState** de **SERVICE STATUS \_ \_ PROCESS**.</span><span class="sxs-lookup"><span data-stu-id="6b85f-140">For possible values, see the **dwCurrentState** member of **SERVICE\_STATUS\_PROCESS**.</span></span>

</dd> <dt>

<span data-ttu-id="6b85f-141">**SubProcessTag**</span><span class="sxs-lookup"><span data-stu-id="6b85f-141">**SubProcessTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b85f-142">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="6b85f-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b85f-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6b85f-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b85f-144">Calificadores: **WmiDataId** (3), **Format("x")**</span><span class="sxs-lookup"><span data-stu-id="6b85f-144">Qualifiers: **WmiDataId** (3), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="6b85f-145">Identifica el servicio.</span><span class="sxs-lookup"><span data-stu-id="6b85f-145">Identifies the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6b85f-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b85f-146">Requirements</span></span>



| <span data-ttu-id="6b85f-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b85f-147">Requirement</span></span> | <span data-ttu-id="6b85f-148">Valor</span><span class="sxs-lookup"><span data-stu-id="6b85f-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6b85f-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b85f-149">Minimum supported client</span></span><br/> | <span data-ttu-id="6b85f-150">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6b85f-150">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6b85f-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b85f-151">Minimum supported server</span></span><br/> | <span data-ttu-id="6b85f-152">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6b85f-152">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6b85f-153">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6b85f-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b85f-154">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="6b85f-154">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




