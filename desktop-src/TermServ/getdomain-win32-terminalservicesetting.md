---
title: Método GetDomain de la clase Win32_TerminalServiceSetting
description: Recupera el nombre del dominio del que es miembro el servidor host de sesión Escritorio remoto (host de sesión de escritorio remoto).
ms.assetid: 11d58068-56df-4040-b7ba-afdd55bd417a
ms.tgt_platform: multiple
keywords:
- Método GetDomain Servicios de Escritorio remoto
- Método GetDomain Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método GetDomain
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetDomain
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8e9b2e5ba62f12c67a753cf8e5c41e8296b31e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996020"
---
# <a name="getdomain-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="86296-106">Método GetDomain de la \_ clase TerminalServiceSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="86296-106">GetDomain method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="86296-107">Recupera el nombre del dominio del que es miembro el servidor host de sesión Escritorio remoto (host de sesión de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="86296-107">Retrieves the name of the domain that the Remote Desktop Session Host (RD Session Host) server is a member of.</span></span>

## <a name="syntax"></a><span data-ttu-id="86296-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="86296-108">Syntax</span></span>


```mof
uint32 GetDomain(
  [out] string Domain
);
```



## <a name="parameters"></a><span data-ttu-id="86296-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86296-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86296-110">*Dominio* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="86296-110">*Domain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86296-111">El nombre de dominio del servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="86296-111">The domain name of the RD Session Host server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86296-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86296-112">Remarks</span></span>

<span data-ttu-id="86296-113">Para conectarse al \\ espacio de \\ nombres TerminalServices de cimv2 raíz \\ , el nivel de autenticación debe incluir privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="86296-113">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="86296-114">En el caso de las llamadas de C/C++, se trata de un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C.</span><span class="sxs-lookup"><span data-stu-id="86296-114">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="86296-115">En el caso de las llamadas de Visual Basic y scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6.</span><span class="sxs-lookup"><span data-stu-id="86296-115">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="86296-116">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="86296-116">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="86296-117">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="86296-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="86296-118">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="86296-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="86296-119">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="86296-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="86296-120">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="86296-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="86296-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86296-121">Requirements</span></span>



| <span data-ttu-id="86296-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="86296-122">Requirement</span></span> | <span data-ttu-id="86296-123">Value</span><span class="sxs-lookup"><span data-stu-id="86296-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86296-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86296-124">Minimum supported client</span></span><br/> | <span data-ttu-id="86296-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="86296-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="86296-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86296-126">Minimum supported server</span></span><br/> | <span data-ttu-id="86296-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86296-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="86296-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="86296-128">Namespace</span></span><br/>                | <span data-ttu-id="86296-129">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="86296-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="86296-130">MOF</span><span class="sxs-lookup"><span data-stu-id="86296-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86296-131"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="86296-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="86296-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="86296-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86296-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86296-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86296-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="86296-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86296-135">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="86296-135">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

