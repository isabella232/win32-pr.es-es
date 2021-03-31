---
title: Método AddLSToSpecifiedLicenseServerList de la clase Win32_TerminalServiceSetting
description: Agrega el servidor de licencias especificado al final de la lista de servidores de licencias especificados.
ms.assetid: 2aebe7c0-5ec2-4c2d-9887-7ecd2d6ec02a
ms.tgt_platform: multiple
keywords:
- Método AddLSToSpecifiedLicenseServerList Servicios de Escritorio remoto
- Método AddLSToSpecifiedLicenseServerList Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método AddLSToSpecifiedLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.AddLSToSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c53a5279523405b760addabb03e381507775e6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996147"
---
# <a name="addlstospecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="72daa-106">Método AddLSToSpecifiedLicenseServerList de la \_ clase TerminalServiceSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="72daa-106">AddLSToSpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="72daa-107">Agrega el servidor de licencias especificado al final de la lista de servidores de licencias especificados.</span><span class="sxs-lookup"><span data-stu-id="72daa-107">Adds the given license server to the end of the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="72daa-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="72daa-108">Syntax</span></span>


```mof
uint32 AddLSToSpecifiedLicenseServerList(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a><span data-ttu-id="72daa-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="72daa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72daa-110">*LicenseServerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="72daa-110">*LicenseServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72daa-111">Nombre del servidor de licencias que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="72daa-111">The name of the license server to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72daa-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="72daa-112">Return value</span></span>

<span data-ttu-id="72daa-113">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="72daa-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="72daa-114">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="72daa-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="72daa-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72daa-115">Requirements</span></span>



| <span data-ttu-id="72daa-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="72daa-116">Requirement</span></span> | <span data-ttu-id="72daa-117">Value</span><span class="sxs-lookup"><span data-stu-id="72daa-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72daa-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72daa-118">Minimum supported client</span></span><br/> | <span data-ttu-id="72daa-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="72daa-119">None supported</span></span><br/>                                                               |
| <span data-ttu-id="72daa-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72daa-120">Minimum supported server</span></span><br/> | <span data-ttu-id="72daa-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="72daa-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="72daa-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="72daa-122">Namespace</span></span><br/>                | <span data-ttu-id="72daa-123">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="72daa-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="72daa-124">MOF</span><span class="sxs-lookup"><span data-stu-id="72daa-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72daa-125"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72daa-125"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="72daa-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="72daa-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72daa-127"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72daa-127"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72daa-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="72daa-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72daa-129">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="72daa-129">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="72daa-130">**EmptySpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="72daa-130">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="72daa-131">**GetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="72daa-131">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="72daa-132">**RemoveLSFromSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="72daa-132">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="72daa-133">**SetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="72daa-133">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





