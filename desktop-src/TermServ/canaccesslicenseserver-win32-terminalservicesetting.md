---
title: Método CanAccessLicenseServer de la clase Win32_TerminalServiceSetting
description: CanAccessLicenseServer ya no está disponible.
ms.assetid: b09fa901-8ae1-431e-8d97-27ee84a84779
ms.tgt_platform: multiple
keywords:
- Método CanAccessLicenseServer Servicios de Escritorio remoto
- Método CanAccessLicenseServer Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método CanAccessLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.CanAccessLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ffa5bd0e108c0ccceed6890adedea7901834804
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150040"
---
# <a name="canaccesslicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="e256f-106">Método CanAccessLicenseServer de la \_ clase TerminalServiceSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="e256f-106">CanAccessLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="e256f-107">\[**CanAccessLicenseServer** ya no está disponible para su uso a partir de Windows Server 2008 R2.\]</span><span class="sxs-lookup"><span data-stu-id="e256f-107">\[**CanAccessLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="e256f-108">\* \* Windows Server 2008: \* \*</span><span class="sxs-lookup"><span data-stu-id="e256f-108">\*\*Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="e256f-109">Determina si el servidor host Escritorio remoto de sesión de RD (host de sesión de escritorio remoto) puede solicitar Servicios de Escritorio remoto licencias de acceso de cliente (cal de RDS) desde un servidor de licencias de Escritorio remoto basado en lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e256f-109">Determines whether the Remote Desktop Session Host (RD Session Host) server is allowed to request Remote Desktop Services client access licenses (RDS CALs) from a Remote Desktop license server based on the following:</span></span>

-   <span data-ttu-id="e256f-110">La configuración de directiva de grupo "grupo de seguridad del servidor de licencias" en el servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="e256f-110">The "license server security group" group policy setting on the Remote Desktop license server.</span></span>
-   <span data-ttu-id="e256f-111">Pertenencia al grupo local de equipos Terminal Server en el servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="e256f-111">Membership in the Terminal Server Computers local group on the license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="e256f-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e256f-112">Syntax</span></span>


```mof
uint32 CanAccessLicenseServer(
  [in]  string ServerName,
  [out] uint32 AccessAllowed
);
```



## <a name="parameters"></a><span data-ttu-id="e256f-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e256f-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e256f-114">*NombreDeServidor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e256f-114">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e256f-115">Nombre del servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="e256f-115">The name of the Remote Desktop license server.</span></span>

</dd> <dt>

<span data-ttu-id="e256f-116">*AccessAllowed* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e256f-116">*AccessAllowed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e256f-117">Si el servidor host de sesión de escritorio remoto puede solicitar cal de RDS del servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="e256f-117">Whether the RD Session Host server is allowed to request RDS CALs from the license server.</span></span>

<dt>

<span data-ttu-id="e256f-118">0</span><span class="sxs-lookup"><span data-stu-id="e256f-118">0</span></span>
</dt> <dd>

<span data-ttu-id="e256f-119">Se permite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e256f-119">The request is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="e256f-120">1</span><span class="sxs-lookup"><span data-stu-id="e256f-120">1</span></span>
</dt> <dd>

<span data-ttu-id="e256f-121">No se permite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e256f-121">The request is not allowed.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e256f-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e256f-122">Return value</span></span>

<span data-ttu-id="e256f-123">Devuelve **S \_ correcto** si el servidor host de sesión de escritorio remoto tiene acceso al servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="e256f-123">Returns **S\_OK** if the RD Session Host server has access to the license server.</span></span> <span data-ttu-id="e256f-124">Devuelve **S \_ false** si el servidor host de sesión de escritorio remoto no tiene acceso al servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="e256f-124">Returns **S\_FALSE** if the RD Session Host server does not have access to the license server.</span></span>

## <a name="remarks"></a><span data-ttu-id="e256f-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e256f-125">Remarks</span></span>

<span data-ttu-id="e256f-126">La configuración de directiva "grupo de seguridad del servidor de licencias" le permite especificar los servidores host de sesión de escritorio remoto que pueden ponerse en contacto con el servidor de licencias para obtener Cal de RDS.</span><span class="sxs-lookup"><span data-stu-id="e256f-126">The "license server security group" policy setting allows you to specify the RD Session Host servers that are permitted to contact the license server to obtain RDS CALs.</span></span> <span data-ttu-id="e256f-127">Si la configuración de directiva está habilitada en el servidor de licencias, el servidor de licencias sólo responderá a las solicitudes CAL de RDS de los servidores host de sesión de escritorio remoto cuyas cuentas de equipo sean miembros del grupo local de Terminal Server equipos en el servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="e256f-127">If the policy setting is enabled on the license server, the license server will only respond to RDS CAL requests from RD Session Host servers whose computer accounts are members of the Terminal Server Computers local group on the license server.</span></span>

<span data-ttu-id="e256f-128">Para conectarse al \\ espacio de \\ nombres TerminalServices de cimv2 raíz \\ , el nivel de autenticación debe incluir privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="e256f-128">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="e256f-129">En el caso de las llamadas de C/C++, se trata de un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C.</span><span class="sxs-lookup"><span data-stu-id="e256f-129">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="e256f-130">En el caso de las llamadas de Visual Basic y scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6.</span><span class="sxs-lookup"><span data-stu-id="e256f-130">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="e256f-131">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="e256f-131">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="e256f-132">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="e256f-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e256f-133">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e256f-133">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e256f-134">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="e256f-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e256f-135">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e256f-135">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e256f-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e256f-136">Requirements</span></span>



| <span data-ttu-id="e256f-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="e256f-137">Requirement</span></span> | <span data-ttu-id="e256f-138">Value</span><span class="sxs-lookup"><span data-stu-id="e256f-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e256f-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e256f-139">Minimum supported client</span></span><br/> | <span data-ttu-id="e256f-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e256f-140">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e256f-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e256f-141">Minimum supported server</span></span><br/> | <span data-ttu-id="e256f-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e256f-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e256f-143">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="e256f-143">End of client support</span></span><br/>    | <span data-ttu-id="e256f-144">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e256f-144">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e256f-145">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="e256f-145">End of server support</span></span><br/>    | <span data-ttu-id="e256f-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e256f-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e256f-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e256f-147">Namespace</span></span><br/>                | <span data-ttu-id="e256f-148">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="e256f-148">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e256f-149">MOF</span><span class="sxs-lookup"><span data-stu-id="e256f-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e256f-150"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e256f-150"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e256f-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e256f-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e256f-152"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e256f-152"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e256f-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="e256f-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e256f-154">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="e256f-154">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

