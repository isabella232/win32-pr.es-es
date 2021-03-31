---
title: Propiedad IVMVirtualNetwork HostAdapter (VPCCOMInterfaces. h)
description: Nombre del adaptador al que está conectada la red virtual.
ms.assetid: 7ee074d2-13ba-42db-84db-ecfd22576a9a
keywords:
- Propiedad HostAdapter Virtual PC
- Propiedad HostAdapter Virtual PC, interfaz IVMVirtualNetwork
- Interfaz IVMVirtualNetwork Virtual PC, propiedad HostAdapter
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.HostAdapter
- IVMVirtualNetwork.get_HostAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0485303c2328a85c70779f16652121729546f3ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079629"
---
# <a name="ivmvirtualnetworkhostadapter-property"></a><span data-ttu-id="a65e7-106">IVMVirtualNetwork:: HostAdapter (propiedad)</span><span class="sxs-lookup"><span data-stu-id="a65e7-106">IVMVirtualNetwork::HostAdapter property</span></span>

<span data-ttu-id="a65e7-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a65e7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a65e7-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a65e7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a65e7-109">Recupera el nombre del adaptador al que está conectada la red virtual.</span><span class="sxs-lookup"><span data-stu-id="a65e7-109">Retrieves the name of the adapter to which the virtual network is connected.</span></span>

<span data-ttu-id="a65e7-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a65e7-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a65e7-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a65e7-111">Syntax</span></span>


```C++
HRESULT get_HostAdapter(
  [out, retval] BSTR *hostAdapter
);
```



## <a name="property-value"></a><span data-ttu-id="a65e7-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a65e7-112">Property value</span></span>

<span data-ttu-id="a65e7-113">El nombre del adaptador de host al que está conectada la red virtual.</span><span class="sxs-lookup"><span data-stu-id="a65e7-113">The name of the host adapter to which the virtual network is connected.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a65e7-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="a65e7-114">Error codes</span></span>



| <span data-ttu-id="a65e7-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="a65e7-115">Name/value</span></span>                                                                                                                                                            | <span data-ttu-id="a65e7-116">Significado</span><span class="sxs-lookup"><span data-stu-id="a65e7-116">Meaning</span></span>                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a65e7-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a65e7-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="a65e7-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a65e7-118">The operation was successful.</span></span><br/>                                                                                                                              |
| <dl> <span data-ttu-id="a65e7-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a65e7-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                 | <span data-ttu-id="a65e7-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="a65e7-120">The parameter is **NULL**.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="a65e7-121"><dt>Máquina virtual \_ \_ \_ No \_ se encontró el adaptador E</dt> <dt>0xA0040700</dt></span><span class="sxs-lookup"><span data-stu-id="a65e7-121"><dt>VM\_E\_ADAPTER\_NOT\_FOUND</dt> <dt>0xA0040700</dt></span></span> </dl> | <span data-ttu-id="a65e7-122">El adaptador Ethernet del host al que estaba conectada esta red virtual ya no está disponible.</span><span class="sxs-lookup"><span data-stu-id="a65e7-122">The host Ethernet adapter to which this virtual network was connected is no longer available.</span></span> <span data-ttu-id="a65e7-123">Es posible que se haya quitado o deshabilitado el adaptador Ethernet del host.</span><span class="sxs-lookup"><span data-stu-id="a65e7-123">The host Ethernet adapter may have been removed or disabled.</span></span><br/> |
| <dl> <span data-ttu-id="a65e7-124"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a65e7-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="a65e7-125">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="a65e7-125">An unexpected error has occurred.</span></span><br/>                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="a65e7-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a65e7-126">Remarks</span></span>

<span data-ttu-id="a65e7-127">El adaptador de red virtual permite que una red virtual se comunique con redes externas.</span><span class="sxs-lookup"><span data-stu-id="a65e7-127">The virtual network adapter allows a virtual network to talk to external networks.</span></span> <span data-ttu-id="a65e7-128">Normalmente, hay un adaptador por cada adaptador Ethernet instalado en el equipo host.</span><span class="sxs-lookup"><span data-stu-id="a65e7-128">There is normally one adapter per Ethernet adapter installed in the host machine.</span></span> <span data-ttu-id="a65e7-129">Por ejemplo, supongamos que un equipo host tenía un adaptador con la etiqueta "10/100 ENET".</span><span class="sxs-lookup"><span data-stu-id="a65e7-129">For example, let's say a host machine had an adapter labeled "10/100 ENET".</span></span> <span data-ttu-id="a65e7-130">Para conectar una NIC virtual a la red conectada a "10/100 ENET", establezca la propiedad **HostAdapter** de red de la red virtual en "10/100 ENET" y conecte la NIC virtual a esta red virtual.</span><span class="sxs-lookup"><span data-stu-id="a65e7-130">To connect a virtual NIC to the network attached to "10/100 ENET", set the virtual network's Network **HostAdapter** property to "10/100 ENET" and connect the virtual NIC to this virtual network.</span></span>

<span data-ttu-id="a65e7-131">Si la propiedad **HostAdapter** se establece en una cadena vacía (""), el adaptador de NIC virtual se conecta a la red "red interna" o "redes compartidas (NAT)".</span><span class="sxs-lookup"><span data-stu-id="a65e7-131">If the **HostAdapter** property is set to an empty string (""), the virtual NIC adapter is connected to the "Internal Network" or "Shared Networking (NAT)" network.</span></span> <span data-ttu-id="a65e7-132">Las NIC virtuales conectadas a la red "red interna" no tendrán acceso a las redes externas en el host del sistema.</span><span class="sxs-lookup"><span data-stu-id="a65e7-132">Virtual NICs attached to the "Internal Network" network will have no access to external networks on the system host.</span></span> <span data-ttu-id="a65e7-133">Sin embargo, las NIC virtuales conectadas a esta red virtual siguen pudiendo comunicarse entre sí.</span><span class="sxs-lookup"><span data-stu-id="a65e7-133">However, the virtual NICs attached to this virtual network are still able to communicate with each other.</span></span>

<span data-ttu-id="a65e7-134">Se puede tener acceso a la lista completa de adaptadores a través de la propiedad [**IVMHostInfo:: adaptadores**](ivmhostinfo-networkadapters.md) .</span><span class="sxs-lookup"><span data-stu-id="a65e7-134">The complete list of adapters can be accessed through the [**IVMHostInfo::NetworkAdapters**](ivmhostinfo-networkadapters.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="a65e7-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a65e7-135">Requirements</span></span>



| <span data-ttu-id="a65e7-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="a65e7-136">Requirement</span></span> | <span data-ttu-id="a65e7-137">Value</span><span class="sxs-lookup"><span data-stu-id="a65e7-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a65e7-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a65e7-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a65e7-139">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="a65e7-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a65e7-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a65e7-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a65e7-141">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a65e7-141">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a65e7-142">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a65e7-142">End of client support</span></span><br/>    | <span data-ttu-id="a65e7-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a65e7-143">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a65e7-144">Producto</span><span class="sxs-lookup"><span data-stu-id="a65e7-144">Product</span></span><br/>                  | <span data-ttu-id="a65e7-145">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a65e7-145">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a65e7-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a65e7-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="a65e7-147"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a65e7-147"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a65e7-148">IID</span><span class="sxs-lookup"><span data-stu-id="a65e7-148">IID</span></span><br/>                      | <span data-ttu-id="a65e7-149">IID \_ IVMVirtualNetwork se define como 431cb7a1-2469-4563-b94e-38b987adca63</span><span class="sxs-lookup"><span data-stu-id="a65e7-149">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="a65e7-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="a65e7-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a65e7-151">**IVMVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="a65e7-151">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> </dl>

 

