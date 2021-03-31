---
title: Propiedad IVMVirtualPC VirtualNetworks (VPCCOMInterfaces. h)
description: Recupera una colección enumerable de redes virtuales.
ms.assetid: 88c68178-0399-44cd-8145-1f2e4d6ac632
keywords:
- Propiedad VirtualNetworks Virtual PC
- Propiedad VirtualNetworks Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, propiedad VirtualNetworks
topic_type:
- apiref
api_name:
- IVMVirtualPC.VirtualNetworks
- IVMVirtualPC.get_VirtualNetworks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf2ea97a7d9bb65bb41842ca028ded88f9a26b63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151171"
---
# <a name="ivmvirtualpcvirtualnetworks-property"></a><span data-ttu-id="e3343-106">IVMVirtualPC:: VirtualNetworks (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e3343-106">IVMVirtualPC::VirtualNetworks property</span></span>

<span data-ttu-id="e3343-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e3343-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e3343-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e3343-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e3343-109">Recupera una colección enumerable de redes virtuales.</span><span class="sxs-lookup"><span data-stu-id="e3343-109">Retrieves an enumerable collection of virtual networks.</span></span>

<span data-ttu-id="e3343-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e3343-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3343-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3343-111">Syntax</span></span>


```C++
HRESULT get_VirtualNetworks(
  [out, retval] IVMVirtualNetworkCollection **virtualNetworkCollection
);
```



## <a name="property-value"></a><span data-ttu-id="e3343-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e3343-112">Property value</span></span>

<span data-ttu-id="e3343-113">Colección de objetos [**IVMVirtualNetwork**](ivmvirtualnetwork.md) .</span><span class="sxs-lookup"><span data-stu-id="e3343-113">A collection of [**IVMVirtualNetwork**](ivmvirtualnetwork.md) objects.</span></span> <span data-ttu-id="e3343-114">Vea [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md).</span><span class="sxs-lookup"><span data-stu-id="e3343-114">See [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="e3343-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="e3343-115">Error codes</span></span>



| <span data-ttu-id="e3343-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="e3343-116">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="e3343-117">Significado</span><span class="sxs-lookup"><span data-stu-id="e3343-117">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e3343-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e3343-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="e3343-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e3343-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="e3343-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e3343-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="e3343-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="e3343-121">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="e3343-122"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e3343-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="e3343-123">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="e3343-123">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="e3343-124"><dt>Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="e3343-124"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="e3343-125">El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).</span><span class="sxs-lookup"><span data-stu-id="e3343-125">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e3343-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3343-126">Requirements</span></span>



| <span data-ttu-id="e3343-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3343-127">Requirement</span></span> | <span data-ttu-id="e3343-128">Value</span><span class="sxs-lookup"><span data-stu-id="e3343-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3343-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3343-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e3343-130">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="e3343-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e3343-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3343-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e3343-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e3343-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e3343-133">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="e3343-133">End of client support</span></span><br/>    | <span data-ttu-id="e3343-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e3343-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e3343-135">Producto</span><span class="sxs-lookup"><span data-stu-id="e3343-135">Product</span></span><br/>                  | <span data-ttu-id="e3343-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e3343-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e3343-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3343-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3343-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3343-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e3343-139">IID</span><span class="sxs-lookup"><span data-stu-id="e3343-139">IID</span></span><br/>                      | <span data-ttu-id="e3343-140">IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="e3343-140">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="e3343-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3343-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3343-142">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="e3343-142">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

