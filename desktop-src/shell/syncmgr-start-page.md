---
description: El administrador de sincronización proporciona una tecnología centralizada y estándar para sincronizar archivos para su uso sin conexión en un equipo móvil o en un equipo conectado a una red de área local.
title: administrador de sincronización
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 6cdac7e5-8985-407a-98bb-936bb20ed069
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbOrient
ms.openlocfilehash: 2fc56b2afec4fdedf98fe213437a27f2592ce72b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997760"
---
# <a name="synchronization-manager"></a><span data-ttu-id="43858-103">administrador de sincronización</span><span class="sxs-lookup"><span data-stu-id="43858-103">Synchronization Manager</span></span>

## <a name="purpose"></a><span data-ttu-id="43858-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="43858-104">Purpose</span></span>

<span data-ttu-id="43858-105">El administrador de sincronización proporciona una tecnología centralizada y estándar para sincronizar archivos para su uso sin conexión en un equipo móvil o en un equipo conectado a una red de área local.</span><span class="sxs-lookup"><span data-stu-id="43858-105">The Synchronization Manager provides a centralized, standard technology for synchronizing files for offline use on a mobile computer or a computer connected to a local area network.</span></span> <span data-ttu-id="43858-106">Junto con las funciones de conectividad, las notificaciones (servicio de notificación de eventos del sistema) y el almacenamiento en caché del lado cliente, el administrador de sincronización proporciona una infraestructura para admitir la informática móvil.</span><span class="sxs-lookup"><span data-stu-id="43858-106">Together with the connectivity functions, notifications (System Event Notification Service), and client side caching, the Synchronization Manager provides an infrastructure to support mobile computing.</span></span> <span data-ttu-id="43858-107">En lugar de cada aplicación que implementa su propia tecnología para almacenar en caché y sincronizar los recursos de red para uso local, el sistema operativo proporciona un modelo integrado que todas las aplicaciones pueden usar.</span><span class="sxs-lookup"><span data-stu-id="43858-107">Instead of each application implementing its own technology to cache and synchronize network resources for local use, the operating system provides an integrated model that all applications can use.</span></span> <span data-ttu-id="43858-108">Los archivos se sincronizan independientemente del protocolo.</span><span class="sxs-lookup"><span data-stu-id="43858-108">Files are synchronized independent of the protocol.</span></span> <span data-ttu-id="43858-109">Por ejemplo, un programa de correo electrónico puede transferir sus mensajes mediante SMTP, NMTP o POP3, mientras que un explorador puede utilizar HTTP y una base de datos puede usar la llamada a procedimiento remoto (RPC).</span><span class="sxs-lookup"><span data-stu-id="43858-109">For example, an email program can transfer its messages using SMTP, NMTP, or POP3, while a browser can use HTTP, and a database can use remote procedure call (RPC) (RPC).</span></span> <span data-ttu-id="43858-110">Los desarrolladores pueden usar la interfaz común para el administrador de sincronización en sus aplicaciones para sincronizar archivos entre el equipo local del usuario y el almacenamiento de red.</span><span class="sxs-lookup"><span data-stu-id="43858-110">Developers can use the common interface to the Synchronization Manager in their applications to synchronize files between the user's local computer and network storage.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="43858-111">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="43858-111">Where applicable</span></span>

<span data-ttu-id="43858-112">El administrador de sincronización está diseñado para aplicaciones que se ejecutan principalmente en equipos móviles.</span><span class="sxs-lookup"><span data-stu-id="43858-112">The Synchronization Manager is intended for applications that run primarily on mobile computers.</span></span> <span data-ttu-id="43858-113">Las aplicaciones que se ejecutan en equipos conectados a redes de área local de latencia alta también pueden beneficiarse del uso del administrador de sincronización.</span><span class="sxs-lookup"><span data-stu-id="43858-113">Applications that run on computers connected to high latency local area networks may also benefit from using the Synchronization Manager.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="43858-114">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="43858-114">Developer audience</span></span>

<span data-ttu-id="43858-115">Este documento está destinado a los desarrolladores de software que desarrollan aplicaciones para la informática móvil y redes de área local de latencia alta.</span><span class="sxs-lookup"><span data-stu-id="43858-115">This document is intended for software developers who develop applications for mobile computing and high latency local area networks.</span></span> <span data-ttu-id="43858-116">En este documento se proporciona una referencia completa de todas las partes del administrador de sincronización, incluidos los métodos e interfaces para el administrador de sincronización.</span><span class="sxs-lookup"><span data-stu-id="43858-116">This document provides a complete reference of all parts of the Synchronization Manager including the methods and interfaces to the Synchronization Manager.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="43858-117">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="43858-117">Run-time requirements</span></span>

<span data-ttu-id="43858-118">Requiere Windows Server 2003, Windows XP, Windows 2000 o Windows Millennium Edition (Windows me).</span><span class="sxs-lookup"><span data-stu-id="43858-118">Requires Windows Server 2003, Windows XP, Windows 2000, or Windows Millennium Edition (Windows Me).</span></span> <span data-ttu-id="43858-119">También está disponible como paquete redistribuible para Microsoft Windows NT 4,0, Windows 98 y Windows 95.</span><span class="sxs-lookup"><span data-stu-id="43858-119">Also available as a redistributable for Microsoft Windows NT 4.0, Windows 98, and Windows 95.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="43858-120">En esta sección</span><span class="sxs-lookup"><span data-stu-id="43858-120">In this section</span></span>



| <span data-ttu-id="43858-121">Tema</span><span class="sxs-lookup"><span data-stu-id="43858-121">Topic</span></span>                                                                                       | <span data-ttu-id="43858-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="43858-122">Description</span></span>                                                                                                                                         |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43858-123">Acerca del administrador de sincronización</span><span class="sxs-lookup"><span data-stu-id="43858-123">About Synchronization Manager</span></span>](syncmgr-about.md)<br/>                               | <span data-ttu-id="43858-124">El administrador de sincronización proporciona una tecnología centralizada y estándar para sincronizar archivos para su uso sin conexión en un equipo local.</span><span class="sxs-lookup"><span data-stu-id="43858-124">The Synchronization Manager provides a centralized, standard technology for synchronizing files for offline use on a local computer.</span></span><br/>     |
| [<span data-ttu-id="43858-125">Configuraciones de informática móvil</span><span class="sxs-lookup"><span data-stu-id="43858-125">Mobile Computing Configurations</span></span>](syncmgr-mobile-computing-configs.md)<br/>          | <span data-ttu-id="43858-126">Las aplicaciones pueden usar sincronización Manager para mantener los archivos y los recursos almacenados en caché localmente y sincronizados en equipos de escritorio y móviles.</span><span class="sxs-lookup"><span data-stu-id="43858-126">Applications can use Sychronization Manager to keep files and resources cached locally and synchronized on mobile and desktop computers.</span></span><br/> |
| [<span data-ttu-id="43858-127">Escenarios de aplicación</span><span class="sxs-lookup"><span data-stu-id="43858-127">Application Scenarios</span></span>](syncmgr-app-scenarios.md)<br/>                               | <span data-ttu-id="43858-128">Aplicaciones y servicios que pueden usar el administrador de sincronización.</span><span class="sxs-lookup"><span data-stu-id="43858-128">Applications and services that can use Synchronization Manager.</span></span><br/>                                                                          |
| [<span data-ttu-id="43858-129">Arquitectura del administrador de sincronización</span><span class="sxs-lookup"><span data-stu-id="43858-129">Synchronization Manager Architecture</span></span>](syncmgr-architecture.md)<br/>                 |                                                                                                                                                     |
| [<span data-ttu-id="43858-130">Usar el administrador de sincronización desde un programa</span><span class="sxs-lookup"><span data-stu-id="43858-130">Using Synchronization Manager from a Program</span></span>](syncmgr-using-from-a-program.md)<br/> |                                                                                                                                                     |
| [<span data-ttu-id="43858-131">Referencia del administrador de sincronización</span><span class="sxs-lookup"><span data-stu-id="43858-131">Synchronization Manager Reference</span></span>](syncmgr-reference.md)<br/>                       | <span data-ttu-id="43858-132">Los siguientes elementos de programación componen la API para el administrador de sincronización.</span><span class="sxs-lookup"><span data-stu-id="43858-132">The following programming elements make up the API for Synchronization Manager.</span></span><br/>                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="43858-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="43858-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43858-134">Acerca del servicio de notificación de eventos del sistema</span><span class="sxs-lookup"><span data-stu-id="43858-134">About System Event Notification Service</span></span>](../sens/about-system-event-notification-service.md)
</dt> </dl>

 

 
