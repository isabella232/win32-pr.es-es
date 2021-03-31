---
description: Permite establecer límites en el uso del proceso de host de los recursos del sistema.
ms.assetid: 5f5ed1c6-bd1a-406d-a682-7a52059d9450
ms.tgt_platform: multiple
title: __ProviderHostQuotaConfiguration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ProviderHostQuotaConfiguration
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 443d66c8e508346444e98a92b341f1e7d67d8cd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277129"
---
# <a name="__providerhostquotaconfiguration-class"></a><span data-ttu-id="9ffcb-103">\_\_Clase ProviderHostQuotaConfiguration</span><span class="sxs-lookup"><span data-stu-id="9ffcb-103">\_\_ProviderHostQuotaConfiguration class</span></span>

<span data-ttu-id="9ffcb-104">La clase del sistema **\_ \_ ProviderHostQuotaConfiguration** es una clase de configuración para los procesos del proveedor de host.</span><span class="sxs-lookup"><span data-stu-id="9ffcb-104">The **\_\_ProviderHostQuotaConfiguration** system class is a configuration class for host provider processes.</span></span> <span data-ttu-id="9ffcb-105">Esta clase reside en el espacio de nombres raíz y permite establecer límites en el uso del proceso de host de los recursos del sistema.</span><span class="sxs-lookup"><span data-stu-id="9ffcb-105">This class resides in the root namespace and allows limits to be set on host process usage of system resources.</span></span>

<span data-ttu-id="9ffcb-106">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9ffcb-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9ffcb-107">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="9ffcb-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ffcb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ffcb-108">Syntax</span></span>

``` syntax
class __ProviderHostQuotaConfiguration : __SystemClass
{
  uint32 ThreadsPerHost;
  uint32 HandlesPerHost;
  uint32 ProcessLimitAllHosts;
  uint64 MemoryPerHost;
  uint64 MemoryAllHosts;
};
```

## <a name="members"></a><span data-ttu-id="9ffcb-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="9ffcb-109">Members</span></span>

<span data-ttu-id="9ffcb-110">La clase **\_ \_ ProviderHostQuotaConfiguration** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9ffcb-110">The **\_\_ProviderHostQuotaConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="9ffcb-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9ffcb-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9ffcb-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9ffcb-112">Properties</span></span>

<span data-ttu-id="9ffcb-113">La clase **\_ \_ ProviderHostQuotaConfiguration** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9ffcb-113">The **\_\_ProviderHostQuotaConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9ffcb-114">**HandlesPerHost**</span><span class="sxs-lookup"><span data-stu-id="9ffcb-114">**HandlesPerHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ffcb-115">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ffcb-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ffcb-116">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9ffcb-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9ffcb-117">Número de identificadores de objetos de kernel que puede tener cada host.</span><span class="sxs-lookup"><span data-stu-id="9ffcb-117">Number of kernel object handles each host can have.</span></span>

</dd> <dt>

<span data-ttu-id="9ffcb-118">**MemoryAllHosts**</span><span class="sxs-lookup"><span data-stu-id="9ffcb-118">**MemoryAllHosts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ffcb-119">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9ffcb-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ffcb-120">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9ffcb-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9ffcb-121">Cantidad combinada de memoria privada en bytes que pueden tener todos los hosts.</span><span class="sxs-lookup"><span data-stu-id="9ffcb-121">Combined amount of private memory in bytes that can be held by all hosts.</span></span>

<span data-ttu-id="9ffcb-122">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9ffcb-122">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9ffcb-123">**MemoryPerHost**</span><span class="sxs-lookup"><span data-stu-id="9ffcb-123">**MemoryPerHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ffcb-124">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9ffcb-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ffcb-125">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9ffcb-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9ffcb-126">Cantidad de memoria privada que se puede almacenar en cada host.</span><span class="sxs-lookup"><span data-stu-id="9ffcb-126">Amount of private memory that can be held by each host.</span></span>

<span data-ttu-id="9ffcb-127">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9ffcb-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9ffcb-128">**ProcessLimitAllHosts**</span><span class="sxs-lookup"><span data-stu-id="9ffcb-128">**ProcessLimitAllHosts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ffcb-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ffcb-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ffcb-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9ffcb-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9ffcb-131">Número total de procesos de host que se pueden ejecutar simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="9ffcb-131">Total number of host processes that can be executing concurrently.</span></span>

</dd> <dt>

<span data-ttu-id="9ffcb-132">**ThreadsPerHost**</span><span class="sxs-lookup"><span data-stu-id="9ffcb-132">**ThreadsPerHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ffcb-133">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ffcb-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ffcb-134">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9ffcb-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9ffcb-135">Número de subprocesos que pertenecen a un host.</span><span class="sxs-lookup"><span data-stu-id="9ffcb-135">Number of threads owned by any one host.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ffcb-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9ffcb-136">Remarks</span></span>

<span data-ttu-id="9ffcb-137">Se pueden cambiar las propiedades que representan los límites pero, dado que la clase es un singleton, todos los hosts del proveedor comparten los mismos límites.</span><span class="sxs-lookup"><span data-stu-id="9ffcb-137">The properties that represent limits can be changed but because the class is a singleton, all the provider hosts share the same limits.</span></span>

<span data-ttu-id="9ffcb-138">Los parámetros siguientes se utilizan al configurar los límites de objetos de trabajo para el objeto de trabajo de host:</span><span class="sxs-lookup"><span data-stu-id="9ffcb-138">The following parameters are used when configuring the job object limits for the host job object:</span></span>

-   <span data-ttu-id="9ffcb-139">**MemoryAllHosts**</span><span class="sxs-lookup"><span data-stu-id="9ffcb-139">**MemoryAllHosts**</span></span>
-   <span data-ttu-id="9ffcb-140">**MemoryPerHost**</span><span class="sxs-lookup"><span data-stu-id="9ffcb-140">**MemoryPerHost**</span></span>
-   <span data-ttu-id="9ffcb-141">**ProcessLimitAllHosts**</span><span class="sxs-lookup"><span data-stu-id="9ffcb-141">**ProcessLimitAllHosts**</span></span>
-   <span data-ttu-id="9ffcb-142">**ThreadsPerHost**</span><span class="sxs-lookup"><span data-stu-id="9ffcb-142">**ThreadsPerHost**</span></span>

<span data-ttu-id="9ffcb-143">Los sondeos del proceso de host controlan el uso y salen del proceso si se infringe la cuota **HandlesPerHost** .</span><span class="sxs-lookup"><span data-stu-id="9ffcb-143">The host process polls handle usage and exits the process if the **HandlesPerHost** quota is violated.</span></span> <span data-ttu-id="9ffcb-144">Los cambios en estos valores surten efecto después de reiniciar el equipo.</span><span class="sxs-lookup"><span data-stu-id="9ffcb-144">Changes to these values take effect after the computer is restarted.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ffcb-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ffcb-145">Requirements</span></span>



| <span data-ttu-id="9ffcb-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ffcb-146">Requirement</span></span> | <span data-ttu-id="9ffcb-147">Value</span><span class="sxs-lookup"><span data-stu-id="9ffcb-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="9ffcb-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ffcb-148">Minimum supported client</span></span><br/> | <span data-ttu-id="9ffcb-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9ffcb-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="9ffcb-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ffcb-150">Minimum supported server</span></span><br/> | <span data-ttu-id="9ffcb-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ffcb-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="9ffcb-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9ffcb-152">Namespace</span></span><br/>                | <span data-ttu-id="9ffcb-153">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="9ffcb-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="9ffcb-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ffcb-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ffcb-155">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="9ffcb-155">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="9ffcb-156">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="9ffcb-156">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

