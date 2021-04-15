---
title: Método RdvCopyBaseVmLocally de la clase Win32_RdvhManagement
description: Copia una máquina virtual base local en un servidor host de virtualización de escritorio remoto (RDV) especificado.
ms.assetid: 13c0c629-42c6-4689-9740-f13f31688e42
ms.tgt_platform: multiple
keywords:
- Método RdvCopyBaseVmLocally Servicios de Escritorio remoto
- Método RdvCopyBaseVmLocally Servicios de Escritorio remoto, clase Win32_RdvhManagement
- Win32_RdvhManagement de clase Servicios de Escritorio remoto, método RdvCopyBaseVmLocally
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvCopyBaseVmLocally
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d96e01038a4b41edcf32a6a5a9b353403fa6021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422569"
---
# <a name="rdvcopybasevmlocally-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="49ef2-106">Método RdvCopyBaseVmLocally de la \_ clase RdvhManagement de Win32</span><span class="sxs-lookup"><span data-stu-id="49ef2-106">RdvCopyBaseVmLocally method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="49ef2-107">Copia una máquina virtual base local en un servidor host de virtualización de escritorio remoto (RDV) especificado.</span><span class="sxs-lookup"><span data-stu-id="49ef2-107">Copies a local base virtual machine to a specified remote desktop virtualization (RDV) host server.</span></span>

## <a name="syntax"></a><span data-ttu-id="49ef2-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="49ef2-108">Syntax</span></span>


```mof
uint32 RdvCopyBaseVmLocally(
  [in] string BaseVmLocation,
  [in] string FarmName,
  [in] string GoldCacheLocation
);
```



## <a name="parameters"></a><span data-ttu-id="49ef2-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="49ef2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49ef2-110">*BaseVmLocation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="49ef2-110">*BaseVmLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49ef2-111">La ubicación de la máquina virtual base.</span><span class="sxs-lookup"><span data-stu-id="49ef2-111">The base virtual machine location.</span></span>

</dd> <dt>

<span data-ttu-id="49ef2-112">*FarmName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="49ef2-112">*FarmName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49ef2-113">Nombre de la granja de host en la que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="49ef2-113">The name of the host farm to copy to.</span></span>

</dd> <dt>

<span data-ttu-id="49ef2-114">*GoldCacheLocation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="49ef2-114">*GoldCacheLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49ef2-115">La ubicación de caché Gold.</span><span class="sxs-lookup"><span data-stu-id="49ef2-115">The gold cache location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49ef2-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49ef2-116">Return value</span></span>

<span data-ttu-id="49ef2-117">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="49ef2-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="49ef2-118">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="49ef2-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="49ef2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49ef2-119">Requirements</span></span>



| <span data-ttu-id="49ef2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="49ef2-120">Requirement</span></span> | <span data-ttu-id="49ef2-121">Value</span><span class="sxs-lookup"><span data-stu-id="49ef2-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="49ef2-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49ef2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="49ef2-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="49ef2-123">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="49ef2-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49ef2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="49ef2-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="49ef2-125">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="49ef2-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="49ef2-126">Namespace</span></span><br/>                | <span data-ttu-id="49ef2-127">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="49ef2-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="49ef2-128">MOF</span><span class="sxs-lookup"><span data-stu-id="49ef2-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49ef2-129"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="49ef2-129"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="49ef2-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="49ef2-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49ef2-131"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49ef2-131"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49ef2-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="49ef2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49ef2-133">**Win32 \_ RdvhManagement**</span><span class="sxs-lookup"><span data-stu-id="49ef2-133">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





