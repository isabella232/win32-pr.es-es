---
title: Método IVMVirtualMachine RemoveNetworkAdapter (VPCCOMInterfaces. h)
description: Quita una interfaz de red de la máquina virtual.
ms.assetid: 25a5b172-55b8-4cbe-98aa-630148cf6b6d
keywords:
- Método RemoveNetworkAdapter Virtual PC
- Método RemoveNetworkAdapter Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método RemoveNetworkAdapter
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27424f7a3dc5445f56d960393aa12345fcf5f1cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492239"
---
# <a name="ivmvirtualmachineremovenetworkadapter-method"></a><span data-ttu-id="ccd61-106">IVMVirtualMachine:: RemoveNetworkAdapter (método)</span><span class="sxs-lookup"><span data-stu-id="ccd61-106">IVMVirtualMachine::RemoveNetworkAdapter method</span></span>

<span data-ttu-id="ccd61-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ccd61-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ccd61-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ccd61-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ccd61-109">Quita una interfaz de red de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ccd61-109">Removes a network interface from the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccd61-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ccd61-110">Syntax</span></span>


```C++
HRESULT RemoveNetworkAdapter(
  [in] IVMNetworkAdapter *networkAdapter
);
```



## <a name="parameters"></a><span data-ttu-id="ccd61-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ccd61-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccd61-112">*adaptador* \[ de la de\]</span><span class="sxs-lookup"><span data-stu-id="ccd61-112">*networkAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccd61-113">Un objeto [**IVMNetworkAdapter**](ivmnetworkadapter.md) que representa el adaptador de red que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="ccd61-113">An [**IVMNetworkAdapter**](ivmnetworkadapter.md) object that represents the network adapter to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccd61-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ccd61-114">Return value</span></span>

<span data-ttu-id="ccd61-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="ccd61-115">This method can return one of these values.</span></span>



| <span data-ttu-id="ccd61-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ccd61-116">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="ccd61-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="ccd61-117">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="ccd61-118"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ccd61-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="ccd61-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ccd61-119">The operation was successful.</span></span><br/>                       |
| <dl> <span data-ttu-id="ccd61-120"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="ccd61-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="ccd61-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="ccd61-121">The parameter is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="ccd61-122"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ccd61-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="ccd61-123">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="ccd61-123">The configuration is unknown.</span></span><br/>                       |
| <dl> <span data-ttu-id="ccd61-124"><dt>**Máquina virtual \_ \_Máquina virtual en \_ ejecución \_ o \_ guardada**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="ccd61-124"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="ccd61-125">La máquina virtual está en estado en ejecución o guardada.</span><span class="sxs-lookup"><span data-stu-id="ccd61-125">The virtual machine is in a running or saved state.</span></span><br/> |
| <dl> <span data-ttu-id="ccd61-126"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ccd61-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="ccd61-127">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="ccd61-127">An unexpected error has occurred.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="ccd61-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ccd61-128">Remarks</span></span>

<span data-ttu-id="ccd61-129">Solo puede quitar una interfaz de red existente de una máquina virtual que esté detenida.</span><span class="sxs-lookup"><span data-stu-id="ccd61-129">You can only remove an existing network interface from a virtual machine that is stopped.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccd61-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccd61-130">Requirements</span></span>



| <span data-ttu-id="ccd61-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccd61-131">Requirement</span></span> | <span data-ttu-id="ccd61-132">Value</span><span class="sxs-lookup"><span data-stu-id="ccd61-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccd61-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ccd61-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ccd61-134">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="ccd61-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ccd61-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ccd61-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ccd61-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ccd61-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ccd61-137">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="ccd61-137">End of client support</span></span><br/>    | <span data-ttu-id="ccd61-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ccd61-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ccd61-139">Producto</span><span class="sxs-lookup"><span data-stu-id="ccd61-139">Product</span></span><br/>                  | <span data-ttu-id="ccd61-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ccd61-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ccd61-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ccd61-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccd61-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccd61-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ccd61-143">IID</span><span class="sxs-lookup"><span data-stu-id="ccd61-143">IID</span></span><br/>                      | <span data-ttu-id="ccd61-144">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="ccd61-144">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="ccd61-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="ccd61-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccd61-146">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="ccd61-146">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

