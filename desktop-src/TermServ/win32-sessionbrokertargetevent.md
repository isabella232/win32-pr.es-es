---
title: Win32_SessionBrokerTargetEvent (clase)
description: Representa un cambio en un destino del agente de sesión.
ms.assetid: ee3ae0ed-eb8b-4777-9b9e-0e50722cf52a
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerTargetEvent clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_SessionBrokerTargetEvent de clase, se describe
topic_type:
- apiref
api_name:
- Win32_SessionBrokerTargetEvent
- Win32_SessionBrokerTargetEvent.SECURITY_DESCRIPTOR
- Win32_SessionBrokerTargetEvent.TIME_CREATED
- Win32_SessionBrokerTargetEvent.ChangeType
- Win32_SessionBrokerTargetEvent.PluginName
- Win32_SessionBrokerTargetEvent.TargetName
- Win32_SessionBrokerTargetEvent.FarmName
- Win32_SessionBrokerTargetEvent.Guid
- Win32_SessionBrokerTargetEvent.Environment
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d7f1cf6aab1c4497ce85cb93318c9ca79368853
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801676"
---
# <a name="win32_sessionbrokertargetevent-class"></a><span data-ttu-id="9c60b-105">\_Clase Win32 SessionBrokerTargetEvent</span><span class="sxs-lookup"><span data-stu-id="9c60b-105">Win32\_SessionBrokerTargetEvent class</span></span>

<span data-ttu-id="9c60b-106">Representa un cambio en un destino del agente de sesión.</span><span class="sxs-lookup"><span data-stu-id="9c60b-106">Represents a change to a session broker target.</span></span>

<span data-ttu-id="9c60b-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9c60b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c60b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c60b-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_SessionBrokerTargetEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint32 ChangeType;
  string PluginName;
  string TargetName;
  string FarmName;
  string Guid;
  string Environment;
};
```

## <a name="members"></a><span data-ttu-id="9c60b-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="9c60b-109">Members</span></span>

<span data-ttu-id="9c60b-110">La **clase \_ SessionBrokerTargetEvent de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9c60b-110">The **Win32\_SessionBrokerTargetEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="9c60b-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9c60b-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9c60b-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9c60b-112">Properties</span></span>

<span data-ttu-id="9c60b-113">La **clase \_ SessionBrokerTargetEvent de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9c60b-113">The **Win32\_SessionBrokerTargetEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9c60b-114">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="9c60b-114">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c60b-115">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c60b-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c60b-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c60b-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c60b-117">Especifica el cambio que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="9c60b-117">Specifies the change that occurred.</span></span> <span data-ttu-id="9c60b-118">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="9c60b-118">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="9c60b-119">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="9c60b-119">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="9c60b-120">No se ha especificado el tipo de cambio.</span><span class="sxs-lookup"><span data-stu-id="9c60b-120">The type of change is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="9c60b-121">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="9c60b-121">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="9c60b-122">La dirección IP externa ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="9c60b-122">The external IP address has changed.</span></span>

</dd> <dt>

<span data-ttu-id="9c60b-123">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="9c60b-123">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="9c60b-124">La dirección IP interna ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="9c60b-124">The internal IP address has changed.</span></span>

</dd> <dt>

<span data-ttu-id="9c60b-125">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="9c60b-125">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="9c60b-126">El destino estaba unido.</span><span class="sxs-lookup"><span data-stu-id="9c60b-126">The target was joined.</span></span>

</dd> <dt>

<span data-ttu-id="9c60b-127">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="9c60b-127">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="9c60b-128">Se quitó el destino.</span><span class="sxs-lookup"><span data-stu-id="9c60b-128">The target was removed.</span></span>

</dd> <dt>

<span data-ttu-id="9c60b-129">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="9c60b-129">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="9c60b-130">El estado del destino ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="9c60b-130">The state of the target has changed.</span></span>

</dd> <dt>

<span data-ttu-id="9c60b-131">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="9c60b-131">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="9c60b-132">El destino está inactivo.</span><span class="sxs-lookup"><span data-stu-id="9c60b-132">The target is idle.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9c60b-133">**Entorno**</span><span class="sxs-lookup"><span data-stu-id="9c60b-133">**Environment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c60b-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9c60b-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c60b-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c60b-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c60b-136">El nombre del entorno.</span><span class="sxs-lookup"><span data-stu-id="9c60b-136">The environment name.</span></span> <span data-ttu-id="9c60b-137">En el caso de un destino de máquina virtual (VM), podría ser el nombre de host de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9c60b-137">In the case of a virtual machine (VM) target, this could be the VM host name.</span></span>

<span data-ttu-id="9c60b-138">**Windows Server 2008 R2:** Esta propiedad no está disponible antes de Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9c60b-138">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="9c60b-139">**FarmName**</span><span class="sxs-lookup"><span data-stu-id="9c60b-139">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c60b-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9c60b-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c60b-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c60b-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c60b-142">El nombre de la granja a la que pertenece el destino.</span><span class="sxs-lookup"><span data-stu-id="9c60b-142">The name of the farm the target belongs to.</span></span>

<span data-ttu-id="9c60b-143">**Windows Server 2008 R2:** Esta propiedad no está disponible antes de Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9c60b-143">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="9c60b-144">**Guid**</span><span class="sxs-lookup"><span data-stu-id="9c60b-144">**Guid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c60b-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9c60b-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c60b-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c60b-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c60b-147">GUID del destino.</span><span class="sxs-lookup"><span data-stu-id="9c60b-147">The GUID of the target.</span></span>

<span data-ttu-id="9c60b-148">**Windows Server 2008 R2:** Esta propiedad no está disponible antes de Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9c60b-148">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="9c60b-149">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="9c60b-149">**PluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c60b-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9c60b-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c60b-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c60b-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c60b-152">Nombre del complemento.</span><span class="sxs-lookup"><span data-stu-id="9c60b-152">The name of the plug-in.</span></span>

<span data-ttu-id="9c60b-153">**Windows Server 2008 R2:** Esta propiedad no está disponible antes de Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9c60b-153">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="9c60b-154">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="9c60b-154">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c60b-155">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="9c60b-155">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="9c60b-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c60b-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c60b-157">Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento.</span><span class="sxs-lookup"><span data-stu-id="9c60b-157">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="9c60b-158">Esta propiedad se hereda del [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="9c60b-158">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="9c60b-159">Para obtener más información sobre las constantes que se usan para establecer este descriptor de seguridad, vea [constantes de seguridad de WMI](/windows/desktop/WmiSdk/wmi-security-constants).</span><span class="sxs-lookup"><span data-stu-id="9c60b-159">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="9c60b-160">**NombreDeDestino**</span><span class="sxs-lookup"><span data-stu-id="9c60b-160">**TargetName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c60b-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9c60b-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c60b-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c60b-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c60b-163">Nombre del destino.</span><span class="sxs-lookup"><span data-stu-id="9c60b-163">The name of the target.</span></span>

<span data-ttu-id="9c60b-164">**Windows Server 2008 R2:** Esta propiedad no está disponible antes de Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9c60b-164">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="9c60b-165">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="9c60b-165">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c60b-166">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c60b-166">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c60b-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c60b-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c60b-168">Valor único que indica la hora a la que se generó el evento.</span><span class="sxs-lookup"><span data-stu-id="9c60b-168">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="9c60b-169">Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="9c60b-169">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="9c60b-170">La información está en el formato de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="9c60b-170">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="9c60b-171">Esta propiedad se hereda del [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="9c60b-171">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="9c60b-172">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9c60b-172">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9c60b-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c60b-173">Requirements</span></span>



| <span data-ttu-id="9c60b-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c60b-174">Requirement</span></span> | <span data-ttu-id="9c60b-175">Value</span><span class="sxs-lookup"><span data-stu-id="9c60b-175">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c60b-176">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c60b-176">Minimum supported client</span></span><br/> | <span data-ttu-id="9c60b-177">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9c60b-177">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9c60b-178">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c60b-178">Minimum supported server</span></span><br/> | <span data-ttu-id="9c60b-179">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9c60b-179">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="9c60b-180">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9c60b-180">Namespace</span></span><br/>                | <span data-ttu-id="9c60b-181">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="9c60b-181">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="9c60b-182">MOF</span><span class="sxs-lookup"><span data-stu-id="9c60b-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c60b-183"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9c60b-183"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c60b-184">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9c60b-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c60b-185"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c60b-185"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

