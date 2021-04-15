---
title: Interfaz IMsRdpDeviceCollection
description: Representa una colección de objetos de dispositivo.
ms.assetid: 9731b16b-12e0-457e-a4e5-a55d8a6db582
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpDeviceCollection
- Servicios de Escritorio remoto de la interfaz IMsRdpDeviceCollection, descrito
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cace1bc684be4e3e8cf20db84ec8923c9b35a8fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421925"
---
# <a name="imsrdpdevicecollection-interface"></a><span data-ttu-id="a906d-105">Interfaz IMsRdpDeviceCollection</span><span class="sxs-lookup"><span data-stu-id="a906d-105">IMsRdpDeviceCollection interface</span></span>

<span data-ttu-id="a906d-106">Representa una colección de objetos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a906d-106">Represents a collection of device objects.</span></span>

## <a name="members"></a><span data-ttu-id="a906d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="a906d-107">Members</span></span>

<span data-ttu-id="a906d-108">La interfaz **IMsRdpDeviceCollection** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a906d-108">The **IMsRdpDeviceCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a906d-109">**IMsRdpDeviceCollection** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a906d-109">**IMsRdpDeviceCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="a906d-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="a906d-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="a906d-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a906d-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a906d-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="a906d-112">Methods</span></span>

<span data-ttu-id="a906d-113">La interfaz **IMsRdpDeviceCollection** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a906d-113">The **IMsRdpDeviceCollection** interface has these methods.</span></span>



| <span data-ttu-id="a906d-114">Método</span><span class="sxs-lookup"><span data-stu-id="a906d-114">Method</span></span>                                                        | <span data-ttu-id="a906d-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="a906d-115">Description</span></span>                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="a906d-116">**RescanDevices**</span><span class="sxs-lookup"><span data-stu-id="a906d-116">**RescanDevices**</span></span>](imsrdpdevicecollection-rescandevices.md) | <span data-ttu-id="a906d-117">Actualiza la lista de objetos de la colección.</span><span class="sxs-lookup"><span data-stu-id="a906d-117">Refreshes the list of objects in the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a906d-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a906d-118">Properties</span></span>

<span data-ttu-id="a906d-119">La interfaz **IMsRdpDeviceCollection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a906d-119">The **IMsRdpDeviceCollection** interface has these properties.</span></span>



| <span data-ttu-id="a906d-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a906d-120">Property</span></span>                                                                 | <span data-ttu-id="a906d-121">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="a906d-121">Access type</span></span>          | <span data-ttu-id="a906d-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="a906d-122">Description</span></span>                                                    |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------|
| [<span data-ttu-id="a906d-123">**DeviceById**</span><span class="sxs-lookup"><span data-stu-id="a906d-123">**DeviceById**</span></span>](imsrdpdevicecollection-devicebyid.md)<br/>       | <span data-ttu-id="a906d-124">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a906d-124">Read-only</span></span><br/> | <span data-ttu-id="a906d-125">Recupera el dispositivo con el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="a906d-125">Retrieves the device with the specified identifier.</span></span><br/> |
| [<span data-ttu-id="a906d-126">**DeviceByIndex**</span><span class="sxs-lookup"><span data-stu-id="a906d-126">**DeviceByIndex**</span></span>](imsrdpdevicecollection-devicebyindex.md)<br/> | <span data-ttu-id="a906d-127">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a906d-127">Read-only</span></span><br/> | <span data-ttu-id="a906d-128">Recupera el dispositivo en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="a906d-128">Retrieves the device at the specified index.</span></span><br/>        |
| [<span data-ttu-id="a906d-129">**DeviceCount**</span><span class="sxs-lookup"><span data-stu-id="a906d-129">**DeviceCount**</span></span>](imsrdpdevicecollection-devicecount.md)<br/>     | <span data-ttu-id="a906d-130">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a906d-130">Read-only</span></span><br/> | <span data-ttu-id="a906d-131">Recupera el recuento de objetos de la colección.</span><span class="sxs-lookup"><span data-stu-id="a906d-131">Retrieves the count of objects in the collection.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="a906d-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a906d-132">Requirements</span></span>



| <span data-ttu-id="a906d-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a906d-133">Requirement</span></span> | <span data-ttu-id="a906d-134">Value</span><span class="sxs-lookup"><span data-stu-id="a906d-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a906d-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a906d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a906d-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a906d-136">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="a906d-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a906d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a906d-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a906d-138">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="a906d-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a906d-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="a906d-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a906d-140"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="a906d-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a906d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a906d-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a906d-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="a906d-143">IID</span><span class="sxs-lookup"><span data-stu-id="a906d-143">IID</span></span><br/>                      | <span data-ttu-id="a906d-144">IID \_ IMsRdpDeviceCollection se define como 56540617-D281-488C-8738-6a8fdf64a118</span><span class="sxs-lookup"><span data-stu-id="a906d-144">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a906d-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="a906d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a906d-146">Referencia de Conexión web a Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="a906d-146">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="a906d-147">**IMsRdpDevice**</span><span class="sxs-lookup"><span data-stu-id="a906d-147">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

