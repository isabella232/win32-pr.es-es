---
title: Método GetGracePeriodDays de la clase Win32_TerminalServiceSetting
description: Recupera el número de días que quedan en el Servicios de Escritorio remoto período de gracia de licencias de un servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto). Un valor cero indica que el período de gracia es superior.
ms.assetid: d84d7815-ee09-43d9-a370-993d23f14898
ms.tgt_platform: multiple
keywords:
- Método GetGracePeriodDays Servicios de Escritorio remoto
- Método GetGracePeriodDays Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método GetGracePeriodDays
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetGracePeriodDays
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0faaf525bb74a8ac4b0164c181e5a20cfb215d7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359693"
---
# <a name="getgraceperioddays-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="d5c76-107">Método GetGracePeriodDays de la \_ clase TerminalServiceSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="d5c76-107">GetGracePeriodDays method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="d5c76-108">Recupera el número de días que quedan en el Servicios de Escritorio remoto período de gracia de licencias de un servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="d5c76-108">Retrieves the number of days that are remaining in the Remote Desktop Services licensing grace period for a Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="d5c76-109">Un valor cero indica que el período de gracia es superior.</span><span class="sxs-lookup"><span data-stu-id="d5c76-109">A zero value indicates that the grace period is over.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5c76-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5c76-110">Syntax</span></span>


```mof
uint32 GetGracePeriodDays(
  [out] uint32 DaysLeft
);
```



## <a name="parameters"></a><span data-ttu-id="d5c76-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5c76-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5c76-112">*DaysLeft* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d5c76-112">*DaysLeft* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5c76-113">Número de días que quedan en el período de gracia.</span><span class="sxs-lookup"><span data-stu-id="d5c76-113">The number of days that are remaining in the grace period.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d5c76-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5c76-114">Remarks</span></span>

<span data-ttu-id="d5c76-115">Para conectarse al \\ espacio de \\ nombres TerminalServices de cimv2 raíz \\ , el nivel de autenticación debe incluir privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="d5c76-115">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="d5c76-116">En el caso de las llamadas de C/C++, se trata de un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C.</span><span class="sxs-lookup"><span data-stu-id="d5c76-116">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="d5c76-117">En el caso de las llamadas de Visual Basic y scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6.</span><span class="sxs-lookup"><span data-stu-id="d5c76-117">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="d5c76-118">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="d5c76-118">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="d5c76-119">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d5c76-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d5c76-120">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d5c76-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d5c76-121">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="d5c76-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d5c76-122">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d5c76-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d5c76-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5c76-123">Requirements</span></span>



| <span data-ttu-id="d5c76-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5c76-124">Requirement</span></span> | <span data-ttu-id="d5c76-125">Value</span><span class="sxs-lookup"><span data-stu-id="d5c76-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5c76-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5c76-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d5c76-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d5c76-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d5c76-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5c76-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d5c76-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5c76-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d5c76-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d5c76-130">Namespace</span></span><br/>                | <span data-ttu-id="d5c76-131">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="d5c76-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d5c76-132">MOF</span><span class="sxs-lookup"><span data-stu-id="d5c76-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5c76-133"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d5c76-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5c76-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d5c76-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5c76-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5c76-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5c76-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5c76-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5c76-137">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="d5c76-137">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

