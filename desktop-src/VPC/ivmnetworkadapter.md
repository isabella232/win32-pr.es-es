---
title: Interfaz IVMNetworkAdapter (VPCCOMInterfaces. h)
description: Actúa como la interfaz de una tarjeta de interfaz de red virtual.
ms.assetid: df050706-09be-47d1-9ae1-1eb0e1836d64
keywords:
- Interfaz IVMNetworkAdapter Virtual PC
- Interfaz IVMNetworkAdapter Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74a0ccf722715896743129b6666609bd8a88df3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422358"
---
# <a name="ivmnetworkadapter-interface"></a><span data-ttu-id="59435-105">Interfaz IVMNetworkAdapter</span><span class="sxs-lookup"><span data-stu-id="59435-105">IVMNetworkAdapter interface</span></span>

<span data-ttu-id="59435-106">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="59435-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="59435-107">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="59435-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="59435-108">Actúa como la interfaz de una tarjeta de interfaz de red virtual (NIC).</span><span class="sxs-lookup"><span data-stu-id="59435-108">Serves as the interface to a virtual network interface card (NIC).</span></span> <span data-ttu-id="59435-109">Se usa para configurar el modo en que una máquina virtual está en red.</span><span class="sxs-lookup"><span data-stu-id="59435-109">It is used to set up how a virtual machine is networked.</span></span> <span data-ttu-id="59435-110">Las tarjetas de interfaz de red se pueden agregar y quitar mediante [**IVMVirtualMachine:: AddNetworkAdapter**](ivmvirtualmachine-addnetworkadapter.md) y [**IVMVirtualMachine:: RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="59435-110">Network interface cards can be added and removed by using [**IVMVirtualMachine::AddNetworkAdapter**](ivmvirtualmachine-addnetworkadapter.md) and [**IVMVirtualMachine::RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md).</span></span> <span data-ttu-id="59435-111">También puede recuperar un objeto **IVMNetworkAdapter** de la colección [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) devuelta desde las propiedades [**IVMVirtualMachine:: adaptadores**](ivmvirtualmachine-networkadapters.md) o [**IVMVirtualNetwork:: adaptadores**](ivmvirtualnetwork-networkadapters.md) .</span><span class="sxs-lookup"><span data-stu-id="59435-111">You can also retrieve an **IVMNetworkAdapter** object from the [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) collection returned from the [**IVMVirtualMachine::NetworkAdapters**](ivmvirtualmachine-networkadapters.md) or [**IVMVirtualNetwork::NetworkAdapters**](ivmvirtualnetwork-networkadapters.md) properties.</span></span>

## <a name="members"></a><span data-ttu-id="59435-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="59435-112">Members</span></span>

<span data-ttu-id="59435-113">La interfaz **IVMNetworkAdapter** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="59435-113">The **IVMNetworkAdapter** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="59435-114">**IVMNetworkAdapter** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="59435-114">**IVMNetworkAdapter** also has these types of members:</span></span>

-   [<span data-ttu-id="59435-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="59435-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="59435-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="59435-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="59435-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="59435-117">Methods</span></span>

<span data-ttu-id="59435-118">La interfaz **IVMNetworkAdapter** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="59435-118">The **IVMNetworkAdapter** interface has these methods.</span></span>



| <span data-ttu-id="59435-119">Método</span><span class="sxs-lookup"><span data-stu-id="59435-119">Method</span></span>                                                                         | <span data-ttu-id="59435-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="59435-120">Description</span></span>                                                                 |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="59435-121">**\_id**</span><span class="sxs-lookup"><span data-stu-id="59435-121">**\_ID**</span></span>](ivmnetworkadapter--id.md)                                          | <span data-ttu-id="59435-122">Recupera el identificador interno de esta interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="59435-122">Retrieves the internal identifier of this network interface.</span></span><br/>     |
| [<span data-ttu-id="59435-123">**AttachToVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="59435-123">**AttachToVirtualNetwork**</span></span>](ivmnetworkadapter-attachtovirtualnetwork.md)     | <span data-ttu-id="59435-124">Conecta la interfaz de red a la red virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="59435-124">Attaches the network interface to the specified virtual network.</span></span><br/> |
| [<span data-ttu-id="59435-125">**DetachFromVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="59435-125">**DetachFromVirtualNetwork**</span></span>](ivmnetworkadapter-detachfromvirtualnetwork.md) | <span data-ttu-id="59435-126">Desasocia la interfaz de red de su red virtual.</span><span class="sxs-lookup"><span data-stu-id="59435-126">Detaches the network interface from its virtual network.</span></span><br/>         |



 

### <a name="properties"></a><span data-ttu-id="59435-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="59435-127">Properties</span></span>

<span data-ttu-id="59435-128">La interfaz **IVMNetworkAdapter** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="59435-128">The **IVMNetworkAdapter** interface has these properties.</span></span>



| <span data-ttu-id="59435-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="59435-129">Property</span></span>                                                                                  | <span data-ttu-id="59435-130">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="59435-130">Access type</span></span>           | <span data-ttu-id="59435-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="59435-131">Description</span></span>                                                                 |
|:------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="59435-132">**Denominaba ethernetaddress**</span><span class="sxs-lookup"><span data-stu-id="59435-132">**EthernetAddress**</span></span>](ivmnetworkadapter-ethernetaddress.md)<br/>                   | <span data-ttu-id="59435-133">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="59435-133">Read/write</span></span><br/> | <span data-ttu-id="59435-134">Dirección Ethernet (MAC) de la interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="59435-134">The Ethernet (MAC) address of the network interface.</span></span><br/>             |
| [<span data-ttu-id="59435-135">**IsEthernetAddressDynamic**</span><span class="sxs-lookup"><span data-stu-id="59435-135">**IsEthernetAddressDynamic**</span></span>](ivmnetworkadapter-isethernetaddressdynamic.md)<br/> | <span data-ttu-id="59435-136">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="59435-136">Read/write</span></span><br/> | <span data-ttu-id="59435-137">Indica si la dirección Ethernet se genera dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="59435-137">Indicates whether the Ethernet address is dynamically generated.</span></span><br/> |
| [<span data-ttu-id="59435-138">**VirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="59435-138">**VirtualMachine**</span></span>](ivmnetworkadapter-virtualmachine.md)<br/>                     | <span data-ttu-id="59435-139">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="59435-139">Read-only</span></span><br/>  | <span data-ttu-id="59435-140">La máquina virtual asociada a esta interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="59435-140">The virtual machine associated with this network interface.</span></span><br/>      |
| [<span data-ttu-id="59435-141">**VirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="59435-141">**VirtualNetwork**</span></span>](ivmnetworkadapter-virtualnetwork.md)<br/>                     | <span data-ttu-id="59435-142">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="59435-142">Read-only</span></span><br/>  | <span data-ttu-id="59435-143">La red virtual a la que está conectada la interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="59435-143">The virtual network to which the network interface is attached.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="59435-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="59435-144">Remarks</span></span>

<span data-ttu-id="59435-145">La dirección Ethernet predeterminada para una interfaz de red es "00-00-00-00-00-00", que se considera una dirección Ethernet no válida en la mayoría de los sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="59435-145">The default Ethernet address for a network interface is "00-00-00-00-00-00", which is considered an invalid Ethernet address by most operating systems.</span></span> <span data-ttu-id="59435-146">Si [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) se establece en **false**, [**denominaba ethernetaddress**](ivmnetworkadapter-ethernetaddress.md) se debe inicializar con una dirección de red Ethernet válida.</span><span class="sxs-lookup"><span data-stu-id="59435-146">If [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) is set to **FALSE**, [**EthernetAddress**](ivmnetworkadapter-ethernetaddress.md) must be initialized with a valid Ethernet network address.</span></span>

<span data-ttu-id="59435-147">En los procedimientos siguientes se explica cómo usar la interfaz **IVMNetworkAdapter** .</span><span class="sxs-lookup"><span data-stu-id="59435-147">The following procedures explain how to use the **IVMNetworkAdapter** interface.</span></span>

<span data-ttu-id="59435-148">**Para asociar una NIC virtual a una NIC de host**</span><span class="sxs-lookup"><span data-stu-id="59435-148">**To attach a virtual NIC to a host NIC**</span></span>

-   <span data-ttu-id="59435-149">Las NIC virtuales (invitado) no se conectan directamente a una NIC de host.</span><span class="sxs-lookup"><span data-stu-id="59435-149">Virtual (guest) NICs are not attached directly to a host NIC.</span></span> <span data-ttu-id="59435-150">En su lugar, la NIC virtual se conecta a una red virtual que está conectada a una NIC de host.</span><span class="sxs-lookup"><span data-stu-id="59435-150">Instead, the virtual NIC is attached to a virtual network that is attached to a host NIC.</span></span> <span data-ttu-id="59435-151">Para obtener más información sobre la configuración de redes virtuales, vea [**IVMVirtualNetwork**](ivmvirtualnetwork.md).</span><span class="sxs-lookup"><span data-stu-id="59435-151">For more information about configuring virtual networks, see [**IVMVirtualNetwork**](ivmvirtualnetwork.md).</span></span> <span data-ttu-id="59435-152">Para asociar la NIC virtual a una red virtual, use el método [**AttachToVirtualNetwork**](ivmnetworkadapter-attachtovirtualnetwork.md) .</span><span class="sxs-lookup"><span data-stu-id="59435-152">To attach the virtual NIC to a virtual network, use the [**AttachToVirtualNetwork**](ivmnetworkadapter-attachtovirtualnetwork.md) method.</span></span>

<span data-ttu-id="59435-153">**Para desconectar una NIC virtual de la red virtual**</span><span class="sxs-lookup"><span data-stu-id="59435-153">**To disconnect a virtual NIC from the virtual network**</span></span>

-   <span data-ttu-id="59435-154">El método [**DetachFromVirtualNetwork**](ivmnetworkadapter-detachfromvirtualnetwork.md) desasociará la NIC virtual de la red virtual.</span><span class="sxs-lookup"><span data-stu-id="59435-154">The [**DetachFromVirtualNetwork**](ivmnetworkadapter-detachfromvirtualnetwork.md) method will detach the virtual NIC from the virtual network.</span></span> <span data-ttu-id="59435-155">Después de llamar a esta función, la propiedad [**VirtualNetwork**](ivmnetworkadapter-virtualnetwork.md) devolverá un identificador de red virtual que no es válido.</span><span class="sxs-lookup"><span data-stu-id="59435-155">After this function is called, the [**VirtualNetwork**](ivmnetworkadapter-virtualnetwork.md) property will return a virtual network ID that is not valid.</span></span>

<span data-ttu-id="59435-156">**Para quitar una NIC virtual de una máquina virtual si tiene el objeto NIC virtual**</span><span class="sxs-lookup"><span data-stu-id="59435-156">**To remove a virtual NIC from a virtual machine if you have the virtual NIC object**</span></span>

1.  <span data-ttu-id="59435-157">Obtenga la máquina virtual asociada a la NIC virtual mediante la propiedad [**VirtualMachine**](ivmnetworkadapter-virtualmachine.md) .</span><span class="sxs-lookup"><span data-stu-id="59435-157">Get the virtual machine associated with the virtual NIC by using the [**VirtualMachine**](ivmnetworkadapter-virtualmachine.md) property.</span></span>
2.  <span data-ttu-id="59435-158">Use el objeto actual como parámetro para el método [**IVMVirtualMachine:: RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="59435-158">Use the current object as a parameter to the [**IVMVirtualMachine::RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="59435-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59435-159">Requirements</span></span>



| <span data-ttu-id="59435-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="59435-160">Requirement</span></span> | <span data-ttu-id="59435-161">Value</span><span class="sxs-lookup"><span data-stu-id="59435-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="59435-162">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59435-162">Minimum supported client</span></span><br/> | <span data-ttu-id="59435-163">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="59435-163">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="59435-164">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59435-164">Minimum supported server</span></span><br/> | <span data-ttu-id="59435-165">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="59435-165">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="59435-166">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="59435-166">End of client support</span></span><br/>    | <span data-ttu-id="59435-167">Windows 7</span><span class="sxs-lookup"><span data-stu-id="59435-167">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="59435-168">Producto</span><span class="sxs-lookup"><span data-stu-id="59435-168">Product</span></span><br/>                  | <span data-ttu-id="59435-169">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="59435-169">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="59435-170">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59435-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="59435-171"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="59435-171"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="59435-172">IID</span><span class="sxs-lookup"><span data-stu-id="59435-172">IID</span></span><br/>                      | <span data-ttu-id="59435-173">IID \_ IVMNetworkAdapter se define como e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="59435-173">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



 

