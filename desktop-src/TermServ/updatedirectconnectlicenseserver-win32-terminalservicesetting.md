---
title: Método UpdateDirectConnectLicenseServer de la clase Win32_TerminalServiceSetting
description: UpdateDirectConnectLicenseServer ya no está disponible.
ms.assetid: 0b6e0dba-e23b-4c8d-8021-93d802501359
ms.tgt_platform: multiple
keywords:
- Método UpdateDirectConnectLicenseServer Servicios de Escritorio remoto
- Método UpdateDirectConnectLicenseServer Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método UpdateDirectConnectLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.UpdateDirectConnectLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2249dd00b44955a4e2712b8b7bf746793e89d57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676771"
---
# <a name="updatedirectconnectlicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="c72fe-106">Método UpdateDirectConnectLicenseServer de la \_ clase TerminalServiceSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="c72fe-106">UpdateDirectConnectLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="c72fe-107">\[**UpdateDirectConnectLicenseServer** ya no está disponible para su uso a partir de Windows Server 2008 R2.\]</span><span class="sxs-lookup"><span data-stu-id="c72fe-107">\[**UpdateDirectConnectLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="c72fe-108">**Windows Server 2008:** Actualiza la lista de servidores de licencias de detección.</span><span class="sxs-lookup"><span data-stu-id="c72fe-108">**Windows Server 2008:** Updates the list of discovery license servers.</span></span> <span data-ttu-id="c72fe-109">La lista de servidores está delimitada por signos de punto y coma (";").</span><span class="sxs-lookup"><span data-stu-id="c72fe-109">The server list is delimited by semicolons (";").</span></span>

## <a name="syntax"></a><span data-ttu-id="c72fe-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c72fe-110">Syntax</span></span>


```mof
uint32 UpdateDirectConnectLicenseServer(
  [in] string LicenseServerList
);
```



## <a name="parameters"></a><span data-ttu-id="c72fe-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c72fe-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c72fe-112">*LicenseServerList* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c72fe-112">*LicenseServerList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c72fe-113">Lista de servidores de licencias.</span><span class="sxs-lookup"><span data-stu-id="c72fe-113">List of license servers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c72fe-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c72fe-114">Return value</span></span>

<span data-ttu-id="c72fe-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="c72fe-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="c72fe-116">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="c72fe-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="c72fe-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c72fe-117">Remarks</span></span>

<span data-ttu-id="c72fe-118">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="c72fe-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c72fe-119">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c72fe-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c72fe-120">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="c72fe-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c72fe-121">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c72fe-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c72fe-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c72fe-122">Requirements</span></span>



| <span data-ttu-id="c72fe-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c72fe-123">Requirement</span></span> | <span data-ttu-id="c72fe-124">Value</span><span class="sxs-lookup"><span data-stu-id="c72fe-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c72fe-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c72fe-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c72fe-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c72fe-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c72fe-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c72fe-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c72fe-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c72fe-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c72fe-129">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="c72fe-129">End of client support</span></span><br/>    | <span data-ttu-id="c72fe-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c72fe-130">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c72fe-131">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="c72fe-131">End of server support</span></span><br/>    | <span data-ttu-id="c72fe-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c72fe-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c72fe-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c72fe-133">Namespace</span></span><br/>                | <span data-ttu-id="c72fe-134">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="c72fe-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c72fe-135">MOF</span><span class="sxs-lookup"><span data-stu-id="c72fe-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c72fe-136"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c72fe-136"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c72fe-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c72fe-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c72fe-138"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c72fe-138"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c72fe-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="c72fe-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c72fe-140">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="c72fe-140">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

