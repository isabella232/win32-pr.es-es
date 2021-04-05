---
title: Propiedad IVMNetworkAdapter VirtualNetwork (VPCCOMInterfaces. h)
description: Recupera la red virtual a la que está conectada la interfaz de red.
ms.assetid: 7f52fd86-5f83-41d8-ba48-7db65e9c357c
keywords:
- Propiedad VirtualNetwork Virtual PC
- Propiedad VirtualNetwork Virtual PC, interfaz IVMNetworkAdapter
- Interfaz IVMNetworkAdapter Virtual PC, propiedad VirtualNetwork
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.VirtualNetwork
- IVMNetworkAdapter.get_VirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b932ef553d3952fbc69edba3416ac20049984810
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078810"
---
# <a name="ivmnetworkadaptervirtualnetwork-property"></a><span data-ttu-id="2ca52-106">IVMNetworkAdapter:: VirtualNetwork (propiedad)</span><span class="sxs-lookup"><span data-stu-id="2ca52-106">IVMNetworkAdapter::VirtualNetwork property</span></span>

<span data-ttu-id="2ca52-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2ca52-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2ca52-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2ca52-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2ca52-109">Recupera la red virtual a la que está conectada la interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="2ca52-109">Retrieves the virtual network to which the network interface is attached.</span></span>

<span data-ttu-id="2ca52-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2ca52-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ca52-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ca52-111">Syntax</span></span>


```C++
HRESULT get_VirtualNetwork(
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="property-value"></a><span data-ttu-id="2ca52-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2ca52-112">Property value</span></span>

<span data-ttu-id="2ca52-113">Una interfaz [**IVMVirtualNetwork**](ivmvirtualnetwork.md) que representa la red virtual a la que está conectada esta interfaz de red virtual.</span><span class="sxs-lookup"><span data-stu-id="2ca52-113">An [**IVMVirtualNetwork**](ivmvirtualnetwork.md) interface that represents the virtual network to which this virtual network interface is attached.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2ca52-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="2ca52-114">Error codes</span></span>



| <span data-ttu-id="2ca52-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="2ca52-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="2ca52-116">Significado</span><span class="sxs-lookup"><span data-stu-id="2ca52-116">Meaning</span></span>                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2ca52-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2ca52-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="2ca52-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="2ca52-118">The operation was successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="2ca52-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2ca52-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="2ca52-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="2ca52-120">The parameter is **NULL**.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="2ca52-121"><dt>S \_ FALSO</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2ca52-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="2ca52-122">Esta interfaz de red está desconectada y no está conectada a una red virtual.</span><span class="sxs-lookup"><span data-stu-id="2ca52-122">This network interface is unplugged and is not connected to a virtual network.</span></span><br/> |
| <dl> <span data-ttu-id="2ca52-123"><dt>Máquina virtual \_ E \_ \_ \_ \_ ID. de red virtual no válido</dt> <dt>0xA00400702</dt></span><span class="sxs-lookup"><span data-stu-id="2ca52-123"><dt>VM\_E\_INVALID\_VIRTUAL\_NETWORK\_ID</dt> <dt>0xA00400702</dt></span></span> </dl> | <span data-ttu-id="2ca52-124">Esta interfaz está conectada a una red virtual con un identificador no válido.</span><span class="sxs-lookup"><span data-stu-id="2ca52-124">This interface is connected to a virtual network with an invalid ID.</span></span><br/>           |
| <dl> <span data-ttu-id="2ca52-125"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2ca52-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="2ca52-126">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="2ca52-126">An unexpected error has occurred.</span></span><br/>                                              |



## <a name="requirements"></a><span data-ttu-id="2ca52-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ca52-127">Requirements</span></span>



| <span data-ttu-id="2ca52-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ca52-128">Requirement</span></span> | <span data-ttu-id="2ca52-129">Value</span><span class="sxs-lookup"><span data-stu-id="2ca52-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ca52-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ca52-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2ca52-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="2ca52-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2ca52-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ca52-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2ca52-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2ca52-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2ca52-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="2ca52-134">End of client support</span></span><br/>    | <span data-ttu-id="2ca52-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2ca52-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2ca52-136">Producto</span><span class="sxs-lookup"><span data-stu-id="2ca52-136">Product</span></span><br/>                  | <span data-ttu-id="2ca52-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2ca52-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2ca52-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ca52-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ca52-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ca52-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2ca52-140">IID</span><span class="sxs-lookup"><span data-stu-id="2ca52-140">IID</span></span><br/>                      | <span data-ttu-id="2ca52-141">IID \_ IVMNetworkAdapter se define como e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="2ca52-141">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="2ca52-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ca52-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ca52-143">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="2ca52-143">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

