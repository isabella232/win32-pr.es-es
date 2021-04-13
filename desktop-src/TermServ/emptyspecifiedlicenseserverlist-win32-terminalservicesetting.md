---
title: Método EmptySpecifiedLicenseServerList de la clase Win32_TerminalServiceSetting
description: Quita todos los servidores de licencias de la lista de servidores de licencias especificados.
ms.assetid: de1633ca-3f0b-4540-8b45-44303a4e72fe
ms.tgt_platform: multiple
keywords:
- Método EmptySpecifiedLicenseServerList Servicios de Escritorio remoto
- Método EmptySpecifiedLicenseServerList Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método EmptySpecifiedLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.EmptySpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1392c05618860f742a13140167e423b312e49b0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493211"
---
# <a name="emptyspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="891ef-106">Método EmptySpecifiedLicenseServerList de la \_ clase TerminalServiceSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="891ef-106">EmptySpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="891ef-107">Quita todos los servidores de licencias de la lista de servidores de licencias especificados.</span><span class="sxs-lookup"><span data-stu-id="891ef-107">Removes all license servers from the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="891ef-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="891ef-108">Syntax</span></span>


```mof
uint32 EmptySpecifiedLicenseServerList();
```



## <a name="parameters"></a><span data-ttu-id="891ef-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="891ef-109">Parameters</span></span>

<span data-ttu-id="891ef-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="891ef-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="891ef-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="891ef-111">Return value</span></span>

<span data-ttu-id="891ef-112">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="891ef-112">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="891ef-113">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="891ef-113">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="891ef-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="891ef-114">Requirements</span></span>



| <span data-ttu-id="891ef-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="891ef-115">Requirement</span></span> | <span data-ttu-id="891ef-116">Value</span><span class="sxs-lookup"><span data-stu-id="891ef-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="891ef-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="891ef-117">Minimum supported client</span></span><br/> | <span data-ttu-id="891ef-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="891ef-118">None supported</span></span><br/>                                                               |
| <span data-ttu-id="891ef-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="891ef-119">Minimum supported server</span></span><br/> | <span data-ttu-id="891ef-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="891ef-120">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="891ef-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="891ef-121">Namespace</span></span><br/>                | <span data-ttu-id="891ef-122">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="891ef-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="891ef-123">MOF</span><span class="sxs-lookup"><span data-stu-id="891ef-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="891ef-124"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="891ef-124"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="891ef-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="891ef-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="891ef-126"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="891ef-126"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="891ef-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="891ef-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="891ef-128">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="891ef-128">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="891ef-129">**AddLSToSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="891ef-129">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="891ef-130">**GetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="891ef-130">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="891ef-131">**RemoveLSFromSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="891ef-131">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="891ef-132">**SetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="891ef-132">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





