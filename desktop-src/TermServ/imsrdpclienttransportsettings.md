---
title: Interfaz IMsRdpClientTransportSettings
description: Administra la configuración de transporte de cliente para el servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto). | Interfaz IMsRdpClientTransportSettings
ms.assetid: d2573727-1dcc-4d4d-af5c-038e9467ba84
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings, descrito
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec240d008ef2f9469fb67f4041cfb33c08383079
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689725"
---
# <a name="imsrdpclienttransportsettings-interface"></a><span data-ttu-id="abc87-106">Interfaz IMsRdpClientTransportSettings</span><span class="sxs-lookup"><span data-stu-id="abc87-106">IMsRdpClientTransportSettings interface</span></span>

<span data-ttu-id="abc87-107">Administra la configuración de transporte de cliente para el servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="abc87-107">Manages client transport settings for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="members"></a><span data-ttu-id="abc87-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="abc87-108">Members</span></span>

<span data-ttu-id="abc87-109">La interfaz **IMsRdpClientTransportSettings** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="abc87-109">The **IMsRdpClientTransportSettings** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="abc87-110">**IMsRdpClientTransportSettings** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="abc87-110">**IMsRdpClientTransportSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="abc87-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="abc87-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="abc87-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="abc87-112">Properties</span></span>

<span data-ttu-id="abc87-113">La interfaz **IMsRdpClientTransportSettings** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="abc87-113">The **IMsRdpClientTransportSettings** interface has these properties.</span></span>



| <span data-ttu-id="abc87-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="abc87-114">Property</span></span>                                                                                                          | <span data-ttu-id="abc87-115">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="abc87-115">Access type</span></span>           | <span data-ttu-id="abc87-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="abc87-116">Description</span></span>                                                 |
|:------------------------------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------|
| [<span data-ttu-id="abc87-117">**GatewayCredsSource**</span><span class="sxs-lookup"><span data-stu-id="abc87-117">**GatewayCredsSource**</span></span>](imsrdpclienttransportsettings-gatewaycredssource.md)<br/>                         | <span data-ttu-id="abc87-118">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="abc87-118">Read/write</span></span><br/> | <span data-ttu-id="abc87-119">El método de autenticación del servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="abc87-119">The RD Gateway server authentication method.</span></span><br/>     |
| [<span data-ttu-id="abc87-120">**GatewayDefaultUsageMethod**</span><span class="sxs-lookup"><span data-stu-id="abc87-120">**GatewayDefaultUsageMethod**</span></span>](imsrdpclienttransportsettings-gatewaydefaultusagemethod.md)<br/>           | <span data-ttu-id="abc87-121">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="abc87-121">Read-only</span></span><br/>  | <span data-ttu-id="abc87-122">Método de uso predeterminado de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="abc87-122">The default RD Gateway usage method.</span></span><br/>             |
| [<span data-ttu-id="abc87-123">**GatewayHostname**</span><span class="sxs-lookup"><span data-stu-id="abc87-123">**GatewayHostname**</span></span>](imsrdpclienttransportsettings-gatewayhostname.md)<br/>                               | <span data-ttu-id="abc87-124">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="abc87-124">Read/write</span></span><br/> | <span data-ttu-id="abc87-125">Nombre de host del servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="abc87-125">Host name of the RD Gateway server.</span></span><br/>              |
| [<span data-ttu-id="abc87-126">**GatewayIsSupported**</span><span class="sxs-lookup"><span data-stu-id="abc87-126">**GatewayIsSupported**</span></span>](imsrdpclienttransportsettings-gatewayissupported.md)<br/>                         | <span data-ttu-id="abc87-127">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="abc87-127">Read-only</span></span><br/>  | <span data-ttu-id="abc87-128">Indica si se admite la puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="abc87-128">Indicates whether RD Gateway is supported.</span></span><br/>       |
| [<span data-ttu-id="abc87-129">**GatewayProfileUsageMethod**</span><span class="sxs-lookup"><span data-stu-id="abc87-129">**GatewayProfileUsageMethod**</span></span>](imsrdpclienttransportsettings-gatewayprofileusagemethod.md)<br/>           | <span data-ttu-id="abc87-130">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="abc87-130">Read/write</span></span><br/> | <span data-ttu-id="abc87-131">Método de uso del perfil de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="abc87-131">The RD Gateway profile usage method.</span></span><br/>             |
| [<span data-ttu-id="abc87-132">**GatewayUsageMethod**</span><span class="sxs-lookup"><span data-stu-id="abc87-132">**GatewayUsageMethod**</span></span>](imsrdpclienttransportsettings-gatewayusagemethod.md)<br/>                         | <span data-ttu-id="abc87-133">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="abc87-133">Read/write</span></span><br/> | <span data-ttu-id="abc87-134">El método de uso del servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="abc87-134">The RD Gateway server usage method.</span></span><br/>              |
| [<span data-ttu-id="abc87-135">**GatewayUserSelectedCredsSource**</span><span class="sxs-lookup"><span data-stu-id="abc87-135">**GatewayUserSelectedCredsSource**</span></span>](imsrdpclienttransportsettings-gatewayuserselectedcredssource.md)<br/> | <span data-ttu-id="abc87-136">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="abc87-136">Read/write</span></span><br/> | <span data-ttu-id="abc87-137">Origen de credenciales de puerta de enlace de escritorio remoto especificado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="abc87-137">The user-specified RD Gateway credential source.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="abc87-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abc87-138">Requirements</span></span>



| <span data-ttu-id="abc87-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="abc87-139">Requirement</span></span> | <span data-ttu-id="abc87-140">Value</span><span class="sxs-lookup"><span data-stu-id="abc87-140">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abc87-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="abc87-141">Minimum supported client</span></span><br/> | <span data-ttu-id="abc87-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abc87-142">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="abc87-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="abc87-143">Minimum supported server</span></span><br/> | <span data-ttu-id="abc87-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="abc87-144">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="abc87-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="abc87-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="abc87-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abc87-146"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="abc87-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="abc87-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abc87-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abc87-148"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="abc87-149">IID</span><span class="sxs-lookup"><span data-stu-id="abc87-149">IID</span></span><br/>                      | <span data-ttu-id="abc87-150">IID \_ IMsRdpClientTransportSettings se define como 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="abc87-150">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="abc87-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="abc87-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abc87-152">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="abc87-152">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="abc87-153">Referencia de Conexión web a Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="abc87-153">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="abc87-154">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="abc87-154">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

