---
title: Servicios de Escritorio remoto (Servicios de Escritorio remoto)
description: Escritorio remoto de Microsoft Services es un software de acceso de equipo remoto que admite el acceso al escritorio remoto. Servicios de Escritorio remoto conecta varios clientes a un servidor host de sesión Escritorio remoto (host de sesión de escritorio remoto).
ms.assetid: 90c40b7a-e324-43fc-a1e6-f29997ed9436
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Servicios de Escritorio remoto, Página principal
- Terminal Services vea Servicios de Escritorio remoto Servicios de Escritorio remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f39e176473c98f1e240d58592463df749a95f939
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105685838"
---
# <a name="remote-desktop-services-remote-desktop-services"></a><span data-ttu-id="d0ee0-107">Servicios de Escritorio remoto (Servicios de Escritorio remoto)</span><span class="sxs-lookup"><span data-stu-id="d0ee0-107">Remote Desktop Services (Remote Desktop Services)</span></span>

## <a name="purpose"></a><span data-ttu-id="d0ee0-108">Propósito</span><span class="sxs-lookup"><span data-stu-id="d0ee0-108">Purpose</span></span>

<span data-ttu-id="d0ee0-109">Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 o Windows Server 2008 con Servicios de Escritorio remoto (anteriormente conocido como Terminal Services) permiten a un servidor hospedar varias sesiones de cliente simultáneas.</span><span class="sxs-lookup"><span data-stu-id="d0ee0-109">Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 with Remote Desktop Services (formerly known as Terminal Services) allow a server to host multiple, simultaneous client sessions.</span></span> <span data-ttu-id="d0ee0-110">Escritorio remoto usa Servicios de Escritorio remoto tecnología para permitir que una sola sesión se ejecute de forma remota.</span><span class="sxs-lookup"><span data-stu-id="d0ee0-110">Remote Desktop uses Remote Desktop Services technology to allow a single session to run remotely.</span></span> <span data-ttu-id="d0ee0-111">Un usuario puede conectarse a Escritorio remoto un servidor host de sesión de escritorio remoto (host de sesión de RD) (conocido anteriormente como Terminal Server) mediante el software cliente de Conexión a Escritorio remoto (RDC).</span><span class="sxs-lookup"><span data-stu-id="d0ee0-111">A user can connect to a Remote Desktop Session Host (RD Session Host) server (formerly known as a terminal server) by using Remote Desktop Connection (RDC) client software.</span></span> <span data-ttu-id="d0ee0-112">La Conexión web a Escritorio remoto extiende Servicios de Escritorio remoto tecnología a la Web.</span><span class="sxs-lookup"><span data-stu-id="d0ee0-112">The Remote Desktop Web Connection extends Remote Desktop Services technology to the web.</span></span>

> [!Note]  
> <span data-ttu-id="d0ee0-113">Este tema está destinado a los desarrolladores de software.</span><span class="sxs-lookup"><span data-stu-id="d0ee0-113">This topic is for software developers.</span></span> <span data-ttu-id="d0ee0-114">Si busca información de usuario para conexiones Escritorio remoto, consulte [conexión a escritorio remoto: preguntas más](https://windows.microsoft.com/windows/remote-desktop-connection-faq#1TC=windows-8)frecuentes.</span><span class="sxs-lookup"><span data-stu-id="d0ee0-114">If you are looking for user information for Remote Desktop connections, See [Remote Desktop Connection: frequently asked questions](https://windows.microsoft.com/windows/remote-desktop-connection-faq#1TC=windows-8).</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="d0ee0-115">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="d0ee0-115">Where applicable</span></span>

<span data-ttu-id="d0ee0-116">Un cliente Conexión a Escritorio remoto (RDC) puede existir en una variedad de formas.</span><span class="sxs-lookup"><span data-stu-id="d0ee0-116">A Remote Desktop Connection (RDC) client can exist in a variety of forms.</span></span> <span data-ttu-id="d0ee0-117">Los dispositivos de hardware de cliente ligero que ejecutan un sistema operativo basado en Windows incrustado pueden ejecutar el software cliente de RDC para conectarse a un servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d0ee0-117">Thin-client hardware devices that run an embedded Windows-based operating system can run the RDC client software to connect to an RD Session Host server.</span></span> <span data-ttu-id="d0ee0-118">Los equipos basados en Windows, Macintosh o UNIX pueden ejecutar el software cliente de RDC para conectarse a un servidor host de sesión de escritorio remoto con el fin de mostrar aplicaciones basadas en Windows.</span><span class="sxs-lookup"><span data-stu-id="d0ee0-118">Windows-, Macintosh-, or UNIX-based computers can run RDC client software to connect to an RD Session Host server to display Windows-based applications.</span></span> <span data-ttu-id="d0ee0-119">Esta combinación de clientes de RDC proporciona acceso a las aplicaciones basadas en Windows desde prácticamente cualquier sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d0ee0-119">This combination of RDC clients provides access to Windows-based applications from virtually any operating system.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="d0ee0-120">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="d0ee0-120">Developer audience</span></span>

<span data-ttu-id="d0ee0-121">Los desarrolladores que usan Servicios de Escritorio remoto deben estar familiarizados con los lenguajes de programación C y C++ y el entorno de programación basado en Windows.</span><span class="sxs-lookup"><span data-stu-id="d0ee0-121">Developers who use Remote Desktop Services should be familiar with the C and C++ programming languages and the Windows-based programming environment.</span></span> <span data-ttu-id="d0ee0-122">Es necesario estar familiarizado con la arquitectura cliente/servidor.</span><span class="sxs-lookup"><span data-stu-id="d0ee0-122">Familiarity with client/server architecture is required.</span></span> <span data-ttu-id="d0ee0-123">El Conexión web a Escritorio remoto incluye interfaces que admiten scripts para crear e implementar canales virtuales con scripts en Servicios de Escritorio remoto aplicaciones Web.</span><span class="sxs-lookup"><span data-stu-id="d0ee0-123">The Remote Desktop Web Connection includes scriptable interfaces to create and deploy scriptable virtual channels within Remote Desktop Services web applications.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="d0ee0-124">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="d0ee0-124">Run-time requirements</span></span>

<span data-ttu-id="d0ee0-125">Las aplicaciones que usan Servicios de Escritorio remoto requieren Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d0ee0-125">Applications that use Remote Desktop Services require Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008, or Windows Vista.</span></span> <span data-ttu-id="d0ee0-126">Para usar la funcionalidad de Conexión web a Escritorio remoto, la aplicación cliente de Servicios de Escritorio remoto requiere Internet Explorer y una conexión a la World Wide Web.</span><span class="sxs-lookup"><span data-stu-id="d0ee0-126">To use Remote Desktop Web Connection functionality, the Remote Desktop Services client application requires Internet Explorer and a connection to the World Wide Web.</span></span> <span data-ttu-id="d0ee0-127">Para obtener información sobre los requisitos de tiempo de ejecución para un elemento de programación determinado, vea la sección de requisitos de la página de referencia de ese elemento.</span><span class="sxs-lookup"><span data-stu-id="d0ee0-127">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d0ee0-128">En esta sección</span><span class="sxs-lookup"><span data-stu-id="d0ee0-128">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="d0ee0-129">Escritorio remoto control ActiveX</span><span class="sxs-lookup"><span data-stu-id="d0ee0-129">Remote Desktop ActiveX control</span></span>](remote-desktop-activex-control.md)
</dt> <dd>

<span data-ttu-id="d0ee0-130">Describe cómo utilizar el control ActiveX Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d0ee0-130">Describes how to use the Remote Desktop ActiveX control.</span></span>

</dd> <dt>

[<span data-ttu-id="d0ee0-131">API del proveedor de Protocolo de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="d0ee0-131">Remote Desktop Protocol Provider API</span></span>](custom-remote-desktop-protocols.md)
</dt> <dd>

<span data-ttu-id="d0ee0-132">La API de proveedor de Protocolo de escritorio remoto se usa para crear un protocolo que proporcione comunicación entre el servicio Servicios de Escritorio remoto y varios clientes.</span><span class="sxs-lookup"><span data-stu-id="d0ee0-132">You use the Remote Desktop Protocol Provider API to create a protocol to provide communication between the Remote Desktop Services service and multiple clients.</span></span>

</dd> <dt>

[<span data-ttu-id="d0ee0-133">Servicios de Escritorio remoto canales virtuales</span><span class="sxs-lookup"><span data-stu-id="d0ee0-133">Remote Desktop Services virtual channels</span></span>](terminal-services-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="d0ee0-134">Los *canales virtuales* son extensiones de software que se pueden usar para agregar mejoras funcionales a una aplicación servicios de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d0ee0-134">*Virtual channels* are software extensions that can be used to add functional enhancements to a Remote Desktop Services application.</span></span>

</dd> <dt>

[<span data-ttu-id="d0ee0-135">API de redirección de medios RemoteFX</span><span class="sxs-lookup"><span data-stu-id="d0ee0-135">RemoteFX Media Redirection API</span></span>](remotefx-api.md)
</dt> <dd>

<span data-ttu-id="d0ee0-136">La API de redirección de medios RemoteFX se usa en una sesión de Escritorio remoto para identificar las áreas del servidor que muestran contenido de cambio rápido, como el vídeo.</span><span class="sxs-lookup"><span data-stu-id="d0ee0-136">The RemoteFX Media Redirection API is used in a Remote Desktop session to identify areas of the server that are displaying fast changing content, such as video.</span></span> <span data-ttu-id="d0ee0-137">Este contenido se puede codificar en vídeo y enviarse al cliente en formato codificado.</span><span class="sxs-lookup"><span data-stu-id="d0ee0-137">This content can then be video encoded and sent to the client in encoded format.</span></span>

</dd> <dt>

[<span data-ttu-id="d0ee0-138">API de cliente de Conexión a Escritorio remoto Broker</span><span class="sxs-lookup"><span data-stu-id="d0ee0-138">Remote Desktop Connection Broker client API</span></span>](connection-broker-client-api.md)
</dt> <dd>

<span data-ttu-id="d0ee0-139">Describe cómo usar la API de cliente de Conexión a Escritorio remoto Broker.</span><span class="sxs-lookup"><span data-stu-id="d0ee0-139">Describes how to use the Remote Desktop Connection Broker client API.</span></span>

</dd> <dt>

[<span data-ttu-id="d0ee0-140">Referencia de API del agente de tareas de escritorio personal</span><span class="sxs-lookup"><span data-stu-id="d0ee0-140">Personal desktop task agent API reference</span></span>](task-agent-api-reference.md)
</dt> <dd>

<span data-ttu-id="d0ee0-141">Personal Desktop Task Agent API se utiliza para controlar las actualizaciones programadas en un escritorio virtual personal.</span><span class="sxs-lookup"><span data-stu-id="d0ee0-141">The personal desktop task agent API is used to handle scheduled updates to a personal virtual desktop.</span></span>

</dd> <dt>

[<span data-ttu-id="d0ee0-142">Acerca de Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="d0ee0-142">About Remote Desktop Services</span></span>](about-terminal-services.md)
</dt> <dd>

<span data-ttu-id="d0ee0-143">Servicios de Escritorio remoto (antes conocido como Terminal Services) proporciona una funcionalidad similar a un entorno de host, centralizado, o de gran sistema (mainframe) en el que varios terminales se conectan a un equipo host.</span><span class="sxs-lookup"><span data-stu-id="d0ee0-143">Remote Desktop Services (formerly known as Terminal Services) provides functionality similar to a terminal-based, centralized host, or mainframe, environment in which multiple terminals connect to a host computer.</span></span>

</dd> <dt>

[<span data-ttu-id="d0ee0-144">Proveedor de servicios de administración de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="d0ee0-144">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> <dd>

<span data-ttu-id="d0ee0-145">El proveedor de servicios de administración de Escritorio remoto (RDMS) administra los entornos de infraestructura de escritorio virtual (VDI).</span><span class="sxs-lookup"><span data-stu-id="d0ee0-145">The Remote Desktop Management Services (RDMS) Provider manages virtual desktop infrastructure (VDI) environments.</span></span>

</dd> <dt>

[<span data-ttu-id="d0ee0-146">Referencia de Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="d0ee0-146">Remote Desktop Services reference</span></span>](terminal-services-reference.md)
</dt> <dd>

<span data-ttu-id="d0ee0-147">Documentación de los métodos de propiedad que puede usar para examinar y configurar Servicios de Escritorio remoto propiedades de usuario.</span><span class="sxs-lookup"><span data-stu-id="d0ee0-147">Documentation of property methods that you can use to examine and configure Remote Desktop Services user properties.</span></span> <span data-ttu-id="d0ee0-148">También se documentan las funciones, estructuras y Conexión web a Escritorio remoto las interfaces que admiten scripts. Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="d0ee0-148">Remote Desktop Services functions, structures, and Remote Desktop Web Connection scriptable interfaces are also documented.</span></span>

</dd> <dt>

[<span data-ttu-id="d0ee0-149">Teclas de método abreviado Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="d0ee0-149">Remote Desktop Services Shortcut Keys</span></span>](terminal-services-shortcut-keys.md)
</dt> <dd>

<span data-ttu-id="d0ee0-150">Una lista de las teclas de método abreviado Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d0ee0-150">A list of the Remote Desktop Services shortcut keys.</span></span>

</dd> <dt>

[<span data-ttu-id="d0ee0-151">Servicios de Escritorio remoto proveedor WMI</span><span class="sxs-lookup"><span data-stu-id="d0ee0-151">Remote Desktop Services WMI provider</span></span>](terminal-services-wmi-provider.md)
</dt> <dd>

<span data-ttu-id="d0ee0-152">El proveedor WMI de Servicios de Escritorio remoto proporciona acceso mediante programación a la información y la configuración que se exponen en el complemento configuración/conexiones de Microsoft Management Console (MMC) de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d0ee0-152">The Remote Desktop Services WMI provider provides programmatic access to the information and settings that are exposed by the Remote Desktop Services Configuration/Connections Microsoft Management Console (MMC) snap-in.</span></span>

</dd> <dt>

[<span data-ttu-id="d0ee0-153">Usar Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="d0ee0-153">Using Remote Desktop Services</span></span>](using-terminal-services.md)
</dt> <dd>

<span data-ttu-id="d0ee0-154">Cómo programar en el entorno de Servicios de Escritorio remoto y cómo extender la tecnología de Servicios de Escritorio remoto (antes conocida como Terminal Services) a la web mediante el uso de Conexión web a Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d0ee0-154">How to program in the Remote Desktop Services environment and how to extend Remote Desktop Services (formerly known as Terminal Services) technology to the web by using Remote Desktop Web Connection.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="d0ee0-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d0ee0-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0ee0-156">Terminal Services es ahora Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="d0ee0-156">Terminal Services Is Now Remote Desktop Services</span></span>](terminal-services-is-now-remote-desktop-services.md)
</dt> </dl>

 

 




