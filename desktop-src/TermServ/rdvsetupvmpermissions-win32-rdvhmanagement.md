---
title: Método RdvSetupVMPermissions de la clase Win32_RdvhManagement
description: Establece los permisos en una máquina virtual para el usuario actual.
ms.assetid: 6ac45983-d468-4a3b-875f-48717ba23ed0
ms.tgt_platform: multiple
keywords:
- Método RdvSetupVMPermissions Servicios de Escritorio remoto
- Método RdvSetupVMPermissions Servicios de Escritorio remoto, clase Win32_RdvhManagement
- Win32_RdvhManagement de clase Servicios de Escritorio remoto, método RdvSetupVMPermissions
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvSetupVMPermissions
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd8028a33bc772f9dd37f25a1dc22074baf771b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490606"
---
# <a name="rdvsetupvmpermissions-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="e871b-106">Método RdvSetupVMPermissions de la \_ clase RdvhManagement de Win32</span><span class="sxs-lookup"><span data-stu-id="e871b-106">RdvSetupVMPermissions method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="e871b-107">Establece los permisos en una máquina virtual para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="e871b-107">Sets the permissions on a virtual machine for the current user.</span></span>

## <a name="syntax"></a><span data-ttu-id="e871b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e871b-108">Syntax</span></span>


```mof
uint32 RdvSetupVMPermissions(
  [in] string VmName
);
```



## <a name="parameters"></a><span data-ttu-id="e871b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e871b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e871b-110">*VmName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e871b-110">*VmName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e871b-111">Nombre de la máquina virtual en la que se van a establecer los permisos.</span><span class="sxs-lookup"><span data-stu-id="e871b-111">The name of the virtual machine to set permissions on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e871b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e871b-112">Return value</span></span>

<span data-ttu-id="e871b-113">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="e871b-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="e871b-114">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="e871b-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="e871b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e871b-115">Requirements</span></span>



| <span data-ttu-id="e871b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e871b-116">Requirement</span></span> | <span data-ttu-id="e871b-117">Value</span><span class="sxs-lookup"><span data-stu-id="e871b-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e871b-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e871b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e871b-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e871b-119">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="e871b-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e871b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e871b-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e871b-121">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="e871b-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e871b-122">Namespace</span></span><br/>                | <span data-ttu-id="e871b-123">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="e871b-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="e871b-124">MOF</span><span class="sxs-lookup"><span data-stu-id="e871b-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e871b-125"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e871b-125"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="e871b-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e871b-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e871b-127"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e871b-127"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e871b-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="e871b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e871b-129">**Win32 \_ RdvhManagement**</span><span class="sxs-lookup"><span data-stu-id="e871b-129">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





