---
title: Propiedad IVMNetworkAdapter VirtualMachine (VPCCOMInterfaces. h)
description: Recupera la máquina virtual asociada a esta interfaz de red.
ms.assetid: a3519041-0081-44e7-aa76-760d59ca8587
keywords:
- Propiedad VirtualMachine Virtual PC
- Propiedad VirtualMachine Virtual PC, interfaz IVMNetworkAdapter
- Interfaz IVMNetworkAdapter Virtual PC, propiedad VirtualMachine
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.VirtualMachine
- IVMNetworkAdapter.get_VirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea50e43bdcffcd16f668ef596a0f9db9d9bccfe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078811"
---
# <a name="ivmnetworkadaptervirtualmachine-property"></a><span data-ttu-id="69547-106">IVMNetworkAdapter:: VirtualMachine (propiedad)</span><span class="sxs-lookup"><span data-stu-id="69547-106">IVMNetworkAdapter::VirtualMachine property</span></span>

<span data-ttu-id="69547-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="69547-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="69547-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="69547-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="69547-109">Recupera la máquina virtual asociada a esta interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="69547-109">Retrieves the virtual machine associated with this network interface.</span></span>

<span data-ttu-id="69547-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="69547-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="69547-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69547-111">Syntax</span></span>


```C++
HRESULT get_VirtualMachine(
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="property-value"></a><span data-ttu-id="69547-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="69547-112">Property value</span></span>

<span data-ttu-id="69547-113">Una interfaz [**IVMVirtualMachine**](ivmvirtualmachine.md) que representa la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="69547-113">An [**IVMVirtualMachine**](ivmvirtualmachine.md) interface that represents the virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="69547-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="69547-114">Error codes</span></span>



| <span data-ttu-id="69547-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="69547-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="69547-116">Significado</span><span class="sxs-lookup"><span data-stu-id="69547-116">Meaning</span></span>                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="69547-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="69547-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="69547-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="69547-118">The operation was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="69547-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="69547-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="69547-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="69547-120">The parameter is **NULL**.</span></span><br/>           |
| <dl> <span data-ttu-id="69547-121"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="69547-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="69547-122">No se encuentra la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="69547-122">The virtual machine cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="69547-123"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="69547-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="69547-124">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="69547-124">An unexpected error has occurred.</span></span><br/>    |



## <a name="requirements"></a><span data-ttu-id="69547-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69547-125">Requirements</span></span>



| <span data-ttu-id="69547-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="69547-126">Requirement</span></span> | <span data-ttu-id="69547-127">Value</span><span class="sxs-lookup"><span data-stu-id="69547-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="69547-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69547-128">Minimum supported client</span></span><br/> | <span data-ttu-id="69547-129">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="69547-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="69547-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69547-130">Minimum supported server</span></span><br/> | <span data-ttu-id="69547-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="69547-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="69547-132">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="69547-132">End of client support</span></span><br/>    | <span data-ttu-id="69547-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="69547-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="69547-134">Producto</span><span class="sxs-lookup"><span data-stu-id="69547-134">Product</span></span><br/>                  | <span data-ttu-id="69547-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="69547-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="69547-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69547-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="69547-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="69547-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="69547-138">IID</span><span class="sxs-lookup"><span data-stu-id="69547-138">IID</span></span><br/>                      | <span data-ttu-id="69547-139">IID \_ IVMNetworkAdapter se define como e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="69547-139">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="69547-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="69547-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69547-141">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="69547-141">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

