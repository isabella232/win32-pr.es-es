---
title: Método RemoveLSFromSpecifiedLicenseServerList de la clase Win32_TerminalServiceSetting
description: Quita el servidor de licencias dado de la lista de servidores de licencias especificados.
ms.assetid: c25eebf9-3a21-41a0-bb7d-c3f909cd8087
ms.tgt_platform: multiple
keywords:
- Método RemoveLSFromSpecifiedLicenseServerList Servicios de Escritorio remoto
- Método RemoveLSFromSpecifiedLicenseServerList Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método RemoveLSFromSpecifiedLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.RemoveLSFromSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 901c2676748e819290855df2de51e5d7936dc793
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905250"
---
# <a name="removelsfromspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="5bbe8-106">Método RemoveLSFromSpecifiedLicenseServerList de la \_ clase TerminalServiceSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="5bbe8-106">RemoveLSFromSpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="5bbe8-107">Quita el servidor de licencias dado de la lista de servidores de licencias especificados.</span><span class="sxs-lookup"><span data-stu-id="5bbe8-107">Removes the given license server from the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bbe8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5bbe8-108">Syntax</span></span>


```mof
uint32 RemoveLSFromSpecifiedLicenseServerList(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a><span data-ttu-id="5bbe8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5bbe8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bbe8-110">*LicenseServerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5bbe8-110">*LicenseServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bbe8-111">Nombre del servidor de licencias que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="5bbe8-111">The name of the license server to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bbe8-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5bbe8-112">Return value</span></span>

<span data-ttu-id="5bbe8-113">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="5bbe8-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="5bbe8-114">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="5bbe8-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bbe8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bbe8-115">Requirements</span></span>



| <span data-ttu-id="5bbe8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bbe8-116">Requirement</span></span> | <span data-ttu-id="5bbe8-117">Value</span><span class="sxs-lookup"><span data-stu-id="5bbe8-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5bbe8-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5bbe8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5bbe8-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5bbe8-119">None supported</span></span><br/>                                                               |
| <span data-ttu-id="5bbe8-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5bbe8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5bbe8-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5bbe8-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="5bbe8-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5bbe8-122">Namespace</span></span><br/>                | <span data-ttu-id="5bbe8-123">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="5bbe8-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="5bbe8-124">MOF</span><span class="sxs-lookup"><span data-stu-id="5bbe8-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5bbe8-125"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5bbe8-125"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="5bbe8-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5bbe8-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bbe8-127"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5bbe8-127"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bbe8-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="5bbe8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bbe8-129">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="5bbe8-129">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="5bbe8-130">**AddLSToSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="5bbe8-130">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="5bbe8-131">**EmptySpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="5bbe8-131">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="5bbe8-132">**GetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="5bbe8-132">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="5bbe8-133">**SetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="5bbe8-133">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





