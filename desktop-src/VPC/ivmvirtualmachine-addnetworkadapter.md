---
title: Método IVMVirtualMachine AddNetworkAdapter (VPCCOMInterfaces. h)
description: Agrega una interfaz de red a la máquina virtual.
ms.assetid: 1fa39d2c-4a5a-42cb-afa4-520bf19b8cc8
keywords:
- Método AddNetworkAdapter Virtual PC
- Método AddNetworkAdapter Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método AddNetworkAdapter
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d24351e5f5a32aff08e755329ac12baaaaf546
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695985"
---
# <a name="ivmvirtualmachineaddnetworkadapter-method"></a><span data-ttu-id="0f34e-106">IVMVirtualMachine:: AddNetworkAdapter (método)</span><span class="sxs-lookup"><span data-stu-id="0f34e-106">IVMVirtualMachine::AddNetworkAdapter method</span></span>

<span data-ttu-id="0f34e-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0f34e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0f34e-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0f34e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0f34e-109">Agrega una interfaz de red a la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0f34e-109">Adds a network interface to the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f34e-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f34e-110">Syntax</span></span>


```C++
HRESULT AddNetworkAdapter(
  [out, retval] IVMNetworkAdapter **networkAdapter
);
```



## <a name="parameters"></a><span data-ttu-id="0f34e-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f34e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f34e-112">*adaptador* \[ de la out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0f34e-112">*networkAdapter* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0f34e-113">Objeto [**IVMNetworkAdapter**](ivmnetworkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="0f34e-113">An [**IVMNetworkAdapter**](ivmnetworkadapter.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f34e-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0f34e-114">Return value</span></span>

<span data-ttu-id="0f34e-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="0f34e-115">This method can return one of these values.</span></span>



| <span data-ttu-id="0f34e-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0f34e-116">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="0f34e-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="0f34e-117">Description</span></span>                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="0f34e-118"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0f34e-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="0f34e-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0f34e-119">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="0f34e-120"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="0f34e-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="0f34e-121">El parámetro *adaptador de adaptador* es **null**.</span><span class="sxs-lookup"><span data-stu-id="0f34e-121">The *networkAdapter* parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="0f34e-122"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="0f34e-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="0f34e-123">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="0f34e-123">The configuration is unknown.</span></span><br/>                        |
| <dl> <span data-ttu-id="0f34e-124"><dt>**Máquina virtual \_ E \_ prefe el \_ \_ valor no válido**</dt> <dt>0xA0040301</dt></span><span class="sxs-lookup"><span data-stu-id="0f34e-124"><dt>**VM\_E\_PREF\_ILLEGAL\_VALUE**</dt> <dt>0xA0040301</dt></span></span> </dl>   | <span data-ttu-id="0f34e-125">No se pueden agregar más de cuatro (4) adaptadores de red.</span><span class="sxs-lookup"><span data-stu-id="0f34e-125">No more than four (4) network adapters can be added.</span></span><br/> |
| <dl> <span data-ttu-id="0f34e-126"><dt>**Máquina virtual \_ \_Máquina virtual en \_ ejecución \_ o \_ guardada**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="0f34e-126"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="0f34e-127">La máquina virtual está en estado en ejecución o guardada.</span><span class="sxs-lookup"><span data-stu-id="0f34e-127">The virtual machine is in a running or saved state.</span></span><br/>  |
| <dl> <span data-ttu-id="0f34e-128"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="0f34e-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="0f34e-129">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="0f34e-129">An unexpected error has occurred.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="0f34e-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f34e-130">Remarks</span></span>

<span data-ttu-id="0f34e-131">Solo puede Agregar una nueva interfaz de red a una máquina virtual detenida.</span><span class="sxs-lookup"><span data-stu-id="0f34e-131">You can only add a new network interface to a stopped virtual machine.</span></span> <span data-ttu-id="0f34e-132">El adaptador de red recién creado no está conectado a una red virtual.</span><span class="sxs-lookup"><span data-stu-id="0f34e-132">The newly created network adapter is not connected to a virtual network.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f34e-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f34e-133">Requirements</span></span>



| <span data-ttu-id="0f34e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f34e-134">Requirement</span></span> | <span data-ttu-id="0f34e-135">Value</span><span class="sxs-lookup"><span data-stu-id="0f34e-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f34e-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f34e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0f34e-137">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="0f34e-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0f34e-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f34e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0f34e-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0f34e-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0f34e-140">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="0f34e-140">End of client support</span></span><br/>    | <span data-ttu-id="0f34e-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0f34e-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0f34e-142">Producto</span><span class="sxs-lookup"><span data-stu-id="0f34e-142">Product</span></span><br/>                  | <span data-ttu-id="0f34e-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0f34e-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0f34e-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f34e-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f34e-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f34e-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0f34e-146">IID</span><span class="sxs-lookup"><span data-stu-id="0f34e-146">IID</span></span><br/>                      | <span data-ttu-id="0f34e-147">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="0f34e-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="0f34e-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f34e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f34e-149">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="0f34e-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

