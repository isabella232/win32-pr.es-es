---
title: Interfaz IVMNetworkAdapterCollection (VPCCOMInterfaces. h)
description: Define una colección de tarjetas de interfaz de red virtual. Para obtener un objeto IVMNetworkAdapterCollection, use las propiedades IVMVirtualMachine adaptadores, IVMVirtualNetwork adaptadores y IVMVirtualPC UnconnectedNetworkAdapters.
ms.assetid: cfb03a7c-a568-488c-9284-798b7e21027a
keywords:
- Interfaz IVMNetworkAdapterCollection Virtual PC
- Interfaz IVMNetworkAdapterCollection Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8005b88cb873f00708829672cdeb6563b606d42b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079470"
---
# <a name="ivmnetworkadaptercollection-interface"></a><span data-ttu-id="a35fd-106">Interfaz IVMNetworkAdapterCollection</span><span class="sxs-lookup"><span data-stu-id="a35fd-106">IVMNetworkAdapterCollection interface</span></span>

<span data-ttu-id="a35fd-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a35fd-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a35fd-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a35fd-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a35fd-109">Define una colección de tarjetas de interfaz de red virtual.</span><span class="sxs-lookup"><span data-stu-id="a35fd-109">Defines a collection of virtual network interface cards.</span></span> <span data-ttu-id="a35fd-110">Para obtener un objeto IVMNetworkAdapterCollection, use las propiedades [**IVMVirtualMachine:: adaptadores**](ivmvirtualmachine-networkadapters.md), [**IVMVirtualNetwork:: adaptadores**](ivmvirtualnetwork-networkadapters.md)y [**IVMVirtualPC:: UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md) .</span><span class="sxs-lookup"><span data-stu-id="a35fd-110">To obtain an IVMNetworkAdapterCollection object, use the [**IVMVirtualMachine::NetworkAdapters**](ivmvirtualmachine-networkadapters.md), [**IVMVirtualNetwork::NetworkAdapters**](ivmvirtualnetwork-networkadapters.md), and [**IVMVirtualPC::UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md) properties.</span></span>

## <a name="members"></a><span data-ttu-id="a35fd-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="a35fd-111">Members</span></span>

<span data-ttu-id="a35fd-112">La interfaz **IVMNetworkAdapterCollection** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="a35fd-112">The **IVMNetworkAdapterCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="a35fd-113">**IVMNetworkAdapterCollection** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a35fd-113">**IVMNetworkAdapterCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="a35fd-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a35fd-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a35fd-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a35fd-115">Properties</span></span>

<span data-ttu-id="a35fd-116">La interfaz **IVMNetworkAdapterCollection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a35fd-116">The **IVMNetworkAdapterCollection** interface has these properties.</span></span>



| <span data-ttu-id="a35fd-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a35fd-117">Property</span></span>                                                             | <span data-ttu-id="a35fd-118">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="a35fd-118">Access type</span></span>          | <span data-ttu-id="a35fd-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="a35fd-119">Description</span></span>                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a35fd-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="a35fd-120">**\_NewEnum**</span></span>](ivmnetworkadaptercollection--newenum.md)<br/> | <span data-ttu-id="a35fd-121">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a35fd-121">Read-only</span></span><br/> | <span data-ttu-id="a35fd-122">Un enumerador de la colección.</span><span class="sxs-lookup"><span data-stu-id="a35fd-122">An enumerator for the collection.</span></span><br/>                                                                  |
| [<span data-ttu-id="a35fd-123">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="a35fd-123">**Count**</span></span>](ivmnetworkadaptercollection-count.md)<br/>        | <span data-ttu-id="a35fd-124">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a35fd-124">Read-only</span></span><br/> | <span data-ttu-id="a35fd-125">Número de interfaces de red de esta colección.</span><span class="sxs-lookup"><span data-stu-id="a35fd-125">The number of network interfaces in this collection.</span></span><br/>                                               |
| [<span data-ttu-id="a35fd-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a35fd-126">**Item**</span></span>](ivmnetworkadaptercollection-item.md)<br/>          | <span data-ttu-id="a35fd-127">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a35fd-127">Read-only</span></span><br/> | <span data-ttu-id="a35fd-128">El objeto [**IVMNetworkAdapter**](ivmnetworkadapter.md) que corresponde al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="a35fd-128">The [**IVMNetworkAdapter**](ivmnetworkadapter.md) object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a35fd-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a35fd-129">Requirements</span></span>



| <span data-ttu-id="a35fd-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a35fd-130">Requirement</span></span> | <span data-ttu-id="a35fd-131">Value</span><span class="sxs-lookup"><span data-stu-id="a35fd-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a35fd-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a35fd-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a35fd-133">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="a35fd-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a35fd-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a35fd-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a35fd-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a35fd-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a35fd-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a35fd-136">End of client support</span></span><br/>    | <span data-ttu-id="a35fd-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a35fd-137">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="a35fd-138">Producto</span><span class="sxs-lookup"><span data-stu-id="a35fd-138">Product</span></span><br/>                  | <span data-ttu-id="a35fd-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a35fd-139">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="a35fd-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a35fd-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="a35fd-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a35fd-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="a35fd-142">IID</span><span class="sxs-lookup"><span data-stu-id="a35fd-142">IID</span></span><br/>                      | <span data-ttu-id="a35fd-143">IID \_ IVMNetworkAdapterCollection se define como ebaeafe9-eBCD-47cf-866e-ad87d735e479</span><span class="sxs-lookup"><span data-stu-id="a35fd-143">IID\_IVMNetworkAdapterCollection is defined as ebaeafe9-ebcd-47cf-866e-ad87d735e479</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a35fd-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="a35fd-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a35fd-145">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="a35fd-145">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> <dt>

[<span data-ttu-id="a35fd-146">**IVMVirtualMachine:: adaptadores**</span><span class="sxs-lookup"><span data-stu-id="a35fd-146">**IVMVirtualMachine::NetworkAdapters**</span></span>](ivmvirtualmachine-networkadapters.md)
</dt> <dt>

[<span data-ttu-id="a35fd-147">**IVMVirtualNetwork:: adaptadores**</span><span class="sxs-lookup"><span data-stu-id="a35fd-147">**IVMVirtualNetwork::NetworkAdapters**</span></span>](ivmvirtualnetwork-networkadapters.md)
</dt> <dt>

[<span data-ttu-id="a35fd-148">**IVMVirtualPC::UnconnectedNetworkAdapters**</span><span class="sxs-lookup"><span data-stu-id="a35fd-148">**IVMVirtualPC::UnconnectedNetworkAdapters**</span></span>](ivmvirtualpc-unconnectednetworkadapters.md)
</dt> </dl>

 

