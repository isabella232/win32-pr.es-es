---
title: Propiedad IVMUSBDevice AttachedToVM (VPCCOMInterfaces. h)
description: Recupera el nombre de la máquina virtual a la que está conectado el dispositivo USB.
ms.assetid: 214ed891-1fca-4311-945a-0ce3d05d604e
keywords:
- Propiedad AttachedToVM Virtual PC
- Propiedad AttachedToVM Virtual PC, interfaz IVMUSBDevice
- Interfaz IVMUSBDevice Virtual PC, propiedad AttachedToVM
topic_type:
- apiref
api_name:
- IVMUSBDevice.AttachedToVM
- IVMUSBDevice.get_AttachedToVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c64e265cba81858bc887cbf595426bffd1b604aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079440"
---
# <a name="ivmusbdeviceattachedtovm-property"></a><span data-ttu-id="b643a-106">IVMUSBDevice:: AttachedToVM (propiedad)</span><span class="sxs-lookup"><span data-stu-id="b643a-106">IVMUSBDevice::AttachedToVM property</span></span>

<span data-ttu-id="b643a-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b643a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b643a-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b643a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b643a-109">Recupera el nombre de la máquina virtual a la que está conectado el dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="b643a-109">Retrieves the name of the virtual machine to which the USB Device is attached.</span></span>

<span data-ttu-id="b643a-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b643a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b643a-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b643a-111">Syntax</span></span>


```C++
HRESULT get_AttachedToVM(
  [out, retval] BSTR *ConfigName
);
```



## <a name="property-value"></a><span data-ttu-id="b643a-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b643a-112">Property value</span></span>

<span data-ttu-id="b643a-113">El nombre de la máquina virtual (VM).</span><span class="sxs-lookup"><span data-stu-id="b643a-113">The name of the virtual machine (VM).</span></span>

## <a name="error-codes"></a><span data-ttu-id="b643a-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="b643a-114">Error codes</span></span>



| <span data-ttu-id="b643a-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="b643a-115">Name/value</span></span>                                                                                                                                                           | <span data-ttu-id="b643a-116">Significado</span><span class="sxs-lookup"><span data-stu-id="b643a-116">Meaning</span></span>                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b643a-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b643a-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="b643a-118">El dispositivo está conectado a la máquina virtual y se devuelve su nombre.</span><span class="sxs-lookup"><span data-stu-id="b643a-118">The device is attached to the VM, and its name is returned.</span></span><br/> |
| <dl> <span data-ttu-id="b643a-119"><dt>S \_ FALSO</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b643a-119"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                           | <span data-ttu-id="b643a-120">El dispositivo está conectado al host.</span><span class="sxs-lookup"><span data-stu-id="b643a-120">The device is attached to the host.</span></span><br/>                         |
| <dl> <span data-ttu-id="b643a-121"><dt>Máquina virtual \_ E 0xA00400929 de \_ \_ \_ máquina virtual externa USB</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b643a-121"><dt>VM\_E\_USB\_EXTERNAL\_VM</dt> <dt>0xA00400929</dt></span></span> </dl> | <span data-ttu-id="b643a-122">El dispositivo está conectado a una máquina virtual en otra sesión de usuario.</span><span class="sxs-lookup"><span data-stu-id="b643a-122">The device is attached to a VM in another user session.</span></span><br/>     |
| <dl> <span data-ttu-id="b643a-123"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b643a-123"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                | <span data-ttu-id="b643a-124">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="b643a-124">The parameter is **NULL**.</span></span><br/>                                  |



## <a name="requirements"></a><span data-ttu-id="b643a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b643a-125">Requirements</span></span>



| <span data-ttu-id="b643a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b643a-126">Requirement</span></span> | <span data-ttu-id="b643a-127">Value</span><span class="sxs-lookup"><span data-stu-id="b643a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b643a-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b643a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b643a-129">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b643a-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b643a-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b643a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b643a-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b643a-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b643a-132">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b643a-132">End of client support</span></span><br/>    | <span data-ttu-id="b643a-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b643a-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b643a-134">Producto</span><span class="sxs-lookup"><span data-stu-id="b643a-134">Product</span></span><br/>                  | <span data-ttu-id="b643a-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b643a-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b643a-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b643a-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b643a-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b643a-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b643a-138">IID</span><span class="sxs-lookup"><span data-stu-id="b643a-138">IID</span></span><br/>                      | <span data-ttu-id="b643a-139">IID \_ IVMUSBDevice se define como 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="b643a-139">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="b643a-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="b643a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b643a-141">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="b643a-141">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

