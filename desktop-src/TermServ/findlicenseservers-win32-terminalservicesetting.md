---
title: Método FindLicenseServers de la clase Win32_TerminalServiceSetting
description: Enumera todos los servidores de licencias de Escritorio remoto y el método de detección.
ms.assetid: 0de2ee6f-6c56-4293-84da-131b433c6a9d
ms.tgt_platform: multiple
keywords:
- Método FindLicenseServers Servicios de Escritorio remoto
- Método FindLicenseServers Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método FindLicenseServers
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.FindLicenseServers
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b83376876009a691fed233cf723f04dcc3bc3c8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996989"
---
# <a name="findlicenseservers-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="54ce0-106">Método FindLicenseServers de la \_ clase TerminalServiceSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="54ce0-106">FindLicenseServers method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="54ce0-107">Enumera todos los servidores de licencias de Escritorio remoto y el método de detección.</span><span class="sxs-lookup"><span data-stu-id="54ce0-107">Enumerates all of the Remote Desktop license servers, and the method of discovery.</span></span>

## <a name="syntax"></a><span data-ttu-id="54ce0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="54ce0-108">Syntax</span></span>


```mof
uint32 FindLicenseServers(
  [out] Win32_TSDiscoveredLicenseServer LicenseServersList[],
  [out] uint32                          Count
);
```



## <a name="parameters"></a><span data-ttu-id="54ce0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54ce0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54ce0-110">*LicenseServersList* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="54ce0-110">*LicenseServersList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54ce0-111">Lista de objetos [**\_ TSDiscoveredLicenseServer de Win32**](win32-tsdiscoveredlicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="54ce0-111">The list of [**Win32\_TSDiscoveredLicenseServer**](win32-tsdiscoveredlicenseserver.md) objects.</span></span> <span data-ttu-id="54ce0-112">Cada objeto de la lista de resultados tiene el nombre del servidor de licencias de Escritorio remoto y el método de detección.</span><span class="sxs-lookup"><span data-stu-id="54ce0-112">Each object in the output list has the name of the Remote Desktop license server, and the method of discovery.</span></span>

</dd> <dt>

<span data-ttu-id="54ce0-113">*Recuento* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="54ce0-113">*Count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54ce0-114">El número total de servidores de licencias Escritorio remoto detectados en la lista de resultados.</span><span class="sxs-lookup"><span data-stu-id="54ce0-114">The total number of discovered Remote Desktop license servers in the output list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="54ce0-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="54ce0-115">Remarks</span></span>

<span data-ttu-id="54ce0-116">Para conectarse al \\ espacio de \\ nombres TerminalServices de cimv2 raíz \\ , el nivel de autenticación debe incluir privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="54ce0-116">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="54ce0-117">En el caso de las llamadas de C/C++, se trata de un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C.</span><span class="sxs-lookup"><span data-stu-id="54ce0-117">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="54ce0-118">En el caso de las llamadas de Visual Basic y scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6.</span><span class="sxs-lookup"><span data-stu-id="54ce0-118">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="54ce0-119">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="54ce0-119">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="54ce0-120">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="54ce0-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="54ce0-121">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="54ce0-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="54ce0-122">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="54ce0-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="54ce0-123">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="54ce0-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="54ce0-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54ce0-124">Requirements</span></span>



| <span data-ttu-id="54ce0-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="54ce0-125">Requirement</span></span> | <span data-ttu-id="54ce0-126">Value</span><span class="sxs-lookup"><span data-stu-id="54ce0-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54ce0-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54ce0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="54ce0-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="54ce0-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="54ce0-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54ce0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="54ce0-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="54ce0-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="54ce0-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="54ce0-131">Namespace</span></span><br/>                | <span data-ttu-id="54ce0-132">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="54ce0-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="54ce0-133">MOF</span><span class="sxs-lookup"><span data-stu-id="54ce0-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54ce0-134"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="54ce0-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="54ce0-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="54ce0-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54ce0-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54ce0-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54ce0-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="54ce0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54ce0-138">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="54ce0-138">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

