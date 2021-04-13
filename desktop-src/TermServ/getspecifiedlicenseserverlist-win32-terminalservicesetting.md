---
title: Método GetSpecifiedLicenseServerList de la clase Win32_TerminalServiceSetting
description: Recupera la lista de servidores de licencias especificados.
ms.assetid: 800be0ce-1002-48e1-be4e-88db22590f12
ms.tgt_platform: multiple
keywords:
- Método GetSpecifiedLicenseServerList Servicios de Escritorio remoto
- Método GetSpecifiedLicenseServerList Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método GetSpecifiedLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f70c50281cad7072d420082db0e6916a631e2b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422008"
---
# <a name="getspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="f84da-106">Método GetSpecifiedLicenseServerList de la \_ clase TerminalServiceSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="f84da-106">GetSpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="f84da-107">Recupera la lista de servidores de licencias especificados.</span><span class="sxs-lookup"><span data-stu-id="f84da-107">Retrieves the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="f84da-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f84da-108">Syntax</span></span>


```mof
uint32 GetSpecifiedLicenseServerList(
  [out] string SpecifiedLSList[]
);
```



## <a name="parameters"></a><span data-ttu-id="f84da-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f84da-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f84da-110">*SpecifiedLSList* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f84da-110">*SpecifiedLSList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f84da-111">Una matriz de cadena que recibe la lista de servidores de licencias.</span><span class="sxs-lookup"><span data-stu-id="f84da-111">A string array that receives the list of license servers.</span></span> <span data-ttu-id="f84da-112">Si no hay servidores de licencias, esta matriz estará vacía.</span><span class="sxs-lookup"><span data-stu-id="f84da-112">If there are no license servers, this array will be empty.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f84da-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f84da-113">Return value</span></span>

<span data-ttu-id="f84da-114">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="f84da-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="f84da-115">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="f84da-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="f84da-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f84da-116">Requirements</span></span>



| <span data-ttu-id="f84da-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f84da-117">Requirement</span></span> | <span data-ttu-id="f84da-118">Value</span><span class="sxs-lookup"><span data-stu-id="f84da-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f84da-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f84da-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f84da-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f84da-120">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f84da-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f84da-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f84da-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f84da-122">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="f84da-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f84da-123">Namespace</span></span><br/>                | <span data-ttu-id="f84da-124">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f84da-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f84da-125">MOF</span><span class="sxs-lookup"><span data-stu-id="f84da-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f84da-126"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f84da-126"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f84da-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f84da-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f84da-128"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f84da-128"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f84da-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="f84da-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f84da-130">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="f84da-130">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="f84da-131">**AddLSToSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="f84da-131">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="f84da-132">**EmptySpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="f84da-132">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="f84da-133">**RemoveLSFromSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="f84da-133">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="f84da-134">**SetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="f84da-134">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





