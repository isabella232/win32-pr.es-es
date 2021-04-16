---
title: Método GetRegisteredLicenseServerList de la clase Win32_TerminalServiceSetting
description: Obtiene la lista de servidores de licencias registrados.
ms.assetid: 32e06b4b-652f-4977-be1f-6d52983d2605
ms.tgt_platform: multiple
keywords:
- Método GetRegisteredLicenseServerList Servicios de Escritorio remoto
- Método GetRegisteredLicenseServerList Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método GetRegisteredLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetRegisteredLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5336910956a0d281fbfc8fbc65e1d3b8d5018cb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686178"
---
# <a name="getregisteredlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="24eee-106">Método GetRegisteredLicenseServerList de la \_ clase TerminalServiceSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="24eee-106">GetRegisteredLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="24eee-107">Obtiene la lista de servidores de licencias registrados.</span><span class="sxs-lookup"><span data-stu-id="24eee-107">Gets the list of registered license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="24eee-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="24eee-108">Syntax</span></span>


```mof
uint32 GetRegisteredLicenseServerList(
  [out] string RegisteredLSList[]
);
```



## <a name="parameters"></a><span data-ttu-id="24eee-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="24eee-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24eee-110">*RegisteredLSList* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="24eee-110">*RegisteredLSList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24eee-111">Una matriz de cadena que recibe la lista de servidores de licencias registrados.</span><span class="sxs-lookup"><span data-stu-id="24eee-111">A string array that receives the list of registered license servers.</span></span> <span data-ttu-id="24eee-112">Si no hay servidores de licencias registrados, esta matriz estará vacía.</span><span class="sxs-lookup"><span data-stu-id="24eee-112">If there are no registered license servers, this array will be empty.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24eee-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="24eee-113">Return value</span></span>

<span data-ttu-id="24eee-114">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="24eee-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="24eee-115">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="24eee-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="24eee-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24eee-116">Requirements</span></span>



| <span data-ttu-id="24eee-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="24eee-117">Requirement</span></span> | <span data-ttu-id="24eee-118">Value</span><span class="sxs-lookup"><span data-stu-id="24eee-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24eee-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24eee-119">Minimum supported client</span></span><br/> | <span data-ttu-id="24eee-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="24eee-120">None supported</span></span><br/>                                                               |
| <span data-ttu-id="24eee-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24eee-121">Minimum supported server</span></span><br/> | <span data-ttu-id="24eee-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="24eee-122">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="24eee-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="24eee-123">Namespace</span></span><br/>                | <span data-ttu-id="24eee-124">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="24eee-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="24eee-125">MOF</span><span class="sxs-lookup"><span data-stu-id="24eee-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24eee-126"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="24eee-126"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="24eee-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="24eee-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24eee-128"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24eee-128"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24eee-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="24eee-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24eee-130">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="24eee-130">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 





