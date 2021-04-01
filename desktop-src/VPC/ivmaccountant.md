---
title: Interfaz IVMAccountant (VPCCOMInterfaces. h)
description: Proporciona acceso a información relacionada con cuentas para una máquina virtual.
ms.assetid: 047fa4c9-cb2e-4830-bab8-0513247eff9b
keywords:
- Interfaz IVMAccountant Virtual PC
- Interfaz IVMAccountant Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMAccountant
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d207833b92794510789e66e31b10e94d70b319fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803757"
---
# <a name="ivmaccountant-interface"></a><span data-ttu-id="c853a-105">Interfaz IVMAccountant</span><span class="sxs-lookup"><span data-stu-id="c853a-105">IVMAccountant interface</span></span>

<span data-ttu-id="c853a-106">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c853a-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c853a-107">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c853a-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c853a-108">Proporciona acceso a información relacionada con cuentas para una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c853a-108">Provides access to accounting-related information for a virtual machine.</span></span> <span data-ttu-id="c853a-109">Para recuperar el **IVMAccountant** de una máquina virtual, use la propiedad [**IVMVirtualMachine:: contable**](ivmvirtualmachine-accountant.md) .</span><span class="sxs-lookup"><span data-stu-id="c853a-109">To retrieve the **IVMAccountant** for a virtual machine, use the [**IVMVirtualMachine::Accountant**](ivmvirtualmachine-accountant.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="c853a-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="c853a-110">Members</span></span>

<span data-ttu-id="c853a-111">La interfaz **IVMAccountant** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="c853a-111">The **IVMAccountant** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="c853a-112">**IVMAccountant** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c853a-112">**IVMAccountant** also has these types of members:</span></span>

-   [<span data-ttu-id="c853a-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c853a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c853a-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c853a-114">Properties</span></span>

<span data-ttu-id="c853a-115">La interfaz **IVMAccountant** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c853a-115">The **IVMAccountant** interface has these properties.</span></span>



| <span data-ttu-id="c853a-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c853a-116">Property</span></span>                                                                        | <span data-ttu-id="c853a-117">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="c853a-117">Access type</span></span>          | <span data-ttu-id="c853a-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="c853a-118">Description</span></span>                                                                                             |
|:--------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c853a-119">**Gráfico**</span><span class="sxs-lookup"><span data-stu-id="c853a-119">**CPUUtilization**</span></span>](ivmaccountant-cpuutilization.md)<br/>               | <span data-ttu-id="c853a-120">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c853a-120">Read-only</span></span><br/> | <span data-ttu-id="c853a-121">El porcentaje de uso actual de la CPU para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c853a-121">The percentage of current CPU utilization for this virtual machine.</span></span><br/>                          |
| [<span data-ttu-id="c853a-122">**CPUUtilizationHistory**</span><span class="sxs-lookup"><span data-stu-id="c853a-122">**CPUUtilizationHistory**</span></span>](ivmaccountant-cpuutilizationhistory.md)<br/> | <span data-ttu-id="c853a-123">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c853a-123">Read-only</span></span><br/> | <span data-ttu-id="c853a-124">El uso de CPU reciente de esta máquina virtual (como una matriz de valores de porcentaje).</span><span class="sxs-lookup"><span data-stu-id="c853a-124">The recent CPU utilization of this virtual machine (as an array of percentage values).</span></span><br/>       |
| [<span data-ttu-id="c853a-125">**DiskBytesRead**</span><span class="sxs-lookup"><span data-stu-id="c853a-125">**DiskBytesRead**</span></span>](ivmaccountant-diskbytesread.md)<br/>                 | <span data-ttu-id="c853a-126">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c853a-126">Read-only</span></span><br/> | <span data-ttu-id="c853a-127">Número total de bytes leídos por todos los controladores de almacenamiento de esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c853a-127">The total number of bytes read by all storage controllers for this virtual machine.</span></span><br/>          |
| [<span data-ttu-id="c853a-128">**DiskBytesWritten**</span><span class="sxs-lookup"><span data-stu-id="c853a-128">**DiskBytesWritten**</span></span>](ivmaccountant-diskbyteswritten.md)<br/>           | <span data-ttu-id="c853a-129">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c853a-129">Read-only</span></span><br/> | <span data-ttu-id="c853a-130">Número total de bytes escritos por todos los controladores de almacenamiento de esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c853a-130">The total number of bytes written by all storage controllers for this virtual machine.</span></span><br/>       |
| [<span data-ttu-id="c853a-131">**NetworkBytesReceived**</span><span class="sxs-lookup"><span data-stu-id="c853a-131">**NetworkBytesReceived**</span></span>](ivmaccountant-networkbytesreceived.md)<br/>   | <span data-ttu-id="c853a-132">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c853a-132">Read-only</span></span><br/> | <span data-ttu-id="c853a-133">El número total de bytes recibidos por todos los adaptadores de red virtual para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c853a-133">The total number of bytes received by all virtual network adapters for this virtual machine.</span></span><br/> |
| [<span data-ttu-id="c853a-134">**NetworkBytesSent**</span><span class="sxs-lookup"><span data-stu-id="c853a-134">**NetworkBytesSent**</span></span>](ivmaccountant-networkbytessent.md)<br/>           | <span data-ttu-id="c853a-135">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c853a-135">Read-only</span></span><br/> | <span data-ttu-id="c853a-136">El número total de bytes enviados por todos los adaptadores de red virtual para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c853a-136">The total number of bytes sent by all virtual network adapters for this virtual machine.</span></span><br/>     |
| [<span data-ttu-id="c853a-137">**Actividad**</span><span class="sxs-lookup"><span data-stu-id="c853a-137">**UpTime**</span></span>](ivmaccountant-uptime.md)<br/>                               | <span data-ttu-id="c853a-138">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c853a-138">Read-only</span></span><br/> | <span data-ttu-id="c853a-139">El número de segundos que se ha estado ejecutando la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c853a-139">The number of seconds that the virtual machine has been running.</span></span><br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="c853a-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c853a-140">Requirements</span></span>



| <span data-ttu-id="c853a-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="c853a-141">Requirement</span></span> | <span data-ttu-id="c853a-142">Value</span><span class="sxs-lookup"><span data-stu-id="c853a-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c853a-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c853a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="c853a-144">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="c853a-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c853a-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c853a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="c853a-146">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c853a-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c853a-147">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="c853a-147">End of client support</span></span><br/>    | <span data-ttu-id="c853a-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c853a-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c853a-149">Producto</span><span class="sxs-lookup"><span data-stu-id="c853a-149">Product</span></span><br/>                  | <span data-ttu-id="c853a-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c853a-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c853a-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c853a-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="c853a-152"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c853a-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c853a-153">IID</span><span class="sxs-lookup"><span data-stu-id="c853a-153">IID</span></span><br/>                      | <span data-ttu-id="c853a-154">IID \_ IVMAccountant se define como 6376c067-7f57-4D63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="c853a-154">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



 

