---
title: Uso de Servicios de Escritorio remoto canales virtuales
description: Para implementar un canal virtual, se proporcionan los módulos de servidor y cliente de la aplicación de un canal virtual.
ms.assetid: 3b378071-ebd6-47b0-8a9c-3e671505011a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539eafca38c19855fdb057ceeb6e79cb4613773a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774287"
---
# <a name="using-remote-desktop-services-virtual-channels"></a><span data-ttu-id="f5286-103">Uso de Servicios de Escritorio remoto canales virtuales</span><span class="sxs-lookup"><span data-stu-id="f5286-103">Using Remote Desktop Services virtual channels</span></span>

<span data-ttu-id="f5286-104">Para implementar un canal virtual, se proporcionan los módulos de servidor y cliente de la aplicación de un canal virtual.</span><span class="sxs-lookup"><span data-stu-id="f5286-104">To implement a virtual channel, you provide the server and client modules of a virtual channel's application.</span></span> <span data-ttu-id="f5286-105">El módulo de servidor puede ser una aplicación de modo de usuario o un controlador en modo kernel.</span><span class="sxs-lookup"><span data-stu-id="f5286-105">The server module can be a user-mode application or a kernel-mode driver.</span></span> <span data-ttu-id="f5286-106">El módulo cliente debe ser un archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="f5286-106">The client module must be a DLL.</span></span>

<span data-ttu-id="f5286-107">Para obtener descripciones de estos módulos, vea los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="f5286-107">For descriptions of these modules, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f5286-108">En esta sección</span><span class="sxs-lookup"><span data-stu-id="f5286-108">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="f5286-109">Aplicación de servidor de canal virtual</span><span class="sxs-lookup"><span data-stu-id="f5286-109">Virtual Channel Server Application</span></span>](virtual-channel-server-application.md)
</dt> <dd>

<span data-ttu-id="f5286-110">El módulo de servidor de una aplicación que usa canales virtuales debe ser una aplicación de modo de usuario que se ejecute en una sesión de cliente en el servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="f5286-110">The server module of an application that uses virtual channels must be a user-mode application running in a client session on the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="f5286-111">Tenga en cuenta que debe proporcionar un método para iniciar la aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="f5286-111">Note that you must provide a method to start the server application.</span></span>

</dd> <dt>

[<span data-ttu-id="f5286-112">DLL de cliente de canal virtual</span><span class="sxs-lookup"><span data-stu-id="f5286-112">Virtual Channel Client DLL</span></span>](virtual-channel-client-dll.md)
</dt> <dd>

<span data-ttu-id="f5286-113">El cliente de una aplicación de canales virtuales es un archivo DLL que se carga durante la inicialización del Servicios de Escritorio remoto en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="f5286-113">The client of a virtual channels application is a DLL that is loaded during the Remote Desktop Services initialization on the client computer.</span></span> <span data-ttu-id="f5286-114">El archivo DLL debe estar registrado en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="f5286-114">The DLL must be registered on the client computer.</span></span>

</dd> <dt>

[<span data-ttu-id="f5286-115">Registro de cliente de canal virtual</span><span class="sxs-lookup"><span data-stu-id="f5286-115">Virtual Channel Client Registration</span></span>](virtual-channel-client-registration.md)
</dt> <dd>

<span data-ttu-id="f5286-116">Debe almacenar el nombre del archivo DLL de cliente en el registro.</span><span class="sxs-lookup"><span data-stu-id="f5286-116">You must store the name of the client DLL in the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="f5286-117">Canales virtuales persistentes de control remoto</span><span class="sxs-lookup"><span data-stu-id="f5286-117">Remote Control Persistent Virtual Channels</span></span>](remote-control-persistent-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="f5286-118">Un canal virtual persistente de control remoto no se cierra cuando un control remoto se conecta o se desconecta para la sesión conectada al cliente.</span><span class="sxs-lookup"><span data-stu-id="f5286-118">A remote control persistent virtual channel is not closed when a remote control connects or disconnects for the session connected to the client.</span></span> <span data-ttu-id="f5286-119">Los datos se seguirán transmitiendo y recibiendo a través de este canal.</span><span class="sxs-lookup"><span data-stu-id="f5286-119">Data will continue to be transmitted and received through this channel.</span></span>

</dd> <dt>

[<span data-ttu-id="f5286-120">Canales virtuales dinámicos</span><span class="sxs-lookup"><span data-stu-id="f5286-120">Dynamic Virtual Channels</span></span>](dynamic-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="f5286-121">Las API de canal virtual dinámico (DVC) amplían las API de canal virtual existentes para Servicios de Escritorio remoto, conocidas como API de canal virtual estático (SVC).</span><span class="sxs-lookup"><span data-stu-id="f5286-121">Dynamic virtual channel (DVC) APIs extend the existing virtual channel APIs for Remote Desktop Services, known as static virtual channel (SVC) APIs.</span></span>

</dd> </dl>

<span data-ttu-id="f5286-122">Si ha habilitado la aplicación de un canal virtual en la implementación de Servicios de Escritorio remoto, también puede hacer que la aplicación esté disponible para los equipos cliente que tienen acceso al servidor host de sesión de escritorio remoto por medio del control ActiveX Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="f5286-122">If you have enabled a virtual channel's application in your Remote Desktop Services deployment, you can also make the application available to client computers that access the RD Session Host server by means of the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="f5286-123">Para obtener más información, vea [usar el control ActiveX escritorio remoto con canales virtuales](using-the-remote-desktop-activex-control-with-virtual-channels.md).</span><span class="sxs-lookup"><span data-stu-id="f5286-123">For more information, see [Using the Remote Desktop ActiveX Control with Virtual Channels](using-the-remote-desktop-activex-control-with-virtual-channels.md).</span></span>

 

 




