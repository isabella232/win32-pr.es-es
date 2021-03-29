---
title: Novedades de Windows Server 2008 R2
description: Windows Server 2008 R2 incorpora los siguientes elementos de programación nuevos para Servicios de Escritorio remoto.
ms.assetid: 605a9a34-11fa-433a-9ccd-8368c75b10f0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fec9c29a142d8c97a17d4a73ee1015f84702851
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "103994902"
---
# <a name="whats-new-in-windows-server-2008-r2"></a><span data-ttu-id="63ae1-103">Novedades de Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="63ae1-103">What's New in Windows Server 2008 R2</span></span>

<span data-ttu-id="63ae1-104">Windows Server 2008 R2 incorpora los siguientes elementos de programación nuevos para Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="63ae1-104">Windows Server 2008 R2 introduces the following new programming elements for Remote Desktop Services.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="63ae1-105">Terminal Services es ahora Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="63ae1-105">Terminal Services Is Now Remote Desktop Services</span></span><br/></td>
<td><span data-ttu-id="63ae1-106">Se ha cambiado el nombre de Terminal Services Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="63ae1-106">Terminal Services has been renamed Remote Desktop Services.</span></span> <span data-ttu-id="63ae1-107">Un servidor que tiene instalado el servicio de rol host Escritorio remoto de sesión de escritorio remoto (host de sesión de RD) se denomina ahora servidor host de sesión de escritorio remoto, en lugar de un servidor de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="63ae1-107">A server that has the Remote Desktop Session Host (RD Session Host) role service installed is now called an RD Session Host server, instead of a terminal server.</span></span><br/>
<ul>
<li><span data-ttu-id="63ae1-108"><a href="terminal-services-is-now-remote-desktop-services.md">Terminal Services es ahora Servicios de Escritorio remoto</a></span><span class="sxs-lookup"><span data-stu-id="63ae1-108"><a href="terminal-services-is-now-remote-desktop-services.md">Terminal Services Is Now Remote Desktop Services</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ae1-109">API de virtualización de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="63ae1-109">Remote Desktop Virtualization API</span></span><br/></td>
<td><span data-ttu-id="63ae1-110">La API de virtualización Escritorio remoto proporciona enumeraciones, interfaces y estructuras que puede usar para crear complementos personalizados que invalidan la lógica de redirección estándar del agente de Conexión a Escritorio remoto (agente de conexión a escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="63ae1-110">The Remote Desktop Virtualization API provides enumerations, interfaces, and structures that you can use to create custom plug-ins that override the standard redirection logic of Remote Desktop Connection Broker (RD Connection Broker).</span></span> <span data-ttu-id="63ae1-111">El agente de conexión a escritorio remoto (anteriormente conocido como agente de sesiones de TS) se amplió para admitir conexiones a máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="63ae1-111">RD Connection Broker (formerly known as TS Session Broker) was expanded to support connections to virtual machines.</span></span><br/>
<ul>
<li><span data-ttu-id="63ae1-112"><a href="using-the-remote-desktop-virtualization-api.md">Uso de la API de virtualización de Escritorio remoto</a></span><span class="sxs-lookup"><span data-stu-id="63ae1-112"><a href="using-the-remote-desktop-virtualization-api.md">Using the Remote Desktop Virtualization API</a></span></span></li>
<li><span data-ttu-id="63ae1-113"><a href="terminal-services-virtualization-api-reference.md">Referencia de API de virtualización de Escritorio remoto</a></span><span class="sxs-lookup"><span data-stu-id="63ae1-113"><a href="terminal-services-virtualization-api-reference.md">Remote Desktop Virtualization API Reference</a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ae1-114">Proveedor de Protocolo de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="63ae1-114">Remote Desktop Protocol Provider</span></span><br/></td>
<td><span data-ttu-id="63ae1-115">La API del proveedor de Protocolo de escritorio remoto se puede usar para crear un protocolo que personalice la interacción entre el servicio Servicios de Escritorio remoto y los clientes de escritorio.</span><span class="sxs-lookup"><span data-stu-id="63ae1-115">The Remote Desktop Protocol Provider API can be used to create a protocol that customizes the interaction between the Remote Desktop Services service and desktop clients.</span></span><br/>
<ul>
<li><span data-ttu-id="63ae1-116"><a href="creating-a-custom-remote-protocol.md">Creación de un proveedor de Protocolo de escritorio remoto</a></span><span class="sxs-lookup"><span data-stu-id="63ae1-116"><a href="creating-a-custom-remote-protocol.md">Creating a Remote Desktop Protocol Provider</a></span></span></li>
<li><span data-ttu-id="63ae1-117"><a href="custom-remote-protocol-reference.md">Referencia del proveedor de Protocolo de escritorio remoto</a></span><span class="sxs-lookup"><span data-stu-id="63ae1-117"><a href="custom-remote-protocol-reference.md">Remote Desktop Protocol Provider Reference</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ae1-118">Servicios de Escritorio remoto API de AudioEndpoint</span><span class="sxs-lookup"><span data-stu-id="63ae1-118">Remote Desktop Services AudioEndpoint API</span></span><br/></td>
<td><span data-ttu-id="63ae1-119">La API de Servicios de Escritorio remoto AudioEndpoint admite enumeraciones, interfaces y estructuras para el transporte de datos y el registro de puntos de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="63ae1-119">The Remote Desktop Services AudioEndpoint API supports enumeration, interfaces, and structures for audio endpoint registration and data transport.</span></span><br/>
<ul>
<li><span data-ttu-id="63ae1-120"><a href="terminal-services-audioendpoint-api-reference.md">Referencia de la API de Servicios de Escritorio remoto AudioEndpoint</a></span><span class="sxs-lookup"><span data-stu-id="63ae1-120"><a href="terminal-services-audioendpoint-api-reference.md">Remote Desktop Services AudioEndpoint API Reference</a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ae1-121">API de servicio Administración de conexiones de RemoteApp y Escritorio</span><span class="sxs-lookup"><span data-stu-id="63ae1-121">RemoteApp and Desktop Connection Management Service API</span></span><br/></td>
<td><span data-ttu-id="63ae1-122">La API del servicio Administración de conexiones de RemoteApp y Escritorio admite interfaces y estructuras que puede usar para realizar un filtrado personalizado de recursos y proporcionar compatibilidad con tipos de archivo que no se admiten de forma nativa en Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="63ae1-122">The RemoteApp and Desktop Connection Management Service API supports interfaces and structures that you can use to perform custom filtering of resources and provide support for file types that are not natively supported in Windows Server 2008 R2.</span></span><br/>
<ul>
<li><span data-ttu-id="63ae1-123"><a href="centralized-publishing-api-reference.md">Referencia de la API de servicio Administración de conexiones de RemoteApp y Escritorio</a></span><span class="sxs-lookup"><span data-stu-id="63ae1-123"><a href="centralized-publishing-api-reference.md">RemoteApp and Desktop Connection Management Service API Reference</a></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 





