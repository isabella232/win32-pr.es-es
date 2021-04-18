---
title: Método GetWinstationDriverNames de la clase Win32_TerminalServiceSetting
description: Recupera una lista de los nombres de controlador de la estación de la.
ms.assetid: 578c2a07-17e7-4bd6-b520-942cd48ee40f
ms.tgt_platform: multiple
keywords:
- Método GetWinstationDriverNames Servicios de Escritorio remoto
- Método GetWinstationDriverNames Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método GetWinstationDriverNames
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetWinstationDriverNames
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41bc0157f368edf129f578765c1b8d73f6f48a33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685934"
---
# <a name="getwinstationdrivernames-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="17dca-106">Método GetWinstationDriverNames de la \_ clase TerminalServiceSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="17dca-106">GetWinstationDriverNames method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="17dca-107">Recupera una lista de los nombres de controlador de la estación de la.</span><span class="sxs-lookup"><span data-stu-id="17dca-107">Retrieves a list of Winstation driver names.</span></span>

## <a name="syntax"></a><span data-ttu-id="17dca-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17dca-108">Syntax</span></span>


```mof
uint32 GetWinstationDriverNames(
  [out] string WinstaDriverNames[]
);
```



## <a name="parameters"></a><span data-ttu-id="17dca-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="17dca-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17dca-110">*WinstaDriverNames* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="17dca-110">*WinstaDriverNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17dca-111">Lista de los nombres de controlador de la estación de la</span><span class="sxs-lookup"><span data-stu-id="17dca-111">The list of Winstation driver names.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17dca-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17dca-112">Remarks</span></span>

<span data-ttu-id="17dca-113">Para conectarse al \\ espacio de \\ nombres TerminalServices de cimv2 raíz \\ , el nivel de autenticación debe incluir privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="17dca-113">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="17dca-114">En el caso de las llamadas de C/C++, se trata de un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C.</span><span class="sxs-lookup"><span data-stu-id="17dca-114">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="17dca-115">En el caso de las llamadas de Visual Basic y scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6.</span><span class="sxs-lookup"><span data-stu-id="17dca-115">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="17dca-116">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="17dca-116">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="17dca-117">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="17dca-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="17dca-118">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="17dca-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="17dca-119">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="17dca-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="17dca-120">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="17dca-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="17dca-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17dca-121">Requirements</span></span>



| <span data-ttu-id="17dca-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="17dca-122">Requirement</span></span> | <span data-ttu-id="17dca-123">Value</span><span class="sxs-lookup"><span data-stu-id="17dca-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17dca-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17dca-124">Minimum supported client</span></span><br/> | <span data-ttu-id="17dca-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17dca-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="17dca-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17dca-126">Minimum supported server</span></span><br/> | <span data-ttu-id="17dca-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17dca-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="17dca-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="17dca-128">Namespace</span></span><br/>                | <span data-ttu-id="17dca-129">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="17dca-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="17dca-130">MOF</span><span class="sxs-lookup"><span data-stu-id="17dca-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17dca-131"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17dca-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="17dca-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="17dca-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17dca-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17dca-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17dca-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="17dca-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17dca-135">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="17dca-135">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

