---
title: Método AddDirectConnectLicenseServer de la clase Win32_TerminalServiceSetting
description: AddDirectConnectLicenseServer ya no está disponible.
ms.assetid: 7920fd28-0fa3-4f96-bec3-d9e37c97920c
ms.tgt_platform: multiple
keywords:
- Método AddDirectConnectLicenseServer Servicios de Escritorio remoto
- Método AddDirectConnectLicenseServer Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método AddDirectConnectLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.AddDirectConnectLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be9bba23f5c0bfc69b4c8d7951ab38eac6690b84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422562"
---
# <a name="adddirectconnectlicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="6cf40-106">Método AddDirectConnectLicenseServer de la \_ clase TerminalServiceSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="6cf40-106">AddDirectConnectLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="6cf40-107">\[**AddDirectConnectLicenseServer** ya no está disponible para su uso a partir de Windows Server 2008 R2.\]</span><span class="sxs-lookup"><span data-stu-id="6cf40-107">\[**AddDirectConnectLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="6cf40-108">**Windows Server 2008:** Configura un nuevo servidor de licencias y agrega el servidor de licencias al registro para que lo pueda detectar Escritorio remoto servidores host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="6cf40-108">**Windows Server 2008:** Configures a new license server and adds the license server to the registry for discovery by Remote Desktop Session Host (RD Session Host) servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cf40-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6cf40-109">Syntax</span></span>


```mof
uint32 AddDirectConnectLicenseServer(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a><span data-ttu-id="6cf40-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6cf40-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cf40-111">*LicenseServerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6cf40-111">*LicenseServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cf40-112">Nombre del servidor de licencias que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="6cf40-112">Name of the license server to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cf40-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6cf40-113">Return value</span></span>

<span data-ttu-id="6cf40-114">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="6cf40-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="6cf40-115">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="6cf40-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cf40-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6cf40-116">Remarks</span></span>

<span data-ttu-id="6cf40-117">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="6cf40-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6cf40-118">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6cf40-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6cf40-119">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="6cf40-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6cf40-120">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6cf40-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6cf40-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cf40-121">Requirements</span></span>



| <span data-ttu-id="6cf40-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cf40-122">Requirement</span></span> | <span data-ttu-id="6cf40-123">Value</span><span class="sxs-lookup"><span data-stu-id="6cf40-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6cf40-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6cf40-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6cf40-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6cf40-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6cf40-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6cf40-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6cf40-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6cf40-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6cf40-128">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="6cf40-128">End of client support</span></span><br/>    | <span data-ttu-id="6cf40-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6cf40-129">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6cf40-130">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="6cf40-130">End of server support</span></span><br/>    | <span data-ttu-id="6cf40-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6cf40-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6cf40-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6cf40-132">Namespace</span></span><br/>                | <span data-ttu-id="6cf40-133">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="6cf40-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="6cf40-134">MOF</span><span class="sxs-lookup"><span data-stu-id="6cf40-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6cf40-135"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6cf40-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="6cf40-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6cf40-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cf40-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cf40-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cf40-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="6cf40-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cf40-139">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="6cf40-139">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

