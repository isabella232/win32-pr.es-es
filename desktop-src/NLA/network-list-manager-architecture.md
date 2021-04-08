---
title: Arquitectura del administrador de lista de redes
description: Arquitectura del administrador de lista de redes
ms.assetid: d3d03891-7c61-4f7e-a2e2-ef13353e8688
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a567b103cfd5d9944aa33a799c2cc1bc4b983759
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994585"
---
# <a name="network-list-manager-architecture"></a><span data-ttu-id="247a1-103">Arquitectura del administrador de lista de redes</span><span class="sxs-lookup"><span data-stu-id="247a1-103">Network List Manager Architecture</span></span>

<span data-ttu-id="247a1-104">Network List Manager se ejecuta como un servicio en el contexto de Svchost.exe y se inicia durante el procedimiento de arranque del equipo.</span><span class="sxs-lookup"><span data-stu-id="247a1-104">Network List Manager runs as a service in the context of Svchost.exe and is started during the computer boot procedure.</span></span> <span data-ttu-id="247a1-105">El servicio Administrador de lista de redes mantiene una tabla de redes disponibles y los atributos de red que recuperan las aplicaciones a través de la API del administrador de lista de redes.</span><span class="sxs-lookup"><span data-stu-id="247a1-105">The Network List Manager service maintains a table of available networks and network attributes that are retrieved by applications through the Network List Manager API.</span></span> <span data-ttu-id="247a1-106">Network List Manager proporciona funciones básicas para filtrar y consultar el servicio Administrador de lista de redes para redes específicas y recuperar los atributos de estas redes.</span><span class="sxs-lookup"><span data-stu-id="247a1-106">Network List Manager provides basic functions to filter and query the Network List Manager service for specific networks and retrieve the attributes of these networks.</span></span> <span data-ttu-id="247a1-107">En el diagrama siguiente se muestra la arquitectura del administrador de listas de redes y la interacción entre el servicio Administrador de lista de redes y la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="247a1-107">The following diagram shows the Network List Manager architecture and the interaction between the Network List Manager service and the client application.</span></span>

![diagrama de arquitectura de reconocimiento de redes](images/architecture.png)

 

 




