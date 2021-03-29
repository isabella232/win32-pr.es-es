---
description: Inicia una operación de apagado del sistema operativo en la máquina virtual secundaria asociada. Si se devuelve cero (0), el cierre se ha iniciado correctamente. Cualquier otro código de retorno indica una condición de error.
ms.assetid: 946BBC62-5479-4AE0-8870-D0A07827B902
title: Método InitiateShutdown de la clase Msvm_ShutdownComponent (winreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent.InitiateShutdown
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 266ab64bb058325ac165a2e12c2a91d442a90269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277569"
---
# <a name="initiateshutdown-method-of-the-msvm_shutdowncomponent-class"></a><span data-ttu-id="90ad8-105">Método InitiateShutdown de la \_ clase ShutdownComponent de MSVM</span><span class="sxs-lookup"><span data-stu-id="90ad8-105">InitiateShutdown method of the Msvm\_ShutdownComponent class</span></span>

<span data-ttu-id="90ad8-106">Inicia una operación de apagado del sistema operativo en la máquina virtual secundaria asociada.</span><span class="sxs-lookup"><span data-stu-id="90ad8-106">Initiates an operating system shutdown operation on the associated child virtual machine.</span></span> <span data-ttu-id="90ad8-107">Si se devuelve cero (0), el cierre se ha iniciado correctamente.</span><span class="sxs-lookup"><span data-stu-id="90ad8-107">If zero (0) is returned, then the shutdown was initiated successfully.</span></span> <span data-ttu-id="90ad8-108">Cualquier otro código de retorno indica una condición de error.</span><span class="sxs-lookup"><span data-stu-id="90ad8-108">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="90ad8-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90ad8-109">Syntax</span></span>


```mof
uint32 InitiateShutdown(
  [in] boolean Force,
  [in] string  Reason
);
```



## <a name="parameters"></a><span data-ttu-id="90ad8-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="90ad8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90ad8-111">*Forzar* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="90ad8-111">*Force* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90ad8-112">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="90ad8-112">Type: **boolean**</span></span>

<span data-ttu-id="90ad8-113">Marca que, si **es true**, obliga a que se cierren las aplicaciones a pesar de tener datos no guardados.</span><span class="sxs-lookup"><span data-stu-id="90ad8-113">A flag which, if **True**, forces applications to be closed despite having unsaved data.</span></span>

</dd> <dt>

<span data-ttu-id="90ad8-114">*Motivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="90ad8-114">*Reason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90ad8-115">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="90ad8-115">Type: **string**</span></span>

<span data-ttu-id="90ad8-116">Motivo de la operación de cierre.</span><span class="sxs-lookup"><span data-stu-id="90ad8-116">The reason for the shutdown operation.</span></span> <span data-ttu-id="90ad8-117">Esta es una cadena definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="90ad8-117">This is a user-defined string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90ad8-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90ad8-118">Return value</span></span>

<span data-ttu-id="90ad8-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="90ad8-119">Type: **uint32**</span></span>

<dl> <dt>

<span data-ttu-id="90ad8-120">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="90ad8-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="90ad8-121">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="90ad8-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="90ad8-122">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="90ad8-122">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="90ad8-123">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="90ad8-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="90ad8-124">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="90ad8-124">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="90ad8-125">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="90ad8-125">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="90ad8-126">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="90ad8-126">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="90ad8-127">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="90ad8-127">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="90ad8-128">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="90ad8-128">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="90ad8-129">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="90ad8-129">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="90ad8-130">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="90ad8-130">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="90ad8-131">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="90ad8-131">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="90ad8-132">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="90ad8-132">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="90ad8-133">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="90ad8-133">**File not found** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="90ad8-134">**El sistema no está listo** (32780)</span><span class="sxs-lookup"><span data-stu-id="90ad8-134">**The system is not ready** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="90ad8-135">**El equipo está bloqueado y no se puede apagar sin la opción Force** (32781)</span><span class="sxs-lookup"><span data-stu-id="90ad8-135">**The machine is locked and cannot be shut down without the force option** (32781)</span></span>
</dt> <dt>

<span data-ttu-id="90ad8-136">**Un apagado del sistema está en curso** (32782)</span><span class="sxs-lookup"><span data-stu-id="90ad8-136">**A system shutdown is in progress** (32782)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="90ad8-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90ad8-137">Remarks</span></span>

<span data-ttu-id="90ad8-138">El acceso a la clase [**MSVM \_ ShutdownComponent**](msvm-shutdowncomponent.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="90ad8-138">Access to the [**Msvm\_ShutdownComponent**](msvm-shutdowncomponent.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="90ad8-139">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="90ad8-139">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="90ad8-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90ad8-140">Requirements</span></span>



| <span data-ttu-id="90ad8-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="90ad8-141">Requirement</span></span> | <span data-ttu-id="90ad8-142">Value</span><span class="sxs-lookup"><span data-stu-id="90ad8-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90ad8-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90ad8-143">Minimum supported client</span></span><br/> | <span data-ttu-id="90ad8-144">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="90ad8-144">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="90ad8-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90ad8-145">Minimum supported server</span></span><br/> | <span data-ttu-id="90ad8-146">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="90ad8-146">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="90ad8-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="90ad8-147">Namespace</span></span><br/>                | <span data-ttu-id="90ad8-148">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="90ad8-148">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="90ad8-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="90ad8-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="90ad8-150"><dt>Winreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="90ad8-150"><dt>Winreg.h</dt></span></span> </dl>                     |
| <span data-ttu-id="90ad8-151">MOF</span><span class="sxs-lookup"><span data-stu-id="90ad8-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90ad8-152"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="90ad8-152"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="90ad8-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="90ad8-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90ad8-154"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="90ad8-154"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="90ad8-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="90ad8-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90ad8-156">**MSVM \_ ShutdownComponent**</span><span class="sxs-lookup"><span data-stu-id="90ad8-156">**Msvm\_ShutdownComponent**</span></span>](msvm-shutdowncomponent.md)
</dt> </dl>

 

