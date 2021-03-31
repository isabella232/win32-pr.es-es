---
title: Método ProvisioningPrepJob de la clase Win32_RDMSVirtualDesktopCollection
description: Crea un trabajo de aprovisionamiento de escritorio virtual.
ms.assetid: 240D4BE6-95BD-4858-8F8F-A00C92042AEF
ms.tgt_platform: multiple
keywords:
- Método ProvisioningPrepJob Servicios de Escritorio remoto
- Método ProvisioningPrepJob Servicios de Escritorio remoto, Win32_RDMSVirtualDesktopCollection interfaz
- Win32_RDMSVirtualDesktopCollection Servicios de Escritorio remoto de interfaz, método ProvisioningPrepJob
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningPrepJob
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9727dec0e31dd199f324ed01a4510041ba3558f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996307"
---
# <a name="provisioningprepjob-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="f0c9d-106">Método ProvisioningPrepJob de la \_ clase RDMSVirtualDesktopCollection de Win32</span><span class="sxs-lookup"><span data-stu-id="f0c9d-106">ProvisioningPrepJob method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="f0c9d-107">Crea un trabajo de aprovisionamiento de escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="f0c9d-107">Creates a virtual desktop provisioning job.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0c9d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0c9d-108">Syntax</span></span>


```mof
uint32 ProvisioningPrepJob(
  [in]  string  CollectionAlias,
  [in]  string  VMHostName,
  [in]  string  VMName,
  [in]  string  ExportToLocation,
  [in]  boolean bSysPrep,
  [in]  string  MachineName,
  [in]  string  UserName,
  [in]  string  Password,
  [out] string  JobGuid
);
```



## <a name="parameters"></a><span data-ttu-id="f0c9d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f0c9d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0c9d-110">*CollectionAlias* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f0c9d-110">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c9d-111">El alias de la colección que hospeda el escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="f0c9d-111">The alias of the collection that hosts the virtual desktop.</span></span>

</dd> <dt>

<span data-ttu-id="f0c9d-112">*VMHostName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f0c9d-112">*VMHostName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c9d-113">El nombre de host de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f0c9d-113">The virtual machine host name.</span></span>

</dd> <dt>

<span data-ttu-id="f0c9d-114">*VMName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f0c9d-114">*VMName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c9d-115">El nombre de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f0c9d-115">The name of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="f0c9d-116">*ExportToLocation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f0c9d-116">*ExportToLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c9d-117">La ruta de acceso completa de la ubicación para exportar el trabajo de aprovisionamiento.</span><span class="sxs-lookup"><span data-stu-id="f0c9d-117">The full path the location to export the provisioning job.</span></span>

</dd> <dt>

<span data-ttu-id="f0c9d-118">*bSysPrep* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f0c9d-118">*bSysPrep* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c9d-119">Indica si el trabajo de aprovisionamiento representa una implementación de Sysprep.</span><span class="sxs-lookup"><span data-stu-id="f0c9d-119">Indicates whether the provisioning job represents a Sysprep deployment.</span></span>

</dd> <dt>

<span data-ttu-id="f0c9d-120">*MachineName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f0c9d-120">*MachineName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c9d-121">El nombre de equipo del equipo que hospeda la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f0c9d-121">The machine name of the computer that hosts the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="f0c9d-122">*Nombre de usuario* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f0c9d-122">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c9d-123">El nombre de usuario del administrador de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f0c9d-123">The user name of the administrator of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="f0c9d-124">*Contraseña* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f0c9d-124">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c9d-125">La contraseña del administrador de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f0c9d-125">The password of the administrator of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="f0c9d-126">*JobGuid* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f0c9d-126">*JobGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c9d-127">**GUID** que identifica de forma única el trabajo de aprovisionamiento.</span><span class="sxs-lookup"><span data-stu-id="f0c9d-127">The **GUID** that uniquely identifies the provisioning job.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0c9d-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f0c9d-128">Return value</span></span>

<span data-ttu-id="f0c9d-129">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="f0c9d-129">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0c9d-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0c9d-130">Requirements</span></span>



| <span data-ttu-id="f0c9d-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0c9d-131">Requirement</span></span> | <span data-ttu-id="f0c9d-132">Value</span><span class="sxs-lookup"><span data-stu-id="f0c9d-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0c9d-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0c9d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f0c9d-134">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f0c9d-134">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="f0c9d-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0c9d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f0c9d-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f0c9d-136">Windows Server 2008</span></span><br/>                                                              |
| <span data-ttu-id="f0c9d-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f0c9d-137">Namespace</span></span><br/>                | <span data-ttu-id="f0c9d-138">RDMs raíz de \\ cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="f0c9d-138">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="f0c9d-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f0c9d-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0c9d-140"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f0c9d-140"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0c9d-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f0c9d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0c9d-142"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0c9d-142"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="f0c9d-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0c9d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0c9d-144">**Win32 \_ RDMSVirtualDesktopCollection**</span><span class="sxs-lookup"><span data-stu-id="f0c9d-144">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





