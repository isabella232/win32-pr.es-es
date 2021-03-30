---
title: Método EnableCentralCAP de la clase Win32_TSGatewayServerSettings
description: Controla la propiedad CentralCAPEnabled, que controla las directivas de autorización de conexión Servicios de Escritorio remoto (RD \ 160; Cap) del servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: 43e476df-714d-43bd-b40f-33511b7757a4
ms.tgt_platform: multiple
keywords:
- Método EnableCentralCAP Servicios de Escritorio remoto
- Método EnableCentralCAP Servicios de Escritorio remoto, clase Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de clase Servicios de Escritorio remoto, método EnableCentralCAP
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableCentralCAP
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 933e91a89f9a5afdcd2ae85fa6cb097ef0c29cd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422630"
---
# <a name="enablecentralcap-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="4f177-106">Método EnableCentralCAP de la \_ clase TSGatewayServerSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="4f177-106">EnableCentralCAP method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="4f177-107">Controla la propiedad **CentralCAPEnabled** , que controla el servicios de escritorio remoto las directivas de autorización de conexión (Cap de RD) para el servidor de puerta de enlace de escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="4f177-107">Controls the **CentralCAPEnabled** property, which controls the Remote Desktop Services connection authorization policies (RD CAPs) for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f177-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f177-108">Syntax</span></span>


```mof
uint32 EnableCentralCAP(
  [in] boolean CentralCAPEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="4f177-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4f177-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f177-110">*CentralCAPEnabled* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4f177-110">*CentralCAPEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f177-111">Si se establece en **true**, se usarán las Cap de RD desde los servidores de Cap de RD centrales.</span><span class="sxs-lookup"><span data-stu-id="4f177-111">If set to **True**, RD CAPs from central RD CAP servers will be used.</span></span> <span data-ttu-id="4f177-112">Si se establece en **false**, solo se usarán las directivas del servidor local.</span><span class="sxs-lookup"><span data-stu-id="4f177-112">If set to **False**, only policies from the local server will be used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f177-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4f177-113">Return value</span></span>

<span data-ttu-id="4f177-114">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="4f177-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="4f177-115">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="4f177-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="4f177-116">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="4f177-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4f177-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4f177-117">Remarks</span></span>

<span data-ttu-id="4f177-118">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="4f177-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="4f177-119">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="4f177-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4f177-120">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="4f177-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4f177-121">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="4f177-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4f177-122">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="4f177-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f177-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f177-123">Requirements</span></span>



| <span data-ttu-id="4f177-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f177-124">Requirement</span></span> | <span data-ttu-id="4f177-125">Value</span><span class="sxs-lookup"><span data-stu-id="4f177-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f177-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f177-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4f177-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4f177-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="4f177-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f177-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4f177-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f177-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="4f177-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4f177-130">Namespace</span></span><br/>                | <span data-ttu-id="4f177-131">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="4f177-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="4f177-132">MOF</span><span class="sxs-lookup"><span data-stu-id="4f177-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f177-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f177-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f177-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4f177-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f177-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f177-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="4f177-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f177-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f177-137">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="4f177-137">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

