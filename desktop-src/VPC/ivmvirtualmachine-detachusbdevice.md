---
title: Método IVMVirtualMachine DetachUSBDevice (VPCCOMInterfaces. h)
description: Libera un dispositivo USB de una máquina virtual.
ms.assetid: ae2b70b1-7bf3-4a84-9f05-4e91de93fa73
keywords:
- Método DetachUSBDevice Virtual PC
- Método DetachUSBDevice Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método DetachUSBDevice
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DetachUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92f5a858c25822e9e9ba1a11686003b326133a59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695983"
---
# <a name="ivmvirtualmachinedetachusbdevice-method"></a><span data-ttu-id="35241-106">IVMVirtualMachine::D método etachUSBDevice</span><span class="sxs-lookup"><span data-stu-id="35241-106">IVMVirtualMachine::DetachUSBDevice method</span></span>

<span data-ttu-id="35241-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="35241-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="35241-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="35241-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="35241-109">Libera un dispositivo USB de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="35241-109">Releases a USB device from a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="35241-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35241-110">Syntax</span></span>


```C++
HRESULT DetachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a><span data-ttu-id="35241-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35241-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35241-112">*inUSBDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="35241-112">*inUSBDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35241-113">Un puntero [**IVMUSBDevice**](ivmusbdevice.md) que representa el dispositivo USB que se va a desasociar de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="35241-113">A [**IVMUSBDevice**](ivmusbdevice.md) pointer that represents the USB device to be detached from the virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35241-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35241-114">Return value</span></span>

<span data-ttu-id="35241-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="35241-115">This method can return one of these values.</span></span>



| <span data-ttu-id="35241-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35241-116">Return code/value</span></span>                                                                                                                                                          | <span data-ttu-id="35241-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="35241-117">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="35241-118"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="35241-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                | <span data-ttu-id="35241-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="35241-119">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="35241-120"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="35241-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                  | <span data-ttu-id="35241-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="35241-121">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="35241-122"><dt>**Máquina virtual \_ La \_ VM E \_ no \_ ejecuta**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="35241-122"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>     | <span data-ttu-id="35241-123">La máquina virtual no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="35241-123">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="35241-124"><dt>**Máquina virtual \_ E \_ \_ \_ no se pudo desasociar USB**</dt> <dt>0xA00400927</dt></span><span class="sxs-lookup"><span data-stu-id="35241-124"><dt>**VM\_E\_USB\_DETACH\_FAILED**</dt> <dt>0xA00400927</dt></span></span> </dl> | <span data-ttu-id="35241-125">No se pudo realizar la operación de desasociación.</span><span class="sxs-lookup"><span data-stu-id="35241-125">The detach operation failed.</span></span><br/>        |
| <dl> <span data-ttu-id="35241-126"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="35241-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>          | <span data-ttu-id="35241-127">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="35241-127">An unexpected error has occurred.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="35241-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35241-128">Requirements</span></span>



| <span data-ttu-id="35241-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="35241-129">Requirement</span></span> | <span data-ttu-id="35241-130">Value</span><span class="sxs-lookup"><span data-stu-id="35241-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="35241-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35241-131">Minimum supported client</span></span><br/> | <span data-ttu-id="35241-132">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="35241-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="35241-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35241-133">Minimum supported server</span></span><br/> | <span data-ttu-id="35241-134">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="35241-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="35241-135">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="35241-135">End of client support</span></span><br/>    | <span data-ttu-id="35241-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="35241-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="35241-137">Producto</span><span class="sxs-lookup"><span data-stu-id="35241-137">Product</span></span><br/>                  | <span data-ttu-id="35241-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="35241-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="35241-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="35241-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="35241-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="35241-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="35241-141">IID</span><span class="sxs-lookup"><span data-stu-id="35241-141">IID</span></span><br/>                      | <span data-ttu-id="35241-142">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="35241-142">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="35241-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="35241-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35241-144">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="35241-144">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

