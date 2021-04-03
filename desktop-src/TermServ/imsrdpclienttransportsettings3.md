---
title: Interfaz IMsRdpClientTransportSettings3
description: Define propiedades adicionales para el servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto). | Interfaz IMsRdpClientTransportSettings3
ms.assetid: c0bdfe23-9a26-4feb-b9b7-e52f04f23aa1
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings3, descrito
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7498db4b39a4ad0e89761cbec439895e4e9a152
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914373"
---
# <a name="imsrdpclienttransportsettings3-interface"></a><span data-ttu-id="f9b36-106">Interfaz IMsRdpClientTransportSettings3</span><span class="sxs-lookup"><span data-stu-id="f9b36-106">IMsRdpClientTransportSettings3 interface</span></span>

<span data-ttu-id="f9b36-107">Define propiedades adicionales para el servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="f9b36-107">Defines additional properties for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="members"></a><span data-ttu-id="f9b36-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f9b36-108">Members</span></span>

<span data-ttu-id="f9b36-109">La interfaz **IMsRdpClientTransportSettings3** hereda de [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md).</span><span class="sxs-lookup"><span data-stu-id="f9b36-109">The **IMsRdpClientTransportSettings3** interface inherits from [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md).</span></span> <span data-ttu-id="f9b36-110">**IMsRdpClientTransportSettings3** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f9b36-110">**IMsRdpClientTransportSettings3** also has these types of members:</span></span>

-   [<span data-ttu-id="f9b36-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f9b36-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f9b36-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f9b36-112">Properties</span></span>

<span data-ttu-id="f9b36-113">La interfaz **IMsRdpClientTransportSettings3** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f9b36-113">The **IMsRdpClientTransportSettings3** interface has these properties.</span></span>



| <span data-ttu-id="f9b36-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f9b36-114">Property</span></span>                                                                                                           | <span data-ttu-id="f9b36-115">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="f9b36-115">Access type</span></span>           | <span data-ttu-id="f9b36-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9b36-116">Description</span></span>                                                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f9b36-117">**GatewayAuthCookieServerAddr**</span><span class="sxs-lookup"><span data-stu-id="f9b36-117">**GatewayAuthCookieServerAddr**</span></span>](imsrdpclienttransportsettings3-gatewayauthcookieserveraddr.md)<br/>       | <span data-ttu-id="f9b36-118">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f9b36-118">Read/write</span></span><br/> | <span data-ttu-id="f9b36-119">Dirección del servidor para la autenticación basada en cookies.</span><span class="sxs-lookup"><span data-stu-id="f9b36-119">The server address for cookie-based authentication.</span></span><br/>                                                                                       |
| [<span data-ttu-id="f9b36-120">**GatewayAuthLoginPage**</span><span class="sxs-lookup"><span data-stu-id="f9b36-120">**GatewayAuthLoginPage**</span></span>](imsrdpclienttransportsettings3-gatewayauthloginpage.md)<br/>                     | <span data-ttu-id="f9b36-121">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f9b36-121">Read/write</span></span><br/> | <span data-ttu-id="f9b36-122">Dirección de la Página Web de inicio de sesión que se va a usar para autenticar a un usuario.</span><span class="sxs-lookup"><span data-stu-id="f9b36-122">The address of the login webpage to use to authenticate a user.</span></span><br/>                                                                           |
| [<span data-ttu-id="f9b36-123">**GatewayCredSourceCookie**</span><span class="sxs-lookup"><span data-stu-id="f9b36-123">**GatewayCredSourceCookie**</span></span>](imsrdpclienttransportsettings3-gatewaycredsourcecookie.md)<br/>               | <span data-ttu-id="f9b36-124">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f9b36-124">Read/write</span></span><br/> | <span data-ttu-id="f9b36-125">Especifica si el origen de credenciales está basado en cookies.</span><span class="sxs-lookup"><span data-stu-id="f9b36-125">Specifies if the credential source is cookie based.</span></span><br/>                                                                                       |
| [<span data-ttu-id="f9b36-126">**GatewayEncryptedAuthCookie**</span><span class="sxs-lookup"><span data-stu-id="f9b36-126">**GatewayEncryptedAuthCookie**</span></span>](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md)<br/>         | <span data-ttu-id="f9b36-127">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f9b36-127">Read/write</span></span><br/> | <span data-ttu-id="f9b36-128">Cookie de autenticación cifrada.</span><span class="sxs-lookup"><span data-stu-id="f9b36-128">The encrypted authentication cookie.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="f9b36-129">**GatewayEncryptedAuthCookieSize**</span><span class="sxs-lookup"><span data-stu-id="f9b36-129">**GatewayEncryptedAuthCookieSize**</span></span>](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md)<br/> | <span data-ttu-id="f9b36-130">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f9b36-130">Read/write</span></span><br/> | <span data-ttu-id="f9b36-131">Tamaño, en caracteres, de la propiedad [**GatewayEncryptedAuthCookie**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md) .</span><span class="sxs-lookup"><span data-stu-id="f9b36-131">The size, in characters, of the [**GatewayEncryptedAuthCookie**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md) property.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f9b36-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9b36-132">Requirements</span></span>



| <span data-ttu-id="f9b36-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9b36-133">Requirement</span></span> | <span data-ttu-id="f9b36-134">Value</span><span class="sxs-lookup"><span data-stu-id="f9b36-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9b36-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9b36-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f9b36-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f9b36-136">Windows 7</span></span><br/>                                                                              |
| <span data-ttu-id="f9b36-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9b36-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f9b36-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9b36-138">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="f9b36-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f9b36-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="f9b36-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9b36-140"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="f9b36-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f9b36-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9b36-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9b36-142"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="f9b36-143">IID</span><span class="sxs-lookup"><span data-stu-id="f9b36-143">IID</span></span><br/>                      | <span data-ttu-id="f9b36-144">IID \_ IMsRdpClientTransportSettings3 se define como 3D5B21AC-748D-41DE-8F30-E15169586BD4</span><span class="sxs-lookup"><span data-stu-id="f9b36-144">IID\_IMsRdpClientTransportSettings3 is defined as 3D5B21AC-748D-41DE-8F30-E15169586BD4</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9b36-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9b36-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9b36-146">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="f9b36-146">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





