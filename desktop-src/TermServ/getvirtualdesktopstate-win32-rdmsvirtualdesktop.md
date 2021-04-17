---
title: Método GetVirtualDesktopState de la clase Win32_RDMSVirtualDesktop
description: Recupera el estado del escritorio virtual.
ms.assetid: 176096ba-2b5f-428c-9216-02e3e97be64e
ms.tgt_platform: multiple
keywords:
- Método GetVirtualDesktopState Servicios de Escritorio remoto
- Método GetVirtualDesktopState Servicios de Escritorio remoto, clase Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop de clase Servicios de Escritorio remoto, método GetVirtualDesktopState
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopState
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 674e9646f0f41166fbfdc9e4ad35df697023329a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685935"
---
# <a name="getvirtualdesktopstate-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="11db6-106">Método GetVirtualDesktopState de la \_ clase RDMSVirtualDesktop de Win32</span><span class="sxs-lookup"><span data-stu-id="11db6-106">GetVirtualDesktopState method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="11db6-107">Recupera el estado del escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="11db6-107">Retrieves the state of the virtual desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="11db6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11db6-108">Syntax</span></span>


```mof
uint32 GetVirtualDesktopState(
  [out] uint32 VMState
);
```



## <a name="parameters"></a><span data-ttu-id="11db6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11db6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11db6-110">*VMState* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="11db6-110">*VMState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11db6-111">Recibe un valor que indica el estado de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="11db6-111">Receives a value that indicates the state of the virtual machine.</span></span>

<span data-ttu-id="11db6-112">Este parámetro puede ser probable que se establezca en uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="11db6-112">This parameter can bet set to one of the following values:</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="11db6-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0 (valor predeterminado))</span><span class="sxs-lookup"><span data-stu-id="11db6-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0 (Default))</span></span>


</dt> <dd>

<span data-ttu-id="11db6-114">No se pudo determinar el estado de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="11db6-114">The state of the virtual machine could not be determined.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="11db6-115"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="11db6-115"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="11db6-116">La máquina virtual se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="11db6-116">The virtual machine is running.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="11db6-117"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="11db6-117"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="11db6-118">La máquina virtual está desactivada.</span><span class="sxs-lookup"><span data-stu-id="11db6-118">The virtual machine is turned off.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="11db6-119"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (32768)</span><span class="sxs-lookup"><span data-stu-id="11db6-119"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="11db6-120">La máquina virtual está en pausa.</span><span class="sxs-lookup"><span data-stu-id="11db6-120">The virtual machine is paused.</span></span>

</dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="11db6-121"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspendido** (32769)</span><span class="sxs-lookup"><span data-stu-id="11db6-121"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (32769)</span></span>


</dt> <dd>

<span data-ttu-id="11db6-122">La máquina virtual está en un estado guardado.</span><span class="sxs-lookup"><span data-stu-id="11db6-122">The virtual machine is in a saved state.</span></span>

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="11db6-123"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (32770)</span><span class="sxs-lookup"><span data-stu-id="11db6-123"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (32770)</span></span>


</dt> <dd>

<span data-ttu-id="11db6-124">La máquina virtual se está iniciando.</span><span class="sxs-lookup"><span data-stu-id="11db6-124">The virtual machine is starting.</span></span>

</dd> <dt>

<span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>

<span data-ttu-id="11db6-125"><span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>**Guardar** (32773)</span><span class="sxs-lookup"><span data-stu-id="11db6-125"><span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>**Saving** (32773)</span></span>


</dt> <dd>

<span data-ttu-id="11db6-126">La máquina virtual está guardando su estado.</span><span class="sxs-lookup"><span data-stu-id="11db6-126">The virtual machine is saving its state.</span></span>

</dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="11db6-127"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (32774)</span><span class="sxs-lookup"><span data-stu-id="11db6-127"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (32774)</span></span>


</dt> <dd>

<span data-ttu-id="11db6-128">Se está apagando la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="11db6-128">The virtual machine is turning off.</span></span>

</dd> <dt>

<span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>

<span data-ttu-id="11db6-129"><span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>**Pausar** (32776)</span><span class="sxs-lookup"><span data-stu-id="11db6-129"><span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>**Pausing** (32776)</span></span>


</dt> <dd>

<span data-ttu-id="11db6-130">La máquina virtual se está pausando.</span><span class="sxs-lookup"><span data-stu-id="11db6-130">The virtual machine is pausing.</span></span>

</dd> <dt>

<span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>

<span data-ttu-id="11db6-131"><span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>**Reanudar** (32777)</span><span class="sxs-lookup"><span data-stu-id="11db6-131"><span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>**Resuming** (32777)</span></span>


</dt> <dd>

<span data-ttu-id="11db6-132">La máquina virtual se está reanudando de un estado pausado.</span><span class="sxs-lookup"><span data-stu-id="11db6-132">The virtual machine is resuming from a paused state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11db6-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11db6-133">Return value</span></span>

<span data-ttu-id="11db6-134">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="11db6-134">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="11db6-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11db6-135">Requirements</span></span>



| <span data-ttu-id="11db6-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="11db6-136">Requirement</span></span> | <span data-ttu-id="11db6-137">Value</span><span class="sxs-lookup"><span data-stu-id="11db6-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="11db6-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11db6-138">Minimum supported client</span></span><br/> | <span data-ttu-id="11db6-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="11db6-139">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="11db6-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11db6-140">Minimum supported server</span></span><br/> | <span data-ttu-id="11db6-141">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="11db6-141">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="11db6-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="11db6-142">Namespace</span></span><br/>                | <span data-ttu-id="11db6-143">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="11db6-143">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="11db6-144">MOF</span><span class="sxs-lookup"><span data-stu-id="11db6-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11db6-145"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="11db6-145"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="11db6-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="11db6-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11db6-147"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11db6-147"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="11db6-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="11db6-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11db6-149">**Win32 \_ RDMSVirtualDesktop**</span><span class="sxs-lookup"><span data-stu-id="11db6-149">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





