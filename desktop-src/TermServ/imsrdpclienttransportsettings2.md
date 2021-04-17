---
title: Interfaz IMsRdpClientTransportSettings2
description: Administra la configuración de transporte de cliente para el servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto). | Interfaz IMsRdpClientTransportSettings2
ms.assetid: 4f9f1905-2693-4666-9f6f-6e00b1eb6a0f
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings2, descrito
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f2f4887c6a4f55f3b9c97c389e9afd702d2ffab
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689738"
---
# <a name="imsrdpclienttransportsettings2-interface"></a><span data-ttu-id="a1d1e-106">Interfaz IMsRdpClientTransportSettings2</span><span class="sxs-lookup"><span data-stu-id="a1d1e-106">IMsRdpClientTransportSettings2 interface</span></span>

<span data-ttu-id="a1d1e-107">Administra la configuración de transporte de cliente para el servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="a1d1e-107">Manages client transport settings for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="members"></a><span data-ttu-id="a1d1e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a1d1e-108">Members</span></span>

<span data-ttu-id="a1d1e-109">La interfaz **IMsRdpClientTransportSettings2** hereda de [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md).</span><span class="sxs-lookup"><span data-stu-id="a1d1e-109">The **IMsRdpClientTransportSettings2** interface inherits from [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md).</span></span> <span data-ttu-id="a1d1e-110">**IMsRdpClientTransportSettings2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a1d1e-110">**IMsRdpClientTransportSettings2** also has these types of members:</span></span>

-   [<span data-ttu-id="a1d1e-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a1d1e-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a1d1e-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a1d1e-112">Properties</span></span>

<span data-ttu-id="a1d1e-113">La interfaz **IMsRdpClientTransportSettings2** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a1d1e-113">The **IMsRdpClientTransportSettings2** interface has these properties.</span></span>



| <span data-ttu-id="a1d1e-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a1d1e-114">Property</span></span>                                                                                                    | <span data-ttu-id="a1d1e-115">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="a1d1e-115">Access type</span></span>           | <span data-ttu-id="a1d1e-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1d1e-116">Description</span></span>                                                                                       |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a1d1e-117">**GatewayCredSharing**</span><span class="sxs-lookup"><span data-stu-id="a1d1e-117">**GatewayCredSharing**</span></span>](imsrdpclienttransportsettings2-gatewaycredsharing.md)<br/>                  | <span data-ttu-id="a1d1e-118">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a1d1e-118">Read/write</span></span><br/> | <span data-ttu-id="a1d1e-119">Indica si la característica de inicio de sesión único para la puerta de enlace de escritorio remoto está habilitada.</span><span class="sxs-lookup"><span data-stu-id="a1d1e-119">Indicates whether the single sign-on feature for RD Gateway is enabled.</span></span><br/>                |
| [<span data-ttu-id="a1d1e-120">**GatewayDomain**</span><span class="sxs-lookup"><span data-stu-id="a1d1e-120">**GatewayDomain**</span></span>](imsrdpclienttransportsettings2-gatewaydomain.md)<br/>                            | <span data-ttu-id="a1d1e-121">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a1d1e-121">Read/write</span></span><br/> | <span data-ttu-id="a1d1e-122">El nombre de dominio que proporciona un usuario para conectarse al servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="a1d1e-122">The domain name that a user provides to connect to the RD Gateway server.</span></span><br/>              |
| [<span data-ttu-id="a1d1e-123">**GatewayEncryptedOtpCookie**</span><span class="sxs-lookup"><span data-stu-id="a1d1e-123">**GatewayEncryptedOtpCookie**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>     | <span data-ttu-id="a1d1e-124">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a1d1e-124">Read/write</span></span><br/> | <span data-ttu-id="a1d1e-125">Cookie de OTP cifrada.</span><span class="sxs-lookup"><span data-stu-id="a1d1e-125">The encrypted OTP cookie.</span></span><br/>                                                              |
| [<span data-ttu-id="a1d1e-126">**GatewayEncryptedOtpCookieSize**</span><span class="sxs-lookup"><span data-stu-id="a1d1e-126">**GatewayEncryptedOtpCookieSize**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/> | <span data-ttu-id="a1d1e-127">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a1d1e-127">Read/write</span></span><br/> | <span data-ttu-id="a1d1e-128">Tamaño, en bytes, de la cookie de OTP cifrada.</span><span class="sxs-lookup"><span data-stu-id="a1d1e-128">The size, in bytes, of the encrypted OTP cookie.</span></span><br/>                                       |
| [<span data-ttu-id="a1d1e-129">**GatewayPassword**</span><span class="sxs-lookup"><span data-stu-id="a1d1e-129">**GatewayPassword**</span></span>](imsrdpclienttransportsettings2-gatewaypassword.md)<br/>                        | <span data-ttu-id="a1d1e-130">Solo escritura</span><span class="sxs-lookup"><span data-stu-id="a1d1e-130">Write-only</span></span><br/> | <span data-ttu-id="a1d1e-131">La contraseña que un usuario proporciona para conectarse al servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="a1d1e-131">The password that a user provides to connect to the RD Gateway server.</span></span><br/>                 |
| [<span data-ttu-id="a1d1e-132">**GatewayPreAuthRequirement**</span><span class="sxs-lookup"><span data-stu-id="a1d1e-132">**GatewayPreAuthRequirement**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthrequirement.md)<br/>    | <span data-ttu-id="a1d1e-133">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a1d1e-133">Read/write</span></span><br/> | <span data-ttu-id="a1d1e-134">Indica si la característica de contraseña de un solo tiempo (OTP) de puerta de enlace de escritorio remoto está habilitada.</span><span class="sxs-lookup"><span data-stu-id="a1d1e-134">Indicates whether the RD Gateway one-time password (OTP) feature is enabled.</span></span><br/>           |
| [<span data-ttu-id="a1d1e-135">**GatewayPreAuthServerAddr**</span><span class="sxs-lookup"><span data-stu-id="a1d1e-135">**GatewayPreAuthServerAddr**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>      | <span data-ttu-id="a1d1e-136">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a1d1e-136">Read/write</span></span><br/> | <span data-ttu-id="a1d1e-137">Dirección web del servidor de autenticación previa.</span><span class="sxs-lookup"><span data-stu-id="a1d1e-137">The web address of the pre-authentication server.</span></span><br/>                                      |
| [<span data-ttu-id="a1d1e-138">**GatewaySupportUrl**</span><span class="sxs-lookup"><span data-stu-id="a1d1e-138">**GatewaySupportUrl**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>             | <span data-ttu-id="a1d1e-139">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a1d1e-139">Read/write</span></span><br/> | <span data-ttu-id="a1d1e-140">Dirección web del sitio que proporciona soporte técnico para el servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="a1d1e-140">The web address of the site that provides technical support for the RD Gateway server.</span></span><br/> |
| [<span data-ttu-id="a1d1e-141">**GatewayUsername**</span><span class="sxs-lookup"><span data-stu-id="a1d1e-141">**GatewayUsername**</span></span>](imsrdpclienttransportsettings2-gatewayusername.md)<br/>                        | <span data-ttu-id="a1d1e-142">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a1d1e-142">Read/write</span></span><br/> | <span data-ttu-id="a1d1e-143">El nombre de usuario que proporciona un usuario para conectarse al servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="a1d1e-143">The user name that a user provides to connect to the RD Gateway server.</span></span><br/>                |



 

## <a name="requirements"></a><span data-ttu-id="a1d1e-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1d1e-144">Requirements</span></span>



| <span data-ttu-id="a1d1e-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1d1e-145">Requirement</span></span> | <span data-ttu-id="a1d1e-146">Value</span><span class="sxs-lookup"><span data-stu-id="a1d1e-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1d1e-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1d1e-147">Minimum supported client</span></span><br/> | <span data-ttu-id="a1d1e-148">Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="a1d1e-148">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="a1d1e-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1d1e-149">Minimum supported server</span></span><br/> | <span data-ttu-id="a1d1e-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1d1e-150">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="a1d1e-151">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a1d1e-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="a1d1e-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1d1e-152"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="a1d1e-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a1d1e-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1d1e-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1d1e-154"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="a1d1e-155">IID</span><span class="sxs-lookup"><span data-stu-id="a1d1e-155">IID</span></span><br/>                      | <span data-ttu-id="a1d1e-156">IID \_ IMsRdpClientTransportSettings2 se define como 67341688-D606-4c73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="a1d1e-156">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a1d1e-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1d1e-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1d1e-158">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="a1d1e-158">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





