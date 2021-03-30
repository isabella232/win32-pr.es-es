---
title: Método RdvMigrateVmToDifferentHost de la clase Win32_RdvhManagement
description: Inicia una migración en vivo de una máquina virtual a un host especificado.
ms.assetid: aa4b1e57-a97c-410b-9b9d-423a1c77de70
ms.tgt_platform: multiple
keywords:
- Método RdvMigrateVmToDifferentHost Servicios de Escritorio remoto
- Método RdvMigrateVmToDifferentHost Servicios de Escritorio remoto, clase Win32_RdvhManagement
- Win32_RdvhManagement de clase Servicios de Escritorio remoto, método RdvMigrateVmToDifferentHost
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvMigrateVmToDifferentHost
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3def1be6332397fb3830ffe8c90f324afc9f1b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802270"
---
# <a name="rdvmigratevmtodifferenthost-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="3b393-106">Método RdvMigrateVmToDifferentHost de la \_ clase RdvhManagement de Win32</span><span class="sxs-lookup"><span data-stu-id="3b393-106">RdvMigrateVmToDifferentHost method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="3b393-107">Inicia una migración en vivo de una máquina virtual a un host especificado.</span><span class="sxs-lookup"><span data-stu-id="3b393-107">Initiates a live migration of a virtual machine to a specified host.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b393-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b393-108">Syntax</span></span>


```mof
uint32 RdvMigrateVmToDifferentHost(
  [in] string VmName,
  [in] string DestinationHost
);
```



## <a name="parameters"></a><span data-ttu-id="3b393-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b393-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b393-110">*VmName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3b393-110">*VmName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b393-111">Nombre de la máquina virtual que se va a migrar.</span><span class="sxs-lookup"><span data-stu-id="3b393-111">Name of the virtual machine to migrate.</span></span>

</dd> <dt>

<span data-ttu-id="3b393-112">*DestinationHost* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3b393-112">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b393-113">nombre del host de destino.</span><span class="sxs-lookup"><span data-stu-id="3b393-113">name of the destination host.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b393-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b393-114">Return value</span></span>

<span data-ttu-id="3b393-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="3b393-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="3b393-116">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="3b393-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b393-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b393-117">Requirements</span></span>



| <span data-ttu-id="3b393-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b393-118">Requirement</span></span> | <span data-ttu-id="3b393-119">Value</span><span class="sxs-lookup"><span data-stu-id="3b393-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b393-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b393-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3b393-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3b393-121">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="3b393-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b393-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3b393-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3b393-123">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="3b393-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3b393-124">Namespace</span></span><br/>                | <span data-ttu-id="3b393-125">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="3b393-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="3b393-126">MOF</span><span class="sxs-lookup"><span data-stu-id="3b393-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b393-127"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b393-127"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="3b393-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3b393-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b393-129"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b393-129"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b393-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b393-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b393-131">**Win32 \_ RdvhManagement**</span><span class="sxs-lookup"><span data-stu-id="3b393-131">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





