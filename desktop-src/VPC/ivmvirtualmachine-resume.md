---
title: Método de reanudación de IVMVirtualMachine (VPCCOMInterfaces. h)
description: Reanuda la máquina virtual.
ms.assetid: 4a2d6b64-8dcf-484e-940d-b0180aba9f01
keywords:
- Reanudar el método virtual PC
- Método resume Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método resume
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Resume
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c24af1e1a00aa0fa29acc077faf48287c0307414
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905486"
---
# <a name="ivmvirtualmachineresume-method"></a><span data-ttu-id="e4231-106">IVMVirtualMachine:: resume (método)</span><span class="sxs-lookup"><span data-stu-id="e4231-106">IVMVirtualMachine::Resume method</span></span>

<span data-ttu-id="e4231-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e4231-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e4231-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e4231-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e4231-109">Reanuda la máquina virtual (VM).</span><span class="sxs-lookup"><span data-stu-id="e4231-109">Resumes the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="e4231-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e4231-110">Syntax</span></span>


```C++
HRESULT Resume();
```



## <a name="parameters"></a><span data-ttu-id="e4231-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e4231-111">Parameters</span></span>

<span data-ttu-id="e4231-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e4231-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e4231-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e4231-113">Return value</span></span>

<span data-ttu-id="e4231-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="e4231-114">This method can return one of these values.</span></span>



| <span data-ttu-id="e4231-115">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e4231-115">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="e4231-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4231-116">Description</span></span>                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e4231-117"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e4231-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="e4231-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e4231-118">The operation was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="e4231-119"><dt>**E \_ ERROR**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="e4231-119"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                                     | <span data-ttu-id="e4231-120">La máquina virtual no está en pausa.</span><span class="sxs-lookup"><span data-stu-id="e4231-120">The VM is not paused.</span></span><br/>                                              |
| <dl> <span data-ttu-id="e4231-121"><dt>**HRESULT \_ DE \_ Win32 (error de \_ acceso \_ denegado)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="e4231-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="e4231-122">El autor de la llamada debe tener permisos de acceso de ejecución para reanudar la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e4231-122">The caller must have execute access permissions to resume this VM.</span></span><br/> |
| <dl> <span data-ttu-id="e4231-123"><dt>**Máquina virtual \_ 0xA0040202 \_ agotó el tiempo de \_ espera**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e4231-123"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="e4231-124">La operación no se completó de manera oportuna.</span><span class="sxs-lookup"><span data-stu-id="e4231-124">The operation did not complete in a timely manner.</span></span><br/>                 |
| <dl> <span data-ttu-id="e4231-125"><dt>**Máquina virtual \_ La \_ VM E \_ no \_ ejecuta**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="e4231-125"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="e4231-126">La máquina virtual no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="e4231-126">The VM is not running.</span></span><br/>                                             |
| <dl> <span data-ttu-id="e4231-127"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e4231-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="e4231-128">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="e4231-128">The configuration is unknown.</span></span><br/>                                      |
| <dl> <span data-ttu-id="e4231-129"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e4231-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="e4231-130">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="e4231-130">An unexpected error has occurred.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="e4231-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4231-131">Requirements</span></span>



| <span data-ttu-id="e4231-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4231-132">Requirement</span></span> | <span data-ttu-id="e4231-133">Value</span><span class="sxs-lookup"><span data-stu-id="e4231-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4231-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4231-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e4231-135">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4231-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e4231-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4231-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e4231-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e4231-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e4231-138">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="e4231-138">End of client support</span></span><br/>    | <span data-ttu-id="e4231-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4231-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e4231-140">Producto</span><span class="sxs-lookup"><span data-stu-id="e4231-140">Product</span></span><br/>                  | <span data-ttu-id="e4231-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e4231-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e4231-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e4231-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4231-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4231-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e4231-144">IID</span><span class="sxs-lookup"><span data-stu-id="e4231-144">IID</span></span><br/>                      | <span data-ttu-id="e4231-145">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="e4231-145">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="e4231-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4231-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4231-147">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="e4231-147">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

