---
title: Método de restablecimiento de IVMVirtualMachine (VPCCOMInterfaces. h)
description: Restablece la máquina virtual.
ms.assetid: 44daf6be-66ce-4291-a535-c30369eed60f
keywords:
- Restablecer método virtual PC
- Método Reset Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método Reset
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Reset
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45314eef6d837ac00647d477f3652b63221d977c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492238"
---
# <a name="ivmvirtualmachinereset-method"></a><span data-ttu-id="54010-106">IVMVirtualMachine:: RESET (método)</span><span class="sxs-lookup"><span data-stu-id="54010-106">IVMVirtualMachine::Reset method</span></span>

<span data-ttu-id="54010-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="54010-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="54010-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="54010-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="54010-109">Restablece la máquina virtual (VM).</span><span class="sxs-lookup"><span data-stu-id="54010-109">Resets the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="54010-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="54010-110">Syntax</span></span>


```C++
HRESULT Reset(
  [out, retval] IVMTask **resetTask
);
```



## <a name="parameters"></a><span data-ttu-id="54010-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54010-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54010-112">*resetTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="54010-112">*resetTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="54010-113">Un objeto [**IVMTask**](ivmtask.md) que se usa para realizar el seguimiento del progreso de finalización de la secuencia de restablecimiento de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="54010-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the VM's reset sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54010-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54010-114">Return value</span></span>

<span data-ttu-id="54010-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="54010-115">This method can return one of these values.</span></span>



| <span data-ttu-id="54010-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54010-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="54010-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="54010-117">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="54010-118"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="54010-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="54010-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="54010-119">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="54010-120"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="54010-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="54010-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="54010-121">The parameter is **NULL**.</span></span><br/>                                        |
| <dl> <span data-ttu-id="54010-122"><dt>**HRESULT \_ DE \_ Win32 (error de \_ acceso \_ denegado)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="54010-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="54010-123">El autor de la llamada debe tener permisos de acceso Execute para restablecer esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="54010-123">The caller must have execute access permissions to reset this VM.</span></span><br/> |
| <dl> <span data-ttu-id="54010-124"><dt>**Máquina virtual \_ La \_ VM E \_ no \_ ejecuta**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="54010-124"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="54010-125">La máquina virtual no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="54010-125">The VM is not running.</span></span><br/>                                            |
| <dl> <span data-ttu-id="54010-126"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="54010-126"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="54010-127">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="54010-127">The configuration is unknown.</span></span><br/>                                     |
| <dl> <span data-ttu-id="54010-128"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="54010-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="54010-129">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="54010-129">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="requirements"></a><span data-ttu-id="54010-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54010-130">Requirements</span></span>



| <span data-ttu-id="54010-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="54010-131">Requirement</span></span> | <span data-ttu-id="54010-132">Value</span><span class="sxs-lookup"><span data-stu-id="54010-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="54010-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54010-133">Minimum supported client</span></span><br/> | <span data-ttu-id="54010-134">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="54010-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="54010-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54010-135">Minimum supported server</span></span><br/> | <span data-ttu-id="54010-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="54010-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="54010-137">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="54010-137">End of client support</span></span><br/>    | <span data-ttu-id="54010-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="54010-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="54010-139">Producto</span><span class="sxs-lookup"><span data-stu-id="54010-139">Product</span></span><br/>                  | <span data-ttu-id="54010-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="54010-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="54010-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="54010-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="54010-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="54010-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="54010-143">IID</span><span class="sxs-lookup"><span data-stu-id="54010-143">IID</span></span><br/>                      | <span data-ttu-id="54010-144">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="54010-144">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="54010-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="54010-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54010-146">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="54010-146">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

