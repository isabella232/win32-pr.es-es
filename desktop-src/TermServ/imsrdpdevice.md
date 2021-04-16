---
title: Interfaz IMsRdpDevice
description: Contiene información sobre un objeto de dispositivo.
ms.assetid: b486a591-870b-446c-8028-9e4406cdf0ce
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpDevice
- Servicios de Escritorio remoto de la interfaz IMsRdpDevice, descrito
topic_type:
- apiref
api_name:
- IMsRdpDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ddfbb739a8cf8e93ee2c2214e14095ac68bd77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676635"
---
# <a name="imsrdpdevice-interface"></a><span data-ttu-id="a4d89-105">Interfaz IMsRdpDevice</span><span class="sxs-lookup"><span data-stu-id="a4d89-105">IMsRdpDevice interface</span></span>

<span data-ttu-id="a4d89-106">Contiene información sobre un objeto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4d89-106">Contains information about a device object.</span></span>

## <a name="members"></a><span data-ttu-id="a4d89-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="a4d89-107">Members</span></span>

<span data-ttu-id="a4d89-108">La interfaz **IMsRdpDevice** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a4d89-108">The **IMsRdpDevice** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a4d89-109">**IMsRdpDevice** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a4d89-109">**IMsRdpDevice** also has these types of members:</span></span>

-   [<span data-ttu-id="a4d89-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a4d89-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a4d89-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a4d89-111">Properties</span></span>

<span data-ttu-id="a4d89-112">La interfaz **IMsRdpDevice** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a4d89-112">The **IMsRdpDevice** interface has these properties.</span></span>



| <span data-ttu-id="a4d89-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a4d89-113">Property</span></span>                                                               | <span data-ttu-id="a4d89-114">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="a4d89-114">Access type</span></span>           | <span data-ttu-id="a4d89-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4d89-115">Description</span></span>                                                                                                   |
|:-----------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a4d89-116">**DeviceDescription**</span><span class="sxs-lookup"><span data-stu-id="a4d89-116">**DeviceDescription**</span></span>](imsrdpdevice-devicedescription.md)<br/> | <span data-ttu-id="a4d89-117">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a4d89-117">Read-only</span></span><br/>  | <span data-ttu-id="a4d89-118">Recupera la descripción del dispositivo que se va a mostrar al usuario si el nombre para mostrar no está disponible.</span><span class="sxs-lookup"><span data-stu-id="a4d89-118">Retrieves the device description to be displayed to the user if the display name is not available.</span></span><br/> |
| [<span data-ttu-id="a4d89-119">**DeviceInstanceId**</span><span class="sxs-lookup"><span data-stu-id="a4d89-119">**DeviceInstanceId**</span></span>](imsrdpdevice-deviceinstanceid.md)<br/>   | <span data-ttu-id="a4d89-120">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a4d89-120">Read-only</span></span><br/>  | <span data-ttu-id="a4d89-121">Recupera el identificador de instancia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4d89-121">Retrieves the device instance identifier of the device.</span></span><br/>                                            |
| [<span data-ttu-id="a4d89-122">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="a4d89-122">**FriendlyName**</span></span>](imsrdpdevice-friendlyname.md)<br/>           | <span data-ttu-id="a4d89-123">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a4d89-123">Read-only</span></span><br/>  | <span data-ttu-id="a4d89-124">Recupera el nombre para mostrar del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4d89-124">Retrieves the display name for the device.</span></span><br/>                                                         |
| [<span data-ttu-id="a4d89-125">**RedirectionState**</span><span class="sxs-lookup"><span data-stu-id="a4d89-125">**RedirectionState**</span></span>](imsrdpdevice-redirectionstate.md)<br/>   | <span data-ttu-id="a4d89-126">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a4d89-126">Read/write</span></span><br/> | <span data-ttu-id="a4d89-127">Indica el estado de la redirección del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4d89-127">Indicates the redirection state of the device.</span></span><br/>                                                     |



 

## <a name="requirements"></a><span data-ttu-id="a4d89-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4d89-128">Requirements</span></span>



| <span data-ttu-id="a4d89-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4d89-129">Requirement</span></span> | <span data-ttu-id="a4d89-130">Value</span><span class="sxs-lookup"><span data-stu-id="a4d89-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4d89-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4d89-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a4d89-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4d89-132">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a4d89-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4d89-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a4d89-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4d89-134">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a4d89-135">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a4d89-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="a4d89-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4d89-136"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a4d89-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a4d89-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4d89-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4d89-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a4d89-139">IID</span><span class="sxs-lookup"><span data-stu-id="a4d89-139">IID</span></span><br/>                      | <span data-ttu-id="a4d89-140">IID \_ IMsRdpDevice se define como 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span><span class="sxs-lookup"><span data-stu-id="a4d89-140">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="a4d89-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4d89-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4d89-142">Referencia de Conexión web a Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="a4d89-142">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="a4d89-143">**IMsRdpDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="a4d89-143">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

