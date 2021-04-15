---
title: Interfaz IVMVirtualNetwork (VPCCOMInterfaces. h)
description: Define una red virtual.
ms.assetid: 1ddafc33-05d4-45fb-924d-9830288aa240
keywords:
- Interfaz IVMVirtualNetwork Virtual PC
- Interfaz IVMVirtualNetwork Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06fb7c759059034874890f1dba7f7e2d1280ea8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105696034"
---
# <a name="ivmvirtualnetwork-interface"></a><span data-ttu-id="6ed10-105">Interfaz IVMVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6ed10-105">IVMVirtualNetwork interface</span></span>

<span data-ttu-id="6ed10-106">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6ed10-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6ed10-107">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6ed10-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6ed10-108">Define una red virtual.</span><span class="sxs-lookup"><span data-stu-id="6ed10-108">Defines a virtual network.</span></span> <span data-ttu-id="6ed10-109">Los objetos **IVMVirtualNetwork** se devuelven desde el método [**IVMVirtualPC**](ivmvirtualpc.md) [**FindVirtualNetwork**](ivmvirtualpc-findvirtualnetwork.md).</span><span class="sxs-lookup"><span data-stu-id="6ed10-109">**IVMVirtualNetwork** objects are returned from [**IVMVirtualPC**](ivmvirtualpc.md) method [**FindVirtualNetwork**](ivmvirtualpc-findvirtualnetwork.md).</span></span> <span data-ttu-id="6ed10-110">También puede recuperar un objeto **IVMVirtualNetwork** del objeto [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md) devuelto desde la propiedad [**IVMVirtualPC:: VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) .</span><span class="sxs-lookup"><span data-stu-id="6ed10-110">You can also retrieve an **IVMVirtualNetwork** object from the [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md) object returned from the [**IVMVirtualPC::VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) property.</span></span>

<span data-ttu-id="6ed10-111">Una red virtual se compone de un conmutador virtual, que realiza todo el enrutamiento interno y varias conexiones que están "conectadas" al conmutador virtual.</span><span class="sxs-lookup"><span data-stu-id="6ed10-111">A virtual network consists of a virtual switch, which performs all internal routing, and several connections that are "plugged in" to the virtual switch.</span></span> <span data-ttu-id="6ed10-112">Estas conexiones pueden ser una conexión de host externo real, una "red interna" o redes compartidas (NAT).</span><span class="sxs-lookup"><span data-stu-id="6ed10-112">These connections can be a real external host connection, an "internal network" or shared networking (NAT).</span></span>

## <a name="members"></a><span data-ttu-id="6ed10-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="6ed10-113">Members</span></span>

<span data-ttu-id="6ed10-114">La interfaz **IVMVirtualNetwork** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="6ed10-114">The **IVMVirtualNetwork** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="6ed10-115">**IVMVirtualNetwork** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6ed10-115">**IVMVirtualNetwork** also has these types of members:</span></span>

-   [<span data-ttu-id="6ed10-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="6ed10-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="6ed10-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6ed10-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6ed10-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="6ed10-118">Methods</span></span>

<span data-ttu-id="6ed10-119">La interfaz **IVMVirtualNetwork** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="6ed10-119">The **IVMVirtualNetwork** interface has these methods.</span></span>



| <span data-ttu-id="6ed10-120">Método</span><span class="sxs-lookup"><span data-stu-id="6ed10-120">Method</span></span>                                | <span data-ttu-id="6ed10-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ed10-121">Description</span></span>                                                          |
|:--------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="6ed10-122">**\_id**</span><span class="sxs-lookup"><span data-stu-id="6ed10-122">**\_ID**</span></span>](ivmvirtualnetwork--id.md) | <span data-ttu-id="6ed10-123">Recupera el identificador interno de la red virtual.</span><span class="sxs-lookup"><span data-stu-id="6ed10-123">Retrieves the internal identifier of the virtual network.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6ed10-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6ed10-124">Properties</span></span>

<span data-ttu-id="6ed10-125">La interfaz **IVMVirtualNetwork** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6ed10-125">The **IVMVirtualNetwork** interface has these properties.</span></span>



| <span data-ttu-id="6ed10-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6ed10-126">Property</span></span>                                                                | <span data-ttu-id="6ed10-127">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="6ed10-127">Access type</span></span>          | <span data-ttu-id="6ed10-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ed10-128">Description</span></span>                                                                    |
|:------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="6ed10-129">**HostAdapter**</span><span class="sxs-lookup"><span data-stu-id="6ed10-129">**HostAdapter**</span></span>](ivmvirtualnetwork-hostadapter.md)<br/>         | <span data-ttu-id="6ed10-130">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ed10-130">Read-only</span></span><br/> | <span data-ttu-id="6ed10-131">El nombre del adaptador al que está conectada la red virtual.</span><span class="sxs-lookup"><span data-stu-id="6ed10-131">The name of the adapter to which the virtual network is connected.</span></span><br/>  |
| <span data-ttu-id="6ed10-132">[**MediaType**](/previous-versions/windows/desktop/legacy/dd796707(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6ed10-132">[**MediaType**](/previous-versions/windows/desktop/legacy/dd796707(v=vs.85))</span></span><br/>             | <span data-ttu-id="6ed10-133">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ed10-133">Read-only</span></span><br/> | <span data-ttu-id="6ed10-134">Determina si la instancia de red virtual es inalámbrica o no.</span><span class="sxs-lookup"><span data-stu-id="6ed10-134">Determines whether the virtual network instance is wireless or not.</span></span><br/> |
| [<span data-ttu-id="6ed10-135">**Name**</span><span class="sxs-lookup"><span data-stu-id="6ed10-135">**Name**</span></span>](ivmvirtualnetwork-name.md)<br/>                       | <span data-ttu-id="6ed10-136">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ed10-136">Read-only</span></span><br/> | <span data-ttu-id="6ed10-137">Nombre único de la instancia de la red virtual.</span><span class="sxs-lookup"><span data-stu-id="6ed10-137">The unique name of the virtual network instance.</span></span><br/>                    |
| [<span data-ttu-id="6ed10-138">**Adaptadores**</span><span class="sxs-lookup"><span data-stu-id="6ed10-138">**NetworkAdapters**</span></span>](ivmvirtualnetwork-networkadapters.md)<br/> | <span data-ttu-id="6ed10-139">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ed10-139">Read-only</span></span><br/> | <span data-ttu-id="6ed10-140">Colección enumerable de NIC conectadas a la red virtual.</span><span class="sxs-lookup"><span data-stu-id="6ed10-140">An enumerable collection of NICs attached to the virtual network.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="6ed10-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ed10-141">Requirements</span></span>



| <span data-ttu-id="6ed10-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ed10-142">Requirement</span></span> | <span data-ttu-id="6ed10-143">Value</span><span class="sxs-lookup"><span data-stu-id="6ed10-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ed10-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ed10-144">Minimum supported client</span></span><br/> | <span data-ttu-id="6ed10-145">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="6ed10-145">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6ed10-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ed10-146">Minimum supported server</span></span><br/> | <span data-ttu-id="6ed10-147">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6ed10-147">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6ed10-148">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="6ed10-148">End of client support</span></span><br/>    | <span data-ttu-id="6ed10-149">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6ed10-149">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6ed10-150">Producto</span><span class="sxs-lookup"><span data-stu-id="6ed10-150">Product</span></span><br/>                  | <span data-ttu-id="6ed10-151">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6ed10-151">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6ed10-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ed10-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ed10-153"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ed10-153"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6ed10-154">IID</span><span class="sxs-lookup"><span data-stu-id="6ed10-154">IID</span></span><br/>                      | <span data-ttu-id="6ed10-155">IID \_ IVMVirtualNetwork se define como 431cb7a1-2469-4563-b94e-38b987adca63</span><span class="sxs-lookup"><span data-stu-id="6ed10-155">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



 

