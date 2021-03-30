---
title: Interfaz IMsRdpClientAdvancedSettings3
description: Administra la configuración de cliente avanzada. Deriva de la interfaz IMsRdpClientAdvancedSettings2.
ms.assetid: bfa9cf74-5943-45ca-9259-3ef0cc9ab2ab
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, descrito
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 760ae7d40742a800556b3d62bc5a1609b89c986b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802161"
---
# <a name="imsrdpclientadvancedsettings3-interface"></a><span data-ttu-id="d125c-106">Interfaz IMsRdpClientAdvancedSettings3</span><span class="sxs-lookup"><span data-stu-id="d125c-106">IMsRdpClientAdvancedSettings3 interface</span></span>

<span data-ttu-id="d125c-107">Administra la configuración de cliente avanzada.</span><span class="sxs-lookup"><span data-stu-id="d125c-107">Manages advanced client settings.</span></span> <span data-ttu-id="d125c-108">Deriva de la interfaz [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) .</span><span class="sxs-lookup"><span data-stu-id="d125c-108">Derives from the [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) interface.</span></span> <span data-ttu-id="d125c-109">Esta interfaz incluye métodos para recuperar y establecer propiedades avanzadas (opcionales) para el control ActiveX Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d125c-109">This interface includes methods to retrieve and set advanced (optional) properties for the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="d125c-110">Para obtener una instancia de esta interfaz, use la propiedad [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) para obtener un puntero de interfaz [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="d125c-110">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="d125c-111">A continuación, llame a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el puntero **IMsTscAdvancedSettings** y pase **IID \_ IMsRdpClientAdvancedSettings3** a **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="d125c-111">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings3** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="d125c-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="d125c-112">Members</span></span>

<span data-ttu-id="d125c-113">La interfaz **IMsRdpClientAdvancedSettings3** hereda de [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md).</span><span class="sxs-lookup"><span data-stu-id="d125c-113">The **IMsRdpClientAdvancedSettings3** interface inherits from [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md).</span></span> <span data-ttu-id="d125c-114">**IMsRdpClientAdvancedSettings3** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d125c-114">**IMsRdpClientAdvancedSettings3** also has these types of members:</span></span>

-   [<span data-ttu-id="d125c-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d125c-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d125c-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d125c-116">Properties</span></span>

<span data-ttu-id="d125c-117">La interfaz **IMsRdpClientAdvancedSettings3** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d125c-117">The **IMsRdpClientAdvancedSettings3** interface has these properties.</span></span>



| <span data-ttu-id="d125c-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d125c-118">Property</span></span>                                                                                                            | <span data-ttu-id="d125c-119">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="d125c-119">Access type</span></span>           | <span data-ttu-id="d125c-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="d125c-120">Description</span></span>                                                                            |
|:--------------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="d125c-121">**ConnectionBarShowMinimizeButton**</span><span class="sxs-lookup"><span data-stu-id="d125c-121">**ConnectionBarShowMinimizeButton**</span></span>](imsrdpclientadvancedsettings3-connectionbarshowminimizebutton.md)<br/> | <span data-ttu-id="d125c-122">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d125c-122">Read/write</span></span><br/> | <span data-ttu-id="d125c-123">Especifica si se va a mostrar el botón **minimizar** en la barra de conexión.</span><span class="sxs-lookup"><span data-stu-id="d125c-123">Specifies whether to display the **Minimize** button on the connection bar.</span></span><br/> |
| [<span data-ttu-id="d125c-124">**ConnectionBarShowRestoreButton**</span><span class="sxs-lookup"><span data-stu-id="d125c-124">**ConnectionBarShowRestoreButton**</span></span>](imsrdpclientadvancedsettings3-connectionbarshowrestorebutton.md)<br/>   | <span data-ttu-id="d125c-125">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d125c-125">Read/write</span></span><br/> | <span data-ttu-id="d125c-126">Especifica si se va a mostrar el botón **restaurar** en la barra de conexión.</span><span class="sxs-lookup"><span data-stu-id="d125c-126">Specifies whether to display the **Restore** button on the connection bar.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="d125c-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d125c-127">Remarks</span></span>

<span data-ttu-id="d125c-128">Esta interfaz se ha extendido mediante las siguientes interfaces, con cada nueva interfaz que hereda todos los métodos y propiedades de las interfaces anteriores:</span><span class="sxs-lookup"><span data-stu-id="d125c-128">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="d125c-129">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="d125c-129">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
-   [<span data-ttu-id="d125c-130">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="d125c-130">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
-   [<span data-ttu-id="d125c-131">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="d125c-131">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="d125c-132">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="d125c-132">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
-   [<span data-ttu-id="d125c-133">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="d125c-133">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)

<span data-ttu-id="d125c-134">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d125c-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d125c-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d125c-135">Requirements</span></span>



| <span data-ttu-id="d125c-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="d125c-136">Requirement</span></span> | <span data-ttu-id="d125c-137">Value</span><span class="sxs-lookup"><span data-stu-id="d125c-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d125c-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d125c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d125c-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d125c-139">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="d125c-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d125c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d125c-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d125c-141">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="d125c-142">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d125c-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="d125c-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d125c-143"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="d125c-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d125c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d125c-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d125c-145"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="d125c-146">IID</span><span class="sxs-lookup"><span data-stu-id="d125c-146">IID</span></span><br/>                      | <span data-ttu-id="d125c-147">IID \_ IMsRdpClientAdvancedSettings3 se define como 19cd856b-c542-4c53-ACEE-f127e3be1a59</span><span class="sxs-lookup"><span data-stu-id="d125c-147">IID\_IMsRdpClientAdvancedSettings3 is defined as 19cd856b-c542-4c53-acee-f127e3be1a59</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d125c-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="d125c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d125c-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="d125c-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="d125c-150">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="d125c-150">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="d125c-151">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="d125c-151">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="d125c-152">Referencia de Conexión web a Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="d125c-152">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

