---
title: API de Servicios de Escritorio remoto
description: La API de Servicios de Escritorio remoto es especialmente útil para las aplicaciones cliente/servidor y para la administración de Servicios de Escritorio remoto.
ms.assetid: 4bd10a15-78d6-4754-9e17-f2576ee8b9d0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5aa187378625242463ea91151a6961b08d2a77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903352"
---
# <a name="remote-desktop-services-api"></a><span data-ttu-id="fff00-103">API de Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="fff00-103">Remote Desktop Services API</span></span>

<span data-ttu-id="fff00-104">La mayoría de las aplicaciones se ejecutan sin modificaciones en un entorno Servicios de Escritorio remoto (antes conocido como Terminal Services) y no necesitan usar la API de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="fff00-104">Most applications run without modification in a Remote Desktop Services (formerly known as Terminal Services) environment and do not need to use the Remote Desktop Services API.</span></span> <span data-ttu-id="fff00-105">La API de Servicios de Escritorio remoto es especialmente útil para las aplicaciones cliente/servidor y para la administración de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="fff00-105">The Remote Desktop Services API is primarily useful to client/server applications and applications for Remote Desktop Services administration.</span></span>

<span data-ttu-id="fff00-106">La API de Servicios de Escritorio remoto es un conjunto de llamadas de función en Wtsapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="fff00-106">The Remote Desktop Services API is a set of function calls into Wtsapi32.dll.</span></span> <span data-ttu-id="fff00-107">Para diseñar la aplicación de forma que se ejecute en entornos Servicios de Escritorio remoto y no Servicios de Escritorio remoto, utilice la vinculación dinámica en tiempo de ejecución para comprobar la presencia de Wtsapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="fff00-107">To design your application to run in both Remote Desktop Services and non-Remote Desktop Services environments, use run-time dynamic linking to check for the presence of Wtsapi32.dll.</span></span> <span data-ttu-id="fff00-108">Para obtener más información, vea [vinculación en tiempo de ejecución a Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).</span><span class="sxs-lookup"><span data-stu-id="fff00-108">For more information, see [Run-Time Linking to Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).</span></span>

<span data-ttu-id="fff00-109">La API de Servicios de Escritorio remoto permite a las aplicaciones realizar las siguientes tareas en un entorno de Servicios de Escritorio remoto:</span><span class="sxs-lookup"><span data-stu-id="fff00-109">The Remote Desktop Services API enables applications to perform the following tasks in a Remote Desktop Services environment:</span></span>

-   <span data-ttu-id="fff00-110">[Servicios de escritorio remoto administración](terminal-services-administration.md), como la enumeración y la escritorio remoto administración de los servidores de host de sesión de escritorio remoto (host de sesión de RD) (anteriormente conocidos como servidores de Terminal Server) en un dominio o la enumeración y administración de sesiones y procesos en un servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="fff00-110">[Remote Desktop Services Administration](terminal-services-administration.md), such as enumerating and managing Remote Desktop Session Host (RD Session Host) servers (formerly known as terminal servers) in a domain or enumerating and managing sessions and processes on an RD Session Host server.</span></span>
-   <span data-ttu-id="fff00-111">Mejorar las aplicaciones cliente/servidor en un entorno de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="fff00-111">Enhancing client/server applications in a Remote Desktop Services environment.</span></span>
-   <span data-ttu-id="fff00-112">El uso de [servicios de escritorio remoto canales virtuales](terminal-services-virtual-channels.md) para comunicarse entre los módulos de cliente y servidor de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="fff00-112">Using [Remote Desktop Services Virtual Channels](terminal-services-virtual-channels.md) to communicate between client and server modules of an application.</span></span>
-   <span data-ttu-id="fff00-113">[Establecer y recuperar servicios de escritorio remoto información de configuración específica del usuario](terminal-services-user-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="fff00-113">[Setting and retrieving Remote Desktop Services specific user configuration information](terminal-services-user-configuration.md).</span></span>

 

 




