---
title: Método pausar IVMVirtualMachine (VPCCOMInterfaces. h)
description: Pausa la máquina virtual.
ms.assetid: 29ac40c4-7713-4782-8a31-42f2c32b8f7d
keywords:
- Pausar método virtual PC
- Pausar método virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, pausar método
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Pause
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c953da05d34c999066a6bc87cb1f51983defbd5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905430"
---
# <a name="ivmvirtualmachinepause-method"></a><span data-ttu-id="d5dfa-106">IVMVirtualMachine::P método ause</span><span class="sxs-lookup"><span data-stu-id="d5dfa-106">IVMVirtualMachine::Pause method</span></span>

<span data-ttu-id="d5dfa-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d5dfa-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d5dfa-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d5dfa-109">Pausa la máquina virtual (VM).</span><span class="sxs-lookup"><span data-stu-id="d5dfa-109">Pauses the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="d5dfa-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5dfa-110">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="d5dfa-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5dfa-111">Parameters</span></span>

<span data-ttu-id="d5dfa-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d5dfa-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5dfa-113">Return value</span></span>

<span data-ttu-id="d5dfa-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-114">This method can return one of these values.</span></span>



| <span data-ttu-id="d5dfa-115">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5dfa-115">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="d5dfa-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5dfa-116">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d5dfa-117"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d5dfa-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="d5dfa-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-118">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="d5dfa-119"><dt>**E \_ ERROR**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="d5dfa-119"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                                     | <span data-ttu-id="d5dfa-120">La máquina virtual ya está en pausa.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-120">The VM is already paused.</span></span><br/>                                         |
| <dl> <span data-ttu-id="d5dfa-121"><dt>**HRESULT \_ DE \_ Win32 (error de \_ acceso \_ denegado)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="d5dfa-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="d5dfa-122">El autor de la llamada debe tener permisos de acceso de ejecución para pausar esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-122">The caller must have execute access permissions to pause this VM.</span></span><br/> |
| <dl> <span data-ttu-id="d5dfa-123"><dt>**Máquina virtual \_ 0xA0040202 \_ agotó el tiempo de \_ espera**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d5dfa-123"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="d5dfa-124">La operación no se completó de manera oportuna.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-124">The operation did not complete in a timely manner.</span></span><br/>                |
| <dl> <span data-ttu-id="d5dfa-125"><dt>**Máquina virtual \_ La \_ VM E \_ no \_ ejecuta**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="d5dfa-125"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="d5dfa-126">La máquina virtual no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-126">The virtual machine is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="d5dfa-127"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d5dfa-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="d5dfa-128">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-128">The configuration is unknown.</span></span><br/>                                     |
| <dl> <span data-ttu-id="d5dfa-129"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d5dfa-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="d5dfa-130">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-130">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="d5dfa-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5dfa-131">Remarks</span></span>

<span data-ttu-id="d5dfa-132">**Pausar** no guarda el estado actual de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-132">**Pause** does not save the current state of the VM.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5dfa-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5dfa-133">Requirements</span></span>



| <span data-ttu-id="d5dfa-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5dfa-134">Requirement</span></span> | <span data-ttu-id="d5dfa-135">Value</span><span class="sxs-lookup"><span data-stu-id="d5dfa-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5dfa-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5dfa-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d5dfa-137">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="d5dfa-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d5dfa-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5dfa-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d5dfa-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d5dfa-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d5dfa-140">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="d5dfa-140">End of client support</span></span><br/>    | <span data-ttu-id="d5dfa-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d5dfa-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d5dfa-142">Producto</span><span class="sxs-lookup"><span data-stu-id="d5dfa-142">Product</span></span><br/>                  | <span data-ttu-id="d5dfa-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d5dfa-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d5dfa-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5dfa-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5dfa-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5dfa-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d5dfa-146">IID</span><span class="sxs-lookup"><span data-stu-id="d5dfa-146">IID</span></span><br/>                      | <span data-ttu-id="d5dfa-147">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="d5dfa-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="d5dfa-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5dfa-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5dfa-149">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="d5dfa-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

