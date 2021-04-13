---
title: Win32_TSDiscoveredLicenseServer (clase)
description: Proporciona detalles sobre el servidor de licencias Escritorio remoto detectado.
ms.assetid: 88523f30-26ad-4f78-a214-f54b7bc1c676
ms.tgt_platform: multiple
keywords:
- Win32_TSDiscoveredLicenseServer clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSDiscoveredLicenseServer de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSDiscoveredLicenseServer
- Win32_TSDiscoveredLicenseServer.LicenseServer
- Win32_TSDiscoveredLicenseServer.HowDiscovered
- Win32_TSDiscoveredLicenseServer.IsLSAvailable
- Win32_TSDiscoveredLicenseServer.IsAdminOnLS
- Win32_TSDiscoveredLicenseServer.IssuingCALs
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d633031df533068f2cf5da65f2f6820a93c78513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492718"
---
# <a name="win32_tsdiscoveredlicenseserver-class"></a><span data-ttu-id="9096c-105">\_Clase Win32 TSDiscoveredLicenseServer</span><span class="sxs-lookup"><span data-stu-id="9096c-105">Win32\_TSDiscoveredLicenseServer class</span></span>

<span data-ttu-id="9096c-106">Proporciona detalles sobre el servidor de licencias Escritorio remoto detectado.</span><span class="sxs-lookup"><span data-stu-id="9096c-106">Provides details about the discovered Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="9096c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9096c-107">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_TSDiscoveredLicenseServer
{
  string LicenseServer;
  uint32 HowDiscovered;
  uint32 IsLSAvailable;
  uint32 IsAdminOnLS;
  uint32 IssuingCALs;
};
```

## <a name="members"></a><span data-ttu-id="9096c-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="9096c-108">Members</span></span>

<span data-ttu-id="9096c-109">La **clase \_ TSDiscoveredLicenseServer de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9096c-109">The **Win32\_TSDiscoveredLicenseServer** class has these types of members:</span></span>

-   [<span data-ttu-id="9096c-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9096c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9096c-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9096c-111">Properties</span></span>

<span data-ttu-id="9096c-112">La **clase \_ TSDiscoveredLicenseServer de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9096c-112">The **Win32\_TSDiscoveredLicenseServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9096c-113">**HowDiscovered**</span><span class="sxs-lookup"><span data-stu-id="9096c-113">**HowDiscovered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9096c-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9096c-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9096c-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9096c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9096c-116">Calificadores: [ **desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9096c-116">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9096c-117">Este propiedad ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="9096c-117">This property is no longer supported.</span></span>

<span data-ttu-id="9096c-118">**Windows Server 2008:** Método de detección del servidor de licencias Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="9096c-118">**Windows Server 2008:** The Remote Desktop license server discovery method.</span></span>

<dt>

<span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>

<span data-ttu-id="9096c-119"><span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>**GroupPolicyConfigured** (0)</span><span class="sxs-lookup"><span data-stu-id="9096c-119"><span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>**GroupPolicyConfigured** (0)</span></span>


</dt> <dd>

<span data-ttu-id="9096c-120">El servidor de licencias se ha detectado mediante la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="9096c-120">The license server was discovered by using group policy.</span></span>

</dd> <dt>

<span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>

<span data-ttu-id="9096c-121"><span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>**RegistryConfigured** (1)</span><span class="sxs-lookup"><span data-stu-id="9096c-121"><span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>**RegistryConfigured** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9096c-122">El servidor de licencias se ha detectado mediante una configuración del registro.</span><span class="sxs-lookup"><span data-stu-id="9096c-122">The license server was discovered by using a registry setting.</span></span>

</dd> <dt>

<span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>

<span data-ttu-id="9096c-123"><span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>**WorkgroupDiscovery** (2)</span><span class="sxs-lookup"><span data-stu-id="9096c-123"><span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>**WorkgroupDiscovery** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9096c-124">El servidor de licencias se ha detectado mediante el ámbito de detección de grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="9096c-124">The license server was discovered by using the workgroup discovery scope.</span></span>

</dd> <dt>

<span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>

<span data-ttu-id="9096c-125"><span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>**DomainDiscovery** (3)</span><span class="sxs-lookup"><span data-stu-id="9096c-125"><span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>**DomainDiscovery** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9096c-126">El servidor de licencias se ha detectado mediante el ámbito de detección de dominios.</span><span class="sxs-lookup"><span data-stu-id="9096c-126">The license server was discovered by using the domain discovery scope.</span></span>

</dd> <dt>

<span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>

<span data-ttu-id="9096c-127"><span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>**EnterpriseDiscovery** (4)</span><span class="sxs-lookup"><span data-stu-id="9096c-127"><span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>**EnterpriseDiscovery** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9096c-128">El servidor de licencias se ha detectado mediante el ámbito de detección de bosque.</span><span class="sxs-lookup"><span data-stu-id="9096c-128">The license server was discovered by using the forest discovery scope.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9096c-129">**IsAdminOnLS**</span><span class="sxs-lookup"><span data-stu-id="9096c-129">**IsAdminOnLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9096c-130">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9096c-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9096c-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9096c-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9096c-132">Indica si la cuenta que se usa para ejecutar el script o el archivo. exe que está utilizando la clase **Win32 \_ TSDiscoveredLicenseServer** tiene acceso de administrador al servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="9096c-132">Indicates whether the account that is being used to run the script or .exe file that is using the **Win32\_TSDiscoveredLicenseServer** class has administrator access to the license server.</span></span>

<dt>

<span id="No"></span><span id="no"></span><span id="NO"></span>

<span data-ttu-id="9096c-133"><span id="No"></span><span id="no"></span><span id="NO"></span>**No** (0)</span><span class="sxs-lookup"><span data-stu-id="9096c-133"><span id="No"></span><span id="no"></span><span id="NO"></span>**No** (0)</span></span>


</dt> <dd>

<span data-ttu-id="9096c-134">La cuenta que se está usando no tiene acceso de administrador al servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="9096c-134">The account that is being used does not have administrator access to the license server.</span></span>

</dd> <dt>

<span id="Yes"></span><span id="yes"></span><span id="YES"></span>

<span data-ttu-id="9096c-135"><span id="Yes"></span><span id="yes"></span><span id="YES"></span>**Sí** (1)</span><span class="sxs-lookup"><span data-stu-id="9096c-135"><span id="Yes"></span><span id="yes"></span><span id="YES"></span>**Yes** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9096c-136">La cuenta que se está usando tiene acceso de administrador al servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="9096c-136">The account that is being used has administrator access to the license server.</span></span>

</dd> <dt>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>

<span data-ttu-id="9096c-137"><span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>No **sé** (2)</span><span class="sxs-lookup"><span data-stu-id="9096c-137"><span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>**Dont know** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9096c-138">No se puede determinar si la cuenta que se está usando tiene acceso de administrador al servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="9096c-138">It cannot be determined whether the account that is being used has administrator access to the license server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9096c-139">**IsLSAvailable**</span><span class="sxs-lookup"><span data-stu-id="9096c-139">**IsLSAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9096c-140">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9096c-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9096c-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9096c-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9096c-142">Indica si el servidor de licencias está disponible (si se \[ puede establecer una conexión RPC de llamada a procedimiento remoto \] en el servidor).</span><span class="sxs-lookup"><span data-stu-id="9096c-142">Indicates whether the license server is available (whether a remote procedure call \[RPC\] connection can be made to the server).</span></span>

<dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span data-ttu-id="9096c-143"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="9096c-143"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>


</dt> <dd>

<span data-ttu-id="9096c-144">El servidor de licencias no está disponible.</span><span class="sxs-lookup"><span data-stu-id="9096c-144">The license server is not available.</span></span>

</dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="9096c-145"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="9096c-145"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9096c-146">El servidor de licencias está disponible.</span><span class="sxs-lookup"><span data-stu-id="9096c-146">The license server is available.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9096c-147">**IssuingCALs**</span><span class="sxs-lookup"><span data-stu-id="9096c-147">**IssuingCALs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9096c-148">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9096c-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9096c-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9096c-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9096c-150">Indica si se permite que el servidor de licencias emita Servicios de Escritorio remoto licencias de acceso de cliente (cal de RDS) en el servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="9096c-150">Indicates whether the license server is allowed to issue Remote Desktop Services client access licenses (RDS CALs) to the RD Session Host server.</span></span>

<dt>

<span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span data-ttu-id="9096c-151"><span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**No permitido** (0)</span><span class="sxs-lookup"><span data-stu-id="9096c-151"><span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Not Allowed** (0)</span></span>


</dt> <dd>

<span data-ttu-id="9096c-152">No se permite que el servidor de licencias emita cal de RDS en el servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="9096c-152">The license server is not allowed to issue RDS CALs to the RD Session Host server.</span></span>

</dd> <dt>

<span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>

<span data-ttu-id="9096c-153"><span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>**Permitido** (1)</span><span class="sxs-lookup"><span data-stu-id="9096c-153"><span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>**Allowed** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9096c-154">El servidor de licencias puede emitir cal de RDS para el servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="9096c-154">The license server is allowed to issue RDS CALs to the RD Session Host server.</span></span>

</dd> <dt>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>

<span data-ttu-id="9096c-155"><span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>No **sé** (2)</span><span class="sxs-lookup"><span data-stu-id="9096c-155"><span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>**Dont know** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9096c-156">No se puede determinar si el servidor de licencias tiene permiso para emitir cal de RDS en el servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="9096c-156">It cannot be determined whether the license server is allowed to issue RDS CALs to the RD Session Host server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9096c-157">**LicenseServer**</span><span class="sxs-lookup"><span data-stu-id="9096c-157">**LicenseServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9096c-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9096c-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9096c-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9096c-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9096c-160">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9096c-160">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9096c-161">Nombre del servidor de licencias Escritorio remoto detectado.</span><span class="sxs-lookup"><span data-stu-id="9096c-161">Name of the discovered Remote Desktop license server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9096c-162">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9096c-162">Remarks</span></span>

<span data-ttu-id="9096c-163">Para conectarse al \\ espacio de \\ nombres TerminalServices de cimv2 raíz \\ , el nivel de autenticación debe incluir privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="9096c-163">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="9096c-164">En el caso de las llamadas de C/C++, se trata de un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C.</span><span class="sxs-lookup"><span data-stu-id="9096c-164">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="9096c-165">En el caso de las llamadas de Visual Basic y scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6.</span><span class="sxs-lookup"><span data-stu-id="9096c-165">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="9096c-166">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="9096c-166">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="9096c-167">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="9096c-167">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9096c-168">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="9096c-168">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9096c-169">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="9096c-169">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9096c-170">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9096c-170">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9096c-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9096c-171">Requirements</span></span>



| <span data-ttu-id="9096c-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="9096c-172">Requirement</span></span> | <span data-ttu-id="9096c-173">Value</span><span class="sxs-lookup"><span data-stu-id="9096c-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9096c-174">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9096c-174">Minimum supported client</span></span><br/> | <span data-ttu-id="9096c-175">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9096c-175">None supported</span></span><br/>                                                               |
| <span data-ttu-id="9096c-176">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9096c-176">Minimum supported server</span></span><br/> | <span data-ttu-id="9096c-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9096c-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9096c-178">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9096c-178">Namespace</span></span><br/>                | <span data-ttu-id="9096c-179">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="9096c-179">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="9096c-180">MOF</span><span class="sxs-lookup"><span data-stu-id="9096c-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9096c-181"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9096c-181"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9096c-182">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9096c-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9096c-183"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9096c-183"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



 

