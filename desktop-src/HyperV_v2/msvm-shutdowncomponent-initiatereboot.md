---
description: Inicia una operación de reinicio del sistema operativo en la máquina virtual secundaria asociada.
ms.assetid: 9f3ebbaf-ee0f-4c01-8f73-1f37c08a0feb
title: Método InitiateReboot de la clase Msvm_ShutdownComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent.InitiateReboot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 527569e8a5d6c2bb0a54294637ae19c13f5e3af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652471"
---
# <a name="initiatereboot-method-of-the-msvm_shutdowncomponent-class"></a><span data-ttu-id="5b001-103">Método InitiateReboot de la \_ clase ShutdownComponent de MSVM</span><span class="sxs-lookup"><span data-stu-id="5b001-103">InitiateReboot method of the Msvm\_ShutdownComponent class</span></span>

<span data-ttu-id="5b001-104">Inicia una operación de reinicio del sistema operativo en la máquina virtual secundaria asociada.</span><span class="sxs-lookup"><span data-stu-id="5b001-104">Initiates an operating system reboot operation on the associated child virtual machine.</span></span>

<span data-ttu-id="5b001-105">Si se devuelve cero (0), el reinicio se ha iniciado correctamente.</span><span class="sxs-lookup"><span data-stu-id="5b001-105">If zero (0) is returned, then the reboot was initiated successfully.</span></span> <span data-ttu-id="5b001-106">Cualquier otro código de retorno indica una condición de error.</span><span class="sxs-lookup"><span data-stu-id="5b001-106">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b001-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b001-107">Syntax</span></span>


```mof
uint32 InitiateReboot(
  [in] boolean Force,
  [in] string  Reason
);
```



## <a name="parameters"></a><span data-ttu-id="5b001-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5b001-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b001-109">*Forzar* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5b001-109">*Force* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b001-110">Marca que, si es TRUE, obliga a que se cierren las aplicaciones a pesar de tener datos no guardados.</span><span class="sxs-lookup"><span data-stu-id="5b001-110">A flag which, if TRUE, forces applications to be closed despite having unsaved data.</span></span>

</dd> <dt>

<span data-ttu-id="5b001-111">*Motivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5b001-111">*Reason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b001-112">Motivo de la operación de reinicio.</span><span class="sxs-lookup"><span data-stu-id="5b001-112">The reason for the reboot operation.</span></span> <span data-ttu-id="5b001-113">Esta es una cadena definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="5b001-113">This is a user-defined string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b001-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5b001-114">Return value</span></span>

<span data-ttu-id="5b001-115">Este método devuelve uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="5b001-115">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="5b001-116">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="5b001-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5b001-117">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="5b001-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="5b001-118">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="5b001-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="5b001-119">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="5b001-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="5b001-120">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="5b001-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="5b001-121">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="5b001-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="5b001-122">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="5b001-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="5b001-123">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="5b001-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="5b001-124">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="5b001-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="5b001-125">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="5b001-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="5b001-126">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="5b001-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="5b001-127">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="5b001-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="5b001-128">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="5b001-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="5b001-129">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="5b001-129">**File not found** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="5b001-130">**El sistema no está listo** (32780)</span><span class="sxs-lookup"><span data-stu-id="5b001-130">**The system is not ready** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="5b001-131">**El equipo está bloqueado y no se puede apagar sin la opción Force** (32781)</span><span class="sxs-lookup"><span data-stu-id="5b001-131">**The machine is locked and cannot be shut down without the force option** (32781)</span></span>
</dt> <dt>

<span data-ttu-id="5b001-132">**Un apagado del sistema está en curso** (32782)</span><span class="sxs-lookup"><span data-stu-id="5b001-132">**A system shutdown is in progress** (32782)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="5b001-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b001-133">Requirements</span></span>



| <span data-ttu-id="5b001-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b001-134">Requirement</span></span> | <span data-ttu-id="5b001-135">Value</span><span class="sxs-lookup"><span data-stu-id="5b001-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b001-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b001-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5b001-137">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="5b001-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="5b001-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b001-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5b001-139">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5b001-139">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="5b001-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5b001-140">Namespace</span></span><br/>                | <span data-ttu-id="5b001-141">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="5b001-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5b001-142">MOF</span><span class="sxs-lookup"><span data-stu-id="5b001-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b001-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5b001-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b001-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5b001-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b001-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5b001-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5b001-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b001-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b001-147">**MSVM \_ ShutdownComponent**</span><span class="sxs-lookup"><span data-stu-id="5b001-147">**Msvm\_ShutdownComponent**</span></span>](msvm-shutdowncomponent.md)
</dt> </dl>

 

 




