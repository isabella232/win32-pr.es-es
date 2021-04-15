---
title: Método GetProvisioningProperties de la clase Win32_RDMSCollectionProperties
description: Recupera las propiedades de aprovisionamiento de la colección de escritorios virtuales.
ms.assetid: c314b7a5-8546-4711-833e-b47bb682aa53
ms.tgt_platform: multiple
keywords:
- Método GetProvisioningProperties Servicios de Escritorio remoto
- Método GetProvisioningProperties Servicios de Escritorio remoto, clase Win32_RDMSCollectionProperties
- Win32_RDMSCollectionProperties de clase Servicios de Escritorio remoto, método GetProvisioningProperties
topic_type:
- apiref
api_name:
- Win32_RDMSCollectionProperties.GetProvisioningProperties
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ca58f82d2918441e5da3cf53d442497c1a6a2eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686072"
---
# <a name="getprovisioningproperties-method-of-the-win32_rdmscollectionproperties-class"></a><span data-ttu-id="557e6-106">Método GetProvisioningProperties de la \_ clase RDMSCollectionProperties de Win32</span><span class="sxs-lookup"><span data-stu-id="557e6-106">GetProvisioningProperties method of the Win32\_RDMSCollectionProperties class</span></span>

<span data-ttu-id="557e6-107">Recupera las propiedades de aprovisionamiento de la colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="557e6-107">Retrieves the provisioning properties of the virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="557e6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="557e6-108">Syntax</span></span>


```mof
uint32 GetProvisioningProperties(
  [out] string  PoolVhdType,
  [out] string  MasterVmLocation,
  [out] string  NamePrefix,
  [out] uint32  NameStartIndex,
  [out] string  LocalVmLocation,
  [out] string  LocalGoldVmLocation,
  [out] boolean RunFromSMB,
  [out] string  SMBLocation,
  [out] boolean SMBStreaming,
  [out] string  VmDomain,
  [out] string  VmOU,
  [out] string  ProductKey
);
```



## <a name="parameters"></a><span data-ttu-id="557e6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="557e6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="557e6-110">*PoolVhdType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="557e6-110">*PoolVhdType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="557e6-111">Especifica el formato VHD (disco duro virtual) del grupo de máquinas virtuales de la colección.</span><span class="sxs-lookup"><span data-stu-id="557e6-111">Specifies the VHD (virtual hard disk) format of the virtual machine pool in the collection.</span></span>

<dt>

<span data-ttu-id="557e6-112">Clonar</span><span class="sxs-lookup"><span data-stu-id="557e6-112">Clone</span></span>
</dt> <dd>

<span data-ttu-id="557e6-113">Un VHD clonado.</span><span class="sxs-lookup"><span data-stu-id="557e6-113">A cloned VHD.</span></span>

</dd> <dt>

<span data-ttu-id="557e6-114">DiffDisk</span><span class="sxs-lookup"><span data-stu-id="557e6-114">DiffDisk</span></span>
</dt> <dd>

<span data-ttu-id="557e6-115">Un VHD de diferenciación.</span><span class="sxs-lookup"><span data-stu-id="557e6-115">A differencing VHD.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="557e6-116">*MasterVmLocation* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="557e6-116">*MasterVmLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="557e6-117">Recibe la ruta de acceso a la imagen de máquina virtual maestra.</span><span class="sxs-lookup"><span data-stu-id="557e6-117">Receives the path to the master VM image.</span></span>

</dd> <dt>

<span data-ttu-id="557e6-118">*NamePrefix* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="557e6-118">*NamePrefix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="557e6-119">Recibe el prefijo de nombre que se va a anexar al principio de los nombres de las máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="557e6-119">Receives the name prefix to append to the beginning of virtual machine names.</span></span>

</dd> <dt>

<span data-ttu-id="557e6-120">*NameStartIndex* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="557e6-120">*NameStartIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="557e6-121">Índice de inicio.</span><span class="sxs-lookup"><span data-stu-id="557e6-121">Start index.</span></span>

</dd> <dt>

<span data-ttu-id="557e6-122">*LocalVmLocation* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="557e6-122">*LocalVmLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="557e6-123">Recibe la ruta de acceso local a las máquinas virtuales en los servidores de Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="557e6-123">Receives the local path to the virtual machines on the Hyper-V servers.</span></span> <span data-ttu-id="557e6-124">Si este parámetro se establece en **null** o está vacío, se usará el directorio predeterminado de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="557e6-124">If this parameter is set to **NULL** or if it is empty, the default virtual machine directory will be used.</span></span>

</dd> <dt>

<span data-ttu-id="557e6-125">*LocalGoldVmLocation* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="557e6-125">*LocalGoldVmLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="557e6-126">Recibe la ruta de acceso local a la imagen del VHD Golden cuando el parámetro *PoolVhdTpe* se establece en "DiffDisk".</span><span class="sxs-lookup"><span data-stu-id="557e6-126">Receives the local path to the golden VHD image when the *PoolVhdTpe* parameter is set to "DiffDisk".</span></span> <span data-ttu-id="557e6-127">Si este parámetro se establece en **null** o está vacío, se usará el directorio predeterminado de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="557e6-127">If this parameter is set to **NULL** or if it is empty, the default virtual machine directory will be used.</span></span>

</dd> <dt>

<span data-ttu-id="557e6-128">*RunFromSMB* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="557e6-128">*RunFromSMB* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="557e6-129">Recibe un valor que indica si se va a ejecutar la colección desde un recurso compartido de bloque de mensajes del servidor (SMB).</span><span class="sxs-lookup"><span data-stu-id="557e6-129">Receives a value that indicates whether to run the collection from an Server Message Block (SMB) share.</span></span> <span data-ttu-id="557e6-130">**True** para ejecutar las máquinas virtuales desde un recurso compartido SBM; casos **False**.</span><span class="sxs-lookup"><span data-stu-id="557e6-130">**TRUE** to run the virtual machines from an SBM share; otherwise; **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="557e6-131">*SMBLocation* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="557e6-131">*SMBLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="557e6-132">Recibe la ruta de acceso al recurso compartido de SMB si está habilitado el uso compartido de SMB.</span><span class="sxs-lookup"><span data-stu-id="557e6-132">Receives the path to the SMB share if SMB sharing is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="557e6-133">*SMBStreaming* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="557e6-133">*SMBStreaming* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="557e6-134">Recibe un valor que indica si está habilitada la transmisión por secuencias de SMB.</span><span class="sxs-lookup"><span data-stu-id="557e6-134">Receives a value that indicates whether SMB streaming is enabled.</span></span> <span data-ttu-id="557e6-135">**True** si está habilitado el uso compartido de SMB; casos **False**.</span><span class="sxs-lookup"><span data-stu-id="557e6-135">**TRUE** if SMB sharing is enabled; otherwise; **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="557e6-136">*VmDomain* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="557e6-136">*VmDomain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="557e6-137">Recibe el nombre de dominio de las máquinas virtuales de la colección.</span><span class="sxs-lookup"><span data-stu-id="557e6-137">Receives the domain name of the virtual machines in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="557e6-138">*VmOU* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="557e6-138">*VmOU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="557e6-139">Recibe el Active Directory unidad organizativa (OU) de las máquinas virtuales de la colección.</span><span class="sxs-lookup"><span data-stu-id="557e6-139">Receives the Active Directory organization unit (OU) of the virtual machines in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="557e6-140">*ProductKey* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="557e6-140">*ProductKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="557e6-141">Recibe las claves de producto del sistema operativo para las máquinas virtuales de la colección.</span><span class="sxs-lookup"><span data-stu-id="557e6-141">Receives the OS product keys for the virtual machines in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="557e6-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="557e6-142">Return value</span></span>

<span data-ttu-id="557e6-143">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="557e6-143">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="557e6-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="557e6-144">Requirements</span></span>



| <span data-ttu-id="557e6-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="557e6-145">Requirement</span></span> | <span data-ttu-id="557e6-146">Value</span><span class="sxs-lookup"><span data-stu-id="557e6-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="557e6-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="557e6-147">Minimum supported client</span></span><br/> | <span data-ttu-id="557e6-148">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="557e6-148">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="557e6-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="557e6-149">Minimum supported server</span></span><br/> | <span data-ttu-id="557e6-150">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="557e6-150">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="557e6-151">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="557e6-151">Namespace</span></span><br/>                | <span data-ttu-id="557e6-152">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="557e6-152">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="557e6-153">MOF</span><span class="sxs-lookup"><span data-stu-id="557e6-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="557e6-154"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="557e6-154"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="557e6-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="557e6-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="557e6-156"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="557e6-156"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="557e6-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="557e6-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="557e6-158">**Win32 \_ RDMSCollectionProperties**</span><span class="sxs-lookup"><span data-stu-id="557e6-158">**Win32\_RDMSCollectionProperties**</span></span>](win32-rdmscollectionproperties.md)
</dt> </dl>

 

 





