---
title: Acerca de Servicios de Escritorio remoto
description: Servicios de Escritorio remoto (antes conocido como Terminal Services) proporciona una funcionalidad similar a un entorno de host, centralizado, o de gran sistema (mainframe) en el que varios terminales se conectan a un equipo host.
ms.assetid: 5b5b0f97-f973-4f52-a965-c9c2390e6c8d
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto Servicios de Escritorio remoto, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4644170cfca3b4bacdd6db647e35549d56844e9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685612"
---
# <a name="about-remote-desktop-services"></a><span data-ttu-id="55071-104">Acerca de Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="55071-104">About Remote Desktop Services</span></span>

<span data-ttu-id="55071-105">Servicios de Escritorio remoto (antes conocido como Terminal Services) proporciona una funcionalidad similar a un entorno de host, centralizado, o de gran sistema (mainframe) en el que varios terminales se conectan a un equipo host.</span><span class="sxs-lookup"><span data-stu-id="55071-105">Remote Desktop Services (formerly known as Terminal Services) provides functionality similar to a terminal-based, centralized host, or mainframe, environment in which multiple terminals connect to a host computer.</span></span> <span data-ttu-id="55071-106">Cada terminal proporciona un conducto para la entrada y la salida entre un usuario y el equipo host.</span><span class="sxs-lookup"><span data-stu-id="55071-106">Each terminal provides a conduit for input and output between a user and the host computer.</span></span> <span data-ttu-id="55071-107">Un usuario puede iniciar sesión en un terminal y, a continuación, ejecutar aplicaciones en el equipo host, tener acceso a archivos, bases de datos, recursos de red, etc.</span><span class="sxs-lookup"><span data-stu-id="55071-107">A user can log on at a terminal, and then run applications on the host computer, accessing files, databases, network resources, and so on.</span></span> <span data-ttu-id="55071-108">Cada sesión de terminal es independiente, con el sistema operativo host que administra los conflictos entre varios usuarios que compiten por recursos compartidos.</span><span class="sxs-lookup"><span data-stu-id="55071-108">Each terminal session is independent, with the host operating system managing conflicts between multiple users contending for shared resources.</span></span>

<span data-ttu-id="55071-109">La principal diferencia entre Servicios de Escritorio remoto y el entorno de mainframe tradicional es que los terminales no de un entorno de gran sistema solo proporcionan entradas y salidas basadas en caracteres.</span><span class="sxs-lookup"><span data-stu-id="55071-109">The primary difference between Remote Desktop Services and the traditional mainframe environment is that the dumb terminals in a mainframe environment only provide character-based input and output.</span></span> <span data-ttu-id="55071-110">Un emulador o cliente Conexión a Escritorio remoto (RDC) proporciona una interfaz gráfica de usuario completa que incluye un escritorio del sistema operativo Windows y compatibilidad con una variedad de dispositivos de entrada, como un teclado y un mouse.</span><span class="sxs-lookup"><span data-stu-id="55071-110">A Remote Desktop Connection (RDC) client or emulator provides a complete graphical user interface including a Windows operating system desktop and support for a variety of input devices, such as a keyboard and mouse.</span></span>

<span data-ttu-id="55071-111">En el entorno de Servicios de Escritorio remoto, una aplicación se ejecuta completamente en el servidor de host de sesión Escritorio remoto (host de sesión de escritorio remoto) (anteriormente conocido como servidor de Terminal Server).</span><span class="sxs-lookup"><span data-stu-id="55071-111">In the Remote Desktop Services environment, an application runs entirely on the Remote Desktop Session Host (RD Session Host) server (formerly known as a terminal server).</span></span> <span data-ttu-id="55071-112">El cliente RDC no realiza ningún procesamiento local del software de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="55071-112">The RDC client performs no local processing of application software.</span></span> <span data-ttu-id="55071-113">El servidor transmite la interfaz gráfica de usuario al cliente.</span><span class="sxs-lookup"><span data-stu-id="55071-113">The server transmits the graphical user interface to the client.</span></span> <span data-ttu-id="55071-114">El cliente vuelve a transmitir la entrada del usuario al servidor.</span><span class="sxs-lookup"><span data-stu-id="55071-114">The client transmits the user's input back to the server.</span></span>

<span data-ttu-id="55071-115">Para obtener más información, vea los siguientes temas.</span><span class="sxs-lookup"><span data-stu-id="55071-115">For more information, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="55071-116">En esta sección</span><span class="sxs-lookup"><span data-stu-id="55071-116">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="55071-117">Modificar el valor predeterminado de redirección del dispositivo</span><span class="sxs-lookup"><span data-stu-id="55071-117">Modify Device Redirection Default</span></span>](modify-device-redirection-default-.md)
</dt> <dd>

<span data-ttu-id="55071-118">Dado que Escritorio remoto servidores de puerta de enlace intentan exigir directivas de redirección de dispositivos seguras antes de pasar la conexión de cliente a un servidor host de sesión Escritorio remoto, puede que tenga que deshabilitar este valor predeterminado en algunos casos.</span><span class="sxs-lookup"><span data-stu-id="55071-118">Because Remote Desktop Gateway servers attempt to enforce secure device redirection policies before passing the client connection through to a Remote Desktop Session Host server, you may need to disable this default in some cases.</span></span>

</dd> <dt>

[<span data-ttu-id="55071-119">Protocolo de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="55071-119">Remote Desktop Protocol</span></span>](remote-desktop-protocol.md)
</dt> <dd>

<span data-ttu-id="55071-120">El protocolo de Escritorio remoto de Microsoft (RDP) proporciona funciones de entrada y visualización remotas a través de conexiones de red para aplicaciones basadas en Windows que se ejecutan en un servidor.</span><span class="sxs-lookup"><span data-stu-id="55071-120">The Microsoft Remote Desktop Protocol (RDP) provides remote display and input capabilities over network connections for Windows-based applications running on a server.</span></span>

</dd> <dt>

[<span data-ttu-id="55071-121">API de Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="55071-121">Remote Desktop Services API</span></span>](terminal-services-api.md)
</dt> <dd>

<span data-ttu-id="55071-122">La API de Servicios de Escritorio remoto es especialmente útil para las aplicaciones cliente/servidor y para la administración de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="55071-122">The Remote Desktop Services API is primarily useful to client/server applications and applications for Remote Desktop Services administration.</span></span>

</dd> <dt>

[<span data-ttu-id="55071-123">Aplicaciones de administración de Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="55071-123">Remote Desktop Services management applications</span></span>](terminal-services-management-applications.md)
</dt> <dd>

<span data-ttu-id="55071-124">Describe las aplicaciones de administración que Servicios de Escritorio remoto admite.</span><span class="sxs-lookup"><span data-stu-id="55071-124">Describes the management applications that Remote Desktop Services supports.</span></span>

</dd> <dt>

[<span data-ttu-id="55071-125">Instrucciones de programación de Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="55071-125">Remote Desktop Services programming guidelines</span></span>](terminal-services-programming-guidelines.md)
</dt> <dd>

<span data-ttu-id="55071-126">Temas que proporcionan instrucciones para desarrollar aplicaciones en un entorno de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="55071-126">Topics that provide guidelines for developing applications in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="55071-127">Sesiones de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="55071-127">Remote Desktop Sessions</span></span>](terminal-services-sessions.md)
</dt> <dd>

<span data-ttu-id="55071-128">Dado que cada inicio de sesión en un cliente de Conexión a Escritorio remoto (RDC) recibe un identificador de sesión independiente, la experiencia del usuario es similar a iniciar sesión en varios equipos al mismo tiempo. por ejemplo, un equipo de Office y un equipo doméstico.</span><span class="sxs-lookup"><span data-stu-id="55071-128">Because each logon to a Remote Desktop Connection (RDC) client receives a separate session ID, the user-experience is similar to being logged on to multiple computers at the same time; for example, an office computer and a home computer.</span></span>

</dd> <dt>

[<span data-ttu-id="55071-129">Conexión web a Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="55071-129">Remote Desktop Web Connection</span></span>](remote-desktop-web-connection.md)
</dt> <dd>

<span data-ttu-id="55071-130">Describe cómo instalar un Conexión web a Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="55071-130">Describes how to install a Remote Desktop Web Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="55071-131">Recursos en un servidor host de sesión Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="55071-131">Resources on a Remote Desktop Session Host Server</span></span>](resources-on-a-terminal-server.md)
</dt> <dd>

<span data-ttu-id="55071-132">Varios usuarios pueden iniciar sesión simultáneamente en un solo servidor host de sesión de escritorio remoto, compartiendo los recursos de hardware y software del servidor.</span><span class="sxs-lookup"><span data-stu-id="55071-132">Multiple users can log on simultaneously to a single RD Session Host server, sharing the hardware and software resources of the server.</span></span>

</dd> <dt>

[<span data-ttu-id="55071-133">Novedades de Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="55071-133">What's New in Remote Desktop Services</span></span>](what-s-new-in-terminal-services.md)
</dt> <dd>

<span data-ttu-id="55071-134">Temas que describen los cambios en cada versión de la API de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="55071-134">Topics that describe the changes in each release of the Remote Desktop Services API.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="55071-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="55071-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55071-136">Conectarse a otro equipo mediante la Conexión a Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="55071-136">Connect to another computer using Remote Desktop Connection</span></span>](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7)
</dt> </dl>

 

 




