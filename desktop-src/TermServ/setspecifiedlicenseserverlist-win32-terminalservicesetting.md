---
title: Método SetSpecifiedLicenseServerList de la clase Win32_TerminalServiceSetting
description: Actualiza la lista de servidores de licencias especificados, reemplazando los servidores de licencias especificados.
ms.assetid: afd7ca11-9db5-4cf3-9706-3c6984789ecd
ms.tgt_platform: multiple
keywords:
- Método SetSpecifiedLicenseServerList Servicios de Escritorio remoto
- Método SetSpecifiedLicenseServerList Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método SetSpecifiedLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d10fde34e490f26c287e63dcddae3c62761670bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686056"
---
# <a name="setspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="9ef85-106">Método SetSpecifiedLicenseServerList de la \_ clase TerminalServiceSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="9ef85-106">SetSpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="9ef85-107">Actualiza la lista de servidores de licencias especificados, reemplazando los servidores de licencias especificados.</span><span class="sxs-lookup"><span data-stu-id="9ef85-107">Updates the list of specified license servers, replacing any existing specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ef85-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ef85-108">Syntax</span></span>


```mof
uint32 SetSpecifiedLicenseServerList(
  [in] string SpecifiedLSList[]
);
```



## <a name="parameters"></a><span data-ttu-id="9ef85-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ef85-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ef85-110">*SpecifiedLSList* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9ef85-110">*SpecifiedLSList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ef85-111">Matriz de cadenas que contiene la nueva lista de servidores de licencias especificados.</span><span class="sxs-lookup"><span data-stu-id="9ef85-111">A string array that contains the new list of specified license servers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ef85-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9ef85-112">Return value</span></span>

<span data-ttu-id="9ef85-113">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="9ef85-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="9ef85-114">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="9ef85-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ef85-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ef85-115">Requirements</span></span>



| <span data-ttu-id="9ef85-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ef85-116">Requirement</span></span> | <span data-ttu-id="9ef85-117">Value</span><span class="sxs-lookup"><span data-stu-id="9ef85-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ef85-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ef85-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9ef85-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9ef85-119">None supported</span></span><br/>                                                               |
| <span data-ttu-id="9ef85-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ef85-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9ef85-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9ef85-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="9ef85-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9ef85-122">Namespace</span></span><br/>                | <span data-ttu-id="9ef85-123">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="9ef85-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="9ef85-124">MOF</span><span class="sxs-lookup"><span data-stu-id="9ef85-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ef85-125"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ef85-125"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ef85-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9ef85-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ef85-127"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ef85-127"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ef85-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ef85-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ef85-129">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="9ef85-129">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="9ef85-130">**AddLSToSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="9ef85-130">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="9ef85-131">**GetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="9ef85-131">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="9ef85-132">**EmptySpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="9ef85-132">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="9ef85-133">**RemoveLSFromSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="9ef85-133">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





