---
description: Recupera el tamaño total de los archivos del sistema de la máquina virtual.
ms.assetid: 492aa0df-1562-4d83-a0ea-43776b12c1b1
title: Método GetSizeOfSystemFiles de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetSizeOfSystemFiles
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ed9fcf93093e17c2989121bf33ee5f5fbf09bab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810315"
---
# <a name="getsizeofsystemfiles-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="cd5f5-103">Método GetSizeOfSystemFiles de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="cd5f5-103">GetSizeOfSystemFiles method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="cd5f5-104">Recupera el tamaño total de los archivos del sistema de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cd5f5-104">Retrieves the total size of the system files of virtual machine.</span></span> <span data-ttu-id="cd5f5-105">Entre ellos se incluyen los archivos de configuración y de estado guardado.</span><span class="sxs-lookup"><span data-stu-id="cd5f5-105">These include the configuration and saved state files.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd5f5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd5f5-106">Syntax</span></span>


```mof
uint32 GetSizeOfSystemFiles(
  [in]  CIM_VirtualSystemSettingData REF Vssd,
  [out] uint64                           Size
);
```



## <a name="parameters"></a><span data-ttu-id="cd5f5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd5f5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd5f5-108">*Vssd* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cd5f5-108">*Vssd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd5f5-109">Referencia a la instancia [**de \_ VirtualSystemSettingData de CIM**](/previous-versions//cc136954(v=vs.85)) cuyo tamaño de archivos del sistema se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="cd5f5-109">A reference to the [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instance whose system files size are to be retrieved.</span></span> <span data-ttu-id="cd5f5-110">Esta instancia puede representar la creación de instancias actual de la máquina virtual o una instancia de una instantánea de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cd5f5-110">This instance may represent either the current instantiation of the virtual machine, or an instance of a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="cd5f5-111">*Tamaño* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cd5f5-111">*Size* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd5f5-112">Tamaño total, en bytes, de los archivos del sistema.</span><span class="sxs-lookup"><span data-stu-id="cd5f5-112">The total size, in bytes, of system files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd5f5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd5f5-113">Return value</span></span>

<span data-ttu-id="cd5f5-114">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="cd5f5-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="cd5f5-115">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="cd5f5-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cd5f5-116">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="cd5f5-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="cd5f5-117">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="cd5f5-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="cd5f5-118">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="cd5f5-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="cd5f5-119">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="cd5f5-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="cd5f5-120">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="cd5f5-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="cd5f5-121">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="cd5f5-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="cd5f5-122">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="cd5f5-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="cd5f5-123">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="cd5f5-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="cd5f5-124">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="cd5f5-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="cd5f5-125">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="cd5f5-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="cd5f5-126">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="cd5f5-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="cd5f5-127">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="cd5f5-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="cd5f5-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd5f5-128">Requirements</span></span>



| <span data-ttu-id="cd5f5-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd5f5-129">Requirement</span></span> | <span data-ttu-id="cd5f5-130">Value</span><span class="sxs-lookup"><span data-stu-id="cd5f5-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd5f5-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd5f5-131">Minimum supported client</span></span><br/> | <span data-ttu-id="cd5f5-132">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="cd5f5-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cd5f5-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd5f5-133">Minimum supported server</span></span><br/> | <span data-ttu-id="cd5f5-134">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="cd5f5-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cd5f5-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cd5f5-135">Namespace</span></span><br/>                | <span data-ttu-id="cd5f5-136">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="cd5f5-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cd5f5-137">MOF</span><span class="sxs-lookup"><span data-stu-id="cd5f5-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd5f5-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd5f5-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd5f5-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cd5f5-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd5f5-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cd5f5-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cd5f5-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd5f5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd5f5-142">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="cd5f5-142">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

