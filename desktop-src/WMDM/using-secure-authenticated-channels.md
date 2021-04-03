---
title: Usar canales autenticados seguros
description: Usar canales autenticados seguros
ms.assetid: ca4ab93c-0a3e-4fb5-be7f-a8f4eea3c9b7
keywords:
- Windows Media Administrador de dispositivos, autenticación
- Administrador de dispositivos, autenticación
- aplicaciones de escritorio, autenticación
- proveedores de servicios, autenticación
- Guía de programación, autenticación
- autenticación
- Windows Media Administrador de dispositivos, comunicación segura
- Administrador de dispositivos, protección de la comunicación
- aplicaciones de escritorio, comunicación segura
- proveedores de servicios, comunicación segura
- Guía de programación, comunicación segura
- comunicación segura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f88c271cecc2e9252a3f7af0540beef3dc57d2b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075351"
---
# <a name="using-secure-authenticated-channels"></a><span data-ttu-id="8d980-115">Usar canales autenticados seguros</span><span class="sxs-lookup"><span data-stu-id="8d980-115">Using Secure Authenticated Channels</span></span>

<span data-ttu-id="8d980-116">Windows Media Administrador de dispositivos habilita la autenticación y la comunicación segura entre los componentes proporcionando dos clases auxiliares, [CSecureChannelClient](csecurechannelclient-class.md) (para aplicaciones) y [CSecureChannelServer](csecurechannelserver-class.md) (para proveedores de servicios), y una interfaz, [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) (para ambos).</span><span class="sxs-lookup"><span data-stu-id="8d980-116">Windows Media Device Manager enables authentication and secure communication between components by providing two helper classes, [CSecureChannelClient](csecurechannelclient-class.md) (for applications) and [CSecureChannelServer](csecurechannelserver-class.md) (for service providers), and one interface, [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) (for both).</span></span> <span data-ttu-id="8d980-117">Juntas, componen una API para el uso de canales autenticados seguros (SAC).</span><span class="sxs-lookup"><span data-stu-id="8d980-117">Together these make up an API for the use of secure authenticated channels (SAC).</span></span> <span data-ttu-id="8d980-118">SAC controla las tres tareas siguientes para proveedores de servicios o aplicaciones que usan Windows Media Administrador de dispositivos:</span><span class="sxs-lookup"><span data-stu-id="8d980-118">SAC handles the following three tasks for service providers or applications using Windows Media Device Manager:</span></span>

-   [<span data-ttu-id="8d980-119">Autenticación de componentes</span><span class="sxs-lookup"><span data-stu-id="8d980-119">Component Authentication</span></span>](component-authentication.md)
-   [<span data-ttu-id="8d980-120">Cifrado y descifrado</span><span class="sxs-lookup"><span data-stu-id="8d980-120">Encryption and Decryption</span></span>](encryption-and-decryption.md)
-   [<span data-ttu-id="8d980-121">Autenticación de mensajes</span><span class="sxs-lookup"><span data-stu-id="8d980-121">Message Authentication</span></span>](message-authentication.md)

<span data-ttu-id="8d980-122">Una aplicación o proveedor de servicios debe administrar la autenticación de componentes, el cifrado y el descifrado. la autenticación de mensajes es opcional.</span><span class="sxs-lookup"><span data-stu-id="8d980-122">An application or service provider must handle component authentication, encryption, and decryption; message authentication is optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d980-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8d980-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d980-124">**Tareas comunes a las aplicaciones y proveedores de servicios**</span><span class="sxs-lookup"><span data-stu-id="8d980-124">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




