---
title: Interfaz IMsRdpClientAdvancedSettings2
description: Administra la configuración de cliente avanzada. Deriva de la interfaz IMsRdpClientAdvancedSettings.
ms.assetid: 78cffdf5-bd99-4140-80b6-aa8632894487
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, descrito
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70d7f9ad9b93c0f3cd1d62fdbbaddf4faa55ad9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359773"
---
# <a name="imsrdpclientadvancedsettings2-interface"></a><span data-ttu-id="370f1-106">Interfaz IMsRdpClientAdvancedSettings2</span><span class="sxs-lookup"><span data-stu-id="370f1-106">IMsRdpClientAdvancedSettings2 interface</span></span>

<span data-ttu-id="370f1-107">Administra la configuración de cliente avanzada.</span><span class="sxs-lookup"><span data-stu-id="370f1-107">Manages advanced client settings.</span></span> <span data-ttu-id="370f1-108">Deriva de la interfaz [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="370f1-108">Derives from the [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) interface.</span></span> <span data-ttu-id="370f1-109">Esta interfaz incluye métodos para recuperar y establecer propiedades avanzadas (opcionales) para el control ActiveX Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="370f1-109">This interface includes methods to retrieve and set advanced (optional) properties for the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="370f1-110">Para obtener una instancia de esta interfaz, use la propiedad [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) para obtener un puntero de interfaz [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="370f1-110">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="370f1-111">A continuación, llame a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el puntero **IMsTscAdvancedSettings** y pase **IID \_ IMsRdpClientAdvancedSettings2** a **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="370f1-111">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings2** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="370f1-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="370f1-112">Members</span></span>

<span data-ttu-id="370f1-113">La interfaz **IMsRdpClientAdvancedSettings2** hereda de [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md).</span><span class="sxs-lookup"><span data-stu-id="370f1-113">The **IMsRdpClientAdvancedSettings2** interface inherits from [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md).</span></span> <span data-ttu-id="370f1-114">**IMsRdpClientAdvancedSettings2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="370f1-114">**IMsRdpClientAdvancedSettings2** also has these types of members:</span></span>

-   [<span data-ttu-id="370f1-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="370f1-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="370f1-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="370f1-116">Properties</span></span>

<span data-ttu-id="370f1-117">La interfaz **IMsRdpClientAdvancedSettings2** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="370f1-117">The **IMsRdpClientAdvancedSettings2** interface has these properties.</span></span>



| <span data-ttu-id="370f1-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="370f1-118">Property</span></span>                                                                                      | <span data-ttu-id="370f1-119">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="370f1-119">Access type</span></span>           | <span data-ttu-id="370f1-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="370f1-120">Description</span></span>                                                                                                                                           |
|:----------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="370f1-121">**CanAutoReconnect**</span><span class="sxs-lookup"><span data-stu-id="370f1-121">**CanAutoReconnect**</span></span>](imsrdpclientadvancedsettings2-canautoreconnect.md)<br/>         | <span data-ttu-id="370f1-122">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="370f1-122">Read-only</span></span><br/>  | <span data-ttu-id="370f1-123">Especifica si el control de cliente puede volver a conectarse automáticamente a la sesión actual en caso de desconexión de red.</span><span class="sxs-lookup"><span data-stu-id="370f1-123">Specifies whether the client control is able to reconnect automatically to the current session in the event of a network disconnection.</span></span><br/>    |
| [<span data-ttu-id="370f1-124">**EnableAutoReconnect**</span><span class="sxs-lookup"><span data-stu-id="370f1-124">**EnableAutoReconnect**</span></span>](imsrdpclientadvancedsettings2-enableautoreconnect.md)<br/>   | <span data-ttu-id="370f1-125">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="370f1-125">Read/write</span></span><br/> | <span data-ttu-id="370f1-126">Especifica si se habilita el control de cliente para que se vuelva a conectar automáticamente a una sesión en caso de desconexión de la red.</span><span class="sxs-lookup"><span data-stu-id="370f1-126">Specifies whether to enable the client control to reconnect automatically to a session in the event of a network disconnection.</span></span><br/>            |
| [<span data-ttu-id="370f1-127">**MaxReconnectAttempts**</span><span class="sxs-lookup"><span data-stu-id="370f1-127">**MaxReconnectAttempts**</span></span>](imsrdpclientadvancedsettings2-maxreconnectattempts.md)<br/> | <span data-ttu-id="370f1-128">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="370f1-128">Read/write</span></span><br/> | <span data-ttu-id="370f1-129">Especifica el número de veces que se intentará volver a conectar durante la reconexión automática.</span><span class="sxs-lookup"><span data-stu-id="370f1-129">Specifies the number of times to try to reconnect during automatic reconnection.</span></span> <span data-ttu-id="370f1-130">Los valores válidos de esta propiedad son de 0 a 200, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="370f1-130">The valid values of this property are 0 to 200 inclusive.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="370f1-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="370f1-131">Remarks</span></span>

<span data-ttu-id="370f1-132">Esta interfaz se ha extendido mediante las siguientes interfaces, con cada nueva interfaz que hereda todos los métodos y propiedades de las interfaces anteriores:</span><span class="sxs-lookup"><span data-stu-id="370f1-132">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="370f1-133">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="370f1-133">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
-   [<span data-ttu-id="370f1-134">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="370f1-134">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
-   [<span data-ttu-id="370f1-135">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="370f1-135">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
-   [<span data-ttu-id="370f1-136">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="370f1-136">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="370f1-137">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="370f1-137">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)

<span data-ttu-id="370f1-138">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="370f1-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="370f1-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="370f1-139">Requirements</span></span>



| <span data-ttu-id="370f1-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="370f1-140">Requirement</span></span> | <span data-ttu-id="370f1-141">Value</span><span class="sxs-lookup"><span data-stu-id="370f1-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="370f1-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="370f1-142">Minimum supported client</span></span><br/> | <span data-ttu-id="370f1-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="370f1-143">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="370f1-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="370f1-144">Minimum supported server</span></span><br/> | <span data-ttu-id="370f1-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="370f1-145">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="370f1-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="370f1-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="370f1-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="370f1-147"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="370f1-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="370f1-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="370f1-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="370f1-149"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="370f1-150">IID</span><span class="sxs-lookup"><span data-stu-id="370f1-150">IID</span></span><br/>                      | <span data-ttu-id="370f1-151">IID \_ IMsRdpClientAdvancedSettings2 se define como 9ac42117-2b76-4320-aa44-0e616ab8437b</span><span class="sxs-lookup"><span data-stu-id="370f1-151">IID\_IMsRdpClientAdvancedSettings2 is defined as 9ac42117-2b76-4320-aa44-0e616ab8437b</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="370f1-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="370f1-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="370f1-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="370f1-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="370f1-154">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="370f1-154">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="370f1-155">Referencia de Conexión web a Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="370f1-155">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

