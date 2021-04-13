---
title: Método de reinicio de IVMGuestOS (VPCCOMInterfaces. h)
description: Reinicia el sistema operativo invitado.
ms.assetid: 328c7aa1-d9bd-452d-95dd-9f6a03fa8c9e
keywords:
- Método de reinicio Virtual PC
- Método de reinicio Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, método de reinicio
topic_type:
- apiref
api_name:
- IVMGuestOS.Restart
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 110718e45d04445dd895a2bdb27419fbd24731c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422360"
---
# <a name="ivmguestosrestart-method"></a><span data-ttu-id="944b6-106">IVMGuestOS:: Restart (método)</span><span class="sxs-lookup"><span data-stu-id="944b6-106">IVMGuestOS::Restart method</span></span>

<span data-ttu-id="944b6-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="944b6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="944b6-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="944b6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="944b6-109">Reinicia el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="944b6-109">Restarts the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="944b6-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="944b6-110">Syntax</span></span>


```C++
HRESULT Restart(
  [in]          VARIANT_BOOL inForced,
  [out, retval] IVMTask      **outRestartTask
);
```



## <a name="parameters"></a><span data-ttu-id="944b6-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="944b6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="944b6-112">no *forzada* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="944b6-112">*inForced* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="944b6-113">**Variante \_ TRUE** si se requiere un reinicio forzado y **Variant \_ false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="944b6-113">**VARIANT\_TRUE** if a forced restart is required and **VARIANT\_FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="944b6-114">*outRestartTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="944b6-114">*outRestartTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="944b6-115">Un objeto [**IVMTask**](ivmtask.md) que se usa para realizar el seguimiento del progreso de finalización de la secuencia de reinicio.</span><span class="sxs-lookup"><span data-stu-id="944b6-115">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the restart sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="944b6-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="944b6-116">Return value</span></span>

<span data-ttu-id="944b6-117">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="944b6-117">This method can return one of these values.</span></span>



| <span data-ttu-id="944b6-118">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="944b6-118">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="944b6-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="944b6-119">Description</span></span>                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="944b6-120"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="944b6-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="944b6-121">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="944b6-121">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="944b6-122"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="944b6-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="944b6-123">El parámetro *outRestartTask* es **null**.</span><span class="sxs-lookup"><span data-stu-id="944b6-123">The *outRestartTask* parameter is **NULL**.</span></span><br/>                     |
| <dl> <span data-ttu-id="944b6-124"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="944b6-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="944b6-125">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="944b6-125">An unexpected error has occurred.</span></span><br/>                               |
| <dl> <span data-ttu-id="944b6-126"><dt>**Máquina virtual \_ 0xA0040202 \_ agotó el tiempo de \_ espera**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="944b6-126"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="944b6-127">La operación no se completó de manera oportuna.</span><span class="sxs-lookup"><span data-stu-id="944b6-127">The operation did not complete in a timely manner.</span></span><br/>              |
| <dl> <span data-ttu-id="944b6-128"><dt>**Máquina virtual \_ La \_ VM E \_ no \_ ejecuta**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="944b6-128"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="944b6-129">La máquina virtual (VM) debe estar en ejecución para esta operación.</span><span class="sxs-lookup"><span data-stu-id="944b6-129">The virtual machine (VM) must be running for this operation.</span></span><br/>    |
| <dl> <span data-ttu-id="944b6-130"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="944b6-130"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                    | <span data-ttu-id="944b6-131">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="944b6-131">The configuration is unknown.</span></span><br/>                                   |
| <dl> <span data-ttu-id="944b6-132"><dt>**Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="944b6-132"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="944b6-133">La característica componentes de integración no está instalada en esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="944b6-133">The integration components feature is not installed in this VM.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="944b6-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="944b6-134">Remarks</span></span>

<span data-ttu-id="944b6-135">Los valores siguientes se pueden devolver a través de la propiedad [**error**](ivmtask-error.md) del objeto [**IVMTask**](ivmtask.md) devuelto.</span><span class="sxs-lookup"><span data-stu-id="944b6-135">The following values can be returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object.</span></span>



| <span data-ttu-id="944b6-136">Código de [**error**](ivmtask-error.md) /valor</span><span class="sxs-lookup"><span data-stu-id="944b6-136">[**Error**](ivmtask-error.md) code/Value</span></span>                                                                                                                                                                                                                                                                          | <span data-ttu-id="944b6-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="944b6-137">Description</span></span>                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="944b6-138"><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` 0x80070005</span><span class="sxs-lookup"><span data-stu-id="944b6-138"><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` (0x80070005)</span></span><br/>                             | <span data-ttu-id="944b6-139">El autor de la llamada debe tener permisos de acceso de ejecución para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="944b6-139">The caller must have execute access permissions for this VM.</span></span><br/>             |
| <span data-ttu-id="944b6-140"><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7)</span><span class="sxs-lookup"><span data-stu-id="944b6-140"><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7)</span></span><br/>                         | <span data-ttu-id="944b6-141">El equipo está bloqueado y no se puede apagar sin la opción Force.</span><span class="sxs-lookup"><span data-stu-id="944b6-141">The computer is locked and cannot be shut down without the force option.</span></span><br/> |
| <span data-ttu-id="944b6-142"><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)</span><span class="sxs-lookup"><span data-stu-id="944b6-142"><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)</span></span><br/>                                             | <span data-ttu-id="944b6-143">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="944b6-143">The device is not ready.</span></span><br/>                                                 |
| <span data-ttu-id="944b6-144"><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)</span><span class="sxs-lookup"><span data-stu-id="944b6-144"><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)</span></span><br/> | <span data-ttu-id="944b6-145">Está en curso un cierre del sistema.</span><span class="sxs-lookup"><span data-stu-id="944b6-145">A system shutdown is in progress.</span></span><br/>                                        |



 

## <a name="requirements"></a><span data-ttu-id="944b6-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="944b6-146">Requirements</span></span>



| <span data-ttu-id="944b6-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="944b6-147">Requirement</span></span> | <span data-ttu-id="944b6-148">Value</span><span class="sxs-lookup"><span data-stu-id="944b6-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="944b6-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="944b6-149">Minimum supported client</span></span><br/> | <span data-ttu-id="944b6-150">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="944b6-150">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="944b6-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="944b6-151">Minimum supported server</span></span><br/> | <span data-ttu-id="944b6-152">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="944b6-152">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="944b6-153">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="944b6-153">End of client support</span></span><br/>    | <span data-ttu-id="944b6-154">Windows 7</span><span class="sxs-lookup"><span data-stu-id="944b6-154">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="944b6-155">Producto</span><span class="sxs-lookup"><span data-stu-id="944b6-155">Product</span></span><br/>                  | <span data-ttu-id="944b6-156">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="944b6-156">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="944b6-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="944b6-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="944b6-158"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="944b6-158"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="944b6-159">IID</span><span class="sxs-lookup"><span data-stu-id="944b6-159">IID</span></span><br/>                      | <span data-ttu-id="944b6-160">IID \_ IVMGuestOS se define como 99fea0db-4880-499A-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="944b6-160">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="944b6-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="944b6-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="944b6-162">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="944b6-162">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

