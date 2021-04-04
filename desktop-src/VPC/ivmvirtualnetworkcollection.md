---
title: Interfaz IVMVirtualNetworkCollection (VPCCOMInterfaces. h)
description: Define una colección de objetos IVMVirtualNetwork. Para obtener un objeto IVMVirtualNetworkCollection, use la propiedad VirtualNetworks de IVMVirtualPC.
ms.assetid: 3d595bc3-1a8d-4e09-a809-944d4dcdc675
keywords:
- Interfaz IVMVirtualNetworkCollection Virtual PC
- Interfaz IVMVirtualNetworkCollection Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76935fd4a67983847e211d8aa53f4a616bed9d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803463"
---
# <a name="ivmvirtualnetworkcollection-interface"></a><span data-ttu-id="1a4f4-106">Interfaz IVMVirtualNetworkCollection</span><span class="sxs-lookup"><span data-stu-id="1a4f4-106">IVMVirtualNetworkCollection interface</span></span>

<span data-ttu-id="1a4f4-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1a4f4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1a4f4-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1a4f4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1a4f4-109">Define una colección de objetos [**IVMVirtualNetwork**](ivmvirtualnetwork.md) .</span><span class="sxs-lookup"><span data-stu-id="1a4f4-109">Defines a collection of [**IVMVirtualNetwork**](ivmvirtualnetwork.md) objects.</span></span> <span data-ttu-id="1a4f4-110">Para obtener un objeto **IVMVirtualNetworkCollection** , use la propiedad [**IVMVirtualPC:: VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) .</span><span class="sxs-lookup"><span data-stu-id="1a4f4-110">To obtain an **IVMVirtualNetworkCollection** object, use the [**IVMVirtualPC::VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="1a4f4-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="1a4f4-111">Members</span></span>

<span data-ttu-id="1a4f4-112">La interfaz **IVMVirtualNetworkCollection** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="1a4f4-112">The **IVMVirtualNetworkCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="1a4f4-113">**IVMVirtualNetworkCollection** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1a4f4-113">**IVMVirtualNetworkCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="1a4f4-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1a4f4-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1a4f4-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1a4f4-115">Properties</span></span>

<span data-ttu-id="1a4f4-116">La interfaz **IVMVirtualNetworkCollection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1a4f4-116">The **IVMVirtualNetworkCollection** interface has these properties.</span></span>



| <span data-ttu-id="1a4f4-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1a4f4-117">Property</span></span>                                                             | <span data-ttu-id="1a4f4-118">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="1a4f4-118">Access type</span></span>          | <span data-ttu-id="1a4f4-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="1a4f4-119">Description</span></span>                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1a4f4-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="1a4f4-120">**\_NewEnum**</span></span>](ivmvirtualnetworkcollection--newenum.md)<br/> | <span data-ttu-id="1a4f4-121">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a4f4-121">Read-only</span></span><br/> | <span data-ttu-id="1a4f4-122">Un enumerador de la colección.</span><span class="sxs-lookup"><span data-stu-id="1a4f4-122">An enumerator for the collection.</span></span><br/>                                                                  |
| [<span data-ttu-id="1a4f4-123">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="1a4f4-123">**Count**</span></span>](ivmvirtualnetworkcollection-count.md)<br/>        | <span data-ttu-id="1a4f4-124">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a4f4-124">Read-only</span></span><br/> | <span data-ttu-id="1a4f4-125">El número de redes virtuales de esta colección.</span><span class="sxs-lookup"><span data-stu-id="1a4f4-125">The number of virtual networks in this collection.</span></span><br/>                                                 |
| [<span data-ttu-id="1a4f4-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1a4f4-126">**Item**</span></span>](ivmvirtualnetworkcollection-item.md)<br/>          | <span data-ttu-id="1a4f4-127">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a4f4-127">Read-only</span></span><br/> | <span data-ttu-id="1a4f4-128">El objeto [**IVMVirtualNetwork**](ivmvirtualnetwork.md) que corresponde al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="1a4f4-128">The [**IVMVirtualNetwork**](ivmvirtualnetwork.md) object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1a4f4-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a4f4-129">Requirements</span></span>



| <span data-ttu-id="1a4f4-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a4f4-130">Requirement</span></span> | <span data-ttu-id="1a4f4-131">Value</span><span class="sxs-lookup"><span data-stu-id="1a4f4-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a4f4-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a4f4-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1a4f4-133">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="1a4f4-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1a4f4-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a4f4-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1a4f4-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1a4f4-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1a4f4-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="1a4f4-136">End of client support</span></span><br/>    | <span data-ttu-id="1a4f4-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1a4f4-137">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="1a4f4-138">Producto</span><span class="sxs-lookup"><span data-stu-id="1a4f4-138">Product</span></span><br/>                  | <span data-ttu-id="1a4f4-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1a4f4-139">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="1a4f4-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1a4f4-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a4f4-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a4f4-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="1a4f4-142">IID</span><span class="sxs-lookup"><span data-stu-id="1a4f4-142">IID</span></span><br/>                      | <span data-ttu-id="1a4f4-143">IID \_ IVMVirtualNetworkCollection se define como 8ed680be-4242-4B2A-a21c-1982d8b0f675</span><span class="sxs-lookup"><span data-stu-id="1a4f4-143">IID\_IVMVirtualNetworkCollection is defined as 8ed680be-4242-4b2a-a21c-1982d8b0f675</span></span><br/> |



 

