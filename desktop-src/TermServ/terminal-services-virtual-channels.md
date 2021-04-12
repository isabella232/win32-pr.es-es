---
title: Servicios de Escritorio remoto canales virtuales
description: Los canales virtuales son extensiones de software que se pueden usar para agregar mejoras funcionales a una aplicación Servicios de Escritorio remoto.
ms.assetid: f7bdebec-ecc3-4f28-9327-f0d2f169c142
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce78331841a41502aa337de19e9879d42d85fe1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357028"
---
# <a name="remote-desktop-services-virtual-channels"></a><span data-ttu-id="af439-103">Servicios de Escritorio remoto canales virtuales</span><span class="sxs-lookup"><span data-stu-id="af439-103">Remote Desktop Services virtual channels</span></span>

<span data-ttu-id="af439-104">Los *canales virtuales* son extensiones de software que se pueden usar para agregar mejoras funcionales a una aplicación servicios de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="af439-104">*Virtual channels* are software extensions that can be used to add functional enhancements to a Remote Desktop Services application.</span></span> <span data-ttu-id="af439-105">Algunos ejemplos de mejoras funcionales pueden ser: compatibilidad con tipos especiales de hardware, audio u otras adiciones a la funcionalidad básica proporcionada por el [Protocolo de escritorio remoto](remote-desktop-protocol.md) de servicios de escritorio remoto (RDP).</span><span class="sxs-lookup"><span data-stu-id="af439-105">Examples of functional enhancements might include: support for special types of hardware, audio, or other additions to the core functionality provided by the Remote Desktop Services [Remote Desktop Protocol](remote-desktop-protocol.md) (RDP).</span></span> <span data-ttu-id="af439-106">El protocolo RDP proporciona administración multiplexada de varios canales virtuales.</span><span class="sxs-lookup"><span data-stu-id="af439-106">The RDP protocol provides multiplexed management of multiple virtual channels.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="af439-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="af439-107">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="af439-108">Uso de Servicios de Escritorio remoto canales virtuales</span><span class="sxs-lookup"><span data-stu-id="af439-108">Using Remote Desktop Services virtual channels</span></span>](using-terminal-services-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="af439-109">Para implementar un canal virtual, se proporcionan los módulos de servidor y cliente de la aplicación de un canal virtual.</span><span class="sxs-lookup"><span data-stu-id="af439-109">To implement a virtual channel, you provide the server and client modules of a virtual channel's application.</span></span>

</dd> <dt>

[<span data-ttu-id="af439-110">Referencia de canales virtuales dinámicos</span><span class="sxs-lookup"><span data-stu-id="af439-110">Dynamic virtual channels reference</span></span>](dynamic-virtual-channels-reference.md)
</dt> <dd>

<span data-ttu-id="af439-111">Servicios de Escritorio remoto admite las interfaces de cliente de canal virtual dinámico (DVC).</span><span class="sxs-lookup"><span data-stu-id="af439-111">Dynamic virtual channel (DVC) client interfaces are supported by Remote Desktop Services.</span></span>

</dd> <dt>

[<span data-ttu-id="af439-112">Referencia de canales virtuales de gráficos</span><span class="sxs-lookup"><span data-stu-id="af439-112">Graphics virtual channels reference</span></span>](graphics-virtual-channels-reference.md)
</dt> <dd>

<span data-ttu-id="af439-113">La referencia de canales virtuales de gráficos contiene elementos de programación que permiten crear un canal de gráficos virtual.</span><span class="sxs-lookup"><span data-stu-id="af439-113">The graphics virtual channels reference contains programming elements that enable you to create a virtual graphics channel.</span></span>

</dd> </dl>

<span data-ttu-id="af439-114">Una aplicación de canal virtual tiene dos partes: un módulo de cliente y un módulo de servidor.</span><span class="sxs-lookup"><span data-stu-id="af439-114">A virtual channel application has two parts, a client module and a server module.</span></span> <span data-ttu-id="af439-115">El módulo de servidor es un programa ejecutable que se ejecuta en el servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="af439-115">The server module is an executable program running on the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="af439-116">El módulo cliente es un archivo DLL que se debe cargar en la memoria del equipo cliente cuando se ejecuta el programa cliente de Conexión a Escritorio remoto (RDC).</span><span class="sxs-lookup"><span data-stu-id="af439-116">The client module is a DLL that must be loaded into memory on the client computer when the Remote Desktop Connection (RDC) client program runs.</span></span>

<span data-ttu-id="af439-117">Los canales virtuales pueden agregar mejoras funcionales a un cliente Conexión a Escritorio remoto (RDC), independientemente del protocolo RDP.</span><span class="sxs-lookup"><span data-stu-id="af439-117">Virtual channels can add functional enhancements to a Remote Desktop Connection (RDC) client, independent of the RDP protocol.</span></span> <span data-ttu-id="af439-118">Con la compatibilidad con canales virtuales, se pueden agregar nuevas características sin tener que actualizar el software de cliente o servidor, o el protocolo RDP.</span><span class="sxs-lookup"><span data-stu-id="af439-118">With virtual channel support, new features can be added without having to update the client or server software, or the RDP protocol.</span></span>

<span data-ttu-id="af439-119">Se han identificado cuatro clases principales de usuarios de canales virtuales:</span><span class="sxs-lookup"><span data-stu-id="af439-119">Four major classes of users of virtual channels have been identified:</span></span>

-   <span data-ttu-id="af439-120">Controladores generales de modo kernel, como controladores serie o de impresora.</span><span class="sxs-lookup"><span data-stu-id="af439-120">General kernel-mode drivers, such as serial or printer drivers.</span></span>
-   <span data-ttu-id="af439-121">Redirección del sistema de archivos (este es solo un caso especial de un controlador de modo kernel general).</span><span class="sxs-lookup"><span data-stu-id="af439-121">File system redirection (this is just a special case of a general kernel-mode driver).</span></span>
-   <span data-ttu-id="af439-122">Aplicaciones en modo de usuario, por ejemplo, de cortar y pegar de forma remota.</span><span class="sxs-lookup"><span data-stu-id="af439-122">User mode applications, for example remote cut-and-paste.</span></span>
-   <span data-ttu-id="af439-123">Dispositivos de audio.</span><span class="sxs-lookup"><span data-stu-id="af439-123">Audio devices.</span></span>

<span data-ttu-id="af439-124">Para obtener más información, consulte [uso de servicios de escritorio remoto canales virtuales](using-terminal-services-virtual-channels.md).</span><span class="sxs-lookup"><span data-stu-id="af439-124">For more information, see [Using Remote Desktop Services Virtual Channels](using-terminal-services-virtual-channels.md).</span></span>

<span data-ttu-id="af439-125">Si ha habilitado una aplicación de canales virtuales en la implementación de Servicios de Escritorio remoto, puede hacer que la aplicación esté disponible para los equipos cliente que tengan acceso al servidor host de sesión de escritorio remoto por medio de la Escritorio remoto control ActiveX de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="af439-125">If you have enabled a virtual channels application in your Remote Desktop Services deployment, you can make the application available to client computers that access the RD Session Host server by means of the Remote Desktop Microsoft ActiveX control.</span></span> <span data-ttu-id="af439-126">Para obtener más información, vea [canales virtuales que admiten scripts](scriptable-virtual-channels.md) y [usar el control ActiveX escritorio remoto con canales virtuales](using-the-remote-desktop-activex-control-with-virtual-channels.md).</span><span class="sxs-lookup"><span data-stu-id="af439-126">For more information, see [Scriptable Virtual Channels](scriptable-virtual-channels.md) and [Using the Remote Desktop ActiveX Control with Virtual Channels](using-the-remote-desktop-activex-control-with-virtual-channels.md).</span></span>

 

 




