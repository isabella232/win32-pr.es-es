---
title: Método de desIVMVirtualMachine (VPCCOMInterfaces. h)
description: Desactiva la máquina virtual.
ms.assetid: 4ea00314-8f1e-47d9-bbb8-b5791af1fb86
keywords:
- Método de apagado Virtual PC
- Método de apagado Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método de apagado
topic_type:
- apiref
api_name:
- IVMVirtualMachine.TurnOff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27a5b14955fcc8a060c49932e3fa4f238497a567
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079630"
---
# <a name="ivmvirtualmachineturnoff-method"></a><span data-ttu-id="2df50-106">IVMVirtualMachine:: caparate (método)</span><span class="sxs-lookup"><span data-stu-id="2df50-106">IVMVirtualMachine::TurnOff method</span></span>

<span data-ttu-id="2df50-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2df50-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2df50-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2df50-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2df50-109">Desactiva la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2df50-109">Turns off the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="2df50-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2df50-110">Syntax</span></span>


```C++
HRESULT TurnOff(
  [out, retval] IVMTask **turnOffTask
);
```



## <a name="parameters"></a><span data-ttu-id="2df50-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2df50-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2df50-112">*turnOffTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="2df50-112">*turnOffTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2df50-113">Un objeto [**IVMTask**](ivmtask.md) que se usa para realizar el seguimiento del progreso de la ejecución de la secuencia de apagado de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2df50-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the virtual machine's turnoff sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2df50-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2df50-114">Return value</span></span>

<span data-ttu-id="2df50-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="2df50-115">This method can return one of these values.</span></span>



| <span data-ttu-id="2df50-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2df50-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="2df50-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="2df50-117">Description</span></span>                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2df50-118"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2df50-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="2df50-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="2df50-119">The operation was successful.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="2df50-120"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2df50-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="2df50-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="2df50-121">The parameter is **NULL**.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="2df50-122"><dt>**HRESULT \_ DE \_ Win32 (error de \_ acceso \_ denegado)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="2df50-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="2df50-123">El autor de la llamada debe tener permisos de acceso de ejecución para desactivar esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2df50-123">The caller must have execute access permissions to turn off this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="2df50-124"><dt>**Máquina virtual \_ La \_ VM E \_ no \_ ejecuta**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="2df50-124"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="2df50-125">La máquina virtual no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="2df50-125">The virtual machine is not running.</span></span><br/>                                               |
| <dl> <span data-ttu-id="2df50-126"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="2df50-126"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="2df50-127">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="2df50-127">The configuration is unknown.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="2df50-128"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2df50-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="2df50-129">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="2df50-129">An unexpected error has occurred.</span></span><br/>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="2df50-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2df50-130">Remarks</span></span>

<span data-ttu-id="2df50-131">Este método desactiva la máquina virtual de la misma manera que apagarla en una máquina física.</span><span class="sxs-lookup"><span data-stu-id="2df50-131">This method turns off the virtual machine in the same manner as turning the power off on a physical machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="2df50-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2df50-132">Requirements</span></span>



| <span data-ttu-id="2df50-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="2df50-133">Requirement</span></span> | <span data-ttu-id="2df50-134">Value</span><span class="sxs-lookup"><span data-stu-id="2df50-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2df50-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2df50-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2df50-136">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="2df50-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2df50-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2df50-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2df50-138">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2df50-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2df50-139">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="2df50-139">End of client support</span></span><br/>    | <span data-ttu-id="2df50-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2df50-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2df50-141">Producto</span><span class="sxs-lookup"><span data-stu-id="2df50-141">Product</span></span><br/>                  | <span data-ttu-id="2df50-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2df50-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2df50-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2df50-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="2df50-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2df50-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2df50-145">IID</span><span class="sxs-lookup"><span data-stu-id="2df50-145">IID</span></span><br/>                      | <span data-ttu-id="2df50-146">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="2df50-146">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="2df50-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="2df50-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2df50-148">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="2df50-148">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

