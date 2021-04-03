---
title: MDM_Policy_Result01_DeviceLock02 (clase)
description: La \_ clase MDM Policy \_ Result01 \_ DeviceLock02 representa las directivas de bloqueo de dispositivo disponibles.
ms.assetid: 9aac25a8-8502-468f-9478-1ac4ccccaf0b
keywords:
- MDM_Policy_Result01_DeviceLock02 (clase)
- MDM_Policy_Result01_DeviceLock02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_DeviceLock02
- MDM_Policy_Result01_DeviceLock02.InstanceID
- MDM_Policy_Result01_DeviceLock02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa93236b99add5cb49e0b54aa10eab9e959ab01a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905275"
---
# <a name="mdm_policy_result01_devicelock02-class"></a><span data-ttu-id="1683f-105">\_ \_ Clase DeviceLock02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="1683f-105">MDM\_Policy\_Result01\_DeviceLock02 class</span></span>

<span data-ttu-id="1683f-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="1683f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1683f-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="1683f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1683f-108">La clase **MDM \_ Policy \_ Result01 \_ DeviceLock02** representa las directivas de bloqueo de dispositivo disponibles.</span><span class="sxs-lookup"><span data-stu-id="1683f-108">The **MDM\_Policy\_Result01\_DeviceLock02** class represents the device lock policies available.</span></span>

<span data-ttu-id="1683f-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1683f-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1683f-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1683f-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_DeviceLock02
{
  string InstanceID;
  string ParentID;
  sint32 AllowScreenTimeoutWhileLockedUserConfig;
  sint32 AllowSimpleDevicePassword;
  sint32 AlphanumericDevicePasswordRequired;
  sint32 DevicePasswordEnabled;
  sint32 DevicePasswordExpiration;
  sint32 DevicePasswordHistory;
  string EnforceLockScreenAndLogonImage;
  string EnforceLockScreenProvider;
  sint32 MinimumPasswordAge;
  sint32 MaxDevicePasswordFailedAttempts;
  sint32 MaxInactivityTimeDeviceLock;
  sint32 MinDevicePasswordComplexCharacters;
  sint32 MinDevicePasswordLength;
  sint32 ScreenTimeoutWhileLocked;
  string PreventLockScreenSlideShow;
};
```

## <a name="members"></a><span data-ttu-id="1683f-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="1683f-111">Members</span></span>

<span data-ttu-id="1683f-112">La clase Result01 de la **\_ Directiva MDM \_ \_ DeviceLock02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1683f-112">The **MDM\_Policy\_Result01\_DeviceLock02** class has these types of members:</span></span>

-   [<span data-ttu-id="1683f-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1683f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1683f-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1683f-114">Properties</span></span>

<span data-ttu-id="1683f-115">La **clase \_ \_ Result01 de \_ DeviceLock02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1683f-115">The **MDM\_Policy\_Result01\_DeviceLock02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1683f-116">AllowScreenTimeoutWhileLockedUserConfig</span><span class="sxs-lookup"><span data-stu-id="1683f-116">AllowScreenTimeoutWhileLockedUserConfig</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1683f-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1683f-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1683f-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1683f-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1683f-119">AllowSimpleDevicePassword</span><span class="sxs-lookup"><span data-stu-id="1683f-119">AllowSimpleDevicePassword</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-allowsimpledevicepassword)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1683f-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1683f-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1683f-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1683f-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1683f-122">AlphanumericDevicePasswordRequired</span><span class="sxs-lookup"><span data-stu-id="1683f-122">AlphanumericDevicePasswordRequired</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-alphanumericdevicepasswordrequired)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1683f-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1683f-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1683f-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1683f-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1683f-125">DevicePasswordEnabled</span><span class="sxs-lookup"><span data-stu-id="1683f-125">DevicePasswordEnabled</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordenabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1683f-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1683f-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1683f-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1683f-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1683f-128">DevicePasswordExpiration</span><span class="sxs-lookup"><span data-stu-id="1683f-128">DevicePasswordExpiration</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordexpiration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1683f-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1683f-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1683f-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1683f-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1683f-131">DevicePasswordHistory</span><span class="sxs-lookup"><span data-stu-id="1683f-131">DevicePasswordHistory</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1683f-132">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1683f-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1683f-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1683f-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1683f-134">EnforceLockScreenAndLogonImage</span><span class="sxs-lookup"><span data-stu-id="1683f-134">EnforceLockScreenAndLogonImage</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-enforcelockscreenandlogonimage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1683f-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1683f-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1683f-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1683f-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1683f-137">EnforceLockScreenProvider</span><span class="sxs-lookup"><span data-stu-id="1683f-137">EnforceLockScreenProvider</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1683f-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1683f-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1683f-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1683f-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1683f-140">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1683f-140">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1683f-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1683f-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1683f-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1683f-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1683f-143">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1683f-143">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1683f-144">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="1683f-144">Identifies the name of the parent node.</span></span> <span data-ttu-id="1683f-145">Para esta clase, la cadena es "DeviceLock".</span><span class="sxs-lookup"><span data-stu-id="1683f-145">For this class, the string is "DeviceLock".</span></span>

</dd> <dt>

[<span data-ttu-id="1683f-146">MaxDevicePasswordFailedAttempts</span><span class="sxs-lookup"><span data-stu-id="1683f-146">MaxDevicePasswordFailedAttempts</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxdevicepasswordfailedattempts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1683f-147">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1683f-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1683f-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1683f-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1683f-149">MaxInactivityTimeDeviceLock</span><span class="sxs-lookup"><span data-stu-id="1683f-149">MaxInactivityTimeDeviceLock</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxinactivitytimedevicelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1683f-150">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1683f-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1683f-151">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1683f-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1683f-152">MinDevicePasswordComplexCharacters</span><span class="sxs-lookup"><span data-stu-id="1683f-152">MinDevicePasswordComplexCharacters</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordcomplexcharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1683f-153">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1683f-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1683f-154">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1683f-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1683f-155">MinDevicePasswordLength</span><span class="sxs-lookup"><span data-stu-id="1683f-155">MinDevicePasswordLength</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1683f-156">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1683f-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1683f-157">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1683f-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1683f-158">MinimumPasswordAge</span><span class="sxs-lookup"><span data-stu-id="1683f-158">MinimumPasswordAge</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-minimumpasswordage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1683f-159">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1683f-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1683f-160">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1683f-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1683f-161">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1683f-161">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1683f-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1683f-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1683f-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1683f-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1683f-164">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1683f-164">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1683f-165">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="1683f-165">Describes the full path to the parent node.</span></span> <span data-ttu-id="1683f-166">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Result".</span><span class="sxs-lookup"><span data-stu-id="1683f-166">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="1683f-167">PreventLockScreenSlideShow</span><span class="sxs-lookup"><span data-stu-id="1683f-167">PreventLockScreenSlideShow</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-preventlockscreenslideshow)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1683f-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1683f-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1683f-169">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1683f-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1683f-170">ScreenTimeoutWhileLocked</span><span class="sxs-lookup"><span data-stu-id="1683f-170">ScreenTimeoutWhileLocked</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1683f-171">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1683f-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1683f-172">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1683f-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1683f-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1683f-173">Requirements</span></span>



| <span data-ttu-id="1683f-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="1683f-174">Requirement</span></span> | <span data-ttu-id="1683f-175">Value</span><span class="sxs-lookup"><span data-stu-id="1683f-175">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1683f-176">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1683f-176">Minimum supported client</span></span><br/> | <span data-ttu-id="1683f-177">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="1683f-177">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1683f-178">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1683f-178">Minimum supported server</span></span><br/> | <span data-ttu-id="1683f-179">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1683f-179">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1683f-180">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1683f-180">Namespace</span></span><br/>                | <span data-ttu-id="1683f-181">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="1683f-181">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="1683f-182">MOF</span><span class="sxs-lookup"><span data-stu-id="1683f-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1683f-183"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1683f-183"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1683f-184">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1683f-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1683f-185"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1683f-185"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1683f-186">Vea también</span><span class="sxs-lookup"><span data-stu-id="1683f-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1683f-187">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="1683f-187">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

