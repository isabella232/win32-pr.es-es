---
title: MDM_Policy_Config01_DeviceLock02 (clase)
description: La \_ clase MDM Policy \_ Config01 \_ DeviceLock02 representa las directivas de bloqueo de dispositivo disponibles.
ms.assetid: 222081ec-c38f-481d-ae38-941fd1317197
keywords:
- MDM_Policy_Config01_DeviceLock02 (clase)
- MDM_Policy_Config01_DeviceLock02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_DeviceLock02
- MDM_Policy_Config01_DeviceLock02.InstanceID
- MDM_Policy_Config01_DeviceLock02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c5926912d276fbe04f75c161196c47d0f0dd384
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150968"
---
# <a name="mdm_policy_config01_devicelock02-class"></a><span data-ttu-id="de7b2-105">\_ \_ Clase DeviceLock02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="de7b2-105">MDM\_Policy\_Config01\_DeviceLock02 class</span></span>

<span data-ttu-id="de7b2-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="de7b2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="de7b2-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="de7b2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="de7b2-108">La clase **MDM \_ Policy \_ Config01 \_ DeviceLock02** representa las directivas de bloqueo de dispositivo disponibles.</span><span class="sxs-lookup"><span data-stu-id="de7b2-108">The **MDM\_Policy\_Config01\_DeviceLock02** class represents the device lock policies available.</span></span>

<span data-ttu-id="de7b2-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="de7b2-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="de7b2-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de7b2-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_DeviceLock02
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

## <a name="members"></a><span data-ttu-id="de7b2-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="de7b2-111">Members</span></span>

<span data-ttu-id="de7b2-112">La clase Config01 de la **\_ Directiva MDM \_ \_ DeviceLock02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="de7b2-112">The **MDM\_Policy\_Config01\_DeviceLock02** class has these types of members:</span></span>

-   [<span data-ttu-id="de7b2-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="de7b2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="de7b2-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="de7b2-114">Properties</span></span>

<span data-ttu-id="de7b2-115">La **clase \_ \_ Config01 de \_ DeviceLock02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="de7b2-115">The **MDM\_Policy\_Config01\_DeviceLock02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="de7b2-116">AllowScreenTimeoutWhileLockedUserConfig</span><span class="sxs-lookup"><span data-stu-id="de7b2-116">AllowScreenTimeoutWhileLockedUserConfig</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de7b2-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="de7b2-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="de7b2-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="de7b2-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="de7b2-119">AllowSimpleDevicePassword</span><span class="sxs-lookup"><span data-stu-id="de7b2-119">AllowSimpleDevicePassword</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-allowsimpledevicepassword)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de7b2-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="de7b2-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="de7b2-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="de7b2-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="de7b2-122">AlphanumericDevicePasswordRequired</span><span class="sxs-lookup"><span data-stu-id="de7b2-122">AlphanumericDevicePasswordRequired</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-alphanumericdevicepasswordrequired)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de7b2-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="de7b2-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="de7b2-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="de7b2-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="de7b2-125">DevicePasswordEnabled</span><span class="sxs-lookup"><span data-stu-id="de7b2-125">DevicePasswordEnabled</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordenabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de7b2-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="de7b2-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="de7b2-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="de7b2-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="de7b2-128">DevicePasswordEnabled no debe establecerse en habilitado (0) cuando se usa WMI para establecer las directivas de DeviceLock de EAS dado que está habilitada de forma predeterminada en el CSP de directivas para la compatibilidad con Windows 8. x.</span><span class="sxs-lookup"><span data-stu-id="de7b2-128">DevicePasswordEnabled should not be set to Enabled (0) when WMI is used to set the EAS DeviceLock policies given that it is Enabled by default in Policy CSP for back compat with Windows 8.x.</span></span> <span data-ttu-id="de7b2-129">Si DevicePasswordEnabled se establece en Enabled (0), el CSP de la Directiva devolverá un error que indica que DevicePasswordEnabled ya existe.</span><span class="sxs-lookup"><span data-stu-id="de7b2-129">If DevicePasswordEnabled is set to Enabled(0) then Policy CSP will return an error stating that DevicePasswordEnabled already exists.</span></span> <span data-ttu-id="de7b2-130">Windows 8. x no admite la Directiva DevicePassword.</span><span class="sxs-lookup"><span data-stu-id="de7b2-130">Windows 8.x did not support DevicePassword policy.</span></span> <span data-ttu-id="de7b2-131">Al deshabilitar DevicePasswordEnabled (1), debe ser la única directiva establecida desde el grupo DeviceLock de directivas a continuación.</span><span class="sxs-lookup"><span data-stu-id="de7b2-131">When disabling DevicePasswordEnabled  (1) then this should be the only policy set from the DeviceLock group of policies below.</span></span> <span data-ttu-id="de7b2-132">A continuación se enumeran las directivas: >-DevicePasswordEnabled es la directiva principal de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="de7b2-132">The policies are listed below: > - DevicePasswordEnabled is the parent policy of the following:</span></span>

-   <span data-ttu-id="de7b2-133">DevicePasswordEnabled es la directiva principal de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="de7b2-133">DevicePasswordEnabled is the parent policy of the following:</span></span>
    -   <span data-ttu-id="de7b2-134">AllowSimpleDevicePassword</span><span class="sxs-lookup"><span data-stu-id="de7b2-134">AllowSimpleDevicePassword</span></span>
    -   <span data-ttu-id="de7b2-135">MinDevicePasswordLength</span><span class="sxs-lookup"><span data-stu-id="de7b2-135">MinDevicePasswordLength</span></span>
    -   <span data-ttu-id="de7b2-136">AlphanumericDevicePasswordRequired es la directiva principal de:</span><span class="sxs-lookup"><span data-stu-id="de7b2-136">AlphanumericDevicePasswordRequired is the parent policy of:</span></span>
        -   <span data-ttu-id="de7b2-137">MinDevicePasswordComplexCharacters</span><span class="sxs-lookup"><span data-stu-id="de7b2-137">MinDevicePasswordComplexCharacters</span></span> 
    -   <span data-ttu-id="de7b2-138">MaxDevicePasswordFailedAttempts</span><span class="sxs-lookup"><span data-stu-id="de7b2-138">MaxDevicePasswordFailedAttempts</span></span>
    -   <span data-ttu-id="de7b2-139">MaxInactivityTimeDeviceLock</span><span class="sxs-lookup"><span data-stu-id="de7b2-139">MaxInactivityTimeDeviceLock</span></span>

</dd> <dt>

[<span data-ttu-id="de7b2-140">DevicePasswordExpiration</span><span class="sxs-lookup"><span data-stu-id="de7b2-140">DevicePasswordExpiration</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordexpiration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de7b2-141">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="de7b2-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="de7b2-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="de7b2-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="de7b2-143">DevicePasswordHistory</span><span class="sxs-lookup"><span data-stu-id="de7b2-143">DevicePasswordHistory</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de7b2-144">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="de7b2-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="de7b2-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="de7b2-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="de7b2-146">EnforceLockScreenAndLogonImage</span><span class="sxs-lookup"><span data-stu-id="de7b2-146">EnforceLockScreenAndLogonImage</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-enforcelockscreenandlogonimage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de7b2-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="de7b2-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de7b2-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="de7b2-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="de7b2-149">EnforceLockScreenProvider</span><span class="sxs-lookup"><span data-stu-id="de7b2-149">EnforceLockScreenProvider</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de7b2-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="de7b2-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de7b2-151">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="de7b2-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="de7b2-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="de7b2-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de7b2-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="de7b2-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de7b2-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="de7b2-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de7b2-155">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="de7b2-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="de7b2-156">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="de7b2-156">Identifies the name of the parent node.</span></span> <span data-ttu-id="de7b2-157">Para esta clase, la cadena es "DeviceLock".</span><span class="sxs-lookup"><span data-stu-id="de7b2-157">For this class, the string is "DeviceLock".</span></span>

</dd> <dt>

[<span data-ttu-id="de7b2-158">MaxDevicePasswordFailedAttempts</span><span class="sxs-lookup"><span data-stu-id="de7b2-158">MaxDevicePasswordFailedAttempts</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxdevicepasswordfailedattempts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de7b2-159">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="de7b2-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="de7b2-160">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="de7b2-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="de7b2-161">MaxInactivityTimeDeviceLock</span><span class="sxs-lookup"><span data-stu-id="de7b2-161">MaxInactivityTimeDeviceLock</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxinactivitytimedevicelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de7b2-162">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="de7b2-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="de7b2-163">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="de7b2-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="de7b2-164">MinDevicePasswordComplexCharacters</span><span class="sxs-lookup"><span data-stu-id="de7b2-164">MinDevicePasswordComplexCharacters</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordcomplexcharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de7b2-165">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="de7b2-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="de7b2-166">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="de7b2-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="de7b2-167">MinDevicePasswordLength</span><span class="sxs-lookup"><span data-stu-id="de7b2-167">MinDevicePasswordLength</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de7b2-168">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="de7b2-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="de7b2-169">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="de7b2-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="de7b2-170">MinimumPasswordAge</span><span class="sxs-lookup"><span data-stu-id="de7b2-170">MinimumPasswordAge</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-minimumpasswordage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de7b2-171">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="de7b2-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="de7b2-172">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="de7b2-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="de7b2-173">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="de7b2-173">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de7b2-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="de7b2-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de7b2-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="de7b2-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de7b2-176">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="de7b2-176">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="de7b2-177">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="de7b2-177">Describes the full path to the parent node.</span></span> <span data-ttu-id="de7b2-178">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Config".</span><span class="sxs-lookup"><span data-stu-id="de7b2-178">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="de7b2-179">PreventLockScreenSlideShow</span><span class="sxs-lookup"><span data-stu-id="de7b2-179">PreventLockScreenSlideShow</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-preventlockscreenslideshow)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de7b2-180">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="de7b2-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de7b2-181">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="de7b2-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="de7b2-182">ScreenTimeoutWhileLocked</span><span class="sxs-lookup"><span data-stu-id="de7b2-182">ScreenTimeoutWhileLocked</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de7b2-183">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="de7b2-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="de7b2-184">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="de7b2-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="de7b2-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de7b2-185">Requirements</span></span>



| <span data-ttu-id="de7b2-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="de7b2-186">Requirement</span></span> | <span data-ttu-id="de7b2-187">Value</span><span class="sxs-lookup"><span data-stu-id="de7b2-187">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de7b2-188">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de7b2-188">Minimum supported client</span></span><br/> | <span data-ttu-id="de7b2-189">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="de7b2-189">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="de7b2-190">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de7b2-190">Minimum supported server</span></span><br/> | <span data-ttu-id="de7b2-191">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="de7b2-191">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="de7b2-192">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="de7b2-192">Namespace</span></span><br/>                | <span data-ttu-id="de7b2-193">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="de7b2-193">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="de7b2-194">MOF</span><span class="sxs-lookup"><span data-stu-id="de7b2-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de7b2-195"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="de7b2-195"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="de7b2-196">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="de7b2-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de7b2-197"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de7b2-197"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de7b2-198">Vea también</span><span class="sxs-lookup"><span data-stu-id="de7b2-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de7b2-199">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="de7b2-199">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

