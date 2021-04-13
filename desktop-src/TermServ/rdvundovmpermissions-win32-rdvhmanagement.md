---
title: Método RdvUndoVMPermissions de la clase Win32_RdvhManagement
description: Revierte los permisos establecidos por RdvSetupVMPermissions en la máquina virtual especificada.
ms.assetid: 3331430e-7427-42f7-ab09-27fece8dc3ca
ms.tgt_platform: multiple
keywords:
- Método RdvUndoVMPermissions Servicios de Escritorio remoto
- Método RdvUndoVMPermissions Servicios de Escritorio remoto, clase Win32_RdvhManagement
- Win32_RdvhManagement de clase Servicios de Escritorio remoto, método RdvUndoVMPermissions
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvUndoVMPermissions
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1dc8892435522dcd2c7457fe4b74a0d9671740
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492760"
---
# <a name="rdvundovmpermissions-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="523a7-106">Método RdvUndoVMPermissions de la \_ clase RdvhManagement de Win32</span><span class="sxs-lookup"><span data-stu-id="523a7-106">RdvUndoVMPermissions method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="523a7-107">Revierte los permisos establecidos por [**RdvSetupVMPermissions**](rdvsetupvmpermissions-win32-rdvhmanagement.md) en la máquina virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="523a7-107">Reverts permissions set by [**RdvSetupVMPermissions**](rdvsetupvmpermissions-win32-rdvhmanagement.md) on the specified virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="523a7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="523a7-108">Syntax</span></span>


```mof
uint32 RdvUndoVMPermissions(
  [in] string VmName
);
```



## <a name="parameters"></a><span data-ttu-id="523a7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="523a7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="523a7-110">*VmName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="523a7-110">*VmName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="523a7-111">Nombre de la máquina virtual en la que se van a deshacer los permisos.</span><span class="sxs-lookup"><span data-stu-id="523a7-111">Name of the virtual machine to undo permissions on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="523a7-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="523a7-112">Return value</span></span>

<span data-ttu-id="523a7-113">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="523a7-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="523a7-114">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="523a7-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="523a7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="523a7-115">Requirements</span></span>



| <span data-ttu-id="523a7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="523a7-116">Requirement</span></span> | <span data-ttu-id="523a7-117">Value</span><span class="sxs-lookup"><span data-stu-id="523a7-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="523a7-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="523a7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="523a7-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="523a7-119">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="523a7-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="523a7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="523a7-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="523a7-121">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="523a7-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="523a7-122">Namespace</span></span><br/>                | <span data-ttu-id="523a7-123">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="523a7-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="523a7-124">MOF</span><span class="sxs-lookup"><span data-stu-id="523a7-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="523a7-125"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="523a7-125"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="523a7-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="523a7-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="523a7-127"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="523a7-127"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="523a7-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="523a7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="523a7-129">**Win32 \_ RdvhManagement**</span><span class="sxs-lookup"><span data-stu-id="523a7-129">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





