---
description: Crea un archivo de disco duro virtual.
ms.assetid: 6c136000-1df2-4456-833c-094671408338
title: Método CreateVirtualHardDisk de la clase Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.CreateVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b80a309274eb51ad7aff768898a9c3bd211f37cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688075"
---
# <a name="createvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="cb31b-103">Método CreateVirtualHardDisk de la \_ clase ImageManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="cb31b-103">CreateVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="cb31b-104">Crea un archivo de disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="cb31b-104">Creates a virtual hard disk file.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb31b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb31b-105">Syntax</span></span>


```mof
uint32 CreateVirtualHardDisk(
  [in]  string              VirtualDiskSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="cb31b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb31b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb31b-107">*VirtualDiskSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb31b-107">*VirtualDiskSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb31b-108">Cadena que contiene una instancia incrustada de la clase [**MSVM \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) que se usa para definir los atributos del disco duro virtual que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="cb31b-108">String that contains an embedded instance of the [**Msvm\_VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) class that is used to define attributes of the virtual hard disk to be created.</span></span>

</dd> <dt>

<span data-ttu-id="cb31b-109">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cb31b-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb31b-110">Referencia al trabajo (puede ser **null** si se ha completado la tarea).</span><span class="sxs-lookup"><span data-stu-id="cb31b-110">A reference to the job (can be **Null** if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb31b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb31b-111">Return value</span></span>

<span data-ttu-id="cb31b-112">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="cb31b-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="cb31b-113">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="cb31b-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cb31b-114">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="cb31b-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="cb31b-115">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="cb31b-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="cb31b-116">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="cb31b-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="cb31b-117">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="cb31b-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="cb31b-118">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="cb31b-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="cb31b-119">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="cb31b-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="cb31b-120">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="cb31b-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="cb31b-121">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="cb31b-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="cb31b-122">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="cb31b-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="cb31b-123">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="cb31b-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="cb31b-124">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="cb31b-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="cb31b-125">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="cb31b-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="cb31b-126">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="cb31b-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="cb31b-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cb31b-127">Remarks</span></span>

<span data-ttu-id="cb31b-128">El acceso a la clase [**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="cb31b-128">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="cb31b-129">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="cb31b-129">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb31b-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb31b-130">Requirements</span></span>



| <span data-ttu-id="cb31b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb31b-131">Requirement</span></span> | <span data-ttu-id="cb31b-132">Value</span><span class="sxs-lookup"><span data-stu-id="cb31b-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb31b-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb31b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="cb31b-134">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="cb31b-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cb31b-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb31b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="cb31b-136">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="cb31b-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cb31b-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cb31b-137">Namespace</span></span><br/>                | <span data-ttu-id="cb31b-138">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="cb31b-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cb31b-139">MOF</span><span class="sxs-lookup"><span data-stu-id="cb31b-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb31b-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cb31b-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb31b-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cb31b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb31b-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cb31b-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cb31b-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb31b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb31b-144">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="cb31b-144">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

