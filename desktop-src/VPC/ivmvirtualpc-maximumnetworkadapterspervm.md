---
title: Propiedad IVMVirtualPC MaximumNetworkAdaptersPerVM (VPCCOMInterfaces. h)
description: Número máximo de interfaces de red por máquina virtual.
ms.assetid: 92da4958-5a67-422e-a6bd-68cabf1835ab
keywords:
- Propiedad MaximumNetworkAdaptersPerVM Virtual PC
- Propiedad MaximumNetworkAdaptersPerVM Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, propiedad MaximumNetworkAdaptersPerVM
topic_type:
- apiref
api_name:
- IVMVirtualPC.MaximumNetworkAdaptersPerVM
- IVMVirtualPC.get_MaximumNetworkAdaptersPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0797775038440c566fa7a3397b05632af839a341
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149850"
---
# <a name="ivmvirtualpcmaximumnetworkadapterspervm-property"></a><span data-ttu-id="f2965-106">IVMVirtualPC:: MaximumNetworkAdaptersPerVM (propiedad)</span><span class="sxs-lookup"><span data-stu-id="f2965-106">IVMVirtualPC::MaximumNetworkAdaptersPerVM property</span></span>

<span data-ttu-id="f2965-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f2965-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f2965-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f2965-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f2965-109">Recupera el número máximo de interfaces de red por máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f2965-109">Retrieves the maximum number of networks interfaces per virtual machine.</span></span>

<span data-ttu-id="f2965-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f2965-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2965-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2965-111">Syntax</span></span>


```C++
HRESULT get_MaximumNetworkAdaptersPerVM(
  [out, retval] long *maxNetworkAdapters
);
```



## <a name="property-value"></a><span data-ttu-id="f2965-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f2965-112">Property value</span></span>

<span data-ttu-id="f2965-113">El número máximo de interfaces de red por máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f2965-113">The maximum number of network interfaces per virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f2965-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="f2965-114">Error codes</span></span>



| <span data-ttu-id="f2965-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="f2965-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="f2965-116">Significado</span><span class="sxs-lookup"><span data-stu-id="f2965-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f2965-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f2965-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="f2965-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f2965-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="f2965-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f2965-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="f2965-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="f2965-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="f2965-121"><dt>Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="f2965-121"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="f2965-122">El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).</span><span class="sxs-lookup"><span data-stu-id="f2965-122">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f2965-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2965-123">Requirements</span></span>



| <span data-ttu-id="f2965-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2965-124">Requirement</span></span> | <span data-ttu-id="f2965-125">Value</span><span class="sxs-lookup"><span data-stu-id="f2965-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2965-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2965-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f2965-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="f2965-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f2965-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2965-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f2965-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f2965-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f2965-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="f2965-130">End of client support</span></span><br/>    | <span data-ttu-id="f2965-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f2965-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f2965-132">Producto</span><span class="sxs-lookup"><span data-stu-id="f2965-132">Product</span></span><br/>                  | <span data-ttu-id="f2965-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f2965-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f2965-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2965-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2965-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2965-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f2965-136">IID</span><span class="sxs-lookup"><span data-stu-id="f2965-136">IID</span></span><br/>                      | <span data-ttu-id="f2965-137">IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="f2965-137">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="f2965-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2965-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2965-139">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="f2965-139">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

