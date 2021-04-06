---
title: Método Shutdown de IVMGuestOS (VPCCOMInterfaces. h)
description: Apaga el sistema operativo invitado en la máquina virtual.
ms.assetid: a1453ad1-c4c2-47bb-a612-d203a6ee8c18
keywords:
- Método de apagado Virtual PC
- Método Shutdown Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, método Shutdown
topic_type:
- apiref
api_name:
- IVMGuestOS.Shutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63025270752af044a572cf9b6299e54b31b89ffe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802696"
---
# <a name="ivmguestosshutdown-method"></a><span data-ttu-id="b1778-106">IVMGuestOS:: Shutdown (método)</span><span class="sxs-lookup"><span data-stu-id="b1778-106">IVMGuestOS::Shutdown method</span></span>

<span data-ttu-id="b1778-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b1778-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b1778-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b1778-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b1778-109">Apaga el sistema operativo invitado en la máquina virtual (VM).</span><span class="sxs-lookup"><span data-stu-id="b1778-109">Shuts down the guest operating system in the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="b1778-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1778-110">Syntax</span></span>


```C++
HRESULT Shutdown(
  [in]          VARIANT_BOOL isForced,
  [out, retval] IVMTask      **outShutdownTask
);
```



## <a name="parameters"></a><span data-ttu-id="b1778-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b1778-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1778-112">*isForced* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b1778-112">*isForced* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1778-113">**Variante \_ TRUE** si se va a forzar el cierre, **Variant \_ false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b1778-113">**VARIANT\_TRUE** if the shutdown is to be forced, **VARIANT\_FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="b1778-114">*outShutdownTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="b1778-114">*outShutdownTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b1778-115">Un objeto [**IVMTask**](ivmtask.md) que se usa para realizar el seguimiento de la finalización del proceso de cierre.</span><span class="sxs-lookup"><span data-stu-id="b1778-115">An [**IVMTask**](ivmtask.md) object that is used to track the completion of the shutdown process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1778-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b1778-116">Return value</span></span>

<span data-ttu-id="b1778-117">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="b1778-117">This method can return one of these values.</span></span>



| <span data-ttu-id="b1778-118">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b1778-118">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="b1778-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1778-119">Description</span></span>                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b1778-120"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b1778-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="b1778-121">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b1778-121">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="b1778-122"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b1778-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="b1778-123">El parámetro *outShutdownTask* es **null**.</span><span class="sxs-lookup"><span data-stu-id="b1778-123">The *outShutdownTask* parameter is **NULL**.</span></span><br/>                    |
| <dl> <span data-ttu-id="b1778-124"><dt>**Máquina virtual \_ 0xA0040202 \_ agotó el tiempo de \_ espera**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b1778-124"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="b1778-125">La operación no se completó de manera oportuna.</span><span class="sxs-lookup"><span data-stu-id="b1778-125">The operation did not complete in a timely manner.</span></span><br/>              |
| <dl> <span data-ttu-id="b1778-126"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b1778-126"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="b1778-127">No se encontró la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b1778-127">The VM could not be found.</span></span><br/>                                      |
| <dl> <span data-ttu-id="b1778-128"><dt>**Máquina virtual \_ La \_ VM E \_ no \_ ejecuta**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="b1778-128"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="b1778-129">La máquina virtual debe estar en ejecución para esta operación.</span><span class="sxs-lookup"><span data-stu-id="b1778-129">The VM must be running for this operation.</span></span><br/>                      |
| <dl> <span data-ttu-id="b1778-130"><dt>**HRESULT \_ DE \_ Win32 (error de \_ acceso \_ denegado)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="b1778-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="b1778-131">El autor de la llamada debe tener permisos de acceso de ejecución para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b1778-131">The caller must have execute access permissions for this VM.</span></span><br/>    |
| <dl> <span data-ttu-id="b1778-132"><dt>**Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="b1778-132"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>       | <span data-ttu-id="b1778-133">La característica componentes de integración no está instalada en esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b1778-133">The integration components feature is not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="b1778-134"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b1778-134"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="b1778-135">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="b1778-135">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="b1778-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b1778-136">Remarks</span></span>

<span data-ttu-id="b1778-137">La máquina virtual debe estar en ejecución y la característica componentes de integración debe instalarse cuando se invoca este método.</span><span class="sxs-lookup"><span data-stu-id="b1778-137">The VM must be running and integration components feature must be installed when this method is invoked.</span></span> <span data-ttu-id="b1778-138">Este método solo es compatible con sistemas operativos invitados basados en Windows.</span><span class="sxs-lookup"><span data-stu-id="b1778-138">This method is only supported for Windows-based guest operating systems.</span></span>

<span data-ttu-id="b1778-139">Los valores siguientes se pueden devolver a través de la propiedad [**error**](ivmtask-error.md) del objeto [**IVMTask**](ivmtask.md) devuelto.</span><span class="sxs-lookup"><span data-stu-id="b1778-139">The following values can be returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object.</span></span>



| <span data-ttu-id="b1778-140">Código de [**error**](ivmtask-error.md) /valor</span><span class="sxs-lookup"><span data-stu-id="b1778-140">[**Error**](ivmtask-error.md) code/Value</span></span>                                                                                                                                                                                                                                                                          | <span data-ttu-id="b1778-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1778-141">Description</span></span>                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b1778-142"><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` 0x80070005</span><span class="sxs-lookup"><span data-stu-id="b1778-142"><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` (0x80070005)</span></span><br/>                             | <span data-ttu-id="b1778-143">El autor de la llamada debe tener permisos de acceso de ejecución para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b1778-143">The caller must have execute access permissions for this VM.</span></span><br/>             |
| <span data-ttu-id="b1778-144"><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7)</span><span class="sxs-lookup"><span data-stu-id="b1778-144"><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7)</span></span><br/>                         | <span data-ttu-id="b1778-145">El equipo está bloqueado y no se puede apagar sin la opción Force.</span><span class="sxs-lookup"><span data-stu-id="b1778-145">The computer is locked and cannot be shut down without the force option.</span></span><br/> |
| <span data-ttu-id="b1778-146"><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)</span><span class="sxs-lookup"><span data-stu-id="b1778-146"><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)</span></span><br/>                                             | <span data-ttu-id="b1778-147">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="b1778-147">The device is not ready.</span></span><br/>                                                 |
| <span data-ttu-id="b1778-148"><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)</span><span class="sxs-lookup"><span data-stu-id="b1778-148"><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)</span></span><br/> | <span data-ttu-id="b1778-149">Está en curso un cierre del sistema.</span><span class="sxs-lookup"><span data-stu-id="b1778-149">A system shutdown is in progress.</span></span><br/>                                        |



 

## <a name="requirements"></a><span data-ttu-id="b1778-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1778-150">Requirements</span></span>



| <span data-ttu-id="b1778-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1778-151">Requirement</span></span> | <span data-ttu-id="b1778-152">Value</span><span class="sxs-lookup"><span data-stu-id="b1778-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1778-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1778-153">Minimum supported client</span></span><br/> | <span data-ttu-id="b1778-154">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b1778-154">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b1778-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1778-155">Minimum supported server</span></span><br/> | <span data-ttu-id="b1778-156">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b1778-156">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b1778-157">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b1778-157">End of client support</span></span><br/>    | <span data-ttu-id="b1778-158">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b1778-158">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b1778-159">Producto</span><span class="sxs-lookup"><span data-stu-id="b1778-159">Product</span></span><br/>                  | <span data-ttu-id="b1778-160">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b1778-160">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b1778-161">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b1778-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1778-162"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1778-162"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b1778-163">IID</span><span class="sxs-lookup"><span data-stu-id="b1778-163">IID</span></span><br/>                      | <span data-ttu-id="b1778-164">IID \_ IVMGuestOS se define como 99fea0db-4880-499A-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="b1778-164">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="b1778-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1778-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1778-166">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="b1778-166">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

