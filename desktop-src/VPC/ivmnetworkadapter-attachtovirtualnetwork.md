---
title: Método IVMNetworkAdapter AttachToVirtualNetwork (VPCCOMInterfaces. h)
description: Conecta la interfaz de red a la red virtual especificada.
ms.assetid: c743e930-c22e-4f32-b691-f7adc2485fed
keywords:
- Método AttachToVirtualNetwork Virtual PC
- Método AttachToVirtualNetwork Virtual PC, interfaz IVMNetworkAdapter
- Interfaz IVMNetworkAdapter Virtual PC, método AttachToVirtualNetwork
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.AttachToVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e7d0d9822e73ef6081a35f19ef628fd10051b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491080"
---
# <a name="ivmnetworkadapterattachtovirtualnetwork-method"></a><span data-ttu-id="2bcc4-106">IVMNetworkAdapter:: AttachToVirtualNetwork (método)</span><span class="sxs-lookup"><span data-stu-id="2bcc4-106">IVMNetworkAdapter::AttachToVirtualNetwork method</span></span>

<span data-ttu-id="2bcc4-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2bcc4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2bcc4-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2bcc4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2bcc4-109">Conecta la interfaz de red a la red virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="2bcc4-109">Attaches the network interface to the specified virtual network.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bcc4-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2bcc4-110">Syntax</span></span>


```C++
HRESULT AttachToVirtualNetwork(
  [in] IVMVirtualNetwork *virtualNetwork
);
```



## <a name="parameters"></a><span data-ttu-id="2bcc4-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2bcc4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bcc4-112">*virtualNetwork* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2bcc4-112">*virtualNetwork* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bcc4-113">La red virtual a la que se conectará esta NIC virtual.</span><span class="sxs-lookup"><span data-stu-id="2bcc4-113">The virtual network to which this virtual NIC will be connected.</span></span> <span data-ttu-id="2bcc4-114">Vea [**IVMVirtualNetwork**](ivmvirtualnetwork.md).</span><span class="sxs-lookup"><span data-stu-id="2bcc4-114">See [**IVMVirtualNetwork**](ivmvirtualnetwork.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bcc4-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2bcc4-115">Return value</span></span>

<span data-ttu-id="2bcc4-116">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="2bcc4-116">This method can return one of these values.</span></span>



| <span data-ttu-id="2bcc4-117">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2bcc4-117">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="2bcc4-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="2bcc4-118">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="2bcc4-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="2bcc4-119"><dt>**S\_OK**</dt></span></span> </dl>                                                                                                       | <span data-ttu-id="2bcc4-120">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="2bcc4-120">The operation was successful.</span></span><br/>                           |
| <dl> <span data-ttu-id="2bcc4-121"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2bcc4-121"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="2bcc4-122">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="2bcc4-122">The parameter is **NULL**.</span></span><br/>                              |
| <dl> <span data-ttu-id="2bcc4-123"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="2bcc4-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                               | <span data-ttu-id="2bcc4-124">El parámetro no contiene una red virtual válida.</span><span class="sxs-lookup"><span data-stu-id="2bcc4-124">The parameter does not contain a valid virtual network.</span></span><br/> |
| <dl> <span data-ttu-id="2bcc4-125"><dt>**HRESULT \_ DE \_ Win32 (error de \_ acceso \_ denegado)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="2bcc4-125"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="2bcc4-126">Se denegó el acceso a la red virtual solicitada.</span><span class="sxs-lookup"><span data-stu-id="2bcc4-126">Access was denied to the requested virtual network.</span></span><br/>     |
| <dl> <span data-ttu-id="2bcc4-127"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="2bcc4-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="2bcc4-128">La máquina virtual no es válida o ya no existe.</span><span class="sxs-lookup"><span data-stu-id="2bcc4-128">The virtual machine is invalid or no longer exists.</span></span><br/>     |
| <dl> <span data-ttu-id="2bcc4-129"><dt>**\_identificador de \_ \_ red virtual \_ no \_ válido de VM E**</dt></span><span class="sxs-lookup"><span data-stu-id="2bcc4-129"><dt>**VM\_E\_INVALID\_VIRTUAL\_NETWORK\_ID**</dt></span></span> </dl>                                                                        | <span data-ttu-id="2bcc4-130">El parámetro no es una red virtual existente.</span><span class="sxs-lookup"><span data-stu-id="2bcc4-130">The parameter is not an existing virtual network.</span></span><br/>       |
| <dl> <span data-ttu-id="2bcc4-131"><dt>**DISP \_ E ( \_ excepción)**</dt></span><span class="sxs-lookup"><span data-stu-id="2bcc4-131"><dt>**DISP\_E\_EXCEPTION**</dt></span></span> </dl>                                                                                          | <span data-ttu-id="2bcc4-132">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="2bcc4-132">An unexpected error has occurred.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="2bcc4-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bcc4-133">Requirements</span></span>



| <span data-ttu-id="2bcc4-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bcc4-134">Requirement</span></span> | <span data-ttu-id="2bcc4-135">Value</span><span class="sxs-lookup"><span data-stu-id="2bcc4-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bcc4-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bcc4-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2bcc4-137">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="2bcc4-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2bcc4-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bcc4-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2bcc4-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2bcc4-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2bcc4-140">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="2bcc4-140">End of client support</span></span><br/>    | <span data-ttu-id="2bcc4-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2bcc4-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2bcc4-142">Producto</span><span class="sxs-lookup"><span data-stu-id="2bcc4-142">Product</span></span><br/>                  | <span data-ttu-id="2bcc4-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2bcc4-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2bcc4-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2bcc4-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bcc4-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bcc4-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2bcc4-146">IID</span><span class="sxs-lookup"><span data-stu-id="2bcc4-146">IID</span></span><br/>                      | <span data-ttu-id="2bcc4-147">IID \_ IVMNetworkAdapter se define como e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="2bcc4-147">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="2bcc4-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="2bcc4-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bcc4-149">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="2bcc4-149">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

