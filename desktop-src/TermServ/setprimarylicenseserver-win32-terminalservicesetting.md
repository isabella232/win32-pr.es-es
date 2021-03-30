---
title: Método SetPrimaryLicenseServer de la clase Win32_TerminalServiceSetting
description: Establece el servidor de licencias dado como la primera entrada de la lista de servidores de licencias especificados.
ms.assetid: 8921e861-3b9a-49c5-a691-ded7be18ca0a
ms.tgt_platform: multiple
keywords:
- Método SetPrimaryLicenseServer Servicios de Escritorio remoto
- Método SetPrimaryLicenseServer Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método SetPrimaryLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetPrimaryLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61d73212230d1ca69e0a0809c48b8f2985920045
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905084"
---
# <a name="setprimarylicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="75852-106">Método SetPrimaryLicenseServer de la \_ clase TerminalServiceSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="75852-106">SetPrimaryLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="75852-107">Establece el servidor de licencias dado como la primera entrada de la lista de servidores de licencias especificados.</span><span class="sxs-lookup"><span data-stu-id="75852-107">Sets the given license server as the first entry in the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="75852-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75852-108">Syntax</span></span>


```mof
uint32 SetPrimaryLicenseServer(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a><span data-ttu-id="75852-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75852-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75852-110">*LicenseServerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="75852-110">*LicenseServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75852-111">Nombre del servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="75852-111">The name of the license server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75852-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75852-112">Return value</span></span>

<span data-ttu-id="75852-113">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="75852-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="75852-114">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="75852-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="75852-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75852-115">Requirements</span></span>



| <span data-ttu-id="75852-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="75852-116">Requirement</span></span> | <span data-ttu-id="75852-117">Value</span><span class="sxs-lookup"><span data-stu-id="75852-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75852-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75852-118">Minimum supported client</span></span><br/> | <span data-ttu-id="75852-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="75852-119">None supported</span></span><br/>                                                               |
| <span data-ttu-id="75852-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75852-120">Minimum supported server</span></span><br/> | <span data-ttu-id="75852-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="75852-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="75852-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="75852-122">Namespace</span></span><br/>                | <span data-ttu-id="75852-123">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="75852-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="75852-124">MOF</span><span class="sxs-lookup"><span data-stu-id="75852-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75852-125"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="75852-125"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="75852-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="75852-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75852-127"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75852-127"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75852-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="75852-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75852-129">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="75852-129">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 





