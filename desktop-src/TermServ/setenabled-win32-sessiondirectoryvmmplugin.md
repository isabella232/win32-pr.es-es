---
title: Método SetEnabled de la clase Win32_SessionDirectoryVMMPlugin
description: Habilita o deshabilita el complemento.
ms.assetid: 25ce0614-5c3b-4a79-9174-1a9de1eb6c33
ms.tgt_platform: multiple
keywords:
- Método SetEnabled Servicios de Escritorio remoto
- Método SetEnabled Servicios de Escritorio remoto, clase Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin Servicios de Escritorio remoto de clase, método SetEnabled
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetEnabled
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7089a21f143b6f3b27fe9fe58563e6777bf2f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803859"
---
# <a name="setenabled-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="a30dc-106">Método SetEnabled de la \_ clase SessionDirectoryVMMPlugin de Win32</span><span class="sxs-lookup"><span data-stu-id="a30dc-106">SetEnabled method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="a30dc-107">Habilita o deshabilita el complemento.</span><span class="sxs-lookup"><span data-stu-id="a30dc-107">Enables or disables the plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="a30dc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a30dc-108">Syntax</span></span>


```mof
uint32 SetEnabled(
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="a30dc-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a30dc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a30dc-110">*Habilitado* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a30dc-110">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a30dc-111">Indica si el complemento está habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="a30dc-111">Indicates whether the plug-in is enabled or disabled.</span></span> <span data-ttu-id="a30dc-112">**True** si el complemento está habilitado o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a30dc-112">**True** if the plug-in is enabled or **false** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a30dc-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a30dc-113">Return value</span></span>

<span data-ttu-id="a30dc-114">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="a30dc-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="a30dc-115">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="a30dc-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="a30dc-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a30dc-116">Requirements</span></span>



| <span data-ttu-id="a30dc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a30dc-117">Requirement</span></span> | <span data-ttu-id="a30dc-118">Value</span><span class="sxs-lookup"><span data-stu-id="a30dc-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a30dc-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a30dc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a30dc-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a30dc-120">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a30dc-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a30dc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a30dc-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a30dc-122">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="a30dc-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a30dc-123">Namespace</span></span><br/>                | <span data-ttu-id="a30dc-124">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="a30dc-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="a30dc-125">MOF</span><span class="sxs-lookup"><span data-stu-id="a30dc-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a30dc-126"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a30dc-126"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a30dc-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a30dc-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a30dc-128"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a30dc-128"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a30dc-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="a30dc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a30dc-130">**Win32 \_ SessionDirectoryVMMPlugin**</span><span class="sxs-lookup"><span data-stu-id="a30dc-130">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





